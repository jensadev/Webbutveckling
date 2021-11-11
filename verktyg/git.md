---
description: Introduktion till Git och Github
---

# Git

## GitHub

[Git](https://git-scm.com) är ett **versions-hanteringssystem** för projekt och [GitHub](https://github.com) är en **utvecklarplattform** för att arbeta med Git som ägs av Microsoft. GitHub är en plattform som är värd för alla möjliga olika arbeten med kod.

### Varför?

GitHub är något som skolan använder i alla programmeringskurser. Anledningen till det är att Git är ett utmärkt verktyg för att se:

* Progression
* Arbete
* Förståelse
* Dokumentation

GitHub låter både lärare och elever att dela kod. GitHub ger även utmärkta möjligheter till samarbete och att lära av varandra. Github är även ett välkänt och väldigt ofta förekommande verktyg i arbetslivet.

GitHub Classroom. kommer även att användas som komplement till Google Classroom i kursen.

{% hint style="info" %}
&#x20;Registrera ett konto på [GitHub](https://github.com).
{% endhint %}

### Installation

GitHub finns både som **desktop**- och **command line** (**cmd) **applikation . Oavsett vilken **klient** du ska använda så behöver du ladda ned och installera den.

{% hint style="info" %}
Hämta desktop-klienten här, [https://desktop.github.com/](https://desktop.github.com).
{% endhint %}

{% content-ref url="git-commandline.md" %}
[git-commandline.md](git-commandline.md)
{% endcontent-ref %}

## Ditt första repository

{% hint style="info" %}
Börja med desktop-klientens tutorial.
{% endhint %}

Ett **repository (**eller **repo**), är en** **folder som innehåller information om ett Git-projekt. Ett repo kan kopplas till en sida på GitHub. Där finns filerna för projektet tillsammans med annat. Github sparar webb-adressen (**Unifrom Resource Locator, URL**) till repos enligt samma mönster.

{% hint style="info" %}
github.com/username/repository-namn
{% endhint %}

För att skapa ett nytt repo med desktop-klienten, klicka på **+ Create a New...**

![GitHubs desktop-klient, det blåmarkerade är start-tutorialen.](https://lh6.googleusercontent.com/TpP2mAMNVohIZ8sSTCgSdI8WyqAm5UaoD-hhy4FpJ5GAeuu8N58mRL-pxQK5gByqLHkuh8DV\_ySIg7Y4DuYPL88hZWGvExwL8RqLeLAd-oDk4W4mk-PnxAxwqKUP2zpEVfSKYUuI)

Ett repo kan även skapas på Github.com. För att koppla det till desktop-klienten klicka "Add an Existing...".

1. Surfa till [https://github.com/](https://github.com).
2. Logga in med ditt konto.
3. Klicka på + i menyn.
4. Välj, New repository.
5. Skriv in ett namn.
6. Klicka på Create.

## Att använda Github

Git är ett versionshanteringssystem, med det menas att det håller reda på filer, filernas innehåll och ändringar. Repot sköter det lokalt på en dator och det kan synkas mot GitHub.

{% hint style="info" %}
Det är god praxis att spara all kod på ett samlat ställe.
{% endhint %}

Först ska du skapa en mapp på din dator där du kan spara all kod. Öppna Utforskaren (Explorer) och skapa en ny **mapp **(folder) i c:\\

![Skapa en code mapp i c: med hjälp av Utforskaren.](../.gitbook/assets/mapp.png)

[Klicka här om du vill hoppa till avsnittet för cmd](git.md#git-cmdline).

### Github desktop

Skapa först ett nytt repo.

![Skapa ett nytt repo.](../.gitbook/assets/cnew.png)

Publicera sedan ditt repo till Github, det kommer då att skapas ett repo på Githubs webbsida som kopplas till det lokala repot. Viktigt i arbetet mellan lokal dator och Github är att filerna är synkroniserade, annars kan det bli [problem](git.md#problem-och-att-loesa-dem).

![Publicera på GitHub.](../.gitbook/assets/pub.png)

Använd sedan **Visual Studio Code** (**vscode**) för att öppna ditt repo. Antingen genom knappen i desktop-klienten, eller i vscode genom att välja Open Folder i File-menyn.

Skapa sedan en ny fil i vscode. Redigera filen och spara som README.md

{% code title="README.md" %}
```bash
# Hallå världen
Hej
```
{% endcode %}

Readme-filen är en standard i repon. I filen skrivs information kring projektet och GitHub visar den automatiskt på projektets sida. Filen skrivs i märkspråket [Markdown](https://guides.github.com/features/mastering-markdown/) (**MD**).

Nu när vi har ändringar i filen så kan vi hoppa över till klienten igen. Vi ser där en lista över våra ändringar.  Klicka sedan Commit to master och efter det Push origin. Du har nu laddat upp dina lokala ändringar till GitHub.

{% hint style="danger" %}
Här förutsätts det att du inte har gjort några ändringar på github.com, du kommer annars få konflikter.
{% endhint %}

### Commit

**Commits **är kärnan i att arbeta med GIthub. Du arbetar med filer på **local**. När du arbetat färdigt med filerna så behöver du först lägga till dem, **add**, sedan **commit**. Det sista steget är **push** för att skicka filerna till **remote**, alltså Github.

{% hint style="info" %}
Github training, Commits, [https://youtu.be/A-Cll9jEnnM](https://youtu.be/A-Cll9jEnnM).
{% endhint %}

### Problem och att lösa dem

Git ett versionshanteringssystem, detta kan leda till att det blir konflikter (**issues**) mellan olika versioner av filer. Git måste bestämma vilken version av filen som ska användas och vad den ska innehålla. För att du ska lära dig hantera en sådan konflikt ska du först få skapa en, för att sedan lösa den.

Börja på Github.com. Redigera (**edit**) README-filen. Gör en eller flera ändringar och välj sedan **Commit changes**.

![Redigera och commita ändringar på GitHub](../.gitbook/assets/commit.png)

{% hint style="info" %}
Det finns nu ett sätt att undvika problem och det är att göra **Fetch origin** följt av **Pull origin**. Då hämtar Git-klienten ändringarna som gjorts från GitHub. Gör du det innan du börjar arbeta med filerna så kommer du förhoppningsvis kunna undvika konflikter av denna typ (**merge issues**).
{% endhint %}

Om en konflikt uppstår måste du kunna lösa problemet för att kunna fortsätta arbeta med Git. För att testa detta.

* Redigera README-filen på remote (Github.com)
* Redigera README-filen på local (din dator)
* Kom ihåg att spara

{% code title="README.md" %}
```bash
# Hallå där!
Hej

Detta är ändringar som inte finns på origin och origin har ändrats!
```
{% endcode %}

Välj sedan **Commit to master** i klienten. Klienten varnar då om att origin behövers hämtas (pull).&#x20;

![Klienten förklarar vad nästa steg är](../.gitbook/assets/pull.png)

En konflikt av typen merge issue har nu uppståt och måste lösas (**resolve**).

![Klienten varnar om konflikten](../.gitbook/assets/resolve.png)

Det du nu behöver göra är att öppna filen i code. Detta för att lösa denna konflikt. I code så kommer då de ändringar som gjorts visas. Du behöver välja vilka ändringar i filen du ska spara. Välj och spara sedan filen.

![Vscode fungerar tillsammans med Git för att underlätta arbetet](../.gitbook/assets/changes.png)

Konflikt-dialogen i klienten uppdateras när filen eller filerna redigerats. Konflikten är då löst och ändringarna behöver commitas. Avsluta med att pusha.

![Konflikten är löst](../.gitbook/assets/resolved.png)

Git konflikter kan ta olika form, men det här är hur du löser en typ av dem.

{% hint style="info" %}
Vscode kan också användas för att jobba mot GitHub. Då används Source Control tabben.
{% endhint %}

## Branches

**Branches** (svenska, grenar) är ett sätt att arbeta med Git. Namnet kommer från den trädstruktur som Git har.

> &#x20;**Branching** is the way to work on different versions of a repository at one time.

Som standard har alla repos en branch som heter **main**. Hittils har allt arbete du gjort skett i main. Det är något som generellt bör undvikas av olika skäl. Att arbeta i main kan leda till säkerhetsproblem, dataförlust och annat. Därför är det bra att arbeta i en annan gren.

{% hint style="info" %}
Github training, Branch, [https://youtu.be/H5GJfcp3p4Q](https://youtu.be/H5GJfcp3p4Q).
{% endhint %}

## Läs mer

* Cheat sheet, [https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
* Hello world på GitHub, [https://guides.github.com/activities/hello-world/](https://guides.github.com/activities/hello-world/)
* Understanding flow, [https://guides.github.com/introduction/flow/](https://guides.github.com/introduction/flow/)
* Pages, [https://guides.github.com/features/pages/](https://guides.github.com/features/pages/)
* [https://guides.github.com/](https://guides.github.com)
* [https://help.github.com/en/github/getting-started-with-github](https://help.github.com/en/github/getting-started-with-github)
* [https://www.youtube.com/playlist?list=PLg7s6cbtAD15G8lNyoaYDuKZSKyJrgwB-](https://www.youtube.com/playlist?list=PLg7s6cbtAD15G8lNyoaYDuKZSKyJrgwB-)

