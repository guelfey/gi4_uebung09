# Übung 9: Objektdateien / Binder / Lader

Die Objektdatei aus der vorherigen Übung soll nun zu einem Programm gebunden werden. Nehmen Sie dazu an, dass sich im Modul `libc` folgende Funktionen mit den angegebenen Längen in der angegebenen Reihenfolge befinden:

* `printf`: 234 Bytes
* `exit`: 80 Bytes
* `malloc`: 260 Bytes
* `scanf`: 544 Bytes
* `free`: 120 Bytes


1. Erzeugen Sie zunächst die Datensätze vom Typ H, S, D, R und E für das Modul `libc`. Nehmen Sie dazu an, dass das Modul nur die genannten Funktionen enthält.
2. Die beiden Objektdateien (`cntdwn.o` und `libc.o`) sollen nun durch einen bindenden Lader in den Arbeitsspeicher geladen werden. Führen Sie manuell die erste und zweite Phase des Laders aus und geben Sie die `ESTAB` sowie `PROGADDR` und `EXECADDR` nach der Ausführung an. Bei Linux wird standardmäßig an die Adresse `0x08048000` geladen. Zeichnen Sie die Aufteilung des Speichers und geben Sie die endgültigen Adressen der relokierten Adressreferenzen an.
3. Die Objekte sollen nun anders gebunden werde. Das Programm soll dabei nur noch aus einer Objektdatei `cntdwn.o` bestehen, die keine überflüssigen Symbole enthält. Geben Sie die notwendigen Schritte an und skizzieren Sie den Aufbau der Objektdatei.
