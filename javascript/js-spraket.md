# Språket

## Variabler

En variabel är en behållare för att spara värden i. En variabel kan deklareras i javascript med nyckelorden `var` eller `let`, av de två så är `let` att föredra.

{% tabs %}
{% tab title="JavaScript" %}
```javascript
// declare
let myvar;

// assign value
myvar = 'Erik';

// anv / hämta dess värde

myvar; // <- "Erik"

// change assigned value
myvar = 'Frida';
```
{% endtab %}
{% endtabs %}

### Datatyper

En variabels värde kan vara av olika datatyper.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Datatyp</th>
      <th style="text-align:left">F&#xF6;rklaring</th>
      <th style="text-align:left">Exempel</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>En sekvens av tecken bilder en str&#xE4;ng.</p>
        <p>En str&#xE4;ng &#xE4;r l&#xE4;tt att k&#xE4;nna igen d&#xE5; v&#xE4;rdet</p>
        <p>alltid &#xE4;r omgivet av enkel- eller dubbel-fnuttar.</p>
      </td>
      <td style="text-align:left">
        <p>let myvar = &apos;Bengt&apos;;</p>
        <p>let myvar = &quot;&#xC5;ke&quot;;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Number</td>
      <td style="text-align:left">Ett nummer. Kan &#xE4;ven vara i decimalform.</td>
      <td style="text-align:left">let myvar = 10;</td>
    </tr>
    <tr>
      <td style="text-align:left">Boolean</td>
      <td style="text-align:left">Har v&#xE4;rdet true eller false.</td>
      <td style="text-align:left">let myvar = true;</td>
    </tr>
    <tr>
      <td style="text-align:left">Array</td>
      <td style="text-align:left">
        <p>En datastruktur som l&#xE5;ter dig spara flera v&#xE4;rden i</p>
        <p>samma variabel. K&#xE4;nns igen p&#xE5; hakparenteser</p>
        <p>(eng. squarebrackets). V&#xE4;rden h&#xE4;mtas genom att</p>
        <p>ange dess index-plats.</p>
      </td>
      <td style="text-align:left">
        <p>let myvar = [1, 2];</p>
        <p>myvar[0];</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Object</td>
      <td style="text-align:left">
        <p>V&#xE4;ldigt mycket i javascript kan vara object och</p>
        <p>kan d&#xE5; sparas i en variabel. Det kan vara allt fr&#xE5;n</p>
        <p>en object literal till ett html element.</p>
      </td>
      <td style="text-align:left">
        <p>let myvar = {</p>
        <p>name : &quot;&#xC5;ke&quot;</p>
        <p>}</p>
        <p>myvar.name;</p>
      </td>
    </tr>
  </tbody>
</table>

## Operatorer

<table>
  <thead>
    <tr>
      <th style="text-align:left">Operator</th>
      <th style="text-align:left">Symbol</th>
      <th style="text-align:left">F&#xF6;rklaring</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Addition</td>
      <td style="text-align:left">+</td>
      <td style="text-align:left">Addera tv&#xE5; tal eller konkatenera en str&#xE4;ng.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Subtraktion,</p>
        <p>multiplikation,</p>
        <p>division</p>
      </td>
      <td style="text-align:left">-, *, /</td>
      <td style="text-align:left">Som i matematiken.</td>
    </tr>
    <tr>
      <td style="text-align:left">Tilldelning</td>
      <td style="text-align:left">=</td>
      <td style="text-align:left">Anv&#xE4;nds f&#xF6;r att tilldela en variabel ett v&#xE4;rde.</td>
    </tr>
    <tr>
      <td style="text-align:left">Likamed</td>
      <td style="text-align:left">===</td>
      <td style="text-align:left">Unders&#xF6;k om tv&#xE5; v&#xE4;rden &#xE4;r densamma.</td>
    </tr>
    <tr>
      <td style="text-align:left">Inte, inte likamed</td>
      <td style="text-align:left">!, !==</td>
      <td style="text-align:left">
        <p>F&#xF6;r att unders&#xF6;ka om n&#xE5;got inte &#xE4;r, eller inte</p>
        <p>&#xE4;r likamed.</p>
      </td>
    </tr>
  </tbody>
</table>

## Villkorssatser, selektion

{% tabs %}
{% tab title="JavaScript" %}
```javascript
let godis = "bilar";
if (godis === "bilar") {
    console.log("Åh min favorit!");
} else {
    console.log("Amen, nedrans då.");
}
```
{% endtab %}
{% endtabs %}

## Loopar, iteration

## Funktioner

## Events

Events är något vi kan lyssna efter i koden, som ett musklick, en ändring eller tangentbordstryck.

## Ett exempel

I följande exempel använder vi det vi lärt oss hittills.

{% tabs %}
{% tab title="HTML" %}
```markup
<button>Klicka mig!</button>
<script>
let button = document.querySelector('button'); // väljer det första button elementet
let clicks = 0; // number variabel

// använd button, html objektet, och skapa en lyssnare på det
// den ska lyssna på click och när det sker så körs functionen
button.addEventListener('click', function() {
    clicks += 1;
    alert('Du har klickat ' + clicks + ' gånger.');
});
</script>
```
{% endtab %}
{% endtabs %}

