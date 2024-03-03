---
title: 2024-03-03-Hacking-Di-Lampadine-Smart.md 
published: true
---
https://research.checkpoint.com/2020/dont-be-silly-its-only-a-lightbulb/

## Contesto

Probabilmente, la maggior parte delle persone ha familiarità con l'Internet of Things (IoT), o Internet delle Cose. Ma, quanti di noi hanno effettivamente sentito parlare delle lampadine intelligenti e sono a conoscenza delle loro caratteristiche?

Questi dispositivi innovativi consentono di gestire l'illuminazione della propria casa in modo estremamente personalizzato. Puoi, infatti, non solo accendere e spegnere le luci a distanza, ma anche regolare l'intensità luminosa e il colore di ogni singola lampadina, utilizzando una semplice app sul tuo smartphone o tramite il tuo assistente virtuale per la casa.

La connessione con le lampadine intelligenti avviene tramite WiFi, oppure attraverso ZigBee, un protocollo radio progettato specificamente per le comunicazioni a bassa potenza e larghezza di banda.

Un fatto interessante è che, alcuni anni fa, un gruppo di ricercatori accademici ha dimostrato come fosse possibile prendere il controllo di queste lampadine intelligenti. Questo avveniva grazie a un attacco informatico che, a sua volta, poteva creare una reazione a catena che si diffondeva rapidamente, potenzialmente interessando un'intera città moderna.

Questa scoperta ha sollevato una questione fondamentale: oltre al pericolo di causare un blackout su larga scala (e potenzialmente scatenare crisi epilettiche a causa del lampeggiamento incontrollato delle luci), queste lampadine potrebbero rappresentare un rischio per la sicurezza della nostra rete digitale? Gli hacker potrebbero sfruttare le lampadine per attaccare obiettivi più appetibili, come la rete informatica nelle nostre case, negli uffici o, in una prospettiva ancora più ampia, nelle nostre smart cities?

La risposta a questa domanda, come siamo qui per dirvi, è un deciso e inequivocabile: **Sì**.

Riprendendo dove la ricerca precedente si era interrotta, ci siamo concentrati sul cuore del sistema: l'hub intelligente che funge da ponte tra la rete IP e la rete ZigBee. Riuscendo a mascherarci come una legittima lampadina ZigBee, abbiamo potuto sfruttare le vulnerabilità che abbiamo individuato nel ponte. Questo ci ha permesso di infiltrarci nella preziosa rete IP, utilizzando un **exploit ZigBee over-the-air remoto**.

## Introduzione a ZigBee

Secondo quanto riportato da Wikipedia, ZigBee è un termine che indica una specifica tecnica basata sul protocollo IEEE 802.15.4. Questa specifica è stata sviluppata per una suite di protocolli di comunicazione di alto livello, i quali vengono utilizzati per la creazione di reti ad hoc wireless. Queste reti si caratterizzano per il loro basso consumo energetico, la bassa velocità di trasmissione dati e la stretta prossimità tra i dispositivi che ne fanno parte. È importante notare che ZigBee non va confuso con IEEE 802.11, noto anche come WiFi. Secondo il modello OSI, l'IEEE 802.15.4 rappresenta lo standard tecnico per il protocollo di rete basato su radio che funge da strati 1-2 dello stack di rete ZigBee.

Per dare un'idea più precisa di cosa significhi 'bassa velocità di trasmissione dati' nel contesto di ZigBee, consideriamo che l'unità di trasmissione massima (MTU) per un frame nel livello MAC sottostante di IEEE 802.15.4 è di soli 127 byte. Questo implica che, a meno che non si ricorra alla frammentazione, i messaggi dello stack di rete ZigBee sono estremamente limitati in termini di dimensioni. Speriamo che queste limitazioni non rappresentino un ostacolo troppo grande nel nostro tentativo di individuare, e successivamente sfruttare, le vulnerabilità presenti nell'implementazione di ZigBee.

Al di là dello strato di rete radio, che rappresenta la base dello stack di rete, ZigBee definisce un intero stack composto da numerosi strati di rete. Questo significa che ZigBee non si limita a fornire un protocollo per la trasmissione radio, ma offre una soluzione di networking completa e ben strutturata, in grado di gestire una vasta gamma di esigenze di comunicazione.

## L'exploit

Nel nostro scenario di attacco, l'obiettivo è di prendere il controllo del ponte che si trova all'interno della rete ZigBee. Non vogliamo limitarci a questo, ma intendiamo utilizzare il ponte come un punto di leva strategico per lanciare attacchi più ampi su ulteriori computer che fanno parte della rete IP.

Tuttavia, prima di poter procedere, dobbiamo affrontare una sfida significativa. La nostra vulnerabilità richiede che riusciamo a ingannare l'utente affinché inizi la ricerca di nuove lampadine. Questo non è un passo semplice da attuare. Utilizzando i primitivi di attacco che sono stati identificati durante la nostra ricerca originale, siamo riusciti a sviluppare il seguente piano d'azione:

1. Iniziamo utilizzando il metodo touchlink, che è stato utilizzato anche nella ricerca originale. Questo ci permette di rubare una lampadina dalla rete dell'utente, così che ora possiamo controllarla a nostro piacimento.
2. Successivamente, cambiamo il colore e l'intensità della lampadina per farla apparire in qualsiasi tonalità fastidiosa di tua scelta. Vogliamo che l'utente pensi che la lampadina abbia un problema, ma che sia ancora funzionante, così da non spegnerla.
3. A questo punto, abbiamo l'opzione di aggiornare il firmware della lampadina (come è stato fatto nel corso della ricerca originale) ed eseguire i passaggi successivi utilizzando la stessa lampadina. Per semplicità, abbiamo scelto di utilizzare la nostra scheda di valutazione invece, poiché non volevamo danneggiare alcuna lampadina nel processo, e non avevamo alcuna motivazione per creare un attacco completamente armato autonomo.
4. L'utente alla fine si accorge che c'è qualcosa che non va con la lampadina. Essa appare come "Irraggiungibile" nell'app mobile. A questo punto, l'utente decide di "resettare" la lampadina.
5. L'unico modo per resettare la lampadina è eliminarla dall'app, e poi dire al ponte di cercare nuove lampadine. Bingo! Ora possiamo iniziare il nostro attacco.
6. La lampadina rubata si trova in una rete ZigBee diversa e quindi non verrà scoperta dal ponte.
7. A questo punto, ci travestiamo da una lampadina legittima che l'utente può vedere nell'app, e riconfiguriamo la lampadina per farla tornare al suo colore originale.
8. Dietro le quinte, creiamo ulteriori lampadine fantasma che sfruttano la vulnerabilità nel ponte e installano la nostra porta dietro.
9. La lampadina "legittima" utilizza questa porta dietro per installare malware sul ponte mirato.
10. Il nostro malware si collega a noi attraverso internet, e abbiamo ora infiltrato con successo la rete IP del bersaglio dalla rete radio ZigBee.

Per la nostra dimostrazione, abbiamo scelto di utilizzare l'exploit NSA `EternalBlue`. Questo exploit viene eseguito dal ponte stesso, ed è usato per attaccare i computer che non sono stati aggiornati e che si trovano all'interno della rete IP del bersaglio.

## Divulgazione Coordinata

- 5 novembre 2019 - Le vulnerabilità sono state rivelate a Philips, e
inoltrate a Signify.
- 5 novembre 2019 - Signify ha riconosciuto la nostra segnalazione, e confermato l'
esistenza della vulnerabilità nel loro prodotto.
- 25 novembre 2019 - Signify ci ha notificato che hanno terminato lo sviluppo
e il test della patch, e che sarebbe stata rilasciata a gennaio
1. 
- 13 gennaio 2020 - La patch è stata distribuita come un aggiornamento del firmware remoto
([1935144040](https://www2.meethue.com/en-us/support/release-notes/bridge)).
- 28 gennaio 2020 - A causa della distribuzione basata sulla geografia, ci è voluto
del tempo al nostro bridge per installare automaticamente l'aggiornamento del firmware.
- 5 febbraio 2020 - Abbiamo pubblicato un video dimostrativo per sensibilizzare, e
abbiamo trattenuto i dettagli tecnici finché gli utenti non hanno avuto abbastanza tempo per aggiornare i loro
prodotti.
- 7 agosto 2020 - Divulgazione pubblica completa durante DEF CON 28.
