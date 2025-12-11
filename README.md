# Analisi dei Dati Cinematografici: Film Horror

## DOI
[https://doi.org/10.5281/zenodo.17896900](https://doi.org/10.5281/zenodo.17896900)

## Descrizione
Questo progetto consiste in un'analisi esplorativa ed esplicativa di un dataset contenente dati cinematografici relativi al genere horror prodotti dal 1950 a oggi. L'analisi è focalizzata sulla verifica di tendenze percepite nel dominio, in particolare l'aumento della produzione di film horror e la relazione tra costi di produzione (budget), guadagni (revenue) e Ritorno sull'Investimento (ROI) nel tempo.

## Quali sono i risultati?
I risultati principali dell'analisi computazionale (contenuti nel Jupyter Notebook) includono:

- La verifica di una crescita esponenziale nella produzione di film horror nel tempo;
- La correzione e bonifica di valori anomali (es. runtime espressi in secondi, budget e revenue pari a zero o impossibili);
- L'identificazione e la visualizzazione del ROI medio per decade, dimostrando come il modello di business dell'horror sia cambiato: da scommesse ad alto rischio negli anni '70 a un genere a basso budget e alto rendimento nell'ultimo decennio;

## Fonte dei dati
I dati in input sono costituiti da un file CSV contenente informazioni dettagliate su film horror. Le variabili considerate sono:

| Variabile | Tipo |	Definizione | Esempio |
| :------- | :--- | :--------- | :------ |
| id       |	int | ID del film | 	4488 |
| original_title | str | Titolo originario del film | Friday the 13th |
| title |	str |	Titolo del film |	Friday the 13th |
| original_language |	str |	Lingua originale del film |	en |
| overview | str | Descrizione del film |	Camp counselors are stalked... |
| tagline |	str | Slogan del film | They were warned... |
| release_date | date |	Data di uscita del film | 1980-05-09 |
| poster_path |	str |	Parte di URL del poster del film. Per l'URL completo bisogna concatenare "https://www.themoviedb.org/t/p/w1280" con il valore della cella |	/HzrPn1gEHWixfMOvOehOTlHROo.jpg |
| popularity | float | Punteggio di popolarità calcolato sulla base di molte altre variabili |	58.957 |
| vote_count | int | Voti totali dati al film | 2289 |
| vote_average | float | Media dei voti dati al film | 6.4 |
| budget | int | Budget del film, calcolato in dollari | 550000 |
| revenue |	int |	Entrate del film, calcolate in dollari | 59754601 |
| runtime |	int |	Durata del film, calcolata in minuti | 95 |
| status | str |	Stato del film | Released |
| genre_names |	str |	Lista di generi del film, ognuno separato dalla virgola `,` | Horror, Thriller |
| collection | int | ID della collezione | 9735 |
| collection_name |	str |	Nome della collezione |	Friday the 13th Collection |

I dati originali sono stati estratti da The Movie Database (tmdb API) e sono stati recuperati dalla repository GitHub di TidyTuesday come file CSV.

Link al dataset: [https://github.com/rfordatascience/tidytuesday/tree/main/data/2022/2022-11-01](https://github.com/rfordatascience/tidytuesday/tree/main/data/2022/2022-11-01)

## Metodi e strumenti
Il progetto è stato sviluppato in un ambiente Google Colab utilizzando il linguaggio di programmazione Python. Lo strumento principale utilizzato per la manipolazione, l'analisi e la visualizzazione dei dati è la libreria Pandas.

Le operazioni includono:

- Caricamento e ispezione dei dati (_pd.read_csv_, _df.info()_, _df.describe()_);
- Bonifica e normalizzazione dei dati (conversione delle date in tipo _datetime_, correzione manuale di outlier come la runtime errata);
- Creazione di nuove variabili calcolate (_year_, _budget_m_, _revenue_m_, _roi_, _decade_);
- Analisi esplorativa tramite aggregazioni (_value_counts()_, _groupby()_) e visualizzazioni tramite grafici a linea (_plot.line()_) e a barre (_plot.barh()_);
- Analisi esplicativa focalizzata sul ROI per decennio per supportare la narrativa sull'evoluzione del genere horror.

## Responsabili
- Barzaghi, Sebastian - [https://orcid.org/0000-0002-0799-1527](https://orcid.org/0000-0002-0799-1527)

## Licenza
I dati di input e il codice di output (incluso in questo Notebook) sono rilasciati sotto licenza [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).
