# S7-Anlagen-Simulationen

In diesem Repository gibt es einige virtuelle Modelle für die Siemens S7-1200 und S7-1500 Steuerung zum Download, welche zum Beispiel im Unterricht oder zu Übungszwecken verwendet werden können.

Die Modelle sind in SCL ausgeführt und die Bausteine können einfach importiert und aufgerufen werden. Wichtig ist beim Aufruf des Bausteins dem generierten Instanz-Datenbaustein die korrekte Nummer zuzuweisen. (z.B.: 800_virt_Reaktor benötigt %DB800)

Zu jedem Modell gehört eine Visualisierung, für welche WinCC Advanced Runtime benötigt wird. Die Visualiserung nutzt den Instanz-Datenbaustein zur Kommunikation mit der Simulation, daher benötigt dieser, wie oben beschrieben, die korrekte Nummer.

Danach muss der Baustein mit den zu nutzenden Aus- und Eingängen beschaltet werden. In den meisten Fällen werden diese Byte- oder Wort-Weise übergeben. Einige Simulationen liefern auch Analogwerte zurück.

Eine Beschreibung der Ein- und Ausgänge ist bei den jeweiligen Simulationen zu finden.

## Anleitung

Eine kurze Anleitung und eine fertige TIA-Bibliothek mit den Simulationsbausteinen gibt es hier: https://helix360.de/s7-simulationen/
