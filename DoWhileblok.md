# Prezentacija: Petlja Do-While

## 1. Uvod

Dobrodošli na prezentaciju o petlji `do-while`!

Petlja `do-while` je kontrolna struktura u programiranju koja omogućuje izvršavanje određenog bloka koda sve dok je zadani uvjet istinit.

---

## 2. Osnovne karakteristike petlje `do-while`

- Petlja `do-while` prvo izvršava blok koda, a zatim provjerava uvjet.
- Ako je uvjet istinit, petlja se ponavlja, inače se petlja zaustavlja.
- Ova petlja osigurava da se blok koda izvrši barem jednom, čak i ako uvjet nije istinit na početku.
- Do while, naredba i izraz uvijet unutar zagrada iza koje slijedi točka zarez čini jednu cjelinu.
- U sklopu petlje može se nalaziti jedna ili blok naredbi.

---

## 3. Nekoliko prednosti petlje `do-while`

- Do-while petlja garantira izvršavanje petlje barem jednom, bez obzira na uvjet. To je korisno kada želite da određeni blok koda bude      izvršen prije nego što se provjeri uvjet.
- Do-while petlja je praktična kada želite obraditi korisnički unos prije nego što se provjeri uvjet petlje. Na taj način osiguravate da 
  se određeni unos ili operacija izvrše barem jednom.
- U programskom jeziku poput C, do-while petlju možete koristiti na primjeru korisničkog unosa, gdje želite da korisnik unese vrijednost 
  barem jednom prije provjere uvjeta petlje.

---
## 4. Primjer korištenja petlje do while na konkretnom zadatku
Omogućiti korisniku unos cijelog broja. Osigurati da bude u intervalu [10, 50].

 #include <stdio.h>
int main(void)
{
  int b; 
  do {
    scanf("%d", &b); 
  } while (b < 10 || b > 50);
  scanf("%d", &b);
  while (b < 10 || b > 50)
    scanf("%d", &b);
  scanf("%d", &b);
  for ( ; b < 10 || b > 50; )
   scanf("%d", &b);
return 0;
}

