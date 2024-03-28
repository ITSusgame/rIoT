---
title: Hacking di Smart TV
published: true
---
## Un Trasmettitore DVB-T per Compromettere la tua Smart TV

### Contesto

Le Smart TV hanno rivoluzionato il modo in cui interagiamo con il contenuto multimediale nel nostro salotto. Grazie alla loro diffusione sempre più ampia, le Smart TV offrono una vasta gamma di funzionalità avanzate che vanno ben oltre la semplice visione dei canali televisivi tradizionali. Una delle principali ragioni della loro popolarità è il loro prezzo sempre più accessibile, che le rende disponibili a un vasto pubblico di consumatori. La capacità "SMART" di queste televisori si manifesta attraverso la connettività Internet integrata, consentendo agli utenti di accedere a una vasta gamma di servizi online come lo streaming di video, la navigazione web, i social media, e molto altro ancora. Inoltre, molte Smart TV sono dotate di sistemi operativi intuitivi e di applicazioni preinstallate che offrono un'esperienza multimediale personalizzata e ricca di contenuti. Grazie alla loro crescente diffusione e alle loro capacità avanzate, le Smart TV stanno rapidamente diventando il fulcro dell'intrattenimento domestico moderno.

### La Ricerca

**Rafael Scheel**, consulente di sicurezza, ha scoperto che l’hacking delle **Smart TV** richiede poco più di un **trasmettitore DVB-T piuttostoeconomico, documentando la sua ricerca in un video YouTube.**

Una volta che un hacker ha il controllo sulla TV di un utente finale, può nuocere all’utente in vari modi. Tra gli altri, la TV potrebbe essere utilizzata per **attaccare altri dispositivi nella rete domestica** o per spiare l’utente tramite la **telecamera e il microfono della TV**. 

Nel video YouTube “Smart TV Hacking”, **Rafael Sheil** discute il processo di hacking delle **Smart TV** e l’attrattiva di questi dispositivi per i **cybercriminali**. Egli spiega che le Smart TV sono essenzialmente **computer con funzionalità televisive**, rendendole affette da una carenza di differenze tra modelli ed esponendole a sfruttamenti con scopi malevoli a causa della loro connessione a **controller cloud centralizzati** che le tiene quasi sempre online, per garantire il funzionamento del sistema. In contrasto, i laptop hanno vari sistemi operativi, browser e misure di sicurezza, che rendono gli attacchi verso di essi più complessi, mentre in questo caso con la recente commercializzazione di Flipper Zero ( [https://flipperzero.one/](https://flipperzero.one/) ) è possibile perfino effettuare attacchi automatici, semplicemente passando in prossimità del dispositivo! 

Si  denota anche la spinta verso una sempre maggiore economicità dei dispositivi IoT per i produttori, il che porta inevitabilmente a misure di sicurezza insufficienti e i cicli di patch lunghi e costosi.

### L'exploit

Il trasmettitore deve trovarsi nel raggio d’azione della TV target per poter inviare segnali malevoli. L’attacco sfrutta i segnali **ibridi di trasmissione televisiva a banda larga** e le vulnerabilità ben note nei **browser web** comunemente utilizzati sulle Smart TV, che sembrano essere in esecuzione in background quasi tutto il tempo.

Scheel è stato incaricato dalla società di **sicurezza informatica Oneconsult** di creare l’exploit. Una volta implementato, l’attaccante ottiene **privilegi di root completi**, consentendo di configurare e accedere tramite **SSH alla TV**, prendendo il controllo completo del dispositivo da qualsiasi parte del mondo. Il codice malevolo rimane attivo anche dopo riavvii o ripristini di fabbrica.

Una volta che un hacker ha il controllo sulla TV di un utente finale, può nuocere all’utente in vari modi. Tra gli altri, la TV potrebbe essere utilizzata per **attaccare altri dispositivi nella rete domestica** o per spiare l’utente tramite la **telecamera e il microfono della TV**.

### Remediation

le soluzioni che si possono mettere in atto sono moltissime e dipendono principalmente dalla volontà dell'utente di proteggere la propria privacy e sicurezza informatica.

Innanzitutto, è importante tenere sempre aggiornato il firmware della TV e di ogni dispositivo connesso alla rete domestica. Aggiornare regolarmente il software riduce le vulnerabilità che potrebbero permettere agli hacker di infiltrarsi nei nostri dispositivi. Inoltre, è sempre consigliabile utilizzare password robuste e complesse per proteggere l'accesso alla rete Wi-Fi e agli account associati alla TV.
Un'altra misura di sicurezza importante è quella di disattivare le funzioni di telecamera e microfono della TV quando non sono necessarie. In questo modo si limita la possibilità che terzi possano spiare l'utente e raccogliere informazioni personali sensibili. È inoltre consigliabile coprire la telecamera con un adesivo quando non viene utilizzata per garantire una maggiore privacy.
Infine, è fondamentale fare attenzione agli abbonamenti e agli aggiornamenti software proposti da terze parti o da fonti non autorizzate. Evitare di scaricare applicazioni o software promettenti funzionalità aggiuntive senza prima verificare la loro affidabilità e provenienza riduce il rischio di installare malware dannosi che possano compromettere la sicurezza della TV e dei dispositivi connessi.

### Fonti

[https://www.youtube.com/watch?v=bOJ_8QHX6OA](https://www.youtube.com/watch?v=bOJ_8QHX6OA)  --  il video in questione NDR

[https://www.makeuseof.com/ways-hackers-attack-smart-tv/](https://www.makeuseof.com/ways-hackers-attack-smart-tv/)
