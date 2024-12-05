# Ferrari vs McLaren Abu Dhabi 2024

## Opis projektu

Projekt ten jest predykcją możliwych miejsc, które dają mistrzostwo konstruktorów Ferrari w walce przeciwko McLarenowi w najbliższym wyścigu odbywającym się w Abu Dhabi.  
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

### 1. McLaren na podium – to nie problem
McLaren może znaleźć się na podium w tym wyścigu. Ferrari jednak musi zdobyć dublet, inaczej będzie musiało liczyć na jeden z trzech scenariuszy:
- McLaren (2 & 9): Ferrari musi zdobyć najszybsze okrążenie, aby pozostać na prowadzeniu.
- McLaren (2 & 10): McLaren nie może zdobyć najszybszego okrążenia, aby Ferrari utrzymało przewagę.
- McLaren (2 & 11): Ferrari utrzyma przewagę nawet wtedy, gdy McLaren zdobędzie najszybsze okrążenie.


### 2. Najlepszy scenariusz dla Ferrari
Najbardziej optymistyczny scenariusz dla Ferrari to:
- Ferrari zdobywa dublet, a McLaren pozostaje poza podium i nie zdobywa najszybszego okrążenia.
- W przypadku, gdy McLaren zdobywa najszybsze okrążenie, dalszy bolid McLarena musi znaleźć się o jedną pozycję niżej, aby Ferrari utrzymało przewagę punktową.


### 3. Tylko jedno trofeum
Ferrari nadal może zdobyć tytuł mistrzowski, nawet jeśli nie znajdzie się na podium. Musi jednak liczyć na sytuację, w której oba bolidy McLarena znajdą się poza punktami. Jeśli jeden z bolidów McLarena zajmie 10. miejsce, Ferrari musi zdobyć najszybsze okrążenie, aby zachować przewagę punktową.


### 4. Wygrana przy jednym bolidzie Ferrari na mecie
Ferrari może zdobyć tytuł mistrza konstruktorów nawet wtedy, gdy tylko jeden ich bolid ukończy wyścig. Warunki, które muszą być spełnione:
- Ferrari musi wygrać wyścig.
- McLaren nie może zająć wyższej pozycji niż 9. miejsce, jeśli Ferrari nie zdobędzie najszybszego okrążenia.

Ten scenariusz pokazuje, jak istotna jest minimalizacja punktów zdobywanych przez McLarena.


### 5. Znaczenie najszybszego okrążenia

#### Zdobycie najszybszego okrążenia przez Ferrari:
- Dodaje dodatkową kombinację miejsc, która pozwala zespołowi na zwycięstwo w klasyfikacji konstruktorów.
- Ma wpływ na 3/4 kombinacji, umożliwiając jednemu bolidowi McLarena zajęcie o maksymalnie 1-2 wyższych pozycji w porównaniu z sytuacją, w której nikt nie zdobył najszybszego okrążenia.

#### Zdobycie najszybszego okrążenia przez McLaren:
- Ma wpływ na ponad połowę kombinacji, wymuszając, aby jeden z bolidów McLarena znalazł się o 1-2 miejsca niżej w porównaniu z sytuacją, w której nikt nie zdobył najszybszego okrążenia.

Zdobycie najszybszego okrążenia znacząco wpływa na końcowe wyniki, szczególnie w kombinacjach, w których McLaren znajduje się w drugiej połowie pierwszej dziesiątki lub nawet poza punktami.

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
  <tr>
    <td class="tg-0pky">1 &amp; 2</td>
    <td class="tg-0pky">3 &amp; 6</td>
    <td class="tg-0pky">1 &amp; 2</td>
    <td class="tg-0pky">3 &amp; 7</td>
    <td class="tg-0pky">1 &amp; 2</td>
    <td class="tg-0pky">3 &amp; 7</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 2</td>
    <td class="tg-0pky">4 &amp; 5</td>
    <td class="tg-0pky">1 &amp; 2</td>
    <td class="tg-0pky">4 &amp; 5</td>
    <td class="tg-0pky">1 &amp; 2</td>
    <td class="tg-0pky">4 &amp; 6</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 3</td>
    <td class="tg-0pky">2 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 3</td>
    <td class="tg-0pky">2 &amp; 10</td>
    <td class="tg-0pky">1 &amp; 3</td>
    <td class="tg-0pky">2 &amp; 11</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 3</td>
    <td class="tg-0pky">4 &amp; 6</td>
    <td class="tg-0pky">1 &amp; 3</td>
    <td class="tg-0pky">4 &amp; 7</td>
    <td class="tg-0pky">1 &amp; 3</td>
    <td class="tg-0pky">4 &amp; 7</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 4</td>
    <td class="tg-0pky">3 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 3</td>
    <td class="tg-0pky">5 &amp; 6</td>
    <td class="tg-0pky">1 &amp; 3</td>
    <td class="tg-0pky">5 &amp; 6</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 4</td>
    <td class="tg-0pky">5 &amp; 7</td>
    <td class="tg-0pky">1 &amp; 4</td>
    <td class="tg-0pky">3 &amp; 10</td>
    <td class="tg-0pky">1 &amp; 4</td>
    <td class="tg-0pky">3 &amp; 11</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 5</td>
    <td class="tg-0pky">3 &amp; 11</td>
    <td class="tg-0pky">1 &amp; 4</td>
    <td class="tg-0pky">5 &amp; 7</td>
    <td class="tg-0pky">1 &amp; 4</td>
    <td class="tg-0pky">5 &amp; 8</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 5</td>
    <td class="tg-0pky">4 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 5</td>
    <td class="tg-0pky">4 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 4</td>
    <td class="tg-0pky">6 &amp; 7</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 5</td>
    <td class="tg-0pky">6 &amp; 7</td>
    <td class="tg-0pky">1 &amp; 5</td>
    <td class="tg-0pky">6 &amp; 7</td>
    <td class="tg-0pky">1 &amp; 5</td>
    <td class="tg-0pky">4 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 6</td>
    <td class="tg-0pky">4 &amp; 10</td>
    <td class="tg-0pky">1 &amp; 6</td>
    <td class="tg-0pky">4 &amp; 11</td>
    <td class="tg-0pky">1 &amp; 5</td>
    <td class="tg-0pky">6 &amp; 8</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 6</td>
    <td class="tg-0pky">5 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 6</td>
    <td class="tg-0pky">5 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 6</td>
    <td class="tg-0pky">5 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 6</td>
    <td class="tg-0pky">7 &amp; 8</td>
    <td class="tg-0pky">1 &amp; 6</td>
    <td class="tg-0pky">7 &amp; 8</td>
    <td class="tg-0pky">1 &amp; 6</td>
    <td class="tg-0pky">7 &amp; 8</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 7</td>
    <td class="tg-0pky">5 &amp; 10</td>
    <td class="tg-0pky">1 &amp; 7</td>
    <td class="tg-0pky">5 &amp; 11</td>
    <td class="tg-0pky">1 &amp; 7</td>
    <td class="tg-0pky">6 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 7</td>
    <td class="tg-0pky">6 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 7</td>
    <td class="tg-0pky">6 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 7</td>
    <td class="tg-0pky">8 &amp; 9</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 8</td>
    <td class="tg-0pky">6 &amp; 10</td>
    <td class="tg-0pky">1 &amp; 8</td>
    <td class="tg-0pky">6 &amp; 11</td>
    <td class="tg-0pky">1 &amp; 8</td>
    <td class="tg-0pky">7 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 8</td>
    <td class="tg-0pky">7 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 8</td>
    <td class="tg-0pky">7 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 9</td>
    <td class="tg-0pky">8 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 9</td>
    <td class="tg-0pky">7 &amp; 10</td>
    <td class="tg-0pky">1 &amp; 9</td>
    <td class="tg-0pky">7 &amp; 11</td>
    <td class="tg-0pky">1 &amp; 10</td>
    <td class="tg-0pky">8 &amp; 11</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 10</td>
    <td class="tg-0pky">7 &amp; 11</td>
    <td class="tg-0pky">1 &amp; 9</td>
    <td class="tg-0pky">8 &amp; 10</td>
    <td class="tg-0pky">1 &amp; 11</td>
    <td class="tg-0pky">9 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 10</td>
    <td class="tg-0pky">8 &amp; 9</td>
    <td class="tg-0pky">1 &amp; 10</td>
    <td class="tg-0pky">8 &amp; 11</td>
    <td class="tg-0pky">2 &amp; 3</td>
    <td class="tg-0pky">5 &amp; 11</td>
  </tr>
  <tr>
    <td class="tg-0pky">1 &amp; 11</td>
    <td class="tg-0pky">8 &amp; 10</td>
    <td class="tg-0pky">1 &amp; 11</td>
    <td class="tg-0pky">8 &amp; 12</td>
    <td class="tg-0pky">2 &amp; 3</td>
    <td class="tg-0pky">6 &amp; 9</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 3</td>
    <td class="tg-0pky">4 &amp; 11</td>
    <td class="tg-0pky">1 &amp; 11</td>
    <td class="tg-0pky">9 &amp; 10</td>
    <td class="tg-0pky">2 &amp; 3</td>
    <td class="tg-0pky">7 &amp; 8</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 3</td>
    <td class="tg-0pky">5 &amp; 9</td>
    <td class="tg-0pky">2 &amp; 3</td>
    <td class="tg-0pky">5 &amp; 10</td>
    <td class="tg-0pky">2 &amp; 4</td>
    <td class="tg-0pky">7 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 3</td>
    <td class="tg-0pky">6 &amp; 8</td>
    <td class="tg-0pky">2 &amp; 3</td>
    <td class="tg-0pky">6 &amp; 9</td>
    <td class="tg-0pky">2 &amp; 4</td>
    <td class="tg-0pky">8 &amp; 9</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 4</td>
    <td class="tg-0pky">6 &amp; 10</td>
    <td class="tg-0pky">2 &amp; 3</td>
    <td class="tg-0pky">7 &amp; 8</td>
    <td class="tg-0pky">2 &amp; 5</td>
    <td class="tg-0pky">8 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 4</td>
    <td class="tg-0pky">7 &amp; 9</td>
    <td class="tg-0pky">2 &amp; 4</td>
    <td class="tg-0pky">6 &amp; 11</td>
    <td class="tg-0pky">2 &amp; 6</td>
    <td class="tg-0pky">9 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 5</td>
    <td class="tg-0pky">7 &amp; 10</td>
    <td class="tg-0pky">2 &amp; 4</td>
    <td class="tg-0pky">7 &amp; 9</td>
    <td class="tg-0pky">2 &amp; 7</td>
    <td class="tg-0pky">10 &amp; 11</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 5</td>
    <td class="tg-0pky">8 &amp; 9</td>
    <td class="tg-0pky">2 &amp; 5</td>
    <td class="tg-0pky">7 &amp; 11</td>
    <td class="tg-0pky">2 &amp; 8</td>
    <td class="tg-0pky">11 &amp; 12</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 6</td>
    <td class="tg-0pky">8 &amp; 10</td>
    <td class="tg-0pky">2 &amp; 5</td>
    <td class="tg-0pky">8 &amp; 9</td>
    <td class="tg-0pky">3 &amp; 4</td>
    <td class="tg-0pky">8 &amp; 11</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 7</td>
    <td class="tg-0pky">9 &amp; 10</td>
    <td class="tg-0pky">2 &amp; 6</td>
    <td class="tg-0pky">8 &amp; 11</td>
    <td class="tg-0pky">3 &amp; 4</td>
    <td class="tg-0pky">9 &amp; 10</td>
  </tr>
  <tr>
    <td class="tg-0pky">2 &amp; 8</td>
    <td class="tg-0pky">10 &amp; 11</td>
    <td class="tg-0pky">2 &amp; 6</td>
    <td class="tg-0pky">9 &amp; 10</td>
    <td class="tg-0pky">3 &amp; 5</td>
    <td class="tg-0pky">9 &amp; 11</td>
  </tr>
  <tr>
    <td class="tg-0pky">3 &amp; 4</td>
    <td class="tg-0pky">7 &amp; 11</td>
    <td class="tg-0pky">2 &amp; 7</td>
    <td class="tg-0pky">9 &amp; 11</td>
    <td class="tg-0pky">3 &amp; 6</td>
    <td class="tg-0pky">11 &amp; 12</td>
  </tr>
  <tr>
    <td class="tg-0pky">3 &amp; 4</td>
    <td class="tg-0pky">8 &amp; 9</td>
    <td class="tg-0pky">2 &amp; 8</td>
    <td class="tg-0pky">11 &amp; 12</td>
    <td class="tg-0pky">4 &amp; 5</td>
    <td class="tg-0pky">11 &amp; 12</td>
  </tr>
  <tr>
    <td class="tg-0pky">3 &amp; 5</td>
    <td class="tg-0pky">8 &amp; 11</td>
    <td class="tg-0pky">3 &amp; 4</td>
    <td class="tg-0pky">8 &amp; 10</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">3 &amp; 5</td>
    <td class="tg-0pky">9 &amp; 10</td>
    <td class="tg-0pky">3 &amp; 5</td>
    <td class="tg-0pky">9 &amp; 10</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">3 &amp; 6</td>
    <td class="tg-0pky">9 &amp; 11</td>
    <td class="tg-0pky">3 &amp; 6</td>
    <td class="tg-0pky">10 &amp; 11</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">3 &amp; 7</td>
    <td class="tg-0pky">11 &amp; 12</td>
    <td class="tg-0pky">4 &amp; 5</td>
    <td class="tg-0pky">11 &amp; 12</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-0pky">4 &amp; 5</td>
    <td class="tg-0pky">10 &amp; 11</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky"></td>
  </tr>
</tbody>
</table>



