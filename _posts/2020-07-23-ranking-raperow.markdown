---
layout: single
classes: wide
title:  "Próba ilościowej lustracji słów bez spacji, w celu literackiej MC gradacji (z ilustracjami)"
date:   2020-07-23 17:00:00 +0200
categories: ranking-raperów
header.image: /assets/ranking-raperow/ranking_cropped.png
---

![open graph](/assets/ranking-raperow/ranking_cropped.png)
---
Znalazłem kiedyś ciekawy post o tym ile słów używają amerykańscy raperzy ([The Largest Vocabulary In Hip Hop][rappers-sorted]) i postanowiłem że zrobię coś takiego dla polskich. Ściągnąłem dane ze Spotify, teksty z Geniusa, połączyłem je ze słownikiem i przyszło mi w międzyczasie do głowy parę innych pomysłów na podsumowanie raperów i ich płyt. Chcę je opisać w paru postach, a w tym popatrzę ile jest wulgaryzmów i jak gęste w słowa są utwory polskich raperów.

------

Do przeanalizowania wybrałem nieco arbitralnie raperów, których znam albo są popularni. Pobrałem ich dyskografię przez API Spotify, przez co na wstępie ograniczyłem się do artystów którzy są tam z w miarę kompletnym dorobkiem. Jeśli zauważyłem jakieś istotne braki albo błędy, które musiałbym poprawiać i uzupełniać ręcznie to na razie wukluczałem raperów, których to dotyczy. Zamierzam kiedyś rozszerzyć listę artystów o tych pominiętych, a także tych, których nie da się tam streamować. Teksty ściągnąłem z Genius.com przy pomocy pakietu [LyricsGenius][lyricsgenius].  

Użyłem słownika z projektu [PoliMorfologik][polimorfologik], który zawiera kilka milionów odmienionych wyrazów z ich nieodmienioną formą (leksemem). Dołączyłem do tego zbiór wyrazów sklasyfikowanych do jednej z 5 emocji ([Nencki Affective Word List][nawl]) oraz pół-automatycznie oznaczyłem wulgarne słowa (wyszło mi ponad 6 tys. przekleństw!).  

## Stopień dopasowania do słownika 
Zacznę od tego jaka część tekstów się w ogóle odnalazła w słowniku. Dlaczego nie wszystko się odnalazło? Są 3 możliwości:
  * nie każde polskie słowo jest w tym słowniku, mimo że zbiór jest ogromny,
  * literówki,
  * autor tekstu świadomie posłużył się słowem, które nie jest obecnie częścią języka polskiego.
  
Dwa pierwsze punkty są mniej więcej losowe, także trzeci punkt powinien być główną przyczyną różnic między raperami. Poniżej najbardziej i najmniej słownikowi raperzy:

<iframe src="/assets/ranking-raperow/bokeh_plots/plot_dictshare.html"
    sandbox="allow-same-origin allow-scripts"
    width="850"
    height="1300"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Widać tu, z paroma wyjątkami, różnicę pokoleniową. W topie są oldskulowi raperzy, w swoich grupach i solo, np. Molesta i Włodi albo Grammatik i Eldo (który jest nieco niżej ale także z >96%). Wykluczyłem z zestawienia Afront i Mor W.A., którzy byliby na 2. i 1. miejscu, ale na podstawie zaledwie kilku utworów.  
Na drugim końcu głównie młodsi raperzy, którzy w swoich tekstach częściej używają zapożyczeń z angielskiego albo slangu, który nie zdążył wejść do słownika. Wśród nich:
- Malik Montana - poza wersami po angielsku ma całe zwrotki po niemiecku, 
- Tuzza Globale - wtrącają też czasem trochę włoskiego,
- Liroy - mam niewiele jego utworów w zbiorze i jest duża szansa że próbka nie jest reprezentatywna dla jego twórczości, ale słowa *Scoobie doobie doo ya* stanowią tu ponad 3% jego tekstów.

## Za szybcy za wulgarni

Teraz mogę przejść do tempa rapowania i zawartości wulgaryzmów. Umieściłem je na dwóch osiach żeby zobaczyć czy korelują ze sobą.

Pogrupowałem artystów na 3 okresy według daty wydania pierwszej płyty. Niestety na Spotify czasem nie ma dawnych albumów, albo są reedycje zamiast oryginałów, stąd jest tu parę niezgodności.

<iframe src="/assets/ranking-raperow/bokeh_plots/artists_vulg_vs_speed.html"
    sandbox="allow-same-origin allow-scripts"
    width="850"
    height="700"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Mimo, że piszę o szybkości albo tempie rapowania to nie do końca celne określenie. Policzyłem je dzieląc liczbę słów przez długość utworu (wersji na Spotify), więc można powiedzieć że to gęstość słów na sekundę utworu. Długie instrumentalne intra, outra i przerywniki albo śpiewane hooki będą zaniżać tę liczbę, więc jest to miara w pewien sposób powiązana ze stylem.

Poniżej albumy zaznaczonych raperów, zredukowane do dwóch wymiarów.

<iframe src="/assets/ranking-raperow/bokeh_plots/albums_vulg_vs_speed_choice.html"
    sandbox="allow-same-origin allow-scripts"
    width="970"
    height="1100"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

- *Slums Attack* - reedycja pierwszej płyty Peji z 1996 roku ma najwięcej przekleństw w tym zbiorze z wynikiem 4.5%, czyli jeden bluzg na jakieś 2-3 wersy. Jego pozostałe albumy są przynajmniej dwa razy mniej wulgarne.
- Tede ma w tym dwuwymiarowym rzucie duży rozrzut, większy niż podobnie płodni i długo aktywni twórcy jak O.S.T.R. i Peja.
- Łona, podobnie jak Peja, pierwszy album ma wulgarniejszy od późniejszych, ale na mniejszą skalę.
- Zaznacz Hemp Gru, Jana-Rapowanie, Paktofonikę i Quebonafide żeby zobaczyć hulajnogę. Dodaj PIHa żeby zrobić z niej skuter. 


[rappers-sorted]: https://pudding.cool/projects/vocabulary/
[polimorfologik]: https://github.com/morfologik/polimorfologik
[nawl]: https://lobi.nencki.gov.pl/research/18/
[lyricsgenius]: https://github.com/johnwmillr/LyricsGenius

