# Viktigt

## Root EM

REM är ett måttvärde i CSS. Det utgår från root elementets font-storlek för att sätta storleken på element.

Värdet skrivs som nedan för att till exempel sätta storleken på texten och det kommer utgå från HTML-elementets textstorlek, vilket som oftast är 16px.

{% tabs %}
{% tab title="CSS" %}
```css
p {
    font-size: 1rem;
}
```
{% endtab %}
{% endtabs %}

Om du anger detta på en sida så kan du sedan inspektera uträknade värden i webbläsarens utvecklingsverktyg. Se Fig 1.

![Fig 1, Computer font-size of 4 rem.](../.gitbook/assets/dev-comp.png)

