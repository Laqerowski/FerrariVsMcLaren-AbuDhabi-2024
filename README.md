# Ferrari vs McLaren Abu Dhabi 2024

## Opis projektu

Projekt ten jest predykcją możliwych miejsc, które dają mistrzostwo konstruktorów Ferrari w walce przeciwko McLarenowi w najbliższym wyścigu odbywającym się w Abu Zabi.  
Znajduje się w nim kod, który:
- Generuje miejsca na mecie wyścigu.
- Sprawdza wyniki pod kątem spełnienia warunków mistrzostwa.
- Przesiewa wyniki do prostych tabel z przypisanymi miejscami oraz punktami.

Projekt ten wykorzystuje biblioteki:
- **Pandas**: do przetwarzania danych i generowania tabel.
- **itertools**: do tworzenia kombinacji i permutacji miejsc.

Kod analizuje trzy główne scenariusze:
1. Żadna ekipa nie zdobywa punktu za najszybsze okrążenie.
2. Ferrari zdobywa punkt za najszybsze okrążenie.
3. McLaren zdobywa punkt za najszybsze okrążenie.

---

## Raport

### 1. McLaren poza podium – klucz do sukcesu Ferrari
McLaren, aby Ferrari mogło zdobyć mistrzostwo konstruktorów, nie może znaleźć się na podium w żadnym scenariuszu. Utrzymanie McLarena na dalszych pozycjach jest kluczowym warunkiem dla Ferrari, niezależnie od innych czynników.


### 2. Najlepszy scenariusz dla Ferrari
Najbardziej optymistyczna kombinacja dla Ferrari to:
- Ferrari zdobywa dublet, a McLaren pozostaje poza podium i bez najszybszego okrążenia.
- W przypadku, gdy McLaren zdobywa najszybsze okrążenie, dalszy bolid McLarena musi być o jedną lokatę niżej, aby Ferrari utrzymało przewagę punktową.


### 3. Wygrana przy jednym bolidzie Ferrari na mecie
Ferrari może zdobyć tytuł mistrza konstruktorów nawet w sytuacji, gdy tylko jeden ich bolid ukończy wyścig. Warunki do spełnienia to:
- Ferrari musi wygrać wyścig.
- McLaren nie może zająć wyższej pozycji niż 9. miejsce.

Ten scenariusz pokazuje, jak istotna jest minimalizacja punktów zdobywanych przez McLarena.


### 4. Znaczenie najszybszego okrążenia

#### Zdobycie najszybszego okrążenia przez Ferrari:
- Dodaje jedną dodatkową kombinację miejsc, która pozwala zespołowi na zwycięstwo w klasyfikacji konstruktorów.
- Ma wpływ na połowę kombinacji, umożliwiając jednemu bolidowi McLarena zajęcie o maksymalnie 1-2 wyższych pozycji w porównaniu z sytuacją, gdy nikt nie zdobył najszybszego okrążenia.

#### Zdobycie najszybszego okrążenia przez McLaren:
- Ma wpływ na połowę kombinacji, wymuszając, aby jeden z bolidów McLarena znalazł się o 1-2 miejsca niżej w porównaniu z sytuacją, gdy nikt nie zdobył najszybszego okrążenia.


Zdobycie najszybszego okrążenia ma wpływ na końcowe wyniki, szczególnie w kombinacjach, w których McLaren znajduje się w drugiej połowie pierwszej dziesiątki lub nawet poza punktami.

# Najszybsze okrążenie
### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Ferrari &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Nikt &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;McLaren
| **Pozycja Ferrari**  | **Pozycja McLarena**| **Pozycja Ferrari** | **Pozycja McLarena**| **Pozycja Ferrari**| **Pozycja McLarena** |
|----------------------|---------------------|---------------------|---------------------|---------------------|---------------------|
| 1 & 2                | 4 & 5               | 1 & 2               | 4 & 5               | 1 & 2               | 4 & 6               |
| 1 & 3                | 4 & 6               | 1 & 3               | 5 & 6               | 1 & 3               | 5 & 6               |
| 1 & 4                | 5 & 7               | 1 & 4               | 5 & 7               | 1 & 4               | 6 & 7               |
| 1 & 5                | 6 & 7               | 1 & 5               | 6 & 7               | 1 & 5               | 6 & 8               |
| 2 & 3                | 6 & 8               | 1 & 7               | 6 & 9               | 2 & 3               | 7 & 8               |
| 1 & 7                | 6 & 9               | 2 & 3               | 7 & 8               | 1 & 6               | 7 & 8               |
| 1 & 6                | 7 & 8               | 1 & 6               | 7 & 8               | 1 & 8               | 7 & 10              |
| 1 & 8                | 7 & 9               | 1 & 8               | 7 & 9               | 1 & 7               | 8 & 9               |
| 2 & 4                | 7 & 9               | 2 & 4               | 7 & 9               | 2 & 4               | 8 & 9               |
| 1 & 9                | 7 & 10              | 2 & 5               | 8 & 9               | 1 & 9               | 8 & 10              |
| 1 & 10               | 8 & 9               | 1 & 9               | 8 & 10              | 2 & 5               | 8 & 10              |
| 2 & 5                | 8 & 9               | 3 & 4               | 8 & 10              | 1 & 10              | 8 & 11              |
| 3 & 4                | 8 & 9               | 1 & 10              | 8 & 11              | 1 & 11              | 9 & 10              |
| 1 & 11               | 8 & 10              | 1 & 11              | 9 & 10              | 2 & 6               | 9 & 10              |
| 2 & 6                | 8 & 10              | 2 & 6               | 9 & 10              | 3 & 4               | 9 & 10              |
| 2 & 7                | 9 & 10              | 3 & 5               | 9 & 10              | 3 & 5               | 9 & 11              |
| 3 & 5                | 9 & 10              | 2 & 7               | 9 & 11              | 2 & 7               | 10 & 11             |
| 3 & 6                | 9 & 11              | 3 & 6               | 10 & 11             | 2 & 8               | 11 & 12             |
| 2 & 8                | 10 & 11             | 2 & 8               | 11 & 12             | 3 & 6               | 11 & 12             |
| 4 & 5                | 10 & 11             | 4 & 5               | 11 & 12             | 4 & 5               | 11 & 12             |
| 3 & 7                | 11 & 12             |                     |                     |                     |                     |
