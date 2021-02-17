# Språket

Cascading Style Sheets \(CSS\) är det språk som webben använder för att beskriva hur ett HTML dokument ska presenteras. Det beskriver hur de olika elementen ska visas på en skärm.

CSS språket är standardiserat och följer, likt HTML, [specifikationer ](https://www.w3.org/Style/CSS/#specs)från [W3C](https://www.w3.org/).

## Syntax

CSS skrivs i regler. En regel har inget namn, utan det består av en selektor som används för att identifiera elementet. Detta följs av en eller flera egenskaper för elementet.

{% tabs %}
{% tab title="CSS" %}
```css
/* Style rule */
selector {
  egenskap(er)
}
```
{% endtab %}
{% endtabs %}

### Selektorer

För att identifiera vilket eller vilka element som en regel ska påverka används selektorer. De kan hänvisa till faktiska element, klasser eller id.

{% tabs %}
{% tab title="CSS" %}
```css
body {
  color: red;
}

.rubrik {
  color: red;
}

#kapitel1 {
  color: red
}
```
{% endtab %}
{% endtabs %}

### Kombinera selektorer

Det går...

## Cascading

Vad betyder det och hur påverkar det dina stylesheets. Hur använder du det.

