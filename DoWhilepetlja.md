# Prezentacija: Petlja Do-While

## 1. Uvod

Dobrodošli na prezentaciju o petlji `do-while`!

Petlja `do-while` je kontrolna struktura u programiranju koja omogućuje izvršavanje određenog bloka koda sve dok je zadani uvjet istinit.

---

## 2. Opći oblik petlje `do-while`
do {
blok_naredbi;
} while (uvjet);

---

## 3. Osnovne karakteristike petlje `do-while`

- Petlja `do-while` prvo izvršava blok koda, a zatim provjerava uvjet.
- Ako je uvjet istinit, petlja se ponavlja, inače se petlja zaustavlja.
- Ova petlja osigurava da se blok koda izvrši barem jednom, čak i ako uvjet nije istinit na početku.
- Do while, naredba i izraz uvijet unutar zagrada iza koje slijedi točka zarez čini jednu cjelinu.
- Opći oblik ove petlje je:
    do
     naredba
    while (uvijet);
- U sklopu petlje može se nalaziti jedna ili blok naredbi.
- Petlja do while može se ugnježđivati jedna u drugu ili kombinirati dvije (ili više) različite petlje.
- Tok petlje do while je slijedeći:
  1. početak while petlje
  2. Istinit izraz ili uvijet se procjenjuje
  3. Ako je izraz istinit, program izvršava tijelo do-while petlje
  4. Ako je izraz neistinit, izvršava se program izvan while petlje.

---

## 4. Nekoliko prednosti petlje `do-while`

- Do-while petlja garantira izvršavanje petlje barem jednom, bez obzira na uvjet. To je korisno kada želite da određeni blok koda bude      izvršen prije nego što se provjeri uvjet.
- Do-while petlja je praktična kada želite obraditi korisnički unos prije nego što se provjeri uvjet petlje. Na taj način osiguravate da 
  se određeni unos ili operacija izvrše barem jednom.
- U programskom jeziku poput C, do-while petlju možete koristiti na primjeru korisničkog unosa, gdje želite da korisnik unese vrijednost 
  barem jednom prije provjere uvjeta petlje.
- Jednostavna sintaksa za osiguranje izvršavanja koda: Sintaksa petlje "do while" je prilično jednostavna i jasna. Ova jednostavnost čini kod čitljivijim i lakšim za održavanje.
 
---

## 5. Nekoliko nedostataka petlje `do-while`

- Do-while petlja zahtijeva inicijaliziju varijable prije same petlje, što dovodi do dodatnog koda izvan petlje i povećava kompleksnost programa.
- Unatoč tome što petlja prvo izvršava blok koda, postoji mogućnost da se blok izvrši barem jednom, čak i ako uvjet nije ispunjen.
- Manje je prikladna za korištenje u složenijim slučajevima, za razliku od petlje while.

---

## 6. Primjer korištenja petlje do while na konkretnom zadatku
Omogućiti korisniku unos dva realna broja. Osigurati da prvi bude manji od drugog.

#include <stdio.h>
int main(void)
{
  float a, b; 
  
  printf("Unesite prvi broj: ");
  scanf ("%f", &a);
  do {
     printf("Unesite drugi broj koji mora biti veci od prvog (%f): ", a);
     scanf("%f", &b);
} while (b <= a); 
return 0;
}
