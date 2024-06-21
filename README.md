# ![_labadessa-19052024-0001](https://github.com/Eklip5e/Piccolo/assets/38536104/1a1ce4a8-7c2e-4a07-bb91-bd0d47d730c3)

Piccolo è un bot per Telegram, Fork di [Fioriktos](https://github.com/FiorixF1/fioriktos-bot). 
Utilizza [Markov chains](https://en.wikipedia.org/wiki/Markov_chain) per imparare a parlare, dai messaggi che i vari utenti inviano. 
Piccolo può rispondere con messaggi di testo, ma anche sticker, gifs ed audio.

Questi sono i comandi che puoi utilizzare:
```
    piccolo - Forzami a parlare
    sticker - Invio uno sticker
    gif - Invio una gif
    audio - Invio un audio
    torrent - Con uno spazio accanto al comando, ed un numero da 1 a 10, deciderai la frequenza di quanto devo parlare
    enablelearning - Impara
    disablelearning - Smetto di imparare
    thanos - Dimezza tutto quello che so.
    boc - Best of Capannina
    gdpr - Robette di privacy :)
```

Il comando ```/gdpr``` ha un ulteriore ruolo, in quanto gestione del bot:
* ```/gdpr download``` :  Scarica tutti i dati della chat in cui ti trovi in un file, così che l'utente può leggere le parole imparate dal bot.

* ```/gdpr delete``` :  Elimina l'intero database della chat in un unica mossa; Utilizza questo comando con parsimonia in quanto l'azione non è reversibile

* ```/gdpr flag``` : Se usato rispondendo ad un determinato sticker o gif, eliminerà quest'ultimo dal database e in futuro, non lo invierà più. Solitamente questo comando può essere usato se c'è uno spam elevato di sticker e gif, come porno o altri generi che potrebbero triggerare i membri;
* L'azione è reversibile con ```/gdpr unflag```.

* ```/gdpr tx``` :  Se desideri trasferire il database di ciò che ha imparato Piccolo, da una chat ad un'altra, questo comando fa a caso tuo, ti basterà usare questo comando sulla chat "Mittente", il bot risponderà con qualcosa del tipo ```/gdpr rx DEADBEEF```, che dovrai copiare ed incollare sulla chat "Destinatario".

Dato che il bot ha accesso ai messaggi di Telegram delle varie chat con cui interagisce, è stato creato con lo scopo di essere letto, modificato ed avere una completa trasparenza con gli utenti che lo usano.
Il codice è quindi pubblico, per garantire agli utenti che i dati, di fronte al bot, non verranno mai utilizzati in maniera impropria;
Cosa che non è paragonabile ad altri bot simili a Fioriktos e Piccolo.
# FAQ

## Chi è Piccolo?
![9788807550492_quarta jpg 800x800_q75](https://github.com/Eklip5e/Piccolo/assets/38536104/1020a2df-64f8-47e7-96ef-a044f517d68c)

Piccolo è un personaggio fictional, creato nel 25 Giugno 2020 dall'illustratore e graphic designer [Mattia Labadessa](https://www.instagram.com/_labadessa/) , abbiamo imparato a conoscere Piccolo all'interno del libro ["Piccolo!"](https://www.feltrinellieditore.it/opera/piccolo/) e nelle varie storie che Mattia posta, con tanto di sondaggi, che rendono l'interazione col personaggio e l'illustratore più dinamica.
#### "Non nel senso che sono piccolo, ma proprio perchè mi chiamo Piccolo!"

Attualmente, quest'anno (2024), Mattia ha creato un canale telegram e successivamente, un gruppo, una piccola parte di questi fan si è riunita in separata sede creando un forte legame.
Dall'esigenza di avere un clone del bot Fioriktos, per rimanere in tema col gruppo che ha fatto sì che nascessero tante amicizie ed amori, nasce il bot Piccolo.

## Quali dati personali conserva Piccolo?
Piccolo conserva solo un set di dati per ogni chat in cui è stato inserito.
Il set di dati è il seguente:
* Chat ID
* Un set di parole costruito dai vari messaggi
* Gli sticker inviati
* Le gif inviate

Piccolo non conserva nient'altro delle cose presenti in questa lista, non avrà quindi accesso a cose come l'username, dati personali e foto di profilo degli utenti.
C'è da mantenere a mente che il bot **non conserverà l'intero messaggio**, (altrimenti renderebbe le cose parecchio disagianti); Ma solo le singole parole che compongono il messaggio, che aiuteranno a rafforzare la catena di Markov.

## Dove gira Piccolo?

A differenza di Fioriktos, che gira su un servizio di hosting a pagamento - [Heroku](https://www.heroku.com/) - e il database delle cose imparate su [Amazon S3 Bucket](https://aws.amazon.com/it/s3/);

Piccolo è invece hostato su una piccola macchina virtuale, tramite il modello di learning  ```TwoLevelCache ```, in quanto un bot dedito ad essere usato da pochissime persone rispetto bot Fioriktos, con una gestione migliore.

## I miei dati verranno conservati permanentemente?

No, Piccolo ha un countdown di 90 giorni di inattività, dove se in quel periodo non è stato usato o è stato rimosso dal gruppo, dopo quel periodo, eliminerà l'intero database;
A meno che non venga riaggiunto in tempo prima di questo periodo.

## Cosa mi assicura che tu non vada a leggere i miei messaggi privati?

Come già detto, Piccolo, come Fioriktos, non conserverà l'intero messaggio, ma lo scomporrà ed utilizzerà solo le singole parole che lo compongono, quindi non è tecnicamente possibile poter riassemblare a ritroso il messaggio.
Comunque, ci tengo a dire che, in qualsiasi modo decidessi di usare altri bot, non per forza Fioriktos e simili, devi essere consapevole di star correndo il rischio che il bot possa usare i dati scorrettamente, in quanto datogli l'accesso da **TE** e nessun altro;
Soprattutto in parecchi casi dove il bot è closed-source, ovvero il codice non è accessibile agli altri e che quindi, non potete mai sapere dove tutti i dati possano andare a finire a meno che non siate voi ad aver programmato il bot e conoscete il suo funzionamento.
Nessuno può garantirvi al 100% che uno sviluppatore di un programma o di un bot closed-source, possa improvvisamente leggere i vostri messaggi e i vostri dati, o che questi ultimi possano essere hostati in paesi dove è lecito farlo, anche senza il vostro consenso. 
Visto che questo progetto è open-source, posso solo che dirvi che nei vostri panni mi sentirei più al sicuro.
Se invece, preferite avere un vostro clone, così da poter avere la certezza che i vostri dati saranno solo ed unicamente visibili da voi, ecco a voi la risposta alla prossima domanda:

## Posso clonare Piccolo?

In questo caso, Piccolo come già accennato prima, è già un clone del [bot ufficiale](https://github.com/FiorixF1/fioriktos-bot).
Se avete quindi intenzione di creare un bot personale, come Piccolo, vi consiglio vivamente di leggere [la guida](https://github.com/FiorixF1/fioriktos-bot?tab=readme-ov-file#can-i-clone-this-project-and-make-my-custom-version-of-fioriktos) presente sulla repository originale.

### In caso di vari problemi non esitate a contattarmi su Telegram - @Eklip5e

## Supporta me e il creatore originale!

Sfortunatamente dopo una serie di cambiamenti sulla piattaforma di Heroku, circa Novembre 2022, non è più possibile hostare gratuitamente i vostri progetti, ed Amazon S3 è sempre stato un servizio a pagamento molto salato. 
Il bot quindi, per restare in vita dev'essere pur finanziato in qualche modo, soprattutto in un progetto aperto a tutti come questo dove il suo funzionamento non è retribuito.
Per questo motivo, vi consiglio di fare una donazione al creatore del bot sul sito _**Buy me a Coffee**_.
Anche una singola donazione può aiutare, in quanto le spese per mantenere il bot in piedi, rientrerebbero nei 15€/mese che, una sola persona non riuscirebbe a sostenere.
Nel caso in cui, foste interessati a sostenere mensilmente il creatore, sono già presenti dei tier a partire dai 2€/mese:
* Bronze 🥉 level 2€ / month
* Silver 🥈 level 5€ / month
* Gold 🥇 level 8€ / month

<img src="https://www.buymeacoffee.com/assets/img/guidelines/download-assets-sm-1.svg" alt="Buymeacoffee logo" width=100/> - [Buy me a coffee](https://www.buymeacoffee.com/fiorixf2W)

## Se invece, siete propensi a fare lo stesso per me, vi lascio qui il mio _**Buy Me a Coffee**_ !

In quanto programmatore, graphic designer e sviluppatore di diversi pacchetti di Minecraft, il mio lavoro lo considero equalmente valido e non retribuito, ma libero di essere apprezzato dai singoli, che si imbatteranno un giorno nei miei progetti.
Se quindi, vi sentite di fare anche a me una piccola donazione, qui sotto troverete il mio link della piattaforma Buy Me a Coffee!

<img src="https://www.buymeacoffee.com/assets/img/guidelines/download-assets-sm-1.svg" alt="Buymeacoffee logo" width=100/> - [Buy me a coffee](https://buymeacoffee.com/eklip5e)

Grazie per il supporto e per la lettura!
