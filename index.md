Język KMMszarp jest czysto alfanumerycznym języka programowania wysokiego poziomu. 
Wykorzystuje on typowanie silne oraz statyczne. Jego główne założenie to czytelność kodu dla zwykłego użytkownika. 
Jest językiem ogólnego przeznaczenia. Obsługuje on polskie znaki diakrytyczne. Jest bezkontekstowy.

## Zmienne

### Deklaracja zmiennej prostej
```
zmienna [typ zmiennej] NAZWA_ZMIENNEJ
```

### Deklaracja zmiennej prostej z przypisaniem wartości
```
zmienna [typ zmiennej] NAZWA_ZMIENNEJ to wartość
```

### Deklaracja tablicy
```
tablica [typ zmiennej] NAZWA_TABLICY o długości DŁUGOŚĆ
```
### Deklaracja tablicy z przypisaniem wartości
```
tablica [typ zmiennej] NAZWA_TABLICY to wartość i wartość i ...
```
Jeśli podczas deklaracji tablicy zmienne są od razu przypisywanie to nie podaje się rozmiaru tablicy – jest ona obliczana na podstawie liczby elementów

### Dostęp do elementów tablicy
```
weź NAZWA_ZMIENNEJ | LICZBA element NAZWA TABLICY
```
### Przypisanie elementów tablicy
```
włóż NAZWA_ZMIENNEJ na NAZWA_ZMIENNEJ | LICZBA miejsce NAZWA_TABLICY
```

## Typy
```liczba``` - liczba całkowita ze znakiem  
```napis``` - ciąg alfanumeryczny  
```prawdziwość``` - typ logiczny  
```nicość``` - typ _void_  

## Operatory
```to``` - przypisanie  

## Operatory matematyczne
```dodać``` - dodawanie  
```odjąć``` - odejmowanie  
```razy``` - mnożenie  
```przez``` - dzielenie  
```moduł``` - modulo  

## Wartości logiczne
```prawda``` - logiczna prawda  
```kłamstwo``` - logiczny fałsz  

## Operatory logiczne
```mniejsze niż``` - równoważne matematycznemu operatorowi mniejszości  
```większe niż``` - równoważne matematycznemu operatorowi większości  
```równe``` - równoważne matematycznemu operatorowi równości  
```nierówne``` - równoważne matematycznemu operatorowi nierówności  
```oraz``` - równoważne logicznej koniunkcji  
```lub``` - równoważne logicznej alternatywnie  

### Równoważne operatory negacji

- ```zaneguj```
- ```nie```
- ```przemień```

## Nawiasy
```począteknawiasu  koniecnawiasu```

## Pętle

### Pętla zakres
```
pętla zakres [deklaracja zmiennej] [NAZWA_ZMIENNEJ] od [NAZWA_ZMIENNEJ] do [NAZWA_ZMIENNEJ] początekpętli

koniecpętli
```

### Pętla podczas
```
pętla podczas [warunek] początekpętli
	
koniecpętli
```

## Instrukcje warunkowe

### Jeżeli
```
jeżeli [warunek] wtedy początekjeżeli

koniecjeżeli 
```

### Jeżeli, w przeciwnym wypadku
```
jeżeli [warunek] wtedy początekjeżeli

koniecjeżeli 
w przeciwnym wypadku [warunek] początek jeżeli

koniecjeżeli
```

## Funkcje
### Deklaracja funkcji z parametrami
```
czynność [NAZWA_CZYNNOŚCI]
parametry [zmienna typzmiennej NAZWA1 i zmienna typzmiennej NAZWA2 i …]
zwraca [typzmiennej] początekczynności

koniecczynności
```

### Deklaracja funkcji bez parametrów
```
czynność [NAZWA_CZYNNOŚCI]
zwraca [typzmiennej] początekczynności

koniecczynności
```

### Wywołanie funkcji
```
wywołaj [NAZWA_CZYNNOŚCI] NAZWA1 i NAZWA 2 i ...
```

## Przykładowy kod

### Pętla zakres
```
pętla zakres zmienna liczba I od 0 do 10 początekpętli
	wywołaj napisz początekcudzysłowu Przykładowy tekst konieccudzysłowu
koniecpętli
```

### Pętla podczas oraz instrukcja warunkowa
```
zmienna liczba TEST to 10
pętla podczas TEST jest mniejsze niż 12 początekpętli
jeżeli TEST moduł 2 równe 0 wtedy początekjeżeli
	   wywołaj napisz początekcudzysłowu liczba jest podzielna przez 2 konieccudzysłowu
koniecjeżeli 
TEST to TEST odjąć 1
    
    koniecjeżeli
    
    TEST to TEST dodaj 1
koniecpętli
```

### Deklaracja i przypisanie zmiennych
```
zmienna liczba A to 10
zmienna liczba B to 5

zmienna liczba WYNIKDODAWANIA to A dodać B
zmienna liczba WYNIKODEJMOWANIA to A odjąć B
zmienna liczba WYNIKMNOŻENIA to A razy B
zmienna liczba WYNIKDZIELENIA to A przez B

zmienna prawdziwość PRAWDZIWAZMIENNA to przemień kłamstwo
PRAWDZIWAZMIENNA to zaneguj PRAWDZIWAZMIENNA

zmienna liczba C
liczba A to 15
liczba B to 20
liczba C to 30
```

### Funkcja
```
czynność dodawanie 
parametry zmienna liczba SKŁADNIK1 i zmienna liczba SKŁADNIK2 
zwraca liczba początekczynności
	zwróć SKŁADNIK1 dodaj SKŁADNIK2
koniecczynności
```

### Sortownie szybkie
```
czynność QUICKSORT
parametry tablica liczba TAB i zmienna liczba L i zmienna liczba R
zwraca nicość początek czynności
	jeżeli L mniejsze niż P wtedy początekjeżeli
		zmienna liczba I to wywołaj PODZIELTABLICE TAB i L i R 
		wywołaj QUICKSORT TAB i L i I odjąć 1
		wywołaj QUICKSORT TAB i I dodać 1 i R
	koniecjeżeli
koniec czynności

czynność PODZIELTABLICE 
parametry tablica liczba TAB o długości zmienna liczba N i zmienna liczba L i zmienna liczba R
zwraca liczba początekczynności
	zmienna liczba INDEKSPODZIAŁU to wywołaj WYBIERZPUNKTPODZIAŁU L i R
	zmienna liczba WARTOŚĆPODZIAŁU to weź INDEKSPODZIAŁU element TAB
	wywołaj ZAMIEN TAB i INDEKSPODZIAŁU i R
	zmienna liczba AKTUALNAPOZYCJA to L
	pętla zakres zmienna liczba I od L do R odjąć 1 początekpętli
		jeżeli weź I element TAB mniejsze niż WARTOŚĆPODZIAŁU wtedy początekjeżeli
			wywołaj ZAMIEŃ TAB i I i AKTUALNAPOZYCJA
			AKTUALNAPOZYCJA to AKTUALNAPOZYJA dodać 1
		koniecjeżeli
	koniecpętli
	wywołaj ZAMIEŃ TAB i AKTUALNAPOZYCJA i R
	zwróć AKTUALNAPOZYCJA
koniecczynności

czynność WYBIERZPUNKTPODZIAŁU 
parametry liczba L i liczba R
zwraca liczba początekczynności
	zwróć L dodaj począteknawiasu R odjąć 1 koniecnawiasu moduł 2
koniecczynności

czynnośc ZAMIEN
parametry tablica liczba TAB o długości zmienna liczba N i zmienna liczba I i zmienna liczba J
zwraca nicość początekczynności
	jeżeli I nierówne J wtedy początekjeżeli
		zmienna liczba POMOC to weź I element TAB
		włóż weź J element TAB na I miejsce TAB
		włóż POMOC na J miejsce TAB
	koniecjeżeli
koniecczynności

tablica liczba TAB to 3 i 2 i 4 i 10 i 6
zmienna liczba ROZMIAR to 5
wywołaj QUICKSORT TABLICA i 0 i ROZMIAR
```

## Inne zarezerwowane słowa kluczowe
- ```minus```

