Wnioski:

Obserwacje poszczególnych hiperparametrów na podstawie kilkudzięsieciu uruchomień algorytmu dla różnych wartości hiperparametrów:

- generations - im większa liczba tym lepsze wyniki na ogół, ale od wartości 100 (ewentualnie do 200 ale te różnice też nie są zbyt zauważalne) nie ma sensu zwiększać liczby generacji,
bo większa liczba nie wpływa już zbytnio na wyniki a spowalnia działania algorytmu.

- population_size - im większa populacja tym większa różnorodność, a za tym powinny być dokładniejsze wyniki,
ale nie ma sensu za bardzo spowalniać programu, gdy zmiany nie są zauważalne już po około 50 osobnikach.

- crossover_rate - każda wartość z danego przedziału 0.8-0.95 daje całkiem dobre wyniki, ale dla wartości 0.9 wyniki są najlepsze

- mutation_rate - dobre wyniki są dla wartosci 0.1, dla mniejszych wartości mutacje mogą zachodzić zbyt rzadko,
a dla większych mogą zachodzić zbyt drastyczne zmiany w ciągu jednej generacji.

- mutation_range - wartość 0.3 jest dobra, dla mniejszych zmiany mogą być zbyt małe przez co nie zdąży zbiec do minimum, a dla większych zazwyczaj kilku osobników zbiega do minimum, ale duża cześć przeskakuje minimum i znajduje się ostatecznie z dala od niego.

Z moich obserwacji wynika że całkiem dobrymi parametrami, wystarczającymi by całkiem dokładnie oszacować wyniki są:
- generations = 100
- population_size = 50
- crossover_rate = 0.85
- mutation_rate = 0.1
- mutation_range = 0.3

Wpływ hiperparametrów na to do którego minimum będzie zbiegał algorytm (współrzędne f1):

1. Prawdopodobieństwo mutacji nie wpływa za bardzo na to do którego minimum funkcja f1 będzie zbiegać.
2. Prawdopodobieństwo krzyżowania nie wpływa za bardzo na to do którego minimum funkcja f1 będzie zbiegać.
3. Rozkład normalny podany w zadaniu i jednorodny na całym obszarze nie ma wpływu na to do którego minimum funkcja f1 będzie zbiegać.
4. Gdyby wartości wokół których tworzymy populacji początkową rozkładem normalnym były bliżej ktoregoś z minimów to algorytm zbiegałby do tego minimum.