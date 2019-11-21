# design-system
Design system methodology

Il caso del CSS

Il CSS è un prodotto corredato da una serie di suite prive di identità, tutte divergenti tra loro e con una scarsa esperienza utente.

Entrando nel dettaglio del progetto CSS, ci si accorge che oltre ad avere una GUI poco consistente, risulta assente anche un’ architettura modulare che permetta il riutilizzo dei moduli nello sviluppo della UI. Per questo motivo le funzionalità esistenti non sono scalabili e di difficile manutenzione e soprattutto aumenta il rischio di impossibilità di implementazione su evolutive di progetto.

Partendo da queste difficoltà ho iniziato a lavorare ad una soluzione scalabile e flessibile, creando un design system.

Dato il ritmo con cui cresce la soluzione CSS è diventato imperativo e fondamentale mantenere una buona esperienza utente. Con ogni nuova funzionalità che viene rilasciata, l’obiettivo dovrebbe essere quello di poter utilizzare altrettanti componenti esistenti in modo da non introdurre incoerenze di UI e UX e di aderire al principio del DRY (Don’t Repeat Yourself). Indipendentemente dal fatto che si tratti di  pixel, codice o flussi di navigazione, è utile disporre di un sistema di progettazione in atto: viene rivelato il suo vero valore. Il team di sviluppo del prodotto è libero di concentrarsi sulla risoluzione di problemi senza dover più perdere tempo a ripensare a come creare scenari di componenti e app comuni. Inoltre nei team che lavorano in parallelo si eviterebbe di ricreare ripetutamente gli stessi elementi dell'interfaccia utente, ha un impatto reale sul progetto in termini di maggiore time-to-market e risparmi sui costi. Il risultato finale è un prodotto migliore per gli utenti.


Processo di creazione del design system CSS

Ecco alcuni principi fondamentali del processo di creazione del design system:

- UCD (User centered design):  Si vuole garantire che ogni interazione che i nostri utenti hanno con il nostro prodotto sia positiva e risolva il compito per cui è stato pensato, creando così una forte connessione con il nostro prodotto su più piattaforme (suites).

- Adattabilità: sulla base degli uses cases, i nostri operatori risultano essere utenti/operatori con un livello di esperienza in alcuni casi alto e in altri più basso - sia per quanto riguarda la conoscenza di dominio dell’applicazione sia nell’utilizzo di supporti informatici - per questo si è pensato di costruire una piattaforma che sia adattabile anche in base al livello di esperienza dell’utente/operatore facendo affidamento su modelli di progettazione comuni esistenti (pattern design) che sono intuitivi nella forma, nella funzione e nel flusso, garantendo un'interfaccia più user-friendly per tutti

- Coerenza: aumentiamo la familiarità e rafforziamo l'intuizione consentendo all'utente di sapere come funziona un elemento semplicemente vedendolo perché sa che elementi simili sembrano uguali e vengono utilizzati allo stesso modo.

- Semplicità: I nostri prodotti sono basati sul web, ricchi di dati e micro interazioni. Semplicità, leggibilità e tempi di caricamento sono fondamentali. Per cui si ritiene necessario un’interfaccia chiara e pulita.


Partendo dalla metodologia “Atomic Design” di Brad Frost è stato eseguito un mapping nel nostro design system, tuttavia è stato necessario declinarne la sua applicazione a favore di una maggiore aderenza ad uno sviluppo con elementi di stile di base e costruzioni di micro-components:

[IMMAGINE]

Settings

I settings sono le linee guida del Brand, che definiscono la tipografia, la palette di colori, le icone, la spaziatura, l’ombra e più in generale l’architettura dell’informazione del nostro design system

I settings sono suddivisi in “behavior” come ad es. lo scorrimento, la spaziatura, numero di caratteri per la troncatura del testo, etc. In modo tale che designer e sviluppatori possano riferirsi ad esso e lo rispettino durante la creazione di nuovi modelli.
E poi ci sono i “basics” come tipografia, colori, ombreggiatura e sistema di icone.

Elements

Gli elementi nella maggior parte dei casi unità indivisibili, ma nel nostro sistema di progettazione il range si estende ai micro-components, ovvero componenti composti da due o più unità nel linguaggio Html ma che nella UI vengono rappresentati come singoli (per esempio un pulsante toggle necessita di una struttura più articolata rispetto ad una semplice checkbox).

Components

I componenti sono suddivisi in “components” e “global (components)”.  I componenti si riferiscono all’insieme di elementi della UI distintivi che vengono utilizzati più volte durante lo sviluppo del prodotto, normalmente utilizzati per svolgere una funzione o talvolta solo per trasmettere significato (blocco informativo). I “global components”, invece, sono un insieme di componenti presenti in ogni vista/pagina dell’applicativo: header, footer, sidebar, main wrapper.

Tutti questi componenti sono archiviati in un repository condiviso, denominato libreria che permette di creare un’interfaccia utente coerente e accelerare lo sviluppo dell’app. La coerenza nella UI aumenta la familiarità con l’applicativo per gli utenti riducendo al minimo la confusione nell’interazione col nostro prodotto. 
  
Templates

Dopo aver definito le basi, raccogliamo tutti i componenti di base, che vengono quindi utilizzati per creare frammenti più complessi, riutilizzabili e scalabili chiamati pattern o template, mostrando la struttura del contenuto sottostante del design.

Pages

Le pagine, che nel nostro sistema sono le viste dell’applicazione (web app), sono lo stage per la variazione dei template (alcune viste posso condividere lo stesso modello/layout ma differenziarsi per colori e contenuti o nel nostro caso gli utenti con privilegi di amministratore potrebbero vedere pulsanti e opzioni aggiuntivi sulla propria o dashboard rispetto agli utenti che non sono amministratori)

App

App è il contenitore dell’applicazione, il quale potrebbe essere anche parte di un prodotto e non solo il prodotto stesso.Il caso del CSS

Il CSS è un prodotto corredato da una serie di suite prive di identità, tutte divergenti tra loro e con una scarsa esperienza utente.

Entrando nel dettaglio del progetto CSS, ci si accorge che oltre ad avere una GUI poco consistente, risulta assente anche un’ architettura modulare che permetta il riutilizzo dei moduli nello sviluppo della UI. Per questo motivo le funzionalità esistenti non sono scalabili e di difficile manutenzione e soprattutto aumenta il rischio di impossibilità di implementazione su evolutive di progetto.

Partendo da queste difficoltà ho iniziato a lavorare ad una soluzione scalabile e flessibile, creando un design system.

Dato il ritmo con cui cresce la soluzione CSS è diventato imperativo e fondamentale mantenere una buona esperienza utente. Con ogni nuova funzionalità che viene rilasciata, l’obiettivo dovrebbe essere quello di poter utilizzare altrettanti componenti esistenti in modo da non introdurre incoerenze di UI e UX e di aderire al principio del DRY (Don’t Repeat Yourself). Indipendentemente dal fatto che si tratti di  pixel, codice o flussi di navigazione, è utile disporre di un sistema di progettazione in atto: viene rivelato il suo vero valore. Il team di sviluppo del prodotto è libero di concentrarsi sulla risoluzione di problemi senza dover più perdere tempo a ripensare a come creare scenari di componenti e app comuni. Inoltre nei team che lavorano in parallelo si eviterebbe di ricreare ripetutamente gli stessi elementi dell'interfaccia utente, ha un impatto reale sul progetto in termini di maggiore time-to-market e risparmi sui costi. Il risultato finale è un prodotto migliore per gli utenti.


Processo di creazione del design system CSS

Ecco alcuni principi fondamentali del processo di creazione del design system:

- UCD (User centered design):  Si vuole garantire che ogni interazione che i nostri utenti hanno con il nostro prodotto sia positiva e risolva il compito per cui è stato pensato, creando così una forte connessione con il nostro prodotto su più piattaforme (suites).

- Adattabilità: sulla base degli uses cases, i nostri operatori risultano essere utenti/operatori con un livello di esperienza in alcuni casi alto e in altri più basso - sia per quanto riguarda la conoscenza di dominio dell’applicazione sia nell’utilizzo di supporti informatici - per questo si è pensato di costruire una piattaforma che sia adattabile anche in base al livello di esperienza dell’utente/operatore facendo affidamento su modelli di progettazione comuni esistenti (pattern design) che sono intuitivi nella forma, nella funzione e nel flusso, garantendo un'interfaccia più user-friendly per tutti

- Coerenza: aumentiamo la familiarità e rafforziamo l'intuizione consentendo all'utente di sapere come funziona un elemento semplicemente vedendolo perché sa che elementi simili sembrano uguali e vengono utilizzati allo stesso modo.

- Semplicità: I nostri prodotti sono basati sul web, ricchi di dati e micro interazioni. Semplicità, leggibilità e tempi di caricamento sono fondamentali. Per cui si ritiene necessario un’interfaccia chiara e pulita.


Partendo dalla metodologia “Atomic Design” di Brad Frost è stato eseguito un mapping nel nostro design system, tuttavia è stato necessario declinarne la sua applicazione a favore di una maggiore aderenza ad uno sviluppo con elementi di stile di base e costruzioni di micro-components:

[IMMAGINE]

Settings

I settings sono le linee guida del Brand, che definiscono la tipografia, la palette di colori, le icone, la spaziatura, l’ombra e più in generale l’architettura dell’informazione del nostro design system

I settings sono suddivisi in “behavior” come ad es. lo scorrimento, la spaziatura, numero di caratteri per la troncatura del testo, etc. In modo tale che designer e sviluppatori possano riferirsi ad esso e lo rispettino durante la creazione di nuovi modelli.
E poi ci sono i “basics” come tipografia, colori, ombreggiatura e sistema di icone.

Elements

Gli elementi nella maggior parte dei casi unità indivisibili, ma nel nostro sistema di progettazione il range si estende ai micro-components, ovvero componenti composti da due o più unità nel linguaggio Html ma che nella UI vengono rappresentati come singoli (per esempio un pulsante toggle necessita di una struttura più articolata rispetto ad una semplice checkbox).

Components

I componenti sono suddivisi in “components” e “global (components)”.  I componenti si riferiscono all’insieme di elementi della UI distintivi che vengono utilizzati più volte durante lo sviluppo del prodotto, normalmente utilizzati per svolgere una funzione o talvolta solo per trasmettere significato (blocco informativo). I “global components”, invece, sono un insieme di componenti presenti in ogni vista/pagina dell’applicativo: header, footer, sidebar, main wrapper.

Tutti questi componenti sono archiviati in un repository condiviso, denominato libreria che permette di creare un’interfaccia utente coerente e accelerare lo sviluppo dell’app. La coerenza nella UI aumenta la familiarità con l’applicativo per gli utenti riducendo al minimo la confusione nell’interazione col nostro prodotto. 
  
Templates

Dopo aver definito le basi, raccogliamo tutti i componenti di base, che vengono quindi utilizzati per creare frammenti più complessi, riutilizzabili e scalabili chiamati pattern o template, mostrando la struttura del contenuto sottostante del design.

Pages

Le pagine, che nel nostro sistema sono le viste dell’applicazione (web app), sono lo stage per la variazione dei template (alcune viste posso condividere lo stesso modello/layout ma differenziarsi per colori e contenuti o nel nostro caso gli utenti con privilegi di amministratore potrebbero vedere pulsanti e opzioni aggiuntivi sulla propria o dashboard rispetto agli utenti che non sono amministratori)

App

App è il contenitore dell’applicazione, il quale potrebbe essere anche parte di un prodotto e non solo il prodotto stesso.
