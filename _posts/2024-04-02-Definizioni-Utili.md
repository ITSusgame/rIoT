---
title: Definizioni utili 
published: true
---
## Definizioni utili

### Introduzione

Al fine di facilitare la comprensione di alcuni termini utilizzati, in questa sezione è possibile trovare un "Vocabolatio" con alcuni termini e definizioni utili

### Malware 

## Introduzione ai Malware

Il malware è un software dannoso che danneggia o disabilita i sistemi informatici e fornisce un controllo limitato o completo dei sistemi al creatore del malware per attività dannose. 
Il malware include: Virus, Malware, Trojan, Worm, Keylogger, Cryptojacking, Adware, Spyware, Rootkit, Ramsomware ed altri. 
L’obiettivo è quello di, tracciare il traffico web, rallentare il sistema arrivando talvolta a volerlo degradare causando guasti, rubare e\o cancellare informazioni.

## I diversi modi in cui un malware entra nel sistema

- **Applicazioni di messaggistica instantanea.**
- **Supporti hardware portatili/dispositivi mobili,** molti utenti/sistemi hanno attiva di default la funzione di Autorun, che interagisce automaticamente con il malware nel dispositivo una volta inserito.
- **Mancati aggiornamenti,** una visita ad un sito dannoso o il controllo della posta elettronica da parte di un utente, con un versione obsoleta possono provocare l’infezione senza aver interagito con alcun file per via delle vulnerabilità sfruttate delle versioni precedenti.
- **Gestione delle patch non sicura,** si rifà al punto precedete, ma riferendosi ad una mancata tempestività di patch dovuta ad una vulnerabilità.
- **Applicazioni rouge/decoy,** inducendo gli utenti a scaricare app dannose sotto mentite spoglie (spacciate anche per noti programmi), i freeware sono fra i più utilizzati (utilizzare software proprietario gratuito, che installa altre app plug-in dannose).
- **Propagazione in rete,** che sfrutta l’errore umano e vulnerabilità del firewall per diffondersi sfruttando un errore di filtraggio del traffico o vulnerabilità dei protocolli di rete.
- **Condivisione di file,** utilizzando le porte adibite **NetBIOS (139), FTP (21) e SMB (145),** per la condivisione e accesso da remoto lasciate aperte o non regolate dal firewall.
- **Malware Chain,** alcuni malware possono installare altri malware utilizzando protocolli di navigazione comune, dando il controllo all’aggressore o eseguendo i comandi dati dall’esterno.
- **Bluetooth e reti wireless,** utilizzando reti a libero servizio per acquisire il traffico di rete, dati all’interno dei dispositivi collegati o infettarli.

## Distribuzione di Malware sul web

- **Black Hat Search Engine Optimization (SEO),** noto anche come SEO non etico (Black Hat SEO), consiste nel manipolare le SEO di google per ottenere un posizionamento più elevato per le pagine web dannose.
- **Clickjacking di social engineering,** injection di malware in siti web che sembrano legittimi, all’interazione dell’utente con il sito il malware si triggera in backgroud senza consenso alcuno.
- **Siti di spear-phishing,** fake web site che imitano istituzioni legittime come le banche con l’intento di rubare le credenziali inserite.
- **Malversting,** incorporamento di malware nelle pubblicità diffuse online tramite canali legittimi.
- **Siti web legittimi compromessi.**
- **Download drive-by,** sfrutta le vulnerabilità di alcuni software di browser per installare malware durante la navigazione del sito web.
- **E-mail spam.**

## Trojan

Programma/applicativo apparentemente innocuo in cui al suo interno è contenuto un codice/applicativo dannoso, tra le principali funzioni vi è quella di rovinare la tabella di allocazione del disco rigido. 
I Trojan vengono attivati su specifiche azioni predefinite, inoltre possono usare la vittima come tramite di diffusione o per attacchi DoS.
I Trojan lavorano allo stesso livello di privilegi delle vittime, tanto più l’utente è elevato tanti più danni esso può arrecare, in alcuni casi sono programmati per effettuare una Privilage Escalation per installare Dropper o aprire backdoor.
A livello enterprise i trojan prendono di mira i sistemi nella rete per lo scambio di credenziali, implicando un altro sistema tramite spoofing (falsificazione d’identità) come fonte dell’attacco. 
L’attaccante o il Trojan possono disabilitare il Task Manager in modo da impedire la visualizzazione delle attività e il conseguente arresto forzato.

## Tipi di Trojan

- **Remote Access Trojan (RAT),** forniscono il pieno controllo del sistema della vittima, consentendo l’accesso remoto. Il RAT fa da server, rimanendo in ascolto su una porta che non dovrebbe essere disponibile agli aggressori; permettendo il keyloggin, l’esecuzione di codice, comandi shell, leggere e scrivere chiavi di registro, etc.
- **Trojan backdoor,** programma che aggira l’autenticazione di sistema o meccanismi di IDS e Firewall senza essere rilevato. Utilizzata per trasferimento, modifica o danneggiamento dei file, fornendo l’accesso ininterrotto alla macchina, tipicamente usata per formare una Botnet. La principale differenza con i RAT è che non possiede un interfaccia utente, ovvero la parte client utilizzata per inviare i comandi.
- **Trojan Botnet,** utilizzati per lanciare attacchi DOS, furto di numeri di serie, ID di accesso e altri dati altamente sensibili.
- **Trojan rootkit,** potenti beckdoor che attaccano specificatamente il root o il sistema operativo. A differenza delle backdoor i rootkit non sono rilevabili nel registro delle attività, forniscono ovviamente il completo controllo del sistema, non è in grado di propagarsi da solo. Proprio per questo fa parte della cosi detta “**Minaccia Mista”**, formata da tre frammenti di codice, Dropper, Loader e Rootkit. Il dropper esegue il file che installa il rootkit in seguito ad un trigger, per poi eliminarsi autonomamente.
- **Trojan e-banking,** intercettano le informazioni prima che il sistema le possa crittografare e inviare. Progettato per rubare importi minimi e massimi generando falsi estratti conto sul sistema infetto per nascondere la fronde. Solo effettuandolo da un altro dispositivo o sistema, si possono vedere le transazioni non autorizzate.
- **Trojan HTTP/HTTPS,** possono bypassare qualsiasi firewall, e funzionare al contrario creando un tunnel HTTP diretto sulla porta 80.
- **IoT Trojan,** creano una botnet con i dispositivi IoT per attaccare gli host connessi alla rete (ad esempio con attacchi DoS).
- **Trojan distruttivi,** hanno lo scopo di eliminare i file del sistema bersaglio in maniera causale, colpendo cartelle, voci di registro, unità locali etc. Il loro avvio può essere programmato dall’aggressore.
- **Trojan DoS,** ha lo scopo di costruire una botnet per eseguire attacchi DoS su macchine, reti o indirizzi Web.

## Virus

I virus sono programmi autoreplicanti che si riproducono allegando copie del loro codice in altri eseguibili. Hanno il potenziale per distruggere e la sua durata dipende dalla sua capacità di riprodursi, ogni aggressore li progetta per far si che si riproducano n volte. 
Alcuni virus colpiscono non appena il loro codice viene eseguito, altri rimangono dormienti finché non viene soddisfatta una circostanza logica predeterminata.

## Caratteristiche dei virus
Un’infezione può portare alla perdita dei dati, all’arresto anomalo e al danneggiamento di file. Le caratteristiche principali di un virus sono la sua natura mutevole, infatti possono moltiplicarsi, trasformarsi, e crittografarsi.

## Indicazioni di attacchi virus
Un attività anomala è il primo sintomo di un attacco virus. Tali attività riflettono la natura dei virus interrompendo il regolare flusso di un processo o di un programma. Tuttavia, non tutti questi comportamenti sono imputabili con certezza alla presenza di virus, potrebbero essere solo bug e quindi falsi positivi. 
Alcune indicazioni di un infezione sono: sovraccarico delle risorse, emissione di suoni acustici senza visualizzazione, frequenti blocchi, attività anomale del disco rigido, pop-up e problemi del browser.
Antivirus, Firewall, crittografia, backup frequenti, VPN/DMZ, segregazione
