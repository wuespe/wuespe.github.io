---
layout: single
classes: wide
title:  "Próba ilościowej lustracji słów bez spacji, w celu literackiej MC gradacji (z ilustracjami)"
date:   2020-07-02 20:20:00 +0200
categories: ranking-raperów
header.image: /assets/ranking-raperow/ranking_cropped.png
---

![open graph](/assets/ranking-raperow/ranking_cropped.png)

Znalazłem kiedyś ciekawy post o tym ile słów używają amerykańscy raperzy ([The Largest Vocabulary In Hip Hop][rappers-sorted]) i postanowiłem że zrobię coś takiego dla polskich. Ściągnąłem dane ze Spotify, teksty z Geniusa, połączyłem je ze słownikiem i zorientowałem się, że mogę policzyć z tego jeszcze parę innych rzeczy.  


Użyłem słownika z projektu [PoliMorfologik][polimorfologik], który zawiera kilka milionów odmienionych wyrazów z ich nieodmienioną formą (leksemem). Dołączyłem do tego zbiór wyrazów sklasyfikowanych do jednej z 5 emocji ([Nencki Affective Word List][nawl]) oraz pół-automatycznie oznaczyłem wulgarne słowa (wyszło mi ponad 6 tys. przekleństw!).  
Przy pomocy tego rozszerzonego słownika podsumowałem albumy i raperów kilkoma miarami. Pogrzebałem w wynikach i znalazłem nieco ciekawych rzeczy i wciąż jeszcze grzebię, więc zrobię z tego projektu pewnie kilka postów! :)  

W tym popatrzę ile jest wulgaryzmów i jak gęste w słowa są utwory polskich raperów. 

# Stopień dopasowania do słownika 
Zacznę od tego jaka część tekstów się w ogóle odnalazła w słowniku. Dlaczego nie wszystko się odnalazło? Są 3 możliwości:
  * W słowniku nie ma każdego polskiego słowa. Zbiór jest ogromny, ale zdarza się że braknie wyrazu,
  * Literówki,
  * Autor tekstu z premedytacją posłużył się słowem, które oficjalnie nie jest częścią języka polskiego (przynajmniej póki co).

Ze względu na ostatni punkt różnice między raperami są interesujące. Poniżej najbardziej i najmniej słownikowi raperzy:

<iframe src="/assets/ranking-raperow/bokeh_plots/plot_dictshare.html"
    sandbox="allow-same-origin allow-scripts"
    width="800"
    height="1350"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Widać tu podział na oldschool i newschool. W topie są reprezentanci pierwszego pokolenia raperów, wysoko jest Molesta i Włodi, Grammatik (Eldo nieco niżej ale także z >96%). Na drugim końcu młodsi raperzy, którzy w swoich tekstach częściej używają zapożyczeń z obcych języków i slangu, który nie zdążył wejść do słownika. Malik Montana ma całe zwrotki po niemiecku, pozostali najczęściej słowa albo zwroty z angielskiego, Tuzza czasem też z włoskiego.

# Za szybcy za wulgarni

Raperzy, podzieleni na 3 okresy według daty wydania pierwszej płyty.

<iframe src="/assets/ranking-raperow/bokeh_plots/artists_vulg_vs_speed.html"
    sandbox="allow-same-origin allow-scripts"
    width="800"
    height="800"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Tutaj same płyty:

<iframe src="/assets/ranking-raperow/bokeh_plots/albums_vulg_vs_speed.html"
    sandbox="allow-same-origin allow-scripts"
    width="800"
    height="800"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Płyty z wyborem rapera

<iframe src="/assets/ranking-raperow/bokeh_plots/albums_vulg_vs_speed_choice.html"
    sandbox="allow-same-origin allow-scripts"
    width="950"
    height="1100"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>



[rappers-sorted]: https://pudding.cool/projects/vocabulary/
[polimorfologik]: https://github.com/morfologik/polimorfologik
[nawl]: https://lobi.nencki.gov.pl/research/18/


