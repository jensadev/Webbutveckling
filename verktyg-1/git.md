---
description: Introduktion till Git och Github
---

# Git

## Github

[Git](https://git-scm.com/) är ett versions-hanteringssystem för projekt och [Github](https://github.com/) är ett webbhotell för Git-projekt.

#### Varför?

Vi använder Github i alla programmeringskurserna på skolan. Anledningen till att vi gör det är att vi dels kan få en bra överblick över din progression genom uppgiften. Men det ger oss även viss dokumentation av ditt arbete samt en samlad plattform där vi sköter inlämningar.

Jag som lärare kan även enkelt dela kod till er och ni kan använda den.

Github ger även utmärkta möjligheter till samarbete och att lära av varandra. Det är även ett välkänt och väldigt ofta förekommande verktyg i arbetslivet.

Vi kommer även att använda oss av Github classroom.

{% hint style="info" %}
 Har du registrerat ett konto på [Github](https://github.com/)?
{% endhint %}

### Installation

Github kommer som en desktop applikation och som ett cmdline verktyg. För desktop klienten så laddar du ned programmet och kör installationsfilen.

{% hint style="info" %}
Ladda ned och installera desktop klienten, [https://desktop.github.com/](https://desktop.github.com/)
{% endhint %}

#### Om du vill installera cmdline Git

För cmdline versionen så laddar du antingen ned [Git portable](https://git-scm.com/download/win), eller kör [WSL](https://jens-andreasson.gitbook.io/webbserverprogrammering/utvecklarmiljo/wsl). Detta är alltså inte en Github klient på samma sätt som Githubs desktop applikation.

{% hint style="info" %}
Ladda ned 64-bit Git portable for Windows, [https://git-scm.com/download/win](https://git-scm.com/download/win)
{% endhint %}

{% hint style="info" %}
Ett _portable_ program är ett program utan installationsfiler. Du laddar ned det, packar\(oftast\) upp det och sedan kan du köra programmet.
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
* [ ] Skriv kommandot `git`, funkar det så bör få en lista över tillgängliga kommandon för programmet.
* [ ] Klart.



