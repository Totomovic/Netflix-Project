# Netflix Movies Data Analysis 
Questo repository contiene un progetto di analisi esplorativa dei dati (EDA) sviluppato in Jupyter Notebook utilizzando Python. L’obiettivo del progetto è analizzare un dataset di film presenti su Netflix per estrarre insight significativi riguardanti i generi cinematografici, la popolarità, i voti medi e la distribuzione temporale delle uscite.

  Descrizione del dataset
Il dataset utilizzato viene caricato da un file CSV (mymoviedb.csv) e contiene informazioni dettagliate su numerosi film. Tra le variabili principali presenti nel dataset troviamo il titolo del film, i generi di appartenenza, la data di uscita, il voto medio assegnato dagli utenti, un indice di popolarità, la lingua originale, una descrizione testuale (overview) e l’URL del poster.
Prima di procedere con l’analisi vera e propria, il dataset viene ispezionato per comprenderne la struttura, i tipi di dato e l’eventuale presenza di valori mancanti o duplicati.

  Caricamento e analisi preliminare dei dati
Dopo aver importato le principali librerie Python per la manipolazione e la visualizzazione dei dati (NumPy, Pandas, Matplotlib e Seaborn), il dataset viene caricato all’interno del notebook. In questa fase vengono visualizzate le prime righe del dataframe e vengono analizzate le informazioni generali sulle colonne.
Questa analisi preliminare permette di individuare alcune criticità tipiche dei dataset reali, come colonne non necessarie all’analisi, formati di data non corretti e variabili che richiedono una trasformazione per poter essere analizzate correttamente.

  Pulizia e preprocessing dei dati
Una parte centrale del progetto è dedicata alla pulizia dei dati. La colonna relativa alla data di uscita (Release_Date) viene convertita in formato datetime e successivamente trasformata estraendo esclusivamente l’anno di uscita del film. Questa scelta semplifica l’analisi temporale e consente di studiare la distribuzione dei film nel tempo.
Successivamente vengono rimosse alcune colonne considerate non rilevanti ai fini dell’analisi, come la descrizione testuale del film, la lingua originale e l’URL del poster. La loro rimozione permette di rendere il dataset più snello e focalizzato sulle variabili di interesse.
Un altro passaggio importante riguarda la trasformazione della variabile Vote_Average. Il voto medio numerico viene convertito in una variabile categoriale, suddividendo i film in quattro classi (not popular, below average, average e popular) sulla base dei quartili della distribuzione. Questa operazione consente un’analisi più intuitiva della qualità percepita dei film.
I valori mancanti presenti nel dataset vengono successivamente rimossi per evitare distorsioni nelle analisi e nelle visualizzazioni.
Infine, viene gestita la colonna Genre. Poiché un film può appartenere a più generi, i valori vengono inizialmente separati in liste e il dataset viene poi “esploso” in modo che ogni riga rappresenti un singolo genere associato a un film. Questo passaggio è fondamentale per analizzare correttamente la distribuzione dei generi cinematografici.

  Analisi esplorativa dei dati
Una volta completata la fase di preprocessing, il progetto si concentra sull’analisi esplorativa dei dati attraverso statistiche descrittive e visualizzazioni grafiche.
Viene innanzitutto analizzata la distribuzione dei generi cinematografici. Dall’analisi emerge chiaramente che il genere Drama è il più rappresentato nel dataset, costituendo una percentuale significativa del catalogo Netflix.
Successivamente viene studiata la distribuzione delle categorie di voto. L’analisi mostra che una parte rilevante dei film rientra nella categoria “popular” e che, anche in questo caso, il genere Drama risulta essere dominante tra i titoli più apprezzati.
Il progetto prosegue individuando i film con i valori estremi di popolarità. Viene identificato il film con la popolarità più alta, che risulta essere Spider-Man: No Way Home, appartenente ai generi Action, Adventure e Science Fiction. Allo stesso modo, viene analizzato il film con la popolarità più bassa presente nel dataset.
Infine, viene analizzata la distribuzione dei film per anno di uscita. Attraverso un istogramma è possibile osservare come l’anno 2020 sia quello con il maggior numero di film prodotti, un risultato coerente con l’aumento di contenuti distribuiti sulle piattaforme di streaming in quel periodo.

  Conclusioni
Questi progetto mostra come un’analisi esplorativa ben strutturata permetta di estrarre informazioni rilevanti da un dataset reale. Attraverso operazioni di pulizia, trasformazione e visualizzazione dei dati è stato possibile individuare trend chiari nei generi cinematografici, nella distribuzione dei voti e nella produzione nel tempo.
Il notebook rappresenta una base solida per eventuali estensioni future, come l’implementazione di modelli di machine learning, sistemi di raccomandazione o analisi comparative tra diversi periodi temporali.
