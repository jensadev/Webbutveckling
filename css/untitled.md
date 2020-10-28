# Layout och design

## SVT, ett mer komplext exempel

I avsnittet kring [struktur ](../html/struktur.md)undersöktes [svt.se](https://svt.se) som exempel för en sidstruktur. I det här avsnittet kommer du att arbeta med en html struktur baserad på SVT Nyheter. Strukturen ser ut som följer.

{% code title="svt.html" %}
```markup
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SVT Nyheter</title>
</head>
<body>
  <nav>
    <a href="#">SVT Nyheter</a>
    <ul>
      <li><a href="#">Nyheter</a></li>
      <li><a href="#">Lokalt</a></li>
      <li><a href="#">Sport</a></li>
    </ul>
  </nav>
  <header>
    <h1><span>Just nu</span> Senaste nytt om coronaviruset
      <a href="#">Läs mer</a>
    </h1>
  </header>
  <main>
      <aside>
      <h3>Snabbkollen</h3>
      <ul>
        <li><a href="#">Lukasjenko svärs in som president</a></li>
        <li><a href="#">Sjukhuset: Navalnyj utskriven</a></li>
      </ul>
    </aside>
    <article>
      <img src="https://picsum.photos/600/300">
      <h2>Ryskt militärfartyg i krock i Öresund</h2>
      <p>Dimma i området. Danmark begär svensk hjälp</p>
    </article>
    <article>
      <img src="https://picsum.photos/600/300">
      <h2>Emma Frans om stigande smittkurvan: "Ganska väntat"</h2>
      <p>Forskare: Stora frågan är om uppgången fortsätter</p>
    </article>
  </main>
  <footer>
    <h4>SVT Nyheter</h4>
    <ul>
      <li>Tjänstgörande webbredaktör: <a href="#">Person Personsson</a></li>
      <li><a href="mailto:svt">Kontakta SVT Nyheter</a></li>
      <li>&copy; Sveriges Television AB</li>
    </ul>
  </footer>
</body>
</html>
```
{% endcode %}

Att förvandla text till grafik är svårt och CSS kan vara väldigt besvärligt att arbeta med. Det finns många faktorer att känna till och förstå sig på.  När du ska återskapa en sida så börja alltid med att försöka strukturera dess innehåll, för att sedan arbeta med stilarna.

När en struktur baserad på sidans komponenter är skapad, så är nästa steg stilarna. Men var medveten att det kan komma att påverka placering och nästling av element.

### Design

För att återskapa sidan så kan vi ta en genväg och det är att studera framträdande element som ska återskapas. Studera skärmdumpen från SVT Nyheter, vilka element noterar du, gör en lista.

![svt.se fr&#xE5;n September 2020](../.gitbook/assets/svt.png)

Designelement och layout att ta fasta på:

* Den röda färgen, med hjälp av utvecklarverktygen kan vi hitta att färgkoden är \#e02e3d.
* Den grå färgen, det finns en varmare och kallare.
  * Senaste nytt grå är \#333333
* Typsnittet, SVT Nyheter använder ett typsnitt som heter Publik, det är inte fritt. Sök efter ett liknande alternativ.
  * Användningen av CAPS, både som stil men också för att väcka uppmärksamhet.
* Layouten
  * En **screamer**, JUST NU, tar vår uppmärksamhet först.
  * Sidan har en tydlig navbar.
  * Dessa två delar följs av ett huvudinnehåll uppdelat på två spalter.
    * Sidans huvudinnehåll, nyheterna.
    * Snabbkollen, en **sidebar** med länkar och senaste.
    * Spalterna försvinner vid lägre upplösning.
  * En sidfot längst ned på sidan.

När dessa element är identifierade så finns det en startpunkt för kodandet av sidan.

## Skapa layouten

### Rubriker

### Den röda linjen

### Navigation

### 2 spalter

### Länkar

### Screamer

## Slutgiltig version

Den färdiga koden för SVT-exemplet finns att hämta [här](https://github.com/jensnti/Webbutveckling/tree/master/exempel)\(svt-css.html, svt.css, img/\). Det är en mer färdig design och hoppet mellan versionerna är markant.

* Strukturen har ändrats.
  * Navbaren har fått en content div för att centrera innehållet.
  * Header-elementet är flyttat utanför main, så att main kan delas i två kolumner.
  * Aside-elementet har flyttats före nyhets-artiklarna, för att möjliggöra en float layout på två kolumner.
* Fler helper klasser har skapats.
* Några element har mer komplexa selektorer för att välja först eller sista elementet.
* Det finns en media regel med brytpunkt på max-width. Detta för att ändra float layouten och ta bort de två spalterna ur main.
* Det finns en media regel på min-width 1280px för att göra sidan mer läsbar på stora skärmar.
* Ett par ikoner används från [Google material icons](https://material.io/resources/icons/). De har sparats som SVG och färgen har ändrats.

## Länkar

* Flexbox
  * [https://www.internetingishard.com/html-and-css/flexbox/](https://www.internetingishard.com/html-and-css/flexbox/)
  * [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS\_Flexible\_Box\_Layout/Basic\_Concepts\_of\_Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)

