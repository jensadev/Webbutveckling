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
  * efterföljande sektioner

Elementen kan även märkas upp med ID för sektionerna för att möjliggöra fragments-navigation. Navigation, hypertext, är en möjlig förbättring vi kan göra av sidan för att utnyttja webbsidans styrkor. Kodad med HTML-element kan första delen se ut såhär. 

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

### Layout med CSS



## 



## Länkar

* Flexbox
  * [https://www.internetingishard.com/html-and-css/flexbox/](https://www.internetingishard.com/html-and-css/flexbox/)
  * [https://developer.mozilla.org/en-US/docs/Web/CSS/CSS\_Flexible\_Box\_Layout/Basic\_Concepts\_of\_Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
* Layout
  * [https://www.w3schools.com/css/css\_templates.asp](https://www.w3schools.com/css/css_templates.asp)
  * [https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS\_layout](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout)



