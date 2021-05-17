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

### Direction

Sidan kommer nu att flexa längs row, då det är standard-inställningen för flex. Vi kan styra detta med flex-direction egenskapen. Genom att sätta flex-direction till column så placeras inte längre sektionerna bredvid varandra. Detta kan vara användbart om vi önskar ändra layouten med till exempel media regler, men det låter oss även ändra ordningen med reverse värden.

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



