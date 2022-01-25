# calcHourlyCAP
Berechnet die Hourly-CAP Preise von aWattar.de für heute und morgen

Im Gegensatz zu den Börsenpreisen des Tarifs HOURLY sind die Preise des CAP bzw. des "Sync-Bonus" nirgends aufgeführt. Dieses Python Programm berechnet anhand der verfügbaren Börsenpreise und des von aWattar verwendeten H0-Standardlastprofils den CAP-Preis und Sync-Bonus je kWh für jede Stunde.
Das H0-Profil wurde vom aWattar Support im Jan/22 als XLS zur Verfügung gestellt.
Um hier besser damit rechnen zu können wurde es umkonfiguriert und als CSV-Datei abgespeichert.

# Installation
Es wird Python3 benötigt und die requests Bibliothek.
Python3 kann bei Bedarf von [python.org](https://www.python.org/downloads/) runtergeladen und installiert werden.

Requests anschließend in einem Terminal/Command Line-Fenster mit `pip install requests` installieren.

Jetzt muss das `calcHourlyCAP`Programm von Github geladen werden. Falls noch nicht vorhanden, dazu das "git"-Tool installieren, siehe hier [install-git](https://github.com/git-guides/install-git).<br/>
Jetzt den Befehl `git clone https://github.com/joeyc64/calcHourlyCAP` ausführen.<br/>
Mit `cd calcHourlyCAP` in das Arbeitsverzeichnis wechseln.<br/>
Mit dem Befehl `python calcHourlyCAP.py` kann jetzt die Preisberechnung durchgeführt und angezeigt werden.
(Statt python evtl. python3 eingeben)

Beispiel Ausgabe:

```
Berechnung der HOURLY-CAP Preise von aWattar.de
2022-01-25 16 = 37.92, 38.22, -0.30
2022-01-25 17 = 43.61, 38.22, 0.00
2022-01-25 18 = 47.49, 38.22, 0.00
2022-01-25 19 = 44.48, 38.22, 0.00
2022-01-25 20 = 36.85, 38.22, -1.37
2022-01-25 21 = 31.54, 38.22, -6.68
2022-01-25 22 = 28.67, 38.22, -9.55
2022-01-25 23 = 25.61, 38.22, -12.61
2022-01-26 00 = 24.94, 28.73, -3.79
2022-01-26 01 = 25.27, 28.73, -3.46
2022-01-26 02 = 25.63, 28.73, -3.10
2022-01-26 03 = 24.98, 28.73, -3.75
2022-01-26 04 = 24.89, 28.73, -3.84
2022-01-26 05 = 25.6, 28.73, -3.13
2022-01-26 06 = 28.58, 28.73, -0.15
2022-01-26 07 = 35.09, 28.73, 0.00
2022-01-26 08 = 37.17, 28.73, 0.00
2022-01-26 09 = 37.21, 28.73, 0.00
2022-01-26 10 = 35.7, 28.73, 0.00
2022-01-26 11 = 33.64, 28.73, 0.00
2022-01-26 12 = 30.9, 28.73, 0.00
2022-01-26 13 = 28.74, 28.73, 0.00
2022-01-26 14 = 28.35, 28.73, -0.38
2022-01-26 15 = 28.17, 28.73, -0.56
2022-01-26 16 = 28.57, 28.73, -0.16
2022-01-26 17 = 31.9, 28.73, 0.00
2022-01-26 18 = 31.23, 28.73, 0.00
2022-01-26 19 = 26.71, 28.73, -2.02
2022-01-26 20 = 25.87, 28.73, -2.86
2022-01-26 21 = 20.39, 28.73, -8.34
2022-01-26 22 = 17.01, 28.73, -11.72
2022-01-26 23 = 14.56, 28.73, -14.17
```
Spalte 1 - Datum und Stunde<br/>
Spalte 2 - Börsenpreis inkl.MwSt.<br/>
Spalte 3 - Durchschnittlicher CAP-Preis des Tages<br/>
Spalte 4 - Sync-Bonus je Stunde /kWh<br/>

Beispiel:<br/>
Liegt der kWh-Preis bei Hourly-CAP z.B. bei 30.94Cent, dann reduziert sich der Preis am 22.01.25 ab 23 Uhr um 12.61 Cent auf 18.33 Cent je kWh.




  
