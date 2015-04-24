Title: Urna — PGMC - come modificare un sito Winston Smith
Date: 2015-04-24 10:20
lang: it


Per modificare uno dei siti Winston Smith realizzati con la catena PMGC è necessario:

1. Clonare (o aggiornare) il repository sorgente sul proprio sistema
2. Modificare i file Markdown
3. Rigenerare i file statici html
4. Verificare il risultato
5. Aggiornare il repository sorgente
6. Pubblicare il risultato su casellante

I repository sorgente di Winston Smith sono i seguenti:

- [Big Brother Awards](https://github.com/progettowinstonsmith/bba-site)
- [E-Privacy](https://github.com/progettowinstonsmith/e-privacy-site)
- [URNA](https://github.com/progettowinstonsmith/urna-site)

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

Ciascuno di questi file rappresenta una pagina del sito in formato testuale [Markdown](http://daringfireball.net/projects/markdown/syntax)
Urna è il repository dei file digitali (audio,video,pdf,ecc…) ed è anche un sito contenente informazioni di lavoro e procedure su come gestire e manutenere tutto il sistema informatico di Winston Smith.

ENTRATE A VOSTRO RISCHIO E PERICOLO.

Tutte le informazioni su questo sito sono altamente instabili e volatili, maneggiare con cura!


## Procedure

### Siti PMGC (Pelican/Markdown/Github/Casellante)

A Winston Smith non piaccono i CMS ed usa solo siti statici. Ha scelto una tecnologia basata sull'integrazione verticale del sistema [Pelican](http://getpelican.org) con il formato testuale [Markdown](http://daringfireball.net/projects/markdown/syntax), il repository [GITHUB](http://github.org/progettowinstonsmith) sul proprio server denominato Casellante. 

- [Attivazione di un sottosistema pelican/markdown](/)
- [Come modificare una pagina di un sito PMGC](/)






