# Din första CSS fil

> Märkspråk och deras inbördes roller, syntax och semantik – där det huvudsakliga innehållet är standarderna för HTML och CSS samt orientering om Ecmaskript och dokumentobjektsmodellen \(DOM\).

**Cascading Style Sheets**\(**CSS**\) är webbens verktyg för att skapa en webbplats utseende eller stil, webbplatsens presentation. CSS låter dig bestämma fonter, placeringar, färger och andra dekorativa funktioner.

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

Med klass-typen av regeln skapar vi ett namn som vi sedan anger på de element där vi vill att regeln ska gälla. Klasser används när du behöver ge en stil-regel till ett eller flera element.

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







