# Text

## Struktur

Strukturerad text följer för det mesta samma mönster, den består av rubriker och paragrafer. Strukturerad text är mer lättläst och gör läsandet roligare.

{% hint style="info" %}
Ett exempel är det här materialet, förhoppningsvis gör sidans struktur det mer lättläst och enklare att förstå.
{% endhint %}

**HTML** innehåller element för att märka upp text utifrån detta mönster. 

För att märka upp en **paragraf**\(engelska **paragraph**\) så används `<p>` elementet.

{% tabs %}
{% tab title="HTML" %}
```markup
<p>P elementet är för att märka upp en paragraf.</p>
```
{% endtab %}
{% endtabs %}

För att skapa en rubrik\(engelska **heading**\) finns det sex olika element att välja mellan, `<h1>` , `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`. Siffrorna i heading-elementet representerar olika rubrik-nivåer där `<h1>` är huvudrubriken.

{% tabs %}
{% tab title="HTML" %}
```markup
<h1>Detta är en huvudrubrik för sidan.</h1>
<h2>Följt av en underrubrik.</h2>
```
{% endtab %}
{% endtabs %}

Genom att märka upp text så skapas en struktur på sidan. Strukturen på texten låter användaren skanna av texten snabbare och uppfatta det som väcker intresse och är relevant. Strukturen underlättar också för sökmotorer som indexerar webbsidan, en bra strukturell hierarki ger bättre resultat. Strukturen är även avgörande för webbsidans tillgänglighet.

## Ett kapitel

Böcker är ett utmärkt exempel på strukturerad text. Se följande exempel, ett utdrag från Bram Stokers [Dracula](https://www.gutenberg.org/files/345/345-h/345-h.htm).

{% tabs %}
{% tab title="Plain Text" %}
```text
D R A C U L A
CHAPTER I

JONATHAN HARKER’S JOURNAL
(Kept in shorthand.)

3 May. Bistritz.—Left Munich at 8:35 P. M., on 1st May, arriving at Vienna early next morning; should have arrived at 6:46, but train was an hour late. Buda-Pesth seems a wonderful place, from the glimpse which I got of it from the train and the little I could walk through the streets. I feared to go very far from the station, as we had arrived late and would start as near the correct time as possible. The impression I had was that we were leaving the West and entering the East; the most western of splendid bridges over the Danube, which is here of noble width and depth, took us among the traditions of Turkish rule.
```
{% endtab %}

{% tab title="HTML" %}
```markup
<h1>D R A C U L A</h1>
<h2>CHAPTER I</h2>
<h3>JONATHAN HARKER’S JOURNAL</h3>
<p>(Kept in shorthand.)</p>
<p>3 May. Bistritz.—Left Munich at 8:35 P. M., on 1st May, arriving at Vienna early next morning; should have arrived at 6:46, but train was an hour late. Buda-Pesth seems a wonderful place, from the glimpse which I got of it from the train and the little I could walk through the streets. I feared to go very far from the station, as we had arrived late and would start as near the correct time as possible. The impression I had was that we were leaving the West and entering the East; the most western of splendid bridges over the Danube, which is here of noble width and depth, took us among the traditions of Turkish rule.</p>
```
{% endtab %}
{% endtabs %}

Studera exemplet och notera mönstret med elementen och vad de representerar. Rubrikerna och paragraferna har en semantisk betydelse vilket är viktigt. Elementet `<h1>` betyder att det är en huvudrubrik, elementets benämning bär en mening.

### Övning

Använd vscode för att skapa ett nytt HTML-dokument och strukturera följande text. 

{% tabs %}
{% tab title="Plain Text" %}
```text
CHAPTER II

JONATHAN HARKER’S JOURNAL—continued
5 May.—I must have been asleep, for certainly if I had been fully awake I must have noticed the approach of such a remarkable place. In the gloom the courtyard looked of considerable size, and as several dark ways led from it under great round arches, it perhaps seemed bigger than it really is. I have not yet been able to see it by daylight.

When the calèche stopped, the driver jumped down and held out his hand to assist me to alight. Again I could not but notice his prodigious strength. His hand actually seemed like a steel vice that could have crushed mine if he had chosen. Then he took out my traps, and placed them on the ground beside me as I stood close to a great door, old and studded with large iron nails, and set in a projecting doorway of massive stone. I could see even in the dim light that the stone was massively carved, but that the carving had been much worn by time and weather. As I stood, the driver jumped again into his seat and shook the reins; the horses started forward, and trap and all disappeared down one of the dark openings.
```
{% endtab %}
{% endtabs %}

## Inline element för text

Text märks inte enbart upp med block-element som ger dem struktur, utan det finns även ett antal inline-element för att formatera texten. Några av elementen är semantiska, de ger mening till formateringen, medans andra är rent visuella.

För att visa att något ord är extra viktigt så kan vi **betona** det.

{% tabs %}
{% tab title="HTML" %}
```markup
<p>Det är viktigt att <strong>fokusera</strong> när du ska lära dig något.</p>
```
{% endtab %}
{% endtabs %}

I exemplet ovan så används taggen strong inuti ett p-element, det är nästlat. Strong-elementet är ett inline-element så det blir ingen radbrytning kring det vilket är viktigt.

För att rent visuellt märka upp text, med **fetstil** och _kursiv stil_ så används element utan semantisk mening. 

{% tabs %}
{% tab title="HTML" %}
```markup
<p>Jag har köpt ett paket <b>Mirakel-flingor</b>. Flingorna är det <i>bästa</i>!</p>
```
{% endtab %}
{% endtabs %}

## Listor

Listor finns överallt i text, att göra listor, handlarlistor och så vidare, du använder dem säkert. Listor kan antingen vara oordnade eller ordnade. En handlarlista kanske inte behöver en speciell ordning, men skriver du en instruktion så kan det vara avgörande att det sker i rätt ordning.

Listor på webben används ofta till annat än det som visuellt kanske kan ses som en lista. De används ofta för att skapa struktur i till exempel menyer.

### Oordnade listor

Listor där ordningen inte spelar något roll.

{% tabs %}
{% tab title="Plain Text" %}
```text
Banan
Äpple
Apelsin
Kiwi
```
{% endtab %}

{% tab title="HTML" %}
```markup
<ul>
  <li>Banan</li>
  <li>Äpple</li>
  <li>Apelsin</li>
  <li>Kiwi</li>
</ul>
```
{% endtab %}
{% endtabs %}

En lista startar med med elementet för listans typ, **unordered** **list** har elementet `<ul>`. Varje element i listan blir sedan ett `<li>` element.

### Ordnade listor

Ordnade listor är listor där ordningen är viktig och det visas också av att det som standard blir en numrerad lista. Elementet för **ordered list** är `<ol>`. Varje enskilt element i listan märks sedan upp med `<li>`.

{% tabs %}
{% tab title="Plain Text" %}
```text
Ta fram stekpannan.
Lägg i en klick smör och låt det smälta.
Häll i ca. 1dl smet.
Stek pannkakan.
```
{% endtab %}

{% tab title="HTML" %}
```markup
<ol>
    <li>Ta fram stekpannan.</li>
    <li>Lägg i en klick smör och låt det smälta.</li>
    <li>Häll i cirka 1dl smet.</li>
    <li>Stek pannkakan.</li>
</ol>
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Notera indragen\(indenteringen, engelska indentation\) i listan, det är viktigt att du arbetar så för att koden ska bli tydlig och läsbar.
{% endhint %}

## Datum

För att märka upp datum finns elementet `<time>`. Detta är väldigt praktiskt för att det finns väldigt mångas olika format att skriva ett datum. Format som kanske en människa begriper, men inte en dator.

{% tabs %}
{% tab title="HTML" %}
```markup
<time datetime="05-03">3 May</time>
<time datetime="T20:35">8:35 P. M.</time>
```
{% endtab %}
{% endtabs %}

## Övning

1. Skapa en ny HTML fil och döp den till dracula.html. 
2. Kopiera två kapitel från [Dracula](https://www.gutenberg.org/files/345/345-h/345-h.htm) och märk upp texten med HTML element. 
   1. Använd alla verktygen du lärt dig. Rubriker, paragrafer, tid.
3. Skapa en innehållsförteckning med en lista.

