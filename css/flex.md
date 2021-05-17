---
description: Lösningen på allt... nästan.
---

# Flex

## Flexbox

Display flex är ett layoutsystem för webben som använder kolumner och rader för att strukturera innehåll. Du använder det genom att sätta display egenskapen på ett element med CSS.

{% tabs %}
{% tab title="CSS" %}
```css
display: flex;
```
{% endtab %}
{% endtabs %}

Flex löser flera problem med positionering och det låter oss mycket enklare skapa komplexa layouter som samtidigt är mobilanpassade. Ett bra första exempel är att placera element bredvid varandra.

Studera och kopiera följande kod. Det är två sektioner med rubriker och brödtext. Hur går du till väga för att placera sektionerna bredvid varandra som spalter. Innan flex så joxade många med floats för att lösa det, men det fungerade sällan bra.

{% tabs %}
{% tab title="HTML" %}
```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flex exempel</title>
</head>
<body>
    <main>
        <section>
            <h1>Lorem ipsum</h1>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nesciunt vitae distinctio beatae unde. Ipsa optio ipsam, quos assumenda obcaecati beatae perferendis soluta dolore dolor quaerat quibusdam aliquam maiores laboriosam. Enim.</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Non veniam dicta hic porro reiciendis id at nemo! Iusto fuga vel ipsum laborum. Voluptatibus iure ex nobis maiores, harum corporis magnam!</p>
            <h2>Lorem ipsum dolor sit amet</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Exercitationem, dignissimos ipsam? Provident culpa quidem repudiandae fuga ea accusantium nisi iusto asperiores sapiente, nostrum illum facilis cumque totam officiis nam expedita!</p>
        </section>
        <section>
            <h1>Lorem ipsum</h1>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptas facere quia officiis ducimus nihil error ab ratione vero recusandae sit rerum repudiandae, perspiciatis sint omnis cum voluptatem sed! Explicabo, qui?</p>
            <h2>Lorem ipsum dolor sit amet consectetur adipisicing elit</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Est ea a debitis ex numquam laborum inventore reiciendis, maxime fugit reprehenderit assumenda necessitatibus nisi, nihil aliquid amet aut repellat! Autem, odio.</p>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolorem magnam in nam voluptas rerum sed exercitationem, illum earum delectus accusantium! Nostrum, soluta quo odit velit enim blanditiis culpa omnis quaerat.</p>
        </section>
    </main>
</body>
</html>
```
{% endtab %}
{% endtabs %}

Med flex räcker det att sätta det överliggande elementet till flex.

{% tabs %}
{% tab title="CSS" %}
```css
main {
    display: flex;
}
```
{% endtab %}
{% endtabs %}

Vi kan sedan ge varje section lite horisontell white-space för att öka sidans läsbarhet.

```text
section {
    padding: 0rem 2rem;
}
```

### Riktning

Sidan kommer nu att flexa i riktningen\(eng. direction\) rader\(row\) då det är standard-inställningen för flex. Vi kan styra detta med flex-direction egenskapen. Genom att sätta flex-direction till column så placeras inte längre sektionerna bredvid varandra. Detta kan vara användbart om vi önskar ändra layouten med till exempel media regler, men det låter oss även ändra ordningen med reverse värden.

{% tabs %}
{% tab title="CSS" %}
```css
main {
    display: flex;
    flex-direction: column;
}
```
{% endtab %}
{% endtabs %}

### Orientering

{% hint style="info" %}
Flex är det universella svaret på frågan, "hur centrerar jag elementet". Flex med justify-content: center och align-items:center. 
{% endhint %}

En av de stora styrkorna med flex är att vi kan styra över elementens orientering \(engelska alignment\). Med flex blir det väldigt mycket enklare att centrera och flytta element. Studera och kopiera följande kod för en navbar.

{% tabs %}
{% tab title="HTML" %}
```markup
<nav>
    <a href="#">Logotyp</a>
    <ul>
        <li>Hem</li>
        <li>Om</li>
        <li>Kontakt</li>
    </ul>
</nav>
```
{% endtab %}
{% endtabs %}

Utan CSS och flex så är resultatet en länk följd av tre list-items. De är vertikalt placerade tillsammans eftersom det är [block](../html/html-spraket.md#block-och-inline-element) element. En vanlig lösning på detta är att sätta li elementen till display: inline, för att slippa radbrytningen. Vi kan istället göra detta med flex och på så vis få mycket större kontroll.

{% tabs %}
{% tab title="CSS" %}
```css
ul {
    display: flex;
    list-style: none;
}
li {
    padding: 0 1rem;
}
```
{% endtab %}
{% endtabs %}

För att sedan placera detta bredvid Logotyplänken så kan vi åter igen använda flex och ändra orienteringen.

{% tabs %}
{% tab title="CSS" %}
```css
nav {
    display: flex;
    justify-content: space-between;
}
```
{% endtab %}
{% endtabs %}

Navbaren bör nu vara separerad så att logon är till vänster och text-listan till höger. Prova gärna att ändra justify-content till andra värden. För vertikal justering så kan du prova align-items: värde. Vi ska försöka att få till centreringen med en logotyp.

Som logotyp kan du använda en valfri bild, exemplet kommer använda hem ikonen från [Google icons ](https://fonts.google.com/icons)med måtten 48x48. Ikonen är sparad som SVG.

{% tabs %}
{% tab title="HTML" %}
```markup
<a href="#">
    <svg xmlns="http://www.w3.org/2000/svg" height="48px" viewBox="0 0 24 24" width="48px" fill="#000000">
        <path d="M0 0h24v24H0V0z" fill="none"/>
        <path d="M12 5.69l5 4.5V18h-2v-6H9v6H7v-7.81l5-4.5M12 3L2 12h3v8h6v-6h2v6h6v-8h3L12 3z"/>
    </svg>
</a>
```
{% endtab %}

{% tab title="CSS" %}
```css
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```
{% endtab %}
{% endtabs %}

### Media regler

{% hint style="info" %}
Läs mer om media regler i [kapitlet om responsiv design](../design/responsiv-design.md).
{% endhint %}

Som sista del så ska vi mobilanpassa den layout vi skapat. För att göra det så vill vi inte visa spalter på mindre skärmar och navbar-menyn ska vara vertikal.

{% tabs %}
{% tab title="CSS" %}
```css
@media (max-width: 567px) {
    main {
        flex-direction: column;
    }
    ul {
        flex-direction: column;
        padding-left: 0;
    }
    nav{
        flex-direction: column;
        align-items: flex-start;
    }
}
```
{% endtab %}
{% endtabs %}

Med en media regel för max-bredd så kan vi styra elementen att visas på ett annat sätt på en mindre skärm.

