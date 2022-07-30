# Opis działania aplikacji

Aplikacja powinna zbierać od użytkownika jak najwięcej informacji, bez przerażania go ilością danych. Okienka szczegółów powinny być ukryte przed użytkownikiem, a każdy formularz powinien mieć najwyżej kilka pól do wypełnienia lub zaznaczenia. Tam, gdzie to możliwe, kreator powinien zadawać konkretne pytania.

## Inicjacja procesu zbierania danych

Użytkownik powinien mieć poczucie, że jest w przyjaznym i zaplanowanym środowisku. Nie powinien zaczynać od pustej kartki. Dlatego na początku będzie wybierać z predefiniowanej listy obiektów. Na oczątek lista może wyglądać następująco:

* szkoła
* przedszkole
* żłobek
* dom kultury
* biblioteka
* urząd
* poczta
* kościół
* sklep
* kino
* teatr
* restauracja
* stacja kolejowa
* inny obiekt

W rzeczywistości różnice będą polegać na zaproponowaniu gotowych miejsc, liczby pięter i rodzajów pomieszczeń. Na przykład szkoła będzie miała domyślnie kondygnacje od -1 do2 i pomieszczenia w rodzaju szatnia, biblioteka szkolna, sekretariat, pokój nauczycielski, sala lekcyjna nr ... itd. Z kolei biblioteka to jedna kondygnacja i pomieszczenia: wypożyczalnia, czytelnia itp. Na każdej kondygnacji domyślnie znajduje się łazienka.

## Budowanie struktury budynku

Okno z pytaniem o liczbę kondygnacji w budynku. Na schematycznym rysunku użytkownik zaznacza zajmowane przez podmiot kondygnacje. W interfejsie graficznym kondygnacje w budynku są ułożone w pionie, zgodnie z rzeczywistością, to znaczy na dole parter, wyżej I piętro, dalej II piętro itd. Poniżej parteru mogą być kolejne kondygnacje, na przykład poziom -1. Nazwy domyślne powinny być naturalne i do zmiany przez użytkownika. Użytkownik może dodawać i usuwać kondygnacje. Opisane kondygnacje powinny się jakoś wyróżniać wizualnie. Jeżeli organizacja ma siedzibę na kondygnacji innej, niż parter i zajmuje tylko jedną, to kondygnacje poniżej i powyżej powinny być również wyświetlone w trybie "nie do edycji". Kondygnacje można dodawać i usuwać.

Po kliknięciu na kondygnację, wyświetla się lista pomieszczeń oraz właściwości samej kondygnacji. Po kliknięciu pomieszczenia można wybrać proste zaznaczenie, że pomieszczenie jest dostępne lub dodać inne właściwości, w tle tworząc miejsce z wszystkimi właściwościami. Użytkownik może zmieniać nazwę pomieszczenia i kondygnację.

## Lokalizacja

Użytkownik wypełnia formatkę adresu. Dane są automatycznie kopiowane do wszystkich miejsc zbioru danych. Ukryte są kategoria, piętro i pomieszczenie.

Na podstawie danych adresowych może być wygenerowana geolokalizacja i mapka orientacyjna. Użytkownik może dodać zdjęcie budynku.


## Walidacja

Aplikacja może dokonać walidacji informacji pod względem ich kompletności.

1. Czy dla każdego miejsca zapewniony jest opis wejścia (entrance)?
2. Czy dodane są elementy obowiązkowe z punktu widzenia ustaw: informacja o usłudze PJM, pętli indukcyjnej, planach dotykowych, powiększonych, systemach dźwiękowych?
3. Czy jest wprowadzona informacja o miejscach parkingowych?
4. Czy wprowadzona jest polityka dotycząca zwierząt?

W przyszłości można będzie wprowadzić kolejne algorytmy walidacji.

## Raporty

Na podstawie zebranych danych użytkownik może wygenerować następujące raporty:

1. Deklaracja dostępności architektonicznej i informacyjno-komunikacyjnej.
2. Dane ustrukturalizowane w formie JSON-LD.
3. Raport z audytu wraz z rekomendacjami.
4. test 01

