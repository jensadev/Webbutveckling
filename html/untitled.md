# Din första HTML fil

> Märkspråk och deras inbördes roller, syntax och semantik – där det huvudsakliga innehållet är standarderna för HTML och CSS samt orientering om Ecmaskript och dokumentobjektsmodellen \(DOM\).

## Vad är HTML?

* **HTML** står för **Hyper Text Markup Language**
* HTML är ett **märkspråk** \(ett språk för att märka upp textfiler\)
* HTML är standardspråket för att skapa webbsidor
* HTML beskriver strukturen för en webbsida
* HTML består av **element** som berättar för webbläsaren hur webbsidan ska se ut

## Ett exempel

Nedan följer grunden för ett korrekt HTML-dokument. Det består av ett antal element med tillhörande **attribut**. Element skrivs med **taggar** \(namnet inom &lt; &gt; tecken\).

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

### Element

* &lt;!DOCTYPE html&gt; deklarerar att dokument är ett HTML5 dokument.
* &lt;html&gt; är **root** \(det första\) elementet för ett HTML dokument.
* &lt;head&gt; elementet innehåller information om webbsidan till webbläsaren.
  * &lt;meta&gt; elementet specificerar [**teckenkodning** ](../teknisk-orientering/teckenkodning.md)bland annat.
  * &lt;title&gt; innehåller sidans titel som värde, vilket syns in webbläsarens titel eller **tab.**
* &lt;body&gt; elementet definierar sidans kropp, det innehåll som vi ser på webbsidan.
  * &lt;h1&gt; elementet skapar en **rubrik** \(engelska **heading**\).
  * &lt;p&gt; elementet skapar en **paragraf** \(engelska **paragraph**\).

Notera att de flesta element består av en öppnings- och stängnings-tagg. Ett elements värde skrivs mellan taggarna. Taggar stängs med en slash /.

### Attribut

Sidan här ovanför har ett antal **attribut** som tillhör taggarna.





