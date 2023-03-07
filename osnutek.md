# Analiza uspešnosti študentov

V projektu bom analiziral podatke uspešnosti študentov iz dveh portugalskih šol. Predvsem me bo zanimalo kakšne so povezave med lastnostmi študentov, njihovimi okoliščinami in uspešnostjo na šoli.

Avtor: Samo Pungaršek Pritržnik

## Podatki

[Podatke](https://www.kaggle.com/datasets/devansodariya/student-performance-data) sem pridobil iz spletne strani [Kaggle](https://www.kaggle.com). Podatki so zbrani iz predmeta matematika.

Podatki so porazdeljeni na stolpce in vrstice. Stolpec predstavlja atribut za vse študente, vrstica pa študenta in njegove atribute. Imamo 32 stolpcev in 396 vrstic.

### Lastnosti podatkov

V podatkovni datoteki imamo 33 različnih atributov, kjer ima vsak atribut svojo lastnost.

Lastnosti so naslednje:
  1. school -> študentova šola (binearno: 'GP' - fakulteta Gabriel Pereira; 'MS' - Moushino da Silveira)
  2. sex -> študentov spol (binarno: 'F' - ženski; 'M' - moški)
  3. age -> študentova starost (numerično: od 15 pa do 22)
  4. address -> tip študentovega naslova (binarno: 'U' - mestni; 'R' - podeželjski)
  5. famsize -> velikost družine (binarno: 'LE3' - manj kot 3; 'GT3' - več kot 3)
  6. Pstatus -> ali starša živita skupaj (binarno: 'T' - živita skupaj; 'A' - živita narazen)
  7. Medu -> mamina stopnja izobrazbe (numeric: 0 - nič; 1 - primarna izobrazba do 4 razreda; 2 - končana primarna izobrazba; 3 - sekundarna izobrazba; 4 - višja izobrazba)
  8. Fedu -> očetova stopnja izobrazbe (numeric: 0 - nič; 1 - primarna izobrazba do 4 razreda; 2 - končana primarna izobrazba; 3 - sekundarna izobrazba; 4 - višja izobrazba)
  9. Mjob -> mamina služba (nominalno: 'teacher' - pedagogika; 'health' - delo v zdravstvu; 'services' - delo v javnem sektorju; 'at_home' - delo od doma; 'other' - drugo)
  10. Mjob -> očetova služba (nominalno: 'teacher' - pedagogika; 'health' - delo v zdravstvu; 'services' - delo v javnem sektorju; 'at_home' - delo od doma; 'other' - drugo)
  11. reason -> razlog izbire šole (nominalno: 'home' - bližina prebivališča; 'reputation' - ugled šole; 'course' - zanimivost predmetov; 'other' - drugo)
  12. guardian -> študentov skrbnik (nominalno: 'mother'; 'father'; 'other')
  13. traveltime -> čas potovanja od doma do šole (numerično: 1 - <15 min; 2 - 15 do 30 min; 3 - 30 min do 1 ure; 4 - >1 ura)
  14. studytime -> tedenski čas učenja (numerično: 1 - <2 uri; 2 - 2 do 5 ur; 3 - 5 do 10 ur; 4 - >10 ur)
  15. failures -> število preteklih neuspehov (numerično: n če 1<=n<3, če ne 4)
  16. schoolsup -> dodatna pomoč pri učenju (binarno: yes ali pa no)
  17. famsup -> družinska pomoč pri učenju (binarno: yes ali pa no)
  18. paid -> plačane inštrukcije v danem predmetu (binarno: yes ali pa no)
  19. activities -> izven šolske aktivnosti (binarno: yes ali pa no)
  20. nursery -> ali je študent obiskoval vrtec (binarno: yes ali pa no)
  21. higher -> ali si študent želi višjo izobrazbo (binarno: yes ali pa no)
  22. internet -> ali ima študent internetni dostop doma (binarno: yes ali pa no)
  23. romantic -> ali je v romantični zvezi (binarno: yes ali pa no)
  24. famrel -> kvaliteta družinskih odnosov (numeric: od 1 (zelo slabo) do 5 (zelo dobro))
  25. freetime -> prosti čas po šoli (numeric: od 1 (zelo malo) do 5 (zelo veliko))
  26. goout -> preživljeni čas s prijatelji (numeric: od 1 (zelo malo) do 5 (zelo veliko))
  27. Dalc -> uživanje alkohola med šolskimi dnevi (numeric: od 1 (zelo malo) do 5 (zelo veliko))
  28. Walc -> uživanje alkohola med vikendom (numeric: od 1 (zelo malo) do 5 (zelo veliko))
  29. health -> trenutni zdravstveno stanje (numeric: od 1 (zelo slabo) do 5 (zelo dobro))
  30. absences -> število šolskih izostankov (numeric: od 0 do 93)
  31. G1 -> ocena prvega semestra (numeric: od 0 do 20)
  32. G2 -> ocena drugega semestra (numeric: od 0 do 20)
  33. G3 -> končna ocena predmeta (numeric: od 0 do 20)
  
## Cilji

Pri projetku bom probal najti povezave med uspešnostjo končne ocene in lastnostmi študentov. 

Cilji so naslednji:
- Povezava med številom preteklih neuspehov in končno oceno predmeta.
- Povezava med tem ali je študent v romantični zvezi in številom preteklih neuspehov.
- Povezava med velikostjo družine in ali si študent želi višjo izobrazbo.
- Povezava med končno oceno predmeta in ali si študent želi višjo izobrazbo.
