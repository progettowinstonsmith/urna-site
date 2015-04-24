Title: Urna - PMGC - Attivazione di un sottosistema pelican/markdown
Date: 2015-04-24 10:20
lang: it

Per attivare un sistema di lavorazione delle pagine web dei nuovi siti di Winston Smith è necessario attivare un sistema autonomo Pelican/Markdown sul proprio computer (i pochi sfortunati che hanno accesso ai server del PWS troveranno un sistema già attivo all'account `ampleforth`).

Il processo è costituito in tre passi:

1. Installazione dell'interprete Python
2. Creazione di un ambiente virtuale dedicato a Pelican
3. Installazione di Pelican e Markdown

Se hai già a disposizione (o sai come fare in autonomia) ciascuno di questi passi, puoi direttamente saltare a quello successivo.

## Installazione di python (con Miniconda)

Miniconda è un progetto che mette a disposizione nello spazio d'utente una installazione completa di Python e un gestore di pacchetti (conda). È un modo molto semplice per gestire ambienti virtuali e installazioni di pacchetti Python anche da parte di chi è alle prime armi. È possibile installare un interprete python con Miniconda anche se si ha già un python installato nel sistema, semplicemente ad un certo punto si sceglierà di usare quello messo a disposizione da miniconda.

Per installare Miniconda scarica il file adatto al tuo sistema operativo (Linux, Mac OS X, Windows) dalla pagina http://conda.pydata.org/miniconda.html e segui le informazioni per l'installazione (in breve: esegui il file dalla linea di comando).

La procedura d'installazione creerà una distribuzione Python completa e funzionante nella tua directory utente $HOME (di solito nella cartella `$HOME/miniconda`). Non hai bisogno dei privilegi di amministrazione del sistema per installare miniconda. Dopo l'installazione basterà includere la directory dei binari per poter utilizzare il nuovo interprete, ad es. sui sistemi basati su Unix si userà il comando:

    export PATH=~/miniconda/bin:$PATH

Questo comando puoi metterlo nella `.bash_profile` per poter usare quest'interprete anche la prossima volta che ti colleghi al sistema.

Hai così installato un interprete python.

## Creazione di un ambiente virtuale per Pelican

Sebbene sia possibile installare i pacchetti necessari al lavoro su Pelican direttamente nell'ambiente base di python è solitamente consigliato creare un ambiente virtuale python dedicato. È molto conosciuto il progetto `virtualenv` per questo. Con Miniconda però  il sistema di distribuzione dei pacchetti (chiamato `conda`) permette di creare ambienti di lavoro separati per progetti.

Quindi ti basterà usare il comando: 

    conda create -n pws python pip

per creare un nuovo ambiente virtuale chiamato `pws` (ma poteva essere qualsiasi altro nome). Installerà all'interno il linguaggio `python` e il pacchetto `pip`.

Per attivare l'ambiente sarà sufficiente usare il comando:

    source activate pws

Da quel momento all'estrema sinistra del prompt vedrai l'indicazione dell'ambiente virtuale:

     (pws) casellante:~# 

Nella prossima sessione di lavoro non ci sarà bisogno di ricreare l'ambiente virtuale, basterà solo attivarlo con il comando già visto:

    source activate pws

Hai così realizzato un ambiente virtuale python per poter lavorare con pelican e i siti PMGC di Winston Smith.

## Installazione di Pelican e Markdown

L'ultimo passo da compiere, una volta creato l'ambiente virtuale di lavoro, è l'installazione dei package di lavoro `pelican` e `markdown` attraverso il sistema di packaging standard di python `pip`.

Il comando è:

    pip install pelican markdown

Il sistema pip scaricherà questi pacchetti e tutte quelli necessari e completerà l'installazione in breve. Al termine potrai usare il comando:

    pelican-quickstart

come indicato dal [tutorial](http://pelican.readthedocs.org/) di pelican.


Ecco fatto!

Ora puoi iniziare a [modificare una pagina di un sito PMGC](/)







