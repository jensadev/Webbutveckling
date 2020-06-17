# Bilder

> Bilder och media med alternativa format, optimering och tillgänglighet.

## Skärmupplösning

En dators skärm har en [**skärmupplösning**](https://sv.wikipedia.org/wiki/Sk%C3%A4rmuppl%C3%B6sning) och ett **bildförhållande**. Du känner säkert till skärmupplösningen 1920 x 1080 och kanske att det är bildförhållandet 16:9. Det är viktigt att känna till då webbsidor används på många olika **enheter** \(**devices**\). Varje enhet har en skärm med tillhörande upplösning och bildförhållande.

På grund av tekniska begränsningar användes webben enbart från stationära datorer \(desktop\) tidigare men i takt med att tekniken utvecklats är nu mobila-enheter minst lika vanliga.

![Mobila-enheter har st&#xF6;rst marknadsandel enligt statcounter](../.gitbook/assets/statcounter-comparison-ww-monthly-201905-202005.png)

## 

#### Vilken upplösning är vanligast?

Statistik från [statcounter](https://gs.statcounter.com/):

* [Stationär \(desktop\)](https://gs.statcounter.com/screen-resolution-stats/desktop/worldwide)
* [Mobiltelefon](https://gs.statcounter.com/screen-resolution-stats/mobile/worldwide)

## Bildstorlek

### Dimension

Alla bilder som är sparade på en dator har en **bredd** och en **höjd**. Det är vanligt att prata om en bilds **upplösning** \(engelska **resolution**\) men det är något [annat](bilder.md#upploesning). Dimensionerna på en bild kan till exempel vara 320 bred och 240 hög \(skrivs 320 x 240\). Att en bild är 320 bred betyder att den är 320 **pixlar** bred. Pixlar är små fyrkanter som innehåller färginformation.

![Bild-dimensioner och dess storleks-relation](../.gitbook/assets/size-relation.svg)

{% hint style="info" %}
Bilder du använder på webbsidan ska sparas med samma bredd och höjd som de visas med.
{% endhint %}

### Upplösning

Den faktiska [bildupplösningen](https://sv.wikipedia.org/wiki/Bilduppl%C3%B6sning) som en bild har mäts i antalet pixlar som bilden har, då används måtten **Pixels Per Inch** \(**PPI**\) eller **Dots Per Inch** \(**DPI**\). Måttet DPI används för tryck \(utskrift\) och då är det viktigt att bilden har åtminstone **300 DPI** för att bilden ska bli skarp. På skärmar fungerar det annorlunda och en måttstock är att använda **72 PPI** för digitala bilder.

{% hint style="info" %}
Att använda 72 PPI för digitala bilder begränsar bildens filstorlek.
{% endhint %}

### Fil

Alla filer på en dator har en storlek, vilket mäts i bytes. När bilder används på en webbsida så blir det en del av en helhet som måste skickas till användarens enhet. Detta tar bandbredd och påverkar hur snabbt sidan visas. Av den anledning så är det viktigt att begränsa storleken på alla filer.

Bilder är något som kan och ofta tar stor plats, därför är det viktigt att begränsa bildernas filstorlek. Något som spelar stor roll för detta är bildens [format](bilder.md#bildformat).

## Bildformat

Det finns ett stort antal digitala bildformat. Några lämpar sig speciellt väl för webben.

### PNG

### JPEG

### GIF

### SVG

### Webbformat

Det finns ett antal nya experimentella bildformat som används på webben. De optimerar bilder i väldigt hög grad, men de stöds ännu inte av alla webbläsare. När dessa format används är det viktigt att kontrollera i vilka webbläsare det fungerar och erbjuda alternativ.

{% hint style="info" %}
Använd experimentella format med försiktighet
{% endhint %}

## Optimering

Becoming a super hero is a fairly straight forward process:

```
$ give me super-powers
```

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

Once you're strong enough, save the world:

{% code title="hello.sh" %}
```bash
# Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```
{% endcode %}



