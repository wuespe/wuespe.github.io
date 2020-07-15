---
layout: single
classes: wide
title:  "Próba ilościowej lustracji słów bez spacji, w celu literackiej MC gradacji (z ilustracjami)"
date:   2020-07-02 20:20:00 +0200
categories: ranking-raperów
image: /assets/ranking-raperow/ranking_cropped.png
---

Znalazłem kiedyś ciekawy post o tym ile słów używają amerykańscy raperzy ([The Largest Vocabulary In Hip Hop][rappers-sorted]) i postanowiłem że zrobię coś takiego dla polskich. Ściągnąłem dane ze Spotify, teksty z Geniusa, połączyłem je ze słownikiem i zorientowałem się, że mogę policzyć z tego jeszcze parę innych rzeczy.  
Użyłem słownika z projektu [PoliMorfologik][polimorfologik], który zawiera kilka milionów odmienionych wyrazów z ich nieodmienioną formą (leksemem). Dołączyłem do tego zbiór wyrazów sklasyfikowanych do jednej z 5 emocji ([Nencki Affective Word List][nawl]) i na koniec pół-automatycznie oznaczyłem wulgarne słowa (wyszło mi ponad 6 tys. przekleństw!).  
Przy pomocy tego rozszerzonego słownika mogę podsumować utwór/album/rapera kilkoma miarami.  
Znalazłem ciekawe rzeczy i wciąż jeszcze grzebię w tych danych, więc zrobię z tego projektu pewnie kilka postów.  
W tym popatrzę na to jaka część tekstów znalazła się w słowniku, ile jest w nich wulgaryzmów i jak gęsto jest od słów.


<iframe src="/assets/ranking-raperow/bokeh_plots/plot_dictshare.html"
    sandbox="allow-same-origin allow-scripts"
    width="800"
    height="1350"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>

Albumy, dla których znalazłem wystarczająco dużo tekstów, z wyborem rapera.

<iframe src="/assets/ranking-raperow/bokeh_plots/albums_vulg_vs_speed.html"
    sandbox="allow-same-origin allow-scripts"
    width="950"
    height="1000"
    scrolling="no"
    seamless="seamless"
    frameborder="0">
</iframe>


[rappers-sorted]: https://pudding.cool/projects/vocabulary/
[polimorfologik]: https://github.com/morfologik/polimorfologik
[nawl]: https://lobi.nencki.gov.pl/research/18/


