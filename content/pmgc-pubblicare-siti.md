Title: Urna — PGMC - come pubblicare un sito Winston Smith
Date: 2015-04-24 10:20
lang: it

Esistono due differenti modi per pubblicare un sito Winston Smith PMGC a seconda che si abbia o meno l'accesso diretto a Casellante:


## Se non hai accesso a Casellante

In questo caso:

- se non hai accesso neppure al [repository](https://github.com/progettowinstonsmith) dei siti su Github, l'unico modo di contribuire è preparare una [pull-request](https://help.github.com/articles/creating-a-pull-request/) e contattare uno degli amministratori.

- se hai almeno accesso al repository dei siti su Github ma non a Casellante puoi rigenerare la versione statica e attendere il prossimo aggiornamento periodico.

## Se hai accesso a Casellante

(ed hai pure particolare fretta tanto da non voler attenere l'aggiornamento periodico)

- rigenera la versione statica e senza attendere il prossimo aggiornamento periodico,
- forza la sincronizzazione immediata


## Come rigenerare la versione statica del sito

Segui semplicemente i passi già indicati in [come modificare un sito Winston Smith](/urna-pgmc-come-modificare-un-sito-winston-smith.html), nel tuo ambiente di lavoro o in quello di `ampleforth`. Verifica sempre che il sito non abbia problemi.

Entra nella directory `output`:

	cd output

Pubblica su github la nuova versione del sito (il repository del sito statico è differente da quello di generazione e contiene solo i file html e di supporto):

	git push

A questo punto il sito sarà pubblicato  attraverso un automatismo periodico.

## Come forzare l'immediata sincronizzazione

Entrare nel proprio utente di Casellante ed eseguire il comando:

	pmgc-resync-now <label>

A questo punto abbi fiducia e dopo qualche minuto verifica che sia andato tutto bene.


## Trucco veramente sporco per sincronizzare SUBITO

Se sei uno dei pochi fortunati dotato di un accesso ssh ai siti web di casellante, puoi dare il seguente comando direttamente dalla directory `<progetto>-site` dopo aver rigenerato (e verificato la correttezza del sito):

	make ssh_update

Attenzione: se non hai committato correttamente *i file statici anche* alla prima fase di aggiornamento periodico le modifiche _scompariranno_ (non del tutto se hai almeno committato il sorgente).

PS - Perché questo trucco funzioni c'è un ingrediente segreto che dovrò dirti a voce.
