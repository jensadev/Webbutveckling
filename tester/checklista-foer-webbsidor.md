---
description: >-
  Gå igenom följande punkter. Dokumentera kortfattat eventuella fel, vad de
  beror på och lösningen.
---

# Checklista för Webbsidor

Innan du lämnar in projekt och arbeten är det bra att testa det. En del tester bör köras tidigt och ofta \(validering\) medans andra lämpar sig bättre i projektets slut. I den här listan som följer är sådant som du hela tiden bör ha i åtanke i ditt webbutvecklingsprojekt. Arbeta kontinuerligt med punkterna och dokumentera det.

## Hosting

* Sidan hostas med Github pages.
  * Alla resurser fungerar och använder **relativa** sökvägar.
  * Alla länkar fungerar.
  * Sidans innehåll och resurser hostas lokalt på Git eller använder en CDN.
* Inga bilder eller annat är länkade till andra webbplatser.

### Om sidan innehåller serverkod

* Hosta all kod som behövs för att sidan ska fungera på Git.
  * Men inte känsliga uppgifter.
* Exportera och bifoga eventuell databas.
  * Om en gemensam databas använts, se till att din kod använder den.
* Skriv tydliga instruktioner för hur det ska gå att köra sidan.
  * Testkör detta, det ska inte krävas felsökning för att få det att fungera.
* Om möjligt:
  * Hosta på skolan.
  * Kör hostingtjänst enligt kurs.
    * [Heroku](https://www.heroku.com/).

## Manuell granskning

* Sidan fungerar i ett par webbläsare.
* Sidan fungerar på telefon.
  * Använd Git pages. live eller lokal server för att testa.
* Kolla av checklistan, [https://webbriktlinjer.se/testa-din-webbplats/  ](https://webbriktlinjer.se/testa-din-webbplats/).

## Lagar och regler

* Sidan följer alla relevanta lagar och regler för publicering på webben.
  * Personuppgifter, GDPR.
  * Copyright.

## Validering

* Alla sidans dokument validerar som korrekt HTML  .
  * [https://validator.nu/    ](https://validator.nu/).
* All CSS validerar som korrekt CSS.
  * [https://jigsaw.w3.org/css-validator/    ](https://jigsaw.w3.org/css-validator/).

## Design

Försök att kontinuerligt utvärdera sidans design, framförallt om den är din egen. Var inte rädd för att ändra om det inte fungerar. 

* Skissa.
* Gör prototyper.
* Utvärdera.
* Testa användbarheten.

## Media

* Sidans media är optimerat.
* Bildstorlek och upplösning.
  * Ska bilden var 32 px x 32 px ska den vara det, inte 1920 x 1080    .
* Bildens format är anpassat efter bildtyp.
  * Inga bmp eller tga filer, är det rimligt att köra png 32 på porträtt?
  * SVG och vektorformat där det passar.
  * PNG där storleken tillåter
  * JPEG på foto.
* Sidans totala storlek är rimlig.
  * Devtools, throttle network, testa.

## Tillgänglighet

* Sidan har testats med Wave.
  * [https://wave.webaim.org/    ](https://wave.webaim.org/).
  * Finns även som extension.
* Arbete är gjort för att begränsa och åtgärda kontrast-varningar.
  * Motivera.
* Sidan använder semantiska strukturelement.
* Sidan är begriplig och fungerar utan:
  * CSS.
  * Javascript.

{% hint style="danger" %}
Sidan du skapat är inte en katastrof enligt [https://webbriktlinjer.se/riktlinjer/](%20https://webbriktlinjer.se/riktlinjer/).
{% endhint %}

## Helhet

* I chrome devtools, kör audits med [Lighthouse](https://developers.google.com/web/tools/lighthouse) för sidan.
* Åtgärda fel, kontrollera och fixa.
  * Du kan bortse från  PWA    .



