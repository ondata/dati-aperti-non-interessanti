## Come assicurarsi che nessuno si interessi ai tuoi dati aperti

Articolo originariamente scritto da Philip Heltweg: [How to Make Sure No One Cares About Your Open Data](https://www.heltweg.org/posts/how-to-make-sure-no-one-cares-about-your-open-data/)

La traduzione italiana è a cura di [Antonio Vivace](https://github.com/avivace) e [Marco]() per [onData](https://www.ondata.it/).

---

Condividere i dati apertamente è un'impresa nobile. Può stimolare la ricerca, l'innovazione e la trasparenza. È anche davvero difficile e tedioso da fare, inoltre si perde il controllo - chissà cosa potrebbe fare la gente. Purtroppo, pubblicare dati aperti è spesso un obbligo legale. Quindi la soluzione migliore è pubblicare tecnicamente i dati aperti, ma assicurarsi che nessuno si interessi a essi. Basandomi sulla mia esperienza parlando con professionisti dei dati aperti, lavorando con varie fonti di dati aperti e insegnando agli studenti l'ingegneria dei dati, ecco un elenco di strategie comuni che ti aiuteranno a evitare qualsiasi attenzione da parte degli utenti effettivamente interessati a lavorare con i tuoi dati.

**1. Licenza oscura**

Confondi gli utenti rendendo difficile capire se i tuoi dati siano realmente aperti. Evita le licenze comuni con descrizioni chiare (come [quelle di OKFN](https://opendefinition.org/licenses/)) e nascondi la licenza effettiva (evita [identificatori SPDX](https://spdx.org/licenses/) nei metadati). Se possibile, non usare proprio alcuna licenza e fai riferimento solo a termini di utilizzo o documenti simili.

Se non puoi evitare una licenza standard, cerca di trovare una licenza nella tua lingua locale, che perlomeno scoraggerà gli utenti internazionali.

Punti bonus se pubblichi su Kaggle con la licenza "Altro (specificato nella descrizione)" e non scrivi nulla sulla licenza nella descrizione.

**2. Pubblica solo metadati**

Guarda questa mappa interattiva realizzata dall'agenzia nazionale francese per i dati sui trasporti: [https://transport.data.gouv.fr/?locale=en](https://transport.data.gouv.fr/?locale=en).

Oppure il progetto [Datenwaben](https://datenwaben.de/?city=vienna&page=cards) di [Thomas Tursics](https://toot.berlin/@tursics@toot.berlin).
Doesn’t that give you ideas for projects using the underlying data and make it sound interesting?

Terribile. Cerca di pubblicare solo i metadati minimi richiesti e scrivi descrizioni ovvie e noiose. Se puoi, evita di presentare esempi dei dati o di spiegare come usarli a tutti i costi. Ci sono così tanti set di dati generici là fuori che puoi nasconderti nella folla.


**2.5 Meno informazioni, meglio è**

Piattaforme come Kaggle mostrano automaticamente agli utenti un'anteprima dei dati. Vedi questo set di dati sull'individuazione delle frodi con carte di credito (con utili visualizzazioni): [https://www.kaggle.com/datasets/kartik2112/fraud-detection](https://www.kaggle.com/datasets/kartik2112/fraud-detection). 

Con anteprime dei dati e riassunti delle distribuzioni dei valori in ciascuna colonna, è davvero facile giudicare se i dati sono appropriati da utilizzare. 

Questo potrebbe semplificare l'esperienza per l'utente e sarà più probabile che li utilizzi effettivamente.

Evita di generare anteprime o riassunti dei tuoi dati.

**3. Rendili difficili da trovare**

Scegli nomi brevi e non descrittivi e descrizioni minimaliste per ostacolare l'indicizzazione da parte dei motori di ricerca. Inoltre, evita di distribuirli ampiamente. 

I portali di dati aperti come govdata.de spesso dispongono di funzioni di ricerca ben fatte o persino di API che possono essere utilizzate programmaticamente. Questo è ovviamente un disastro, quindi assicurati di creare un altro portale di dati che usi solo tu e pubblica i dati solo lì.

**4. Formati scomodi e rari**

Se pubblichi i tuoi dati in formati facilmente utilizzabili come CSV o JSON, devi accettare il rischio che gli utenti possano accedere ai tuoi dati liberamente. Puoi provare a pubblicarli in un formato che richiede software proprietario come XSL, ma anche quelli possono essere convertiti dalla maggior parte delle persone al giorno d'oggi. La cosa migliore sarebbe utilizzare un formato di file che non leggibile dalle macchine. 

I PDF sono una scelta popolare, specialmente se includi del testo di riempimento come intestazioni o piè di pagina oltre ai dati stessi.

**4.5 Esportazione "human-friendly"**

Quando esporti dati tabulari, considera di mantenere la struttura in un modo progettato originariamente per i lettori umani. Includi celle unite, intestazioni elaborate e note a piè di pagina. Se esporti in CSV, aggiungi alcuni metadati in puro testo, come le clausole di copyright, per rendere le importazioni automatiche più ostiche. Se i tuoi utenti devono affrontare un'ampia pulizia e un lavoro manuale prima di poter utilizzare i tuoi dati, potrebbero rinunciare.

**5. Errori 404**

Se devi condividere i set di dati su portali open data, sfrutta il fatto che spesso contengono solo metadati e un collegamento alla tua fonte originale. Riorganizza frequentemente il tuo portale senza reindirizzamenti e mostra agli utenti entusiasti una pagina di errore 404 (o meglio, una pagina che spiega la nuova struttura e che i dati sono altrove). Niente scoraggia più di un interesse iniziale infranto.

**5.5 Cambia i dati dopo la pubblicazione**

Anche senza spostare i dati, puoi modificarli allo stesso URL senza controllo delle versioni o notifiche. Così, gli utenti che li scaricano e usano potrebbero ritrovarsi confusi a rieseguire i loro software. Un utente che deve continuamente riscaricare e riconvalidare i tuoi dati è un utente che probabilmente non tornerà più.

**6. Frammenta i set di dati collegati**

Hai un dataset che copre diversi anni? Perfetto. Dividilo in molti file individuali e non collegarli in modo ovvio. Trovare tutti i dataset e collegarli è un lavoro aggiuntivo per ogni utente che commette l'errore di cercare di usare i tuoi dati. Fortunatamente per te, i data scientist odiano il lavoro aggiuntivo.

Questo ha il vantaggio aggiuntivo di nascondere meglio il valore dei tuoi dati. Un potenziale utente che trova solo uno dei tuoi dataset potrebbe pensare che non sia recente o sufficientemente esteso e lasciarti in pace. Considera questo dataset con dati calcistici dal 1960. Non ti fa forse immediatamente venir voglia di scoprire come i dati cambiano nel tempo? Immagina quanto peggiore potrebbe essere se tu pubblicassi solo un file per ogni anno. Con un po' di fortuna, chiunque si imbatterebbe solo nei dati del 1960, penserebbe che siano troppo vecchi e non aggiornati e disturberebbe qualcun altro.

Obiettivo a lungo termine: Diffondi i dati automaticamente sui portali di dati ma lascia descrizioni e contesto importante solo sul tuo sito web per rendere i dati più difficili da usare e apparentemente di qualità inferiore.

**Conclusione**

Questi sono i migliori consigli per assicurarti che nessuno si interessi ai tuoi dati aperti, garantiti per frustrare qualsiasi potenziale utente. Ne ho dimenticato qualcuno? Fammi sapere altri metodi che hai trovato per rendere noioso l'utilizzo dei dati aperti.
