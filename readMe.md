# Spis treści

1. [Wprowadzenie](#wprowadzenie)
    - [Klasa i obiekt](#klasa-i-obiekt)
2. [Podstawowy program](#podstawowy-program)
    - [Wyświetlanie w konsoli](#wyświetlanie-w-konsoli)
3. [Zmienna](#zmienna)
    - [Podstawowe operatory](#podstawowe-operatory)
    - [Dodatkowe operatory przypisania](#dodatkowe-operatory-przypisania)
    - [Konkatenacja](#konkatenacja)
    - [Ciągi znaków](#ciągi-znaków)
4. [Pobieranie wartości od użytkownika](#pobieranie-wartości-od-użytkownika)
5. [Instrukcje warunkowe](#instrukcje-warunkowe)
    - [Operatory relacyjne](#operatory-relacyjne)
6. [Wartości logiczne](#wartości-logiczne)
    - [Konstrukcja instrukcji warunkowej](#konstrukcja-instrukcji-warunkowej)
    - [Warunki złożone](#warunki-złożone)
7. [Pętle](#pętle)
    - [Iterator i iteracja](#iterator-i-iteracja)
    - [While](#while)
    - [Do while](#do-while)
    - [For](#for)
    - [Iterowanie po ciągach znaków](#iterowanie-po-ciągach-znaków)
8. [Tablice](#tablice)
    - [Deklaracja tablicy](#deklaracja-tablicy)
    - [Iterowanie po tablicach](#iterowanie-po-tablicach)
    - [Tablice wielowymiarowe](#tablice-wielowymiarowe)

&nbsp;

# Wprowadzenie

Java to obiektowy język programowania wysokiego poziomu, ogólnego przeznaczenia.

## Klasa i obiekt

Na podstawie **klas** tworzone są **obiekty**. Można je rozumieć jak pewngeo rodzaju przepisy na ich stworzenie. Definiujemy w nich **stan** oraz **zachowanie** obiektów. Poprzez stan rozumiemy wszelkie dane przechowywane w obrębie obiektu, z kolei zachowaniem są **metody**, czyli funkcje, które mogą operować na tych danych.

# Podstawowy program

```java
public class HelloWorld {
    public static void main(String[] args) {

        System.out.println("Hello world!");
    }
}
```

Pisanie programu zaczynamy od zdefiniowania przykładowej klasy `HelloWorld`. Jej nazwa musi pokrywać się z nazwą pliku z rozszerzeniem `java`. Kod Java zawsze znajduje się wewnątrz pewnej klasy. Jej ciało wyznaczone jest poprzez nawiasy klamrowe.

> Nazwy klas przyjęło się pisać z wielkiej litery

W ciele klasy `HelloWorld` znajduje się definicja metody `main`. To właśnie od tej metody program rozpoczyna pracę. Ciało metody znajduje się pomiędzy nawiasami klamrowymi.

> Jeżeli jakaś instrukcja ma zostać wykonana, to musi znajdować się w obrębie metody głównej.

W ciele głównej metody znajuje się jedna instrukcja. Jest odpowiedzialna za wyświetlenie tekstu wpisanego w nawiasach okrągłych.

> `println` również jest pewną metodą. Należy do jednej z klas biblioteki standardowej.

**Biblioteka standardowa** to zbiór tysięcy klas, które dostępne są dla programistów. Zostały one napisane przez twórców języka Java.

> Na końcu każdej instrukcji znajduje się średnik.

## Wyświetlanie w konsoli

Najprostszym sposobem porozumiewania się z użytkownikiem jest korzystanie z konsoli. W celu wyświetlenia tam danych informacji posłużą nam dwie podstawowe funkcje:

```java
System.out.println("Przykładowy tekst");
System.out.print("Inny tekst");
```

Metoda `println` poza wyświetleniem podanego napisu przejdzie do następnej linii. W przypadku `print` tekst zostanie wyświetlony bez dodatkowego przejścia na końcu.

> Napisy, ciągi znaków, czy też łańcuchy znaków zapisujemy w języku Java w cudzysłowie.

# Zmienna

**Zmienna** to pewne wydzielone miejsce w pamięci komputera, gdzie mogą być przechowywane dane, na przykład wyniki wykonywanych operacji. Wartością zmiennej może być na przykład liczba lub ciąg znaków. Zmienna musi posiadać **nazwę symboliczną**, przez którą można odwoływać się do niej w programie. Nazwa może być dowolna, ale musi spełniać następujące warunki:

- Nazwa zmiennej nie może być słowem kluczowym języka Java,
- Nazwa nie może zaczynać się od cyfry,
- Nazwa nie może zawierać znaków białych i większości znaków specjalnych.

> **Słowa kluczowe** to zastrzeżone słowa, które mają specjalne znaczenie w językach programowania.

Ponadto należy pamiętać, że wielkie i małe litery są rozróżnialne. Poza powyższymi wymogami zaleca się nadawanie nazw jawnie określających przeznaczenie danej zmiennej i odradza stosowanie polskich znaków (staramy się korzystać tylko z alfabetu łacińskigo).

W przypadku nazw wieloczłonowych możemy posłużyć się jedną z popularnych notacji:

- **camelCase** - wszystkie wyrazy piszemy łącznie, każdy kolejny zaczynając od wielkiej litery,
- **PascalCase** - wszystkie wyrazy piszemy łącznie, każdy (łącznie z pierwszym) zaczynając od wielkiej litery,
- **snake_case** - wyrazy oddzielamy znakiem myślnika,
- **kebab-case** - wyrazy oddzielamy znakiem myślnika.

Javę cechuje **typowanie silne**, w związku z tym trzeba jawnie określić typ zmiennej, poprzez dodanie słowa kluczowego. Kilka podstawowych, **prymitywnych typów wbudowanych**, oferowancyh przez Javę to:

- `int` - liczba całkowita,
- `double` - liczba rzeczywista,
- `char` - znak,
- `boolean` - wartość logiczna.

> Pojedyncze znaki zapisujemy w apostrofach, na przykład `'a'`, a liczby rzeczywiste z kropką pomiędzy częścią całkowitą, z dziesiętną, na przykład *9.8*.

Deklaracja zmiennej:
```java
int number;
```

Nadanie lub zmiana wartości zmiennej - operator przypisania:
```java
int number;

number = 3;
```

Inicjalizacja zmiennej - nadanie wartości zmiennej podczas jej deklaracji:
```java
int number = 3;
```

> Deklaracja, czyli utworzenie nowej zmiennej odbywa się poprzez podanie typu danych oraz nazwy symbolicznej, po której będziemy mogli odwoływać się do danej zmiennej. Korzystając ze znaku `=` możemy od razu przypisać zmiennej pewną wartość.

Inicjalizacja stałej:
```java
final double PI = 3.14;
```

> W przypadku stałych rozpoczynamy inicjalizację od słowa `final`. Stała, jak sama nazwa wskazuje, nie pozwala na przypisanie nowej wartości, zatem musimy ją nadać podczas deklaracji. Przyjęło się, że nazwy symboliczne stałych zapisujemy wielkimi literami.

# Podstawowe operatory

Podobnie jak inne języki, Java oferuje kilka podstawowych operatorów arytmetycznych, znanych z matematyki:
- `+` - dodawanie,
- `-` - odejmowanie,
- `*` - mnożenie,
- `/` - dzielenie,
- `%` - dzielenie modulo, reszta z dzielenia.

> Większość oznaczeń operatorów jest intuicyjna. W przypadku `modulo` nie należy sugerować się oznaczeniem i mylić operator z pojęciem procenta.

Dzielenie modulo najczęściej wykorzystywane jest do sprawdzania podzielności liczb. Jeżeli reszta z dzielenia równa jest zero, to znaczy, że pierwsza liczba dzieli się całkowicie przez drugą liczbę.

```java
int a = 3,
    b = -5;
    
int result = a + b;

System.out.println("Wynik działania: " + result);
System.out.println("To samo działanie: " + (a + b));
```

Powyższy przykład przedstawia dodawanie dwóch liczb. Na początku deklarujemy dwie zmienne i inicjujemy je ustalonymi wartościami całkowitymi. Jeżeli typ danych jest taki sam dla kilku zmiennych, to możemy wypisywać je po przecinku, bez konieczności powtarzania słowa kluczowego `int`. W celu wyświetlenia sumy (wyniku dodawania) możemy zadeklarować kolejną zmienną, ale możemy również wykonać operację bezpośrednio w nawiasach metody `println`.

> Często poza wartościami liczbowymi będziemy chcieli wyświetlić napis mówiący, czym jest dana wartość. Można to zrobić na kilka sposobów. Jednym z rozwiązań jest kilka oddzielych wywołań metod `println` lub `print`. Innym jest dodawanie ciągów znaków.

## Dodatkowe operatory przypisania

Często będziemy musieli zmieniać wartość danej zmiennej, nadpisując ją inną wartością.

```java
int number = 5;

number = number + 2;
```

Przykładowo, liczbę możemy nadpisać wartością o *2* większą, przypisując jej nową wartość w postaci sumy jej starej wartości i liczby *2*. Taki zapis można skrócić:
- +=,
- -=,
- *=,
- /=,
- %=.

```java
int number = 5;

number += 2;
```

Powyższy zapis jest równoważny. Wynik działania będzie identyczny poprzednim. W obu wypadkach zwiększamy liczbę o *2*.

## Konkatenacja

**Konkatenacja** oznacza w informatyce dodawanie ciągów znaków, czy inaczej sklejanie napisów. Operatorem odowiedzialnym za tę operację jest znak `+`, a jej argumentami są na przykład napisy.

> W przypadku poprzedniego przykładu konkatenacji został poddany napis oraz liczba całkowita. Nastąpiła tak zwana konwersja niejawna. Przed doklejeniem wyniku dodawania do napisu, liczba została zmieniona na napis.

## Ciągi znaków

`String` to wbudowany złożony typ danych. Służy do przechowywania ciągów znaków.

> Złożone typy danych, jak sama nazwa wskazuje, z czegoś się składają. Mogą być zawierać typy proste, jak też inne typy złożone.

Typ `String` odnosi się do napisów. Te z kolei, składają się na przykład z poszczególnych liter i cyfr - znaków.

# Pobieranie wartości od użytkownika

```java
import java.util.Scanner;

public class HelloWorld {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        String text = scanner.next();

        System.out.println(text);

        scanner.close();
    }
}
```

Aby mieć możliwość pobierania wartości wpisywanych przez użytkownika, musimy zaimportować klasę `Scanner` przy pomocy słowa kluczowego `import`. By móc korzystać z jej metod, musimy na jej podstawie utworzyć obiekt. Robimy to tworząc zmienną o typie złożonym `Scanner` i przypisując jej nowo stworzony obiekt przy pomocy `new`. Teraz odwołując się do nowej zmiennej możemy korzystać z metod interesującej nas klasy.

Do dyspozycji mamy kilka podstawowych metod, w  zależności od typu danych:
- `next` - pobiera całe napisy,
- `nextInt` - pobiera liczbę całkowitą,
- `nextDouble` - pobiera liczbę rzeczywistą.

> Zawsze należy pamiętać o nadaniu nowej zmiennej odpowiedniego typu danych.

Inny przykład:

```java
import java.util.Scanner;

public class HelloWorld {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        double first = scanner.nextDouble(),
               second = scanner.nextDouble();

        System.out.println("Suma: " + (first + second));

        scanner.close();
    }
}
```

# Instrukcje warunkowe

Instrukcje warunkowe służą warunkowemu wykonywaniu instrukcji, w zależności czy pewne przyjęte założenia zostały spełnione.

Instrukcja warunkowa jest spełniona, gdy zawarty w niej warunek jest prawdziwy - zwraca wartość logiczną `true`. W przypadku wartości fałszywej - `false`, wskazane instrukcje nie zostaną wykonane.

```java
public class Main {
    public static void main(String[] args) {

        int age = 21;

        if (age >= 18) {

            System.out.println("Osoba jest pełnoletnia.");
        }
    }
}
```

> Powyższa instrukcja warunkowa sprawdza, czy wartość zmiennej `age` (przehowującej wiek) jest większa lub równa *18*. Jeżeli tak, to wyświetlany jest stosowny napis.

Instrukcje, które mają zostać wykonane, gdy spełniony jest warunek zapisujemy pomiędzy nawiasami klamrowymi. W przypadku pojedynczej instrukcji klamry możemy pominąć

```java
int age = 21;

if (age >= 18)
    System.out.println("Osoba jest pełnoletnia.");
```

## Operatory relacyjne

Do dyspozycji mamy kilka operatorów służących porównywaniu danych wartości:

|operator|nazwa|
|-|-|
|`==`|równe|
|`!=`|równe|
|`>`|większe niż|
|`>=`|większe lub równe|
|`<`|mniejsze niż|
|`<=`|mniejsze lub równe|

> Pojedynczy znak równości zarezerwowany jest dla operacji przypisania, więc do porównywania wartości służą dwa znaki.

# Wartości logiczne

Zmienne typu `boolean` mogą przechowywać jedynie dwie wartości - `true` (prawda) lub `false` (fałsz). Są to tak zwane wartości logiczne. Operatory logiczne, czyli wszelkie porównania, zwracają wynik w postaci takiej wartości.

## Konstrukcja instrukcji warunkowej

```java
double number = 2.1;

if (number > 0)
    System.out.println("Liczba jest dodatnia.");
else if (number == 0)
    System.out.println("Liczba równa zero.");
else
    System.out.println("Liczba jest ujemna.");
```

Poza instrukcją `if` mamy do dyspozycji `else if` odpowiedzialne za sprecyzowanie kolejnego, odrębnego warunku, oraz `else` służące przechwytywaniu wszelkich pozostałych przypadków.

> Instrukcje w `else` zostaną wykonane, jeżeli żadna z wcześniejszych instrukcji warunkowych nie została spełniona.

## Warunki złożone

Dane warunki proste, opierające się na przykład na porównaniach, możemy łączyć w bardziej złożone i precyzyjne konstrukcje.

|operator|nazwa|opis|
|-|-|-|
|`&&`|koniunkcja|and, i, oraz - oba warunki muszą być spełnione|
|`\|\|`|alternatywa|or, lub - przynajmniej jeden z warunków musi być spełnony|
|`!`|negacja|not, zaprzeczenie - odwrócenie wartości logicznej|

Przykłady:

```java
int x = 6;

if (-2 <= x && x < 7)
    System.out.println("Liczba x znajduje się w przedziale.");
```

Liczba znajduje się w przedziale prawostronnie domkniętym *[-2; 7)* (jest większa lub równa od *-2* oraz mniejsza niż *7*).

```java
int x = 2;

if ( !(x == 3 || x == -3) )
    System.out.println("Liczba x nie jest równa 3 ani -3");
```

Liczba nie jest równa *3* ani *-3* (nieprawdą jest, że jest równa *3* lub *-3*).

# Pętle

Pętle służą do wielokrotnego wykonywania danych instrukcji, tak długo, jak określony warunek pozostaje spełniony.

## Iterator i iteracja

Iteracja pętli to jednorazowe wykonanie się wszystkich instrukcji w niej zawartych, pojedynczy obrót pętli.

Iterator to pomocnicza zmienna sterująca wykonywaną pętlą. Na przykład zliczająca kolejne iteracje.

## While

```java
int i = 0;

while (i < 10) {

    System.out.println("Iterator: " + i);
    i++;
}
```

W przypadku pętli `while` po słowie kluczowym, w nawiasach okrągłych, wpisujemy warunek, a między klamrami instrukcje, które mają się wykonywać. Pętla działa dopóki zadany warunek jest spełniony.

> Instrukcja `i++` odpowiedzialna jest za zwiększenie wartości zmiennej `i` o 1. Jest to tak zwana inkrementacja. Zmniejszenie wartości o 1 nazywamy dekrementacją i oznaczamy jako `i--`.

## Do while

```java
int i = 0;

do {

    System.out.println("Iterator: " + i);
    i++;
} while (i < 10);
```

Pętlę `do while` charakteryzuje umiejscowanie warunku na końcu pętli. Oznacza to, że najpierw wykonane zostaną instrukcje zawarte w pętli, a dopiero później zostanie sprawdzony warunek.

## For

```java
for (int i = 0; i < 10; i++) {

    System.out.println("Iterator: " + i);
}
```

W deklaracji pętli for znajduje się deklaracja iteratora, warunek oraz zmiana wartości iteratora po każdym wykonaniu pętli.

## Iterowanie po ciągach znaków

W przypadku typów złożonych często będziemy chcieli mieć możliowść odwołania się do poszczególnych elementów.

```java
String text = "Ala ma kota";
char character = text.charAt(4);

System.out.println("Znak o indeksie 4: " + character);
```

W przypadku typu `String` posłuży nam do tego metoda `charAt`, w której jako argument podajemy interesujący nas indeks.

> Indeks oznacza numer danego znaku w napisie. W informatyce przyjęło się, że kolejne elementy numerowane są od zera.

```java
String text = "Ala ma kota";
int length = text.length();

System.out.println("Długość tekst: " + length);
```

Przydatna może być również metoda `length`, zwracająca długość danego napisu.

Przykład zastosowania tych dwóch metod:

```java
String text = "Ala ma kota";
int length = text.length();

for (int i = 0; i < length; i++) {

    char character = text.charAt(i);

    System.out.println(character);
}
```

# Tablice

**Tablice** to struktury pozwalające na przechowywanie większej ilości danych w uporządkowanej formie.

## Deklaracja tablicy

```java
int [] numbers = {3, 2, 1};
```

Deklarację tablicy zaczynamy od podania typ danych, jaki będzie przechowywała, nawiasów kwadratowych oraz nazwy symbolicznej. Inicjalizujemy ją poprzez podanie wartości w nawiasach klamrowych.

```java
int [] numbers = new int[3];
```

W przypadku, gdy nie chcemy od razu podawać wartości, stosujemy inny zapis, gdzie jawnie podajemy rozmiar tablicy.

> Rozmiaru tablicy nie można zmienić po jej utworzeniu.

Elementy tablicy są uporządkowane, to znaczy, że mają ustaloną kolejność określone przez `indeks`, czyli liczbę, po której możemy odwołać się do danego elementu.

> Elementy indeksowane są od *0*.

```java
int [] numbers = {8, -2, 3};

System.out.println("Pierwszy element: " + numbers[0]);

System.out.println("Drugi element: " + numbers[1]);
```

Oczywiście poza odczytywaniem wartości z tablicy, mamy również możliwość ich zmiany.

```java
int [] numbers = new int [2];

System.out.println("Stara wartość: " + numbers[0]);

numbers[0] = -4;

System.out.println("Nowa wartość: " + numbers[0]);
```

## Iterowanie po tablicach

Tworzone tablice często zawierać będą dużo danych, na których najłatwiej będzie operować przy pomocy wcześniej poznanych pętli.

```java
int [] numbers = {8, 4, 5, 2};

for (int i = 0; i < numbers.length; i++)
    System.out.println(numbers[i]);
```

W celu pobrania długości tablicy korzystamy z pola `length`. Wartość wykorzystać można do ograniczenia iteratora. Przy próbie odwołania się do indeksu spoza tablicy otrzymamy błąd.

## Tablice wielowymiarowe

Tablice mogą mieć więcej niż jeden wymiar - tablica może zawierać kolejne tablice. Mowa wtedy o tablicach **wielowymiarowych** lub **zagnieżdżonych**.

```java
int [][] numbers = new int[2][3];

numbers[0][1] = 3;

System.out.println("Element o indeksach 0,1: " + numbers[0][1]);
```

### Inicjalizowanie tablic wielowymiarowych

```java
int [][] numbers = {

    {1, 1},
    {3, 2}
};

System.out.println(numbers[1][1]);
```

### Iterowanie po tablicach zagnieżdżonych

```java
char [][] letters = {

    {'a', 'b'},
    {'c', 'd'}
};

for (int y = 0 ; y < letters.length; y++)
    for (int x = 0 ; x < letters.length; x++)
        System.out.println(letters[y][x]);
```
