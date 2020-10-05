# Layout

## CV, en första layout

För att skapa en sida med ett CV så är det i första hand en fråga om att märka upp text. När detta är gjort och en struktur har skapats finns det utrymme att arbeta vidare med att skapa en personlig stil. Det CV som skapas i detta exempel är ett CV för en fiktiv karaktär.

{% hint style="info" %}
Börja med att identifiera webbsidans komponenter och struktur.
{% endhint %}

![Marios CV, skapat av Stina&#xA9;](../.gitbook/assets/mario.png)

Strukturmässigt så kan vi dela upp det i följande element.

* `header`, bestånde av rubrik, kontaktuppgifter och porträtt
* `main`
  * `section`, med rubrik, tidsangivelse och resume
  * efterföljande section

Elementen kan även märkas upp med ID för sektionerna för att möjliggöra fragments-navigation. Detta kan användas om vi vill göra dokumentet till mer av en webbsida, än en direkt kopia.

{% code title="cv.html" %}
```markup
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CV - Mario Mario</title>
</head>
<body>
  <header id="contact">
    <img src="https://via.placeholder.com/200x200?text=Mario+portrait" alt="Mario portrait">
    <h1>Mario Mario</h1>
    <h2>Plumber, princess rescuer and race car driver</h2>
    <h3>Contact Information</h3>
    <address>
      Phone: +39 1985 1985
      Email: mario@super.it
      Twitter: @supermariobro
    </address>
  </header>
  <main id="professionalexperience">
    <h1>Professional experience</h1>
    <section id="twentyseventeen">
      <h2><time datetime="2017">2017</time></h2>
      <p><strong>Princess rescuer and wedding crasher</strong>, self-employed, Various Kingdoms</p>
      <ul>
        <li>In charge of magic cap</li>
        <li>Controlled the art of shapeshifting</li>
        <li>Collected valuable power moons for profit</li>
        <li>Defeated numerous enemies, e.g. t-rexes and broodals</li>
      </ul>
    </section>
```
{% endcode %}

## SVT, ett exempel

För att kunna arbeta med CSS behöver vi ett HTML dokument att utgå ifrån. Det som följer är index.html från kapitlet om HTML. Du kan ladda ned filen [här](https://raw.githubusercontent.com/jensnti/Webbutveckling/dffa89ec9e99f9d869c2b93d47e80afdc52c82e3/exempel/html-struktur.html). 

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
    <a href="#">SVT NYHETER</a>
    <ul>
      <li><a href="#">Nyheter</a></li>
      <li><a href="#">Lokalt</a></li>
      <li><a href="#">Sport</a></li>
    </ul>
  </nav>
  <main>
    <header>
      <h1>JUST NU <span>SENASTE NYTT OM CORONAVIRUSET</span>
        <a href="#">LÄS MER</a>
      </h1>
    </header>
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
    <aside>
      <h3>SNABBKOLLEN</h3>
      <ul>
        <li><a href="#">Lukasjenko svärs in som president</a></li>
        <li><a href="#">Sjukhuset: Navalnyj utskriven</a></li>
      </ul>
    </aside>
  </main>
  <footer>
    <h4>SVT NYHETER</h4>
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

Att förvandla text till grafik är svårt och CSS kan vara väldigt besvärligt att arbeta med. Det finns många faktorer att känna till och förstå sig på.

Version två av exempel-dokumentet med CSS klasser tillagda. Den här versionen har lagt grunden för sidans layout. Den använder flexbox för att positionera vissa element. Main-elementet har centrerats. Sidan innehåller vissa grafiska avgörande element för att vi ska känna igen den.

{% code title="svt.html" %}
```markup
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SVT Nyheter</title>
  <link rel="stylesheet" href="stylesheets/svt.css">
</head>
<body>
  <nav class="navbar d-flex align-center">
    <a href="#">SVT NYHETER</a>
    <ul class="d-flex">
      <li class="nav-item"><a href="#">Nyheter</a></li>
      <li class="nav-item"><a href="#">Lokalt</a></li>
      <li class="nav-item"><a href="#">Sport</a></li>
    </ul>
  </nav>
  <main>
    <header class="d-flex focus">
      <h1><span class="now">JUST NU</span> SENASTE NYTT OM CORONAVIRUSET
        <a href="#">LÄS MER</a>
      </h1>
    </header>
    <article>
      <img class="w-100" src="https://picsum.photos/600/300">
      <h2>Ryskt militärfartyg i krock i Öresund</h2>
      <p>Dimma i området. Danmark begär svensk hjälp</p>
    </article>
    <article>
      <img class="w-100" src="https://picsum.photos/600/300">
      <h2>Emma Frans om stigande smittkurvan: "Ganska väntat"</h2>
      <p>Forskare: Stora frågan är om uppgången fortsätter</p>
    </article>
    <aside>
      <h3>SNABBKOLLEN</h3>
      <ul>
        <li><a href="#">Lukasjenko svärs in som president</a></li>
        <li><a href="#">Sjukhuset: Navalnyj utskriven</a></li>
      </ul>
    </aside>
  </main>
  <footer>
    <h4>SVT NYHETER</h4>
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

Tillhörande stylesheet.

{% code title="stylesheets/svt.css" %}
```css
body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  padding: 0;
  margin: 0;
}

h1 {
  font-size: 2rem;
}

h2 {
  font-size: 3rem;
}

header {
  margin: 1rem 0;
}

main {
  width: 80%;
  margin: 0 auto;
}

ul {
  list-style: none;
}

footer {
  color: #fff;
  padding: 2rem 0;
  text-align: center;
  background-color: #333;
}

.navbar {
  width: 100%;
  justify-content: space-around;
  border-bottom: 4px solid #e02e3d;
  height: 4rem;
}

.nav-item {
  padding: 0 1rem;
}

.focus {
  background-color: #333;
  color: #fff;
}

.now {
  background-color: #e02e3d;
}

/* helpers */

.d-flex {
  display:flex;
}

.h-100 {
  height: 100%;
}

.w-100 {
  width: 100%;
}

.align-center {
  align-items: center;
}
```
{% endcode %}

## 



## Länkar

* Flexbox
  * [https://www.internetingishard.com/html-and-css/flexbox/](https://www.internetingishard.com/html-and-css/flexbox/)
  * [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS\_Flexible\_Box\_Layout/Basic\_Concepts\_of\_Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
* Layout
  * [https://www.w3schools.com/css/css\_templates.asp](https://www.w3schools.com/css/css_templates.asp)
  * [https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS\_layout](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout)



