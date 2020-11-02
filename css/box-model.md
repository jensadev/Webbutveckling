# Box model

Allt i CSS har en låda omkring sig, därför är det centralt att förstå hur detta fungerar för att kunna skapa layout med CSS. Se Fig 1.

![Fig 1, box model fr&#xE5;n Chromes utvecklarverktyg.](../.gitbook/assets/box-model.png)

## Vad är box model

Förenklat är det hur mycket plats element tar på en webbsida, hur stort det är. Men hur detta räknas ut och påverkas av andra element är komplicerat. Elementets box model är uppdelad i flera olika delar, se fig 1. Elementets storlek är summan av alla delarna.

### Content

De/det element eller innehåll\(engelska content\) som finns i elementet. Innehållet styr elementets storlek.

{% tabs %}
{% tab title="HTML" %}
```markup
<div>
    <p>Den omgivande divens storlek är beroende av den här textens storlek.</p>
    <p>Men p-elementen styrs också av box model för sin storlek.
</div>
```
{% endtab %}
{% endtabs %}

### Padding

Runt elementets innehåll finns det en padding på alla sidor. Denna padding är tomt utrymme som skapar luft runt elementets innehåll.

{% tabs %}
{% tab title="HTML" %}
```markup
<div class="w-100 p-5">
    <p>I det här exemplet styr vi div elementets storlek med klassen w-100.
    Utöver det så sätts en padding med p-5, detta kommer ställa till problem.
    </p>
</div>
```
{% endtab %}

{% tab title="CSS" %}
```css
.w-100 {
    width: 100%;
}

.p-5 {
    padding: 5rem;
}
```
{% endtab %}
{% endtabs %}

### Border

Om elementet har en ram så läggs även det till i elementets storlek.

### Margin

Runt elementet finns slutligen en marginal som omger elementet.

## Block och inline-element

Se avsnittet från HTML-kapitlet, [Block och inline-element](../html/html-spraket.md#block-och-inline-element).

## Display typer

## Läs mer

* [https://developer.mozilla.org/en-US/docs/Learn/CSS/Building\_blocks/The\_box\_model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)

