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

<img src="./bubble Sort.png" alt="Bubble Sort Block Scheme" style='width: 50%'/>

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

```c

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

void tabGen(int *tab, int n);
void quick_sort(int *tab, int lewy, int prawy);

int main(void) {
    int n, *tab;
    srand((unsigned int)time(NULL));

    printf("Podaj wielkosc tablicy: ");
    scanf("%d", &n);
    
    tab = malloc(sizeof(n));

    printf("\nWygenerowana tablica to: \n");
    tabGen(tab, n);

    printf("\nPosortowana tablica to: \n");
    quick_sort(tab, 0, n-1);
    for (int i = 0; i < n; i++) {
        printf("%d ", tab[i]);
    }

    return 0;
}

void tabGen(int *tab, int n) {
    for (int i = 0; i < n; i++){
        tab[i] = rand() % 100 + 1;
        printf("%d ", tab[i]);
    }
}

void quick_sort(int *tab, int poczatek, int koniec) {
    int p, q, pivot, pomocnicza;
    if (poczatek >= koniec)
        return;
    p = poczatek -1;
    q = koniec + 1;
    pivot = tab[(poczatek + koniec) / 2];

    while (1) {
        while (pivot > tab[++p])
            ;
        while (pivot < tab[--q])
            ;
        if (p <= q) {
            pomocnicza = tab[p];
            tab[p] = tab[q];
            tab[q] = pomocnicza;
        } else 
            break;
        
    }

    if (q > poczatek)
        quick_sort(tab, poczatek, q);
    if (p < koniec)
        quick_sort(tab, p, koniec);
}

```

___


__Carpye & [@Verti1234]('https://github.com/verti1234')__
