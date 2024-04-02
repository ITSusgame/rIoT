---
title: Hacking Di Frigoriferi Smart
published: true
---
## Rischi e Rimedi per i Frigoriferi Smart

### Contesto

Durante il DefCon 23's IoT Village, è stato lanciato un intrigante sfida: "Puoi prendere il controllo del nostro frigorifero Samsung RF28HMELBSR IoT?" Questo frigorifero, parte della linea Smart Home di Samsung, offre funzionalità come la visualizzazione del calendario di Google e la gestione degli eventi direttamente dallo schermo del frigorifero.

### Vulnerabilità

Un team di esperti ha individuato diverse vulnerabilità nel frigorifero, rendendolo suscettibile a vari tipi di attacchi.

- **Attacco Man-in-the-Middle (MITM)**

Nonostante l'implementazione di SSL, il frigorifero non convalida correttamente i certificati SSL, consentendo quindi attacchi MITM contro la maggior parte delle connessioni. Questo include le connessioni ai server di Google per scaricare le informazioni del calendario Gmail, rendendo potenzialmente esposte le credenziali Gmail degli utenti.

- **Servizio Google Calendar**

Il frigorifero esegue Google Calendar, consentendo agli utenti di impostare eventi e gestire gli impegni direttamente dallo schermo del frigorifero. Tuttavia, sono state riscontrate alcune vulnerabilità legate agli aggiornamenti dell'API.

- **Attacco Firmware**

È stata esaminata la possibilità di compromettere il frigorifero attraverso un falso aggiornamento del firmware. Sebbene sia stato individuato lo schema URL per scaricare il file del firmware, alcuni parametri necessari per completare l'URL rimangono sconosciuti.

- **Servizi TCP e sfide legate ai certificati**

Il terminale del frigorifero dispone di almeno due servizi in ascolto, uno sulla porta 4444 (SSL) e uno sulla porta 8888. Il servizio sulla porta 4444 richiede un certificato lato client per la maggior parte delle richieste, sebbene non tutte siano convalidate contro il certificato lato client.

### Conclusioni

Le vulnerabilità scoperte nel frigorifero Samsung RF28HMELBSR evidenziano la necessità di rigorose misure di sicurezza nell'ambito degli dispositivi IoT. È fondamentale che i produttori implementino soluzioni di sicurezza robuste per proteggere i dispositivi e i dati degli utenti.

### FONTI

[https://www.pentestpartners.com/security-blog/hacking-defcon-23s-iot-village-samsung-fridge/](https://www.pentestpartners.com/security-blog/hacking-defcon-23s-iot-village-samsung-fridge/)
