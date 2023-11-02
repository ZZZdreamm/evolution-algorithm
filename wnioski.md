Wnioski:

Z moich obserwacji wynika że całkiem dobrymi parametrami, wystarczającymi by całkiem dokładnie oszacować wyniki są:
- generations = 400 - powyżej 200 jest całkiem dobry
- population_size = 45 - powyżej 40 nie wpływa zbytnio na wyniki
- crossover_rate = 0.85 - powyżej 0.8 jest całkiem dobry
- mutation_rate = 0.05 - poniżej 0.1 jest całkiem dobry
- mutation_range = 0.3 - prawie dowolny jeśli poniżej 1

1. Prawdopodobieństwo mutacji nie wpływa za bardzo na to do którego minimum funkcja f1 będzie zbiegać.
2. Prawdopodobieństwo krzyżowania nie wpływa za bardzo na to do którego minimum funkcja f1 będzie zbiegać.
3. Rozkład normalny podany w zadaniu i jednorodny na całym obszarze nie ma wpływu na to do którego minimum funkcja f1 będzie zbiegać.
4. Gdyby wartości wokół których tworzymy populacji początkową rozkładem normalnym były bliżej ktoregoś z minimów to algorytm zbiegałby do tego minimum.