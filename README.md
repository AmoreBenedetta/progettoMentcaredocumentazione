# **DOCUMENTAZIONE PROGETTO: MENTCARE**
## ESAME DI INGEGNERIA DEL SOFTWARE
### Studente: Amore Benedetta
### Matricola: VR 445458
### Docente: Mariano Ceccato
### Anno Accademico: 2020/2021

#  
## INDICE

 - ### REQUISITI
 - ### SCENARI
 - ### DESIGN
 - USE CASE COMPLETO DI TUTTI GLI UTENTI DEL SISTEMA
 - ACTIVITY PER MEDICO
 - SEQUENCE DIAGRAM PER CONTROLLER
 - CLASS DIAGRAM PER LE CLASSI IMPLEMENTATE
 - ### QUALITY ASSURANCE
 - TEST SELECTION (SCENARI E DATI)
 - TEST COVERAGE (UNIT TEST)
 - ### SCELTE IMPLEMENTATIVE 
 - TOOL DI SVILUPPO
#
# REQUISITI
Siamo di fronte ad un sistema di cliniche che, al fine di garantire la praticità a tutti gli utenti, prevede un'applicazione utilizzabile sia da computer sia da smartphone. 
L'applicazione gestisce in un database un sistema di cliniche diurne, i pazienti ospitati e visitati e consente diversi privilegi di accesso. Le cliniche in gestione sono sia strutture diurne, come comunità, in cui i pazienti si recano per svolgere attività ricreative, incontrare medici specialisti e ricevere le cure adeguate, sia cliniche ospedaliere.
Le informazioni dei pazienti riguardano i dati personali, le cartelle cliniche, i trattamenti ricevuti, per esempio prescrizione di farmaci o visite mediche. Questi dati sono soggetti al trattamento della privacy, per i quali il tutore o il paziente stesso firmano il modulo di consenso. Inoltre il manager delle cliniche ha il consenso a rilasciare i dati alle forze dell'ordine, per compiere indagini giudiziarie o processi.
Il paziente non ha alcun tipo di interazione con il sistema, perciò è necessario memorizzare il contatto di un parente o tutore, che sarà usato in caso di urgenze o allarmi. Alcuni di questi casi sono: 
 - il paziente può compiere azioni pericolose per se stesso o per gli altri
 - il paziente può perdersi nella clinica
 - il paziente può dimenticare (volontariamente) una visita
 - il paziente può perdere (volontariamente) la prescrizione
In queste situazioni un medico o un infermiere dovrà segnalare l'accaduto tramite un allert nel sistema.
 Gli utenti del sistema sono:
 - staff medico: medici, infermieri e infermieri a domicilio
 - staff non medico: receptionist, IT e manutentori, amministratore
 
UTILIZZO DA PARTE DEL MEDICO CURANTE
I medici possono accedere al database con login medica e password, dalla propria area privata vedono la lista di pazienti e possono aggiornare la cartella clinica di ognuno. Nella cartella devono inserire la diagnosi con l'eventuale stato di pericolosità, le visite con eventuali prescrizioni (farmacologiche e psicologiche) e possono segnalare situazioni di pericolo (allert). Inoltre possono vedere e stampare lo storico di ogni paziente.

UTILIZZO DA PARTE DELL'INFERMIERE
Gli infermieri possono accedere al database con login e password, dalla propria area privata vedono la lista di pazienti e possono aggiornare la cartella clinica di ognuno. Nella cartella devono inserire lo svolgimento delle terapie psicologiche, la somministrazione dei farmaci prescritti e possono segnalare un allert. Inoltre possono vedere e stampare lo storico di ogni paziente.
 
UTILIZZO DA PARTE DELLA RECEPTIONIST
Le receptionist accedono al sistema con la propria login e password e possono vedere l'agenda di ogni medico, per prendere gli appuntamenti con i pazienti o con i loro famigliari.
 
UTILIZZO DA PARTE DEL MANAGER DELLE CLINICHE
Il manager ha accesso come amministratore e può inserire un nuovo paziente, creandone la cartella clinica, in questa fase fa firmare il modulo per il trattamento dei dati personali e il consenso di fornire informazioni necessarie a eventuali indagini. Quando un paziente finisce la cura la cartella verrà archiviata. Il manager potrà vedere un report mensile relativo all'andamento economico delle cliniche e al numero di pazienti in terapia.
Nello specifico il report contiene il numero di pazienti in ogni clinica diurna, il numero di pazienti che sono stati registrati e il numero di pazienti che hanno concluso le cure, il numero di pazienti visitati nelle cliniche ospedaliere e, per ogni clinica, il totale del costo dei farmaci prescritti e somministrati, suddivisi in dosi. 

#
# SCENARI (MEDICO)

 1. Allert: un medico può segnalare una situazione urgente o di pericolo per un certo paziente. L'allarme viene lanciato inserendo l'allert. La chiamata arriva sia ai colleghi sia al parente del paziente, di cui si ha memorizzato il numero nel database;
 2. Visualizzazione della lista dei pazienti (Homepage);
 3. Aggiornamento della cartella clinica di un paziente inserendo la diagnosi e la pericolosità;
 4. Aggiornamento della cartella clinica di un paziente a seguito di una visita e eventuale prescrizione;
 5. Visualizzazione e stampa dello storico di ogni paziente.
 

#
# DESIGN
## USE CASE
### MEDICO
Le attività previste per lo staff medico sono:
 - Accesso al sistema con login e password mediche;
 - Nella homepage, visualizzare la lista di pazienti;
 - Dalla homepage, aprire la cartella clinica dei pazienti; 
 - Dalla cartella clinica inserire le diagnosi, le visite effettuate con eventuali terapie prescritte;
 - Dalla cartella clinica, segnalare un allert nel caso di situazione critica;
 - Dalla homepage, stampare lo storico di un paziente.

### INFERMIERE e INFERMIERE A DOMICILIO
Le attività previste per gli infermieri sono:
 - Accesso al sistema con login e password sub-mediche;
 - Nella homepage, visualizzare la lista di pazienti;
 - Dalla homepage, aprire la cartella clinica dei pazienti;
 - Dalla cartella clinica inserire le attività svolte e i farmaci somministrati;
 - Dalla cartella clinica, segnalare un allert nel caso di situazione critica; 
 - Dalla homepage, visualizzare e stampare lo storico di un paziente.
 
### RECEPTIONIST
Le attività previste per le receptionist sono:
 - Accesso al sistema con login e password semplici;
 - Nella homepage, visualizzare l'agenda di ogni medico;
 - Inserire un appuntamento con un paziente o con un famigliare/tutore.
 
### MANAGER
Le attività previste per il manager sono:
 - Accesso al sistema con login e password da amministratore;
 - Inserire un nuovo paziente e creare una cartella clinica contenente l'anagrafica e il modulo per la privacy;
 - Archiviare la cartella clinica dei pazienti che concludono il trattamento;
 - Visualizzare lo storico del paziente ed esportarlo su richiesta;
 - Visualizzare il report mensile amministrativo ed economico.

#
## ACTIVITY DIAGRAM

#
## SEQUENCE DIAGRAM


#
## CLASS DIAGRAM


#
# QUALITY ASSURANCE
## TEST SELECTION

## TEST COVERAGE

#
# SCELTE IMPLEMENTATIVE
Il patter su cui si basta il nostro progetto è Spring-MVC, in cui il Controller gestisce le azioni che può compiere un medico, una volta loggato; il Model è un database di pazienti, visite e prescrizioni; il View è l'interfaccia con il medico, creata in HTML.
Abbiamo scelto questo pattern strutturale in quanto si adatta alla nostra piattaforma web e all'utilizzo della stessa sia su computer sia su smartphone, in quanto l'interfaccia può subire delle variazioni, ed è richiesta tra i requisiti l'interazione diretta tra i medici e un famigliare/tutore del paziente.
Inoltre Spring-MVC consente di dividere nettamente la parte di visualizzazione e gestione della base di dati, che può aumentare o diminuire indipendentemente dal resto del sistema.
Abbiamo scelto di implementare per intero la parte di controllo sulle attività che può svolgere il medico, su cui sono stati eseguiti tutti i casi di test.
In fase di implementazione, abbiamo evitato di gestire il login del medico e la parte grafica, al fine di concentrarci sul controller e sui test.

## TOOL DI SVILUPPO
Per lo sviluppo della nostra applicazione abbiamo usato il tool IntelliJ, proposto a lezione.
Abbiamo scelto di implementare l'interfaccia web in HTML, per quanto riguarda l'impaginazione e la grafica, in JavaScript abbiamo fatto i controlli sui form di inserimento e il codice lo abbiamo scritto in Java. Come requisito abbiamo sviluppato in gradle la parte di compilazione e testing del software.
Le versioni del software le abbiamo condivise in modo centralizzato su OneDrive, per scaricarle e aggiornarle in locale, invece la condivisione del progetto finito è avvenuta su github.
I diagrammi UML li abbiamo creati con il tool on-line genmymodel e li abbiamo importati nella documentazione.
Per scrivere la documentazione in formato .md abbiamo usato il tool on-line stackedit.
