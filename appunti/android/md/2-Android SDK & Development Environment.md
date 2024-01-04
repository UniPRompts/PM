
```toc
```

## Android SDK

### Android Studio

Android Studio è il nuovo ambiente di sviluppo integrato (IDE) ufficiale per lo sviluppo delle applicazioni Android, si basa su IntelliJ IDEA ed offre nuove funzionalità e miglioramenti rispetto a Eclipse ADT.

Le principali sono:

- Flessibile sistema di build basato su Gradle
- Varianti di build e generazione di più APK
- Supporto espanso dei template per i servizi di Google e vari tipi di dispositivi
- Editor di layout avanzato con supporto per l'editing dei temi
- Strumenti Lint per individuare problemi di prestazioni, usabilità, compatibilità delle versioni e altri problemi
- Capacità di ProGuard e di firmare l'applicazione
- Supporto integrato per Google Cloud Platform, semplificando l'integrazione di Google Cloud Messaging e App Engine


### Android SDK Manager

Prima di poter compilare un'applicazione Android o anche creare un progetto, è necessario installare uno o più target di compilazione, utilizzando Android SDK Manager si può selezionare i componenti delle piattaforme che si desidera installare sulla macchina di sviluppo.

> Nota
> Ci sono diversi pacchetti relativi a diversi livelli di API

> Nota
> Nel corso si utilizzerà il livello API 10 e il 4.x per poter vedere le ultime versioni della piattaforma e compilare le applicazioni sviluppate per i dispositivi reali disponibili

### Richieste

Caratteristiche richieste:

- Android 10 (API 29)
- Android 4.x > a.1.2 (API 16)
- Extra:
	- Android Support Library
	- Google Play Services


---

## Hello World

### Selezione progetto

![[activity.png]]


### Configurazione progetto

![[proprietà.png]]

### Struttura progetto

![[struttura.png]]

Contenuto: 

- AndroidManifest.xml
- res/
    - drawable/ : immagini, patch, drawable, file XML
    - raw/ : file di dati che possono essere caricati come stream
    - values/ : file XML con stringhe, valori numerici utilizzati nel codice, ad esempio per localizzare l'applicazione in diverse lingue
- src/
    - java/package/directories
- gen/ : directory generata dall'IDE e Android SDK
- layout/ : file di layout dell'applicazione


### Android Studio & Gradle

Gradle è un sistema di compilazione, basato su JVM che consente di scrivere script personalizzati utilizzando il linguaggio Java, che prende le migliori caratteristiche da altri sistemi di compilazione (come ANT e Maven) e le combina in uno solo.

I file di compilazione di Gradle utilizzano un linguaggio specifico per il dominio (DSL) per definire la logica di compilazione personalizzata e interagire con gli elementi specifici di Android tramite il plugin Android per Gradle.

I progetti di Android Studio sono composti da uno o più moduli, che sono componenti che è possibile compilare, testare e debuggare in modo indipendente, ogni modulo ha il proprio file di compilazione, quindi ogni progetto di Android Studio contiene due tipi di file di compilazione Gradle:

- File di compilazione di livello superiore (top-level), si trovano le opzioni di configurazione comuni a tutti i moduli che compongono il tuo progetto

- File di compilazione di livello del modulo(module-level), ogni modulo ha il proprio file di compilazione Gradle che contiene le impostazioni di compilazione specifiche del modulo. Si dedicherà la maggior parte del tempo a modificare i file di compilazione di livello del modulo anziché il file di compilazione di livello superiore del progetto

### Android Emulator

L'SDK include un emulatore di dispositivo mobile virtuale che viene eseguito sul computer, consentendo di prototipare, sviluppare e testare applicazioni Android senza utilizzare un dispositivo fisico.

L'emulatore emula tutte le caratteristiche hardware e software di un tipico dispositivo mobile, ad eccezione del fatto che non può effettuare vere chiamate telefoniche, fornisce una varietà di tasti di navigazione e controllo, con cui si può interagire "premendo" utilizzando il mouse o la tastiera per generare eventi per la tua applicazione.

> Nota
> Fornisce anche uno schermo in cui viene visualizzata la tua applicazione, insieme a tutte le altre applicazioni Android in esecuzione.

Per consentirti di modellare e testare più facilmente l'applicazione, l'emulatore utilizza le configurazioni del dispositivo virtuale Android (AVD). Gli AVD ti consentono di definire alcuni aspetti hardware del telefono emulato e permettono di creare molte configurazioni per testare diverse versioni di Android e diverse combinazioni hardware.
Una volta che la tua applicazione è in esecuzione sull'emulatore, può utilizzare i servizi della piattaforma Android per invocare altre applicazioni, accedere alla rete, riprodurre audio e video, memorizzare e recuperare dati, notificare l'utente e creare transizioni e temi grafici.

L'emulatore include anche diverse funzionalità di debug, come una console dalla quale è possibile registrare l'output del kernel, simulare interruzioni dell'applicazione (come messaggi SMS o chiamate in arrivo) e simulare effetti di latenza e interruzioni sul canale dati, queste funzionalità consentono di testare e risolvere eventuali problemi nell'applicazione durante lo sviluppo e il testing.

L'emulatore Android supporta molte delle caratteristiche hardware che si trovano comunemente sui dispositivi mobili, tra cui:
  
L'emulatore Android include:

- Un processore ARMv* e la corrispondente unità di gestione della memoria (MMU)
- Un display LCD
- Un chip audio con capacità di output e input
- Un modem GSM, compresa una SIM card simulata
- Una o più tastiere (una tastiera basata su Qwerty e pulsanti associati per la navigazione)
- Partizioni di memoria flash (emulate attraverso file immagine disco sulla macchina di sviluppo)
- E altre caratteristiche hardware tipiche dei dispositivi mobili


### Create an emulator instance

![[device-manager.png]]

![[device-configuration.png]]