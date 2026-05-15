# Simulare circuite de curent continuu:

## Declaratii de elemente:

### General:

Un_nume nod1 nod2 <nod3...> <MODEL_nume> <valoare1...>

### Rezistor liniar:

**Nu conteaza ordinea nodurilor!**

*Declaratie:* R_nume N1 N2 valoare

### Sursa independenta de tensiune:

**N4 -> simbol V -> N3**

*Declaratie:* V_nume N3 N4 valoare

### Sursa independeneta de curent:

**N5 -> simbol I -> N6**

*Declaratie:* I_nume N5 N6 valoare

### Sursa de tensiune comandata in tensiune:

*Ecuatie:* E = A * U, A = factor de amplificare.

**N1 -> simbol E -> N2**

**N3 -> sageata U -> N4**

*Declaratie:* E_nume N2 N1 N3 N4 factor

### Sursa de tensiune comandata in curent:

*Ecuatie:* E = R * I

**N1 -> simbol E -> N2**

Se adauga V_comanda cu tensiune 0V cu simbol in sens contrar fata de I (nu stiu de ce invers!).

**-> I -> | <- simbol V <-**

*Declaratie:* H_nume N2 N1 V_comanda rezistenta

### Sursa de curent comandata in tensiune:

*Ecuatie:* I = G * U

**N1 -> simbol I -> N2**

**N3 -> sageata U -> N4**

*Declaratie:* G_nume N1 N2 N3 N4 conductanta

### Sursa de curent comandata in curent:

*Ecuatie:* Ig = B * I, B = factor de amplificare.

Se adauga V_comanda cu tensiune 0V cu simbol in sens contrar data curent I (nu stiu de ce invers!).

**N+ -> simbol I -> N-**

**-> I -> | <- simbol V <-**

*Declaratie:* F_nume N+ N- V_comanda factor

-------------------------------------------------------------------------------

*Observatii:*

- Spice e case-insensitive.

- Factorii de scala sunt riscanti, pot induce in eroare.

- Trebuie pus .END la final.

- Este recomandatata utilizarea .PRINT si .DC.

