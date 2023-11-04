Wnioski:

Obserwacje poszczególnych hiperparametrów:

- generations - im większa liczba tym lepsze wyniki, wykresy wskazywałyby, że od 70 nie ma sensu zwiększać liczby generacji, ale wtedy zmniejsza się poprawność innych parametrów, więc bezpieczną i optymalną liczbą jest 200,
bo większa liczba nie wpływa to zbytnio na wyniki a spowalnia działania algorytmu.

- population_size - im większa populacja tym większa różnorodność, a za tym powinny być dokładniejsze wyniki,
ale nie ma sensu za bardzo spowalniać programu, gdy zmiany nie są zauważalne już po około 50 osobnikach.

- crossover_rate - dla dystybucji losowej najlepszy jest w od 0.8 do 0.84 (dla większych wartości wyniki są gorsze), a
dla rozkładu normalnego wyniki ogólnie są nie za dobre, ale najlepsze są dla wartości 0.87.

- mutation_rate - dobre wyniki są dla wartosci 0.1, dla mniejszych wartości mutacje zachodzą zbyt rzadko,
a dla większych mogą zachodzić zbyt drastyczne zmiany w ciągu jednej generacji.

- mutation_range - wartość 0.7 jest dobra, dla mniejszych zmiany mogą być zbyt małe przez co nie zdąży zbiec do minimum, a dla większych zbyt duże mogą powodować przeskoki przez minimum, ewentualnie dla o wiele za dużych wartości może zacząć zbiegać do innego minimum.

Z moich obserwacji wynika że całkiem dobrymi parametrami, wystarczającymi by całkiem dokładnie oszacować wyniki są:
- generations = 200
- population_size = 50
- crossover_rate = 0.90
- mutation_rate = 0.1
- mutation_range = 0.7

Wpływ hiperparametrów na to do którego minimum będzie zbiegał algorytm (współrzędne f1):

1. Prawdopodobieństwo mutacji nie wpływa za bardzo na to do którego minimum funkcja f1 będzie zbiegać.
2. Prawdopodobieństwo krzyżowania nie wpływa za bardzo na to do którego minimum funkcja f1 będzie zbiegać.
3. Rozkład normalny podany w zadaniu i jednorodny na całym obszarze nie ma wpływu na to do którego minimum funkcja f1 będzie zbiegać.
4. Gdyby wartości wokół których tworzymy populacji początkową rozkładem normalnym były bliżej ktoregoś z minimów to algorytm zbiegałby do tego minimum.