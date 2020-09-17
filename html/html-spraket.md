# Språket

## Vad är HTML?

Hypertext Markup Language\(**HTML**\)är inte ett **programmeringsspråk.** HTML är ett märkspråk skapat för att berätta för webbläsaren hur en sida är strukturerad. HTML består av element som märker upp text. Texten märks upp med elementets tillhörande taggar. 

{% tabs %}
{% tab title="Plain text" %}
```text
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

I exemplet ovan så används paragraf elementet. Som de flesta HTML element består det av tre delar.

* Öppningstaggen
  * Indikerar vars elementet börjar. Det använder mindre än tecken, elementets namn och större än tecken.
* Innehåll
  * Det innehåll som elementet ska visa \(innehålla\).
* Stängnigstaggen
  * Indikerar vars elementet slutar. Det använder mindre än tecken, snedstreck \(front slash\), elementets namn och större än tecken. 

{% hint style="info" %}
HTML är ett otroligt robust språk då webbläsaren tolkar alla element och visar dess innehåll, även om det är element som inte finns. Testa att märka upp text med &lt;finnsinte&gt;.
{% endhint %}

#### Nästla element

I HTML kan element placeras innuti andra element, det kallars för att **nästla**\(engelska **nesting**\) element.

{% tabs %}
{% tab title="HTML" %}
```markup
<p>Det här är <strong>otroligt</strong> viktigt att förstå.</p>
```
{% endtab %}
{% endtabs %}

#### Block- och inline-element

Det finns två kategorier av element, **block** element och **inline** element.

* Block element skapar ett tydligt block på en sida. Block element börjar på en ny rad efter det innehåll som finns före det. Efter ett block element kommer en radbrytning. Block element är ofta strukturella element på en sida.
* Inline element är innehåll i block element. Inline element börjar eller slutar inte med en radbrytning.

I exemplet ovan är p ett block element och strong är ett inline element.

#### Tomma element

Vissa element följer inte mönstret med öppningstagg, innehåll och stängningstagg. De elementen kallas för tomma element. De används framförallt för att lägga till något annat i koden, till exempel bilder. 

{% tabs %}
{% tab title="HTML" %}
```markup
<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png">
```
{% endtab %}
{% endtabs %}

## Attribut

Attribut innehåller extra information om elementet som inte är innehåll.

