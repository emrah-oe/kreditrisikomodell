# Kreditrisiko-Modellierung

## Projektübersicht
Dieses Projekt widmet sich der **Modellierung von Kreditrisiken**, mit dem Ziel, die Wahrscheinlichkeit von Kreditausfällen präzise vorherzusagen. Durch den Einsatz von **Machine Learning** und einer umfassenden explorativen Datenanalyse (EDA) wurde ein leistungsfähiges Kreditrisikomodell entwickelt und bewertet.

Zusätzlich wurde mithilfe einer **Szenarioanalyse** die Modellrobustheit unter verschiedenen wirtschaftlichen Bedingungen getestet, um die Stabilität der Vorhersagen zu gewährleisten.

Die verwendeten Daten stammen aus dem [Statlog (German Credit Data)](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data) Dataset.

---

## Projektstruktur

### 1. Business Understanding
- **Ziel:** Vorhersage der Kreditausfallwahrscheinlichkeit zur Entwicklung eines robusten Kreditrisikomodells.
- **Nutzen:**
  - Reduktion von Kreditrisiken
  - Bessere Entscheidungsfindung
  - Erhöhung der Profitabilität
- **Stakeholder:** Banken, Risikomanager, Regulierungsbehörden.

### 2. Data Understanding
- Exploration des **German Credit Data-Datensatzes**.
- Identifikation und Analyse relevanter Features.
- Visualisierungen zur Erkennung von Mustern und Prüfung der Datenqualität.

### 3. Data Preparation
- **Kodierung** kategorialer Variablen und **Skalierung** numerischer Features.
- Feature Engineering (z. B. Belastungsfaktor).
- Auswahl von Features basierend auf Relevanzanalysen.

### 4. Modeling
- **Trainierte Modelle:**
  - Logistic Regression
  - Random Forest
  - XGBoost
- **Optimierung:** Hyperparameter-Tuning
- Bewertung anhand von Precision, Recall und Accuracy.

### 5. Evaluation
- **Vergleich der Modelle:** XGBoost liefert die beste Performance.
- Durchführung von Szenario-Analysen zur Bewertung der Modellrobustheit.
- Interpretation der Ergebnisse im Kontext des Kreditrisikomanagements.

---

## Datenquelle
Die verwendeten Daten stammen aus dem [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data).

**Beschreibung der Daten:**
- 1000 Beobachtungen
- 20 Features (numerische und kategoriale Merkmale)
- Zielvariable: Kreditwürdigkeit ("Bad Credit" = 0, "Good Credit" = 1)

---

## Ergebnisse im Überblick

### Wichtige Erkenntnisse:
- Die **monetären Faktoren** wie **monatliche Belastung** und **Kreditsumme** spielen eine zentrale Rolle.
- **Monatliche Belastung**: Höchster Einfluss auf die Kreditentscheidung: Eine hohe monatliche Belastung erhöht das Risiko.
- **Kreditsumme**: Kredite mit höherem Volumen werden häufiger als risikobehaftet eingestuft.
- **Alter**: Das Alter zeigt eine hohe Erklärungskraft für die Vorhersage. Jüngere Kreditnehmer weisen möglicherweise aufgrund geringerer finanzieller Stabilität ein höheres Risiko auf.


### Modellvergleich nach dem Tuning

| Modell                  | Klasse | Präzision | Recall | F1-Score |
|-------------------------|--------|-----------|--------|----------|
| **Logistische Regression** | 0      | 68%       | 39%    | 49%      |
|                         | 1      | 78%       | 92%    | 85%      |
| **Random Forest**        | 0      | 82%       | 39%    | 53%      |
|                         | 1      | 79%       | 96%    | 87%      |
| **XGBoost**              | 0      | 82%       | 53%    | 64%      |
|                         | 1      | 83%       | 95%    | 88%      |

**Gesamt-Accuracy der Modelle:**

| Modell                  | Gesamt-Accuracy |
|-------------------------|-----------------|
| Logistische Regression  | 77%            |
| Random Forest           | 80%            |
| XGBoost                 | 82%            |

---

## Szenarioanalyse
Um die Robustheit der Modelle zu testen, wurden verschiedene Szenarien simuliert:

- **Wirtschaftliches Wachstum:** Stabilere Einkommenssituationen und höhere Rückzahlungsraten führen zu einer verbesserten Kreditwürdigkeit.
- **Wirtschaftliche Unsicherheit:** Erhöhte monatliche Belastungen und sinkende Ersparnisse verschlechtern die Ausfallwahrscheinlichkeit deutlich.

---

## Fazit
Das entwickelte **XGBoost-Modell** hat sich als das leistungsstärkste Modell erwiesen und liefert die besten Ergebnisse hinsichtlich Präzision, Recall und Accuracy. Die Analyse zeigt, dass monetäre Faktoren wie die **monatliche Belastung** und die **Kreditsumme** maßgebliche Einflussgrößen für die Vorhersage von Kreditrisiken sind.

Durch die **Szenarioanalyse** konnte die Modellrobustheit unter verschiedenen wirtschaftlichen Bedingungen validiert werden, was die Zuverlässigkeit und praktische Anwendbarkeit des Modells untermauert.

---

## Technologien
- **Python**: pandas, numpy, scikit-learn, matplotlib, seaborn
- **Jupyter Notebook** für die interaktive Entwicklung

---

## Kontakt
Falls Fragen oder Anregungen bestehen, gerne via **GitHub** melden.
