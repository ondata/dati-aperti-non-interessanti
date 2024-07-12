## Come Assicurarsi che Nessuno Si Interesserà ai Tuoi Dati Aperti

Articolo originariamente scritto da Philip Heltweg: [How to Make Sure No One Cares About Your Open Data](https://www.heltweg.org/posts/how-to-make-sure-no-one-cares-about-your-open-data/)

Nota: Questo testo ironico fornisce consigli per pubblicare "open data" (dati aperti) in modo che nessuno li utilizzi.

Condividere i dati apertamente è un'impresa nobile. Può stimolare la ricerca, l'innovazione e la trasparenza. È anche davvero difficile e tedioso da fare, inoltre si perde il controllo - chissà cosa potrebbe fare la gente. Purtroppo, pubblicare dati aperti è spesso un obbligo legale. Quindi la soluzione migliore è pubblicare tecnicamente i dati aperti, ma assicurarsi che nessuno si interessi a essi. Basandomi sulla mia esperienza parlando con professionisti dei dati aperti, lavorando con varie fonti di dati aperti e insegnando agli studenti l'ingegneria dei dati, ecco un elenco di strategie comuni che ti aiuteranno a evitare qualsiasi attenzione da parte degli utenti effettivamente interessati a lavorare con i tuoi dati.

**1. Licenza oscura**

Confondi gli utenti rendendo difficile capire se i tuoi dati siano realmente open data. Evita le licenze comuni con descrizioni chiare (come quelle di OKFN) e nascondi la licenza effettiva (evita identificatori SPDX nei metadati). Se possibile, non usare alcuna licenza e fai riferimento solo a termini di utilizzo o documenti simili. 
**Bonus:** pubblica su Kaggle con la licenza "Altra (specificata nella descrizione)" senza specificarla poi nella descrizione.

**2. Pubblica solo metadati**

Guarda questa mappa interattiva realizzata dall'agenzia nazionale francese per i dati sui trasporti: [https://transport.data.gouv.fr/?locale=en](https://transport.data.gouv.fr/?locale=en). Sembra invitante, vero? 
**Sbagliato!** Pubblica solo i metadati minimi richiesti e scrivi descrizioni fattuali e noiose. Evita esempi di dati o del loro utilizzo. Mimetizzati tra i tanti set di dati generici.

**2.5 Meno informazioni, meglio è**

Piattaforme come Kaggle mostrano automaticamente agli utenti un'anteprima dei dati. Vedi questo set di dati sull'individuazione delle frodi con carte di credito (con utili visualizzazioni): [https://www.kaggle.com/datasets/kartik2112/fraud-detection](https://www.kaggle.com/datasets/kartik2112/fraud-detection). 
Questo è il tuo nemico! Evita anteprime o riassunti dei dati.

**3. Rendili difficili da trovare**

Scegli nomi brevi e non descrittivi e descrizioni minimaliste per ostacolare l'indicizzazione da parte dei motori di ricerca. Inoltre, evita di distribuirli ampiamente. Portali come govdata.de hanno ottime funzioni di ricerca e API. Un disastro! Crea un tuo portale dati personale per scoraggiare l'utilizzo.

**4. Formati scomodi e rari**

CSV o JSON sono facili da usare, quindi evita questi per scoraggiare l'accesso libero. Pubblica in formati che richiedono software costosi (come XSL), ma anche questi possono essere superati. Opzioni ideali? Formati non leggibili dalle macchine, come i PDF. Puoi anche includere testo di riempimento come intestazioni e piè di pagina.

**4.5 Esportazione "human-friendly"**

Per i dati tabulari, mantieni una struttura pensata per la lettura umana. Includi celle unite, intestazioni elaborate e note a piè di pagina. Se esportato in CSV, aggiungi testo in chiaro (come dichiarazioni di copyright) per complicare l'importazione automatica. Più gli utenti devono pulire i dati, più è probabile che rinuncino.

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
