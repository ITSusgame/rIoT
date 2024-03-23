---
title: Hacking Di Baby Monitor Smart
published: true
---

## CONTESTO

L'hacking dei baby monitor rappresenta una minaccia sempre più diffusa per la sicurezza dei bambini e la privacy delle famiglie. Recentemente, diversi casi hanno evidenziato la vulnerabilità di questi dispositivi a manipolazioni da parte di estranei. Una coppia australiana ha scoperto un intruso che comunicava con la loro figlia di un anno attraverso il baby monitor, mentre una famiglia a Houston ha subito minacce da parte di un hacker che aveva preso il controllo del loro sistema di monitoraggio. Inoltre, il noto baby monitor Mi-Cam è stato trovato ad avere varie vulnerabilità che permettono agli hacker di accedere a informazioni personali e riprese video. Le conseguenze di questi attacchi vanno oltre l'invasione della privacy, mettendo a rischio la sicurezza dei bambini e la tranquillità delle famiglie. È essenziale che i genitori adottino misure di sicurezza adeguate, come cambiare le password predefinite, aggiornare regolarmente il firmware e disconnettere i dispositivi quando non sono in uso. Inoltre, le aziende produttrici di baby monitor e altri dispositivi connessi devono assumersi la responsabilità di garantire la sicurezza dei loro prodotti, implementando misure di protezione efficaci e rispondendo prontamente alle segnalazioni di vulnerabilità da parte degli utenti e dei ricercatori.

## LA VULNERABILITA’

Il baby monitor video Mi-Cam, promosso per la sua facilità d'uso e la qualità dell'immagine ad alta definizione, si è rivelato vulnerabile a diverse vulnerabilità critiche. Queste vulnerabilità includono:

- **Gestione di Sessioni Danneggiata e Riferimenti Diretti a Oggetti Non Sicuri**
    
    L'applicazione Android associata al baby monitor Mi-Cam presenta una gestione delle sessioni danneggiata, consentendo agli attaccanti di accedere a informazioni sensibili e di interagire con i baby monitor connessi.
    
- **Mancata Invalidazione dei Codici di Verifica per il Cambio Password**
    
    Il processo di cambio password non invalida i codici di verifica precedentemente generati, aprendo la porta a potenziali attacchi di forza bruta per ottenere il controllo dell'account.
    
- **Interfaccia Seriale Accessibile**
    
    Il baby monitor Mi-Cam presenta un'interfaccia UART accessibile, che permette agli attaccanti di ottenere accesso hardware al dispositivo e di analizzare il firmware per individuare ulteriori vulnerabilità.
    
- **Credenziali Predefinite Deboli**
    
    Le credenziali predefinite del baby monitor, inclusa la password per l'utente "root", sono estremamente deboli e facilmente violabili.
    
- **Enumerazione degli Account Utente**
    
    La funzionalità di reset della password rivela informazioni sugli account utente esistenti, facilitando ulteriori attacchi di forza bruta.
    
- **Software Obsoleto e Vulnerabile**
    
    Il firmware del baby monitor utilizza componenti software obsoleti e vulnerabili, aumentando il rischio di exploit da parte degli attaccanti.
    
    Queste vulnerabilità pongono una seria minaccia alla sicurezza dei bambini e delle loro famiglie, evidenziando l'importanza di implementare misure di sicurezza robuste nei dispositivi IoT. Gli sviluppatori e i fornitori di dispositivi IoT devono assumere la responsabilità di garantire che i loro prodotti siano adeguatamente protetti contro minacce informatiche e vulnerabilità di sicurezza.
    

## **Soluzione**

Il fornitore non è stato contattabile e non è disponibile alcun aggiornamento, pertanto si consiglia vivamente di non utilizzare questo prodotto in quanto non esiste alcuna soluzione alternativa disponibile.

## FONTI

[https://nypost.com/2023/10/23/lifestyle/parents-say-baby-monitor-was-hacked-someone-talked-to-child/](https://nypost.com/2023/10/23/lifestyle/parents-say-baby-monitor-was-hacked-someone-talked-to-child/)

[https://www.washingtonpost.com/technology/2018/12/20/nest-cam-baby-monitor-hacked-kidnap-threat-came-device-parents-say/](https://www.washingtonpost.com/technology/2018/12/20/nest-cam-baby-monitor-hacked-kidnap-threat-came-device-parents-say/)

[https://threatpost.com/rsac-2020-another-smart-baby-monitor-vulnerable-to-remote-hackers/153272/](https://threatpost.com/rsac-2020-another-smart-baby-monitor-vulnerable-to-remote-hackers/153272/)

[https://sec-consult.com/vulnerability-lab/advisory/hijacking-of-arbitrary-misafes-mi-cam-video-baby-monitors/](https://sec-consult.com/vulnerability-lab/advisory/hijacking-of-arbitrary-misafes-mi-cam-video-baby-monitors/)  — lo studio

[https://www.youtube.com/watch?v=SsYnXRUhpL0](https://www.youtube.com/watch?v=SsYnXRUhpL0)  — il PoC
