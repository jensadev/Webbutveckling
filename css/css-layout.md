# Layout

## CV, en första design

För att skapa en sida med ett CV så är det i första hand en fråga om att märka upp text. När detta är gjort och en struktur har skapats finns det utrymme att arbeta vidare med att skapa en personlig stil. Det CV som skapas i detta exempel är ett CV för en fiktiv karaktär.

{% hint style="info" %}
Börja med att identifiera webbsidans komponenter och struktur.
{% endhint %}

![Marios CV, skapat av Stina©](../.gitbook/assets/mario.png)

Strukturmässigt så kan vi dela upp det i följande element.

* `header`, bestånde av rubrik, kontaktuppgifter och porträtt
* `main`
  * `section`, med rubrik, tidsangivelse och resume.
  * efterföljande sektioner

Elementen kan även märkas upp med ID för sektionerna för att möjliggöra fragments-navigation. Navigation, hypertext, är en möjlig förbättring vi kan göra av sidan för att utnyttja webbsidans styrkor. Kodad med HTML-element kan första delen se ut såhär.&#x20;

#### Uppgift

Koda resten av CV sidan. Texten hittar du i engelska-uppgiften. När du är klar så kan du jämföra ditt resultat med det [här](https://raw.githubusercontent.com/jensnti/Webbutveckling/1c9b95925e22827d8be32e8e4e620f53dda991ec/exempel/cv.html).

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

### Länka ett CSS dokument

För att länka ett extern CSS dokument så behövs en länk i sidans head-element. Skapa cv.css.

{% code title="cv.html" %}
```markup
<link rel="stylesheet" href="cv.css">
```
{% endcode %}

Sidan läser nu in stilarna från det externa css-dokumentet.

### Layout med CSS

Marios CV har en relativt enkelt struktur, det är en kolumns layout uppdelat i en `header `och en `main `för innehållet. Strukturen med dessa element och underliggande skapar vi för att gruppera sidans delar.

Sidan är en kolumn som är centrerad. Detta kan skapas genom att justera sidans bredd och marginaler. Egenskapen `margin` styr marginalen på ett element, värdet som ges styr top, bottom och left, right.

{% code title="cv.css" %}
```css
body {
    margin: 0 auto;
    width: 60%;
}
```
{% endcode %}

Headern innehåller porträttet, namn-rubriken och kontaktinformation med tillhörande rubriknivåer. För att placera bilden kan vi använda egenskapen `float`. Skapa en klass för detta och koppla den till elementet.

{% tabs %}
{% tab title="HTML" %}
{% code title="cv.html" %}
```markup
  <header id="contact">
    <img class="portrait" src="https://via.placeholder.com/200x200?text=Mario+portrait" alt="Mario portrait">
    <h1>Mario Mario</h1>
    <h2>Plumber, princess rescuer and race car driver</h2>
    <h3>Contact Information</h3>
    <address>
      Phone: +39 1985 1985
      Email: mario@super.it
      Twitter: @supermariobro
    </address>
  </header>
```
{% endcode %}
{% endtab %}

{% tab title="CSS" %}
{% code title="cv.css" %}
```css
.portrait {
    float: right;
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

Ladda om sidan och bilden placeras nu till höger om texten, texten anpassar sig även till bildens storlek.&#x20;

{% hint style="info" %}
Float fungerar bra i vissa upplösningar, om du ändrar storleken på webbläsarfönstret till att vara riktigt smalt så kan du se att float får problem.
{% endhint %}

Den andra delen av sidan är samlad i ett `main `element, den innehåller huvuddelen av CV-informationen. Under detta är varje del strukturerad i en `section `med tillhörande rubrik. Marios färdigheter och erfarenheter är sedan strukturerad i en o-ordnad lista, `ul`.

{% code title="cv.html" %}
```markup
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

### Typsnitt

Typsnittet som används på Mario sidan är en så kallad sans-seriff. En seriff är klacken på ett tecken och sans betyder utan, så utan klack.&#x20;

{% hint style="info" %}
[Läs mer här om vad en seriff är.](https://sv.wikipedia.org/wiki/Seriff)
{% endhint %}

**Visual Studio Code** ger ett antal förslag och exempel på fonter som kan användas när css-egenskpen `font-family` anges. Egenskapen tar en eller flera fonter som värde, där den provar den första om den fungerar, den andra och så vidare.

{% tabs %}
{% tab title="CSS" %}
```css
body {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1rem;
}
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Font-storleken rem är root em, den baseras på root elementets font-storlek och det styrs av webbläsaren. Om standardstorleken är vald så kan du utgå från att 1rem = 16 i fontstorlek.
{% endhint %}

#### Egna fonter

Att använda de föreslagna fonterna fungerar självklart utmärkt, men för ett mer personligt uttryck för Mario så används en extern font från Google fonts. För att använda en font därifrån behöver du:

1. Leta reda på en font du vill använda.
2. Klicka på den.
3. På fontens sida väljer du **+ Select this style**.
   1. Välj **Regular 400** om du inte har andra behov.
4. Öppna sidebaren med **Selected family**.
5. Klicka på **Embed**.
6. Kopiera länken till ditt html dokument.
7. Kopiera CSS egenskapen font-family till ditt CSS dokument.

Marios CV får Google fonten Roboto. Följande ändringar görs. Att ge body elementet en `font-family` påverkar fonterna på alla platser i dokumentet.

{% tabs %}
{% tab title="HTML" %}
{% code title="cv.html" %}
```markup
<link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
```
{% endcode %}
{% endtab %}

{% tab title="CSS" %}
{% code title="cv.css" %}
```css
body {
    font-family: 'Roboto', sans-serif;
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Google fonts är ett enormt bibliotek av gratis fonter du kan använda i dina projekt. Vill du lära dig mer så läs den [här guiden](https://design.google/library/choosing-web-fonts-beginners-guide/) om att välja typsnitt för webb-projekt.
{% endhint %}

### Rubriker

Dokumentet innehåller ett stor antal rubriker med olika formatering. Rubrikelementet förekommer på flera platser i dokumentet, så därför kommer vi att använda klasser för denna styling.

{% tabs %}
{% tab title="HTML" %}
{% code title="cv.html" %}
```markup
    <h1 class="main-heading">Professional experience</h1>
    <section id="twentyseventeen">
      <h2 class="time-heading"><time datetime="2017">2017</time></h2>
```
{% endcode %}
{% endtab %}

{% tab title="CSS" %}
{% code title="cv.css" %}
```css
.main-heading {
    font-size: 2rem;
    font-color: rgb(28,69,135);
    border-bottom: 1px solid rgb(28,69,135);
}

.time-heading {
    font-size: 1.4rem;
    color: #959595;
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

### Listor

I HTML så används ofta listor för att strukturera innehåll. Listorna i Marios CV är ett bra exempel på detta. I dokumentet så används - för att notera varje rad i listan, denna stil finns dock inte i HTML.&#x20;

Prova olika list stilar och gör ett eget val. Utöver detta så justerar du den padding som elementet har till vänster.

{% code title="cv.css" %}
```css
ul {
    list-style: none;
    padding-left: 1rem;
 }
```
{% endcode %}

&#x20;I en lista skapas varje rad av ett `li` element, det är block element så det blir en radbrytning vid varje. Det kan ändras med display egenskapen. Antingen kan listan, ul-elementet, ändras med `display: flex` eller så ges varje enskilt li-element egenskapen `display: inline`. Detta är användbart om en lista används för en navigation.

### Navigation

För att utnyttja det faktum att Marios CV nu är ett hypertextdokument så kan det skapas en navigation för dokumentet med fragmentsnavigering.

{% tabs %}
{% tab title="HTML" %}
{% code title="cv.html" %}
```markup
  <nav>
    <ul class="nav-list">
      <li class="nav-item"><a href="#twentyseventeen">2017</a></li>
      <li class="nav-item"><a href="#twentythirteen">2013</a></li>
      <li class="nav-item"><a href="#twentyotwo">2002</a></li>
      <li class="nav-item"><a href="#nineteenninetyfive">1995</a></li>
    </ul>
  </nav>
```
{% endcode %}
{% endtab %}

{% tab title="CSS" %}
{% code title="cv.css" %}
```css
.nav-list {
    list-style: none;
    padding: 0;
    display: flex;
}

.nav-item {
    margin: 0 1rem;
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

Med flex så kan vi justera hur element ska positioneras och visas i relation till varandra. Du kan använda CSS-egenskaperna `justify-content` och `align-items` för att styra detta.

### Länkar

Om du önskar att ändra länkarna i dokumentet så kan du skapa regler för a-elementet. För att påverka länkar när muspekaren är över dem så används regeln `:hover`.

```css
a {
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
}
```

## Övning

Skapa alla de stilar som behövs för att återge Marios CV.

## Länkar

Här finns det ytterligare material samlat för dig att arbeta med.

* CSS
  * [https://developer.mozilla.org/en-US/docs/Learn/CSS/First\_steps](https://developer.mozilla.org/en-US/docs/Learn/CSS/First\_steps)
* Layout
  * [https://www.w3schools.com/css/css\_templates.asp](https://www.w3schools.com/css/css\_templates.asp)
  * [https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS\_layout](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS\_layout)

