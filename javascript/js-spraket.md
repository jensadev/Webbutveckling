# Språket

## Variabler

En variabel är en behållare för att spara värden i. En variabel kan deklareras i javascript med nyckelorden `var `eller `let`, av de två så är `let `att föredra.

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

| Datatyp | Förklaring                                                                                                                                                                                      | Exempel                                                               |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| String  | <p>En sekvens av tecken bilder en sträng. </p><p>En sträng är lätt att känna igen då värdet</p><p>alltid är omgivet av enkel- eller dubbel-fnuttar.</p>                                         | <p>let myvar = 'Bengt';</p><p>let myvar = "Åke";</p>                  |
| Number  | Ett nummer. Kan även vara i decimalform.                                                                                                                                                        | let myvar = 10;                                                       |
| Boolean | Har värdet true eller false.                                                                                                                                                                    | let myvar = true;                                                     |
| Array   | <p>En datastruktur som låter dig spara flera värden i</p><p>samma variabel. Känns igen på hakparenteser </p><p>(eng. squarebrackets). Värden hämtas genom att</p><p>ange dess index-plats. </p> | <p>let myvar = [1, 2];</p><p>myvar[0];</p>                            |
| Object  | <p>Väldigt mycket i javascript kan vara object och </p><p>kan då sparas i en variabel. Det kan vara allt från</p><p>en object literal till ett html element.</p>                                | <p>let myvar = {</p><p>    name : "Åke"</p><p>}</p><p>myvar.name;</p> |

## Operatorer

| Operator                                                 | Symbol   | Förklaring                                                              |
| -------------------------------------------------------- | -------- | ----------------------------------------------------------------------- |
| Addition                                                 | +        | Addera två tal eller konkatenera en sträng.                             |
| <p>Subtraktion,</p><p>multiplikation,</p><p>division</p> | -, \*, / | Som i matematiken.                                                      |
| Tilldelning                                              | =        | Används för att tilldela en variabel ett värde.                         |
| Likamed                                                  | ===      | Undersök om två värden är densamma.                                     |
| Inte, inte likamed                                       | !, !==   | <p>För att undersöka om något inte är, eller inte</p><p>är likamed.</p> |

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
