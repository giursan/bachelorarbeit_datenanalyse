# Bachelorarbeit: Analyse der Einsatzfähigkeit von KI-erstellten Produktbeschreibungen im E-Commerce

Willkommen zu meinem GitHub-Repository, welches die Datenanalyse für meine Bachelorarbeit **"Analyse der Einsatzfähigkeit von KI-erstellten Produktbeschreibungen im E-Commerce"** enthält. In diesem Repository werden verschiedene Analysemethoden eingesetzt, um KI-generierte und menschlich erstellte Produktbeschreibungen zu vergleichen und zu analysieren.

## Inhaltsverzeichnis

1. [Projektübersicht](#projektübersicht)
2. [Repository-Struktur](#repository-struktur)
3. [Verwendete Daten](#verwendete-daten)
4. [Notebook-Gliederung](#notebook-gliederung)

## Projektübersicht

In dieser Analyse werden Produktbeschreibungen für vier ausgewählte Produkte (Laufschuh, Ecksofa, Parfüm, Trainingsjacke) mithilfe von KI generiert. Anschließend werden diese mit menschlich erstellten Produktbeschreibungen, sowohl mit als auch ohne KI-Vorschlag, verglichen. Hauptziel ist es, die Einsatzfähigkeit von KI-generierten Produktbeschreibungen im E-Commerce zu untersuchen.

Die Hauptfragestellungen betreffen:
- Textähnlichkeit (über Kosinus-Ähnlichkeit)
- Wortdiversität (Type-Token Ratio)
- Clustering der Produktbeschreibungen (mithilfe von k-Means und PCA)

## Repository-Struktur
```bash
bachelorarbeit_datenanalyse
├── data/                 # Ordner mit den generierten Produktbeschreibungen (CSV-Dateien)
│   ├── prod_1.csv           # Produktbeschreibungen für Laufschuh (250 Beschreibungen)
│   ├── prod_2.csv           # Produktbeschreibungen für Ecksofa (250 Beschreibungen)
│   ├── prod_3.csv           # Produktbeschreibungen für Parfüm (250 Beschreibungen)
│   └── prod_4.csv           # Produktbeschreibungen für Trainingsjacke (250 Beschreibungen)
├── notebook/            # Jupyter Notebooks für die Analyse
│   └── Experiment_Produktbeschreibungen.ipynb
└── README.md                # Dieses Dokument
```
## Verwendete Daten

* KI-generierte Produktbeschreibungen: Für jedes der vier Produkte wurden 250 Beschreibungen mithilfe der OpenAI API generiert.
* Menschliche Produktbeschreibungen ohne KI-Vorschlag: Beschreibungen, die von Umfrageteilnehmern ohne Einfluss eines KI-Vorschlags erstellt wurden.
* Menschliche Produktbeschreibungen mit KI-Vorschlag: Beschreibungen, die von Umfrageteilnehmern basierend auf einem KI-generierten Vorschlag erstellt wurden.

## Notebook-Gliederung

Das Jupyter Notebook Experiment_Produktbeschreibungen.ipynb ist wie folgt strukturiert:

1. **Import-Statements:** Herunterladen und Import der benötigten Python-Pakete.
2. **Generierung der KI-Produktbeschreibungen:** Generierung von 250 Produktbeschreibungen für jedes der vier Produkte mithilfe der OpenAI API.
3. **Menschlich generierte Produktbeschreibungen (ohne KI-Vorschlag):** Einlesen der Umfrageergebnisse ohne KI-Vorschlag.
4. **Menschlich generierte Produktbeschreibungen (mit KI-Vorschlag):** Einlesen der Umfrageergebnisse mit KI-Vorschlag.
5. **Statistiken der Produktbeschreibungen:** Vergleich grundlegender Textmerkmale wie Wortanzahl, Satzanzahl etc.
6. **Generierung von Embeddings:** Erstellung von Embeddings für alle Produktbeschreibungen über die OpenAI API.
7. **Analyse der Produktbeschreibungen:** Berechnung der Kosinus-Ähnlichkeit zwischen Produktbeschreibungen (Textähnlichkeit) und Berechnung der Type-Token Ratio (Wortdiversität) und K-Means-Clustering mit Visualisierung durch PCA (Clustering).
8. **Vergleichende Analyse:** Vergleich der Kosinus-Ähnlichkeit, Type-Token Ratio und Cluster zwischen den verschiedenen Beschreibungsarten.

