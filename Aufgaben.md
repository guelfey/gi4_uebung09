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
