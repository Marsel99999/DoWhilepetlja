# Prezentacija: Petlja Do-While

## 1. Uvod

Dobrodošli na prezentaciju o petlji `do-while`!

Petlja `do-while` je kontrolna struktura u programiranju koja omogućuje izvršavanje određenog bloka koda sve dok je zadani uvjet istinit.

---

## 2. Opći oblik petlje `do-while`
do {
    blok_naredbi;
} while(uvjet);

- do – početak izvršavanja naredbe (ulazak u blok)
- naredba – dio koda koji će obavljati operacije nad nekom prije zadanom vrijednosti
- while(uvjet) – izvršavanje naredbe dok je uvjet istinit (izlazak iz bloka)

---

## 3. Osnovne karakteristike petlje `do-while`

- Naziva se još petlja kontrolirana izlazom (engl. exit-condition loop).
- Petlja `do-while` prvo izvršava blok koda, a zatim provjerava uvjet.
- Ako je uvjet istinit, petlja se ponavlja, inače se petlja zaustavlja.
- Ova petlja osigurava da se blok koda izvrši barem jednom, čak i ako uvjet nije istinit na početku.
- Do while, naredba i izraz uvjet unutar zagrada iza koje slijedi točka zarez čini jednu cjelinu.
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
- Sintaksa petlje "do while" je prilično jednostavna i jasna. Ova jednostavnost čini kod čitljivijim i lakšim za održavanje.
- Za razliku od petlje "while" koja prvo provjerava uvjet pa tek onda izvršava blok koda, petlja "do while" izvršava blok koda prvo, a zatim provjerava uvjet. Ova karakteristika može biti korisna u situacijama kada je potrebno izvršiti određene operacije prije nego što se provjeri uvjet za nastavak petlje.
- Koristi se za validaciju unosa podataka: Petlja do-while je korisna kada trebate provjeriti ispravnost unosa korisnika. Na primjer, ako korisnik unosi broj koji mora biti u određenom rasponu, petlja do-while omogućuje ponovno traženje unosa sve dok korisnik ne unese ispravan podatak.
 
---

## 5. Nekoliko nedostataka petlje `do-while`

- Do-while petlja zahtijeva inicijaliziju varijable prije same petlje, što dovodi do dodatnog koda izvan petlje i povećava kompleksnost programa.
- Unatoč tome što petlja prvo izvršava blok koda, postoji mogućnost da se blok izvrši barem jednom, čak i ako uvjet nije ispunjen.
- Manje je prikladna za korištenje u složenijim slučajevima, za razliku od petlje while.
- Postoji mogućnost beskonačne petlje, ako se uvjet izlaska iz petlje pogrešno postavi, petlja će se neprekidno izvršavati.
- Ponekad je potrebno koristiti dodatne varijable kako bi se postavio uvjet izlaska iz petlje što može povećati kompleksnost koda.

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

}

## 7. Upotreba u praksi
Do while petlja se često koristi za rad s korisničkim unosima, validaciju podataka, obradu liste elemenata ili bilo koje situacije gdje je potrebno barem jednom izvršiti određeni blok koda prije provjere uvjeta.

---

## 8. Provjera uvjeta u petlji do-while

U petlji `do-while`, uvjet se provjerava na kraju svakog prolaza kroz petlju. To znači da se blok koda unutar petlje uvijek izvršava barem jednom, bez obzira na to je li uvjet ispunjen ili ne. Nakon izvršavanja bloka koda, uvjet se provjerava. Ako je uvjet istinit, petlja se ponavlja; inače, petlja se zaustavlja.

## Provjera uvjeta na početku petlje

U petlji s provjerom uvjeta na početku, uvjet se provjerava prije izvršavanja bloka koda. Ako uvjet nije ispunjen na početku, blok koda se uopće ne izvršava. Ova vrsta petlje je klasična `while` petlja.

Primjer:

```c
int broj = 0;
while (broj < 5) {
printf("Broj: %d\n", broj);
broj++;
}

## 9.Razlika između do-while petlje i while petlje
Razlika između do-while petlje i while petlje leži u načinu provjere uvjeta za ponavljanje bloka koda.

Do-while petlja:
-Prvo izvršava blok koda, a zatim provjerava uvjet.
-Osigurava da se blok koda izvrši barem jednom, čak i ako uvjet nije ispunjen na početku.
-Koristi se kada želimo garantirati barem jedno izvršavanje bloka koda prije provjere uvjeta za ponavljanje petlje.

While petlja:
-Provjerava uvjet na početku petlje prije izvršavanja bloka koda.        
-Može se preskočiti izvršavanje bloka koda ako uvjet nije ispunjen na početku.
-Koristi se kada želimo provjeriti uvjet prije izvršavanja bloka koda.
