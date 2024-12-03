# Ferrari vs McLaren 2024

## Opis projektu

Projekt ten jest predykcją możliwych miejsc, które dają mistrzostwo konstruktorów Ferrari w walce przeciwko McLarenowi w najbliższym wyścigu odbywającym się w Abu Zabi.  
Znajduje się w nim kod, który:
- Generuje miejsca na mecie wyścigu.
- Sprawdza wyniki pod kątem spełnienia warunków mistrzostwa.
- Przesiewa wyniki do prostych tabel z przypisanymi miejscami oraz punktami.

Projekt ten wykorzystuje biblioteki:
- **Pandas**: Do przetwarzania danych i generowania tabel.
- **itertools**: Do tworzenia kombinacji i permutacji miejsc.

Kod analizuje trzy główne scenariusze:

Żadna ekipa nie zdobywa punktu za najszybsze okrążenie.
Ferrari zdobywa punkt za najszybsze okrążenie.
McLaren zdobywa punkt za najszybsze okrążenie.

Raport

1. McLaren poza podium – klucz do sukcesu Ferrari
McLaren, aby Ferrari mogło zdobyć mistrzostwo konstruktorów, nie może znaleźć się na podium w żadnym scenariuszu. Utrzymanie McLarena na dalszych pozycjach jest kluczowym warunkiem dla Ferrari, niezależnie od innych czynników.

2. Najlepszy scenariusz dla Ferrari
Najbardziej optymistyczna kombinacja dla Ferrari to:

-Ferrari zdobywa dublet, a Maclaren poza podium i bez najszybszego okrążenia.
-W przypadku gdy McLaren zdobywa najszybsze okrążenie to dalszy bolid McLarena musi być o jedną lokatę niżej, aby utrzymać przewagę punktową.

3. Wygrana przy jednym bolidzie Ferrari na mecie
Ferrari może zdobyć tytuł mistrza konstruktorów nawet w sytuacji, gdy tylko jeden ich bolid ukończy wyścig. Warunki do spełnienia to:

-Ferrari musi wygrać wyścig.
-McLaren nie może zająć wyższej pozycji niż 9. miejsce.

Ten scenariusz pokazuje, jak istotna jest minimalizacja punktów zdobywanych przez McLarena.

4. Znaczenie najszybszego okrążenia
Zdobycie najszybszego okrążenia przez Ferrari:

-Dodaje jedną dodatkową kombinację miejsc, która pozwala zespołowi na zwycięstwo w klasyfikacji konstruktorów.
-Ma wpływ na połowe kombinacji, że jeden bolid McLarena może być wyżej o 1 max 2 pozycje w porównaniu gdyby nikt nie zdobył najszybszego okrążenia.

Zdobycie najszybszego okrążenia przez McLaren:

-Ma wpływ na połowe kombinacji, że jeden bolid Mclarena musi być niżej o 1 lub 2 miejsca w porównaniu gdyby nikt nie zdobył najszybszego okrążenia.

Zdobycie najszybszego okrążenia ma wpływ na końcowe wyniki, natomiast ukazują się one głównie w kombinacjach gdzie McLaren jest w drugiej połowe pierwszej dziesiątki lub nawet poza punktami.