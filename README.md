<a href="https://ondata.substack.com/" target="_blank">
  <img src="https://img.shields.io/badge/onData-newsletter-blue?style=for-the-badge&logo=substack&logoColor=white&labelColor=FF4B4B" alt="onData newsletter">
</a>

# Come assicurarsi che nessuno si interessi ai tuoi dati aperti <!-- omit in toc -->

Articolo originariamente scritto da Philip Heltweg: [How to Make Sure No One Cares About Your Open Data](https://www.heltweg.org/posts/how-to-make-sure-no-one-cares-about-your-open-data/)

La traduzione italiana è a cura di [Antonio Vivace](https://github.com/avivace) e [Marco Cortella](https://github.com/mcortella) per [onData](https://www.ondata.it/). Puoi contribuire a migliorarla [qui](https://github.com/ondata/dati_aperti_senza_interesse).

---

- [1. Utilizza una licenza oscura](#1-utilizza-una-licenza-oscura)
- [2. Pubblica solo metadati](#2-pubblica-solo-metadati)
  - [2.5 Meno informazioni dai, meglio è](#25-meno-informazioni-dai-meglio-è)
- [3. Rendili difficili da trovare](#3-rendili-difficili-da-trovare)
- [4. Usa formati scomodi e rari](#4-usa-formati-scomodi-e-rari)
  - [4.5 Esporta in modalità "human-friendly"](#45-esporta-in-modalità-human-friendly)
- [5. Assicurati della presenza degli errori 404](#5-assicurati-della-presenza-degli-errori-404)
  - [5.5 Cambia i dati dopo la pubblicazione](#55-cambia-i-dati-dopo-la-pubblicazione)
- [6. Frammenta i set di dati collegati](#6-frammenta-i-set-di-dati-collegati)
- [Conclusione](#conclusione)

Condividere dati aperti è un'impresa nobile. Può stimolare la ricerca, l'innovazione e la trasparenza. È anche molto difficile e fastidioso da fare, e in più si perde il controllo: chissà cosa combinerà la gente. Purtroppo, pubblicare dati aperti è spesso un obbligo legale. La soluzione migliore è quindi pubblicarli, ma assicurandosi che nessuno se ne interessi. Basandomi sulla mia esperienza parlando con professionisti dei dati aperti, lavorando con varie fonti di dati aperti e insegnando agli studenti l'ingegneria dei dati, ecco un elenco di strategie comuni che ti aiuteranno a evitare qualsiasi attenzione da parte degli utenti effettivamente interessati a lavorare con i tuoi dati.

## 1. Utilizza una licenza oscura

Il modo più semplice per spaventare i potenziali utenti è quello di rendere difficile comprendere se i tuoi dati sono aperti. Evita le licenze comuni con descrizioni chiare (come [quelle di OKFN](https://opendefinition.org/licenses/)) e nascondi la licenza effettiva (evita [identificatori SPDX](https://spdx.org/licenses/) nei metadati). Se possibile, non usare proprio alcuna licenza e fai riferimento solo a termini di utilizzo o documenti simili.

Se non puoi evitare una licenza standard, cerca di trovare una licenza nella tua lingua locale, che perlomeno scoraggerà gli utenti internazionali.

Punti bonus se pubblichi su Kaggle con la licenza "Altro (specificato nella descrizione)" e non scrivi nulla sulla licenza nella descrizione.

## 2. Pubblica solo metadati

Guarda questa mappa interattiva realizzata dall'agenzia nazionale francese per i dati sui trasporti: [https://transport.data.gouv.fr/?locale=en](https://transport.data.gouv.fr/?locale=en).

![Explore page of the French national access point to transport data](https://www.heltweg.org/posts/how-to-make-sure-no-one-cares-about-your-open-data/explore-map.png#center)

Oppure il progetto [Datenwaben](https://datenwaben.de/?city=vienna&page=cards) di [Thomas Tursics](https://toot.berlin/@tursics@toot.berlin).

Non ti stimolano idee per progetti basati su questi dati? Non te li fanno sembrare interessanti?

Terribile. Cerca di pubblicare solo i metadati minimi richiesti e di scrivere descrizioni ovvie e noiose. Se puoi, evita di presentare esempi dei dati o di spiegare come usarli a tutti i costi. Ci sono così tanti set di dati generici là fuori che puoi nasconderti nella folla.

### 2.5 Meno informazioni dai, meglio è

Piattaforme come Kaggle mostrano automaticamente agli utenti un'anteprima dei dati. Vedi questo set di dati sull'individuazione delle frodi con carte di credito (con utili visualizzazioni): [https://www.kaggle.com/datasets/kartik2112/fraud-detection](https://www.kaggle.com/datasets/kartik2112/fraud-detection).

![Useful visualization of data on Kaggle. This is the enemy.](https://www.heltweg.org/posts/how-to-make-sure-no-one-cares-about-your-open-data/data-visualisation.png#center)

Con anteprime dei dati e riassunti delle distribuzioni dei valori in ciascuna colonna, è davvero facile giudicare se i dati sono appropriati da utilizzare.

Questo potrebbe semplificare l'esperienza per l'utente e sarà più probabile che li utilizzi effettivamente.

Quindi, evita di generare anteprime o riassunti dei tuoi dati.

## 3. Rendili difficili da trovare

Scegli nomi brevi e non descrittivi e descrizioni minimaliste per ostacolare l'indicizzazione da parte dei motori di ricerca. Inoltre, evita di distribuirli ampiamente.

I portali di dati aperti come [govdata.de](https://www.govdata.de/) spesso dispongono di funzioni di ricerca ben fatte o persino di API che possono essere utilizzate programmaticamente. Questo è ovviamente un disastro, quindi assicurati di creare un altro portale di dati che usi solo tu e pubblica i dati solo lì.

## 4. Usa formati scomodi e rari

Se pubblichi i tuoi dati in formati facilmente utilizzabili come CSV o JSON, devi accettare il rischio che gli utenti possano accedere ai tuoi dati liberamente. Puoi provare a pubblicarli in un formato che richiede software proprietario come XLS, ma anche questo oggi può essere convertito dalla maggior parte delle persone. La cosa migliore sarebbe utilizzare un formato di file non leggibile dalle macchine.

I PDF sono una scelta popolare, specialmente se includi del testo di "riempimento" come intestazioni o piè di pagina oltre ai dati stessi.

![The Federal Statistical Office of Germany foolishly offering a choice of common data formats to download](https://www.heltweg.org/posts/how-to-make-sure-no-one-cares-about-your-open-data/multiple-file-formats.png#center)

### 4.5 Esporta in modalità "human-friendly"

Quando esporti dati tabellari, è bene mantenere la struttura originariamente pensata per la lettura da parte delle persone. Includi celle unite, intestazioni elaborate e note a piè di pagina. Se esporti in CSV, aggiungi alcuni metadati in puro testo, come le clausole di *copyright*, per rendere le importazioni automatiche più ostiche. Se i tuoi utenti devono fare un'ampia pulizia e un lavoro manuale prima di poter utilizzare i tuoi dati, potrebbero rinunciare.

## 5. Assicurati della presenza degli errori 404

Se devi proprio condividere i tuoi dati su portali open data, sfrutta il fatto che spesso contengono solo metadati e un collegamento alla tua fonte originale. Riorganizza frequentemente il tuo portale senza impostare reindirizzamenti appropriati e mostra agli utenti entusiasti una pagina di errore 404 (o meglio ancora, una pagina che spiega la nuova struttura e che i dati sono altrove).

Non c'è niente di meglio che deludere i potenziali utenti proprio dopo che stavano cominciando ad interessarsi.

### 5.5 Cambia i dati dopo la pubblicazione

Anche se non puoi spostare i dati, puoi modificarli allo stesso URL senza alcuna notifica o controllo di versione. Così, gli utenti che li scaricano e usano potrebbero ritrovarsi confusi a rieseguire i loro software. Un utente che deve continuamente riscaricare e riconvalidare i tuoi dati è un utente che probabilmente non tornerà più.

## 6. Frammenta i set di dati collegati

Hai un dataset che copre diversi anni? Perfetto. Dividilo in molti file individuali e non collegarli in modo chiaro. Trovare tutti i dataset e collegarli è un lavoro aggiuntivo per ogni utente che commette l'errore di cercare di usare i tuoi dati. Fortunatamente per te, i *data scientist* odiano lavorare piu del necessario.

Questo ha il vantaggio aggiuntivo di nascondere meglio il valore dei tuoi dati. Un potenziale utente che trova solo uno dei tuoi dataset potrebbe pensare che non sia recente o sufficientemente esteso e lasciarti in pace. Considera [questo insieme di dati con dati sul calcio dal 1960](https://www.kaggle.com/datasets/piterfm/football-soccer-uefa-euro-1960-2024). Non ti fa forse immediatamente venir voglia di scoprire come i dati cambiano nel tempo? Immagina quanto peggiore potrebbe essere se tu pubblicassi solo un file per ogni anno. Con un po' di fortuna, le persone potrebbero imbattersi solo nei dati del 1960, pensare che siano troppo vecchi e non aggiornati e disturberebbero qualcun altro.

Obiettivo aggiuntivo: distribuisci automaticamente i dati ai portali di dati, ma lascia la descrizione e il contesto solo sul tuo sito web per rendere i dati più difficili da utilizzare e farli apparire di qualità inferiore.

## Conclusione

Questi sono i principali consigli per far sì che nessuno si interessi ai tuoi dati aperti. La frustrazione per qualsiasi potenziale utente è assicurata. Ne manca qualcuno? Facci sapere di altri metodi che hai trovato per rendere l'uso dei dati aperti meno divertente.
