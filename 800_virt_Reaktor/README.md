# Reaktionsprozess

![Bild der Visualisierung](800_virt_Reaktor.png)

## Belegungstabellen

Das an __#PAA_AB0__ zu übergebende Ausgangsbyte ist wie folgt belegt:

Bit | Betriebsmittel | Beschreibung
--- | -------------- | ------------
  0 |             Y1 | Zulaufventil 1
  1 |             Y2 | Zulaufventil 2
  2 |             Y3 | Ablassventil
  3 |             H1 | Heizung
  4 |             M1 | Rührmotor

Das an __#PAE_EB0__ ausgegebene Eingangsbyte liefert folgende Signale:

Bit | Betriebsmittel | Beschreibung
--- | -------------- | ------------
  0 |             S1 | Taster S1 (NO)
  1 |             B1 | Niveauschalter unten (NO)
  2 |             B2 | Niveauschalter mitte (NO)
  3 |             B3 | Niveauschalter oben (NO)
  4 |             B4 | Temperatursensor (NO)
  5 |             S2 | Taster S2 (NO)
  6 |             S3 | Taster S3 (NC)

Der Ausgang __#PAE_EW64__ liefert den aktuellen Füllstand als Analogwert, wobei 0V bis 10V einen Füllstand von 0% bis 100% entsprechen.

## Beispielaufgabe

In einem Behälter werden zwei unterschiedliche chemische Ausgangsstoffe zusammengeführt, bis zu einer vorgegebenen Temperatur erwärmt und danach noch eine bestimmte Zeit gerührt.

Nach Betätigung des Tasters S1 wird, sofern der Behälter leer und das Ventil Y3 geschlossen ist, das Vorlaufventil Y1 geöffnet, bis der Niveauschalter B2 anspricht.

Danach schaltet das Rührwerk M1 ein und das Ventil Y2 wird geöffnet.

Spricht der Niveuaschalter B3 an, schliesst das Ventil Y2 wieder und die Heizung H1 schaltet ein.

Meldet der Temperatursensor B4 das Erreichen der vorgegebenen Temperatur, wird die Heizung H1 abgeschaltet und für 10 Sekungen weiter gemischt.

Danach schaltet das Rührwerk ab und das Ventil Y3 öffnet.

Meldet der Niveauschalter B1, dass der Behälter leer ist, wird das Ventil Y3 wieder geschlossen und der Prozessablauf kann wiederholt werden.

Mit dem Taster S2 kann die Ablaufkette in zurückgesetzt werden.

Mit dem Taster S3 kann der Prozess vorzeitig beendet werden. Dabei werden alle Aktoren abgeschaltet und das Ventil Y3 geöffnet, bis der Niveauschalter B1 meldet, dass der Behälter leer ist. Danach kann der Prozessablauf erneut gestartet werden.
