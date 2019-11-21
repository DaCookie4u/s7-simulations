# S7-Anlagen-Simulationen

In diesem Repository gibt es einige virtuelle Modelle für die Siemens S7-1200 und S7-1500 Steuerung zum Download, welche zum Beispiel im Unterricht oder zu Übungszwecken verwendet werden können.

Die Modelle sind in SCL ausgeführt und, die Bausteine können einfach importiert und aufgerufen werden.

Zu jedem Modell gehört eine Visualisierung, für welche WinCC Advanced Runtime benötigt wird.

Der Simulations-FB muss als erster Baustein im Programmablauf aufgerufen werden (z.B. OB1 / NW1) und der erzeugte Instand-Datenbaustein, benötigt als Nummer die selbe Nummer wie die Anlage (z.B. 800_virt_Reaktor: %DB800).

Danach muss der Baustein mit den gewünschten Aus- und Eingängen beschaltet werden. In den meisten Fällen werden diese Byte- oder Wort-Weise übergeben. Einige Simulationen liefern auch Analogwerte zurück.

Eine Beschreibung der Ein- und Ausgänge ist bei den jeweiligen Simulationen zu finden.
