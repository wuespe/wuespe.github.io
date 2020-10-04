---
layout: single
classes: wide
title:  "Problem z liczeniem unikalnych słów w próbce tekstów"
date:   2020-09-16 22:00:00 +0200
categories: ranking-raperów
---

W poprzednim poście pokazałem liczbę unikalnych słów w pewnym wycinku tekstów raperów. Ten wycinek to było pierwsze N (dla N = 10k, 20k, 30k) słów z tekstów, które udało mi się pobrać z Geniusa i które były posortowane chronologicznie wg daty wydania albumu ze Spotify.  
Czyli w pierwszej kolejności używam najwcześniejszych tekstów żeby podsumować twórczość rapera.  
Innym podejściem które rozważałem było wylosowanie N słów ze zbioru wszystkich tekstów. Styl rapera i jego teksty często ewoluują, więc to podejście miałoby ten plus, że losowa próbka mogłaby reprezentować cały dorobek rapera z zachowaniem wymogu by porównywać ich między sobą na zbiorach tej samej wielkości.

Jest jednak poważny problem z liczeniem unikatów w losowej próbce - ta liczba będzie zawyżona.

Pokażę to na przykładzie 3 raperów z największym dorobkiem: OSTR-a, Peji i Tedego. Dla każdego z nich wybrałem 10 zbiorów zawierających 10 tysięcy słów na dwa sposoby:
* 10 razy wylosowałem 10-tysięczną próbkę ze zbioru pierwszych 100 tys. słów,
* podzieliłem pierwsze 100 tys. słów ich twórczości na 10 równych i rozłącznych wycinków (1. zbiór to słowa od 1 do 10000, 2. od 10001 do 20000, itd.).

Poniżej liczba unikatów w każdym 10 tysięcznym zbiorze jako punkt na wykresie.

{% include figure image_path="/assets/ranking-raperow3/uqN_per_source" caption="Po lewej liczba unikatów w próbkach, po prawej w wycinkach" %}

Rozrzut wartości jest większy dla wycinków niż dla losowych próbek, co wydaje mi się intuicyjne. To co mnie zaskoczyło to fakt, że próbki mają wyraźnie więcej unikalnych słów. Prawie żaden wycinek (poza jednym w przypadku Tedego) nie ma tylu unikatów co dowolna próbka. Dlaczego losowy podział działa w ten sposób? Dlaczego losowe próbki mają wyraźnie więcej unikatów?

Odpowiedź, którą się zadowoliłem, to większy asortyment różnych słów w pełnym zbiorze.

Policzyłem liczbę unikalnych słów w wycinkach w każdym rozmiarze. Poniżej widać, że dla wszystkich trzech raperów ta liczba nie przestaje rosnąć i dla 100 tys. słów unikatów wśród nich jest w okolicach 20 tysięcy.

{% include figure image_path="/assets/ranking-raperow3/uqN_perN" caption="Liczba unikatów rośnie coraz wolniej, ale nawet po 100k słów daleko do nasycenia" %}

Na przykładzie OSTRa - w żadnym 10-tysięcznym wycinku nie było więcej niż 4 tys. różnych słów, ale w zbiorze z którego wylosowałem próbki jest 20 tys. różnych słów do wyboru. Stąd wyższy wynik jest możliwy. Wpływ na niego mają oczywiście dwie wartości: zarówno rozmiar zbioru jak i liczba unikalnych wartości. Gdyby losować te próbki z np. 11 tysięcznego zbioru to wyniki nie mogłyby się tak drastycznie różnić. 

Żeby zobaczyć jaki to ma właściwie wpływ, wylosowałem 100 razy 10-tysięczną próbkę ze zbioru pierwszych 11 tysięcy wyrazów w tekstach OSTRa i policzyłem unikaty. Następnie to samo dla 12 tysięcy, 13, 14, i tak dalej, aż do pełnego zbioru. Wyniki przedstawiają się następująco:

<iframe src="/assets/ranking-raperow3/OSTR_uqN_in_samples.html"
	    sandbox="allow-same-origin allow-scripts"
	    width="1000"
	    height="900"
	    scrolling="no"
	    seamless="seamless"
	    frameborder="0">
</iframe>

Na górze liczba unikatów w zbiorze danej wielkości. W miarę zwiększania zbioru jest w nim więcej różnych słów, ale stosunek liczby unikatów do całości łagodnie spada.  
Na dole średnia liczba unikatów w 10-tysięcznej próbce wylosowanej ze zbioru o danej wielkości. Najpierw szybko rośnie, następnie wypłaszcza się, a potem coś dziwnego się dzieje, bo tymczasowo spada. 

Zobaczmy jak to wygląda u innych raperów.

#### Peja

<iframe src="/assets/ranking-raperow3/PEJA_uqN_in_samples.html"
	    sandbox="allow-same-origin allow-scripts"
	    width="1000"
	    height="900"
	    scrolling="no"
	    seamless="seamless"
	    frameborder="0">
</iframe>

Dla Peji średnio najwyższą liczbę unikatów dostałem losując ze zbiorów ok. 80 tys. wyrazów. Gdy przyjrzy się blisko tym wykresom w okolicach x=72k to widać skok na dolnym, a górny jest nieco bardziej stromy. Stromość albo pochodna krzywej na górnym wykresie to stosunek unikatów do całości w danym punkcie. Czyli między 72000 a 73000 słowem Peja dodał więcej nowych słów, niż w poprzedzającym tysiącu. Średnia z próbek wzrosła przez to trochę bardziej. 

#### Tede

<iframe src="/assets/ranking-raperow3/TEDE_uqN_in_samples.html"
	    sandbox="allow-same-origin allow-scripts"
	    width="1000"
	    height="900"
	    scrolling="no"
	    seamless="seamless"
	    frameborder="0">
</iframe>

U Tedego podobnie, unikaty w próbce osiągają szczyt, po czym zaczynają spadać.

Jak widać u każdego z tych 3 raperów, ta miara w pewnym momencie się stabilizuje i zaczyna spadać. U każdego dzieje się to w innym punkcie, więc może ma na to wpływ też zawartość nowych tekstów? Na pewno wpływa na to liczba słów, unikatów i stosunek tych dwóch liczb. Może nawet dałoby się znaleźć parametry rozkładu statystyk z próbkowania, w sensie wzór na tą średnią. 

Nie zamierzam tego dalej badać. Zadowolę się wnioskiem, że dwóch artystów lepiej nie porównywać po losowej próbce ich tekstów.

