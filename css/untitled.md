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

## 

