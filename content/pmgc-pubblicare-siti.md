Title: Urna — PGMC - come pubblicare un sito Winston Smith
Date: 2015-04-24 10:20
lang: it

Esistono due differenti modi per pubblicare un sito Winston Smith PMGC a seconda che si abbia o meno l'accesso diretto a Casellante:


## Se non hai accesso a Casellante

In questo caso:

- se non hai accesso neppure al [repository](https://github.com/progettowinstonsmith) dei siti su Github, l'unico modo di contribuire è preparare una [pull-request](https://help.github.com/articles/creating-a-pull-request/) e contattare uno degli amministratori.


## Se hai accesso a Casellante

(ed hai pure particolare fretta tanto da non voler attendere l'aggiornamento periodico)

- rigenera la versione statica e senza attendere il prossimo aggiornamento periodico,
- forza la sincronizzazione immediata


## Come rigenerare la versione statica del sito

Segui semplicemente i passi già indicati in [come modificare un sito Winston Smith](/urna-pgmc-come-modificare-un-sito-winston-smith.html), nel tuo ambiente di lavoro o in quello di `ampleforth`. Verifica sempre che il sito non abbia problemi.

## Come forzare l'immediata sincronizzazione

Entrare nel proprio utente di Casellante ed eseguire il comando:

	~/bin/eprivacy-resync-now 

A questo punto abbi fiducia e dopo qualche minuto verifica che sia andato tutto bene.


## Trucco veramente sporco per sincronizzare SUBITO

Se sei uno dei pochi fortunati dotato di un accesso ssh ai siti web di casellante, puoi dare il seguente comando direttamente dalla directory `<progetto>-site` dopo aver rigenerato (e verificato la correttezza del sito):

	make ssh_update

PS - Perché questo trucco funzioni c'è un ingrediente segreto che dovrò dirti a voce.
