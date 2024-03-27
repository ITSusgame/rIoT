# Smart Speakers

## CONTESTO

Una delle principali preoccupazioni riguardo a questi dispositivi risiede nella capacità degli assistenti vocali installati su di essi, gestendo le periferiche installate a bordo come il microfono, di ascoltare costantemente l'ambiente circostante in attesa di comandi vocali per eseguire le richieste dell’utente finale. Questi dispositivi trasmettono parte dei dati audio registrati ai server delle aziende produttrici per un’analisi più accurata del contenuto e, questa comunicazione, potrebbe essere accessibile agli hacker. L'ascolto costante dell'ambiente circostante solleva preoccupazioni legate alla privacy degli utenti, poiché potrebbero essere esposti a registrazioni non autorizzate delle loro conversazioni o attività quotidiane. Tale violazione della privacy può avere conseguenze gravi, minacciando la sicurezza e la fiducia degli utenti nei confronti di tali dispositivi e delle aziende che li producono.

## LA VULNERABILITA’

Il fatto allarmante riguarda la capacità dei sistemi di riconoscimento vocale basati sull'IA di percepire suoni al di fuori della gamma uditiva umana. Questo apre la strada a potenziali attacchi come il "DolphinAttack", dove gli hacker possono inviare comandi "inaudibili" ai dispositivi utilizzando rumori di fondo o trasmissioni ultrasoniche. In questo modo, la macchina interpreta erroneamente questo rumore come un comando impartito dall'utente.

In aggiunta, altri attacchi come il "LightCommands" o il "Laser Attack" sfruttano i laser per interferire con gli assistenti vocali presenti negli altoparlanti intelligenti e negli smartphone. I microfoni di tali dispositivi interpretano i segnali luminosi e le variazioni di temperatura come comandi vocali, eseguendo le istruzioni impartite dagli attaccanti.

Questi attacchi hanno il potenziale di causare numerose conseguenze disastrose, come il forzare dispositivi attivati vocalmente a compiere azioni indesiderate, installare malware, facilitare furti di identità, effettuare acquisti fraudolenti e agevolare estorsioni o ricatti. Le implicazioni vanno oltre la semplice minaccia alla sicurezza e alla privacy degli utenti, potendo causare danni finanziari significativi e danneggiare la reputazione delle vittime coinvolte. Di conseguenza, diventa cruciale una maggiore consapevolezza e precauzione da parte degli utenti e delle aziende per proteggere se stessi e i propri dati da queste minacce emergenti, considerando la sempre più diffusa presenza di dispositivi con assistenti vocali.

## REMEDIATION

Gli utenti possono adottare diverse strategie per mitigare il rischio derivante dalle vulnerabilità dei dispositivi IoT e degli assistenti vocali in essi contenuti. In primo luogo, è consigliabile mantenere costantemente aggiornati i firmware dei dispositivi, applicando le patch di sicurezza rilasciate dai produttori al fine di correggere eventuali falle di sicurezza.

Inoltre è opportuno gestire attentamente le autorizzazioni dei dispositivi, limitando le loro capacità solo alle funzionalità essenziali e disattivando le opzioni non utilizzate che potrebbero costituire potenziali vulnerabilità per la rete domestica e l’utente finale.

In aggiunta, è fondamentale adottare pratiche di sicurezza per la gestione delle password, utilizzando credenziali robuste e uniche e cambiandole regolarmente al fine di prevenire l'accesso non autorizzato.

Per difendersi da questi attacchi, infine, i produttori stanno valutando diverse soluzioni, come l'analisi radio del segnale ricevuto e l'alterazione della frequenza per proteggersi dagli attacchi ultrasonici, l'aggiunta di un PIN vocale per i comandi principali degli assistenti vocali.

## FONTI

CVE-2017-13107, CVE-2019-13156, CVE-2020-11976

[https://www.businessinsider.com/hackers-hijack-smart-speakers-apple-google-facebook-amazon-14-laser-2019-11](https://www.businessinsider.com/hackers-hijack-smart-speakers-apple-google-facebook-amazon-14-laser-2019-11)

[https://www.mdpi.com/2079-9292/12/8/1928](https://www.mdpi.com/2079-9292/12/8/1928) - Ricerca 1 

[https://www.youtube.com/watch?v=ORji7Tz5GiI](https://www.youtube.com/watch?v=ORji7Tz5GiI&ab_channel=LightCommands) - Ricerca video

[https://www.youtube.com/watch?v=ihRAwc24nXw](https://www.youtube.com/watch?v=ihRAwc24nXw) - Demo video

###