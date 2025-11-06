# 2025/2026

Kurz **Programování na Nuselské** bude probíhat od 18. září 2025
a volně navazuje na kurz **začátečníci**. Je určen pro děti druhých
až pátých tříd libovolné základní školy s tím, že děti druhých
tříd musí mít absolvovaný kurz začátečníci, šikovní jedinci z
řad třetích či čtvrtých tříd mohou přijít i bez předchozího
vzdělání.

Cílem tohoto kurzu je pokračování v rozvoji systematického
myšlení, hlubší poznávání světa informační techniky
a osvojení si základů elektrotechniky.

Kurz bude probíhat 1x týdně, každý čtvrtek od 14:15 do 15:05
v počítačové učebně.

V kurzu budeme využívat robůtky [Cubetto](https://www.primotoys.com),
[Beebot](https://www.bee-bot.us/) i [Ozobot](https://ozobot.com/).
Později si představíme platformu [Micro:bit](https://microbit.org)
a s ní zabředneme trochu blíže k elektrotechnice. Kromě těchto
se budeme věnovat i práci na PC, kde se budeme učit programovat
pomocí vybraných kurzů na [code.org](https://www.code.org),
prostředí [scratch](https://scratch.mit.edu/) a dalších.
To vše proložíme tvůrčími aktivitami s papírem, kostkami a jinými
rekvizitami.

Cílem kurzu není vzdělat hotového programátora, ale rozvíjet logické
myšlení, algoritmizaci a jiné vlastnosti, které se dětem budou hodit
při studiu jakéhokoliv oboru.

Kurz bude organizován a veden [Lukášem Doktorem](../lectors/ldoktor)

## 1. hodina (2025-09-18)

<img align="right" src="pokrocili-1-01-html-small.jpg" data-full="pokrocili-1-01-html.jpg" style="height:85px" class="obrazek">

* Seznámení s prvním tématem - HTML stránky
* Ukázková stránka s různými prvky a hledání easter-eggů [zde](https://ldoktor.github.io/assets/html/)
  * Pokud rodiče dovolí, můžete hledat dále. Všechny easter-eggy nebyly ještě nalezeny
* Přihlášení do [code.org](https://www.code.org) pomocí hesel

## 2. hodina (2025-09-25)

<img align="right" src="pokrocili-1-02-html-small.jpg" data-full="pokrocili-1-02-html.jpg" style="height:85px" class="obrazek">

* [code.org](https://www.code.org)
  * Co jsou to tagy; některé jsme si vyzkoušeli použít
  * ``<head></head>`` - hlavička (obecné informace pro prohlížeč)
  * ``<body></head>`` - tělo (to co vidí uživatel)
  * ``<h1></h1>`` - (headding) velký nadpis (dále pak menší a menší pod-nadpisy `<h2><h3><h4>...`)
  * ``<p></p>`` - (paragraph) odstavec (html ignoruje mezery a entery při formátování)

## 3. hodina (2025-10-02)

* [code.org](https://www.code.org)
  * Opakovací hodina (pro nemocné)
* Ti kdož nepotřebovali opakovat se věnovali psaní všemi deseti, zonerai, skřítkům a podobným

## 4. hodina (2025-10-09)

<img align="right" src="pokrocili-1-04-code-small.jpg" data-full="pokrocili-1-04-code.jpg" style="height:85px" class="obrazek">

* [code.org](https://www.code.org)
  * Procvičování tagů nadpisu ``<h1>Nadpis</h1>``
  * Seznámení se seznamem ``<ul><li>prvek1</li><li>prvek2</li></ul>``
  * Zlepšování se v odhalování chyb (začnu jeden tag, ukončím jiný; ukončím tag, který nezačal; přeházený vstup; ...)

## 5. hodina (2025-10-16)

<img align="right" src="pokrocili-1-05-driver-small.jpg" data-full="pokrocili-1-05-driver.jpg" style="height:85px" class="obrazek">

* Praktická ukázka postarší hry
  * Demoverze k dispozici například [zde](https://archive.org/details/DriverDemo)
  * Zklkamaly nás počítače, hra fungovala pouze na učitelském, proto jsme využili učitelský a můj notebook; po krátkém hledání to vypadá na problémy s Windows 10, proto doporučuji GNU/Linux (wine/lutris/proton), případně mohou pomoci ovladače [dgVoodoo](https://www.pcgamingwiki.com/wiki/DgVoodoo_2), pokud bude čas, můžeme někdy opět vyzkoušet
  * Ukázali jsme si lehce adresářovou strukturu:
    * ``Audio/`` - Zvuky, můžeme nahradit vlastními
    * ``Levels/`` - Mapy, nelehké úpravy, takže nezajímavé
    * ``Scripts/Events`` - Události, které se mohou dít když cestujeme po mapě, nebo je spouštět - zajímavé, ale moc toho neuděláme
    * ``Scripts/Missions`` - Definice misí - nejzajímavější, v demoverzi se vždy spustí skript ``mission661.dms`` a můžeme si ji trošku upravit
  * Nejzajímavějším zjištěním byl prostý formát definice misí a fakt, že demoverze nám dovolí jakékoliv úpravy v souboru ``Scripts/Missions/mission661.dms``, například:
    * Vypnutí časovače (``Countdown``), abychom získali víc času na hraní
    * Změna cíle (``SetTarget 0,1,917,398517``), čímž se vyhneme splnění mise a ukončení hry
    * Vypnutí ničení (``DisablePlayerDamage``), čímž nás tolik netrápí policisté
    * Případně vypnutí policistů kompletně (``cops_off``) a můžeme jezdil dle libosti
  * Následně jsme si vyzkoušeli splnit [upravenou misi](driver.dms) (v základu nesplnitelná, je nutnost upravit podmínky, kreativitě se meze nekladou)

## 6. hodina (2025-10-23)

* [code.org](https://www.code.org)
  * Ukázali jsme si CSS - kaskádové styly, které se používají pro definici stylu (barvy, pozice, efektů) na HTML stránce
  * Styl můžeme "importovat" pomocí ``<link rel="stylesheet" href="nas_styl.css">`` v hlavičce naší HTML stránce
  * Následně v tomto dokumentu můžeme definovat styl jednotlivým elementům na základě typu/tagu/třídy, např.:

stranka.html

```html
<!DOCTYPE html>
<html>
<head>
  <!-- Hlavička stránky, sem jdou informace pro počítač -->
  <link rel="stylesheet" href="nas_styl.css">
  <meta charset="UTF-8">
</head>
<body>
  <!-- Tělo naší stránky, sem jdou veci co chceme uživateli zobrazi -->
  <h1>Nadpis</h1>
  <p>Nějaký text</p>
</body>
```

nas_styl.css

```css
/* Nastavíme pozadí těla stránky */
body {
  background-color: lightblue;
}

/* Nastavíme barvu, zarovnání a velikost písma nadpisu h1 */
h1 {
  color: rgb(0, 255, 128);
  font-size: 70px
  text-align: center;
}

/* Nastavíme druh, barvu a velikost písma textu odstavce p */
p {
  font-family: verdana;
  font-size: 20px;
  color: #ffcc11
}
```

## 7. hodina (2025-10-30)

* [html stránky](/programovani-html)
  * Distribuce hesel
  * Neúspěšný pokus o využití WebTop tenkých klientů skrz prohlížeč. Loni nám to jakž-takž fungovalo, letos byly latence příliš veliké (prostě se to sekalo natolik, že se to nedalo použít). Budeme si muset vystačit s Windows a portable verzemi programů.
  * Vytvoření účtů na lokálně hostovaném Gogs (jednoduchá alternativa github/gitlab, využijeme v dalších hodinách)

<div id="overlay" class="overlay hidden">
  <span id="prev" class="nav">&#9664;</span>
  <img id="overlay-img" src="" alt="Obrázek">
  <span id="next" class="nav">&#9654;</span>
  <span id="close" class="close">&times;</span>
</div>
<link rel="stylesheet" href="/assets/gallery.css">
<script src="/assets/gallery.js"></script>

<img align="right" src="../media/robots_bottom.jpg">
