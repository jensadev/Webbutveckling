# Språket

## Vad är HTML?

Hypertext Markup Language(**HTML**)är inte ett **programmeringsspråk.** HTML är ett märkspråk skapat för att berätta för webbläsaren hur en sida är strukturerad. Språket följer en [levande standard](https://html.spec.whatwg.org). HTML består av element som märker upp text. Texten märks upp med elementets tillhörande taggar.&#x20;

{% tabs %}
{% tab title="Plain text" %}
```
En paragraf med text.
```
{% endtab %}

{% tab title="HTML" %}
```markup
<p>En paragraf med text i html.</p>
```
{% endtab %}
{% endtabs %}

### Element

I exemplet ovan så används paragraf-elementet. Som de flesta HTML element består det av tre delar.

* Öppningstaggen
  * Indikerar vars elementet börjar. Det använder mindre än tecken, elementets namn och större än tecken.
* Innehåll
  * Det innehåll som elementet ska visa (innehålla).
* Stängnigstaggen
  * Indikerar vars elementet slutar. Det använder mindre än tecken, snedstreck (front slash), elementets namn och större än tecken.&#x20;

{% hint style="info" %}
HTML är ett otroligt robust språk då webbläsaren tolkar alla element och visar dess innehåll, även om det är element som inte finns. Testa att märka upp text med \<finnsinte>.
{% endhint %}

#### Nästla element

I HTML kan element placeras inuti andra element, det kallas för att **nästla**(engelska **nesting**) element.

{% tabs %}
{% tab title="HTML" %}
```markup
<p>Det här är <strong>otroligt</strong> viktigt att förstå.</p>
```
{% endtab %}
{% endtabs %}

#### Block- och inline-element

Det finns två kategorier av element, **block-element **och **inline-element**.

* Block-element skapar ett tydligt block på en sida. Block-element börjar på en ny rad efter det innehåll som finns före det. Efter ett block-element kommer en radbrytning. Block-element är ofta strukturella element på en sida.
* Inline-element är innehåll i block element. Inline-element är oftast en mindre del av en sida. Inline-element börjar eller slutar inte med en radbrytning.

I exemplet ovan är p ett block-element och strong är ett inline-element.

#### Tomma element

Vissa element följer inte mönstret med öppningstagg, innehåll, stängningstagg. De elementen kallas för tomma element. De används framförallt för att lägga till innehåll, till exempel bilder.&#x20;

{% tabs %}
{% tab title="HTML" %}
```markup
<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png">
```
{% endtab %}
{% endtabs %}

## Attribut

Attribut innehåller extra information om elementet som inte är innehåll.

## Semantik

Semantik är grekiska för tecken. I HTML används **semantiska element** för att beskriva innehållet. Elementet ska vara meningsbärande. Detta enligt [W3C dokument](https://www.w3.org/standards/semanticweb/).

De flesta element i HTML är semantiska. Semantiska element hjälper oss utvecklare att förstå koden, men det hjälper även webbläsaren att förstå och presentera strukturen. Rubrik-element får till exempel en större och fetare stil än en paragraf.

Studera följande exempel och försök dra slutsatser kring innehållet. Om du vill, testa det i en webbläsare för att se skillnaden.

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



