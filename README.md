# NLP Project – Consumer Complaints Analysis

Dieses Projekt beschäftigt sich mit der Analyse unstrukturierter Beschwerdetexte mithilfe von Natural Language Processing (NLP) in Python. Ziel ist es, häufige Themen und Problemfelder innerhalb großer Mengen von Verbraucherbeschwerden automatisch zu identifizieren und semantisch auszuwerten.

## Verwendeter Datensatz

Für das Projekt wurde der Datensatz **Consumer Complaints Classification** verwendet:

https://github.com/supreetkt/Consumer-Complaints-Classification

Die ursprüngliche CSV-Datei des Datensatzes ist aufgrund ihrer Größe nicht im Repository enthalten und muss separat heruntergeladen werden. Die Datei sollte anschließend im Ordner `data/` gespeichert werden und folgenden Namen haben: `consumer_complaints.csv`.

## Projektstruktur

```text
nlp_project_dlbdseda02_d/
│
├── data/
├── processed_data/
├── notebooks/
├── results/
├── requirements.txt
└── README.md
```

## Vorgehensweise

Die Analyse wurde schrittweise in mehreren Jupyter Notebooks durchgeführt:

### 01_data_loading.ipynb

* Laden und erste Analyse des Datensatzes
* Untersuchung der Datenstruktur
* Identifikation der relevanten Textspalte
* Entfernen fehlender Werte
* Vereinheitlichung der Spaltennamen

Am Ende wird ein bereinigter Datensatz exportiert.

### 02_preprocessing.ipynb

* Textvorverarbeitung (Preprocessing)
* Entfernen von Sonderzeichen und Stopwörtern
* Lemmatization mit spaCy
* Erstellung bereinigter NLP-Texte

Die erste bereinigte Datendatei ist aufgrund ihrer Größe ebenfalls nicht im Repository enthalten.

### 03_vectorization.ipynb

* Vektorisierung der Texte
* Bag-of-Words (BoW)
* TF-IDF
* Vergleich der Verfahren

### 04_topic_modeling.ipynb

* Themenanalyse mit:

  * Latent Dirichlet Allocation (LDA)
  * Latent Semantic Analysis (LSA)
* Extraktion häufiger Beschwerdethemen

### 05_visualization.ipynb

* Visualisierung der Ergebnisse
* Wordclouds
* Balkendiagramme
* Interpretation der Analyse

## Verwendete Bibliotheken

* pandas
* numpy
* nltk
* spaCy
* scikit-learn
* matplotlib
* wordcloud

## Hinweise zur Ausführung

Vor dem Start sollte eine virtuelle Umgebung (Conda) eingerichtet werden. Anschließend können die benötigten Abhängigkeiten mit folgendem Befehl installiert werden:

```bash
pip install -r requirements.txt
```

Zusätzlich muss das spaCy-Sprachmodell installiert werden:

```bash
python -m spacy download en_core_web_sm
```

Die Notebooks bauen inhaltlich aufeinander auf und sollten in der angegebenen Reihenfolge ausgeführt werden.
