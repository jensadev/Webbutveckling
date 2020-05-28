---
description: Introduktion till Git och Github
---

# Git

## GitHub

[Git](https://git-scm.com/) är ett versions-hanteringssystem för projekt och [GitHub](https://github.com/) är ett webbhotell\(enkelt uttryckt\) för Git-projekt.

### Varför?

Vi använder GitHub i alla programmeringskurserna på skolan. Anledningen till att vi gör det är att vi dels kan få en bra överblick över din progression genom uppgiften. Men det ger oss även viss dokumentation av ditt arbete samt en samlad plattform där vi sköter inlämningar.

Jag som lärare kan även enkelt dela kod till er och ni kan använda den.

GitHub ger även utmärkta möjligheter till samarbete och att lära av varandra. Det är även ett välkänt och väldigt ofta förekommande verktyg i arbetslivet.

Vi kommer även att använda oss av GitHub classroom.

{% hint style="info" %}
 Har du registrerat ett konto på [GitHub](https://github.com/)?
{% endhint %}

### Installation

GitHub kommer som en desktop applikation och som ett cmdline verktyg. För desktop klienten så laddar du ned programmet och kör installationsfilen.

{% hint style="info" %}
Ladda ned och installera desktop klienten, [https://desktop.github.com/](https://desktop.github.com/)
{% endhint %}

#### Om du vill installera cmdline Git

För cmdline versionen så laddar du antingen ned [Git portable](https://git-scm.com/download/win), eller kör [WSL](https://jens-andreasson.gitbook.io/webbserverprogrammering/utvecklarmiljo/wsl). Detta är alltså inte en GitHub klient på samma sätt som GitHubs desktop applikation.

{% hint style="info" %}
Ladda ned 64-bit Git portable for Windows, [https://git-scm.com/download/win](https://git-scm.com/download/win)
{% endhint %}

{% hint style="info" %}
Ett _portable_ program är ett program utan installationsfiler. Du laddar ned det, packar\(oftast\) upp det och sedan kan du köra programmet
{% endhint %}

PortableGit är en .exe fil som packar upp sina filer där du väljer att spara dem. Kör det och välj att spara filerna under `c:\tools\portablegit`.

För att sedan kunna använda Git från cmdline behöver vi lägga till det i ditt systems PATH variabel, detta så att systemet kan hitta programmet.

* [ ] Starta Utforskaren\(Explorer\), `win+E`
* [ ] Högerklicka på den här datorn, välj Egenskaper.
* [ ] Du får nu upp Kontrollpanelen, System och säkerhet, System
* [ ] Välj Avancerade systeminställningar
* [ ] Klicka på Miljövariabler
* [ ] Under Användarvariabler för din användare, så letar du upp och dubbelklickar på Path
* [ ] Välj Ny och skriv in sökvägen till `\bin` mappen i Git katalogen. Det bör vara, `C:\tools\PortableGit\bin`
* [ ] Starta Powershell \(eller starta om det om du hade det igång\)
* [ ] Skriv kommandot `git`, funkar det så bör få en lista över tillgängliga kommandon för programmet
* [ ] Klart, fira!

### Ditt första repository

{% hint style="info" %}
Tips: Kör igenom desktop klientens tutorial om detta är helt nytt
{% endhint %}

Ett repository, eller repo, är en sida på GitHub där alla dina filer till projektet är samlade\(tillsammans med massa annat\). På github.com så har det en url som följer samma mönster.

{% hint style="info" %}
github.com/username/repository-namn
{% endhint %}

För att skapa ett nytt repo med desktop klienten så kan vi klicka på **+ Create a New...** och följer instruktionerna.

![](https://lh6.googleusercontent.com/TpP2mAMNVohIZ8sSTCgSdI8WyqAm5UaoD-hhy4FpJ5GAeuu8N58mRL-pxQK5gByqLHkuh8DV_ySIg7Y4DuYPL88hZWGvExwL8RqLeLAd-oDk4W4mk-PnxAxwqKUP2zpEVfSKYUuI)

Alternativt så gör vi detta på webbplatsen, men då behöver du välja "Add an Existing..." i desktop klienten för att koppla ihop dem.

* [ ] Surfa till [https://github.com/](https://github.com/)
* [ ] Logga in
* [ ] Klicka på + i menyn och välj, New repository
* [ ] Skriv in ett namn
* [ ] Klicka på att skapa

## Att använda Github

Git är ett versionshanteringssystem, med det menas att det håller reda på dina filer och innehållet i dem. Detta sker lokalt med git, men när vi använder GitHub så kan vi synka det med filer som sparas på deras tjänst. Vi ska nu testa detta.

{% hint style="info" %}
Att ha ett centralt ställe på din dator där du sparar allt arbetet med kod är god praxis
{% endhint %}

Först ska vi se till att vi har en mapp där vi kan spara allt arbete med kod på din dators hårddisk. Öppna Utforskaren\(Explorer\) i Windows och skapa en ny mapp\(Folder\) i c:\

![Skapa en c:\code mapp i Utforskaren](../.gitbook/assets/mapp.png)

Bra, nu kan vi komma igång. [Klicka här om du vill hoppa till avsnittet för cmdline](git.md#git-cmdline).

### Github desktop

{% hint style="warning" %}
Här förutsätts det att du har kört igenom desktop klientens tutorial
{% endhint %}

Först så ska vi skapa ett repo att använda.

![Skapa ett nytt repo](../.gitbook/assets/cnew.png)

När det är klart så kan du sedan välja att publicera detta till Github, det kommer då att skapas ett repo på Githubs webbsida som kopplas till din lokala mapp.

![Publicera p&#xE5; GitHub](../.gitbook/assets/pub.png)

Vi är nu redo att börja arbeta. Förslagsvis öppnar du nu ditt repo med Visual Studio Code. Använd antingen knappen eller i code så väljer du Open Folder i File menyn.

I code så skapar du sedan en ny fil. I filen skriver du det som följer och sparar det sedan som `README.md`

```bash
# Hallå världen
Hej
```

I alla repon bör det finnas en `README.md` fil, detta är en den fil som GitHub automatiskt visar för repot och den är skriven i [Markdown](https://guides.github.com/features/mastering-markdown/).

Nu när vi har ändringar i filen så kan vi hoppa över till klienten igen. Vi ser där en lista över våra ändringar.  Klicka sedan Commit to master och efter det Push origin. Du har nu laddat upp dina lokala ändringar till GitHub.

{% hint style="danger" %}
Här förutsätts det att du inte har gjort några ändringar på github.com, du kommer annars få konflikter
{% endhint %}

### Problem och att lösa dem

Som tidigare nämnt så är Git ett versionshanteringssystem, detta kan leda till att det blir konflikter mellan dina lokala filer och de som finns sparade på GitHub. Git måste bestämma vilken version av filen som ska användas och vad den ska innehålla. För att lära oss hantera detta så ska vi skapa en sådan konflikt.

Börja med att surfa till ditt repo på github.com. Där väljer du sedan att redigare din README.md fil. Gör en ändring och välj Commit changes.

![Redigera och commita &#xE4;ndringar p&#xE5; GitHub](../.gitbook/assets/commit.png)

{% hint style="success" %}
Det finns nu ett sätt att undvika problem och det är att göra Fetch origin följt av Pull origin. Då hämtar du och laddar ned ändringarna som gjorts på GitHub. Gör du detta innan du börjat arbeta så kommer du inte att få någon konflikt, eller merge issue
{% endhint %}

Om vi inte har haft framförhållningen att köra Fetch så måste vi då kunna lösa problemet. Det gör vi som följer. Se nu till att du har ändringar på origin som du inte har lokalt. Gå sedan in i code och gör ändringar.

{% code title="README.md" %}
```bash
# Hallå där!
Hej

Detta är ändringar som inte finns på origin och origin har ändrats!
```
{% endcode %}

Öppna sedan klienten och välj Commit to master. Du kommer då att få en varning om att du behöver hämta origin. 

![Klienten ber&#xE4;ttar vad vi beh&#xF6;ver g&#xF6;ra f&#xF6;r att kunna ladda upp v&#xE5;r senaste commit](../.gitbook/assets/pull.png)

Detta kommer leda till en konflikt som behöver lösas innan vi kan slå ihop de ändringar vi har gjort.

![Klienten varnar oss](../.gitbook/assets/resolve.png)

Det du nu behöver göra är att öppna filen i code. Detta för att lösa denna konflikt. I code så kommer då de ändringar som gjorts visas. Du behöver välja vilka ändringar i filen du ska spara. Välj och spara sedan filen.

![Code hj&#xE4;lper oss att redigera filerna och v&#xE4;lja vilken kod vi vill spara](../.gitbook/assets/changes.png)

Konflikt dialogen i klienten kommer sedan uppdateras när du sparat filen, löst konflikten och du kan nu committa dina ändringar. Avsluta sedan med att pusha.

![L&#xF6;st!](../.gitbook/assets/resolved.png)

Det är inte alltid så här lätt att lösa konflikter mot GitHub, men detta är grundprincipen.

{% hint style="info" %}
Du kan även använda code för att jobba mot GitHub. Du hittar mer om det i Source Control tabben
{% endhint %}

### Git cmdline

Att arbeta med de grafiska klienterna för att prata med GitHub funkar utmärkt, men det är väldigt bra att ha koll på hur det fungerar med cmdline verktygen också. Här följer instruktioner för hur vi skapar ett repo och löser en konflikt i cmdline klienten.

{% hint style="warning" %}
Skapa en code mapp om du inte har gjort det
{% endhint %}

Vi använder sedan `cmd`, `windows terminal`, `ubuntu`, `wsl` eller liknande för att skapa mappar och initiera Git.

```bash
# I Windows cmdline skriver du
c:
cd \
md code # md är make directory, så använd bara om du inte skapat med Utforskaren
cd code
md wu1-test
cd wu1-test

git init # initierar detta som ett repository

code . # startar visual studio code i mappen
```

{% hint style="info" %}
Du kan närsomhelst i cmdline skriva dir eller ls för att se vars i mappstrukturen du är. Notera även att i prompten så står det längst till vänster "vars du är"
{% endhint %}

När du nu har mappen skapad så behöver vi skapa repot på GitHub, gör det genom att repetera stegen som står här [ovan](git.md#ditt-foersta-repository), men döp repot till wu1-test.

{% hint style="info" %}
Det är generellt en bra ide att döpa mappen för sitt repo till repots namn
{% endhint %}

