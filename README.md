Progetto di Machine Learning: Classificazione Automatica delle Notizie Vere e False

Descrizione del Progetto

Questo progetto ha come obiettivo lo sviluppo di un sistema di classificazione automatica delle notizie, utilizzando tecniche di machine learning per determinare se una notizia è vera o falsa. L'analisi è stata effettuata su tre diverse configurazioni di input: combinazione di titolo e testo, solo titolo e solo testo, per valutare quale approccio offra le migliori prestazioni in termini di accuratezza e precisione nella classificazione.

Dataset
Il dataset utilizzato è il "Fake and Real News Dataset" disponibile su Kaggle, composto da 72.134 articoli di notizie etichettati come veri o falsi. Ogni articolo include:

Title: il titolo della notizia
Text: il corpo del testo della notizia
Label: etichetta binaria (0 = vera, 1 = falsa)
Il dataset può essere scaricato dal seguente link: https://www.kaggle.com/datasets/saurabhshahane/fake-news-classification

Strumenti e Librerie Utilizzati
Manipolazione dei Dati e Visualizzazione: NumPy, Pandas, Matplotlib, Seaborn, WordCloud
Natural Language Processing (NLP): NLTK, FTFY, Regular Expressions (RE)
Machine Learning: Scikit-learn, XGBoost
Modelli: Logistic Regression, SVC, MultinomialNB, KNeighborsClassifier, RandomForestClassifier, AdaBoostClassifier, BaggingClassifier, ExtraTreesClassifier, GradientBoostingClassifier
Metriche di Valutazione: accuracy_score, precision_score
Pipeline e Riduzione della Dimensionalità: TruncatedSVD, Pipeline
Altre Librerie: Time, Collections (Counter)

Procedura del Progetto

STEP#1:Caricamento dei Dati
Caricamento e preparazione del dataset utilizzando Pandas e NumPy.

STEP#2:Analisi Esplorativa dei Dati (EDA)
Visualizzazione delle distribuzioni delle etichette e delle caratteristiche del testo per comprendere meglio la struttura del dataset.

STEP3#:Pulizia dei Dati
Rimozione di duplicati e righe vuote, gestione dei valori mancanti, e normalizzazione dei testi. Identificazione e analisi degli outliers nella lunghezza dei titoli e dei testi:
Outliers Titolo: 2.417
Outliers Testo: 3.524

STEP#4:Feature Engineering
Preprocessing dei testi, creazione di caratteristiche numeriche, vettorizzazione del testo usando TF-IDF, e scaling delle caratteristiche numeriche.

STEP#5:Suddivisione del Dataset
Divisione del dataset in set di addestramento (90%) e di test (10%).
Istanziamento e Addestramento dei Modelli

STEP#6:Utilizzo di vari modelli di machine learning e valutazione delle loro prestazioni.

STEP#7: Valutazione delle Prestazioni
Misurazione dell'accuratezza e della precisione dei modelli.
Confronto dei risultati tra le diverse configurazioni di input:
Titolo e Testo Combinati: Migliori prestazioni in termini di accuratezza e precisione, ma tempi di esecuzione più lunghi.
Solo Titolo: Configurazione più veloce ma con leggero calo di accuratezza.
Solo Testo: Prestazioni simili alla combinazione di titolo e testo con tempi di esecuzione comparabili.

Considerazioni Finali
I modelli avanzati come XGBoost, Random Forest e Bagging Classifier si sono dimostrati i più efficaci nella classificazione delle notizie. La scelta della configurazione di input dipende dalle esigenze specifiche in termini di accuratezza e velocità di esecuzione.
