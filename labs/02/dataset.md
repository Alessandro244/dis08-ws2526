# Open Data (lab 02)

## Auswählen eines Datensets und Beschreibung dieses Datensets:
- **Titel:** World Population Dataset  

- **Quelle:** Von der Open Source Quelle Kaggle ([Link zum Datenset](https://www.kaggle.com/datasets/iamsouravbanerjee/world-population-dataset)). Autor des Datensatz ist Sourav Banerjee. Zuletzt geupdated wurde das Datenset vor 3 Jahren.  

- **Dateiformat:** Liegt als CSV-Datei vor und ist jederzeit kostenlos herunterladbar.   

- **Größe und Aufbau:** Das Datenset besteht aus diversen Spalten (insgesamt 17 Spalten und ca. 235 Zeilen), die Informationen über die Bevölkerungszahlen, Bevölkerungsdichte, Fläche und andere demografische Merkmale von Ländern und Gebieten beschreiben, wie zum Beispiel die Spalte 2020 Population die die Bevölkerung eines bestimmten Landes im Jahre 2020 aufzeigt oder die Spalte Area die die Fläche des Landes in Quadratkilometern wiedergibt. Die CSV-Datei hat eine Größe von 29.25 kB.  

- **Statistische Kennzahlen:** Diverse einfache statistische Kennzahlen sind den Spalten entnehmbar, wie zum Beispiel Minimum und Maximum Wert der Spalte 2022 Population mit einer Minimumbevölkerungsanzahl von 510 bis hin zu einer Maximumbevölerkungsanzahl der dort dargestellten Länder von ca. 1,43 Milliarden Menschen im Jahre 2020. Andere Spalten wie die eingetragenen Länder haben 234 einzigartige Werte (Länder).  
**Geografische und zeitliche Abdeckung:** Das Datenset enthält Bevölkerungszahlen über eine Großzahl an Ländern verteilt über jeden Kontinent in den Jahren 2000 - 2022.  

- **Lizenz:** Open Source Quelle auf Kaggle, keine genaue Lizenzbeschreibung ersichtlich, im Bereich Lizenz steht "Other (specified in description)", in der Beschreibung ist allerdings keine genaue Lizenz angegeben. Das Datenset ist downloadbar und einsehbar, da aber keine genaue Lizenz angegeben ist, würde ich im Falle der Verwendung erstmal den Autor (Sourav Banerjee) kontaktieren und nachfragen, inwiefern das Datenset frei verwendbar ist.   

## Erweitern des Datensets:  
Zur Erweitern habe ich mich für ein weiteres Datenset entschieden ([Link zum anderen Datenset](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india)). Dieses Datenset handelt von der gemessenen Luftqualität in verschiedenen Städte Indiens im Zeitraum von 2015 - 2020. Die Idee wäre dieses Datenset mit den Daten des ersten Datensets zu verwenden, um bestimmte Fragestellung oder Hypothesen zu prüfen. Eine mögliche Fragestellung wäre beispielsweise, ob die Dichte/ Menge der Population auf einer bestimmten Quadratmeterfläche (in diesem Fall die Bevölkerungsanzahl von Städten in Indien) mit der Qualität der Luft korreliert, insofern, dass eine hohe Bevölkerungsdichte zu einer verschlechterung der Luftqualität führen könnte. Man könnte sich auch den Verlauf der Luftqualität in den Jahren 2015 - 2020 mit verändernder Bevölkerungsdichte pro Stadt in Indien anschauen, um mögliche Muster oder Korrelationen zu finden. Die nächste Schritte, um solche Analysen mit den beiden Datensets zu ermöglichen, wäre sich die Spalten beider Datensets zu nehmen, die für die Analyse relevant sind und vom Zeitraum passend sind und diese zu importieren, um eventuelle Bereinigungen oder Transformationen vornehmen zu können. Anschließend könnte man einfache Analysen mit diesen Daten erstellen und die Ergebnisse in Form von Grafiken visualisieren. 

## Bewertung der Datensets nach den FAIR Prinzipien  
**Findable (Auffindbar):** Beide Datensets liefern genaue Informationen über Inhalt, Quelle, Erstellungsdatum und Dateiformat (F2).  

**Accessible (Zugänglich):** Beide Datensets können über Python Code abgerufen werden (A1). Beide Datensets sind jederzeit aufrufbar und downloadbar (A1.1). Beide Datensets benötigen die Erstellung eines kostenlosen Kaggle Accounts für den Download und unterstützten somit Protokoll Authentifizierung (A1.2).  

**Interoperable (Verarbeitbar):** Beide Datensets liegen im CSV-Format vor und sind damit gut verarbeitbar (I1).  

**Resuable (Wiederverwendbar):** Beide Datensets liefern genaue Informationen über Inhalt, Quelle, Erstellungsdatum und Dateiformat (R1). Nur eines der Datensets hat eine eindeutige Datenverarbeitungslizenz (R1.1 gilt also nur für eines der beiden Datensets). Herkunft und Entsteheung der Daten ist bei beiden Datensets angegeben (R1.2).  

### In Tabellenform (Überblick der erfüllten FAIR Prinzipien der beiden Datensets):
| Findable (Auffindbar)       | Accessible (Zugänglich)       | Interoperable (Verarbeitbar)       | Resuable (Wiederverwendbar):       |
|:-----------------------:|:-----------------------------:|:-----------------------------------:|:-------------------------------------:|
| F2                      | A1                            | I1                                  | R1                                    |
|                         | A1.1                          |                                     | R1.1                                  |
|                         | A1.2                          |                                     | R1.2                                  |

