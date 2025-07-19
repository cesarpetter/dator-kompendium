---
title: 6 – Windows Server
nav_order: 5
---

# 6 – Windows Server

6.1 Installation av Windows Server

Att installera Windows Server skiljer sig inte mycket från installationen av Windows 11, men det finns några viktiga skillnader att känna till. Framför allt finns det olika editioner och möjligheten att installera med eller utan grafiskt gränssnitt (GUI).

I denna instruktion utgår vi ifrån att du redan har en ISO-fil tillgänglig.

6.1.1 Skapa installationsmedia med Rufus

För att installera Windows Server på en fysisk dator behöver du ett bootbart USB-minne.

Ladda ner och starta Rufus ()

Välj din USB-enhet under Device

Klicka på SELECT och välj ISO-filen för Windows Server

Partition scheme: MBR (för äldre BIOS) eller GPT (för UEFI)

Klicka på START

När klart – starta om datorn och ändra bootordning i BIOS/UEFI

6.1.2 Installera i en virtuell miljö

Om du använder t.ex. Proxmox, VirtualBox eller Hyper-V:

Skapa en ny virtuell maskin

Tilldela RAM (minst 4 GB) och lagringsutrymme (minst 40 GB)

Montera ISO-filen som virtuell CD/DVD

Starta upp och följ installationsguiden

6.1.3 Editioner: Standard, Datacenter och Core/Desktop Experience

Vid installation kommer du att få välja mellan olika versioner. Här är en kort förklaring:

✅ Välj alltid Desktop Experience om du inte är bekväm med kommandoraden ännu.

6.1.4 Steg-för-steg-installation

När ISO är startad:

Välj språk, tangentbord och tid → Klicka Nästa

Klicka Install now

Välj rätt edition (t.ex. "Standard Desktop Experience")

Acceptera licensvillkor

Välj Custom installation

Skapa/markera en partition → Next

Vänta medan Windows installeras

Skapa administratörslösenord

🛠 Efter installationen bör du:

Ge servern ett namn

Ställa in IP-adress

Köra Windows Update

Eventuellt lägga till roller/funktioner via Server Manager

6.1.5 Systemkrav och rekommendationer

Minimikrav för Windows Server 2022:

1.4 GHz 64-bitars processor

512 MB RAM (2 GB med Desktop Experience)

32 GB ledigt lagringsutrymme

UEFI med Secure Boot (rekommenderas)

Internetanslutning för aktivering/uppdateringar

Rekommenderade krav för smidig drift:

2+ GHz flertrådad CPU

8+ GB RAM

60+ GB SSD

1 Gbit nätverkskort

6.2 Workgroup, Domain och Active Directory

För att förstå hur Windows Server används i nätverk är det viktigt att känna till tre centrala begrepp: Workgroup, Domain och Active Directory (AD).

6.2.1 Vad är en Workgroup?

En Workgroup är en enkel typ av nätverksstruktur där varje dator är oberoende och hanterar sina egna användare och resurser.

Ingen central styrning – varje dator har sina egna användarkonton och lösenord

Fildelning sker via delade mappar, skrivare och rättigheter per maskin

Alla datorer måste vara i samma workgroup-namn för att hitta varandra enklare

🧠 En workgroup är som ett kollektiv – alla ansvarar för sig själva.

❗ Viktigt att förstå:
 I en workgroup måste datorn som delar ut resurser vara påslagen. Om någon delar ut en skrivare eller en mapp från sin dator, så slutar den vara tillgänglig i nätverket om datorn stängs av.

🔧 Exempel:
 Bob har delat ut sin skrivare i hemnätverket. Om Bob stänger av sin dator, kan ingen annan längre skriva ut via den skrivaren. Det finns ingen central server som tar över delningen – vilket är en av de största begränsningarna med workgroup jämfört med en domän.

6.2.2 Vad är en Domain?

En Domain är en centraliserad nätverksmodell som styrs av en domänkontrollant (Domain Controller).

Alla användarkonton och resurser hanteras centralt

Logga in från vilken dator som helst med ett enda konto

Kräver en server som kör Active Directory Domain Services (AD DS)

Används i skolor, företag och organisationer med behov av central administration

💼 En domän fungerar som ett företag – du loggar in och får tillgång till det du är behörig till, var du än sitter.

6.2.3 Vad är Active Directory?

Active Directory (AD) är tekniken bakom domäner i Windows-världen. Den tillhandahåller:

En katalogtjänst över alla användare, datorer, grupper, skrivare etc.

Möjlighet att styra policies (GPO – Group Policy Objects)

Central hantering av konton och rättigheter

Flexibilitet att organisera resurser i Organizational Units (OU)

🔐 AD gör det möjligt att sköta säkerhet, åtkomst och struktur i stora nätverk.

6.2.4 Sammanfattning: skillnader mellan Workgroup och Domain

6.2.5 När används vad?

6.3 Diskussions- och kontrollfrågor

Vad är skillnaden mellan Standard och Datacenter edition av Windows Server?

När bör du använda Desktop Experience istället för Core-installation?

Vad är syftet med en domän?

Hur skiljer sig en workgroup från en domain i användarhantering?

Vad används Active Directory till?

6.4 Fördjupningslänkar

Microsoft Learn – Windows Server Installation Overview

Microsoft Docs – Compare Windows Server editions

What is Active Directory? (JumpCloud)

Group Policy Overview

Workgroup vs Domain (How-To Geek)

6.5 Egna anteckningar

(Här kan du som elev skriva egna anteckningar om Windows Server-installation, skillnader mellan Workgroup och Domain eller vad Active Directory egentligen gör)

7. Linux – Historia, filosofi och ekosystem

7.1 Vad är Linux?

Linux är inte ett operativsystem i sig – det är en kärna, en central del av ett operativsystem som hanterar resurser som minne, CPU och hårddiskar. Linuxkärnan utvecklades av Linus Torvalds 1991 som ett hobbyprojekt medan han studerade vid Helsingfors universitet. Han ville skapa ett fritt alternativ till UNIX, som på den tiden var kraftfullt men ofta dyrt och stängt.

Linuxprojektet växte snabbt tack vare ett engagerat community och en öppen utvecklingsmodell. Med tiden började andra utvecklare bidra, och tillsammans med komponenter från projekt som GNU skapades kompletta operativsystem som kunde användas av både privatpersoner och företag.

Idag är Linux ett av världens mest använda operativsystem – inte för att det syns i butikshyllan, utan för att det körs i bakgrunden överallt. Du hittar Linuxkärnan i:

Android-telefoner

Servrar och superdatorer

Internet of Things (IoT)

Molntjänster som Google Cloud och AWS

Steam Deck och andra spelsystem

Bilar, flygplan och smarta TV-apparater

Linux finns överallt, men märks sällan.

7.1.2 Upphovsrätt, öppen källkod och programvarutyper

För att förstå Linux på riktigt måste man förstå open source-rörelsen. Linux är mer än bara kod – det är en idé om att kunskap ska vara fri och tillgänglig för alla. Här är några centrala begrepp:

Open Source

Programvara med öppen källkod där vem som helst får läsa, ändra och distribuera koden. Det gör att tusentals personer kan bidra till samma projekt – som Linux – från hela världen.

Free Software

Inte “gratis” i första hand – utan frihet. Free Software Foundation, startad av Richard Stallman, förespråkar att användare ska ha rätten att använda, ändra och dela programvara. Ett klassiskt citat är:

“Think free as in free speech, not free beer.”

Freeware

Gratis programvara, men ofta utan tillgång till källkoden. Exempel: Skype, Spotify (gratisversion). Det är alltså inte samma sak som open source.

Shareware

Programvara som är gratis att testa, men sedan kräver betalning för full funktionalitet. Vanligt före internet-eran.

Proprietär programvara

Proprietär (eller sluten) programvara är motsatsen till open source. Här är källkoden hemlig, och användaren får inte ändra, kopiera eller distribuera den fritt.
 Exempel på proprietär programvara är Microsoft Windows, Adobe Photoshop och drivrutiner från t.ex. NVIDIA.

De flesta Linuxdistributioner erbjuder möjligheten att installera vissa proprietära drivrutiner (som inte finns i den öppna källkoden) för att få bättre stöd för grafik, ljud och nätverk – särskilt viktigt om datorn innehåller NVIDIA-grafikkort eller vissa Wi-Fi-kretsar.

Git

Ett versionshanteringssystem skapat av Linus Torvalds (ironiskt nog, eftersom han inte gillade alternativen). Git används för att spåra ändringar i kod och samarbeta i stora projekt. Github är idag den största plattformen för Git-projekt.

GNU

Ett projekt som ville skapa ett helt fritt operativsystem. De lyckades nästan – men saknade en kärna. När Linuxkärnan kom, kunde GNU + Linux kombineras till ett helt fungerande system. Därför kallas Linux ibland för “GNU/Linux”.

Linuxvärlden bygger på samarbete, delning och frihet – både tekniskt och juridiskt.

7.1.3 Linuxkärnans grenar (distributioner)

Eftersom Linux är fri att använda och modifiera, har det vuxit fram många olika “smaker” av Linux – så kallade distributioner eller “distros”.

De flesta distros bygger på en av tre stora familjer:

Debian – stabil och populär, med barn som Ubuntu och Linux Mint. Vanlig i skolor, servrar och nybörjarsystem.

Red Hat – affärsfokuserad med stöd och certifiering. Fedora är dess testplattform, medan CentOS och AlmaLinux är communityversioner.

Arch – minimalistisk och avancerad. “DIY-Linux” där man bygger allt själv. Populär bland entusiaster.

Man kan se Linux som en motor (kärnan), och varje distro som en bilmodell byggd kring motorn, med olika inredning, reglage och målgrupper.

7.1.4 Fördelar med Linux

Gratis att använda – De flesta distributioner är helt fria att ladda ner och använda, vilket gör dem perfekta för skolor, hobbyister och utvecklare.

Öppen källkod – Du kan granska, ändra och anpassa koden själv, vilket skapar insyn och möjlighet till innovation.

Stabilt och säkert – Linux används ofta på servrar eftersom det sällan kraschar och har färre sårbarheter än vissa kommersiella alternativ.

Flexibelt och anpassningsbart – Du kan välja precis vilken skrivbordsmiljö, mjukvara och konfiguration du vill ha – från minimalistiskt till fullt GUI.

Stort community – Det finns tusentals guider, forum och hjälpsidor, vilket gör det lättare att få hjälp vid problem.

7.1.5 Nackdelar med Linux

Inte alla program finns tillgängliga – Vissa program (t.ex. Adobe Photoshop eller Microsoft Office) har inte fullständigt Linux-stöd, vilket kan vara ett problem för vissa användare.

Kan vara svårt att komma igång för nybörjare – Kommandoraden kan kännas överväldigande, särskilt för den som är van vid Windows.

Begränsat stöd från vissa tillverkare – Drivrutiner och hårdvarustöd kan ibland saknas, särskilt för nyare eller ovanlig utrustning.

Spelstöd inte alltid lika bra – Även om det blivit mycket bättre med Steam och Proton, finns fortfarande vissa begränsningar.

Fler steg vid installation och underhåll – Du förväntas ibland hantera saker manuellt, till exempel montering av diskar eller konfigurering av nätverk.

7.1.6 Fördjupningslänkar

Linux Foundation –

History of Linux –

GNU Project –

What is Git –

Ubuntu –

Debian –

Red Hat –

Arch Linux –

Free Software Foundation –

Steam Deck (Linux-baserad) –

7.1.7 Kontroll- och diskussionsfrågor

Vem skapade Linux och varför?

Vad är skillnaden mellan Linuxkärnan och ett operativsystem?

Nämn tre platser där Linux används idag utan att man tänker på det.

Förklara begreppet "free software".

Vad är skillnaden mellan open source och freeware?

Vad är GNU och varför är det viktigt i Linuxhistorien?

Beskriv skillnaden mellan Debian-, Red Hat- och Arch-familjerna.

Nämn två fördelar med att använda Linux.

Nämn två nackdelar med att använda Linux.

Vad är Git och varför är det viktigt inom öppen källkod?

7.1.8 Egna anteckningar

(Här lämnas plats för elevens egna reflektioner, tankar och eventuella kompletteringar under lektionen.)

7.2 Installation av Ubuntu Desktop

Ubuntu är idag världens mest använda Linuxdistribution för både privatpersoner och företag. Den är känd för att vara användarvänlig, stabil och modern, och används som grund för många andra Linux-varianter – som Linux Mint, Pop!_OS och Elementary OS. Det gör att Ubuntu fungerar som en slags "ledare" inom Linuxvärlden när det gäller teknisk utveckling, paketsystem och stöd för ny hårdvara.

Bakom Ubuntu står Canonical, ett brittiskt företag och en stiftelse som ansvarar för utvecklingen. Canonical bidrar även till molntjänster, servrar och Internet of Things, men det är deras skrivbordsversion – Ubuntu Desktop – som ofta används i undervisning och som introduktion till Linux.

Ubuntu släpper två versioner per år:

En i april (04)

En i september (09)

Versionerna numreras enligt formatet ÅR.MÅNAD, t.ex. 24.04 = april 2024.

Det finns två typer av versioner:

LTS – Long Term Support
 En LTS-version ges ut vartannat år (jämna år i april: 20.04, 22.04, 24.04...)
 Dessa har 5 års support, vilket innebär säkerhetsuppdateringar, buggfixar och stabilitet över lång tid.
 De används ofta i företag, skolor och produktion eftersom de är testade extra noggrant.

STS – Short Term Support
 Släpps mellan LTS-versionerna (t.ex. 23.10, 24.10) och har 9 månaders support.
 Dessa versioner innehåller ofta nyare teknik och funktioner, vilket gör dem intressanta för utvecklare och entusiaster som vill ligga i framkant – men de är inte lika långsiktigt stabila som LTS.

I denna guide använder vi Ubuntu 24.04 LTS, vilket är den version som rekommenderas för skolor, företag och nybörjare – tack vare dess stabilitet och långsiktiga support.

Viktigt om Secure Boot

Ubuntu är en av få Linuxdistributioner som fungerar direkt med Secure Boot aktiverat. Däremot kräver vissa drivrutiner (t.ex. NVIDIA eller vissa Wi-Fi-kretsar) att man signerar moduler och registrerar en nyckel med hjälp av MOK (Machine Owner Key).
 För mer information om vad Secure Boot är, se kapitel 2.7.1.

Steg för steg: Installera Ubuntu Desktop

1. Ladda ner Ubuntu

Besök  och ladda ner den senaste LTS-versionen (t.ex. Ubuntu 24.04 LTS).

2. Skapa en startbar USB

Använd ett verktyg som:

Rufus (Windows)

Balena Etcher (Windows/macOS/Linux)

Startup Disk Creator (på annan Ubuntu)

Välj .iso-filen och skriv till ett USB-minne (minst 8 GB).

3. Starta datorn från USB

Starta om datorn och välj att boota från USB-enheten. Detta görs ofta via en särskild tangent (t.ex. F12, ESC, F2 beroende på tillverkare).

⚠️ På de flesta datorer behöver man inte stänga av Secure Boot – Ubuntu fungerar direkt med det aktiverat.

4. Välj språk och tangentbord

I installationsmenyn:

Välj språk

Välj tangentbordslayout (Svenskt tangentbord är standard i Sverige)

5. Anslut till Wi-Fi eller nätverk

Det är rekommenderat att ha internetanslutning under installationen. Då kan Ubuntu automatiskt installera drivrutiner och uppdateringar.

6. Installationsalternativ

Du får nu välja mellan:

Normal installation: inkluderar webbläsare, kontorsprogram, mediauppspelare m.m.

Minimal installation: endast webbläsare och grundläggande verktyg

Markera också:

☑ Install third-party software for graphics and Wi-Fi hardware
☑ Download updates while installing Ubuntu

☝️ Den första rutan är viktig – den ser till att proprietära drivrutiner installeras, vilket kan kräva MOK efter omstart.

7. Välj installationsläge

Välj “Erase disk and install Ubuntu” om du vill att Ubuntu använder hela hårddisken

Eller “Something else” om du vill göra avancerad partitionering (rekommenderas endast för vana användare)

Ubuntu sköter automatiskt partitionering och skapar swap om inget annat anges.

8. Skapa användare

Ange:

Fullständigt namn

Datornamn

Användarnamn

Lösenord (används även för att bekräfta systemändringar via sudo)

9. Installationen startar

Ubuntu kopierar filer och konfigurerar systemet. Detta tar ca 5–15 minuter beroende på datorns hastighet.

Efter installationen: MOK och drivrutiner

Vid första omstart kan du få upp ett blått MOK-fönster om du installerat proprietära drivrutiner (som kräver Secure Boot-signering). Gör då följande:

Välj “Enroll MOK”

Ange det lösenord du valde under installationen (du blir tillfrågad om det innan omstart)

Bekräfta och starta om

Detta registrerar Canonicals signeringsnyckel, så att drivrutiner kan laddas även med Secure Boot aktivt.

Justera drivrutiner i efterhand

Om något inte fungerar (t.ex. Wi-Fi, grafik), kan du:

Gå till Programvara och uppdateringar

Välj fliken Ytterligare drivrutiner

Aktivera alternativ som “Proprietär, testad”

Bekräfta och starta om

7.2.1 Fördjupningslänkar

Ubuntu Desktop Download –

Canonical –

What is Secure Boot –

Installing Proprietary Drivers –

Ubuntu LTS vs STS –

7.2.2 Kontrollfrågor

Vad är Ubuntu och varför är det en av de mest använda Linuxdistributionerna?

Vad heter organisationen som står bakom Ubuntu?

Hur döps Ubuntu-versioner och vad betyder till exempel “24.04”?

Vad innebär LTS och hur länge får en sådan version support?

Vad är skillnaden mellan en LTS-version och en STS-version?

Vilket verktyg kan du använda i Windows för att skapa ett startbart USB-minne?

Vad är Secure Boot, och varför behöver man känna till det vid Linuxinstallation?

Vad är MOK och när kan det behövas?

Varför bör man markera alternativet “Install third-party software…” under installationen?

Hur kan man aktivera proprietära drivrutiner i efterhand?

7.9.3 Egna anteckningar

(Här kan du som elev skriva ner egna tankar, saker du upptäckte under installationen eller frågor du vill ställa vid nästa lektion.)

7.3 Konfiguration av Ubuntu Desktop

Efter installationen är det dags att börja utforska Ubuntu och förstå hur systemet är uppbyggt och hanteras – både via terminalen och det grafiska gränssnittet. Till skillnad från Windows är Ubuntu flexibelt: nästan allt du kan göra i grafiskt gränssnitt kan också göras i terminalen – och vice versa.

Här går vi igenom grunderna i hur du håller systemet uppdaterat, installerar program, förstår filsystemet och hanterar rättigheter.

7.3.1 Uppdatera systemet

Ubuntu hämtar program och uppdateringar från repositories – det är samlingar av godkända paket som är säkra att installera. Man kan jämföra det med en appbutik fast för hela systemet. När du uppdaterar Ubuntu kontaktar systemet dessa källor och laddar ner de senaste versionerna.

Uppdatering via terminalen:

sudo apt update
sudo apt upgrade

Uppdatering via grafiskt gränssnitt:

Öppna Programuppdaterare (Software Updater)

Klicka på Installera uppdateringar

7.3.2 Installera och avinstallera program

Ubuntu erbjuder flera sätt att installera och ta bort program. Oavsett om du föredrar GUI eller terminal kan du hantera systemet på dina egna villkor.

Via terminalen:

sudo apt install vlc
sudo apt remove vlc

Via Synaptic (pakethanterare):

Installera Synaptic om det inte finns:

sudo apt install synaptic

Starta Synaptic och sök efter program, markera och installera

Via Ubuntu Software Center:

Öppna Program (Software)

Sök och installera appar med ett klick

🧠 Viktigt att förstå: Allt går att göra både i GUI och terminalen – det är samma paket i bakgrunden. Det som skiljer är hur du interagerar med systemet.

7.3.3 Filsystem i Linux

Linux använder ett filsystem med en gemensam rot (/) – alla filer och enheter placeras någonstans under denna rot.

Här är några viktiga mappar:

🔧 Till skillnad från Windows används inte enhetsbokstäver (C:, D:). Nya diskar monteras in i det befintliga filsystemet, t.ex. /media/usb.

7.3.4 Rättigheter och grupper i Linux

Linux använder ett rättighetssystem som styr vem som får göra vad med varje fil. Systemet bygger på tre delar:

Ägare (User) – användaren som äger filen

Grupp (Group) – gruppen filen tillhör

Övriga (Others) – alla andra användare

Varje fil har tre rättighetstyper:

r – read (läsa)

w – write (skriva)

x – execute (köra)

Exempel på rättigheter:

-rw-r--r--  1 robin itlärare myfil.txt

Det betyder:

rw- (ägaren får läsa och skriva)

r-- (gruppen får läsa)

r-- (övriga får läsa)

Oktal notation

Rättigheter kan också skrivas i siffraform, så kallad oktal notation:

Exempel:

chmod 755 script.sh

Betyder:

Ägare: rwx (7)

Grupp: r-x (5)

Övriga: r-x (5)

Grupper i Linux

Användare kan tillhöra en primär grupp och flera sekundära grupper.

Den primära gruppen skapas ofta automatiskt vid kontoskapande.

Sekundära grupper kan användas för att ge särskilda rättigheter (t.ex. sudo, docker, www-data).

Kommandon:

groups robin
sudo usermod -aG docker robin

🧠 Genom att använda grupper kan du ge många användare tillgång till samma resurser, utan att behöva ge dem root-rättigheter.

7.3.5 Felsökning och underhåll

Precis som i Windows uppstår ibland problem i Ubuntu – det kan handla om nätverk, drivrutiner, program som inte startar eller uppdateringar som krånglar. Lyckligtvis erbjuder Ubuntu en mängd verktyg för att felsöka och lösa dessa problem – både grafiskt och via terminal.

Här är några vanliga områden och metoder att känna till:

7.3.5.1 Uppdateringsproblem

Om uppdateringar misslyckas eller låser sig:

sudo apt update
sudo apt upgrade
sudo apt --fix-broken install

Tips: Använd sudo apt autoremove för att rensa bort gamla paket du inte längre behöver.

7.3.5.2  Nätverksproblem

För att kontrollera nätverksstatus:

ip a
ping 8.8.8.8
nmcli device status

Om nätverket inte fungerar:

Kontrollera om du är ansluten till rätt nätverk

Starta om nätverkstjänsten:

sudo systemctl restart NetworkManager

7.3.5.3 Program kraschar eller vägrar starta

Du kan starta program från terminalen för att se felmeddelanden, t.ex.:

firefox

Om det inte fungerar, prova att installera om:

sudo apt remove firefox
sudo apt install firefox

7.3.5.4 Systemloggar

Loggfiler hjälper dig att se vad som gått fel:

Grafiskt: Loggboken (Logs) från programmenyn

Terminalen:

journalctl -xe
dmesg
tail -f /var/log/syslog

7.3.5.5 Användbara verktyg för underhåll

7.3.5.6 Återställa grafiskt gränssnitt (vid GUI-problem)

Ibland kraschar skrivbordsmiljön (t.ex. GNOME). Då kan du starta om den:

sudo systemctl restart gdm3

7.3.5.7 Skapa systemrapport (t.ex. vid support)

Ubuntu har ett verktyg som samlar systeminformation:

sudo ubuntu-report

7.3.5.8 Säkerhetskopiering och återställning

Använd gärna Déjà Dup (Backups) – det är ett inbyggt verktyg i Ubuntu.

Starta det via “Backuper” och ställ in:

Vad som ska sparas

Var (t.ex. USB, nätverksenhet)

Hur ofta

7.3.6 Kontrollfrågor

Vad är ett repository och varför behövs det?

Nämn tre sätt att installera program i Ubuntu.

Vad är skillnaden mellan /etc och /home?

Hur monteras en USB-sticka in i Linuxfilsystemet?

Vad gör kommandot chmod 644 fil.txt?

Vad betyder -rw-r--r-- i rättighetssträngen?

Hur lägger du till en användare i en grupp?

Hur kan du starta om nätverksanslutningen i Ubuntu?

Vad gör journalctl -xe och när är det användbart?

Vilket grafiskt verktyg kan du använda för backup i Ubuntu?

7.3.7 Fördjupningslänkar

Ubuntu – Basic Troubleshooting Guide

How-To Geek – 8 Deadly Commands You Should Never Run on Linux

Linux Handbook – How to Check Logs in Linux

DigitalOcean – How to Use fsck to Check and Repair File System Issues

Linuxize – How to Use the top Command

7.3.8 Egna anteckningar

(Här kan du skriva ner egna kommandon, lösningar, tips eller saker du vill komma ihåg.)

7.4 Installation av Ubuntu Server och Webmin

Ubuntu Server är ett resurssnålt, textbaserat operativsystem som används för att driva allt från webbservrar till filservrar och databaser. Till skillnad från Ubuntu Desktop innehåller serverversionen inget grafiskt användargränssnitt, vilket gör den snabbare och mer effektiv – särskilt i virtuella miljöer.

Att installera Ubuntu Server är inte svårt, men kräver att man är noggrann med inställningarna under installationen, eftersom valet av tjänster och nätverkskonfiguration får direkt påverkan på hur servern fungerar.

Steg för steg: Installera Ubuntu Server

1. Ladda ner Ubuntu Server

Besök  och ladda ner den senaste LTS-versionen (t.ex. Ubuntu Server 24.04 LTS).

2. Skapa en startbar USB

Använd till exempel:

Rufus (Windows)

Balena Etcher

Startup Disk Creator (på Linux)

Skriv .iso-filen till ett USB-minne på minst 4 GB.

3. Starta datorn från USB

Starta om och välj att boota från USB-enheten. Detta görs vanligtvis via F12, F2, ESC eller DEL beroende på tillverkare.

4. Välj språk, tangentbord och tidszon

5. Nätverksinställningar

Om du har en DHCP-server (t.ex. i Proxmox eller OPNsense) så får servern IP automatiskt.
 Annars kan du ställa in en statisk IP-adress direkt.

6. Användare och lösenord

Skapa ett användarnamn och välj ett starkt lösenord.
 Du får även möjlighet att installera OpenSSH-server, vilket rekommenderas så att du kan ansluta till servern via SSH i efterhand.

7. Lagring och partitionering

Välj:

Use an entire disk (om du vill låta Ubuntu automatiskt partitionera)

Custom storage layout (om du vill lägga upp partitioner själv)

8. Installera valfria tjänster

Ubuntu Server ger möjlighet att installera färdiga paketgrupper:

OpenSSH

Samba

LAMP/LEMP

Docker

Print server

etc.

I skolsammanhang är det oftast bäst att börja rent och installera det du behöver i efterhand.

9. Starta installationen

Installationen tar 5–10 minuter.

Webmin – ett grafiskt gränssnitt för serversystem

Att jobba i terminalen är kraftfullt – men kan vara avskräckande för nya användare. Här kommer Webmin in i bilden. Det är ett webbaserat gränssnitt för att administrera Linux-servrar, där du enkelt kan hantera:

Användare och grupper

Brandvägg och nätverksinställningar

Paketinstallationer

Tjänster som SSH, Samba, FTP och mycket mer

Webmin gör det enklare att förstå hur en server fungerar, eftersom du ser helheten – inte bara kommandon. Det är ett utmärkt sätt att kombinera pedagogik med riktig systemadministration.

Så här installerar du Webmin på Ubuntu Server

Webmin har numera ett officiellt installationsscript som automatiserar allt du behöver:

curl -o webmin-setup-repo.sh https://raw.githubusercontent.com/webmin/webmin/master/webmin-setup-repo.sh
sh webmin-setup-repo.sh

Efter installationen kommer Webmin att vara tillgängligt på:

https://<serverns-ip>:10000

⚠️ Webmin använder HTTPS med ett självsignerat certifikat, så webbläsaren kommer att varna – det är normalt.
 Logga in med det användarnamn och lösenord du skapade under installationen av Ubuntu Server.

7.4.1 Fördjupningslänkar

Ubuntu Server Download –

Ubuntu Server Guide (official) –

Webmin –

Webmin GitHub Repository –

Install Webmin on Ubuntu –

7.4.2 Kontrollfrågor

Vad är skillnaden mellan Ubuntu Desktop och Ubuntu Server?

Vad är fördelen med att Ubuntu Server saknar grafiskt gränssnitt?

Vad kan du göra under installationen om servern inte får någon IP-adress automatiskt?

Vilken typ av användare och lösenord skapar du under installationen?

Vad används OpenSSH till och varför bör det installeras på en server?

Varför rekommenderas det att börja med en "ren" installation utan extra tjänster?

Vad är Webmin och varför kan det vara ett bra verktyg i en undervisningsmiljö?

Hur når du Webmin när det är installerat?

Vad betyder det att Webmin använder ett självsignerat certifikat?

Vilka två kommandon används för att installera Webmin med det officiella installationsscriptet?

7.4.3 Egna anteckningar

(Här kan du skriva ner vad du lärde dig under installationen, vilka val du gjorde, eller hur det kändes att arbeta med servern via Webmin istället för terminalen.)

