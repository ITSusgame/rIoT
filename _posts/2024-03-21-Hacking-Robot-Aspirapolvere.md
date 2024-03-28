---
title: Hacking Di Robot Aspirapolvere Smart
published: true
---

### Contesto

Nel vasto panorama dell'Internet delle Cose (IoT), dove dispositivi connessi semplificano e arricchiscono le nostre vite quotidiane, sorgono anche sfide di sicurezza intricate e spesso nascoste. Uno degli aspetti meno considerati, ma ugualmente rilevanti, è la vulnerabilità dei dispositivi domestici intelligenti, 
come i robot aspirapolvere. Questi gadget, pur offrendo comodità e automazione nelle pulizie domestiche, possono essere soggetti a minacce informatiche che mettono a rischio la privacy e la sicurezza delle abitazioni. In questo articolo, esploreremo una vulnerabilità specifica che affligge i robot aspirapolvere smart,
analizzandone le implicazioni e suggerendo possibili soluzioni per mitigare il rischio.

### GLI EXPLOIT

Due ricercatori dell'azienda di sicurezza Positive Technologies hanno scoperto vulnerabilità che colpiscono la linea di robot aspirapolvere Dongguan Diqee 360 prodotti dal produttore cinese di smart home Diqee.
In generale questo tipo di dispositivi sono dotati di Wi-Fi e di una telecamera a 360 gradi per una modalità conosciuta come "monitoraggio dinamico" che trasforma la macchina in un dispositivo di sorveglianza domestica. 
È dunque proprio la telecamera l'obiettivo degli attaccanti, che tenteranno di sfruttare l'exploit per prenderne il controllo.

La vulnerabilità, nota come **CVE-2018-10987**, può concedere a un attaccante (che ottiene l'indirizzo MAC del dispositivo) i privilegi di amministratore di sistema. Secondo il rapporto, la vulnerabilità è contenuta nella funzione **REQUEST_SET_WIFIPASSWD** e sfruttarla richiede l'autenticazione, facilmente aggirabile poiché composta da
combinazione di nome utente e password predefinita molto comune (admin/888888).
I ricercatori sospettano che la vulnerabilità nel Dongguan Diqee 360 potrebbe influenzare anche altri dispositivi che condividono lo stesso modulo video, inclusi telecamere di sorveglianza esterne, campanelli intelligenti e DVR. Diqee produce anche aspirapolveri venduti sotto altre marche (come spesso accade per molti produttori asiatici)
e dunque nel rapporto sulla vulnerabilità si sospetta che anche quei dispositivi potrebbero essere soggetti dalla stessa vulnerabilità.

Positive Technologies ha notato una seconda vulnerabilità, nota come **CVE-2018-10988**, che colpisce anche il modello di aspirapolvere Vacuum di Roomba, anche se richiede ,in questo caso, un accesso fisico attraverso lo slot per la scheda SD per compromettere la macchina.
Il modello di Roomba, tuttavia, è dotato di una copertura di protezione della privacy davanti all'obiettivo della telecamera, ossia una barriera fisica che "risolve la perdita di privacy dall'hardware" dato dallo sfruttamento di questa vulnerabilità secondo il produttore, che necessità però di essere inserito\disinserito a mano e rendendolo di fatto scomodo e poco utilizzato.

 Lo sfruttamento di questo exploit come dichiarato da Leigh-Anne Galloway, responsabile della sicurezza informatica di Positive Technologies, potrebbe portare questi prodotti, e qualsiasi altro dispositivo IoT presente nella rete, ad essere impiegati in un botnet per attacchi DDoS,
 ma questo non è nemmeno il peggiore degli scenari, almeno per i proprietari, poiché nello specifico questo tipo i robot dotati di telecamera di sorveglianza con visione notturna e navigazione controllata tramite smartphone, possono permettere all'attaccante che ne assume il controllo
 di spiare segretamente il proprietario e persino utilizzare l'aspirapolvere come un 'microfono su ruote'.

### REMEDIATION

Una delle prime linee di difesa contro le vulnerabilità del firmware è l'applicazione di aggiornamenti regolari. Gli utenti dei robot aspirapolvere Dongguan Diqee 360 e dispositivi simili dovrebbero essere vigili riguardo agli aggiornamenti del firmware forniti dal produttore e installarli prontamente. 
Questi aggiornamenti spesso includono patch di sicurezza che mitigano le vulnerabilità note ai produttori.

Un altro passo essenziale per mitigare il rischio di sfruttamento della vulnerabilità CVE-2018-10987 è modificare immediatamente le credenziali predefinite del dispositivo. Gli utenti dovrebbero cambiare sia il nome utente che la password da impostazioni predefinite come "admin/888888" a combinazioni uniche e robuste. 
Questo ridurrà significativamente la possibilità di accesso non autorizzato tramite la vulnerabilità di codice remoto, spesso si sottovaluta questo aspetto perché ci si affida troppo alla presunta sicurezza offerta dai modem dei provider, o delle password degli account che gestiscono i dispositivi,
lasciando quest'ultimi con credenziali di default note agli attaccati poiché uguali per tutti i prodotti. Inoltre, è consigliabile configurare correttamente le impostazioni di sicurezza dei dispositivi IoT per disabilitare le funzionalità non necessarie e limitare l'esposizione del dispositivo agli attacchi.

Gli utenti devono mantenere un monitoraggio attivo dei propri dispositivi IoT. La vigilanza costante sull'attività sospetta o anomala può aiutare a identificare tempestivamente eventuali tentativi di sfruttare le vulnerabilità e adottare misure correttive appropriate.

Implementando queste misure di remediation, gli utenti possono ridurre significativamente il rischio derivante dalle vulnerabilità dei robot aspirapolvere intelligenti e garantire la sicurezza e la privacy delle proprie abitazioni.

Infine, gli sviluppatori di dispositivi IoT dovrebbero integrare misure di sicurezza avanzate direttamente nel design e nello sviluppo del prodotto. Questo include la realizzazione di controlli di sicurezza robusti e la conduzione di test approfonditi di vulnerabilità e penetrazione per identificare e risolvere eventuali falle di sicurezza prima del rilascio sul mercato.

### FONTI

[https://techcrunch.com/2018/07/19/vacuum-vulnerability-hack-diqee-positive-technologies/](https://techcrunch.com/2018/07/19/vacuum-vulnerability-hack-diqee-positive-technologies/)

[https://techmonitor.ai/technology/cybersecurity/robot-vacuum-cleaners-vulnerabilities](https://techmonitor.ai/technology/cybersecurity/robot-vacuum-cleaners-vulnerabilities)

[https://www.infosecurity-magazine.com/news/vulnerable-iot-vacuums-dvrs-put/](https://www.infosecurity-magazine.com/news/vulnerable-iot-vacuums-dvrs-put/)

[https://nvd.nist.gov/vuln/detail/CVE-2018-10988](https://nvd.nist.gov/vuln/detail/CVE-2018-10988)
[https://nvd.nist.gov/vuln/detail/CVE-2018-10987](https://nvd.nist.gov/vuln/detail/CVE-2018-10987)

