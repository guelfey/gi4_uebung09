## Lader

ESTAB:
```
| Symbol | Typ   | Wert     |
|--------|-------|----------|
| libc   | modul | 80480000 |
| printf | near  | 80480000 |
| exit   | near  | 804800EA |
| malloc | near  | 8048013A |
| scanf  | near  | 8048023E |
| free   | near  | 8048045E |
| cntdwn | modul | 804804D6 |
| main   | near  | 804804D6 |
| msg    | BYTE  | 80480553 |
```

PROGADDR: 80480000
EXEXADDR: 804804D6

Speicher:
```
80480553 | .data von cntdwn
    ^    |
    |    |
804804D6 | .text von cntdwn
    ^    |
    |    |
80480000 | .text von libc
```

Adressen:
| Symbol | Wert |
|--------|------|
| libc   | 80480000 |
| printf | 80480000 |
| exit   | 804800EA |
| malloc | 8048013A |
| scanf  | 8048023E |
| free   | 8048045E |
| cntdwn | 804804D6 |
| main   | 804804D6 |
| msg    | 80480553 |
| schleife | 804804F4 |
| ende   | 80480523 |

## Eine Objektdatei

Eine Möglichkeit, um nur noch eine Objektdatei für das Programm zu benötigen,
wäre libc als dynamische Bibliothek zu benutzen. Dann wäre dieses Modul als
dynamische Bibliothek auf der Festplatte und der Lader würde beim Laden des
Programm sicher stellen, dass libc ebenfalls geladen ist. Dann müssten
Referenzen von Symbolen aus libc von cntdwn aus vom Lader ersetzt werden, denn
zur Zeit des Kompilierens bzw. Linkens wären die Adressen noch nicht bekannt.
Die Objektdatei ctndwn.o wäre im Prinzip vom Aufbau gleich, nur dass noch
Informationen über zur Ladezeit zu modifizierende Symbole hinzugefügt werden
müssten. Diese müssten dann auch in die ausführbare Datei übernommen werden.
