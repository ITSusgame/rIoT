---
title: Hacking di Termostati Smart
published: true
---

## Contesto

L'IoT (Internet of Things) ha rivoluzionato il modo in cui interagiamo nel nostro quotidiano con la casa, sia in termini di comodità sia in termini di gestione oconomica dei consumi. Grazie alla sua diffusione sempre più ampia, l'IoT offre una vasta gamma di prodotti/elettrodfomestici avanzati che vanno ben oltre la semplice accensione/spegnimento remoti o programmati. Una delle principali ragioni della loro popolarità è il loro prezzo sempre più accessibile, i tantissimi produttori che offorono soluzioni divedrse ed i vari ecosistemi che li rende sempre più versatili in modo da coprire le esegenze di un vasto pubblico di consumatori. In particolare uno dei prodotti più "colpiti" dall'IoT sono i termostati, divventati sempre più connessi, articolati ed inteligenti, ossia SMART. La capacità "SMART" di questi prodotti si manifesta attraverso la connettività Internet integrata, consentendo agli utenti di accedere a una vasta gamma di servizi online come l'apprendimento e l'ottimizzazione dell'utilizzo dell'impianto di riscaldamente grazie a degli algoritmi che apprendimento, l'accensione\spegnimento, gestione della temperatura programmati, da remoto, vocali e tramite geolocalizzazione. Grazie alla loro crescente diffusione e alle loro capacità avanzate, stanno rapidamente diventando uno degli elementi più importanti ed insostituibili all'interno dell'ambiente domestico moderno.

## La Ricerca

E' inevitabile che i cyber criminali prendano di mira dei dispositivi l'IoT sempre più frequanentemente, poichè una Smart Home offre una superfice d'attacco ampia e spesso priva di grandi ostacoli. 

**L'Institute for Critical Infrastructure Technology (ICIT)** descrive l'aumento dei malware come una "epidemia" e afferma che l'IoT è particolarmente a rischio. 
**James Scott, senior fellow presso l’Institute for Critical Infrastructure Technology, e Drew Spaniel, visiting fellow dell’ICIT presso la Carnegie Mellon University** che definiscono l'IoT come una "superfice d'attacco infinita", e il conseguente aumento dello sviluppo e diffusione dei 
malware che lo prendono di mira come "nomale"  poichè molti dispositivi IoT mancano di qualsiasi forma di sicurezza, sia da parte dei produittori che nel loro utilizzo da perte degli utenti.  

## L'exploit
**Sostanzialmente un Ransomware è un programma informatico malevolo che può “infettare” un dispositivo digitale (PC, tablet, smartphone, smart TV, etc), bloccando l'accesso a tutti o ad alcuni dei suoi contenuti o funzioni, per poi chiedere un riscattoda pagare per “liberarli”.**
**Andrew Tierney e Ken Munro ricercatori britannici della nota azienda di sicurezza Pen Test Partners** che si occupa di scoprire le vulnerabilità dei sistemi, ha scoperto l'esistenza di un Ransomware in grado di bloccare determinati termostati SMART. 

Il termostato in questione ha un grosso display LCD su cui giro il sistema operativo Linux customizzato, ed è munito di una scheda SD che permette agli utenti di caricare delle impostazioni (chiamate in gergo "scene") modificate/personalizzate, dei wallpaper/immagini personali per customizzare l'interfaccia
e aggiornamenti software manuali.
L'exploit scoperto dai ricercatori consiste nella mancata verifica del tipo di file caricato nella scheda ed eseguito poi nel sistema operativo. Ciò permetterebbe a un hacker di nascondere un malware dentro un file che assomiglia ad un'immagine, ad una "scena"/routine del dispositivo smart scaricata dall'utente facendola passare anche come creata dal produttore,
ingannando l'utente, facendogli caricare in memoria quindi, un file compromesso che il termostato SMART eseguirà senza alcun tipo di controllo, eseguendo quindi il malware/ransomware o permettendo l'installazione di un applicativo dannoso all'interno del dispsoitivo. 

## Remediation

le soluzioni che si possono mettere in atto sono moltissime e dipendono principalmente dalla volontà del' produttore di dare supporto ai propri dispositivi, e dell'utente di proteggere la propria privacy e sicurezza informatica.

I produttori dovrebbero impegnarsi nello sviluppo di soluzioni sicure, affidabili, aggiornabili, ripensando in modo coordinato alle policy in materia di sicurezza, fornendo continuo supporto attravverso il rilascio di regolari patch di sicurezza.

Importante, da parte dell'utente è tenere quindi sempre aggiornato il firmware del dispositivo SMART ma in generale di ogni dispositivo connesso alla rete domestica. Aggiornare regolarmente il software riduce le vulnerabilità che potrebbero permettere agli hacker di infiltrarsi nei nostri dispositivi. 
Inoltre, è sempre consigliabile utilizzare password robuste e complesse per proteggere l'accesso alla rete Wi-Fi e all'account associato al termostato smart. Accorgimento mai banale, poichè gran parte degli attacchi ai dispositivi è frutto di credenziali di default (note a tutti poichè uguali per tutti i prodotti) lasciate immutate.
Un'altra misura di sicurezza importante è quella di abilitare l'accesso al termostato solamente ai dispostivi realmente necesari per la sua gestione\utilizzo. In questo modo riduce notevolmente la superficie d'attacco e si limita la possibilità che terzi possano accedere al termostato senza prima aver violato il nostro dispositivo.
Infine, è fondamentale fare attenzione agli abbonamenti e agli aggiornamenti software proposti da terze parti o da fonti non autorizzate.
Evitare di scaricare applicazioni o software promettenti funzionalità aggiuntive senza prima verificare la loro affidabilità e provenienza riduce il rischio di installare malware dannosi che possano compromettere la sicurezza del dispositivo e di tutti quelli connessi.

## Fonti

[https://www.pentestpartners.com/security-blog/

[https://www.vice.com/it/article/d7dbbx/ransomware-termostati-smart-internet-of-things

[https://www.infosecurity-magazine.com/news/defcon-thermostat-control-hacked/
