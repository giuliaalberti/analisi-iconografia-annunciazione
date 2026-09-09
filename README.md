# **ANALISI DELL'ICONOGRAFIA DELL'_ANNUNCIAZIONE_**

## Descrizione
Questo studio si basa su un’analisi esplorativa ed esplicativa di un dataset contenente un insieme di dati riguardanti 2444 opere d’arte figurativa realizzate in un arco temporale compreso tra il XIII e il XXI secolo. 
La nostra ricerca si è focalizzata sull’analisi del soggetto iconografico sacro dell’_Annunciazione_ concentrandosi su tre punti di ricerca principali:
1. In quale arco temporale si concentra la maggior presenza dell'iconografia dell'_Annunciazione_ e quali sono i principali stili artistici che caratterizzano la produzione.
2. Analizzare l'area dei quadri raffiguranti l'_Annunciazione_' nei diversi secoli. Osserviamo come si distruibuisce negli anni la grandezza dell'annunciazione.
3.  I luoghi con maggiore frequenza dell'_Annunciazione_.

### Quali sono i risultati?
1. **Frequenza e Distribuzione Cronologica dell'_Annunciazione_**: l'_Annunciazione_ è emersa come uno dei soggetti sacri più rappresentati nel dataset, con la sua massima concentrazione produttiva nel **sedicesimo secolo** (Cinquecento).
2. **Analisi ed Evoluzione Dimensionale dell'_Annunciazione_**: il sedicesimo secolo non solo detiene il primato per il numero di attestazioni, ma mostra anche la più elevata dispersione dimensionale delle opere, variando da formati contenuti (sotto i $20.000 \text{ cm}^2$) fino a una monumentale opera di oltre $90.000 \text{ cm}^2$).
3. **I Luoghi con Maggiore Frequenza dell'_Annunciazione_**: le **Gallerie dell'Accademia di Venezia** e la **Pinacoteca Nazionale di Bologna** sono i due musei che conservano il maggior numero di opere con soggetto iconografico dell'_Annunciazione_.

l progetto è stato realizzato nell'ambito del corso Digital Humanities e Data Management per I Beni Culturali - Informatica per I Beni Culturali 2025-2026 dell'Università di Bologna.

## Fonti di dati 
I dati in input sono costituiti da un file CSV di 229.3+ KB scaricato da una repository GitHub del corso Digital Humanities e Data Management per I Beni Culturali - Informatica per I Beni Culturali dell'anno 2025/2026 (https://raw.githubusercontent.com/dhdmch/2025-2026/refs/heads/main/data/lispod/data.csv).
I dati in output consistono in questo Jupyter Notebook, contenente testo e codice per l'analisi computazionale dei dati.
 Le variabili considerate sono:

| Variabile | Tipo |	Definizione | Esempio |
| :------- | :--- | :--------- | :------ |
|  id     |	str | link ID dell'opera | 	http://www.wikidata.org/entity/Q368788	 |
| titolo | str | titolo dell'opera | Pietà |
| artisti | str | nome dell'artista | Perugino |
| data_creazione | int | anno di creazione dell'opera | 1483 |
| generi | str | generi ai quali l'opera afferisce | arte religiosa |
| luoghi | str | luogo di conservazione dell'opera | Palazzo degli Uffizi|
| collezioni | str | collezione alla quale l'opera appartiene | Palazzo degli Uffizi|
| contenuti | str | contenuto dell'opera | Gesù; donna; Maria; uomo|
| movimenti | str | movimenti artistici ai quali l'opera afferisce | rinascimento italiano |
soggetti | str | soggetti rappresentati | Pietà |
| altezza | float | altezza dell'opera in cm | 168.0 |
| larghezza | float | larghezza dell'opera in cm | 176.0 |
| area opera | float | area dell'opera in cm² | 29568.00|

## Metodi e strumenti
Il progetto è stato elaborato all'interno dell'ambiente di calcolo Google Colab.
Per la manipolazione e l'interpretazione del dataset è stato impiegato il linguaggio Python, avvalendosi in particolare di tre librerie fondamentali per il Data Management umanistico:
`pandas` per la modellazione, la strutturazione e la pulizia dei dati tabellari;
`numpy` per la gestione avanzata dei valori mancanti (missing values) e le operazioni vettoriali;
`matplotlib` per la sintesi visiva e la generazione dei grafici a supporto delle ipotesi interpretative.

Le operazioni includono:
- Caricamento e ispezione dei dati (__pd.read_csv, .head(), .iloc(), .tail(), .shape(), .info(), .columns(), .duplicated(), .nunique(), .duplicated()__);
- Processamento dei dati (correzione manuale dei valori massimi e minimi di altezze e larghezze errate, conversione dei valori della colonna `data_creazione` in `Int64`, normalizzazione delle colonne con valori separati da `;`);
- Analisi esplicativa tramite aggregazioni (come __.value_counts()__) e visualizzazioni tramite grafici a dispersione, a barre e a torta;

## Responsabili
- Alberti Giulia
- Corrado Valentina

## Licenza
I dati di input e il codice di output (incluso in questo Notebook) sono rilasciati sotto licenza [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)
