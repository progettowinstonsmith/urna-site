Title: Urna — PGMC - come modificare un sito Winston Smith
Date: 2015-04-24 10:20
lang: it


Per modificare uno dei siti Winston Smith realizzati con la catena PMGC è necessario:

1. Clonare (o aggiornare) il repository sorgente sul proprio sistema
2. Modificare i file Markdown
3. Rigenerare i file statici html
4. Verificare il risultato
5. Aggiornare il repository sorgente

Dopo la conclusione di quest'ultimo passo è possibile compiere i passi necessari alla
[pubblicazione del sito su casellante](/urna-pgmc-come-pubblicare-un-sito-winston-smith.html)

I repository sorgente di Winston Smith sono i seguenti:

- [Big Brother Awards](https://github.com/progettowinstonsmith/bba-site)
- [E-Privacy](https://github.com/progettowinstonsmith/e-privacy-site)
- [URNA](https://github.com/progettowinstonsmith/urna-site) (questo sito)
- [ANTANI](https://github.com/progettowinstonsmith/antani-site) (sito di prova, facci quello che ti va)

I collaboratori hanno accesso diretto ai repository e possono fare commit direttamente, gli altri possono comunque proporre pull-request.

### Clonare (o aggiornare) il repository sorgente sul proprio sistema

Se non si ha una versione locale dei file di creazione del sito è possibile clonare il repository con il comando:

	git clone https://github.com/progettowinstonsmith/urna-site.git

Verrà creata una directory `urna-site` all'interno della quale, tra gli altri ci sono i seguenti file o directory:

`pelicanconf.py`:
File di configurazione del sito

`content`:
Directory contenente i documenti Markdown o i file statici del sito

`theme`:
Directory contenente il _tema_ di rappresentazione del sito


All'interno della directory dei contenuti (`content`) ci sono i file delle differenti pagine presenti nel sito, ad es:


	$ ls -1 content/
	attivazione-pelican-markdown.md
    pmgc-modificare-siti.md
    urna.md

Ciascuno di questi file rappresenta una pagina del sito in formato testuale [Markdown](http://daringfireball.net/projects/markdown/syntax).

Se si ha già una directory contenente il clone della directory di lavoro *è necessario* prima della sessione di lavoro aggiornare i propri file integrando le modifiche esterne con il comando:

	git pull

### Modificare i file Markdown

I file Markdown devono essere creati o modificati usando un qualsiasi editor di testi (ad es. emacs o vi). Se si creano nuove pagine Markdown è sufficiente inserirle nella directory `content` per essere prese in considerazione per la pubblicazione, non è necessario aggiornare alcun elenco di pubblicazione.

### Rigenerare i file html

Una volta modificata la pagina Markdown è possibile ricreare l'intero sito e tutte le sue pagine HTML usando il comando:

	make html

Il sistema risponderà con un messaggio simile:

	Done: Processed 3 article(s), 0 draft(s) and 0 page(s) in 0.19 seconds.

### Verificare il risultato

I file generati sono disponibili nella cartella output (per capire bene il funzionamento della directory `output` leggere il documento sulla [pubblicazione online]() ).

Per verificare il risultato sulla macchina di lavoro è possibile lanciare un server HTTP locale con il comando:

	make serve

Un server verrà messo in esecuzione in modo sincrono e potrà essere verificato il contenuto del sito collegandosi al server (o a localhost) sulla porta 8000, ad es.:

	http://localhost:8000

Il sito dovrà risultare completamente funzionante e navigabile.

Per chiudere il server è sufficiente bloccare il comando con CTRL-C.

È anche possibile attivare un server in background con:

	make devserver

Che potrà essere abbattuto con il comando:

	make stopserver

### Aggiornare il repository sorgente

Accertatisi della correttezza delle modifiche apportate è possibile aggiornare il repository sorgente con il comando:

	git pull

oppure preparando una pull-request nelle modalità solite.


### Pubblicazione del sito online


Giunti a questo punto è possibile compiere di seguito i passi riportati nel documento di [pubblicazione del sito su casellante](/urna-pgmc-come-pubblicare-un-sito-winston-smith.html)






