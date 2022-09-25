# Sorting Algorithms

---

### Bubble Sort

1. Rozpocznij proces.
2. Podaj listę.
3. Spójrz na pierwszy element listy.
4. Jeśli następna liczba jest mniejsza od obecnej, zamień miejscami te dwie liczby.
5. Przejdź do następnego pozycji na liście i zrób z niej obecną.
6. Powtarzaj krok 4 dopóki obecna liczba nie bedzie na końcu listy.
7. Jeśli jakakolwiek liczba została zamieniona, przejdź do kroku 3.
8. Zakończ proces.

<img src="./BUBBLE SORT.png" alt="Bubble Sort Block Scheme" style='width: 50%'/>

___

### Quick Sort

1. Rozpocznij proces.
2. Wprowadź listę, i & j = 0, pivot = null.
3. Ustaw pivot na środkowy element tablicy. (ew. na element z mniejszym indexem w przypadku tablicy o parzystej długości)
4. Ustaw  i na 0 & j na wielkość tablicy - 1;
5. Zwiekszaj i, aż lista[i] > pivot.
6. Zmiejszaj j, aż lista[j] < pivot.
7. Jeśli i < j to zamień lista[i] z lista[j].
8. Powtarzaj kroki 4, 5, 6, aż i > j.
9. Zamień element pivot na element lista[j].

__Nie udało nam się zrobić schematu blokowego. Oto nasze starania.__

<img src='./Quick Sort.png' alt="Quick Sort" style='width: 50%'/>

___


##### Kacper Kozłowski i Krzysztof Godyń
