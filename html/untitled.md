# Din första HTML fil

> Märkspråk och deras inbördes roller, syntax och semantik – där det huvudsakliga innehållet är standarderna för HTML och CSS samt orientering om Ecmaskript och dokumentobjektsmodellen \(DOM\).

## Vad är HTML?

* **HTML** står för **Hyper Text Markup Language**
* HTML är ett **märkspråk** \(ett språk för att märka upp textfiler\)
* HTML är standardspråket för att skapa webbsidor
* HTML beskriver strukturen för en webbsida
* HTML består av **element** som berättar för webbläsaren hur webbsidan ska se ut

## Ett exempel

{% hint style="info" %}
Om en HTML-fil har filnamnet **index** så kommer den automatiskt öppnas av webbläsaren när adressen besöks. Filändelsen är **.html**
{% endhint %}

Nedan följer grunden för ett korrekt HTML-dokument. Det består av ett antal element med tillhörande **attribut**. Element skrivs med **taggar** \(namnet inom &lt; &gt; tecken\).

{% code title="index.html" %}
```markup
<!DOCTYPE html>
<html lang="se">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mitt första html dokument</title>
</head>
<body>
  <h1>Välkommen!</h1>
  <p>Detta är p elementets värde.</p>
</body>
</html>
```
{% endcode %}

### Element

* &lt;!DOCTYPE html&gt; deklarerar att dokument är ett HTML5 dokument.
* &lt;html&gt; är **root** \(det första\) elementet för ett HTML dokument.
* &lt;head&gt; elementet innehåller information om webbsidan till webbläsaren.
  * &lt;meta&gt; elementet specificerar [**teckenkodning** ](../teknisk-orientering/teckenkodning.md)bland annat.
  * &lt;title&gt; innehåller sidans titel som värde, vilket syns in webbläsarens titel eller **tab.**
* &lt;body&gt; elementet definierar sidans kropp, det innehåll som vi ser på webbsidan.
  * &lt;h1&gt; elementet skapar en **rubrik** \(engelska **heading**\).
  * &lt;p&gt; elementet skapar en **paragraf** \(engelska **paragraph**\).

Notera att de flesta element har en öppnings- och stängnings-tagg. Ett elements värde skrivs mellan taggarna. Taggar stängs med en slash /.

{% hint style="info" %}
Studera indragen i exemplet, det är väldigt viktigt att skriv koden med indrag för att öka dess läsbarhet. Det underlättar för dig som utvecklar koden.
{% endhint %}

### Attribut

Exemplet ovanför har ett antal **attribut** som tillhör taggarna.

* lang, med ett värde som anger webbsidans språk. Webbläsaren använder det för eventuell översättning av sidan baserat på användarens språk.
* charset, vilket [teckenkodning ](../teknisk-orientering/teckenkodning.md)sidan ska använda. Detta kommer i 99.9% av fallen vara [**UTF-8**](../teknisk-orientering/teckenkodning.md#utf-8).
* name, viewport. Detta anger skalan som används av olika enheter när sidan visas.

{% hint style="info" %}
Med element, attribut och tillhörande text så byggs en webbsidas struktur upp.
{% endhint %}

## Att koda exemplet

Exemplet som finns här ovanför innehåller de element som krävs för en korrekt skriven HTML sida, vi säger att den [validerar ](../tester/kodkvalitet.md#validering)som korrekt HTML. Du kommer att behöva dessa element för varje sida du skapar, så att skriva av dem för hand är inte rimligt.

Du kan kopiera koden från exemplet här, men det är inte praktiskt i längden. Istället är det viktigt att du bekantar dig med den textredigerare eller [IDE ](../verktyg/visual-studio-code.md)som du använder för att koda. Den innehåller med största sannolikhet ett verktyg för att skapa viss kod. I Visual Studio Code skapar du en .html fil, sedan skriver du `html:5` och trycker tab.

{% hint style="info" %}
Nästan alla kod-element har kortkommandon i ditt IDE, lär dig dem!
{% endhint %}

