# Java

Java to obiektowy język programowania wysokiego poziomu, ogólnego przeznaczenia.

---

## Podstawowy program

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

W ciele głównej metody znajuje się jedna instrukcja. Jest odpowiedzialna za wyświetlenie tekstu wpisanego w nawiasach okrągłych.

> `println` również jest pewną metodą. Należy do jednej z klas biblioteki standardowej.

Biblioteka standardowa to zbiór tysięcy klas, które dostępne są dla programistów. Zostały one napisane przez twórców języka Java.

> Na końcu każdej instrukcji znajduje się średnik.

## Zmienna

`Zmienna` to pewne wydzielone miejsce w pamięci komputera, gdzie mogą być przechowywane dane, na przykład wyniki wykonywanych operacji. Wartością zmiennej może być na przykład liczba lub ciąg znaków. Zmienna musi posiadać `nazwę symboliczną`, przez którą można odwoływać się do niej w programie. Nazwa może być dowolna, ale musi spełniać następujące warunki:

- Nazwa zmiennej nie może być słowem kluczowym języka Java,
- Nazwa nie może zaczynać się od cyfry,
- Nazwa nie może zawierać znaków białych i większości znaków specjalnych.

> `Słowa kluczowe` to zastrzeżone słowa, które mają specjalne znaczenie w językach programowania.

Ponadto należy pamiętać, że wielkie i małe litery są rozróżnialne. Poza powyższymi wymogami zaleca się nadawanie nazw jawnie określających przeznaczenie danej zmiennej i odradza stosowanie polskich znaków (staramy się korzystać tylko z alfabetu łacińskigo).

W przypadku nazw wieloczłonowych możemy posłużyć się jedną z popularnych notacji:

- `camelCase` - wszystkie wyrazy piszemy łącznie, każdy kolejny zaczynając od wielkiej litery,
- `PascalCase` - wszystkie wyrazy piszemy łącznie, każdy (łącznie z pierwszym) zaczynając od wielkiej litery,
- `snake_case` - wyrazy oddzielamy znakiem myślnika,
- `kebab-case` - wyrazy oddzielamy znakiem myślnika.

Javę cechuje typowanie silne, w związku z tym trzeba jawnie określić typ zmiennej, poprzez dodanie słowa kluczowego. Kilka podstawowych typów wbudowanych, oferowancyh przez Javę to:

- `int` - liczba całkowita,
- `double` - liczba rzeczywista,
- `char` - znak,
- `boolean` - wartość logiczna.

Deklaracja zmiennej:
```java
int number;
```

Zmiana wartości zmiennej - operator przypisania:
```java
int number;

number = 3;
```

Inicjalizacja zmiennej:
```java
int number = 3;
```

Inicjalizacja stałej:
```java
final int PI = 3.14;
```

> W przypadku stałych rozpoczynamy inicjalizację od słowa `final`.

## Podstawowe operatory

Podobnie jak inne języki, Java oferuje kilka podstawowych operatorów arytmetycznych, znanych z matematyki:
- `+` - dodawanie,
- `-` - odejmowanie,
- `*` - mnożenie,
- `/` - dzielenie.

## String

`String` to wbudowany złożony typ danych. Służy do przechowywania ciągów znaków.

## Pobieranie wartości od użytkownika

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

> Aby mieć możliwość pobierania wartości wpisywanych przez użytkownika, musimy zaimportować klasę `Scanner` przy pomocy słowa kluczowego `import`.
