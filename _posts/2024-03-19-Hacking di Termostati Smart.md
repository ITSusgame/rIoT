---
title: Hacking di Termostati Smart
published: true
---
## Ransomware e termostati smart

### CONTESTO

Le caratteristiche "SMART" di questi prodotti si traducono nella loro connettività Internet integrata che consente agli utenti di accedere a una vasta gamma di servizi su questi dispositivi attraverso il controllo da remoto. Tra questi, vi sono funzionalità come l'ottimizzazione del sistema di riscaldamento attraverso algoritmi di apprendimento delle abitudini dell’utente, la programmazione dell'accensione/spegnimento e ovviamente la gestione a distanza della temperatura. Grazie alla loro crescente diffusione e alle loro capacità avanzate, questi prodotti stanno rapidamente diventando degli elementi importanti all'interno delle moderne abitazioni.

E' inevitabile che i cyber criminali prendano di mira i dispositivi l'IoT in modo sempre più frequente, poiché una Smart Home offre una superficie d'attacco ampia e spesso priva di misure di protezione adeguate.

### L’EXPLOIT

**Un Ransomware è un programma informatico malevolo che può “infettare” un dispositivo digitale bloccando l'accesso a tutti o ad alcuni dei suoi contenuti o servizi, per poi chiedere un riscatto da pagare per poter tornare a fruire di tutte le funzioni dell’apparecchio.**

**Alcuni ricercatori britannici** hanno scoperto l'esistenza di un Ransomware in grado di bloccare determinati modelli termostati IoT.

Il termostato in questione ha un grosso display LCD attraverso il quale il sistema operativo Linux installato a bordo può interagire con l’utente, ed è munito di una scheda SD che permette a chi lo usa di caricare delle impostazioni (chiamate in gergo "scene") personalizzate, dei wallpaper per customizzare l'interfaccia e aggiornamenti software manuali.
La criticità scoperta dai ricercatori consiste nel fatto che il dispositivo non controlla correttamente  l’estensione del tipo di file caricato nella scheda, con la possibilità di eseguire poi nel sistema operativo azioni non previste o addirittura indesiderate. 

Ciò permette ad un hacker di nascondere un malware dentro un file che si spaccia per un'immagine oppure ad una "scena" del dispositivo, che il termostato SMART eseguirà senza alcun tipo di controllo, attivando il codice malevolo.
Questo tipo di compromissione, nel caso si sia infettati da un Ransomware, può causare il blocco completo del dispositivo o persino il settaggio della temperatura a valori troppo alti o freddi per risultare confortevoli, fino al pagamento di un riscatto ai malintenzionati al fine di ridarti il controllo sul tuo dispositivo.

### REMEDIATION

le soluzioni che si possono mettere in atto sono plurime e dipendono sia dalla volontà del produttore di dare supporto continuato ai propri dispositivi, sia dalla volontà dell'utente di proteggere la propria privacy.

I produttori dovrebbero impegnarsi nello sviluppo di soluzioni sicure, affidabili, aggiornabili, rifacendosi alle policy  e “best practices” in materia di sicurezza, fornendo un supporto continuato attraverso il rilascio di regolari patch di sicurezza del firmware, del software e dei servizi sugli apparati che distribuiscono.

Da parte dell'utente invece è richiesto di mantenere sempre aggiornato il dispositivo riducendo la possibilità che determinate vulnerabilità permettano agli hacker di infiltrarsi nei nostri elettrodomestici.
Inoltre, l’utilizzo di password robuste per proteggere gli accessi alla rete, ai servizi e all'account associati al termostato smart, dal momento che gran parte degli attacchi ai dispositivi è frutto di credenziali di default facilmente reperibili online.
Un'altra misura di sicurezza importante è quella di limitare l'accesso al termostato solamente ai dispositivi necessari al suo utilizzo e di spegnere tutti i servizi extra che non vengono utilizzati. In questo modo si riduce notevolmente la superficie d'attacco e si limita la possibilità che i male intenzionati possano accedere al termostato.

### Fonti

[https://www.pentestpartners.com/security-blog/](https://www.pentestpartners.com/security-blog/)

[https://www.vice.com/it/article/d7dbbx/ransomware-termostati-smart-internet-of-things/](https://www.vice.com/it/article/d7dbbx/ransomware-termostati-smart-internet-of-things/)

[https://www.infosecurity-magazine.com/news/defcon-thermostat-control-hacked/](https://www.infosecurity-magazine.com/news/defcon-thermostat-control-hacked/)
