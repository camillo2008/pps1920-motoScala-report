---
abstract: |
  Il presente documento è un report contenente una descrizione
  dettagliata di tutte le fasi di sviluppo del progetto MotoScala: un
  applicativo, ispirato al gioco arcade Motos, rilasciato da Namco nel
  1985. Questo progetto è il risultato di un lavoro di gruppo svolto ai
  fini del sostenimento dell'esame di Paradigmi di Programmazione e
  Sviluppo.
author:
- |
  Kiade Sara\
  [`sara.kiade@studio.unibo.it`](mailto:sara.kiade@studio.unibo.it)
- |
  Caminati Gyordan\
  [`gyordan.caminati@studio.unibo.it`](mailto:gyordan.caminati@studio.unibo.it)
- |
  Giulianini Luca\
  [`luca.giulianini2@studio.unibo.it`](mailto:luca.giulianini2@studio.unibo.it)
- |
  Ceroni Ruben\
  [`ruben.ceroni@studio.unibo.it`](mailto:ruben.ceroni@studio.unibo.it)
bibliography:
- references.bib
date: October 2020
title:  MOTOSCALA
---

Introduzione
============

L'obiettivo del progetto è quello di **sviluppare** un gioco arcade
ispirato a **Motos**, avendo cura di mantenere un alto grado di
**qualità** non solo nel risultato dell'**implementazione** ma anche in
tutto ciò che riguarda il **processo di sviluppo**. Per questo motivo
tutti i **passaggi** che porteranno al risultato finale verranno
**analizzati** con attenzione e **documentati** in maniera
**dettagliata**.

Il gioco
--------

L'arcade **originale** consiste in un un **campo** bidimensionale sul
quale il giocatore **pilota** una navicella e ha l'obiettivo di
**eliminare** le entità nemiche spingendole **fuori** dal campo,
**senza** essere eliminato a sua volta.

**MotoScala** replicherà gli aspetti principali del gioco originale,
arricchendoli con l'inserimento di nuove **feature**, come il concetto
di **durata vitale** delle entità e il **multiplayer**.

Gli obiettivi
-------------

Durante lo svolgimento del progetto si punterà al raggiungimento di
**obiettivi** riguardanti il **processo di sviluppo**:

-   Rispetto delle **specifiche** non opzionali ed eventualmente
    integrazione di quelle aggiuntive.

-   Utilizzo appropriato di tecniche **avanzate** di **gestione** del
    progetto.

-   Rispetto degli standard di **qualità** introdotti a lezione.

Processo di Sviluppo
====================

In questo capitolo verranno analizzati in dettaglio i processi relativi
alle **metodologie di sviluppo** e **gestione di progetto** utilizzati.
Per ogni processo inoltre, verrà fornita una breve descrizione di come
esso sia stato **implementato** (tools, websites, ecc) e
**automatizzato** (CI).

Metodologia di Sviluppo
-----------------------

Per quanto riguarda la metodologia di sviluppo scelta si è deciso di
optare per un approccio moderno di tipo iterativo. Fra i tanti modelli
presenti abbiamo scelto di mettere in pratica la metodologia **Agile**
basata su `Scrum`. Data l'inesperienza nel campo del project management
abbiamo deciso di non scegliere una figura di **Scrum Master** in modo
da avere un maggiore equilibrio decisionale. È stato invece definito il
ruolo di **Product Owner**, svolto da Luca Giulianini, al quale è stato
affidate le mansioni di **controllo qualità** e **validazione dei
requisiti**.

### Scrum {#subsec:scrum}

##### Sprint {#par:sprint}

Gli **Sprint** hanno durata **settimanale** e, al termine di ognuno di
essi, viene effettuata una **runione** generale di tutto il team al fine
di **valutare i risultati** ottenuti. La riunione funge inoltre da
*strumento di confronto e dialogo* per quanto riguarda eventuali
problemi emersi durante lo stesso Sprint. Una volta conclusa la riunione
viene lasciata la parola al **Product Owner** il quale riassume
brevemente lo stato attuale dello Sprint fornendo una breve
**valutazione** circa la **qualità** dei **deliverables** prodotti e la
loro aderenza ai **requisiti** precedentemente analizzati. Nel caso in
cui vengano rilevate problematiche a livello qualitativo o di
tempistiche, il team procederà a una ridefinizione del **piano di
lavoro** modificando opportunamente la **schedula** in modo da
permettere un recupero graduale.

##### Backlog {#par:backlog}

Lo **Sprint Backlog** viene stilato dal team di settimana in settimana e
alla fine di ogni Sprint, durante la consueta riunione generale, vengono
valutati gli eventuali problemi aggiornando opportunamente il **Product
Backlog**. Nel caso in cui uno Sprint venga completato con successo, il
team procederà a incontrarsi nuovamente al fine di definire la
documentazione relativa alla **nuova iterazione** e quindi il nuovo
Sprint Backlog. Gli **items** del Product Backlog da introdurre nello
Sprint sono **concordati** dall'intero team di sviluppo. Ogni item per
comodità viene scomposto nei suoi **Sprint Tasks** di base e per ognuno
di essi viene attribuito un valore di **effort** concordato dal team.
Infine l'**assegnazione** dei task ai vari componenti del gruppo viene
effettuata seguendo principalmente l'affinità con le **abilità** dei
singoli membri del team.

Gestione di Progetto
--------------------

Come abbiamo visto in [2.1.1](#subsec:scrum){reference-type="ref"
reference="subsec:scrum"} la metodologia di sviluppo utilizzata è
caratterizzata da una grande componente di **interazione** fra i membri
del gruppo. Dato questo presupposto è fondamentale mettere in campo una
serie di **tecnologie** e **strumenti** che permettano di semplificare
questo processo. Al giorno d'oggi il mercato propone una serie di
strumenti estremamente potenti e molti di questi vengono forniti
gratuitamente a studenti universitari. Qui di seguito verranno elencati
i tool utilizzati e verrà fornita una breve descrizione delle loro
peculiarità.

##### Trello

Trello è un tool web di carattere manageriale basato sullo stile a
Kanban. La struttura di una Kanban board è molto semplice:

-   **Colonne:** Rappresentano gli **stadi** di un determinato processo.
    Nella versione più snella il processo segue tre semplici fasi:
    *ToDo, Doing* e *Done*, mentre nell'ambito dello sviluppo software
    questo può introdurre anche le fasi di sviluppo stesse come:
    *review, backlog, doc, ecc*.

-   **Cards:** Gli **items** in una Kanban board sono rappresentati da
    carte. Ogni carta contiene una serie di informazioni relative a un
    **task** come: *durata, effort, ecc*.

-   **Swimlanes:** In alcuni casi una Kanban board può essere integrata
    con il concetto di **Gantt Chart** connettendo così ogni singolo
    **task** a un determinato **membro** del team.

##### Gantt Chart

Il Gantt è molto utile nella fase di **assegnamento** dei vari task,
esso permette infatti di poter fornire una stima temporale per ogni task
permettendo così di avere un controllo totale sulla **schedula**.
Inoltre unire il Gantt a un'approccio Kanban ci ha permesso di calcolare
eventuali **ritardi** relativi ad ogni singolo task.

##### Github Project Management

I **DVCS** negli ultimi anni sono passati dal-l'essere semplici gestori
di codice a veri e propri gestori di progetto. **Github** è stato uno
dei primi a partecipare a questa transizione e ha integrato nel tempo
una serie di tool estremamente interessanti.

-   **Organizzazioni:** In Github c'è la possibilità di creare gruppi
    eterogenei facenti riferimento ad una organizzazione (reale o
    fittizia). Nel nostro caso è stata creata una organizzazione
    chiamata `Unibo-PPS-1920` che va a richiamare un **gruppo fittizio**
    dedicato al corso di Paradigmi di Programmazione e Sviluppo.

-   **Teams:** Una volta definita una organizzazione è possibile creare
    all'inter-no di essa una serie di sottogruppi chiamati **teams**.
    Ogni team idealmente rappresenta uno **Scrum Team** costituito
    all'interno di una organizzazione o azienda con lo scopo di
    **portare a termine un progetto**. Il team dunque idealmente dovrà
    attraversare tutte le fasi di costruzione, partendo da una prima
    fase di presentazione dei membri e arrivando fino alla definizione
    delle **figure chiave** (Scrum Master, Product Owner). Nel nostro
    caso il team è stato nominato `CaminatiCeroniGiulianiniKiade` al
    fine di rispecchiare l'aspetto democratico dello stesso.

-   **Progetto:** I progetti reali sono generalmente proposti
    dall'organizzazione (*Senior Management*) e poi successivamente sono
    assegnati ai vari team. Nel nostro caso abbiamo voluto simulare
    questa situazione assegnando il progetto al team suddetto. Al fine
    di mantenere una corretta separazione di contenuti si è deciso di
    creare due progetti: uno dedicato agli **aspetti di documentazione**
    e l'altro dedicato agli **aspetti** di carattere **implementativo**.
    I progetti sono sincronizzati tra loro attraverso Trello e Github
    Projects.

-   **Projects:** I Github Projects sono entità presenti all'interno
    dell'organiz-zazione e rappresentano una **interfaccia gestionale**
    sui vari progetti gestiti dall'organizzazione stessa. Nel nostro
    caso abbiamo definito un unico **Github Project** nel quale è stata
    implementata una piccola gestione di progetto a **livello
    operativo**. Al progetto infatti, sono delegati i compiti relativi
    alla gestione delle **Issues** e delle **Pull Requests** permettendo
    agli utenti di avere sotto controllo le **azioni** principali svolte
    dal **DVCS**.

##### Telegram

Relativamente agli aspetti di **comunicazione informale** si è optato
per uno strumento di messaggistica estremamente versatile: **Telegram**.
Grazie a Telegram e ai famosi telegram bots è stato possibile avere
aggiornamenti diretti dal DVCS e CI consentendo un maggiore
**controllo** su tutta la fase di **gestione e sviluppo** del progetto.

##### Discord

Discord è stato utilizzato come strumento di **comunicazione**
**semi-formale** `VoIP`. Su Discord è stato possibile chiarire dubbi e
definire al meglio i task assegnati ai vari membri.

##### Teams

Microsoft Teams è una piattaforma di comunicazione e collaborazione
unificata che combina chat di lavoro persistente, teleconferenza,
condivisione di contenuti. Come si può notare da questa definizione
Teams è uno strumento di **comunicazione** estremamente **formale** ed è
stato dunque utilizzato come **host principale** per le **riunioni
Scrum**.

##### Notion

Notion è un'applicazione a tutto tondo che fornisce supporto per quanto
riguarda **gestione di task** e definizione di **ToDo lists**. È molto
utile nella fase di **definizione** e **decomposizione** del **Product
Backlog**.

Continuous Integration e Automatizzazione
-----------------------------------------

Gli aspetti di **automatizzazione** di processi ripetitivi sono
estremamente importanti al fine di risparmiare tempo e migliorare la
gestione di progetto. Al giorno d'oggi sempre più servizi forniscono
supporti di continuous integration e gran parte di essi garantiscono
all'utente un **elevato** grado di **libertà** per quanto riguarda gli
aspetti di progetto da automatizzare.

Nel nostro caso approcci di automatizzazione sono stati impiegati per
fornire supporto a due ambiti fondamentali:

##### Gestione di Progetto

Gran parte degli aspetti del project management sono legati al concetto
di controllo sulle **fasi di progetto** (Planning, Scoping ecc). Una
delle problematiche fondamentali risiede in un **accesso fruibile** e
**facilitato** da parte del team allo stato attuale del progetto. Grazie
alla CI è possibile notificare l'intero team sullo stato attuale del
progetto garantendo così maggiore **consistenza** e **consapevolezza**.

###### Tool utilizzati

Gran parte dei tool di gestione utilizzati forniscono **API** che
possono essere interrogate da servizi esterni. Questo è il caso di
Trello che fonisce un'ottima integrazione con **IFTTT** e di conseguenza
con svariati servizi collegabili a quest'ultimo. Nel nostro caso è stato
utilizzato IFTTT in accoppiata a **Telegram** al fine di fornire
**notifiche real-time** sullo stato di progetto.

##### Gestione di Sviluppo

La CI esprime il suo massimo potenziale nella **fase di sviluppo**. In
questo caso le funzioni fornite sono state espanse permettendo di
integrare il concetto di **notifica** a fronte di azioni effettuate dai
membri del team.

###### Tool utilizzati

Per quanto riguarda la gestione di sviluppo ci si è affidati ai classici
sistemi di CI integrati con il DVCS utilizzato. Nella nostra situazione
è stato scelto il sistema **Travis** poiché garantisce un'ottima
integrazione con il DVCS Github e permette inoltre di personalizzare a
fondo le **pipeline di integrazione**. Travis è stato utilizzato come
strumento di CI in due casistiche differenti:

-   **Relazione di Progetto:** Travis è stato associato al repository
    contenente i sorgenti LaTeX della relazione. La configurazione è
    stata scritta definendo due **stage condizionali** e uno **stage di
    deploy**:

    1.  ***Telegram notification:*** dedicato all'invio di **notifiche**
        a fronte di azioni di tipo **push** (non taggate) da parte dei
        membri del team.

    2.  ***Latex build:*** dedicato alla compilazione del codice
        LaTeX mediante un'opportuna immagine **Docker** di `TexLive`

    3.  ***Deploy:*** dedicato al **deploy su Github** del pdf compilato
        precedentemente da `Latex build`. È stato infine definito un
        piccolo script che si occupa dell'invio di una **notifica
        Telegram** al team contenente il **link al pdf** rilasciato.

-   **Progetto Principale:** Travis è stato utilizzato anche nel
    progetto principale, definendo due stage: **Check** e **Deploy**.

    1.  ***Check:*** durante questa fase viene chiamato il *Check* di
        **Gradle** e vengono generati **report** e **build**. Viene
        inoltre creata la **dashboard** che consiste in un file **html**
        che riunisce **tutti** i report.

    2.  ***Deploy:*** il deploy viene eseguito solo nel caso in cui si
        faccia una push su un **branch** con **tag**. **Prima** di esso
        vengono eseguite le seguenti operazioni:

        1.  *Assemble:* viene chiamata la `assemble` di **Gradle**, che
            si occupa di creare i file `.jar` che devono essere caricati
            sul **repository** GitHub.

        2.  *Scaladoc:* viene generata la **Scaladoc**, che viene
            mantenuta in **locale**.

        3.  *Report:* **docs** e **report** vengono copiati all'interno
            di una cartella `report` che conterrà un file `index.html`
            che li riunirà. I **report** comprendono: i risultati dei
            **test**, le percentuali di **coverage** e l'albero delle
            **dipendenze**.

        **Successivamente** si passa al vero e proprio stage di Deploy
        che effettua la **release** di tutti i file `.jar` creati dal
        task `assemble` di Gradle su GitHub e procede a **linkare** la
        **Dashboard** creata nella cartella report con le **pages** di
        GitHub.

    Nella configurazione di **Travis** è stato sfruttato **Gradle**. La
    versione base (3.4.1) è stata arricchita con diversi **plugin**:

    -   ***Java:*** aggiunge la possibilità di **compilare** e
        **testare** sorgenti Java

    -   ***Java Library:*** espande il plugin Java fornendo delle
        **conoscenze specifiche** riguardanti le librerie.

    -   ***Scala:*** un'estensione del plugin Java per la
        **compilazione** e il **testing** dei sorgenti **Scala**

    -   ***Jacoco:*** per la creazione del report sulla **coverage** dei
        sorgenti **Scala**; utilizzato in sostituzione del più adatto
        plugin **Scoverage** che non è però compatibile con Scala 2.13
        su Gradle.

    -   ***Application:*** facilita la creazione di un **eseguibile**
        JVM, rendendo più semplice l'esecuzione dell'applicazione in
        **locale** durante la fase di sviluppo.

    -   ***Project Report:*** fornisce al progetto dei **task** per la
        generazione delle informazioni relative al progetto. Di questi è
        stato utilizzato il **dependency task**, per la generazione
        dell'albero delle dipendenze.

    -   ***Build Dashboard:*** viene utilizzato per la generazione di un
        singolo file `.html` che verrà poi utilizzato per linkare i
        **report** e la **scaladoc**.

    -   ***Shadow:*** serve per collassare tutte le **dipendenze** del
        progetto in un singolo `.jar`

    -   ***Sensitive Semantic Versioning:*** viene utilizzato per fare
        **semantic versioning** in modo che ad ogni `jar` prodotto venga
        assegnato lo **stesso nome** del tag della relativa **release**
        fornito da Git.

Analisi dei Requisiti
=====================

In questa fase sono stati individuati i **requisiti** del sistema,
partendo da una descrizione di **alto livello**, ottenuta mettendosi nei
panni di un committente, e procedendo con un **raffinamento** che ha
portato alla definizione di requisiti più **specifici**, **chiari** e
**strutturati**.

Requisiti di Business
---------------------

Si definiscono di seguito i requisiti che dovrà avere il sistema visti
ad un **alto livello** di astrazione e le **aspettative** di un
potenziale committente sul risultato finale.

-   Il sistema dovrà essere una replica del gioco arcade **Motos** (by
    Namco).

    -   Il gioco si svolge all'interno di un **piano** immerso nello
        spazio, che rappresenta il campo di gioco. All'interno del piano
        si muovono delle **navicelle**.

    -   Il giocatore ha il **comando** di una delle navicelle e ha
        l'obiettivo di spingere tutte le navicelle nemiche **fuori** dal
        campo attraverso **collisioni** che generano urti elastici.

    -   Sul campo sono presenti altre entità, al di fuori delle
        navicelle, che permettono all'utente di ottenere dei
        **power-up**.

    -   Il giocatore ottiene una **vittoria** se non sono più presenti
        navicelle nemiche sull'arena e va incontro alla **sconfitta** se
        esce **fuori** dalla griglia per distrazione o perché spinto da
        un'altra navicella.

-   Il sistema dovrà mettere a disposizione un **menu** che permetta:

    -   La selezione della **difficoltà** di gioco

    -   La possibilità di modificare il **volume** e
        **attivare/disattivare** la musica di sottofondo

    -   La visualizzazione della lista dei **punteggi migliori**
        ottenuti nelle partite precedenti.

    -   La scelta della **modalità** di gioco

-   Il sistema dovrà permettere all'utente di usufruire di un **gioco
    piacevole**, senza interruzioni involontarie, ritardi nelle azioni e
    altri elementi che possano rovinare l'esperienza di gioco.

Requisiti Utente
----------------

Per l'utente dovrà essere possibile svolgere le seguenti attività:

-   Interagire con il sistema tramite un'**interfaccia grafica**
    intuitiva;

-   **Giocare:**

    -   Avviare una sessione di gioco **single-player**;

    -   Avviare una sessione di gioco **multi-player**

        -   selezionare un server a cui connettersi;

    -   Scegliere ad ogni partita la **difficoltà** di gioco;

    -   **Giocare** attivamente inviando al sistema appositi
        **comandi**;

-   Accedere alle **impostazioni** e modificarle;

-   Visualizzare le **statistiche** di gioco.

![Diagramma dei casi d'uso che evidenzia le operazioni che dovranno
poter essere svolte
dall'utente[]{label="fig:figure1"}](Diagrams/useCaseDiagram.pdf){#fig:figure1
width="0.80\\columnwidth"}

Requisiti Funzionali
--------------------

Si elencano i requisiti funzionali per ognuno dei seguenti
macro-componenti:

-   **Gioco**

-   **Multiplayer**

-   **Impostazioni**

-   **Statistiche**

### Gioco

Il gioco deve rispecchiare le meccaniche di base dell'originale. Sono
presenti diverse entità, ognuna con caratteristiche specifiche:

-   **Navicella**: la navicella pilotata dal giocatore dovrà:

    -   **Spostarsi** all'interno del campo di gioco 2D in base agli
        **input** ricevuti da tastiera

    -   Avere una **massa** che influisce sull'**urto** con gli altri
        elementi in campo

    -   Potersi **scontrare** con le altre navicelle generando un urto
        elastico che spinge entrambi e che **non** tiene conto della
        **velocità** (come nel gioco originale)

    -   (opzionale) Avere una **durata vitale** che si decrementa ad
        ogni urto e il quale esaurimento comporta l'**eliminazione**.

-   **Navicella nemica**: le navicelle nemiche in campo, controllate dal
    sistema, dovranno:

    -   Muoversi in base a **regole predefinite**.

    -   Avere l'obiettivo di **eliminare** la navicella del giocatore

    -   (opzionale) Avere una **durata vitale** il quale esaurimento
        comporta l'eliminazione.

    -   Seguire delle **strategie**. Un esempio di strategia potrebbe
        essere accerchiare la navicella dell'utente per spingerla fuori
        dal campo di gioco.

-   **Entità power-up**(opzionale): sul campo di gioco dovranno
    comparire degli elementi che tramite un'**interazione** con la
    navicella pilotata dal giocatore potranno fornirle dei **power-up**.

    -   **Aumento della massa**: la massa influisce sull'urto;
        aumentandola il giocatore ottiene il vantaggio di prevalere in
        caso di collisione, spingendo l'oggetto più lontano.

    -   **Aumento della velocità**: la velocità viene ignorata nel
        calcolo della spinta generata da una collisione, tuttavia il suo
        incremento può essere utile per sfuggire ai nemici più lenti.

    -   **Vita aggiuntiva**: permette alla navicella dell'utente di
        guadagnare un tentativo in più in caso di sconfitta.

    -   **Rimozione dei power-up**: reimposta la massa e la velocità a
        quelle di default.

    -   **Incremento del punteggio**: è contenuto in degli elementi che
        possono essere spinti fuori dal campo come le navicelle e
        assegnano un punteggio se eliminati dal campo di gioco.

-   **Giocatore**: il giocatore è l'entità principale, intorno alla
    quale ruotano le dinamiche di gioco.

    -   Il giocatore può **controllare** una navicella

    -   Accumula **punti** eliminando le altre navicelle e,
        opzionalmente, interagendo con le entità power-up

    -   Ha un determinato numero di **vite**, che rappresentano il
        numero di volte in cui si può riprendere il gioco dopo essere
        stati eliminati, senza che venga fatto un **reset** dello stato

    -   Ha l'obiettivo di **eliminare** le navicelle nemiche

-   **Arena di gioco**: è lo **spazio** su cui si muovono gli elementi
    del gioco.

    -   Si compone di un piano **bidimensionale** suddiviso da una
        **griglia** che rappresenta le *piastrelle* dell'arena.

    -   (opzionale) L'arena può presentare al suo interno delle
        *piastrelle* **mancanti** che non fanno parte del campo di gioco
        e che comportano quindi l'eliminazione delle navicelle che le
        attraversano.

    -   Ha dei **bordi** ben definiti che la delimitano dall'area
        circostante e che se attraversati da una navicella ne comportano
        l'eliminazione.

### Multiplayer

Opzionalmente il gioco sarà fruibile anche in modalità **Multiplayer**.
La modalità Multiplayer dovrà permettere a **più giocatori** di
interagire all'interno della **stessa arena**.\
Il multiplayer potrà essere di **due tipi**:

-   **Cooperativo**: i giocatori sono **alleati** e hanno l'obiettivo di
    eliminare le navicelle pilotate dal sistema.

    -   Le condizioni di **vittoria** saranno:

        -   **Eliminazione** delle navicelle **nemiche**

        -   **Sopravvivenza** di almeno una delle navicelle **alleate**.

    -   I giocatori andranno incontro alla **sconfitta** se:

        -   Sul campo rimangono **solo** le navicelle nemiche

-   **Competitivo**: i giocatori sono **avversari** e ognuno di loro ha
    l'obiettivo di rimanere l'**unica** navicella sul campo.

    -   Le condizioni di **vittoria** saranno:

        -   **Eliminazione** delle navicelle pilotate dal **sistema**.

        -   **Eliminazione** delle navicelle pilotate da altri
            **giocatori**.

    -   I giocatori andranno incontro alla **sconfitta** se:

        -   La navicella da loro pilotata **esce** dal campo di gioco

        -   (opzionale) I **punti vita** della loro navicella arrivano a
            **zero** per aver subito danni

### Impostazioni

Deve essere prevista la possibilità di gestire le impostazioni che
riguardano l'ambiente dentro il quale si trova il gioco.\
Le **impostazioni** disponibili saranno le seguenti:

-   **Musica**: deve essere possibile **attivare** o **disattivare** la
    musica di sottofondo.

-   **Volume**: l'utente deve poter **regolare** il volume della musica
    di sottofondo.

### Statistiche

Dovranno essere disponibili delle statistiche, basate sulle **partite
precedenti** in modalità single player. Le statistiche dovranno mostrare
i **record** raggiunti dai giocatori; in particolare verranno
visualizzate le seguenti informazioni:

-   **Posizione** in classifica.

-   **Username** dell'utente che detiene quel record.

-   **Punteggio** totalizzato in quella circostanza.

Alla vittoria da parte di un giocatore, nel caso in cui il suo punteggio
gli consentisse il piazzamento in classifica, avrà l'opzione di inserire
il suo nome utente, al fine di registrare il punteggio raggiunto in
classifica.

Requisiti non Funzionali
------------------------

Il sistema dovrà rispettare alcuni requisiti non funzionali che ne
determineranno la **qualità**:

-   **Reattività**: l'utente non deve percepire **ritardi** tra l'invio
    di un comando e l'esecuzione dello stesso da parte del gioco, il
    feedback grafico deve essere immediato.

-   **Prestazioni**: devono essere tenute particolarmente in
    considerazione le **performance** affinché il gioco risulti fluido.

-   **Scalabilità**: in caso venga gestita la modalità multiplayer, il
    gioco deve essere **scalabile** per poter supportare la gestione più
    client.

-   **Fault tollerance**: la **gestione degli errori** deve essere
    adeguatamente implementata affinché le interruzioni involontarie del
    gioco avvengano solo in casi particolari.

Requisiti Implementativi
------------------------

Si definiscono i **constraint** a livello di implementazione che sarà
necessario rispettare nella realizzazione del progetto.

### Scala

Il gioco deve essere realizzato utilizzando un linguaggio funzionale
**JVM-based**, preferibilmente il linguaggio **Scala** che è stato
trattato in maniera approfondita durante il corso di Paradigmi di
Programmazione e Sviluppo.

Design Architetturale
=====================

Dopo un'attenta analisi dei requisiti, si è proceduto con la fase di
**design architetturale** che si è sviluppata in più passi, partendo
dalla definizione ad alto livello di un'architettura generale e
**raffinandola** gradualmente.

Architettura Generale
---------------------

Il primo passo per quanto riguarda l'aspetto della **progettazione** è
consistito nella ricerca dei pattern più adatti da applicare,
nell'individuazione dei principali componenti dell'**architettura
generale**, e nella definizione dei modi in cui essi interagiscono.

La seguente immagine (fig:
[4.1](#fig:architectureClassDiagram){reference-type="ref"
reference="fig:architectureClassDiagram"}) definisce il **core**
dell'architettura generale che è stato successivamente **ampliato** per
gestire anche la parte di architettura **client-server** necessaria alla
realizzazione della modalità **multiplayer**.

![Diagramma raffigurante le entità principali dell'architettura e le
loro interazioni ad un alto livello di
astrazione.[]{label="fig:architectureClassDiagram"}](plantuml/rendered/classDiagrams/architectureClassDiagram.pdf){#fig:architectureClassDiagram
width="0.80\\columnwidth"}

Spiegazione breve delle entità in gioco

-   **View:** ha l'obbiettivo di fornire all'utente una **schermata**
    intuitiva per il controllo del gioco.

-   **Controller:** rappresenta il punto di **snodo** per la gestione
    della logica principale dell'applicazione. La sua funzione primaria
    è quella di gestire la **comunicazione** tra: View, ECS, e
    GameEngine.

-   **ECS:** è un aggregato di **sistemi**, **entità** e **componenti**
    che esprimono e contengono in maniera astratta la logica di gioco.

-   **GameEngine:** rappresenta il cuore del gioco; incapsula il flusso
    di controllo principale e tramite ECS calcola continuamente il nuovo
    ambiente.

Pattern Architetturali Utilizzati
---------------------------------

### ECS

Trattandosi dello sviluppo di un videogioco, per il quale è necessario
creare un motore di gioco, è stato scelto di utilizzare il pattern
architetturale **Entity-Component-System** (ECS). Questo pattern è
largamente utilizzato nello svi-luppo di videogiochi per motivi di
performance e per la sua estensibilità e manutenibilità.

ECS si compone di tre parti principali:

-   **Entità:** rappresentano gli elementi in gioco, ad esempio Bumper
    car, PowerUp o Enemy. Ad ogni entità vengono associati uno o più
    componenti.

-   **Componenti:** sono delle proprietà che vengono possedute da una o
    più entità e ne rappresentano lo stato. Esempi di possibili
    componenti sono direzione o posizione.

-   **Sistemi:** definiscono dei comportamenti necessari a gestire dei
    sottoinsiemi della logica di gioco. Gestiscono le interazioni tra le
    entità agendo sui componenti associati ad esse.

### MVC

Il pattern **MVC** rappresenta uno standard per quanto riguarda il
**design** di applicazioni *robuste* ed *estendibili*. Nel nostro caso
il pattern è stato utilizzato in concomitanza con il pattern **ECS**
permettendo così di raggiungere una maggiore **separazione dei
concetti**. L'MVC progettato si compone dei seguenti moduli:

-   **Model:** All'interno del nostro applicativo esistono due tipi di
    modello:

    -   **Game Model:** Il **modello di gioco** rappresenta l'insieme
        delle **strutture dati** utili per modellare il gameplay. Nel
        nostro caso questo compito è stato catturato interamente dal
        **pattern ECS**.

    -   **Application Logic Model:** Il modello della **logica
        applicativa** riguarda tutti i dati utili al **corretto
        funzionamento** dell'applica-zione (Impostazioni, Livelli, Dati
        utente, ecc).

-   **View:** L'interfaccia grafica si configura come un **punto di
    intersezione** fra **ECS** e **MVC** per quanto riguarda gli aspetti
    dell'interazione utente. Essa si compone di due tipologie di
    schermate:

    -   **Game Screen:** È una schermata di gioco connessa interamente
        al modulo ECS. Essa ha come scopo principale quello di mostrare
        gli **aggiornamenti di gioco** e acquisire i **comandi** da
        parte dell'utente.

    -   **Application Screen:** È istanza di una semplice **schermata di
        presentazione**. Lo scopo di una application screen consiste
        essenzialmente nel garantire all'utente una buona **usabilità**
        e **interazione** col sistema, incapsulando le informazioni di
        modello in una **visualizzazione fruibile**.

-   **Controller:** Gestisce le **interazioni** fra i principali moduli
    dell'architet-tura e mette a disposizione una serie di
    **funzionalità** relative alla **gestione delle risorse**.

### Client-Server {#subsec:client_server}

Un'architettura di tipo client-server si è resa necessaria per poter
gestire la modalità di gioco **multiplayer**. Il sistema deve infatti
permettere ad un utente di **ospitare** una partita assumendo il ruolo
di `server` e ad altri utenti di **partecipare** ricoprendo il ruolo di
`client`.

#### Scelta del paradigma

Per gestire l'interazione tra Client e Server si è ritenuto adatto
l'utilizzo del **paradigma ad attori** applicato mediante la
modellazione di un attore `Server` e un attore `Client` che
interagiscono tramite scambio di **messaggi**.

#### Distribuito vs centralizzato

Quando ci si cimenta nella progettazione di un sistema che si
interfaccerà in **rete** è necessario definire quale **approccio**
utilizzare. Essenzialmente vi sono due strade percorribili: una basata
su uno schema **centralizzato** mentre l'altra basata su uno schema
**peer-to-peer**.

-   Approccio centralizzato

    -   Semplicità

    -   Reattività

    -   Consistenza

    -   Single Point of Failure

-   Approccio distribuito

    -   Fault-tolerance

    -   Carico suddiviso

    -   Modulare

    -   Complesso

    -   Incline all'inconsistenza

Si è preferito utilizzare un approccio centralizzato anziché distribuito
perché, data la natura del sistema che è da realizzare, si è ritenuto
che una scelta diversa avrebbe portato, a fronte di un maggiore sforzo
progettuale e implementativo, a dei risultati peggiori in termini di
performance, reattività e consistenza.

Come mostrato dalla figura
[4.2](#fig:clientServerComponentDiagram){reference-type="ref"
reference="fig:clientServerComponentDiagram"} il sistema è stato
progettato in modo da poter estendere l'architettura core per il
multiplayer, \"staccando\" l'engine del client e sostituendolo con
l'attore client che poi comunicherà con l'attore server, che si
interfaccia direttamente con il server.

![Diagramma raffigurante gli attori di tipo Client e Server e le loro
interazioni.[]{label="fig:clientServerComponentDiagram"}](plantuml/rendered/componentDiagrams/clientServerComponentDiagram.pdf){#fig:clientServerComponentDiagram
width="0.70\\columnwidth"}

Scelte Tecnologiche Cruciali
----------------------------

### Akka

Per l'implementazione del paradigma ad attori sì e scelto di utilizzare
**Akka** [@akkaSite akkaSite] come layer di **comunicazione** nello
sviluppo del multiplayer. Akka garantisce un'ottima **scalabilità** e un
buon livello di **astrazione**, che permette di gestire la comunicazione
in maniera più trasparente rispetto ai classici metodi basati sulle
**socket**. Il modello **Client-Server** basato su Akka risulta così di
facile **implementazione**.

Inoltre, il fatto che Akka sia implementato in **Scala** rende più
semplice e naturale l'utilizzo del framework.

Design di Dettaglio
===================

ECS {#sec:ecs_design}
---

Tradizionalmente nello sviluppo di applicazioni si tende ad utilizzare
un approccio di design basato sull'**ereditarietà**. Questa scelta,
attraverso la crea-zione di **gerarchie semantiche** precise (Persona
-\> Studente), permette generalmente di ottenere implementazioni più
**robuste** e **strutturate**. Nell'ambito dei videogiochi, dove è
necessario un elevato grado di **flessibilità**, queste gerarchie
strutturate possono risultare **costrittive**. Al fine di eliminare
questa problematica nel tempo ci si è diretti verso approcci basati
maggiormente sulla **composizione**. Il pattern architetturale `ECS`
nasce proprio seguendo questa filosofia di pensiero.

### Il pattern {#subsec:ecs_pattern}

Il modello **ECS** è costituito da tre parti fondamentali: entità,
componenti e sistemi.

-   **Entity:** costituisce una **rappresentazione astratta** di una
    entità in gioco. Essa è caratterizzata in un dato momento da una
    serie di proprietà che possono *variare liberamente*.
    *Concettualmente*, pur avendo un aspetto **dinamico** dal punto di
    vista delle proprietà ad essa associate, un'entità deve rimanere
    **fedele** alla sua natura.

    Per esempio un'entità nemica manterrà sempre la sua natura avversa
    al giocatore, pur avendo la possibilità di *modificare le sue
    proprietà*.

-   **Component:** le proprietà associate all'entità prendono il nome di
    **componenti**. Essi sono la vera **componente modulare** di ECS
    poiché possono essere **aggregati** ad ogni entità in modo
    **dinamico**. La loro composizione costituisce lo **stato**
    dell'entità a cui sono associati.

-   **System:** il sistema rappresenta il vero aspetto **funzionale** di
    ECS poiché costituisce un *modulo* dedicato unicamente alla gestione
    del **comportamento** delle singole entità. Il punto di forza del
    pattern sta nel fatto che ogni **sistema agisce** su una serie di
    **componenti** (in base alla tipologia), di conseguenza nel momento
    in cui un componente verrà rimosso da un'entità quest'ultima vedrà
    **modificato** il proprio comportamento.

### Approcci di design

Come visto in precedenza in
[5.1.1](#subsec:ecs_pattern){reference-type="ref"
reference="subsec:ecs_pattern"}, l'idea alla base di ECS è molto
semplice, tuttavia durante il processo di **concretizzazione** alcuni
aspetti concettuali vengono realizzati in modo leggermente diverso per
*esigenze di carattere implementativo* (performance, cache, ecc). Dal
punto di vista progettuale esistono diversi **approcci possibili**:

-   **Approccio OOP:** questa tipologia di approccio riprende l'idea che
    sta alla base della **programmazione ad oggetti**; in particolare
    viene promosso il concetto secondo il quale ogni oggetto possiede al
    proprio interno uno **stato** e un **comportamento**. Un ECS di tipo
    OOP sarà caratterizzato da entità che **contengono** i propri
    **componenti** e si occupano della loro **gestione**.

-   **Approccio Data-Driven:** in questo caso stato e comportamento
    vengono mantenuti in **moduli dedicati** promuovendo una maggiore
    **separazione dei concetti**. L'ECS in questo caso sarà
    caratterizzato da **moduli di gestione** ai quali saranno delegati
    il **controllo** e la **connessione** di entità e componenti.

##### Alcune considerazioni di basso livello:

Nella definizione del pattern ECS ogni sistema si occupa di gestire
solamente uno o più componenti, **aggiornandoli** in blocco
contemporaneamente.

Un approccio più OOP consisterebbe nel modellare *ogni entità come un
oggetto* che deve implementare una sotto-interfaccia diversa in base al
tipo, ereditando, di conseguenza, i metodi per l'aggiornamento. Questo
causa **problemi di performance** all'aumentare delle entità da gestire,
poiché ad ogni aggiornamento verrebbe caricato in **cache** l'intero
oggetto aumentando così la **latenza** relativa alla fase di loading.
Ciò comporta un **degradamento** importante delle **performance**.

### Design Proposto

L'analisi delle opzioni possibili e del loro sviluppo ha portato a
scegliere un approccio data-driven dato che garantisce nel complesso una
maggiore **estendibilità** e **performance** migliori. L'approccio
scelto inoltre si **integra** molto bene con il **paradigma funzionale**
poiché permette di sfruttare al meglio le caratteristiche di
quest'ultimo.

Il design finale ottenuto è quello raffigurato in
[5.1](#fig:ECS){reference-type="ref" reference="fig:ECS"}.

![Diagramma di classe rappresentante il design
proposto.[]{label="fig:ECS"}](drawio/ECS/ECS.pdf){#fig:ECS
width="0.99\\columnwidth"}

Come si evince dal diagramma si è scelto di utilizzare una **struttura
basata su gestori** (`Manager`) ognuno responsabile di un particolare
aspetto di ECS. Inoltre è stato introdotto un **punto di snodo**
(`Coordinator`) con il compito di **coordinare** i vari gestori. Di
seguito verranno presentati i principali moduli presenti all'interno del
diagramma:

-   **Core ECS:**

    -   **Entity:** rappresenta il concetto di entità classico di ECS.
        Nel nostro caso un'entità è rappresentata dalla propria
        **istanza di tipo** (che ne descrive la natura) e un
        **identificatore**.

    -   **Component:** rappresenta in toto il concetto di componente di
        ECS.

    -   **System:** costituisce un **modulo passivo** di gestione di
        entità che viene aggiornato dall'esterno (`update()`). Ogni
        sistema è inoltre caratterizzato da una `Signature` che
        corrisponde ad un **insieme di componenti** gestiti.

-   **Manager:**

    -   **Entity Manager:** modulo dedicato alla gestione delle entità
        di gioco. Consiste in un **accentratore** per tutte le
        **istanze** di entità e si occupa del loro **inserimento** e
        **rimozione**.

    -   **Component Manager:** tiene traccia delle **associazioni** fra
        **entità** e **componenti** e gestisce l'**aggiunta** e
        **rimozione** di questi ultimi.

    -   **System Manager:** costituisce un aggregatore di sistemi e ha
        lo scopo di **mantenere coerenti** i legami fra sistema, entità
        e componente in base alla **signature del sistema**.

-   **Coordinator:** contiene la logica core di tutto l'ECS e ha lo
    scopo fondamentale di **coordinare i manager** **accentrando** le
    operazioni da essi fornite.

### Funzionamento

Introdotto il design di dettaglio relativo ad ECS è necessario definirne
il **funzionamento** evidenziando le interazioni.

![Diagramma di sequenza che mostra le varie interazioni fra gli elementi
di
design.[]{label="fig:sequenceECS"}](plantuml/rendered/sequenceDiagrams/sequenceECS.pdf){#fig:sequenceECS
width="0.90\\columnwidth"}

Il diagramma in figura [5.2](#fig:sequenceECS){reference-type="ref"
reference="fig:sequenceECS"} mostra le interazioni principali fra gli
elementi in gioco. I passi fondamentali che vengono mostrati possono
essere riassunti in pochi macro step:

1.  **Registrazione dei componenti:** un componente prima poter essere
    utilizzato deve essere **registrato** al `ComponentManager` in modo
    da **verificare** che non si utilizzino **componenti diversi** a
    runtime.

2.  **Registrazione dei sistemi:** successivamente è possibile
    registrare sistemi. La registrazione è molto semplice e consiste
    nell'assegnazione di una `Signature` al sistema. Una `Signature` non
    è altro che una **lista di tipi di componente** che definiscono la
    **natura del sistema**. Grazie a questo espediente è possibile
    delegare un sistema alla **gestione delle entità** a lui
    **compatibili**.

3.  **Creazione di entità:** in qualsiasi momento è possibile creare
    un'entità la cui **istanza** verrà conservata all'interno
    dell'`EntityManager`. È importante sottolineare che in questo caso
    l'entità non è ancora gestita da **nessun sistema** poiché **non
    possiede** componenti associati.

4.  **Aggiunta di componenti ad entità:** una volta che viene
    **associato** un componente ad una entità, l'entità potrà essere
    **assegnata** ai **sistemi compatibili** e quindi gestita.

Mediator {#sec:mediator_design}
--------

Dopo un attento studio delle **specifiche** sviluppate nella fase di
analisi è emerso un importante **problema di interazione** fra alcuni
**componenti cardine**. Come è stato ribadito in
[4.2.3](#subsec:client_server){reference-type="ref"
reference="subsec:client_server"} il design è stato sviluppato cercando
di tenere conto dei principali **requisiti di qualità** e **buona
progettazione**. Questo grado di **estendibilità** e
**modularizzazione** si è esplicitato nella defini-zione di una
architettura (`Core`) **espandibile a richiesta** verso un modello
**client-server** ad **attori** (`Core + Actor`).

Mantenere un **core unico** e **polifunzionale** non è semplice ed è
necessario ridefinire gli elementi mobili utilizzando il cosidetto
`loose coupling`.

### Il problema

Nell'architettura core definita in fase di progettazione il problema
risiede essenzialmente nella gestione del passaggio da **single-player**
game a **multiplayer**.

##### Single-player:

Nella versione single-player il sistema di gioco si appoggia sul
cosiddetto `GameEngine` il quale è in grado di **calcolare autonomamente
gli aggiornamenti** da inviare alla/e schermata/e di gioco.

##### Multiplayer:

Nel caso multiplayer esiste un **server unico** a cui sono collegati una
serie di **client**. Il server agisce da **leader** poiché, possedendo
un `GameEngine` proprio, è in grado di calcolare gli **aggiornamenti di
gioco** a fronte di **input propri** e **dei client**. I client, al fine
di promuovere **semplicità**, sono stati concepiti come **architetture
core** private del motore di calcolo `GameEngine`. Essi in poche parole
si presentano come **attori passivi** che **acquisiscono aggiornamenti**
dal server e li mostrano all'utente attraverso una **interfaccia
grafica**.

Un approccio di questo tipo è molto utile poiché permette di poter
utilizzare il server per giocare **ospitando contemporaneamente la
partita in corso**. Inoltre promuove **leggerezza** e **riusabilità**
dato che i client devono mostrare le **stesse informazioni** che il
server produrrebbe per sé stesso in modalità single-player.

##### Da Single-player a Multiplayer:

Il problema, come abbiamo detto, si presenta nel passaggio dalla
modalità **single-player** a quella **multiplayer**. Nel caso di un
passaggio a **server-mode** il sistema dovrà mantenere il core intatto
ma dovrà aver cura di **inviare gli aggiornamenti** non solo
all'**interfaccia locale** ma anche all'**attore server** (il quale
effettuerà un broadcast ai client). Il passaggio a **client-mode** è
ancora più delicato; in questo caso, infatti, sarà necessario spegnere
il modulo `GameEngine` **dirottando i flussi di informazione** verso il
**client-actor**.

### La soluzione {#subsec:mediator_solution}

Al fine di definire una soluzione valida ci si è appoggiati su un
pattern di design di tipo comportamentale, il **pattern Mediator**. Il
pattern consiste nella definizione di un **modulo** esterno a tutti gli
altri il cui scopo consiste essenzialmente nella **mediazione e
ridirezionamento dei flussi** di dati.

Nel nostro caso il Mediator ha lo scopo principe di **mediare le
interazioni** fra quattro componenti fondamentali:

-   **Schermata di gioco:** Deve essere in grado di inviare comandi al
    **proprio** `GameEngine` (single-player) oppure al `GameEngine`
    **del server** (multiplayer).

-   **Engine:** Riceve i comandi dal proprio `GameScreen`
    (single-player) o dai `GameScreen` dei client e li elabora
    producendo un **nuovo aggiornamento**.

-   **Attore Client:** Può essere concepito come un `Core` munito solo
    di un unico `GameScreen`.

-   **Attore Server:** Può essere concepito come un `Core` agganciato a
    un numero di `GameScreen` variabile.

Al fine di gestire al meglio le interazioni è stato scelto di
implementare un **approccio basato su eventi** che è stato poi pensato
in **due versioni molto simili**:

-   **Mediator Handler:** Il **Mediator** è stato progettato sfruttando
    il **pattern ad handler** basato su **eventi**.

-   **Mediator Observer:** Il **Mediator** è stato progettato sfruttando
    il **pattern observer ad eventi**.

Come vediamo in figura [5.3](#fig:mediatorHandler){reference-type="ref"
reference="fig:mediatorHandler"} la prima scelta porta come principale
vantaggio l'ottenimento di **performance migliori** poiché ogni handler
rappresenta del **codice associato ad un evento immediatamente
eseguibile**. A questo però si aggiungono una **serie di problematiche**
(vedi
[6.1.1.2.1](#subsubsec:mediator_handler_problem){reference-type="ref"
reference="subsubsec:mediator_handler_problem"}) che hanno portato a
rivedere la soluzione proposta dirigendosi verso un'altra soluzione.

![Design del Mediator basato su
handlers.[]{label="fig:mediatorHandler"}](drawio/mediator/mediatorHandler.pdf){#fig:mediatorHandler
width="0.99\\columnwidth"}

La versione basata su handler è stata quindi rivista in un **approccio**
maggiormente **strutturato** incentrato principalmente sul **Pattern
Observer ad eventi**. (fig:
[5.4](#fig:mediatorObserver){reference-type="ref"
reference="fig:mediatorObserver"}).

![Design del Mediator basato su
observer.[]{label="fig:mediatorObserver"}](drawio/mediator/mediatorObserver.pdf){#fig:mediatorObserver
width="0.99\\columnwidth"}

### Funzionamento

La presenza del **`Mediator`** gioca un ruolo fondamentale nel **riuso**
del codice perché, come approfondito in
[5.2.2](#subsec:mediator_solution){reference-type="ref"
reference="subsec:mediator_solution"} permette di **passare in maniera
semplice** dalla modalità single-player a quella multi-player e
viceversa.

Il diagramma di **sequenza**, raffigurato in
[5.5](#fig:sequenceMediator){reference-type="ref"
reference="fig:sequenceMediator"} mostra le dinamiche delle
**interazioni** che coinvolgono il `Mediator` nel caso in cui ci si
trovi nella modalità di gioco **multiplayer** e che, di conseguenza,
siano coinvolti **Client** e **Server**.

![Diagramma di sequenza di un ciclo di comunicazione
Client-Server.[]{label="fig:sequenceMediator"}](plantuml/rendered/sequenceDiagrams/sequenceMediator.pdf){#fig:sequenceMediator
width="0.99\\columnwidth"}

Partendo dal messaggio immediatamente successivo allo start della
partita si avranno, in maniera **iterativa**, le seguenti interazioni:

1.  Il **Client** avrà appena ricevuto il **mondo di gioco** e sarà in
    **attesa dell'input** generato dalla reazione del giocatore. Il
    `GameScreen` rileva il comando e **pubblica** il relativo evento
    verso il proprio **Mediator**

2.  Il `Mediator` del **Client** procede a **propagare** l'evento a
    tutti coloro che sono ad esso **sottoscritti**. Nel caso del Client,
    solo il **`ClientActor`**.

3.  Il `ClientActor`, ricevuto l'evento, lo comunicherà al `ServerActor`
    che procederà con la **pubblicazione** sul proprio `Mediator`

4.  Il `Mediator` del **Server** propaga l'evento ricevuto a tutti gli
    interessati. L'unico ad essere sottoscritto, nel caso del Server è
    l'`Engine`.

5.  Il `GameScreen` del **Server** cattura il **comando** del giocatore
    che ospita alla partita. Questo comando, come accadeva per il
    Client, viene inoltrato al `Mediator` di riferimento.

6.  Il `Mediator` invia a questo punto il comando all'`Engine`

7.  L'`Engine`, a questo punto, potrà calcolare il **nuovo mondo di
    gioco**, basandosi sulle azioni dell'**Intelligenza Artificiale** e
    dei **giocatori**, e inviarlo al proprio `Mediator` di riferimento.

8.  In conclusione il `Mediator` invia il messaggio al `GameScreen` di
    tutti i giocatori: al Server in maniera diretta e ai Client tramite
    il layer di comunicazione.

##### Single-player

Nella modalità single-player si mantengono le dinamiche principali, ma
senza tenere conto del layer di comunicazione dato da `ClientActor` e
`ServerActor` poiché in tale modalità non sono presenti. Le interazioni
principali avverranno quindi tra `GameScreen`, `Mediator` e `Engine`,
nelle stesse modalità riportate precedentemente.

View {#sec:view_design}
----

L'**interfaccia grafica** rappresenta uno degli elementi di spicco per
quanto riguarda l'**aspetto visivo** di un videogioco. Gli utenti
finali, infatti, non saranno interessati tanto alla progettazione del
gioco quanto al modo con cui esso si presenta.

Al fine di garantire un'**aspetto gradevole** al gioco si è deciso
quindi di puntare verso un **design modulare** che permettesse di poter
definire in modo chirurgico l'intera **user experience**.

### Struttura a schermate

Il sistema di presentazione è stato così scomposto in **schermate
multiple** (`Screen`) delegando ad ognuna di esse un particolare aspetto
dell'**interazione con l'utente**.

![Diagramma delle classi relativo all'implementazione del pattern
façade.[]{label="fig:viewFacade"}](drawio/viewFacade/viewFacade.pdf){#fig:viewFacade
width="0.99\\columnwidth"}

Come vediamo in [5.6](#fig:viewFacade){reference-type="ref"
reference="fig:viewFacade"} sono presenti cinque schermate fondamentali:

-   **GameScreen:** Costituisce il cuore dell'interazione con **ECS** ed
    è il luogo in cui prende vita il vero e proprio **gameplay**. Come
    già anticipato in [5.2](#sec:mediator_design){reference-type="ref"
    reference="sec:mediator_design"}, questa schermata avrà la capacità
    di collegarsi in modo lasco con il `Mediator` e agirà da
    **Input/Output** di **eventi** (`SendCommand` `DrawEntities`).

-   **SelectLevelScreen:** Rappresenta una delle poche **schermate
    innestate dinamicamente** nell'esperienza di gioco e il suo scopo
    consiste essenzialmente nella **scelta** dei vari **livelli
    disponibili**.

-   **MultiplayerScreen:** È qui dove la logica del multiplayer prende
    vita. L'utente che vorrà giocare con questa modalità non dovrà fare
    altro che portarsi in questa schermata e selezionare la **modalità
    di gioco**\
    (`client/server-mode`) da utilizzare.

-   **StatScreen:** È una semplice schermata relativa alle statistiche
    di gioco. Come in ogni **arcade** che si rispetti, questa mostrerà
    una lista dei **migliori punteggi** correlati al giocatore
    corrispondente.

-   **SettingsScreen:** Ogni gioco necessita di una serie di
    impostazioni al fine di garantire una **buona usabilità** e
    **personalizzazione**. Questo aspetto sarà presente e sarà
    posizionato in una schermata dedicata.

##### ScreenController:

Un dettaglio che potrebbe far storcere il naso risiede nel fatto che
ogni schermata **estende** da un'unica classe `ScreenController`.
Que-sto dettaglio dipende fortemente dalla tecnologia utilizzata in fase
di implementazione, `JavaFx`. In `JavaFx`, infatti, ad ogni layer di
presentazione (`fxml`) è associato un **modulo di controllo** chiamato,
appunto, `ScreenController`. Ogni `ScreenController` deve possedere la
capacità di interfacciarsi con il\
`Controller` e come vedremo dovrà allo stesso modo poter **interagire**
con le altre **schermate**.

### Il pattern Façade

Il **pattern Façade** si configura come una soluzione davvero
interessante al **problema di interazione** tra schermate introdotto
precedentemente. Un **façade** (facciata) consiste in un oggetto che
permette, attraverso un'**interfaccia più semplice**, l'**accesso a
sottosistemi** che espongono **interfacce complesse** e **molto diverse
tra loro**.

Nella situazione mostrata precedentemente, il façade (`ViewFacade`)
permette di poter **gestire l'interazione** con ogni sotto-schermata da
**qualsiasi schermata** mostrata in un certo istante all'utente. Questo
permette alle sotto-schermate di poter essere **sostituite** in un unico
modo garantendo così il **Single Responsability Principle**. Il pattern
inoltre permette di elevare un insieme di **metodi comuni** all'interno
di un'**unica interfaccia** permettendo così di rispettare il principio
**DRY**.

##### Façade e MVC:

L'oggetto façade proposto (`ViewFacade`) implementa interamente il
contratto definito per l'interfaccia grafica (`View`); di conseguenza
esso rappresenta a tutti gli effetti il modulo di **View** all'interno
del pattern architetturale `MVC`.

##### Façade e gestione delle schermate:

Poiché il `ViewFacade` rappresenta un **accesso** disponibile **a tutte
le sotto-schermate**, esso deve poter accedere a tutta la **logica**
relativa alle stesse. Per garantire maggiori performance di caricamento
si è deciso di costruire un **modulo** dedicato al **loading** e al
**caching** delle **schermate**: lo `ScreenLoader`.

Il funzionamento è molto semplice: quando viene richiesta una schermata
essa viene **cercata nella cache**, nel caso in cui non sia presente
allora verrà **caricata** e successivamente **mostrata all'utente**. È
importante che la **cache** di alcune schermate particolari
(`GameScreen`) venga **invalidata** al fine di garantire una
**dinamicità del contenuto**.

File Manager {#sec:file_manager_design}
------------

A seguito di un analisi dei file utilizzati e delle varie risorse
caricate da jar e non, sono state individuate tre principali
**categorie** di operazioni.

Operazioni su:

1.  **File generici**

2.  **File Yaml**

3.  **Altri dati (musica, sprite, ecc)**

Ogni categoria è gestita con una classe separata: i file generici sono
stati gestiti dal **FileManager**, i file Yaml con lo **YamlManager** e
gli altri dati con il **DataManager**.

![Diagramma di classe rappresentante la struttura dei tre
manager.[]{label="fig:FileManager"}](drawio/fileManager/fileManager.pdf){#fig:FileManager
width="0.90\\columnwidth"}

-   **FileManager**: le operazioni di **base** sui file come il
    **caricamento** di una risorsa da jar o da sistema, possono essere
    effettuate da qualunque modulo dell'applicazione.

    Un solo FileManager è sufficiente per la gestione dei file in tutto
    l' applicativo; di conseguenza è stato progettato avvalendosi
    dell'utilizzo del pattern **Singleton**. Inoltre la divisione dei
    compiti e l'accesso globale consentono di diminuire il rischio di
    creare **God class**.

-   **YamlManager**: i file **Yaml** sono la principale tecnica di
    **serializzazione** dei dati utilizzata nel contesto di questo
    progetto; in essi vengono salvati **livelli**, **record** e **dati
    utente**. Per questo è stato introdotto un **gestore** unicamente
    dedicato ai file Yaml che si appoggia sul `FileManager` per le
    **operazioni di base** e ne consente **scrittura** e **lettura**.

-   **DataManager**: consente l'accesso a tutti i dati **astratti** del
    programma (livelli, impostazioni, statistiche, ecc). Si basa sullo
    `YamlManager` e il `FileManager` per effettuare le operazioni di
    caricamento e salvataggio ed è utilizzato dal **Controller** che lo
    sfrutta per accedere alle varie risorse **testuali**.

Audio Manager {#sec:audio_manager_design}
-------------

I videogiochi richiedono in generale il lancio di un elevato numero di
**suoni** per partita. Questi suoni rientrano generalmente in una delle
seguenti categorie:

-   **Effetti sonori:** sono generalmente legati a **eventi** o a
    **interazioni** con la **GUI** del gioco.

-   **Musica:** ricoprono un ruolo di **sottofondo** e vengono
    riprodotto con **minor frequenza**.

##### Un modello ad agenti:

L'elevata frequenza di eventi ha portato allo sviluppo di un **Agente**
al quale è stato affidato il compito di **gestire** e **manipolare**
internamente tutti gli aspetti sonori del gioco.

Il `SoundAgent` è caratterizzato da un **flusso di controllo separato**
e utilizza una **coda di eventi** per tracciare tutte le **azioni** che
deve effettuare. Gli utilizzatori possono infatti **accodare eventi**
esternamente **senza** così **inquinare** l'operatività del **proprio
flusso** di controllo. Un flusso di controllo separato consente di
**disaccoppiare** al massimo il carico di lavoro, permettendo così di
non gravare sulla logica principale del programma né tantomeno sulla
**View**.

![Diagramma di classe rappresentante la struttura del
SoundAgent.[]{label="fig:AudioAgent"}](drawio/audioAgent/audioAgent.pdf){#fig:AudioAgent
width="0.99\\columnwidth"}

Un solo `SoundAgent` è in grado di riprodurre una grossa **quantità di
clip**, ciò nonostante è possibile istanziarne più di uno, questo per
non limitare il numero di suoni. È inoltre possibile creare `SoundAgent`
specifici.

Un eventuale utilizzatore potrà quindi schedulare un nuovo evento
semplicemente sfruttando il pattern **Strategy** implementando
l'interfaccia funzionale `SoundAgentLogic`. Questo consente di evitare
l'utilizzo reiterato di **match case** all'interno dell'agente, rendendo
l'esecuzione più **performante** e il **codice più snello**.

Client Server {#sec:client_server_design}
-------------

La realizzazione della modalità di gioco **multiplayer** richiede di
elaborare una struttura che permetta a due o più giocatori di interagire
**contemporaneamente** con la medesima partita.

Come introdotto in [4.2.3](#subsec:client_server){reference-type="ref"
reference="subsec:client_server"} si è scelto di realizzare un sistema
multi-giocatore con le seguenti caratteristiche:

-   I giocatori interagiscono con il gioco da **istanze separate**.

-   La gestione del sistema è **centralizzata** e la partita è gestita
    da un **Server**.

![Diagramma delle classi che rappresenta le connessioni tra il
Controller e gli attori Client e
Server.[]{label="fig:Controller-Actors-Interaction"}](drawio/client-server/Controller-Actors-Interaction.pdf){#fig:Controller-Actors-Interaction
width="0.99\\columnwidth"}

Per gestire l'**interazione** tra il Server e i Client era necessario
disporre di un **canale di comunicazione** tra di essi. Per
concretizzare ciò si è scelto di utilizzare un approccio ad **attori**,
introducendo `ClientActor` e `ServerActor`. La **modellazione**
dell'architettura **Client-Server** è stata realizzata come raffigurato
in [5.9](#fig:Controller-Actors-Interaction){reference-type="ref"
reference="fig:Controller-Actors-Interaction"}.

La struttura del diagramma si presenta con due elementi principali: gli
**attori** e il **Controller**.

-   **Controller:** rappresenta il punto di **snodo** dello schema ed
    espone, tra le altre cose, i metodi necessari per gestire le
    informazioni che arrivano dal `ClientActor` o dal `ServerActor`, a
    seconda della modalità in cui si vuole giocare.

-   **Attori:** `ClientActor` e `ServerActor` sono intesi come
    **interfaccia di comunicazione** tra il sistema presente
    nell'istanza di gioco che agisce come **Server** e quello presente
    nelle istanze in funzione sui **Client**. I due attori comunicano
    mediante **scambio di messaggi**.

### Assetto Client-Server

Il diagramma delle classi è stato progettato promuovendo un'idea di
**flessibi-lità**. A seconda della modalità di gioco scelta, l'assetto
deve poter **variare** per permettere una gestione **efficiente** delle
dinamiche del sistema.

#### Modalità Client

Nella modalità Client la struttura delle classi è la seguente:

-   L'`Engine` del gioco **non viene utilizzato** e pertanto risulta
    slegato dal Controller.

-   Il Controller **crea** e **mantiene** un'istanza del `ClientActor`.

-   Il `ServerActor` è **assente**.

#### Modalità Server

Quando il sistema passa in modalità Server, viene assunto un assetto
diverso che si presenta in questo modo:

-   Il Controller **crea** e **mantiene** un'istanza del `ServerActor`.

-   Il `ClientActor` è **assente**.

-   L'`Engine` del gioco viene **mantenuto**, poiché dovrà occuparsi
    completamente della gestione della partita in corso.

### Gestione della comunicazione

Ottenuta la configurazione relativa al **ruolo** scelto è possibile
gestire i **flussi** di comunicazione che vanno dal **Client** al
**Server** e viceversa.

##### Gestione in entrata:

ciascun **attore**, nel momento in cui **riceve** un messaggio dalla sua
controparte esterna, chiama, sul **Controller**, il **metodo** preposto
alla gestione dello stesso.

Ad esempio, alla ricezione di un messaggio che indica l'inizio del
gioco, il `ClientActor` dovrà chiamare il metodo `notifyGameStart()`
sull'istanza di `ActorController` da esso **mantenuta internamente**.

##### Gestione in uscita:

nel momento in cui, invece, è il sistema locale a dover **aggiornare**
la controparte esterna su qualcosa, il flusso si inverte: il
**Controller**, a fronte di un **evento**, chiama sull'attore il
**metodo** preposto alla gestione dello stesso.

Ad esempio, alla pressione di un tasto da parte dell'utente, il
Controller chiamerà il metodo `handle()` esposto dalla sua istanza di
`ClientActor`, passando come parametro un `CommandEvent`. All'interno di
questo metodo verrà eseguita una `send` che permetterà di inviare un
messaggio al Server esterno al fine di notificare la ricezione del
comando.

### Sequenze di interazioni

La gestione dell'**inizio**, dello **svolgimento** e dell'**arresto** di
una partita **multiplayer** si svolge attraverso una serie di **fasi**
di interazione tra gli elementi in gioco. Queste interazioni sono state
evidenziate nel diagramma in
[5.10](#fig:sequenceClientServer){reference-type="ref"
reference="fig:sequenceClientServer"}

Le fasi di interazione possono essere raggruppate in tre **macro-fasi**:

1.  **Setup:** prima di cominciare una partita è necessaria una prima
    fase di **configurazione** che si svolge nel seguente modo:

    1.  Inizialmente si ha che un'istanza del gioco assume il ruolo di
        **Server**, mentre una o più altre istanze scelgono il ruolo di
        **Client**

    2.  Prima di iniziare il gioco, il giocatore che si trova
        sull'istanza Server sceglie il **numero di giocatori** e
        configura le **impostazioni della partita**.

    3.  Il Server rimane in **attesa delle richieste di join**
        provenienti dai Client.

    4.  Ad ogni richiesta di `join` ricevuta, il Server **controlla** se
        è stato raggiunto il **numero massimo di giocatori**. In caso
        affermativo **respinge** la richiesta, altrimenti la
        **accoglie**.

    5.  Quando vi è un **numero corretto** di Client collegati e quando
        questi si trovano tutti nello stato `ready`, il Server può
        **avviare** la partita.

2.  **Gioco:** è la fase principale dove avvengono interamente le
    dinamiche di gioco e consiste nella ripetizione ciclica di tre step.

    1.  Ciascun Client invia al Server la propria azione, derivante dal
        **comando** impartito dal proprio utente.

    2.  Il Server **riceve** i comandi e li **elabora** insieme ai
        propri.

    3.  Il Server calcola il **nuovo mondo** e lo invia a tutti i
        Client.

3.  **Arresto:** quando la partita giunge al termine avvengono le
    seguenti interazioni:

    1.  Il Server calcola i **punteggi**

    2.  Il Server **invia l'esito** della partita a tutti Client.

    3.  Le **connessioni** tra il Server e i Client vengono **chiuse**

![Diagramma di sequenza che rappresenta la fase di join alla partita e
lo svolgimento di
essa.[]{label="fig:sequenceClientServer"}](plantuml/rendered/sequenceDiagrams/sequenceClientServer.pdf){#fig:sequenceClientServer
width="0.80\\columnwidth" height="0.95\\linewidth"}

Interazioni {#sec:interactions_design}
-----------

#### Interazione tra Engine, ECS e controller

Come spiegato in [5.1](#sec:ecs_design){reference-type="ref"
reference="sec:ecs_design"}, i vari gestori di componenti che formano
l'ECS sono coordinati tra di loro tramite un `Coordinator`. Esso fa da
punto di contatto con l'`Engine`, che rappresenta il gestore della
partita e contiene:

-   **Coordinator:** è l'entry point per interagire con le entità
    fondamentali di ECS, esponendo il metodo `updateAllSystems`;

-   **GameLoop:** modellato come un flusso di controllo separato, è
    l'effettivo motore del gioco. Ha una visione limitata dell'engine,
    `UpdateableEngine`, su cui richiama ciclicamente update, causando
    l'aggiornamento dei sistemi, mantenendo costanti e modificabili gli
    fps mostrati all'utente;

-   **Mediator:** consente al gioco di far comunicare **Engine** e il
    GameScreen in modalità single-player, mentre al join di una partita
    multiplayer come client l'engine verrà staccato da parte del
    controller e il mediator comunicherà con l'attore client. Invece,
    durante l'hosting di una partita multiplayer il server si affianca
    al `GameScreen` e tramite il `Mediator` riceve gli eventi
    dall'`Engine` e li comunica ai client partecipanti alla partita.

![Diagramma raffigurante ecs, engine e controller e le loro
interazioni.[]{label="fig:ecs-engine-controller"}](drawio/ECS-engine-controller/ecs-engine-controller.pdf){#fig:ecs-engine-controller
width="\\columnwidth"}

#### Interazione tra Controller e View

Per rendere possibile l'aggiornamento della View da parte del controller
è stato utilizzato il pattern observer, fornendo al controller un
oggetto che implementa il trait **ObserverUI**. Esso fornisce al
controller la possibilità di per poter comandare la view in tre scenari
principali:

-   **Aggiornamento impostazioni globali:** quando l'utente cambia
    impostazioni globali, o quando vengono caricati i valori di default
    permette alla view di essere aggiornata con i valori correnti;

-   **Aggiornamento impostazioni multiplayer:** è necessario poter
    mos-trare ogni nuovo status della lobby, sia quando si unisce un
    nuovo giocatore alla partita sia al cambiamento dello stato di
    \"ready\" di un giocatore. Inoltre aggiorna i client sui cambiamenti
    delle impostazioni globali della partita effettuati lato server, che
    vengono anche essi mostrati nella schermata della lobby;

-   **Notifica di avvio partita multiplayer:** quando l'host della
    partita decide di avviarla è necessario far cambiare schermata ai
    client e fargli caricare il loro GameScreen;

Invece, per garantire la possibilità alla view di comunicare al
controller le operazioni necessarie al setup delle differenti modalità
di gioco gli viene fornito il trait **ObservableUI** che permette le
seguenti operazioni:

-   **attachUI, detachUI:** quando viene fatto eseguire il gioco in
    modalità server \"headless\" è necessario staccare la view, mentre
    al setup è necessario attaccarla al resto del sistema;

-   **loadAllLevels, loadStats, saveStats:** durante la modifica e il
    caricamento delle impostazioni e delle statistiche, consentono alla
    view di caricarle da file e modificarle;

-   **becomeHost, startMultiplayer, shutDownMultiplayer:**

    permettono lo switch tra le varie modalità di gioco, e causano il
    setup o la distruzione dei vari componenti associati;

-   **tryJoinLobby, kickSomeone, leaveLobby:** permettono l'interazione
    con la lobby in modalità multiplayer;

-   **start, startMultiplayer:** in modalità singleplayer e in modalità
    multiplayer quando si è host, notificano al controller l'intenzione
    dell'utente di iniziare una partita;

![Diagramma raffigurante view, controller e observer e le loro
interazioni.[]{label="fig:view-controller-observer"}](drawio/view-controller-observer/view-controller-observer.pdf){#fig:view-controller-observer
width="\\columnwidth"}

Implementazione
===============

Luca Giulianini
---------------

Lo studente Luca Giulianini si è occupato della **progettazione** e
**implementazione** delle seguenti macro-parti:

-   
-   
-   
-   
-   

ha contribuito alla **progettazione** di:

-   

inoltre ha contribuito al lavoro dei colleghi svolgendo una serie di
**task implementativi**:

-   
-   
-   

#### Approfondimenti

Parallelamente all'esperienza di progetto sono stati approfonditi una
serie di argomenti relativi al mondo di **Scala** e della
**programmazione funzionale**.

-   **Teoria delle Categorie:** sono stati chiarite le principali
    astrazioni funzionali provenienti dalla teoria delle categorie. La
    libreria `cats` in questo senso fornisce ottime astrazioni per il
    concetto di `Semigroup, Monoid, Functor, Monad` (vedi
    [6.1.8](#subsubsec:risorse){reference-type="ref"
    reference="subsubsec:risorse"}).

-   **Pogrammazione funzionale:** sono stati approfonditi gli aspetti
    teorici (**referential transparency, effects, ecc**) ed è stato
    appreso un insieme di **buone pratiche** relative alla
    programmazione funzionale. Questo è stato fatto seguento svariate
    **conferenze** dedicate al mondo Scala e appoggiandosi a una serie
    di **libri** dedicati.

-   **Refined Types:** Molto utili nella fase di **validazione statica e
    dinamica** di input. Attualmente non utilizzati data la natura del
    progetto in questione.

-   **Monix:** È stato approfondito il mondo della programmazione
    **reattiva** focalizzandosi maggiormente sul framework `Monix`.

### Architettura generale e mediazione MVC-ECS {#subsec:arc_mediator}

#### Progettazione

La definizione di una architettura generale ha richiesto un grande
sforzo dal punto di vista del **design**. I principali problemi da
risolvere sono stati essenzialmente i seguenti:

-   **Interazione MVC-ECS:** il problema in questo caso risiede nella
    **natura architetturale** dei due **pattern**. Essi generalmente
    sono utilizzati **singolarmente** per plasmare una applicazione e
    una possibile **integrazione** con altri pattern avrebbe potuto
    portare a **seri conflitti**.

-   **Estendibilità al modello client-server:** l'idea architetturale
    fondante, per quanto riguarda l'intero applicativo, è sempre stata
    diretta verso la definizione di un **core funzionante** espandibile
    attraverso **moduli client-server** (attori). L'idea è stata
    sicuramente ambiziosa ma ha portato con se una serie di
    problemantiche non banali a livello interazionale. Infatti,
    sviluppare un **core** **modulare** e **dinamico** in base alla
    tipologia di interazione richiede un alto tasso di ingegnerizzazione
    e **anticipazione del cambiamento**.

##### La Soluzione {#la-soluzione}

La soluzione come già anticipato in
[5.2](#sec:mediator_design){reference-type="ref"
reference="sec:mediator_design"} è consistita nella defini-zione di un
oggetto di tipo `publish/subscribe` (il `Mediator`) capace di **mediare
i flussi di dati** fra un numero di oggetti indefinito.

#### Implementazione

##### Approccio ad Handlers {#subsubsec:mediator_handler_problem}

L'implementazione del `Mediator` è stata inizialmente incentrata su una
architettura basata su **handlers** ad **eventi** (vedi
[5.3](#fig:mediatorHandler){reference-type="ref"
reference="fig:mediatorHandler"}). L'architettura però ha da subito
presentato alcune **lacune** molto gravi fra le quali troviamo
l'impossibilità di poter **rimuovere facilmente handlers relativi a un
subscriber** e una **più difficile gestione delle gerarchie di eventi**.
Per questo motivo si è deciso di sacrificare un briciolo di performance
e puntare maggiormente su una architettura più **pulita** e **stabile**
basata su **Observers**.

##### Approccio ad Observers

Questo approccio si basa essenzialmente sul modello proposto dal
**Pattern Observer**. Nel caso proposto però la parte\
`Observable` è stata incapsulata all'interno di un unico elemento, il
`Mediator`. Così facendo il `Mediator` si configura come **unico punto
di snodo** capace di **osservare** e **ridirigere** gli eventi verso
l'`Observer` **appropriato** (**Subscriber**). La ridirezione è svolta
osservando il **tipo dell'evento** in **entrata** e il tipo dell'evento
al quale un `Observer` **è interessato**. Ogni `Observer` è interessato
a tutti gli eventi che sono **covarianti** rispetto al tipo di evento al
quale si sono **sottoscritti** (vedi
[\[lst:listato1\]](#lst:listato1){reference-type="ref"
reference="lst:listato1"})

``` {#lst:listato1 .scala caption="Mediator" label="lst:listato1"}
```

Per quanto riguarda la definizione degli eventi, si è deciso di
utilizzare un approccio basato su `Algebraic Data Type` grazie al quale
è possibile definire una gerarchia di eventi (vedi
[\[lst:listato2\]](#lst:listato2){reference-type="ref"
reference="lst:listato2"})

``` {#lst:listato2 .scala caption="Event" label="lst:listato2"}
```

#### Contributi e validazioni

-   **Gyordan Caminati:** l'implementazione del `Mediator` tramite
    l'utilizzo di `Observers` è stata **validata** da Gyordan Caminati.
    Inoltre Gyordan ha fornito un **contributo** molto importante nella
    **risoluzione di un problema** riscontrato durante l'utilizzo di
    **reflections** in Scala.

### Architettura ECS {#subsec:arc_ecs}

#### Progettazione

La fase di progettazione relativa ad ECS è consistita in un **processo
di continuo raffinamento**, iniziato prendendo spunto da alcuni
**articoli proposti in rete** e concluso con una **soluzione**
estremamente **pulita** e **concisa**.

##### Composition over Inheritance

Personalmente la sfida più grande in questo caso è stata trovare un
design che permettesse di ottenere una **buona estendibilità**
mantenendo allo stesso tempo delle **buone performance**. Si è passati
così alla definizione di un modello **data-driven**, molto vicino ad una
**visione funzionale**. Come vediamo in
[5.1](#fig:ECS){reference-type="ref" reference="fig:ECS"} si è deciso di
spostare l'intera architettura verso un approccio basato su
**composizione**, molto **estendibile** e **manutenibile**.

##### Managers

L'intera **logica di gestione** è stata spostata **al di fuori** delle
entità in gioco, all'interno di moduli dedicati chiamati `Manager`. Ogni
manager è caratterizzato da un **insieme ridotto di operazioni**
dedicate a **gestire** e **connettere** al più due **tipologie** di
oggetti. Per esempio un `ComponentManager` è in grado di gestire
solamente `Component` e per farlo mette in relazione ad essi anche delle
`Entity`.

##### Coordinator

Poichè la gestione di singoli `Manager` separatamente produrrebbe un
**design frammentato** e difficilmente controllabile, è stato deciso di
**coordinare** quest'ultimi grazie ad un unico modulo che prende il nome
appunto di\
`Coordinator`.

#### Implementazione

L'implementazione dell'architettura di `ECS` è risultata estramente
**lineare** e **non si è discostata** di molto da ciò che era stato
**progettato**.

#### Contributi e validazioni

-   **Ruben Ceroni:** l'implementazione dell'architettura di `ECS` è
    stata **validata** da Ruben Ceroni il quale ha **incoraggiato**
    verso lo sviluppo di una **soluzione** basata su **managers**.

### Framework View {#subsec:arc_view}

Le interfacce grafiche sono generalmente formate da più schermate che
rappresentano **moduli di interazione** utente-applicativo. Una delle
sfide più grandi che si devono affrontare nel momento in cui si sviluppa
un'interfaccia grafica è la definizione di un **framework** capace di
gestire al meglio questi moduli.

#### Progettazione

##### Problemi

Il framework proposto si pone come obiettivo la risoluzione di due
problemi fondamentali:

-   **Gestione e cambio di schermate:** come introdotto precedentemente,
    dovrà essere possibile gestire in modo **dinamico** le schermate
    garantendo proprietà di **scalabilità** nel **numero** delle stesse.
    Inoltre si dovrà definire un modo per garantire un **controllo** nel
    **cambio di schermata**.

-   **Interazione View-Controller:** l'interazione fra `View` e
    `Controller`\
    deve essere definita in modo **pulito** ed **efficace**. Lo scopo
    sarà quello di evitare la generazione di **God-Class** costituite da
    una moltitudine di **metodi** dedicati alle singole schermate.

##### Soluzioni

La soluzione proposte sono le seguenti:

-   **Gestione e cambio di schermata:** in questo caso la soluzione si
    basa sull' uso di un pattern molto utilizzato nel contesto delle
    GUI, il `Pattern Façade`. Il façade garantisce una **facciata di
    interazione** a tutte le sotto-schermate espondendo ad esse alcuni
    **comandi fondamentali**. In questo modo ogni sotto-schermata può
    chiedere al façade di essere **sostituita** o può chiedere il
    **caricamento** di una ulteriore schermata.

-   **Interazione View-Controller:** L'interazione fra `View` e
    `Controller` è spesso regolamentata all'interno di MVC tramite il
    `Pattern Observer` basato sul **Interface Segregation Principle**.
    Secondo questa forma di Observer, `View` e `Controller` possiedono
    **reciprocamente una sotto-interfaccia** e tramite essa possono
    invocare metodi in modo sicuro.

    Un problema che emerge dall'utilizzo di questo pattern risiede nel
    fatto che una **aggiunta** continua di **funzionalità** a queste
    sotto-interfacce potrebbe portare nel tempo a un'**esplosione**
    della dimensione due moduli (God-Class).

    Al fine di evitare ciò si è deciso di utilizzare una versione più
    scalabile del Pattern Observer basata su **eventi**.

#### Implementazione

##### Gestione delle schermate

La gestione delle schermate è stata delegata ad un modulo a parte
chiamato `ScreenLoader`. Questo modulo è molto semplice e consiste, come
vediamo nello snippet
[\[lst:listato3\]](#lst:listato3){reference-type="ref"
reference="lst:listato3"}, nella definizione di una **cache** dedicata
alla gestione delle schermate.

`ScreenLoader` mette a disposizione una serie di funzionalità di
**caricamento di schermate** e **gestione dei controller** relativi. Il
modulo permette inoltre di poter **applicare una schermata ad un nodo**
abilitando così il **cambio di schermata**.

``` {#lst:listato3 .scala caption="ScreenLoader" label="lst:listato3"}
private[view] trait ScreenLoader {
  def getScreenController(screen: FXMLScreens): ScreenController
  def applyScreen(screen: FXMLScreens, root: Pane): Unit
  def loadFXMLNode(screen: FXMLScreens, controller: ScreenController): Unit
}
private[view] object ScreenLoader {
  class ScreenLoaderImpl extends ScreenLoader {
    private var cache: Map[FXMLScreens, (Node, ScreenController)] = Map()
    ....
}
```

##### Logica di cambio di schermata

La **logica** del cambio di schermata deve essere **separata** dalle
singole schermate in modo che esse **non debbano proccuparsi** di dove
ridirigere l'utente.

Seguento il principio di **Separation of Concept** si è deciso di
delegare il cambio di schermata a una **Macchina a Stati Finiti**
(`FSM`). Così facendo è possibile definire in modo dichiarativo una
serie di coppie (`Event` `->` `State`) che costituiscono le
`transizioni` della nostra `FSM`. Ovviamente, dato il contesto,
definiremo uno `State` come `Screen`: ossia ogni stato sarà
caratterizzato dalla schermata che sta mostrando (vedi
[\[lst:listato4\]](#lst:listato4){reference-type="ref"
reference="lst:listato4"}).

``` {#lst:listato4 .scala caption="View e StateMachine" label="lst:listato4"}
private class ViewImpl(controller: UpdatableUI) extends View with ViewFacade {
  private val stateMachine = ViewStateMachine.buildStateMachine()
  private val root = new StackPane()
  override def changeScreen(event: ScreenEvent): Unit = screenLoader.applyScreen(stateMachine.consume(event), root)
  ....
}

private[view] object ViewStateMachine {
  def buildStateMachine(): StateMachine[FXMLScreens, ScreenEvent] = StateMachine
    .WithFunctionTransitions[FXMLScreens, ScreenEvent]()
    .initialState(FXMLScreens.HOME)
    .transition({
      case (HOME, GotoLevels) => LEVELS
      case (HOME, GotoLobby) => LOBBY
      ...
    }).build()
}
```

##### Interazione View-Controller

L'interazione tra `View` e `Controller` è stata implementata, come
abbiamo già anticipato, sfruttando i pattern Observer ba-sato su Eventi.
Al fine limitare una possibile esplosione di eventi si è deciso di
sfruttare una struttura ad `Algebraic Data Type` **gerarchica**.

Si è deciso di creare una **famiglia di eventi** per ogni schermata
definendo un **trait dedicato**. Così facendo il façade si trova a
gestire solamente **un tipo di evento per schermata** delegando la
gestione dell'**evento concreto** (sotto-tipo) alla schermata
corrispondente.Questo approccio basato su **deleghe**, permette di
ottenere un'**implementazione pulita** ed **estendibile** (vedi
[\[lst:listato5\]](#lst:listato5){reference-type="ref"
reference="lst:listato5"}).

``` {#lst:listato5 .scala caption="Observer[Event]" label="lst:listato5"}
trait ObserverUI {
  def notify(ev: ViewEvent): Unit
}
trait View extends ObserverUI
override def notify(ev: ViewEvent): Unit = ev match {
  case event: ViewEvent.HomeEvent => screenLoader.getScreenController(FXMLScreens.HOME).notify(event)
  case event: ViewEvent.GameEvent => screenLoader.getScreenController(FXMLScreens.GAME).notify(event)
  case event: ViewEvent.LobbyEvent => screenLoader.getScreenController(FXMLScreens.LOBBY).notify(event)
  ...
}
```

#### Contributi e validazioni

-   **Gyordan Caminati:** l'implementazione del framework proposto è
    stata **validata** da Gyordan Caminati. Gyordan ha contribuito
    inoltre a fornire un **input** per un'idea di **interazione ad
    eventi**, sopra alla quale poi è stata sviluppata l'implementazione
    finale.

### Schermata di Gioco {#subsec:game_screen}

Come introdotto precedentemente in
[5.2](#sec:mediator_design){reference-type="ref"
reference="sec:mediator_design"} lo scopo di `Mediator` consiste nel
creare un collegamento **lasco** fra `GameScreen` e
`Engine/ClientActor`. La schermata di gioco si configura quindi come
punto di incontro fra pattern `ECS` e `MVC`; di conseguenza è molto
importante saper suddividere le varie **responsabilità**. Come vediamo
in [\[lst:listato6\]](#lst:listato6){reference-type="ref"
reference="lst:listato6"} la separazione dei concetti è molto forte ed è
dettata dall'implementazione di due interfacce separate:

-   `Displayable:` gestisce gli eventi provenienti da `Mediator`.
    Ovviamente questi sono inoltrati solamente previa **sottoscrizione**
    al `Mediator` che è così in grado di associare alla schermata di
    gioco l'insieme di eventi compatibili (subtype di `Displayable`).

-   `ScreenController:` abstract root class che fornisce un metodo
    `notify` che veicola tutti i messaggi che giungono al `View-Façade`.
    Ogni schermata implementa una gestione dedicata ai soli **propri
    messaggi**.

`GameScreen` dovrebbe idealmente rappresentare una schermata utile solo
in **fase di gioco**, di conseguenza ci si auspica che la gestione di
eventi provenienti da `Controller` sia ridotta al minimo.

``` {#lst:listato6 .scala caption="ScreenControllerGame" label="lst:listato6"}
class ScreenControllerGame(viewFacade, controller) extends AbstractScreenController(viewFacade, controller) with Displayable {
  private val mediator: Mediator = controller.getMediator
  mediator.subscribe(this)
  //Events from mediator to Displayable (GameScreen)
  override def notifyDrawEntities(player: EntityData, entities: Seq[EntityData]): Unit = handleDrawEntities(players, entities))
  override def notifyEntityLife(data: LifeData): Unit = handleEntityLife(data)
  override def notifyLevelEnd(data: LevelEndData): Unit = handleLevelEnd(data)
  //Mvc events from Controller
  override def notify(ev: ViewEvent): Unit = ev match {
    case LevelSetupEvent(data) => handleLevelSetup(data)
  }
  def sendCommandEvent(event: Event.CommandEvent): Unit = mediator.publishEvent(event)
```

#### Eventi di gioco

La gestione del gamplay è modellata su questi eventi:

-   **LevelSetup:** inviato nel momento in fase di caricamento di un
    livello: esso è responsabile della creazione e inizializzazione
    delle logiche di **comando** e **visualizzazione**.

-   **DrawEntities:** evento di **visualizzazione** contenente le entità
    da **disegnare**.

-   **EntityLife:** evento di **gioco** che contiene il **danno
    inferto** all'entità governata dall'utente.

-   **LevelEnd:** evento utilizzato per **dismettere** le strutture dati
    create per gestire il gamplay.

#### Implementazione gameplay

La gestione del vero e proprio gameplay è stata nascosta in una classe
astratta chiamata `AbstractScreenControllerGame`. La suddivisione è
stata proposta per garantire una maggiore pulizia e definire una
**separazione** fra interazione e operazioni interne che verranno
appunto gestite da questa classe. La gestione del gameplay si focalizza
su due operazioni fondamentali:

-   **Elaborazione e invio di comandi**

-   **Visualizzazione delle entità**

##### Elaborazione e invio di comandi

L'elaborazione di comandi è un'opera-zione molto delicata poiché si basa
sull'**acquisizione** real-time dell'input dell'u-tente. In questo
frangente la libreria `JavaFx` si è rivelata molto utile poiché permette
di ottenere, tramite `handlers`, un **flusso continuo** di eventi da
**qualsiasi nodo** della schermata.

Dato che l'acquisizione non deve essere costante ma solo dedicata alla
**fase di gioco**, si è deciso di **racchiudere** la logica di gestione
ed elaborazione dell'input in un **modulo immutabile**,
`GameEventHandler` (vedi
[\[lst:listato7\]](#lst:listato7){reference-type="ref"
reference="lst:listato7"}).

``` {#lst:listato7 .scala caption="GameEventHandler" label="lst:listato7"}
case class GameEventHandler(val pane: Pane, val handleCommand: CommandEvent => Unit, val entity: Entity) {
	private val activeKeys = mutable.HashSet()
	pane.addEventHandler(KeyEvent.KEY_PRESSED, keyPressedHandler)
	object ImplicitConversions {
    implicit def keyToDir(key: KeyCode): Direction = key match {
      case W => North
      case S => South
      ...
		}		
	}
  private def createKeyPressHandler(): EventHandler = e => {
    val dir = e.getCode
    if (!activeKeys.contains(dir)) {
      activeKeys add dir
      update()
    }
  }
  private def createKeyReleasedHandler(): EventHandler ....
  private def update(): Unit = {
    val dir = activeKeys.foldLeft[Direction](Center)(_ + _)
    handleCommand(CommandEvent(CommandData(entity, dir)))
  } 
}
```

Il funzionamento del modulo è molto semplice: esso infatti rispecchia le
fasi di *setup* (`LevelSetupEvent`) e *teardown* (`LevelEndEvent`)
elencate precedentemente con una modalità operativa che questa volta è
dedicata all'*invio di comandi* piuttosto che alla visualizzazione di
entità.

-   **Setup:** in fase di setup vengono **inizializzati** e
    **agganciati** gli handler utili per la generazione di eventi.
    Inoltre viene fornito l'**uuid** del player, utile per marcare i
    messaggi inviati.

-   **Teardown:** una volta completato il gameplay potranno essere
    **sganciati** gli **handler**.

###### Invio di CommandEvent

La gestione dell'invio di comandi si svolge in questo modo: Quando
l'utente preme un testo il sistema in tempo reale invoca l'handler
dedicato il quale restituirà un evento contente il **codice** del
pulsante premuto. Il codice, opportunamente convertito in `Direction`
viene aggiunto a un set che mantiene le **direzioni attualmente attive**
e dopo aver calcolato la **direzione risultate** essa viene inviata
sotto forma di `CommandEvent` all'`Engine`.

##### Visualizzazione delle entità

Dato che la visualizzazione di entità è strettamente legata alla
tipologia delle stesse si è deciso di racchiudere la logica di disegno
all'interno di particolari oggetti chiamati `EntityWrapper`. Ogni
wrapper possiede un'immagine specifica per ogni entità e contiene
inoltre un metodo `draw` che ne definisce la visualizzazione.

### Continuous Integration e configurazione dei Build-Tools {#subsec:ci}

Data la buona esperienza accumulata nell'ambito della `CI`
l'implementazione della stessa è stata svolta interamente dallo
studente. In questo caso si è deciso di sperimentare un processo di
**rilascio** basanto interamente su `GitHub`. Per fare ciò ci è affidati
ai servizi `Releases` e `Pages` messi a disposizione dalla piattaforma.
Un'altra sperimentazione ha portato a definire un processo di deploy
dedicato ai file `.tex`, il quale permetteva di **compilare
remotamente** la relazione per poi **inviarla** ai colleghi in modo
automatico.

### Sound Agent - design basato su Handlers {#subsec:media_event}

#### Progettazione

Rifacendosi alla grande intuizione di Gyordan nel dotare il `SoundAgent`
di un **thread di elaborazione separato**, si è colta l'opportunità di
migliorare ancora di più il design aggiungendo una **gestione ad
eventi**. È stato poi definito un tipo di evento standard, `MediaEvent`
il quale fornisce un unico metodo `handle` che opera su un
`SoundEventLogic` (vedi
[\[lst:listato8\]](#lst:listato8){reference-type="ref"
reference="lst:listato8"}).

``` {#lst:listato8 .scala caption="MediaEvent e Integrazione in SoundAgent" label="lst:listato8"}
private final class ConcreteSoundAgent extends SoundAgendLogic {
	override def run(): Unit = {
		while (true) {
  		Try(this.blockingQueue.take()) match {
    		case Success(ev) => processEvent(ev)
    		case Failure(exception) => logger warn (exception.getMessage)
    	}
def processEvent(ev: MediaEvent): Unit = ev.handle(this)
...

sealed trait MediaEvent {
  def handle(sl: SoundAgentLogic): Unit
}
object MediaEvent {
final case class PlayMusicEvent(media: Music) extends MediaEvent {
  def handle(sl: SoundAgentLogic): Unit = sl.playMusic(media)
} ...
```

Un `MediaEvent` si configura quindi come un **handler**, ossia un
contenitore di codice che potrà essere eseguito su un qualsiasi oggetto
che implementi `SoundAgentLogic`. L'integrazione di `MediaEvent` e
`SoundAgent` ha portato alla definizione di un **event loop** capace di
eseguire eventi che hanno come target lo stesso `SoundAgent`:

    case Success(ev) => ev.handle(this)

### Altri Task

#### Input System {#subsubsec:input_sys}

L'`InputSystem` è il sistema dedicato all'elaborazione dell'input
dell'utente il cui scopo principe è quello di fornire una **direzione**
alle entità di gioco. In questo caso la soluzione ottima è stata
ottenuta andando a **completare** quella proposta dal lato `View`.

I comandi precedentemente accodati vengono estratti dalla coda,
**filtrati** in base all'**entità corrispondente** e infine mappati in
**direzioni**. Poiché le direzioni contenute nei comandi seguono un
**ordine cronologico**, sarà necessario mantenere solamente l'**ultima
direzione** disponibile scartando tutte le altre [^1].

#### Life points e collision damage {#subsubsec:damage}

Data la grande **flessibilità** di ECS è stato molto facile introdurre
il concetto di **danno a fronte di collisioni**. L'implementazione
consiste di due parametri all'interno del `CollisionComponent`: **vita**
(`life`) e **danno** (`damage`). Nel momento in cui viene rilevata una
**collisione** i **life points** dell'utente vengono **decrementati** in
base al danno indicato sulla medesima entità.

L'implementazione è stata **decisamente migliorata** da **Sara Kiade**
che ha aggiunto **nuove dinamiche** irrobustendo contemporaneamente
quelle già proposte.

##### Interazione con View:

Al fine di **comunicare** i vari punti vita alle varie **interfacce
grafiche** è stato predisposto un **messaggio di mediazione** dedicato:
`EntityLifeEvent`. Nel momento della ricezione del messaggio, lato view,
è stata creata una **barra di caricamento** che viene mano a mano
decrementata a seconda del **danno inferto**.

#### Monix - Parallelizzazione update dei sistemi {#subsubsec:monix_sys}

Uno dei problemi di ECS risiede nella sua natura **poco
parallelizzabile**. Al fine di mantenere la **consistenza** fra le varie
entità, infatti, il framework richiede che l'**aggiornamento di gioco**
venga svolto **in maniera sequenziale** invocando il metodo `update()`
su ogni sistema. Relativamente all'implementazione del metodo
`update()`, invece, non vi sono restrizioni particolari e ciò garantisce
**ampio margine per ottimizzazioni**.

L'ottimizzazione proposta si basa sul reactive-framework `Monix` e
consiste essenzialmente nel **eseguire le operazioni sulle entità**
(collisioni) in modo **parallelo** splittando il Set in base al numero
di core disponibili.

### Risorse {#subsubsec:risorse}

Gli approfondimenti sono stati svolti grazie all'utilizzo delle seguenti
risorse:

-   **Libri:**

    -   **Learning Scala [@scalaLearning:2014]:** libro che riassume
        interamente le **principali features** del linguaggio Scala in
        ambito **funzionale**. È stato usato per consolidare alcune
        conoscenze pregresse.

    -   **Programming in Scala [@scalaBook:2014]:** rappresenta la
        bibbia di Scala ed è stato scritto dal grandissimo **Martin
        Odersky**.

    -   **Scala with Cats [@scalaCats:2020]:** libro che copre gli
        aspetti più **avanzati** del linguaggio Scala dal punto di vista
        **funzionale**. Per ogni singolo aspetto è fornita una
        **definizione teorica** e la relativa implementazione nella
        libreria ufficiale [`Cats`](https://typelevel.org/cats-effect/).
        È un libro particolarmente **complesso** ed è stato utilizzato
        come approfondimento.

    -   **Scala Cookbook [@scalaCook:2013]:** I **Cookbook** di O'Reilly
        sono conosciuti per essere estremamente **pragmatici**. Anche in
        questo caso il libro si configura come un'**enciclopedia del
        problem solving** dedicata interamente al linguaggio Scala.

    -   **Functional Programming in Scala [@functionalScala:2014]:**
        davvero una grande scoperta. Questo libro rappresenta un insieme
        di **buone pratiche** e **aspetti teorici** che ogni
        programmatore Scala dovrebbe conoscere. Personalmente di grande
        utilità sono stati i capitoli che trattano la **gestione degli
        errori** e gli aspetti funzionali più avanzati
        (`monoids, monads` e `applicative functors`).

-   **Conferenze:**

    -   **Scala Days:** Sono le conferenze ufficiali di Scala che ogni
        anno hanno luogo in un paese diverso. I talk proposti sono
        estremamente interessanti e permettono di apprendere un gran
        numero di **tecniche avanzate** e sopratutto costituiscono un
        ottimo esempio di **buona programmazione**. Conferenze
        consigliate:

        -   *[Functional Programming with Effects by Rob
            Norris](https://www.youtube.com/watch?v=30q6BkBv5MY)*

        -   *[Scala best practices I wish someone'd told me about -
            Nicolas
            Rinaudo](https://www.youtube.com/watch?v=DGa58FfiMqc)*

        -   *[Migrating to Scala 2.13 by Julien Richard Foy and Stefan
            Zeiger](https://www.youtube.com/watch?v=pHHKUKubs1Q&t=2002s)*

        -   *[Akka Streams to the Extreme - Heiko
            Seeberger](https://www.youtube.com/watch?v=CrpJJYPzdJE&t=630s)*

        -   *[Concurrent programming in 2019: Akka, Monix or ZIO? - Adam
            Warski](https://www.youtube.com/watch?v=TqJg4AuxEIQ)*

        -   *[Security with Scala Refined Types and Object Capabilities
            by Will
            Sargent](https://www.youtube.com/watch?v=wfbF5jQiAhQ)*

        -   *[A Tour of Scala 3 - Martin
            Odersky](https://www.youtube.com/watch?v=_Rnrx2lo9cw)*

    -   **Scalapeño:** come dice il nome stesso, sono **conferenze
        piccanti** che hanno lo scopo di smuovere le acque all'interno
        della comunità di Scala. Conferenze consigliate:

        -   *[The Last Hope for Scala's Infinity War - John A. De
            Goes](https://www.youtube.com/watch?v=v8IQ-X2HkGE)*

        -   *[Scala vs. Kotlin, friend or foe? - Ohad
            Shai](https://www.youtube.com/watch?v=Arwb6DSrWXE&t=102s)*

    -   **Altre conferenze:**

        -   *[John De Goes - 12 Steps To Better Scala
            (Part I)](https://www.youtube.com/watch?v=71yhnTGw0hY&feature=youtu.be)*

Ruben Ceroni
------------

Lo studente Ruben Ceroni, conclusa la parte iniziale di analisi e
progettazione comune si è concentrato sull'implementazione dei sistemi
core del gioco e della loro integrazione con il resto del sistema.

### AISystem

L'`AISystem` si occupa di generare gli spostamenti per le entità non
controllate dal giocatore dotate di intelligenza artificiale e quindi di
un AIComponent, nel quale è specificata la precisione dell'intelligenza
artificiale e i possibili bersagli della stessa.

Il core della logica di movimento è stato implementato in **Prolog**,
attraverso il predicato `move_avoiding(+Q,+(SX,SY),+(TX,TY),+O,-DX,-DY)`
che, prendendo in input una tupla (X,Y) di partenza e una di
destinazione, fornisce in output il vettore direzione da prendere per
arrivare alla destinazione. La precisione è influenzabile tramite
l'argomento Q, che esprime di quanto verrà falsata la posizione da
raggiungere fornita in input. L'array di posizioni O è necessario ad
evitare che più nemici con lo stesso bersaglio si scontrino
eccessivamente tra di loro inseguendolo. La direzione risultante
calcolata viene inserita nella stessa coda gestita dall'InputSystem che
quindi gestisce lo spostamento delle entità nemiche allo stesso modo dei
player.

### EndGameSystem

L'EndgameSystem si occupa di monitorare lo stato della partita e di
rimuovere le entità che escono dal bordo fornitogli in input o la cui
vita abbia raggiunto lo 0 a causa delle collisioni subite.
All'eliminazione di un'entità viene inviato tramite il mediator un
**LevelEndEvent** contenente lo status della partita, l'entità eliminata
e il punteggio ottenuto eliminandola. Nel caso si tratti di un'entità
nemica esso viene semplicemente rimosso dal gioco. Mentre se si tratta
di un'entità player o il player stesso rimane da solo in gioco, la
partita viene considerata conclusa e viene stoppato l'engine, mentre
lato view è mostrata la schermata di vittoria o di sconfitta.

### PowerUpSystem

Sono stati implementati 3 differenti tipi di powerUp.

L'attivazione di un powerUp è controllata dal **CollisionSystem**, che
alla collisione di una entità player con un powerUp ne inserirà il
riferimento all'interno del **PowerUpComponent** del powerUp.

Il comportamento specifico del singolo powerUp è specificato invece
all'in-terno del suo **PowerUpEffect**, tramite una funzione che
specifica come modificare il valore del componente modificato.

### Engine e GameLoop

L'Engine rappresenta la parte core del gioco, e si occupa di istanziare
i componenti principali e di registrare le entità del livello presso il
Coordinator. Il **GameLoop** è stato implementato come un thread
separato che durante la sua esecuzione chiamerà il metodo tick
dell'**UpdatableEngine** fornitogli in input, che porta
all'aggiornamento di tutti i sistemi e la produzione di un frame di
gioco. Per mantenere costante la frequenza di aggiornamento viene
calcolato il tempo trascorso per produrre il frame e nel caso sia
inferiore alla durata necessaria a mantenere gli fps costanti viene
fatto attendere il thread.

Gyordan Caminati
----------------

Lo studente Gyordan Caminati si è occupato prevalentemente nelle
seguenti macro-aree:

1.  **Manager**

2.  **Multiplayer**

3.  **View**

4.  **Controller**

### Manager

Lo studio e l'implementazione di tutti i **Manager** sono stati svolti
individualmente. In particolare, lo studente si è occupato delle
seguenti parti:

-   File Manager

-   Package Object

-   Audio Agent

-   Data Manager

-   Yaml Manager

#### File Manager {#file-manager}

Il File Manager permette di effettuare le operazioni di gestione dei
file, come, ad esempio, il caricamento da Jar, la cancellazione di una
cartella o la creazione di un albero delle cartelle. Il File Manager è
stato realizzato come un *Singleton* poiché si è ritenuto
concettualmente corretto che ne esistesse solo uno, visibile da
qualsiasi punto ci si trovi e che espone i metodi principali per la
gestione dei file.

#### Package Object

All'interno del package File, dove risiedono diversi manager che
necessitano di eseguire operazioni su file, si è ritenuto necessario
introdurre un Package Object che esponesse dei metodi per facilitarne la
gestione. Alcune delle operazioni da agevolare riguardavano, ad esempio,
l'utilizzo pervasivo di `Path`, `File` e `Stringhe` che identificano il
percorso in forma testuale. Nel **Package Object** sono inoltre presenti
anche tutte le costanti che servono a risalire al percorso dei file
testuali.

L'introduzione del Package Object ha migliorato notevolmente il flusso
di programmazione dato che il passaggio da `String` a `Path` è molto
intuivo e naturale. Lo stesso discorso può essere applicato anche per
`Path` e `File`. L'aggiunta di questi due metodi impliciti fornisce
gratuitamente il passaggio da `String` a `File`.

Data la **forte probabilità** di incappare in una `Exception` durante
una qualunque operazione I/O,si è deciso di sviluppare un ultimo metodo
che incapsulasse una `Try` e trasformasse l'eventuale `Exception` in un
`Boolean`, riportando successivamente su un **Log** l'accaduto.

``` {#lst:listato2222 .scala caption="Package Object" label="lst:listato2222"}
implicit def stringPathToPath(path: String): Path = Paths.get(path)

implicit def pathToFile(path: Path): File = path.toFile

def tryAndBoolResult[T](operation: => T)(Logger): Boolean =
  Try(operation).fold(error => {logger.warn(error.getMessage); false }, _ => true)
```

##### Frammento di codice dall'Package Object in nel package file.

#### Audio Agent

L'`Audio Agent` è il modulo preposto alla gestione dei suoni. Nonostante
se ne utilizzi effettivamente uno solo si è scelto di non renderlo un
**Singleton**, come è stato invece fatto con il `File Manager`. Alla
base di questa scelta vi è la volontà di non precludere estensioni
future.

Per la realizzazione dell'Agente, si è scelto di mantenere un approccio
più conservativo.

L'Agent mantiene al suo interno un `Thread` che manipola e riproduce
effetti e musica. La riproduzione di musica e effetti con un alta
frequenza, richiede notevoli risorse, l'unione del Thread a una coda di
messaggi(poi divenuta coda di eventi grazie all'apporto fornito da
Giulianini) consente un' ottima separazione dei flussi di controllo, e
coesione con altri Thread.

Nonostante l'implementazione attuale volga lo sguardo verso un approccio
generico, l'interfaccia lascia la strada aperta a successive
implementazioni, come Agent specifici per suoni ad alta qualità,
mantenendo sempre un approccio molto pulito e neutrale.

Il contributo di design apportato dal collega **Giulianini** ha
consentito di trasformare il modello a messaggi, in un modello ad
eventi. In questo modo si è riusciti a rendere il tutto più pulito e ad
evitare un match case che avrebbe sporcato l'implementazione.

#### Yaml Manager

La serializzazione e la deserializzazione di tutti i dati **Locali** è
gestita unicamente dallo **Yaml Manager**. Esso fornisce solo poche
funzioni generiche, astraendo e delegando ad un livello superiore la
concatenazione e l'utilizzo delle stesse.

La **Serializzazione** è effettuata principalmente utilizzando il
formato `Yaml`. Inizialmente è stato valutato anche l'utilizzo di
`Json`, ma quest'ultimo risultava più prolisso e meno leggibile. Per
questo motivo si è preferito scegliere Yaml. Questa decisione è stata
guidata anche dal fatto che il **livello** (la principale fonte di
serializzazione) è composto prevalentemente da una lista di `Entity` e
alcuni parametri. Le liste in `Yaml` sono particolarmente leggibili.

Per la serializzazione si è scelto di utilizzare un serializzatore
basato su `Jackson`, perché esso è molto veloce. `Jackson`, inoltre, ha
consentito una scrittura pulita dei dati da serializzare. Normalmente
per la serializzazione di una classe, sarebbe necessario l'utilizzo
pervasivo di annotazioni come, ad esempio: `@JsonProperty` o
`@JsonFormat`; tuttavia la definizione di dati snelli e l'utilizzo di un
`PolymorphicTypeValidator` hanno consentito di serializzare e
deserializzare senza la necessità di ricorrere ad annotazioni.

#### Data Manager

La gestione di tutti i dati è demandata al **Data Manager** il quale
fornisce metodi diretti per il salvataggio e il caricamento di tutti i
file testuali del progetto come: livelli, punteggi e impostazioni. Il
caricamento e il salvataggio dei livelli può avvenire sia nel **File
System** sia nel **Jar**.

### View {#view}

Lo studente si è occupato in particolare dello sviluppo di tutte le
schermate ad eccezione di **Level** e **Game**. Ogni schermata si
appoggia sopra l'architettura base sviluppata dal collega
**Giulianini**. Tutte le view utilizzano il pattern `Observer`.

Di seguito, le schermate che lo studente ha realizzato e gestito:

-   Stats

-   Settings

-   ModeSelection

-   Home

-   Lobby

#### Stats

Una semplice schermata che fornisce all'utente una visuale su tutti i
record degli utenti registrati al sistema. Chiede al **Controller** la
tabella dei record e la mostra.

#### Settings

La schermata adibita alle impostazioni, che appoggia sul Controller per
le operazioni di IO. Essa consente al giocatore di cambiare: Nome,
Difficoltà e volume di suoni e musica. Quando un giocatore cambia nome,
può inserire anche un nome già utilizzato in precedenza; in questo caso
ulteriori nuovi record con quel nome sovrascriveranno il precedente.

#### ModeSelection

La schermata di ModeSelection separa la **Home** dal **Game**. Essa
permette di scegliere se diventare un **Client** o un **Server**. Nel
primo caso è necessario fornire un IP e una porta per potersi connettere
al server; mentre nel secondo caso verranno scelta una porta libera e un
interfaccia di rete disponibile su cui far connettere i client. Il
controllo dell'input consente di evitare inserimenti erronei e le
notifiche avvisano il giocatore nel caso in cui il suo nome sia già
presente in partita oppure il server sia pieno.

Nel caso in cui si cerchi di contattare un server su un indirizzo
sbagliato, verrà notificato un messaggio di timeout.

#### Home

La schermata iniziale presenta sullo sfondo un tema a griglia e consente
all'utente di navigare attraverso tutte le opzioni.

#### Lobby

La schermata di lobby mostra un notevole numero di informazioni; l'IP
del server e la sua porta, la lista di giocatori pronti e non pronti. Il
server ha inoltre il potere di espellere giocatori a piacimento, un
eventuale giocatore espulso riceverà una notifica di allontanamento.

Quando tutti i giocatori presenti nella lobby sono pronti, il server può
far partire la partita. È possibile partire anche con un numero
inferiore di giocatori, a patto che siano tutti pronti.

##### Ogni bottone presente nelle view quando premuto accoda un evento al `SoundAgent` che lo applica. Le varie view sviluppate dallo studente non possono comunicare tra loro, e l'unico punto di contatto rimane sempre il controller, tramite l'interfaccia dell'observer ObservableUI.

### Controller

Il Controller contiene la struttura dati della lobby, usata per il
mantenimento di una lobby durante la fase preliminare di una partita.
Contiene tutta la configurazione di akka e anche un attore. Non vi sono
mai due attori aperti in contemporanea, mentre è possibile che non siano
presenti attori(Single Player). Mantiene anche il `Mediator` che però
non utilizza direttamente. Internamente utilizza anche il **Data
Manager** che viene impiegato per il caricamento e la serializzazione di
tutti i dati. Contiene anche l'**Engine** e il **Sound Agent**, i quali
sono comandati direttamente dal controller stesso.

Il controller è suddiviso in quattro Interfacce:

-   `ActorController`

-   `EngineController`

-   `ObservableUI`

-   `SoundController`

L'interfaccia `SoundController` viene estesa da `EngineController`,
ActorController e ObservableUI; così facendo il controller fornisce un
punto di ingresso al metodo `redirectSoundEvent` che consente di
accodare un evento che successivamente verrà eseguito.

L'interfaccia `EngineController` estende il `SoundController`; di
conseguenza, oltre a fornire la possibilità di accodare `MediaEvent`,
fornisce anche un getter per il `Mediator`, così l'`Engine` che lo
contiene può sottoscriversi, ma può anche passare l'EngineController ad
alcuni dei suoi come: `CollisionSystem` e `PowerUpSystem`, i quali ne
faranno uso per pubblicare eventi sul `Mediator` e inviare eventi
all'`AudioAgent`.

L'interfaccia `ActorController` mette a disposizione degli attori i
metodi necessari per instaurare una partita, gestirla e terminarla.
Inoltre fornisce anche la possibilità agli attori di inviare alla lobby
tramite un metodo generico una **strategia** per interrogarne e
manipolarne direttamente il contenuto.

``` {#lst:listato212 .scala caption="Actor Controller" label="lst:listato212"}
override def sendToLobbyStrategy[T](strategy: MultiPlayerSetup => T): T = strategy.apply(matchSetupMp.get)

override def sendToViewStrategy(strategy: ObserverUI => Unit): Unit =
  observers.foreach(obs => Platform.runLater(() => strategy(obs)))
```

Allo stesso modo ma senza ritorno alcuno, fornisce la possibilità di
inviare una strategia verso la View, nella quale incapsula un evento che
viene gestito poi dalla view stessa tramite `notify`.

### Multiplayer

Lo studente si è occupato prevalentemente dell'integrazione di
`ClientActor` e `Server Actor`.

Entrambi gli attori comunicano con l'`Actor controller` chiamando metodi
su di esso; mentre tra di loro comunicano tramite scambio di messaggi.
Sono presenti diversi messaggi e sono gestiti in `Behaviour` ben
precisi.

Dato che entrambi gli attori dovevano riportare un log nel caso in cui
avessero ricevuto un messaggio fuori dal `Behaviour` corretto e che
entrambi dovevano gestire il messaggio `PlayMediaMessage` (Inviato dal
server per permettere al client di riprodurre suoni come collisioni e
vittoria) è stato ritenuto necessario introdurre un `ActorWithLogging`.
Questa classe astratta estende `Actor` e `ActorLogging` e fornisce un
metodo `changeBehaviourWhitLogging` che viene utilizzato
alternativamente alla `context.become`. Questa funzione concatena la
`PartialFunction` `Receive` fornita in input(Behaviour) e fornisce in
uscita una `PartialFunction` che è di fatto esaustiva dato che effettua
un match su tutto e effettua una operazione di log.

Questo consente di extendere il `Behaviour` passato e ottenere per ogni
caso non gestito la certezza di un log, evitando così anche errori.

Inoltre è possibile introdurre un ulteriore `Behaviour` di default, che
verrà chiamato dopo il classico `Behaviour`, ma prima di quello
esaustivo.

Nel caso del server il `Behaviour` di default introdotto ridireziona
tutti i `PlayMediaMessage` verso i suoi client. Nel caso del Client il
`PlayMedia-Message` viene inviato al `SoundAgentSoundAgent` il quale lo
consumerà lanciando il media.

``` {#lst:listato22 .scala caption="Actor Controller" label="lst:listato22"}
override def sendToLobbyStrategy[T](strategy: MultiPlayerSetup => T): T = strategy.apply(matchSetupMp.get)

override def sendToViewStrategy(strategy: ObserverUI => Unit): Unit =
  observers.foreach(obs => Platform.runLater(() => strategy(obs)))
```

##### Contributi esterni

Lo studente ha contribuito all'implementazione delle strutture dati
principali del model come : `MatchSetup`(lobby), `Difficulties` e
`Settings`. Inoltre ha prodotto la prima implementazione di difficoltà,
poi rifinita da **Giulianini**.

Retrospettiva
=============

Processo di Sviluppo
--------------------

Durante le fasi iniziali di analisi dei requisiti e durante la Sprint 0
ci si è appoggiati al tool **Trello** per tenere traccia dei task da
eseguire e degli artefatti prodotti.

In seguito, entrati nel vivo del progetto, si è deciso di utilizzare ai
**Project** di **GitHub**, che mettono a disposizione un kanban virtuale
come trello, ma completamente integrato con le issue di github e
automatizzabile.

Una volta completata la fase iniziale e definiti gli item del backlog,
essi sono stati inseriti in un **GitHub Project** relativo
all'organizzazione GitHub creata per il progetto, consultabile
all'indirizzo <https://github.com/orgs/Unibo-PPS-1920/projects/2>.

Sotto la stessa organizzazione sono stati creati sia il repository che
contiene la relazione che quello contenente l'effettivo progetto. Per
ogni sprint è stato creato un nuovo github project in cui
ddddddddddddddsono stati importati gli **item** del backlog relativi
alla sprint dal project globale.

Questo approccio ha consentito di avere una visione pulita dello stato
del progetto a livello alto e una visione più granulare a livello di
sprint.

Backlog {#backlog}
-------

Ogni item del backlog è stato formulato sotto forma di **User story**,
dopo avere selezionato gli item da completare durante lo sprint
planning, essi vengono tradotti in uno o più sotto-task implementativi.

Iterazioni
----------

### Sprint 0

A questo sprint è stato assegnato il numero 0 perchè non propriamente
parte del processo di sviluppo iterativo, ma fondamentale per la
produzione di solide basi per gli sprint successivi.

#### Svolgimento

Sono stati identificati i pattern architetturali applicabili e
sviluppati in dettaglio i modelli delle parti principali del sistema

### Sprint 1

#### Svolgimento

In questo sprint ci si è concentrati sul setup del progetto, in
particolare di **Travis CI** e di **Gradle**, l'implementazione dello
scheletro modellato nello sprint precendente. In particolare sono stati
implementati i componenti principali di ECS e il game engine.

### Sprint 2

L'obiettivo di questa sprint è stato quello di mostrare una schermata
all'uten-te con cui esso possa interagire.

#### Svolgimento

Lato view è stata sviluppata l'architettura principale MVC, il menu
principale e il canvas. Sono stati aggiunti i 3 system principali:
InputSystem, DrawSystem e MovementSystem.

#### Considerazioni

Questo sprint è stato terminato con un leggero ritardo dovuto alla mole
di lavoro necessaria a raggiungere l'obiettivo prefissatosi.

### Sprint 3

L'obiettivo di questa sprint è stato quello di introdurre le feature
mancanti dell'esperienza base del gioco.

#### Svolgimento

Sono state introdotte le componenti relative alla gestione degli scontri
e l'intelligenza artificiale dei nemici, la gestione dei powerUp e la
riproduzione dei suoni.

#### Considerazioni

Questo sprint si è rivelato più corposo del previsto, principalmente
dovuto a un'astrazione non perfetta delle componenti di fisica, che
hanno portato a un parziale redesign delle stesse all'introduzione del
collision system.

### Sprint 4

In questo sprint ci si è concentrati sull'aggiunta degli aspetti più
avanzati come il multiplayer e sulla pulizia finale del codice

#### Svolgimento

È stato completato e rifinito il gioco. Sono state portate a termine la
parte di integrazione con il multiplayer, la definizione dei livelli,
l'aggiunta della durata vitale e del danno, il completamento e la
revisione della documentazione, l'individuazione e la correzione di bug,
il refactoring e la pulizia del codice.

[^1]: Questo avviene solamente quando la frequenza di invio dei comandi
    supera la frequenza di aggiornamento di gioco.
