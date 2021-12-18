# Przetw-sygn-wielowymiarowych
 PWR - 2 semestr - MGR

# Spis treści
* [Teoria z wykładu](#teoria-z-wykładu)
* [Pojęcie obrazu cyfrowego](#pojęcie-obrazu-cyfrowego)

# Teoria z wykładu

## Czym jest cyfrowe przetwarzanie sygnału 


,,Cyfrowe przetwarzanie obrazów, to przetwarzanie obrazów przez komputer cyfrowy.''

Obraz cyfrowy zawsze składa się ze skończonej liczby elementów, a każdy z nich ma jednoznaczną lokalizację i wartość.


## Pojęcie obrazu cyfrowego

Obraz jest funkcją 2 zmiennych gdzie f(x,y) gdzie x i y to koordynaty przestrzenne określający dokładny punkt w przestrzeni 2D, w której dokonujemy jakąś pomiaru. f(x,y) to intensywność lub poziom szarości obrazu.

Powyższa funkcja jest funkcją ciągłą. Mając do czynienia z obrazem cyfrowym, wszystkie jego wartości są skończone i dyskretne (W pierwszej kolejności będą spróbkowane). Pula x i y będzie skończona. A lista dopuszczalnych wartości intensywności będzie skończona i będzie uzależniona silnie od głębi obrazu.

### Piksel (ang. pixel)
Pojęcie pikselu co do zasadny to skrót zawierający w sobie słowa ,, picutre elements''. Na początku powstał konflikt, ponieważ wedle analityków grafiki komputerowej podstawowym elementem obrazu jest jakiś prymityw, który ten obraz buduje (kwadrat, okrą, linia). Niemniej jednak środowisko inżynierskie z czasem przyjęło to pojęcie.

### Wykład I (inne)
Podstawowy sensor do odczytywania obrazu - oczy
Obraz cyfrowy musi być dyksrety! 

Inne sensory pozwalające na uzyskanie obrazu:
 * Aparat cefrowy (matryca CCD)
 * Soner

###  Alternatywne ścieżki pozysykiwania obrazu (inne niż np.kamera)

Są niezaskakujące, ale nie do końca intuicyjnie. Ponieważ echosonda zwana sonografem również służy do pozyskania obrazu. Obraz nie musi opierać się na promieniowaniu elektromagnetycznym. Obraz cyfrowy istnieje w momencie, w którym dysponujemy przestrzenią, którą możemy spróbować (nie musi ograniczać się do pasm wizyjnych!)

## Dziedziny przetwarzania obrazu.

### Niskopoziomowe przetwarzanie obrazu.
W przypadku niskopoziomowego przetwarzania obrazu zawsze wejściem i wyjściem przetwarzanego obrazu jest obraz. Przykładem niskiego przetwarzania obrazu jest np. filtracja częstotliwościowa, która na wejściu dostaję zaburzony obraz, a na wyjściu dostaje obraz, który został odszumiony. Każda operacja, która prowadzi do tego, aby uzyskać inny obraz (np. dodanie do siebie dwóch obrazów) będzie w obszarze niskopoziomowego przetwarzania obrazy.


### Średniopoziomowe przetwarzanie obrazu.

Wejście nadal jest obrazem, ale wyjście jest już pewnym opisem obrazu. Czyli niekoniecznie musi być już obrazem. Są tutaj wszystkie metody ekstrakcji atrybutów. Są w tym obszarze wszystkie metody, które służą do wykrywania kluczowych punktów w obrazie (np. tutaj jest okrąg, a tutaj jest coś, co wygląda jak narożnik budynku).


### Wysokopoziomowe przetwarzanie obrazu (Machine Vision)

Tutaj są wszystkie metody wykorzystujące modele rozpoznawania wzorców, które służą do tego, aby dostać obraz na samym początku, ale na końcu podjąć wobec niego jakąś decyzję. Najbardziej powszechnym i modnym obecnie przykładem są głębokie sieci konwolucyjne służące do klasyfikacji bądź regresji (rozwiązują złożone problemy które są reprezentowane przez obrazy)


"To jest wykorzystanie pewnych atrybutów wejściowych obrazów, aby system wizyjny mógł stać się zdolnym do podejmowania decyzji i rozumienia tych obrazów."
"Różnicą pomiędzy wysokopoziomym a średniopoziomym p.o jest wyjście. W przypadku wysokopoziomowego wyjściem jest atrybuty, w drugim jest obraz"


## Czynności przetwarzania obrazów

* 1 poziom. Akwizycja obrazu (próbkowanie, kwantyzacja, modalność)
* 2 poziom. Wzmacnianie obrazu (np. kontrast, pozbywanie się zanieczyszczeń)
* 3 poziom. Odtwarzanie obrazu (np. uzupełnianie ubytków w obrazie, wykorzystując elementry zanajdujące się na obrazie).
* 4 poziom. Obrazy barwne. (interpretacja jako tensor)
* 5 poziom. Przekształcenie morfologiczne (baza przekształceń konwolucyjnych)
* 6 poziom. Segmentacja obrazu.
* 7 poziom. Rozpoznawanie obiektów.

# Wykład II 

"Kiedy odbieramy barwy to obieramy jako przekształcenie 3D infomacji naszego oka który ma 2 wymiary przestrzenne i jeden wymiar długości fali i spłaszczamy go przy użyciu wektoraj"

## Interpolacja
Interpolacja jest to metoda numeryczna, która polega na wyznaczaniu przybliżonych wartości tzw. funkcji interpolacyjnej w danym przedziale, która przyjmuje z góry zadane wartości, w ustalonych punktach nazywanych węzłami. (np. interrpolacja liniowa)

## Rodzaje interpolacji

## Przepróbkowanie 
Przepróbkowanie (Resampling)- rtansformacja sygnału jedno-lub wielowymiarowego polegająca na utworzeniu nowych próbek wyjściowych na podstawie już istniejących próbek wejściowych, pozwalająca na zmianę częstotliwości próbkowania.

W "numpy" obraz jest reprezentowany obraz w skali szarości w macierzy 2D, zaś barwny w macierzy 3D. 
Wymiary macierzy to szerokość x wysokość x 3 (nie zawsze jest 3, możemy mieć 7 a nawet 200. ~ mogą być kamery wielowidmowe/nadwidmowe)
Adresowanie 

###  Coś o ludzkim oku i widzeniu 

"Dlaczego plamka ślepa nie widzi? :) Nie ma czopków ani pręcików. Jest to wejście nerwu wzorkowego."  \

###  Widzenie monochromatyczne 
Monochromatyzm, także: monochromacja (ang. monochromacy) – całkowita niezdolność do rozpoznawania barw - całkowitym zniesieniem widzenia barw. 

###  Widzenie Fotopowe i mezopowe 

Widzenie mezopowe, widzenie zmierzchowe – termin oznaczający pracę ludzkiego narządu wzroku w warunkach przejściowych, czyli przy niedostatecznej ilości światła. W odbieraniu bodźców świetlnych biorą udział wtedy zarówno czopki (działające przy dobrym oświetleniu i zapewniające widzenie barwne), jak i pręciki (działające przy niedostatecznym oświetleniu i dające jedynie możliwość widzenia achromatycznego).

###  Widzenie mezopowe 

Widzenie mezopowe jest stanem pośrednim pomiędzy widzeniem w normalnych warunkach oświetleniowych, zwanym widzeniem fotopowym, a postrzeganiem świata wyłącznie w barwach szarości, gdy światła jest bardzo mało, zwanym widzeniem skotopowym.

###  Pasma Macha

Pasmo Macha (efekt pasm Macha, wstęga Macha) – odkryta w 1865 przez Ernsta Macha właściwość wzroku ludzkiego, która objawia się dostrzeganiem nieistniejących pasm i zmiany jasności sąsiednich obszarów różniących się znacznie jasnością.

###  Konwolucja czyli połączenie dwóch funkcji

w numpy cipy.signal.convolve.

##  Iluminacja i Reflektancja 

Obraz jest iloczynem  dwóch wartości. (I) Iluminacji i (R) Reflektancji/ Transmutacją 

# Akwizycja obrazu cyfrowego 

Aby zrealizować akwizycję obrazu cyuforwego. najwpierw musimy dysponować sensorem zdolnym zdobyć informację przestrzenną. W momencie w którym realiuzujemy skowanie w której określonej częstotilowści będziemy go zapisywać to prubkowanie. Po prubklowanie realizujemy kwantyzację. 

## Kwantyzacja

Polega na podziale zakresu wartosci jasnosci na przedziały i przypisaniu każdemu punktowi wybranej wartosci dyskretnej.

Najpopularniejszym standardem jest  True color (2^24, czyli 16.777.216 kolorów). 
Mimo że w tym trybie do określenia koloru piksela wystarczą 24 bity, to najczęściej każdy kolor jest zapisywany na 32 bitach, czyli 4 bajtach. Te dodatkowe 8 bitów jest albo nieużywane, albo określa poziom przezroczystości piksela, czyli kanał alfa.


Ile kanałów intensywnbości obrazu mamy :
8 bitowych mamy 2
Zakres 0 - 255 (zakres dynamiczny)

Na ilu bitach infomacja jest zapisywana  - 24 
Ile mamy kanałów barw - 3 

# Sąsiedztwa 
W przetwarzaniu obrazów binarnych ważne jest określenie, kiedy dwa piksele sąsiadują ze sobą. W tym celu definiuje się dla każdego piksela jego sąsiedztwo.


## Sąsiedztwo otwarte / zamknięte 

Sasiedztwo zamknięte zawiera piksel zaś sąsiedztwo otwarte nie zawiera go.

## Sąsiedztwo 4 - spójne (von Neumanna) 

Obejmuje cztery piksele przyległe do danego z góry, dołu i po bokach
 
##  Sąsiedztwo 8 - spójne (Moore’a) 


# Operacje morfologiczne


Przekształcenia morfologiczne cyfrowych obrazów, to takie przekształcenia, w wyniku których struktura lub forma obiektu na obrazie zostaje zmieniona.

* Erozja
* Dylatacja
* Otwarcie i zamknięcie

# Metryki 


