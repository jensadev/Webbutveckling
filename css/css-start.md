# Din första CSS fil

> Märkspråk och deras inbördes roller, syntax och semantik – där det huvudsakliga innehållet är standarderna för HTML och CSS samt orientering om Ecmaskript och dokumentobjektsmodellen \(DOM\).

**Cascading Style Sheets**\(**CSS**\) är webbens verktyg för att skapa en webbplats utseende eller stil, webbplatsens presentation. CSS låter dig bestämma fonter, placeringar, färger och andra dekorativa funktioner. Ofta används namnet **stylesheet** för CSS-dokument.

## Syntax

Alla CSS regler börjar med en **selektor**\(engelska **selector**\) vilken väljer elementet som regeln ska gälla. Om vi önskar att ge alla rubriker med nivå ett röd text så kan h1 elementet användas. Efter att elementet har valts så visar en uppsättning måsvingar, `{}`, regelns början och slut. CSS värden skrivs med `attribut: värde;`

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
    color: red;
}
```
{% endtab %}
{% endtabs %}

## Selektorer

I CSS finns det tre olika typer av selektorer, element, klass och id.

### Element

Element-selektor använder HTML-elementets namn och påverkar alla element på sidan av den typen.

{% tabs %}
{% tab title="CSS" %}
```css
p {
    color: darkgrey;
    font-size: 1.2rem;
}
```
{% endtab %}
{% endtabs %}

### Klass

Med klass-typen av regeln skapar vi ett namn som vi sedan anger på de element där vi vill att regeln ska gälla. Klasser används när du behöver ge en stil-regel till ett eller flera element. Klasser skrivs med `.regelnamn` och används med genom att ge elementet `class="regelnamn"` attributet.

{% tabs %}
{% tab title="CSS" %}
```css
.lead {
    color: #101010;
    font-size: 1.4rem;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<p class="lead">Den här texten får CSS-regeln lead</p>
```
{% endtab %}
{% endtabs %}

### ID

Den sista typen av selektor är ID. ID används främst för att namnge element och ska helst inte användas vid CSS regler. Ett ID ska vara unikt och således ska ett enskilt ID bara användas en gång. Så om du behöver använda CSS-regler på element så använd klasser.

{% tabs %}
{% tab title="CSS" %}
```css
#chapter-ii {
    color: rgb(200, 10, 10);
    font-weight: 800;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<h2 id="chapter-ii">Kapitel 2</h2>
```
{% endtab %}
{% endtabs %}

## Cascading

När du arbetar med CSS är det viktigt att känna till hur reglerna appliceras, reglerna har en ordning för hur de användas, **cascading**\(kaskad, flöde, vattenfall\). De appliceras i en särskild ordning.

### Den sista i ordningen vinner

Detta gäller inom samma fil.

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
    color: red;
}

h1 {
    color: blue;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<h1>Den här texten blir blå.</h1>
```
{% endtab %}
{% endtabs %}

Men ordningen gäller även när reglerna läses in. De läses in i följande ordning.

* Extern fil, länkad inuti dokumentets head. `<link rel="stylesheet" href="style.css">`
* style-element i dokumentet. `<style>h1 { color: red; } </style>`
* Slutligen så kallade inline-stilar som attribut på element. `<h1 style="color: green;">`

Ordningen kan ignoreras med attributet `!important`, men använd det med försiktighet då det kan göra felsökning svårare.

{% tabs %}
{% tab title="CSS" %}
```css
h1 {
    color: pink !important;
}
```
{% endtab %}
{% endtabs %}

### Klass före element

{% tabs %}
{% tab title="CSS" %}
```css
.heading {
    color: red;
}

h1 {
    color: blue;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<h1 class="heading">Den här texten blir röd.</h1>
```
{% endtab %}
{% endtabs %}



