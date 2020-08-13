---
layout: single
classes: wide
title:  "Polscy raperzy i raperki. Ile słów używają? Czy używają dużo słów? Przekonajmy się!"
date:   2020-08-13 20:00:00 +0200
categories: ranking-raperów
---
![open graph](/assets/ranking-raperow2/header_albums.jpg)
---
W tym poście zajmę się zasobem słów polskich MC, albo raczej jak dużo zdecydowali się użyć pisząc swoje teksty. 

------

Wzorując się na [podobnym porównaniu dla amerykańskich raperów][rappers-sorted] podsumowałem ilościowo teksty około setki polskich raperów i paru raperek. Żeby wyniki były porównywalne liczbę unikalnych słów policzyłem ograniczając się do pierwszych 10, 20 i 30 tys. słów, poczynając od najwcześniejszych utworów (wg datu wydania albumu).

Użyłem [słownik polskich leksemów][polimorfologik] żeby sprowadzić różne odmiany jednego słowa do podstawowej formy, czyli policzyć np. "mamy" i "mają" jako jedno słowo - "mieć". Oczywiście "mamy" to może być też liczba mnoga od "mama" i zliczając słowa bez brania pod uwagę kontekstu nie wiem jakie słowo autor miał na myśli. Dlatego dla słów gdzie pojawiał się konflikt, podstawową formę wybierałem na dwa sposoby:
1. W pierwszym wybierałem formę, która powtarzała się w zbiorze najczęściej.
2. W drugim dla danego słowa z konfliktem wybierałem najrzadszą formę i usuwałem ją z listy leksemów w pozostałych słowach. Następnie powtarzałem to dla kolejnych słów, aż dla każdego pozostał jednoznaczny wybór. Ta iteracyjna procedura była intensywna obliczeniowo, ale wydaje mi się, że konieczna żeby wykorzystać wszystkie mozliwości.

Poniżej przykład czterech słów, które mogą być formą od 1 do 4 leksemów:


|	| słowo        | leksemy           | wybór do dolnego ograniczenia  | wybór do górnego ograniczenia |
|:---- | -------------|:------------      | -----:                         | -----:|
| 1.   | mamy         | mieć, mama        | mieć                           | mama      |
| 2.   | mają         | mieć, maić, maja  | mieć                           | maja      |
| 3.   | mają         | mieć, maić, maja  | mieć                           | maić      |
| 4.   | mają         | mieć, maić, maja  | mieć                           | mieć      |

Prawdziwa liczba unikalnych słów powinna mieścić się pomiędzy wartościami policzonymi tymi dwoma sposobami, przynajmniej dla tej częsci tekstu, która odnalazła się w słowniku. Słowa spoza słownika nie mogły zostać sprowadzone do swojej podstawowej formy tym sposobem, dlatego im mniejszy udział tekstu odnalazł się w słowniku, tym bardziej liczba leksemów będzie zawyżona. Na wykresach poniżej uszeregowałem raperów po zwykłej liczbie unikalnych słów (na czerwono), z zaznaczonym zakresem leksemów (ze środkiem przedziału na żółto).

<div class="tabset">
  <!-- Tab 1 -->
  <input type="radio" name="tabset" id="tab1" aria-controls="10k">
  <label for="tab1">W 10 tys. słowach</label>
  <!-- Tab 2 -->
  <input type="radio" name="tabset" id="tab2" aria-controls="20k" checked>
  <label for="tab2">W 20 tys. słowach</label>
  <!-- Tab 3 -->
  <input type="radio" name="tabset" id="tab3" aria-controls="30k">
  <label for="tab3">W 30 tys. słowach</label>
  
  <div class="tab-panels">
    <section id="10k" class="tab-panel">
	<iframe src="/assets/ranking-raperow2/plot_10k.html"
	    sandbox="allow-same-origin allow-scripts"
	    width="850"
	    height="1900"
	    scrolling="no"
	    seamless="seamless"
	    frameborder="0">
	</iframe>
  </section>
    <section id="20k" class="tab-panel">
	<iframe src="/assets/ranking-raperow2/plot_20k.html"
	    sandbox="allow-same-origin allow-scripts"
	    width="850"
	    height="1520"
	    scrolling="no"
	    seamless="seamless"
	    frameborder="0">
	</iframe>
    </section>
    <section id="30k" class="tab-panel">
	<iframe src="/assets/ranking-raperow2/plot_30k.html"
	    sandbox="allow-same-origin allow-scripts"
	    width="850"
	    height="1200"
	    scrolling="no"
	    seamless="seamless"
	    frameborder="0">
	</iframe>
    </section>
  </div>
  
</div>




#### L.U.C. i Słoń na czele

Dwaj artyści o różnych stylach wyraźnie prowadzą w tym zestawieniu. L.U.C. słynie z tworzenia neologizmów i bawienia się językiem.  
Słoń natomiast jest czołowym przedstawicielem [horrorcore'u][horrorcore]. W utworach, które są utrzymane w tej stylistyce, buduje makabryczny klimat przy pomocy m.in. barwnego słownictwa. Duży wpływ na wysoki wynik ma też fakt, że te utwory często nie mają refrenu, hooka ani w zasadzie żadnych powtórzeń, są po prostu rapowanymi opowieściami o śmierci, krwi, szatanie, itp. 


#### donGURALesko

Jego wysoka pozycja zaskoczyła mnie początkowo, bo kojarzyłem jego muzykę z imprezowym stylem, a teksty ze śmiesznym [braggadocio]. Nie ma tu jednak sprzeczności, bo bragga to także popisywanie się bogatym słownictwem. Poniżej jeden z kawałków, który podbił mu wynik:

{% include video id="SYGmXSc7DiA" provider="youtube" %}

#### Ten Typ Mes

> Gdybym mógł być Supermanem jeden dzień  
> Usunąłbym wtedy to frajerstwo w cień  
> Ale nie mogę, niech zastąpi to słów zasób  
> Chcesz być Kombii czy Republiką naszych czasów?  

Piotr Szmidt, czyli Mes poza pisaniem swoich tekstów jest także autorem felietonów, a ostatnio napisał książkę. Wygląda, że słusznie kiedyś chwalił się zasobem słów. 

#### Łona poza czołówką - czy to błąd?

Łona jest bez wątpienia oczytanym raperem, który wyróżnia się przemyślanymi tekstami. Dlaczego więc w tym rankingu nie ma go w czołówce? Jedną z przyczyn mogą być powtórzenia, które często pojawiają się u niego jako zabieg stylistyczny, który pomaga coś zaakcentować. Najlepsze przykłady jakie znalazłem to słowo "gdyby" w "Gdzie Tak Pięknie" oraz tytułowe "Nie pytaj nas":

{% include video id="ZVguWNI7RPs" provider="youtube" %}

#### Wdowa

Jedyna raperka, która się tu załapała wylądowała między Grubsonem a Tedem. Dla innych kobiet (Lilu, Adma, Guova) nie udało mi się pobrać dosyć tekstów, by przebić próg 10 tys. słów. 

#### Nowe pokolenie na końcu rankingu

Twórcy z najmniejszymi wynikami to głównie debiutanci z ostatnich lat. Odzwierciedla to trendy zza oceanu, w nowym rapie jest więcej powtórzeń, mniej storytellingu.

Poniżej raperzy na osi czasu według daty ich pierwszego wydawnictwa (które jest na Spotify, przez braki i reedycje, część raperów ze środka powinno być dalej na lewo).

<iframe src="/assets/ranking-raperow2/plot_uq_words_per_debut.html"
	    sandbox="allow-same-origin allow-scripts"
	    width="1000"
	    height="800"
	    scrolling="no"
	    seamless="seamless"
	    frameborder="0">
</iframe>



[rappers-sorted]: https://pudding.cool/projects/vocabulary/
[polimorfologik]: https://github.com/morfologik/polimorfologik
[horrorcore]: https://pl.wikipedia.org/wiki/Horrorcore
[braggadocio]: https://pl.wikipedia.org/wiki/Braggadocio

