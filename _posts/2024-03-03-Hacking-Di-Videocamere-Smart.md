---
title: 2024-03-03-Hacking-Di-Videocamere-Smart.md 
published: true
---
# HACKING DI VIDEOCAMERE SMART

## Contesto

Le telecamere di sicurezza smart rappresentano una componente fondamentale nel panorama dei dispositivi IoT. Questi dispositivi, grazie alla loro capacità di connettersi ad Internet, permettono un controllo remoto in tempo reale, rappresentando un efficace strumento per garantire la sicurezza delle nostre case e dei nostri uffici. Inoltre, molte di queste telecamere sono dotate di funzionalità avanzate, come il rilevamento del movimento, l'analisi video ed il supporto per l'intelligenza artificiale.

Oltre a queste funzionalità, le telecamere di sicurezza smart offrono anche la possibilità di inviare notifiche in tempo reale al proprietario nel caso in cui rilevino un'attività sospetta. Questa capacità di risposta immediata può fare la differenza quando si tratta di prevenire potenziali minacce alla sicurezza. Alcune telecamere sono anche dotate di una funzione di allarme che può essere attivata a distanza, offrendo un ulteriore livello di protezione.

Un aspetto interessante delle telecamere di sicurezza smart è la loro facilità di installazione e configurazione. Spesso, basta collegarli alla rete WiFi di casa o dell'ufficio e impostare le preferenze attraverso un'applicazione dedicata sullo smartphone. Questa semplicità d'uso è un altro motivo per cui questi dispositivi stanno diventando sempre più popolari.

Uno dei principali fattori che ha contribuito alla crescente popolarità delle telecamere di sicurezza smart è il loro costo sempre più accessibile. Grazie agli avanzamenti tecnologici e alla maggiore competizione nel settore, il prezzo di questi dispositivi è notevolmente diminuito, rendendoli accessibili a un pubblico più ampio. Questo ha permesso a un numero sempre maggiore di persone di beneficiare delle funzionalità avanzate che offrono, contribuendo alla loro diffusione sia in ambito domestico che aziendale.

È importante notare, tuttavia, che mentre queste telecamere offrono molti vantaggi, è fondamentale garantire che siano correttamente protette contro potenziali attacchi informatici. Dato che sono connessi a Internet, questi dispositivi possono essere soggetti a hacking, quindi è essenziale mantenere sempre aggiornati i software e utilizzare misure di sicurezza adeguate.

## MIRAI

La botnet Mirai ha attirato l'attenzione mondiale nel 2016 quando ha orchestrato uno dei più devastanti attacchi distribuiti di negazione del servizio (DDoS) nella storia dell'internet. Questo attacco ha messo in evidenza le fragilità esistenti nei dispositivi IoT, che spesso vengono trascurate in termini di sicurezza.

Mirai ha sfruttato queste vulnerabilità, in particolare nelle telecamere di sicurezza smart, per trasformare questi dispositivi in 'bot' controllati da un centro di comando e controllo. Questi bot inviavano poi un flusso di traffico superfluo ai server bersaglio, causando interruzioni di servizio e danni significativi.

Il software Mirai è stato progettato per infettare i dispositivi in modo molto semplice ma efficace. Mirai scansionava l'internet alla ricerca di dispositivi IoT protetti da password predefinite o facilmente indovinabili. Una volta che un dispositivo veniva infettato, veniva aggiunto alla botnet e poteva essere controllato dal centro di comando e controllo.

L'attacco di Mirai ha dimostrato l'importanza di una robusta sicurezza IoT. Ha evidenziato che i dispositivi intelligenti, nonostante le loro numerose comodità, possono essere sfruttati come strumenti di attacco se non adeguatamente protetti. Inoltre, ha sottolineato l'importanza di cambiare le password predefinite sui dispositivi e di mantenere i software sempre aggiornati per proteggersi da potenziali attacchi informatici.

Dal punto di vista tecnico, il funzionamento di Mirai può essere articolato in tre fasi principali.

La prima è la fase di scansione. Durante questa fase, il bot Mirai scansiona attivamente l'Internet alla ricerca di dispositivi IoT vulnerabili. Per farlo, utilizza un sottoinsieme limitato di 10 porte TCP, cercando di identificare dispositivi che potrebbero essere facilmente compromessi. Questa fase è cruciale per l'espansione della botnet, poiché permette a Mirai di identificare un gran numero di dispositivi potenzialmente vulnerabili.

Una volta identificato un dispositivo vulnerabile, Mirai passa alla seconda fase: l'infezione. In questa fase, Mirai tenta di stabilire una connessione Telnet con il dispositivo target. Per farlo, utilizza una lista di combinazioni di username e password predefinite, sfruttando la frequente negligenza degli utenti nell'aggiornare queste credenziali di default. Se le credenziali di accesso sono corrette, Mirai procede installando una copia di se stesso sul dispositivo compromesso. Contemporaneamente, stabilisce una connessione con il server di comando e controllo, segnalando così l'avvenuta infezione.

Con il dispositivo ora sotto il suo controllo, Mirai lo aggiunge alla sua botnet. A questo punto, il dispositivo infetto non è più sotto il controllo del legittimo proprietario, ma è diventato un 'bot' sotto il controllo di Mirai.

La terza e ultima fase è quella dell'attacco. In questa fase, il server di comando e controllo di Mirai invia istruzioni ai dispositivi compromessi. Queste istruzioni ordinano ai dispositivi di iniziare un attacco DDoS contro un obiettivo specifico. L'obiettivo può variare, ma l'effetto finale è lo stesso: un massiccio afflusso di traffico indesiderato che può causare gravi interruzioni del servizio.

Complessivamente, il funzionamento di Mirai dimostra l'efficacia e la pericolosità di questo tipo di attacchi. Sottolinea l'importanza di mantenere sempre aggiornate le credenziali di accesso e di implementare misure di sicurezza appropriate per proteggere i dispositivi IoT.

## ALTRE BOTNET

Dopo l'attacco di Mirai, numerosi malware simili hanno sfruttato le stesse vulnerabilità nei dispositivi IoT. Ad esempio, la botnet Reaper, emersa nel 2017, si è rivelata ancora più pericolosa di Mirai, in grado di infettare una vasta gamma di dispositivi IoT utilizzando vulnerabilità note piuttosto che semplici combinazioni di nome utente e password. Un altro esempio è la botnet Satori, che è una variante di Mirai e che ha mostrato una capacità di diffusione ancora più veloce. Infine, la botnet Hide 'N Seek, scoperta nel gennaio 2018, è stata la prima botnet ad utilizzare il protocollo peer-to-peer per la comunicazione, rendendo la sua rilevazione e la sua eliminazione molto più complicate. Questi esempi dimostrano l'evoluzione continua delle minacce ai dispositivi IoT e sottolineano l'importanza di una sicurezza efficace.

## REMEDIATION

Per proteggere le telecamere smart da potenziali attacchi informatici, è necessario adottare una serie di pratiche di sicurezza. Queste pratiche non solo aiutano a prevenire gli attacchi, ma possono anche limitare le potenziali conseguenze se un attacco dovesse verificarsi.

Innanzitutto, è importante cambiare le credenziali di accesso predefinite dei dispositivi. Questo perché molti dispositivi vengono venduti con password predefinite facilmente indovinabili, che possono essere sfruttate dagli aggressori. È consigliato utilizzare password forti e uniche, che combinano lettere, numeri e simboli in un modo non prevedibile. Questo può rendere molto più difficile per un aggressore indovinare o decifrare la password.

Inoltre, è fondamentale mantenere il software dei dispositivi sempre aggiornato. Gli aggiornamenti del software non solo introducono nuove funzionalità, ma spesso includono anche patch di sicurezza per le vulnerabilità note. Queste vulnerabilità possono essere sfruttate dagli aggressori per guadagnare l'accesso ai dispositivi, quindi è importante installare gli aggiornamenti non appena diventano disponibili.

Un'altra pratica di sicurezza utile è l'utilizzo di reti private virtuali (VPN) per accedere ai dispositivi da remoto. Le VPN criptano la comunicazione tra il dispositivo e l'utente, rendendo molto più difficile per un aggressore intercettare o manipolare i dati trasmessi. Questo può essere particolarmente utile se si accede ai dispositivi da una rete non sicura, come un hotspot WiFi pubblico.

Infine, è consigliabile disattivare le funzionalità non necessarie sui dispositivi. Questo include le porte aperte o i servizi in esecuzione che non sono necessari per il funzionamento del dispositivo. Queste funzionalità possono rappresentare potenziali punti di ingresso per gli aggressori, quindi è meglio disattivarle se non sono necessarie.

Ricordate, tuttavia, che nessuna misura di sicurezza è infallibile. È importante monitorare regolarmente i dispositivi e le reti per eventuali attività sospette e adottare un approccio proattivo alla sicurezza. 

## FONTI

[https://spectrum.ieee.org/mirai-botnet](https://spectrum.ieee.org/mirai-botnet)

[https://therecord.media/mirai-based-botnet-gets-exploit-updates](https://therecord.media/mirai-based-botnet-gets-exploit-updates)

[https://securityboulevard.com/2023/12/mirai-botnet-exploits-zero-day-bugs-for-ddos-attacks/](https://securityboulevard.com/2023/12/mirai-botnet-exploits-zero-day-bugs-for-ddos-attacks/)
