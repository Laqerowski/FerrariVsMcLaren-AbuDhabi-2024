# Ferrari vs McLaren Abu Dhabi 2024

## Opis projektu

Projekt ten jest predykcją możliwych miejsc, które dają mistrzostwo konstruktorów Ferrari w walce przeciwko McLarenowi w najbliższym wyścigu odbywającym się w Abu Zabi.  
Znajduje się w nim kod, który:
- Generuje miejsca na mecie wyścigu.
- Sprawdza wyniki pod kątem spełnienia warunków mistrzostwa.
- Przesiewa wyniki do prostych tabel z przypisanymi miejscami oraz punktami.

Projekt ten wykorzystuje biblioteki:
- **Pandas**: do przetwarzania danych i generowania tabel.
- **Itertools**: do tworzenia kombinacji i permutacji miejsc.

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
<table style="width:100%; border-collapse:collapse; text-align:center; border: 1px solid black;">
    <thead>
        <tr>
            <th colspan="2" style="border: 1px solid black;">Ferrari</th>
            <th colspan="2" style="border: 1px solid black;">Nikt</th>
            <th colspan="2" style="border: 1px solid black;">McLaren</th>
        </tr>
        <tr>
            <th style="border: 1px solid black;">Pozycja Ferrari</th>
            <th style="border: 1px solid black;">Pozycja McLarena</th>
            <th style="border: 1px solid black;">Pozycja Ferrari</th>
            <th style="border: 1px solid black;">Pozycja McLarena</th>
            <th style="border: 1px solid black;">Pozycja Ferrari</th>
            <th style="border: 1px solid black;">Pozycja McLarena</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>1 & 2</td><td>4 & 5</td><td>1 & 2</td><td>4 & 5</td><td>1 & 2</td><td>4 & 6</td></tr>
        <tr><td>1 & 3</td><td>4 & 6</td><td>1 & 3</td><td>5 & 6</td><td>1 & 3</td><td>5 & 6</td></tr>
        <tr><td>1 & 4</td><td>5 & 7</td><td>1 & 4</td><td>5 & 7</td><td>1 & 4</td><td>6 & 7</td></tr>
        <tr><td>1 & 5</td><td>6 & 7</td><td>1 & 5</td><td>6 & 7</td><td>1 & 5</td><td>6 & 8</td></tr>
        <tr><td>2 & 3</td><td>6 & 8</td><td>1 & 7</td><td>6 & 9</td><td>2 & 3</td><td>7 & 8</td></tr>
        <tr><td>1 & 7</td><td>6 & 9</td><td>2 & 3</td><td>7 & 8</td><td>1 & 6</td><td>7 & 8</td></tr>
        <tr><td>1 & 6</td><td>7 & 8</td><td>1 & 6</td><td>7 & 8</td><td>1 & 8</td><td>7 & 10</td></tr>
        <tr><td>1 & 8</td><td>7 & 9</td><td>1 & 8</td><td>7 & 9</td><td>1 & 7</td><td>8 & 9</td></tr>
        <tr><td>2 & 4</td><td>7 & 9</td><td>2 & 4</td><td>7 & 9</td><td>2 & 4</td><td>8 & 9</td></tr>
        <tr><td>1 & 9</td><td>7 & 10</td><td>2 & 5</td><td>8 & 9</td><td>1 & 9</td><td>8 & 10</td></tr>
        <tr><td>1 & 10</td><td>8 & 9</td><td>1 & 9</td><td>8 & 10</td><td>2 & 5</td><td>8 & 10</td></tr>
        <tr><td>2 & 5</td><td>8 & 9</td><td>3 & 4</td><td>8 & 10</td><td>1 & 10</td><td>8 & 11</td></tr>
        <tr><td>3 & 4</td><td>8 & 9</td><td>1 & 10</td><td>8 & 11</td><td>1 & 11</td><td>9 & 10</td></tr>
        <tr><td>1 & 11</td><td>8 & 10</td><td>1 & 11</td><td>9 & 10</td><td>2 & 6</td><td>9 & 10</td></tr>
        <tr><td>2 & 6</td><td>8 & 10</td><td>2 & 6</td><td>9 & 10</td><td>3 & 4</td><td>9 & 10</td></tr>
        <tr><td>2 & 7</td><td>9 & 10</td><td>3 & 5</td><td>9 & 10</td><td>3 & 5</td><td>9 & 11</td></tr>
        <tr><td>3 & 5</td><td>9 & 10</td><td>2 & 7</td><td>9 & 11</td><td>2 & 7</td><td>10 & 11</td></tr>
        <tr><td>3 & 6</td><td>9 & 11</td><td>3 & 6</td><td>10 & 11</td><td>2 & 8</td><td>11 & 12</td></tr>
        <tr><td>2 & 8</td><td>10 & 11</td><td>2 & 8</td><td>11 & 12</td><td>3 & 6</td><td>11 & 12</td></tr>
        <tr><td>4 & 5</td><td>10 & 11</td><td>4 & 5</td><td>11 & 12</td><td>4 & 5</td><td>11 & 12</td></tr>
        <tr><td>3 & 7</td><td>11 & 12</td><td></td><td></td><td></td><td></td></tr>
    </tbody>
</table>



