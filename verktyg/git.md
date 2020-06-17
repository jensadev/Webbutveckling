---
description: Introduktion till Git och Github
---

# Git

## GitHub

[**Git**](https://git-scm.com/) är ett **versions-hanteringssystem** för projekt och [**GitHub**](https://github.com/) är en **utvecklarplattform** för att arbeta med Git som ägs av Microsoft. GitHub är en plattform som är värd för alla möjliga olika arbeten med kod.

### Varför?

GitHub är något som skolan använder i alla programmeringskurser. Anledningen till det är att Git är ett utmärkt verktyg för att se:

* Progression
* Arbete
* Förståelse
* Dokumentation

GitHub låter både lärare och elever att dela kod. GitHub ger även utmärkta möjligheter till samarbete och att lära av varandra. Github är även ett välkänt och väldigt ofta förekommande verktyg i arbetslivet.

GitHub Classroom. kommer även att användas som komplement till Google Classroom i kursen.

{% hint style="info" %}
 Registrera ett konto på [GitHub](https://github.com/).
{% endhint %}

### Installation

GitHub finns både som **desktop**- och **command line** \(**cmd\)** applikation . Oavsett vilken **klient** du ska använda så behöver du ladda ned och installera den.

{% hint style="info" %}
Hämta desktop-klienten här, [https://desktop.github.com/](https://desktop.github.com/).
{% endhint %}

#### Om du vill installera cmd Git

För cmd-versionen så laddar du antingen ned [Git portable](https://git-scm.com/download/win), eller kör [WSL](https://jens-andreasson.gitbook.io/webbserverprogrammering/utvecklarmiljo/wsl). Detta är alltså inte en GitHub klient på samma sätt som GitHubs desktop-klient.

{% hint style="info" %}
Ladda ned 64-bit Git portable for Windows, [https://git-scm.com/download/win](https://git-scm.com/download/win).
{% endhint %}

{% hint style="info" %}
Ett _portable_ program är ett program utan installationsfiler. Du laddar ned det, packar\(oftast\) upp det och sedan kan du köra programmet.
{% endhint %}

**PortableGit** är en **körbar** \(**executable, exe**\) fil som låter dig packa upp de filer du behöver. Kör programmet och välj att spara filerna under `c:\tools\portablegit`.

Windows behöver kunna hitta program för att kunna köra dem från cmd \(till exempel **Powershell**\). För det används systemets **PATH**, en global sökväg som går att redigera. För att lägga till ett program i PATH:

1. Starta **Utforskaren** \(**Explorer**\) win+e.
2. Högerklicka på **Den här datorn**, välj **Egenskaper.**
3. Öppna **System och säkerhet, System**    i **Kontrollpanelen.**
4. Välj **Avancerade systeminställningar   .**
5. Klicka på **Miljövariabler   .**
6. Välj **Användarvariabler** för din användare.
7. Dubbelklicka på PATH.
8. Välj **Ny** och skriv in **sökvägen** c:\tools\PortableGit\bin   .
   1. Byt sökväg om du installerar andra program.
9. Starta Powershell   .
10. Kör git, du kommer att se programmets hjälp.
11. Klart.

{% hint style="warning" %}
Efter ändringar i PATH måste cmd-program startas om för att ändringarna ska gälla.
{% endhint %}

## Ditt första repository

{% hint style="info" %}
Börja med desktop-klientens tutorial.
{% endhint %}

Ett **repository \(**eller **repo**\), är en ****folder som innehåller information om ett Git-projekt. Ett repo kan kopplas till en sida på GitHub. Där finns filerna för projektet tillsammans med annat. Github sparar webb-adressen \(**Unifrom Resource Locator, URL**\) till repos enligt samma mönster.

{% hint style="info" %}
github.com/username/repository-namn
{% endhint %}

För att skapa ett nytt repo med desktop-klienten, klicka på **+ Create a New...**

![GitHubs desktop-klient, det bl&#xE5;markerade &#xE4;r start-tutorialen.](https://lh6.googleusercontent.com/TpP2mAMNVohIZ8sSTCgSdI8WyqAm5UaoD-hhy4FpJ5GAeuu8N58mRL-pxQK5gByqLHkuh8DV_ySIg7Y4DuYPL88hZWGvExwL8RqLeLAd-oDk4W4mk-PnxAxwqKUP2zpEVfSKYUuI)

Ett repo kan även skapas på Github.com. För att koppla det till desktop-klienten klicka "Add an Existing...".

1. Surfa till [https://github.com/](https://github.com/).
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

Först ska du skapa en mapp på din dator där du kan spara all kod. Öppna Utforskaren \(Explorer\) och skapa en ny **mapp** \(folder\) i c:\

![Skapa en code mapp i c: med hj&#xE4;lp av Utforskaren.](../.gitbook/assets/mapp.png)

[Klicka här om du vill hoppa till avsnittet för cmd](git.md#git-cmdline).

### Github desktop

Skapa först ett nytt repo.

![Skapa ett nytt repo.](../.gitbook/assets/cnew.png)

Publicera sedan ditt repo till Github, det kommer då att skapas ett repo på Githubs webbsida som kopplas till det lokala repot. Viktigt i arbetet mellan lokal dator och Github är att filerna är synkroniserade, annars kan det bli [problem](git.md#problem-och-att-loesa-dem).

![Publicera p&#xE5; GitHub.](../.gitbook/assets/pub.png)

Använd sedan **Visual Studio Code** \(**vscode**\) för att öppna ditt repo. Antingen genom knappen i desktop-klienten, eller i vscode genom att välja Open Folder i File-menyn.

Skapa sedan en ny fil i vscode. Redigera filen och spara som README.md

```bash
# Hallå världen
Hej
```

Readme-filen är en standard i repon. I filen skrivs information kring projektet och GitHub visar den automatiskt på projektets sida. Filen skrivs i märkspråket [**Markdown**](https://guides.github.com/features/mastering-markdown/) \(**MD**\).

Nu när vi har ändringar i filen så kan vi hoppa över till klienten igen. Vi ser där en lista över våra ändringar.  Klicka sedan Commit to master och efter det Push origin. Du har nu laddat upp dina lokala ändringar till GitHub.

{% hint style="danger" %}
Här förutsätts det att du inte har gjort några ändringar på github.com, du kommer annars få konflikter.
{% endhint %}

### Commit

**Commits** är kärnan i att arbeta med GIthub. Du arbetar med filer på **local**. När du arbetat färdigt med filerna så behöver du först lägga till dem, **add**, sedan **commit**. Det sista steget är **push** för att skicka filerna till **remote**, alltså Github.

{% hint style="info" %}
Github training, Commits, [https://youtu.be/A-Cll9jEnnM](https://youtu.be/A-Cll9jEnnM).
{% endhint %}

### Problem och att lösa dem

Git ett versionshanteringssystem, detta kan leda till att det blir konflikter \(**issues**\) mellan olika versioner av filer. Git måste bestämma vilken version av filen som ska användas och vad den ska innehålla. För att du ska lära dig hantera en sådan konflikt ska du först få skapa en, för att sedan lösa den.

Börja på Github.com. Redigera \(**edit**\) README-filen. Gör en eller flera ändringar och välj sedan **Commit changes**.

![Redigera och commita &#xE4;ndringar p&#xE5; GitHub](../.gitbook/assets/commit.png)

{% hint style="info" %}
Det finns nu ett sätt att undvika problem och det är att göra **Fetch origin** följt av **Pull origin**. Då hämtar Git-klienten ändringarna som gjorts från GitHub. Gör du det innan du börjar arbeta med filerna så kommer du förhoppningsvis kunna undvika konflikter av denna typ \(**merge issues**\).
{% endhint %}

Om en konflikt uppstår måste du kunna lösa problemet för att kunna fortsätta arbeta med Git. För att testa detta.

* Redigera README-filen på remote \(Github.com\)
* Redigera README-filen på local \(din dator\)
* Kom ihåg att spara

{% code title="README.md" %}
```bash
# Hallå där!
Hej

Detta är ändringar som inte finns på origin och origin har ändrats!
```
{% endcode %}

Välj sedan **Commit to master** i klienten. Klienten varnar då om att origin behövers hämtas \(pull\). 

![Klienten f&#xF6;rklarar vad n&#xE4;sta steg &#xE4;r](../.gitbook/assets/pull.png)

En konflikt av typen merge issue har nu uppståt och måste lösas \(**resolve**\).

![Klienten varnar om konflikten](../.gitbook/assets/resolve.png)

Det du nu behöver göra är att öppna filen i code. Detta för att lösa denna konflikt. I code så kommer då de ändringar som gjorts visas. Du behöver välja vilka ändringar i filen du ska spara. Välj och spara sedan filen.

![Vscode fungerar tillsammans med Git f&#xF6;r att underl&#xE4;tta arbetet](../.gitbook/assets/changes.png)

Konflikt-dialogen i klienten uppdateras när filen eller filerna redigerats. Konflikten är då löst och ändringarna behöver commitas. Avsluta med att pusha.

![Konflikten &#xE4;r l&#xF6;st](../.gitbook/assets/resolved.png)

Git konflikter kan ta olika form, men det här är hur du löser en typ av dem.

{% hint style="info" %}
Vscode kan också användas för att jobba mot GitHub. Då används  Source Control tabben
{% endhint %}

### Git command line

Det är bra att ha kunskapr kring hur Git fungerar i cmd. Det här avsnittet repeterar hur du löser en konflikt med Git i cmd.

{% hint style="warning" %}
Skapa en code mapp om du inte har gjort det
{% endhint %}

Använd sedan en terminal \(Powershell, cmd, [WSL](https://jens-andreasson.gitbook.io/webbserverprogrammering/utvecklarmiljo/wsl)\) för att skapa en mapp för ditt repo.

{% hint style="info" %}
Använd samma namn på mappen för repot som repots namn
{% endhint %}

```bash
# I Windows cmdline skriver du
c:
cd \
md code # md är make directory, så använd bara om du inte skapat med Utforskaren
cd code
md wu1-test
cd wu1-test
```

{% hint style="info" %}
För att lista innehållet \(i en mapp\) eller se var i en filstruktur du befinner dig kan du i cmd skriva **dir** \(Windows\) eller **ls** \(Linux\).
{% endhint %}

Skapa sedan ett nytt repo på GitHub, gör det genom att [repetera de här stegen](git.md#ditt-foersta-repository), ge repot namnet **wu1-test**.

![Skapa ett nytt repository-dialogen p&#xE5; GitHub.com](../.gitbook/assets/newrepo.png)

Klicka **Create repository** för att skapa repot. Då kommer **Quick setup** att visas.

{% hint style="info" %}
Om du markerat "Intialize this repository with a README" så kommer inte Quick setup instruktionerna visas.
{% endhint %}

![Quick setup p&#xE5; Github.com](../.gitbook/assets/qset.png)

Quick setup är en lista över de kommandon som behöver köras för att slutföra skapandet av repot. Det skapar även en README-fil. **Om du kopierar Quick setup-koden, var noga med att köra den från rätt mapp!**

```bash
cd c:\code\wu1-test

echo "# wu1-test" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/jensnti/wu1-test.git
git push -u origin master
```

1. echo skriver ut text och med &gt;&gt; så pipar \(skickas informationen, engelska **pipe**\) det texten till en fil. Det skapar filen README.md.
2. git init, initialiserar mappen som ett git repo.
3. git add _filnamn_ lägger till en eller flera filer till repot.
4. git commit -m "meddelande", skapar en commit med ett namn.
5. git remote add origin _github url_, detta kopplar samman git repot med remote origin på GitHub.
6. git push, skickar repots commits till GitHub.

{% hint style="info" %}
Github training, Init, [https://youtu.be/WxMFZncm12s](https://youtu.be/WxMFZncm12s)
{% endhint %}

Om du kört kommandona ovan så har du initierat repot och skapat readme filen. Hade du för bråttom och klistrade in det i c:, leta upp mappen .git i utforskaren och ta bort den. Börja sedan om.

Nästa steg är att redigera en fil och ladda upp det på GitHub.

Starta vscode från cmd genom att skriva.

```bash
code .
```

Öppna filen README.md och redigera den. Använd sedan terminalen igen för att skapa en commit och skicka den till remote.

```bash
git add README.md
git commit -m "Uppdaterade README"
git push
```

{% hint style="warning" %}
Var noga med att läsa vad det står i terminalen, försök lösa eventuella fel
{% endhint %}

Första gången du commitar från cmd så behöver du ange dina användaruppgifter.

```bash
git config user.name "Your Git Username"
git config user.email "your@address.com"
```

Upprepa sedan kommandona för att skapa en commit och skicka den till remote.

```bash
c:\code\wu1-test>git push
Counting objects: 39, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (28/28), done.
Writing objects: 100% (39/39), 5.44 KiB | 928.00 KiB/s, done.
Total 39 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/jensnti/wu1-test.git
 * [new branch]      master -> master
```

### Problem och att lösa dem från cmd

Konflikter kan ske oavsett vilken typ av Git-klient du använder. Precis som i tidigare [avsnitt ](git.md#problem-och-att-loesa-dem)ska du nu få lösa en konflikt, den här gången från cmd.

Synkronisera först ditt lokala repo mot remote.

```bash
git fetch
git pull
```

Öppna repot på GitHub.com. Redigera README.md och commita dina ändringar..

![Redigera README-filen p&#xE5; GitHub](../.gitbook/assets/commit.png)

Öppna vscode och redigera README-filen. Sparan ändringarna och skapa en ny commit.

```bash
git add README.md
git commit -m"uppdatering av readme"
git push
```

Att pusha filerna resulterar i en konflikt \(merge issue\). Felmeddelandet ser ut ungefär såhär.

```bash
To https://github.com/jensnti/wu1-test.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/jensnti/wu1-test.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

Push misslyckades. Var noga med att läsa hela meddelandet, då Git ger tips om hur felet ska lösas.

Kör git pull för att initiera arbetet med att lösa konflikten.

```bash
git pull
```

Eftersom filerna i det lokala repot skiljer sig från filerna på remote kan inte Git automatisk slå ihop dem. Du behöver ange vad, eller vilken version som ska sparas.

```bash
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
```

Använd sedan vscode för att öppna de filer som har konflikter. Vscode hjälper dig att redigera dem och välja vad som ska sparas.

![Redigera de filer som har konflikter och spara](../.gitbook/assets/changes.png)

Spara sedan ändringarna; skapa en ny commit och pusha.

```bash
git add README.md
git commit -m"fixade konflikter"
git push
```

## Branches

**Branches** \(svenska, grenar\) är ett sätt att arbeta med Git. Namnet kommer från den trädstruktur som Git har. Den här guiden visar hur du arbetar med branches i Git cmd.

> **Branching** is the way to work on different versions of a repository at one time.

Som standard har alla repos en branch som heter **master**. Hittils har allt arbete du gjort skett i master. Det är något som generellt bör undvikas av olika skäl. Att arbeta i master kan leda till säkerhetsproblem, dataförlust och annat.

{% hint style="info" %}
Github training, Branch, [https://youtu.be/H5GJfcp3p4Q](https://youtu.be/H5GJfcp3p4Q).
{% endhint %}



#### Skapa en ny branch

Kontrollera att du är i rätt mapp. Fortsätt från det tidigare [test-repot](git.md#git-command-line).

```bash
cd \code
cd wu1-test
git branch feature
git checkout feature
```

Kommandot git branch skapar en ny branch. Git branch följs av namnet på den branch som ska skapas. Git checkout följt av namnet på den branch som ska användas byter branch. Namnet på branchen i det här fallet är feature. Den branch som är vald blir **active** \(svenska, **aktiv**\).

{% hint style="info" %}
GitHub training, Checkout, [https://youtu.be/HwrPhOp6-aM](https://youtu.be/HwrPhOp6-aM).
{% endhint %}

```bash
git branch
# Vilket ger oss en lista av de branches som finns och * för den aktiva
* feature
  master

```

![Aktiv branch i vscode](../.gitbook/assets/branch.png)

{% hint style="danger" %}
Kontrollera alltid att du arbetar i rätt branch.
{% endhint %}

Med branchen feature aktiv. Skapa en ny fil med namnet log.md.

![Ny fil i vscode](../.gitbook/assets/bfile.png)

När arbetet med en branch är färdigt så behöver det commitas och sedan slås ihop \(**merge**\) med master. Det kan göras på två sätt. Allt kan antingen slås ihop lokalt för att sedan pusha det till master. Eller så utförs det på GitHub med en pull request. Det första alternativet fungerar när du arbetar själv på ett projekt, i alla andra fall är det senare att föredra. 

Instruktionerna som följer visar hur du slår ihop dina branches lokalt. För att skapa en pull request, läs Githubs guide [här](https://guides.github.com/activities/hello-world/).

```bash
git branch # kontrollera aktiv branch
git add . # . betyder, lägg till alla filer i mappen
git commit -m "ny fil i ny branch"
```

Kontrollera vilka filer som finns  i mappen med dir eller ls. Byt sedan branch och kontrollera igen.

För att slå ihop branches väljer du först den branch som ska ta emot koden från en branch. Från den aktiva branchen körs kommandot git merge, med namnet på den branch som ska slås ihop till den aktiva.

```bash
git checkout master
git merge feature
```

Om konflikter uppstår så läs felmeddelande och försöka att lösa dem som tidigare.

{% hint style="info" %}
GitHub training, Merge, [https://youtu.be/yyLiplDQtf0](https://youtu.be/yyLiplDQtf0).
{% endhint %}

Efter att de slagits ihop så tar du bort den branch som inte längre används.

```bash
git branch -d feature
```

Att arbeta med branches är GitHubs workflow, läs mer om det i GitHubs material för att få en bättre förståelse för hur det fungerar.

## Läs mer

* Cheat sheet, [https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
* Hello world på GitHub, [https://guides.github.com/activities/hello-world/](https://guides.github.com/activities/hello-world/)
* Understanding flow, [https://guides.github.com/introduction/flow/](https://guides.github.com/introduction/flow/)
* Pages, [https://guides.github.com/features/pages/](https://guides.github.com/features/pages/)
* [https://guides.github.com/](https://guides.github.com/)
* [https://help.github.com/en/github/getting-started-with-github](https://help.github.com/en/github/getting-started-with-github)
* [https://www.youtube.com/playlist?list=PLg7s6cbtAD15G8lNyoaYDuKZSKyJrgwB-](https://www.youtube.com/playlist?list=PLg7s6cbtAD15G8lNyoaYDuKZSKyJrgwB-)



