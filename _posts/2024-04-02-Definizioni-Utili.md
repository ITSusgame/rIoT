---
title: Definizioni utili 
published: true
---
## Definizioni utili

### Introduzione

Al fine di facilitare la comprensione di alcuni termini utilizzati, in questa sezione è possibile trovare un "Vocabolario" con alcuni termini e definizioni utili

### Malware 

## Introduzione ai Malware

Il malware è un software dannoso che danneggia o disabilita i sistemi informatici e fornisce un controllo limitato o completo dei sistemi al creatore del malware per attività dannose. 
Il malware include: Virus, Trojan, Worm, Keylogger, Cryptojacking, Adware, Spyware, Rootkit, Ransomware ed altri. 
L’obiettivo è quello di tracciare il traffico web, rallentare il sistema arrivando talvolta a volerlo degradare causando guasti, rubare e\o cancellare informazioni.

## I diversi modi in cui un malware entra nel sistema

- **Supporti hardware portatili/dispositivi mobili,** molti utenti/sistemi hanno attiva di default la funzione di Autorun, che interagisce automaticamente con il malware nel dispositivo una volta inserito.
- **Mancati aggiornamenti,** una visita ad un sito dannoso o il controllo della posta elettronica da parte di un utente, con una versione obsoleta possono provocare l’infezione senza aver interagito con alcun file per via delle vulnerabilità sfruttate delle versioni precedenti.
- **Gestione delle patch non sicura,** si rifà al punto precedente, ma riferendosi ad una mancata tempestività di patch dovuta ad una vulnerabilità.
- **Propagazione in rete,** che sfrutta l’errore umano e vulnerabilità del firewall per diffondersi sfruttando un errore di filtraggio del traffico o vulnerabilità dei protocolli di rete.
- **Condivisione di file,** utilizzando le porte adibite **NetBIOS (139), FTP (21) e SMB (145),** per la condivisione e accesso da remoto lasciate aperte o non regolate dal firewall.
- **Malware Chain,** alcuni malware possono installare altri malware utilizzando protocolli di navigazione comune, dando il controllo all’aggressore o eseguendo i comandi dati dall’esterno.
- **Bluetooth e reti wireless,** utilizzando reti a libero servizio per acquisire il traffico di rete, dati all’interno dei dispositivi collegati o infettati.

## Distribuzione di Malware sul web

- **Black Hat Search Engine Optimization (SEO),** noto anche come SEO non etico (Black Hat SEO), consiste nel manipolare le SEO di google per ottenere un posizionamento più elevato per le pagine web dannose.
- **Clickjacking di social engineering,** injection di malware in siti web che sembrano legittimi, all’interazione dell’utente con il sito il malware si triggera in backgroud senza consenso alcuno.
- **Siti di spear-phishing,** fake web site che imitano istituzioni legittime come le banche con l’intento di rubare le credenziali inserite.
- **Malversting,** incorporamento di malware nelle pubblicità diffuse online tramite canali legittimi.
- **Siti web legittimi compromessi.**
- **E-mail spam.**

## Trojan

Programma/applicativo apparentemente innocuo in cui al suo interno è contenuto un codice/applicativo dannoso, tra le principali funzioni vi è quella di rovinare la tabella di allocazione del disco rigido. 
I Trojan vengono attivati su specifiche azioni predefinite, inoltre possono usare la vittima come tramite di diffusione o per attacchi DoS.
I Trojan lavorano allo stesso livello di privilegi delle vittime, tanto più l’utente è elevato tanti più danni esso può arrecare, in alcuni casi sono programmati per effettuare una Privilage Escalation per installare Dropper o aprire backdoor.
A livello enterprise i trojan prendono di mira i sistemi nella rete per lo scambio di credenziali, implicando un altro sistema tramite spoofing (falsificazione d’identità) come fonte dell’attacco. 
L’attaccante o il Trojan possono disabilitare il Task Manager in modo da impedire la visualizzazione delle attività e il conseguente arresto forzato.

## Tipi di Trojan

- **Remote Access Trojan (RAT),** forniscono il pieno controllo del sistema della vittima, consentendo l’accesso remoto. Il RAT fa da server, rimanendo in ascolto su una porta che non dovrebbe essere disponibile agli aggressori; permettendo il keylogging, l’esecuzione di codice, comandi shell, leggere e scrivere chiavi di registro, etc.
- **Trojan backdoor,** programma che aggira l’autenticazione di sistema o meccanismi di IDS e Firewall senza essere rilevato. Utilizzata per trasferimento, modifica o danneggiamento dei file, fornendo l’accesso ininterrotto alla macchina, tipicamente usata per formare una Botnet. La principale differenza con i RAT è che non possiede un interfaccia utente, ovvero la parte client utilizzata per inviare i comandi.
- **Trojan e-banking,** intercettano le informazioni prima che il sistema le possa crittografare e inviare. Progettato per rubare importi minimi e massimi generando falsi estratti conto sul sistema infetto per nascondere la fronde. Solo effettuandolo da un altro dispositivo o sistema, si possono vedere le transazioni non autorizzate.
- **IoT Trojan,** creano una botnet con i dispositivi IoT per attaccare gli host connessi alla rete (ad esempio con attacchi DoS).
- **Trojan distruttivi,** hanno lo scopo di eliminare i file del sistema bersaglio in maniera causale, colpendo cartelle, voci di registro, unità locali etc. Il loro avvio può essere programmato dall’aggressore.
- **Trojan DoS,** ha lo scopo di costruire una botnet per eseguire attacchi DoS su macchine, reti o indirizzi Web.

## Virus

I virus sono programmi auto replicanti che si riproducono allegando copie del loro codice in altri eseguibili. Hanno il potenziale per distruggere e la sua durata dipende dalla sua capacità di riprodursi, ogni aggressore li progetta per far sì che si riproducano n volte. 
Alcuni virus colpiscono non appena il loro codice viene eseguito, altri rimangono dormienti finché non viene soddisfatta una circostanza logica predeterminata.

## Caratteristiche dei virus
Un’infezione può portare alla perdita dei dati, all’arresto anomalo e al danneggiamento di file. Le caratteristiche principali di un virus sono la sua natura mutevole, infatti possono moltiplicarsi, trasformarsi, e crittografarsi.

## Indicazioni di attacchi virus
Un attività anomala è il primo sintomo di un attacco virus. Tali attività riflettono la natura dei virus interrompendo il regolare flusso di un processo o di un programma. Tuttavia, non tutti questi comportamenti sono imputabili con certezza alla presenza di virus, potrebbero essere solo bug e quindi falsi positivi. 
Alcune indicazioni di un infezione sono: sovraccarico delle risorse, emissione di suoni acustici senza visualizzazione, frequenti blocchi, attività anomale del disco rigido, pop-up e problemi del browser.

## Tipi di Virus

I Virus hanno due fasi:
La **fase di infezione** (nel quale si replica e si attacca ad un .exe),
La **fase di attacco** (nel quale infetta ogni volta che viene eseguito o solo al verificarsi del trigger stabilito).

I virus sono categorizzati in base al loro funzionamento e obiettivo:
- **File virus,** infettano i file eseguiti o interpretati dal sistema. Possono essere ad azione diretta (o non residenti) o residenti in memoria, tali virus si copiano negli eseguibili salvando le sue istruzioni originali, in modo che tutto appaia normale nascondendo la propria presenza.
- **Macro virus,** infettano Word e applicativi simili, eseguendo automaticamente una sequenza di azioni dopo aver attivato un’applicazione. Viene sfruttata l’esecuzione automatica delle macro all’apertura del file che fa da trigger trasformando un file .doc/.xls in “eseguibile”.
- **File Extension Viruses,** alcuni virus incapsulati all’interno di un file ne modificano l’estensione, che può essere nascosta/modificata nelle impostazioni del file accessibili con il click destro.
- **File Bomb virus,** detto anche Bomba Logica si attiva con un determinato trigger, da un click ad una data specifica. Utilizzata per eseguire un keylogger, ad esempio, all’accesso su un determinato sito web che richiede le credenziali.

## Worms

Sono un sotto tipo di virus, definiti come programmi dannosi autonomi che si replicano, eseguono e si diffondono attraverso le connessioni di rete in modo indipendente. La loro diffusione di massa è mirata a consumare le risorse di elaborazione disponibili e sovraccaricare i server di rete, web e in alcuni casi danneggiano anche gli host. 

In alcuni casi si utilizzano payload di worm per installare backdoor e creare una botnet.

## Differenze

Differiscono dai virus per la loro natura autonoma di diffusione e replicazione, non si agganciano agli eseguibili per essere attivati o diffusi, non mirano ai file ma a consumare le risorse hardware e di rete, sono di più facile rilevazione e rimozione.

## Keylogger

Tipologia di malware che può essere utilizzata dai malintenzionati digitali per “intercettare” le sequenze di tasti sul PC o i tocchi eseguiti su uno smartphone e avere accesso, quindi, a ciò che fa l’utente sul proprio dispositivo, incluse password e credenziali di accesso. 
Tutto ciò che viene "catturato" viene inserito su un file di registro che, chiaramente, sarà destinato a persone esterne pronte a sfruttare queste informazioni contro gli utenti ignari.


## Cryptojacking 

Il cryptojacking è una tecnica che sfrutta i dispositivi altrui (computer, smartphone, tablet o persino server) senza che l'utente ne sia consapevole o dia il proprio consenso, per generare criptovalute in segreto a spese della vittima. Anziché costruire un computer per il cryptomining, gli hacker utilizzano il cryptojacking per rubare le risorse di elaborazione dai dispositivi delle loro vittime.
La maggior parte dei software di cryptojacking è progettata per rimanere nascosta, ma questo non significa che non ci siano delle conseguenze. Il furto delle risorse di elaborazione rallenta gli altri processi, aumenta le bollette dell'elettricità e riduce la vita utile del dispositivo. A seconda di quanto è sottile l'attacco, è possibile notare alcuni segnali d'allarme come ad es. il rallentamento o l'utilizzo della ventola di raffreddamento più del normale.

## Adware

L'Adware è un software indesiderato progettato per lanciare messaggi pubblicitari sullo schermo, spesso all'interno di un browser web. Alcuni professionisti della sicurezza li considerano i precursori del moderno PUP (programma potenzialmente indesiderato). 
Gli adware si avvalgono in genere di un metodo subdolo, mascherandosi da componenti legittimi o causando il trasferimento su un altro programma al fine di provocarne con l'inganno l'installazione su PC, tablet o dispositivo mobile.

## Spyware

Si tratta di un termine generico che indica qualunque software dannoso che infetta PC e dispositivi mobili al fine di raccogliere informazioni sugli utenti e dati sulle abitudini di navigazione, l'utilizzo di internet, ecc.
Agisce silenziosamente in background, raccogliendo informazioni o monitorando le attività degli utenti per aprire la strada ad attività dannose legate ai contenuti e alle modalità d'uso del computer. 
Questo può includere la memorizzazione di tasti premuti, screenshot, credenziali di autenticazione, indirizzi e-mail personali, dati ricavati da moduli web, informazioni sull'uso di internet e altri dati personali, come i numeri di carta di credito.
Gli spyware possono infettare i sistemi proprio come ogni altro malware, per mezzo di trojan, virus, worm, exploit e altri tipi di malware.
 
## Rootkit

Un rootkit è un particolare tipo di malware, pensato per ottenere l’accesso da remoto al dispositivo infettato.
Il significato di “rootkit” è legato al concetto di root. Nei sistemi Unix, viene chiamato root l’utente con i più elevati privilegi di amministratore. Con kit si intende invece un’applicazione che consente di accedere al livello di root senza averne l’autorizzazione.
Un rootkit può infettare un sistema con gli stessi metodi usati da un malware “tradizionale”. Tramite social engineering, ad esempio, un hacker può ottenere una serie di informazioni che gli permettono di inviare e installare rootkit sul computer della vittima.
Il loro scopo è variabile, infatti possono essere sfruttati per ottenere non solo l'accesso remoto, ma anche per ottenere credenziali funzionando a grandi linee come un keylogger, per l'instrallazione di altri malware e per eseguire attacchi DDos.

## Ransomware
Tipo di malware che blocca l'accesso ai sistemi o ai file personali degli utenti e chiede il pagamento di un riscatto per renderli nuovamente accessibili.

## Tipi di Ransomware

Esistono tre tipi principali di ransomware diversi fra di loro per l'impatto che hanno sui dato dell'utente:

- **Scareware,** caratterizzate da falsi messaggi di software di sicurezza o di servizi di supporto tecnico. Ad esempio, l'utente riceve un messaggio pop-up che segnala un'infezione da malware e avverte che l'unico modo per risolvere il problema consiste nel pagare una certa somma. Se l'utente non fa niente, continuerà probabilmente ad essere bombardato dai messaggi pop-up ma i suoi file saranno essenzialmente al sicuro.
- **Lockscreen** Quando un computer è infettato da ransomware blocca schermo, l'accesso al PC risulta completamente bloccato. All'avvio del computer compare una finestra a tutto schermo, spesso in base al contesto anche accompagnata da loghi di autorità nazionali, che invita a pagare un una sanzione per lo sblocco del dispositivo.
- **Ransomware crittografici,** è la tipologia più conosciuta, ed anche la più pericolosa. Gli autori di questi attacchi prelevano i file e li criptano, richiedendo poi il pagamento di un riscatto per ri consegnarli decriptati. Il motivo per cui questo tipo di ransomware è così pericoloso è che, una volta che i criminali informatici si sono impossessati dei file, non esiste alcun software o sistema di sicurezza che possa restituirli al legittimo proprietario. L'unica soluzione per sperare di recuperare i dati è pagare il riscatto. E anche se si accetta di pagare, non vi è alcuna garanzia che i file sottratti vengano restituiti.
