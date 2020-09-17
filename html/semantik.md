# Semantik

Semantik är grekiska för tecken. I HTML används **semantiska element** för att beskriva innehållet. Elementet ska vara meningsbärande.

Studera följande exempel och försök dra slutsatser kring innehållet.

{% tabs %}
{% tab title="HTML" %}
```markup
<!-- Utan semnatiska element -->
<div>
    <a href="#">Hem</a>
    <a href="#">Om</a>
</div>
<div>
    Lorem ipsum
    <br>
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusantium voluptates eos accusamus incidunt recusandae nemo quidem. Doloremque repudiandae adipisci debitis. Nobis aliquid, dolorum quis pariatur harum neque. Quas, reiciendis ducimus.
    <br>    
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit voluptas earum perspiciatis, tempore, eum, iusto porro est totam sit explicabo facilis asperiores non libero ea dolor consequuntur atque sequi fuga?
</div>
```
{% endtab %}

{% tab title="HTML" %}
```markup
<!-- Med semantiska element -->
<nav>
    <ul>
        <li>
            <a href="#">Hem</a>
        </li>
        <li>
            <a href="#">Om</a>
        </li>
    </ul>
</nav>
<main>
    <h1>Lorem ipsum</h1>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusantium voluptates eos accusamus incidunt recusandae nemo quidem. Doloremque repudiandae adipisci debitis. Nobis aliquid, dolorum quis pariatur harum neque. Quas, reiciendis ducimus.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit voluptas earum perspiciatis, tempore, eum, iusto porro est totam sit explicabo facilis asperiores non libero ea dolor consequuntur atque sequi fuga?</p>
</main>
```
{% endtab %}
{% endtabs %}



