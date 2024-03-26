---
title: Hacking Di Router
published: true
---

## CONTESTO:

Nel mondo sempre più interconnesso di oggi, la minaccia dei botnet rappresenta un pericolo significativo per la sicurezza informatica. Recentemente, un nuovo giocatore nel panorama delle minacce è emerso: il botnet **Meris**. Questo botnet, scoperto per la prima volta alla fine di giugno 2021 da **QRator** e **Yandex**, ha rapidamente guadagnato notorietà per i suoi attacchi DDoS devastanti che hanno preso di mira migliaia di siti web in tutto il mondo. La sua complessa infrastruttura e le tattiche sofisticate lo rendono una minaccia difficile da affrontare per le aziende e gli operatori di rete.

## LA VULNERABILITÀ

Il botnet Meris si basa su una vulnerabilità nel sistema operativo dei router prodotti da MikroTik, un'azienda lettone. Questa vulnerabilità, identificata come **CVE-2018-14847**, consente agli aggressori di ottenere accesso remoto non autenticato ai dispositivi infetti, compromettendo così la sicurezza delle reti in cui sono installati i router. Sfruttando questa falla, il botnet è in grado di orchestrare attacchi DDoS massicci utilizzando tecniche avanzate come il pipelining HTTP, che consente l'invio di molteplici richieste su una singola connessione, aumentando così la sua potenza di attacco complessiva. Nonostante la vulnerabilità sia stata scoperta nel 2018 e le patch siano state rilasciate, molti dispositivi non sono stati aggiornati, lasciandoli vulnerabili agli attacchi del botnet Meris.

Ulteriori informazioni emerse dal recente rapporto di Qrator Labs e Yandex sottolineano la natura complessa e sofisticata di Meris. Si stima che il botnet sia composto da oltre 200.000 dispositivi, principalmente router MikroTik. Utilizzando una combinazione di proxy Socks4, pipelining HTTP e attacchi basati su RPS (richieste al secondo), il botnet è in grado di sferrare attacchi devastanti con una potenza senza precedenti. Inoltre, la scoperta di porte aperte specifiche, come la porta 5678 utilizzata per il protocollo Mikrotik Neighbor Discovery, fornisce ulteriori dettagli sulle vulnerabilità sfruttate dal botnet.

## SOLUZIONE

Per quanto osservato da MikroTik, questi attacchi utilizzano gli stessi router che sono stati compromessi nel 2018, quando MikroTik RouterOS aveva una vulnerabilità, che è stata rapidamente risolta. È fondamentale quindi assicurarsi che tutti i router MikroTik siano aggiornati con le ultime patch di sicurezza fornite dai produttori per mitigare il rischio di compromissione.

Più specificamente, suggeriscono di disabilitare SOCKS e di guardare nel menu Sistema -> Pianificatore. Disabilita tutte le regole che non riesci a identificare. Per impostazione predefinita, non dovrebbero esserci regole del Pianificatore e SOCKS dovrebbe essere spento.

In aggiunta, consigliamo di:

- Aggiornamento dei dispositivi: È essenziale assicurarsi che tutti i dispositivi di rete, in particolare i router MikroTik, siano aggiornati con le ultime patch di sicurezza fornite dai produttori. Gli aggiornamenti del firmware possono correggere le vulnerabilità note e migliorare la sicurezza complessiva dei dispositivi.

- Gestione delle password: Cambiare regolarmente le password predefinite e utilizzare password complesse può contribuire a ridurre il rischio di accessi non autorizzati ai dispositivi di rete. Inoltre, è consigliabile disabilitare l'accesso remoto non sicuro e configurare le restrizioni di accesso per limitare le connessioni ai dispositivi solo da indirizzi IP autorizzati.

- Monitoraggio del traffico di rete: Implementare sistemi di monitoraggio del traffico di rete per rilevare e analizzare attività sospette o anomalie che potrebbero indicare un potenziale attacco da parte del botnet Meris. Il monitoraggio costante del traffico di rete può consentire una risposta tempestiva agli attacchi e la mitigazione dei danni.

- Implementazione di filtri di sicurezza: Utilizzare firewall e filtri di sicurezza per bloccare il traffico dannoso proveniente da indirizzi IP noti associati al botnet Meris. I filtri possono essere configurati per rilevare e bloccare le richieste di connessione sospette o non autorizzate provenienti da dispositivi compromessi.

Implementando queste misure di sicurezza e adottando un approccio proattivo alla gestione della sicurezza informatica, le organizzazioni possono ridurre significativamente il rischio di essere vittime di attacchi da parte del botnet Meris e proteggere le proprie infrastrutture online da danni e compromissioni.

## FONTI

https://blog.qrator.net/en/meris-botnet-climbing-to-the-record_142/

https://blog.cloudflare.com/meris-botnet/

https://forum.mikrotik.com/viewtopic.php?f=21&t=178417