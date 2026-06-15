# NLP Project – Consumer Complaints Analysis

## Projektbeschreibung

Dieses Projekt beschäftigt sich mit der Analyse unstrukturierter Beschwerdetexte mithilfe von Natural Language Processing (NLP) in Python. Ziel ist es, häufige Themen und Problemfelder innerhalb großer Mengen von Verbraucherbeschwerden automatisch zu identifizieren und semantisch auszuwerten.

---

## Verwendeter Datensatz

Verwendet wurde der öffentliche Datensatz:

**Consumer Complaints Classification**

https://github.com/supreetkt/Consumer-Complaints-Classification

Der Originaldatensatz enthält mehrere Millionen Datensätze und ist aufgrund seiner Größe nicht Bestandteil dieses Repositorys.

Für die Analyse wurde eine Stichprobe von **5.000 Beschwerdetexten** verwendet. Dadurch bleibt das Projekt reproduzierbar und kann auch auf normalen Rechnern ohne hohe Hardwareanforderungen ausgeführt werden. Diese Reduzierung wurde im Notebook **00_create_data_csv.ipynb** gemacht. Einen weiteren Zweckn hat diese Datei nicht.

---

## Projektstruktur

```text
nlp_project_dlbdseda02_d/
│
├── data/│
├── notebooks/
├── processed_data/
├── results/
├── requirements.txt
├── environment.md
└── README.md
```

---

## Analyseablauf

Die Analyse wurde in fünf aufeinander aufbauende Jupyter Notebooks unterteilt.

### 01_data_loading.ipynb

* Laden des Datensatzes
* Untersuchung der Datenstruktur
* Identifikation der relevanten Textspalte
* Vereinheitlichung der Spaltennamen
* Entfernen fehlender Werte

### 02_preprocessing.ipynb

* Umwandlung in Kleinbuchstaben
* Entfernen von Sonderzeichen
* Entfernen von Zahlen
* Stopwortentfernung mit NLTK
* Lemmatization mit spaCy

### 03_vectorization.ipynb

* Vektorisierung mit Bag-of-Words (BoW)
* Vektorisierung mit TF-IDF
* Vergleich beider Verfahren

### 04_topic_modeling.ipynb

* Themenanalyse mit Latent Dirichlet Allocation (LDA)
* Themenanalyse mit Latent Semantic Analysis (LSA)
* Interpretation der identifizierten Themen

### 05_visualization.ipynb

* Erstellung einer Wordcloud
* Visualisierung der häufigsten Begriffe
* Zusammenfassung und Interpretation der Ergebnisse

---

## Installation

### Repository klonen

```bash
git clone https://github.com/ManuElito1725/nlp_project_dlbdseda02_d.git
cd nlp_project_dlbdseda02_d
```

### Virtuelle Umgebung erstellen (empfohlen)

```bash
conda create -n nlp_project python=3.11
conda activate nlp_project
```

### Benötigte Pakete installieren

```bash
pip install -r requirements.txt
```

### spaCy-Sprachmodell installieren

```bash
python -m spacy download en_core_web_sm
```

---

## Ausführung

Die Notebooks bauen aufeinander auf und müssen in der folgenden Reihenfolge ausgeführt werden:

1. `01_data_loading.ipynb`
2. `02_preprocessing.ipynb`
3. `03_vectorization.ipynb`
4. `04_topic_modeling.ipynb`
5. `05_visualization.ipynb`

Während der Verarbeitung werden Zwischenergebnisse im Ordner `processed_data/` gespeichert und von den nachfolgenden Notebooks verwendet.

---

## Verwendete Python-Bibliotheken

* pandas
* numpy
* nltk
* spaCy
* scikit-learn
* matplotlib
* wordcloud
* jupyterlab

---

## Ergebnisse

Zur Vektorisierung wurden die Verfahren:

* Bag-of-Words (BoW)
* TF-IDF

verwendet.

Für die Themenanalyse kamen die Verfahren:

* Latent Dirichlet Allocation (LDA)
* Latent Semantic Analysis (LSA)

zum Einsatz.

Die Analyse identifizierte insbesondere folgende Themenbereiche:

* Kreditberichte und Bonitätsinformationen
* Konten und Kontostände
* Zahlungsverhalten und verspätete Zahlungen
* Inkassoverfahren und Forderungen
* Streitfälle mit Auskunfteien

Die Ergebnisse wurden zusätzlich mithilfe von Wordclouds und Diagrammen visualisiert.

---

## Hinweise zur Reproduzierbarkeit

Das Projekt wurde mit Python 3.11 und Anaconda entwickelt.

Die ursprüngliche Version des Projekts verwendete den vollständigen Datensatz. Für eine bessere Reproduzierbarkeit wurde die Analyse auf eine Stichprobe von 5.000 Beschwerdetexten begrenzt.

Bei der Verwendung des vollständigen Datensatzes können längere Laufzeiten und ein höherer Speicherbedarf auftreten.

---

## Autor

Manuel Anders

Projekt im Rahmen eines Uni Moduls 
