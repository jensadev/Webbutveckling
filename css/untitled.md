# Din första CSS fil

> Märkspråk och deras inbördes roller, syntax och semantik – där det huvudsakliga innehållet är standarderna för HTML och CSS samt orientering om Ecmaskript och dokumentobjektsmodellen \(DOM\).

## Ett exempel

Index.html första versionen. 

{% code title="index.html" %}
```markup
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SVT Nyheter</title>
  <link rel="stylesheet" href="stylesheets/main.css">
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

{% embed url="https://raw.githubusercontent.com/jensnti/Webbutveckling/dffa89ec9e99f9d869c2b93d47e80afdc52c82e3/exempel/html-struktur.html" %}



Version två med css

{% code title="index.html" %}
```markup
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SVT Nyheter</title>
  <link rel="stylesheet" href="stylesheets/main.css">
</head>
<body>
  <nav class="d-flex">
    <a href="#">SVT NYHETER</a>
    <ul>
      <li><a href="#">Nyheter</a></li>
      <li><a href="#">Lokalt</a></li>
      <li><a href="#">Sport</a></li>
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

{% embed url="https://raw.githubusercontent.com/jensnti/Webbutveckling/158752f5608cffe24514dd5bac35403c6e8c8d08/exempel/html-struktur.html" %}

{% code title="stylesheets/main.css" %}
```css
body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
}

h1 {
  font-size: 2rem;
}

h2 {
  font-size: 3rem;
}

nav {
  width: 100%;
  justify-content: center;
}

main {
  width: 60%;
  margin: 0 auto;
}

.d-flex {
  display:flex;
}

.h-100 {
  height: 100%;
}

.w-100 {
  width: 100%;
}

.focus {
  background-color: #333;
  color: #fff;
}

.now {
  background-color: #e02e3d;
}
```
{% endcode %}

{% embed url="https://raw.githubusercontent.com/jensnti/Webbutveckling/158752f5608cffe24514dd5bac35403c6e8c8d08/exempel/stylesheets/html-struktur.css" %}







