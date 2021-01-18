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
 - ACTIVITY COMPLETO PER TUTTI GLI UTENTI DEL SISTEMA
 - SEQUENCE DIAGRAM
 - CLASS DIAGRAM
 - ### QUALITY ASSURANCE
 - TEST SELECTION (SCENARI E DATI)
 - TEST COVERAGE (UNIT TEST)
 - ### SCELTE IMPLEMENTATIVE 
#
# REQUISITI
Al fine di garantire la praticità a tutti gli utenti, il sistema di cliniche prevede un'applicazione utilizzabile sia da computer sia da smartphone. 
Il sistema gestisce in un database un sistema di cliniche diurne, i pazienti ospitati e consente diversi tipi di accesso e attività consentite. Le cliniche in gestione sono sia strutture diurne, come comunità, in cui i pazienti si recano per svolgere attività ricreative, incontrare medici specialisti e ricevere le cure adeguate, sia cliniche ospedaliere.
Le informazioni dei pazienti riguardano i dati personali, le cartelle cliniche, i trattamenti ricevuti, per esempio prescrizione di farmaci o visite mediche. Questi dati sono soggetti al trattamento della privacy, per cui il tutore o il paziente stesso firmano il modulo di consenso. Inoltre il manager delle cliniche ha il consenso a rilasciare i dati alle forze dell'ordine, per compiere indagini giudiziarie o processi.
Il paziente non ha alcun tipo di interazione con il sistema, perciò è necessario memorizzare il contatto di un parente o tutore, che sarà usato in caso di urgenze o allarmi. Alcuni di questi casi sono: 
 - il paziente può compiere azioni pericolose per se stesso o per gli altri
 - il paziente può perdersi nella clinica
 - il paziente può dimenticare (volontariamente) una visita
 - il paziente può perdere (volontariamente) la prescrizione
 In queste situazioni un medico o infermiere dovrà segnalare l'accaduto tramite un allert nel sistema.
 Gli utenti del sistema sono:
 - staff medico: medici, infermieri e infermieri a domicilio
 - staff non medico: receptionist, IT e manutentori, amministratore

# SCENARI

 1. SEGNALAZIONE DI ALLERT
 Un medico o un infermiere può segnalare una situazione urgente o di pericolo per un certo paziente. L'allarme viene lanciato inserendo l'allert dall'applicazione cellulare o da computer. La chiamata arriva sia ai colleghi sia al parente del paziente, di cui si ha memorizzato il numero nel database;
 
 2. UTILIZZO DA PARTE DEL MEDICO CURANTE
 I medici possono accedere al database con login medica e password, dalla propria area privata vedono la lista di pazienti e possono aggiornare la cartella clinica di ognuno. Nella cartella devono inserire la diagnosi con l'eventuale stato di pericolosità e le terapie (farmacologiche e psicologiche) prescritte e somministrate. Dalla home possono vedere e stampare lo storico di ogni paziente;
 
 3. UTILIZZO DA PARTE DELL'INFERMIERE
 Gli infermieri possono accedere al database con login medica e password, dalla propria area privata vedono la lista di pazienti e possono aggiornare la cartella clinica di ognuno. Nella cartella devono inserire lo svolgimento delle terapie psicologiche e la somministrazione dei farmaci prescritti. Dalla home possono vedere e stampare lo storico di ogni paziente;
 
 4. UTILIZZO DA PARTE DELLA RECEPTIONIST
 Le receptionist accedono al sistema con la propria login e password e possono vedere l'agenda e il calendario di ogni medico per prendere gli appuntamenti con i pazienti o con i loro famigliari;
 
 5. UTILIZZO DA PARTE DEL MANAGER DELLE CLINICHE
Il manager ha accesso come amministratore e può inserire un nuovo paziente, creandone la cartella clinica, in questa fase farà firmare il modulo per il trattamento dei dati personali e il consenso di fornire informazioni necessarie a eventuali indagini.
