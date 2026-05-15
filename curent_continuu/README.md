# Cateva notite:

## Declaratii de elemente:

### General:

Un_nume nod1 nod2 <nod3...> <MODEL_nume> <valoare1...>

### Rezistor liniar:

**Nu conteaza ordinea nodurilor!**

R_nume N1 N2 valoare

### Sursa independenta de tensiune:

**N4 -> V -> N3**

V_nume N3 N4 [DC] valoare

### Sursa independeneta de curent:

**N5 -> I -> N6

I_nume N5 N6 [DC] valoare

**Observatii:**

- Spice e case-insensitive.

- Factorii de scala sunt riscanti, pot induce in eroare.

- Trebuie pus .END la final.

- Este recomandatata utilizarea .PRINT si .DC.

*Cod care contine cat mai mult: circuit3.cir.*

