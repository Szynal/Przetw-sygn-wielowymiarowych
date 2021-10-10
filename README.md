# Przetw-sygn-wielowymiarowych
 PWR - 2 semestr - MGR


# Teoria z wykładu

## Czym jest cyfrowe przetwarzanie sygnału 


,,Cyfrowe przetwarzanie obrazów, to przetwarzanie obrazów przez komputer cyfrowy.''

Obraz cyfrowy zawsze składa się ze skończonej liczby elementów, a każdy z nich ma jednoznaczną lokalizację i wartość.


## Pojęcie obrazu cyfrowego

Obraz jest funkcją 2 zmiennych gdzie f(x,y) gdzie x i y to koordynaty przestrzenne określający dokładny punkt w przestrzeni 2D, w której dokonujemy jakąś pomiaru. f(x,y) to intensywność lub poziom szarości obrazu.

Powyższa funkcja jest funkcją ciągłą. Mając do czynienia z obrazem cyfrowym, wszystkie jego wartości są skończone i dyskretne (W pierwszej kolejności będą spróbkowane). Pula x i y będzie skończona. A lista dopuszczalnych wartości intensywności będzie skończona i będzie uzależniona silnie od głębi obrazu.

### Piksel (ang. pixel)
Pojęcie pikselu co do zasadny to skrót zawierający w sobie słowa ,, picutre elements''. Na początku powstał konflikt, ponieważ wedle analityków grafiki komputerowej podstawowym elementem obrazu jest jakiś prymityw, który ten obraz buduje (kwadrat, okrą, linia). Niemniej jednak środowisko inżynierskie z czasem przyjęło to pojęcie.


###  Alternatywne ścieżki pozysykiwania obrazu (inne niż np.kamera)

Są niezaskakujące, ale nie do końca intuicyjnie. Ponieważ echosonda zwana sonografem również służy do pozyskania obrazu. Obraz nie musi opierać się na promieniowaniu elektromagnetycznym. Obraz cyfrowy istnieje w momencie, w którym dysponujemy przestrzenią, którą możemy spróbować (nie musi ograniczać się do pasm wizyjnych!)

## Dziedziny przetwarzania obrazu.

### Niskopoziomowe przetwarzanie obrazu.
W przypadku niskopoziomowego przetwarzania obrazu zawsze wejściem i wyjściem przetwarzanego obrazu jest obraz. Przykładem niskiego przetwarzania obrazu jest np. filtracja częstotliwościowa, która na wejściu dostaję zaburzony obraz, a na wyjściu dostaje obraz, który został odszumiony. Każda operacja, która prowadzi do tego, aby uzyskać inny obraz (np. dodanie do siebie dwóch obrazów) będzie w obszarze niskopoziomowego przetwarzania obrazy.


### Średniopoziomowe przetwarzanie obrazu.

Wejście nadal jest obrazem, ale wyjście jest już pewnym opisem obrazu. Czyli niekoniecznie musi być już obrazem. Są tutaj wszystkie metody ekstrakcji atrybutów. Są w tym obszarze wszystkie metody, które służą do wykrywania kluczowych punktów w obrazie (np. tutaj jest okrąg, a tutaj jest coś, co wygląda jak narożnik budynku).


### Wysokopoziomowe przetwarzanie obrazu (Machine Vision)

Tutaj są wszystkie metody wykorzystujące modele rozpoznawania wzorców, które służą do tego, aby dostać obraz na samym początku, ale na końcu podjąć wobec niego jakąś decyzję. Najbardziej powszechnym i modnym obecnie przykładem są głębokie sieci konwolucyjne służące do klasyfikacji bądź regresji (rozwiązują złożone problemy które są reprezentowane przez obrazy)

## Czynności przetwarzania obrazów

* 1 poziom. Akwizycja obrazu (próbkowanie, kwantyzacja, modalność)
* 2 poziom. Wzmacnianie obrazu (np. kontrast, pozbywanie się zanieczyszczeń)
* 3 poziom. Odtwarzanie obrazu (np. uzupełnianie ubytków w obrazie, wykorzystując elementry zanajdujące się na obrazie).
* 4 poziom. Obrazy barwne. (interpretacja jako tensor)
* 5 poziom. Przekształcenie morfologiczne (W przekształceniach morfologicznych pozwalają nam na dokonywanie dowolnych przekształceniach geometrycznych obrazu. np możemy wyliczyć sobie miejsce, w którym znalazłby się piksel obrazu, gdyby obraz zostałby pochylony/przeskalowany )






