---
title: 5 – Windows
nav_order: 4
---

# 5 – Windows

5.1 Historia

Windows är idag världens mest spridda operativsystem för persondatorer. Men resan dit har varit lång och innehållsrik. För att förstå dagens Windows 11 (och även Windows Server) är det bra att ha en grundläggande bild av hur systemet har utvecklats.

5.1.1 Utveckling

✅ MS-DOS och tidiga Windows-versioner (1980-tal – början av 90-talet)

Windows började som ett grafiskt skal ovanpå MS-DOS.

Windows 1.0, 2.0 och 3.x var inte egna operativsystem i egentlig mening, utan byggde på MS-DOS som kärna.

Gränssnittet gjorde det enklare att starta program, hantera filer och jobba med fler fönster.

✅ Windows 95 och Windows 98 (mitten/slutet av 90-talet)

Stort steg framåt: integrerade DOS och Windows i ett mer sammanhållet system.

Introducerade Start-menyn och aktivitetsfältet – kännetecken som finns kvar än idag.

Bättre stöd för 32-bitarsprogram, Plug and Play och nätverk.

✅ Windows NT-linjen

Parallellt utvecklade Microsoft Windows NT (New Technology) som en stabil och säker kärna för företag.

Windows NT 3.5, 4.0 och senare Windows 2000 byggde på en modern mikrokärnearkitektur.

NT-linjen introducerade bättre användarhantering och filsystemet NTFS med avancerade rättigheter.

✅ Windows XP (2001)

Enade konsument- och företagslinjen under NT-kärnan.

Stabilare än 9x-serien och mycket populärt.

Stöd för flera användare, fjärrskrivbord och bättre drivrutinshantering.

Introducerade tydligare säkerhetsfunktioner.

✅ Windows Vista (2006)

Kort nämnt: anses ofta som mindre lyckat.

Införde dock viktiga tekniker som UAC (User Account Control) för säkerhet.

✅ Windows 7 (2009)

Förbättrad version av Vista – mycket populärt och stabilt.

Förbättrat gränssnitt, bättre drivrutinssupport.

✅ Windows 8 och 8.1 (2012–2013)

Stort designomslag för att passa pekskärmar.

Startmenyn ersattes av Startskärmen – något som var impopulärt hos många användare.

Windows 8.1 förbättrade balansen mellan skrivbord och touch.

✅ Windows 10 (2015)

Återintroducerade Startmenyn i förbättrad form.

Designat som en “plattform” för ständiga uppdateringar.

Inkluderade funktioner som Windows Defender, Cortana och den nya webbläsaren Edge.

Första Windows som fick gratis uppdateringar på bred front.

✅ Windows 11 (2021 och framåt)

Modernare gränssnitt med centrerad Startmeny.

Fokus på design, säkerhet (t.ex. TPM-krav) och integration med molntjänster.

Förbättrad hantering av virtuella skrivbord och fönsterlayout (Snap Layouts).

Bygger fortfarande på NT-kärnan och har mycket gemensamt med Windows 10 under huven.

✅ Windows Server

Viktigt att förstå att Windows Server-versionerna är byggda på samma grund som desktop-versionerna.

Använder samma NT-kärna och liknande gränssnitt (exempel: Server 2008 R2 ≈ Windows 7, Server 2022 ≈ Windows 10/11).

Anpassat för serverroller som AD (Active Directory), fil- och printtjänster, DNS/DHCP, webbserver (IIS) m.m.

Eleverna kommer inte arbeta praktiskt med Server i årskurs 2, men ska känna till att det i grunden är samma operativsystem med fler funktioner och annan licensmodell.

5.1.2 Diskussions- och kontrollfrågor

Vad var skillnaden mellan Windows 95 och tidigare versioner?

Varför skapade Microsoft en separat NT-linje?

Vad gjorde Windows XP så populärt?

Varför blev Windows 8 kritiserat?

Hur skiljer sig Windows 11 från Windows 10?

Vad är skillnaden mellan Windows Desktop och Server?

5.1.3 Fördjupande länkar

Microsoft – History of Windows

Wikipedia – History of Microsoft Windows

How-To Geek – A Brief History of Windows

Microsoft – Windows Server Documentation (för den som vill se skillnader)

Computer Hope – Microsoft Windows Versions

5.1.4 Egna anteckningar

(Här kan du som elev skriva egna anteckningar om Windows historia, frågor eller reflektioner)

5.2 Uppbyggnad

Windows är ett modernt operativsystem med många komponenter som samarbetar för att ge en användarvänlig och flexibel plattform. Här går vi igenom några grundläggande byggstenar i Windows: enheter, filsystem, rättigheter (NTFS) och registret.

5.2.1 Enheter och enhetsbokstäver

Windows identifierar lagringsenheter med enhetsbokstäver, t.ex. C:, D:, E:.

Systemdisken är oftast C: och innehåller Windows-installationen.

USB-minnen, externa hårddiskar och optiska enheter får automatiskt nästa lediga bokstav.

Du kan ändra enhetsbokstäver i Diskhantering (diskmgmt.msc).

5.2.2 Filsystem och NTFS

Det vanligaste filsystemet i Windows är NTFS (New Technology File System).

NTFS har många fördelar jämfört med äldre FAT32:

Stöd för stora filer och diskar.

Möjlighet till filkomprimering.

Journalföring (skydd mot datakorruption).

Avancerade rättigheter och säkerhetsinställningar.

Alla moderna Windows-versioner (inkl. Server) använder NTFS som standard på systemdisken.

5.2.3 Rättigheter och behörigheter

NTFS-rättigheter styr vem som får göra vad med filer och mappar.

Du kan ange rättigheter via Egenskaper → Säkerhet i Utforskaren.

Exempel på rättigheter: Läs, Skriv, Ändra, Fullständig behörighet.

Rättigheter kan ärvas från mappstrukturen – bra för att hantera stora filsystem.

Administratörer kan alltid ta ägarskap och ändra behörigheter vid behov.

Viktigt för säkerhet i både hem- och företagsmiljöer.

5.2.4 Registret

Windows-registret är en hierarkisk databas som lagrar inställningar för operativsystemet och installerade program.

Består av nycklar och värden – ungefär som mappar och filer.

Centralt för konfiguration av Windows, drivrutiner och applikationer.

Kan redigeras med Registereditorn (regedit) – kraftfullt men riskabelt.

Viktigt att vara försiktig: felaktiga ändringar kan göra systemet instabilt eller obrukbart.

5.2.5 Sammanfattning

Windows bygger på en kombination av tydliga enhetsbokstäver, avancerat filsystem med säkerhetsfunktioner (NTFS), och ett centralt register som styr konfigurationen. Att förstå dessa delar är viktigt för både grundläggande användning och mer avancerad systemadministration.

5.2.6 Diskussions- och kontrollfrågor

Vad är enhetsbokstäver i Windows och vad används de till?

Vad är fördelarna med att använda NTFS jämfört med FAT32?

Hur kan du ändra rättigheter för en fil eller mapp i Windows?

Vad är Windows-registret och vad används det till?

Varför ska man vara försiktig när man ändrar i registret?

5.2.7 Fördjupande länkar

Microsoft – File Systems in Windows

Microsoft – NTFS Overview

Microsoft – Change Permissions for Files and Folders
  in-windows-8bfef146-0b22-47f6-9f77-5ef9f4e6a9d4

Microsoft – What is the Windows Registry?

Wikipedia – Windows Registry

5.2.8 Egna anteckningar

(Här kan du som elev skriva egna anteckningar om Windows uppbyggnad, frågor eller reflektioner)

5.3 Fördelar och nackdelar med Windows som operativsystem

Windows är världens mest använda stationära operativsystem. Enligt olika uppskattningar (2024) har Windows över 1,4 miljarder aktiva användare globalt, vilket gör det till en mycket dominerande plattform för både privatpersoner och företag.

Att förstå styrkor och svagheter med Windows är viktigt både som användare och som blivande IT-tekniker.

5.3.1 Skillnader mellan Windows-versioner

Windows finns i flera olika utgåvor, anpassade för olika användargrupper. I denna kurs arbetar vi främst med Windows 11 Pro, eftersom den är vanlig i skol- och företagsmiljö. Men det är bra att känna till skillnaderna mellan Home, Pro och Enterprise.

Tabellen på nästa sida visar viktiga skillnader:

💡 Att tänka på:

Home-versionen fungerar för hemmabruk men saknar funktioner som krävs i en IT-miljö.

Pro är den vanligaste versionen i utbildning, företag och labbmiljöer.

Enterprise används främst i större organisationer och hanteras via volymlicens och fjärradministration.

5.3.2 Fördelar

✅ Användarvänligt gränssnitt

Kända menyer, Start-knappen, och grafiskt skrivbord.

Lätt att komma igång även för nybörjare.

✅ Brett programstöd

Stort utbud av programvara, spel och affärsapplikationer.

Många leverantörer utvecklar främst för Windows.

✅ Hårdvarukompatibilitet

Stöd för en mängd olika tillverkare och drivrutiner.

Enklare att få hårdvara att “bara fungera” utan kompilering eller manuell konfiguration.

✅ Backat av Microsoft

Långsiktig support, regelbundna uppdateringar.

Microsoft 365-integration och molntjänster.

✅ Professionella verktyg och serverfunktioner

Active Directory, Group Policy, Hyper-V m.m.

Möjlighet att växa från hemmabruk till avancerade företagsmiljöer.

5.3.3 Nackdelar

⚠️ Licenskostnad

Inte gratis – licens krävs för varje dator.

Serverlicenser ännu dyrare.

⚠️ Stängd källkod

Inte möjligt att själv se eller modifiera systemets källkod.

Användare är beroende av Microsofts utveckling och prioriteringar.

⚠️ Resurskrävande

Nya versioner kan kräva kraftfullare hårdvara.

Äldre datorer kan bli långsamma eller obrukbara.

⚠️ Säkerhetsmål

På grund av sin stora spridning är Windows en vanlig måltavla för virus och malware.

Kräver aktivt underhåll som uppdateringar och antivirus.

⚠️ Komplexitet i företagsmiljöer

Kan vara svåradministrerat i större nätverk utan rätt kunskap.

Många olika versioner och licensmodeller att hålla reda på.

5.3.4 Sammanfattning

Windows är ett kraftfullt, välkänt och flexibelt operativsystem med mycket brett stöd – både i mjukvara och hårdvara. Samtidigt har det en del utmaningar kring licenskostnad, säkerhet och resurshantering.

Att förstå dessa styrkor och svagheter är viktigt för att kunna välja rätt system för rätt behov – både för privat användning och professionella IT-lösningar.

5.3.5 Diskussions- och kontrollfrågor

Varför är Windows så vanligt som operativsystem?

Nämn två fördelar med Windows som gör det lätt för nybörjare att använda.

Varför kan Windows bli en säkerhetsrisk om det inte underhålls?

Vad är en nackdel med att Windows är stängd källkod?

Varför kan licenskostnaden vara en nackdel för vissa användare?

5.3.6 Fördjupande länkar

Microsoft – Windows 11 Overview

Wikipedia – Usage share of operating systems

Microsoft Learn – What is Windows?

How-To Geek – Pros and Cons of Windows vs Linux

TechRadar – Windows 11 review

5.3.7 Egna anteckningar

(Här kan du som elev skriva egna anteckningar om Windows fördelar och nackdelar, frågor eller reflektioner)

5.4 Installation av Windows 11 i fysisk maskin/VM

Att kunna installera Windows 11 är en grundläggande färdighet både för privatpersoner och IT-tekniker. Här går vi igenom hur man laddar ner en ISO-fil, skapar ett startbart USB-minne, ändrar bootordning i BIOS/UEFI och installerar systemet, både på fysisk hårdvara och i en virtuell maskin.

5.4.1 Förberedelser

✅ Kontrollera systemkrav

Processor: 64-bitars, 1 GHz eller snabbare, minst 2 kärnor.

RAM: Minst 4 GB (rekommenderat 8+ GB).

Lagring: 64 GB eller mer.

TPM 2.0 och Secure Boot (krav för Windows 11).

5.4.2 Ladda ner Windows 11 ISO

Microsoft tillhandahåller ett officiellt verktyg som heter Media Creation Tool.

✅ Steg för steg:

Gå till den officiella nedladdningssidan:

Klicka på Download now under Media Creation Tool.

Kör verktyget när det laddats ner.

Välj Create installation media (USB flash drive, DVD, or ISO file).

Välj språk och edition.

Välj att skapa ISO-fil och spara den på datorn.

Alternativ: Skapa direkt USB om du redan har en sticka ansluten.

✅ För VM-installation räcker det att ha ISO-filen sparad lokalt.

5.4.3 Skapa en startbar USB-sticka

Om du ska installera på en fysisk dator behöver du göra ett USB-minne startbart.

✅ Media Creation Tool kan göra detta åt dig direkt:

Välj USB flash drive istället för ISO i steg 6 ovan.

Välj din USB-enhet (minst 8 GB rekommenderas).

Verktyget laddar ner och skriver filerna automatiskt.

✅ Alternativt kan du använda Rufus:

Hämta Rufus:

Starta programmet.

Välj din USB-enhet.

Välj din ISO-fil.

Kontrollera partitionstyp (GPT för UEFI).

Klicka Start.

5.4.4 Ändra bootordning i BIOS/UEFI

För att starta från USB behöver du ofta ändra bootordning:

✅ Steg för steg:

Starta om datorn.

Tryck rätt tangent för BIOS/UEFI (vanligtvis Del, F2, F10 eller Esc – står oftast på skärmen).

Leta upp Boot Order eller Boot Priority.

Sätt USB-enheten högst upp i listan.

Spara och avsluta (Save & Exit).

Datorn startar om från USB-stickan.

5.4.5 Installera Windows 11

✅ Steg för steg-installation:

Välj språk, tid och tangentbord.

Klicka på Install now.

Ange produktnyckel eller välj I don’t have a product key.

Välj edition (Pro eller Home).

Acceptera licensvillkoren.

Välj Custom: Install Windows only (advanced).

Välj/Skapa partition (ta bort gamla om du vill rensa disken helt).

Installationen körs automatiskt och datorn startar om flera gånger.

Konfigurera språk, region och tangentbord efter första uppstart.

5.4.6 Skapa lokalt konto på Windows 11 (offline)

För att slippa Microsoft-konto kan du göra så här vid kontoinställning:

✅ Steg för steg:

När du kommer till inloggningssteget – koppla ur nätverkskabel eller inaktivera Wi-Fi.

Windows försöker tvinga onlinekonto men erbjuder alternativ för offlinekonto/offlinekonto eller “Limited Experience”.

Om du inte ser alternativet:

Tryck Shift + F10 för att öppna kommandoprompt.

Skriv: start ms-cxh:localonly

Tryck Enter.

Skärmen för lokalt konto visas.

Ange användarnamn och lösenord.

✅ Detta fungerar även i VM om du "stänger av nätverk" under installationen.

5.4.7 Installation i virtuell maskin

Att installera Windows 11 i en virtuell maskin (t.ex. VirtualBox eller VMware) är snarlikt:

✅ Steg för steg:

Skapa en ny VM med typ Windows 11.

Tilldela minst 4 GB RAM och 64 GB disk (rekommenderat mer för bättre prestanda).

Montera ISO-filen som optisk enhet i VM-inställningarna.

Starta VM – installationsprogrammet startar direkt.

Följ samma installationssteg som på fysisk maskin.

För offlinekonto – koppla ur nätverkskortet i VM-inställningarna eller använd Shift + F10-tricket.

5.4.8 Diskussions- och kontrollfrågor

Vilket verktyg tillhandahåller Microsoft för att ladda ner och skapa installationsmedia?

Vad behöver du göra i BIOS/UEFI för att starta från USB?

Varför behöver man ibland ändra bootordning?

Hur kan man skapa ett lokalt offlinekonto på Windows 11?

Vad är en fördel med att installera i en virtuell maskin jämfört med på fysisk hårdvara?

5.4.9 Egna anteckningar

(Här kan du som elev skriva egna anteckningar om installationen, kommandon, eller saker du vill komma ihåg)

5.5 Konfiguration och hantering av Windows

När Windows är installerat behöver du kunna hantera och konfigurera det på rätt sätt. Här går vi igenom grunderna i att installera och avinstallera program, filhantering, användarhantering och rättigheter samt felsökning och underhåll.

5.5.1 Installera och avinstallera program

✅ Från webben

Ladda ner installationsfil (ofta .exe eller .msi).

Kör filen som administratör vid behov.

Följ installationsguiden.

Programmet hamnar vanligtvis i C:\Program Files eller C:\Program Files (x86).

✅ Från Microsoft Store

Öppna Microsoft Store.

Sök efter appen.

Klicka Installera.

Appar från Store är ofta enklare att uppdatera och hantera.

✅ Avinstallera program

Gå till Inställningar → Appar → Appar och funktioner.

Välj programmet och klicka Avinstallera.

Alternativt via Kontrollpanelen → Program och funktioner.

5.5.2 Filhantering

✅ Skapa mappar

Högerklicka i Utforskaren → Ny mapp.

Namnge mappen direkt.

✅ Flytta och kopiera

Dra och släpp mellan mappar eller diskar.

Ctrl+C (kopiera), Ctrl+V (klistra in), Ctrl+X (klipp ut).

Högerklicka → Kopiera eller Klipp ut, och Klistra in.

✅ Sökvägar

Visar var filer finns på disken.

Exempel:

C:\Users\Namn\Documents

D:\Backup\Bilder

Viktigt att hålla ordning för att snabbt hitta filer.

✅ Visa filändelser

Utforskaren → Visa → markera Filnamnstillägg.

Bra för att se filtyper (.exe, .txt, .jpg).

5.5.3 Användarhantering, grupper och rättigheter (Windows 11 Pro)

Kontotyper

Windows har olika kontotyper som styr vad användaren får göra på datorn:

Standardanvändare (User):

Kan använda installerade program.

Kan ändra sina egna inställningar och filer.

Kan inte installera eller ta bort program för alla användare.

Kan inte ändra systeminställningar som påverkar andra.

Administratör (Administrator):

Full behörighet att ändra alla inställningar.

Kan installera och ta bort program för alla användare.

Kan skapa eller ta bort användarkonton.

Kan ändra säkerhetsinställningar och köra alla program som administratör.

✅ Viktigt: För att skydda systemet bör vanliga användare inte alltid köra som administratör.

Grupper och hur de påverkar rättigheter

Windows använder grupper för att förenkla hantering av behörigheter. En grupp är en samling användare med samma rättigheter.

Vanliga grupper:

Administrators – fullständig kontroll över datorn.

Users – standardanvändare med begränsad åtkomst.

Guests – mycket begränsad åtkomst för tillfälliga användare.

✅ Exempel:
 Om du lägger en användare i gruppen Administrators får hen automatiskt alla administratörsrättigheter.

✅ Hantering av grupper och konton:

Inställningar → Konton → Andra användare – för enkel hantering.

Lokal användar- och grupphantering (lusrmgr.msc) – i Pro-versioner för att mer avancerat skapa, ändra eller ta bort konton och grupper.

✅ Viktigt att förstå:
 Grupper används för att enkelt tilldela rättigheter till flera användare utan att behöva sätta rättigheter individuellt på varje användare.

Rättigheter i filsystemet (NTFS)

Windows använder NTFS (New Technology File System) för att hantera rättigheter på filer och mappar. Det låter dig styra exakt vad olika användare eller grupper får göra.

✅ Exempel på rättigheter:

Läsa: Öppna filer, visa innehåll.

Skriva: Skapa eller ändra filer.

Ändra: Kombinerar läsa, skriva och ta bort.

Fullständig behörighet: Alla ovanstående + ändra ägare och rättigheter.

✅ Ärvda rättigheter

Som standard ärver nya filer och mappar rättigheter från den mapp de ligger i.

Det gör det enklare att hantera behörighet i hela mappstrukturer.

Du kan bryta ärvning om du behöver anpassa rättigheterna för en specifik fil eller mapp.

✅ Hantera rättigheter

Högerklicka på fil eller mapp → Egenskaper → Säkerhet.

Här kan du se och ändra vilka användare och grupper som har rättigheter.

Under Avancerat kan du se ärvda rättigheter och ändra ägarskap.

✅ Viktigt att veta:

Administratörer kan alltid ta ägarskap över filer eller mappar, även om de saknar andra rättigheter.

Att förstå och använda rättigheter korrekt är en viktig del av säkerheten både hemma och i företagsmiljö.

5.5.4 Felsökning och underhåll

Windows har många inbyggda verktyg för att hålla systemet i gott skick. Här är viktiga exempel – med hur du hittar dem och vad de gör:

✅ Standardprogram (Default apps)

Hur hittar du det?

Inställningar → Appar → Standardappar.

Vad gör den?

Styr vilket program som öppnar olika filtyper, t.ex. webbsidor eller bilder.

✅ Diskrensning (Disk Cleanup)

Hur hittar du det?

Sök i Startmenyn: Diskrensning.

Vad gör den?

Tar bort tillfälliga filer och frigör utrymme på disken.

✅ chkdsk

Hur hittar du det?

Kommandoprompt som administratör → skriv chkdsk.

Viktiga växlar:

/f (fixar fel), /r (letar dåliga sektorer och återställer data).

Vad gör den?

Kontrollerar och reparerar filsystemfel på disken.

✅ Defragmentera / Optimize Drives

Hur hittar du det?

Sök i Startmenyn: Defragmentera eller Optimize Drives.

Vad gör den?

Omorganiserar filer på hårddisken för snabbare åtkomst (SSD använder trim).

✅ Felsökning (Troubleshoot)

Hur hittar du det?

Inställningar → System → Felsökning.

Vad gör den?

Guidade lösningar för vanliga problem (ljud, nätverk, uppdateringar).

✅ Kompatibilitetsläge (Compatibility settings)

Hur hittar du det?

Högerklick på program → Egenskaper → Kompatibilitet.

Vad gör den?

Gör att äldre program kan köras som om de vore på tidigare Windows-versioner.

✅ Tillförlitlighetshistorik (Reliability Monitor)

Hur hittar du det?

Sök i Startmenyn: Tillförlitlighetshistorik.

Vad gör den?

Visar stabilitetsproblem, krascher och ger lösningsförslag.

✅ Aktivitetshanteraren (Task Manager)

Hur hittar du det?

Ctrl+Shift+Esc eller högerklick på aktivitetsfältet.

Vad gör den?

Visar aktiva program, processer och resursanvändning.

✅ Resursövervakaren (Resource Monitor)

Hur hittar du det?

Sök i Startmenyn: Resursövervakaren.

Vad gör den?

Ger detaljerad information om CPU, minne, disk och nätverk.

✅ Msconfig / Systemkonfiguration

Hur hittar du det?

Sök i Startmenyn: Systemkonfiguration eller kör msconfig.

Vad gör den?

Hanterar uppstartsalternativ, tjänster och boot-inställningar.

✅ Minnesdiagnostik

Hur hittar du det?

Sök i Startmenyn: Windows Memory Diagnostic.

Vad gör den?

Testar datorns RAM-minne för fel.

✅ Lokal säkerhetsprincip (Local Security Policy)

Hur hittar du det?

Sök i Startmenyn: Local Security Policy (Pro/Enterprise).

Vad gör den?

Hanterar säkerhetsregler som lösenordspolicyer och användarrättigheter.

✅ Fjärrskrivbord (Remote Desktop)

Hur hittar du det?

Inställningar → System → Fjärrskrivbord.

Vad gör den?

Gör att du kan fjärransluta till datorn via RDP.

✅ Registereditorn

Hur hittar du det?

Sök i Startmenyn: regedit.

Vad gör den?

Visar och låter dig redigera Windows-registret (avancerat).

✅ Enhetshanteraren (Device Manager)

Hur hittar du det?

Högerklick på Start → Enhetshanteraren.

Vad gör den?

Visar och hanterar drivrutiner och anslutna enheter.

✅ Schemaläggaren (Task Scheduler)

Hur hittar du det?

Sök i Startmenyn: Schemaläggaren.

Vad gör den?

Skapa och hantera automatiska uppgifter.

✅ diskpart

Hur hittar du det?

Öppna Kommandoprompt som administratör → skriv diskpart.

Vad gör den?

Avancerat verktyg för att hantera diskar och partitioner.

✅ Utskriftshantering (Print Management)

Hur hittar du det?

Sök i Startmenyn: Print Management (Pro/Enterprise).

Vad gör den?

Hanterar skrivare och utskriftsköer.

✅ Hjälpmedel (Accessibility)

Hur hittar du det?

Inställningar → Hjälpmedel.

Vad gör den?

Anpassar datorn för olika funktionshinder (förstoringsglas, skärmläsare, högkontrast).

5.5.5 Diskussions- och kontrollfrågor

Vad är skillnaden mellan en standardanvändare och en administratör?

Hur används grupper för att styra rättigheter i Windows?

Vad betyder att rättigheter ärvs i en mappstruktur?

Hur kan du kontrollera och ändra rättigheter på en fil eller mapp?

Ge exempel på tre Windows-verktyg du kan använda för att felsöka eller underhålla datorn.

5.5.6 Egna anteckningar

(Här kan du som elev skriva egna anteckningar om användarhantering, rättigheter eller felsökning i Windows)

