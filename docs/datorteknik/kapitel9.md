---
title: 9 – Introduktion till IT-säkerhet
nav_order: 7
---

# 9 – Introduktion till IT-säkerhet

9.1 Vad är IT-säkerhet?

IT-säkerhet handlar om att skydda digital information, system och tjänster mot obehörig åtkomst, skada eller avbrott. Det inkluderar både tekniska lösningar, som brandväggar och kryptering, och organisatoriska åtgärder, som rutiner och policies.

En fungerande IT-säkerhet ser till att rätt personer har tillgång till rätt information vid rätt tidpunkt – och att obehöriga inte har det. Samtidigt handlar det om att kunna lita på att informationen inte manipulerats och att den finns tillgänglig när den behövs.

För företag och organisationer är IT-säkerhet avgörande. Inte bara för att skydda interna resurser, utan också för att uppfylla lagkrav som GDPR och för att upprätthålla kundernas förtroende. För privatpersoner handlar det ofta om att skydda personliga uppgifter, bilder, bankinformation och annan känslig data.

9.1.1 Hotbild och risker

IT-säkerhet hotas ständigt av olika typer av attacker, både avsiktliga och oavsiktliga. De vanligaste hoten kan delas in i följande kategorier:

Malware (skadlig kod): Virus, trojaner, maskar, spyware och ransomware används för att stjäla information, låsa datorer eller sprida sig till andra system.

Social engineering: Manipulationstekniker där angriparen försöker lura användare att avslöja information eller klicka på farliga länkar, t.ex. via phishing-mail.

Dataintrång: Angripare som bryter sig in i nätverk eller system för att komma åt känslig data.

Slarv eller misstag: Mänskliga fel, t.ex. svaga lösenord eller felaktig konfiguration, står bakom många säkerhetsproblem.

Insiderhot: Anställda eller tidigare anställda som utnyttjar sin behörighet för att skada verksamheten.

Avbrott och störningar: DDoS-attacker, hårdvarufel eller elavbrott som gör system otillgängliga.

I takt med att allt fler tjänster flyttas till molnet och fler enheter kopplas upp (IoT), ökar attackytan – och behovet av god säkerhet ökar i samma takt.

9.1.2 CIA-triaden

CIA-triaden är en grundmodell inom IT-säkerhet och beskriver tre viktiga principer som all säkerhetsarbete bör utgå ifrån:

C – Confidentiality (Sekretess)

Endast behöriga personer ska kunna ta del av viss information. Exempel: lösenordsskyddade filer, krypterade meddelanden och åtkomstkontroll på nätverksresurser.

I – Integrity (Integritet)

Information ska vara korrekt och inte ha förändrats utan tillstånd. Exempel: kontrollsummor, loggning av ändringar och signering av dokument.

A – Availability (Tillgänglighet)

System och data ska vara tillgängliga när de behövs. Exempel: redundanta servrar, UPS (avbrottsfri strömförsörjning) och skydd mot DDoS-attacker.

Ett välbalanserat säkerhetsarbete tar hänsyn till alla tre. Om man skyddar informationen så hårt att den inte går att använda, är tillgängligheten hotad. Om man däremot släpper in alla, förloras både sekretess och integritet.

9.1.3 Kontrollfrågor

Vad innebär begreppet IT-säkerhet?

Nämn tre exempel på vanliga hot mot IT-system.

Vad är skillnaden mellan ett virus och en trojan?

Hur fungerar social engineering?

Varför är användarnas misstag ett säkerhetsproblem?

Vad innebär "insiderhot" inom IT-säkerhet?

Beskriv vad "C" i CIA-triaden står för och ge ett exempel.

Vad innebär "I" i CIA-triaden?

Hur skyddar man tillgängligheten i ett IT-system?

Hur kan man uppnå balans mellan sekretess, integritet och tillgänglighet?

9.1.4 Fördjupningslänkar

Microsoft – What is cybersecurity?

CISA – Cybersecurity Awareness

OWASP Top 10 (hot och sårbarheter)

MSB – Så skyddar du dig mot nätfiske

CERT-SE – Aktuella hot och sårbarheter

9.1.5 Egna anteckningar

(Lämna plats för elevernas egna reflektioner och noteringar här)

9.2 Skydd på olika nivåer

Fysisk säkerhet är en grundläggande men ofta förbisedd del av IT-säkerheten. Den handlar om att skydda själva utrustningen – servrar, datorer, nätverksutrustning och annan hårdvara – från fysiska hot som stöld, sabotage, brand eller oavsiktlig skada.

Ett serverrum bör till exempel ha lås, brandlarm, övervakning och skydd mot överspänning. Endast behörig personal ska ha tillgång, gärna genom passerkort eller biometriska system. Kablar bör inte vara lättillgängliga, särskilt inte om de leder till nätverksinfrastruktur eller kritisk utrustning.

Även bärbara datorer, USB-minnen och mobila enheter bör hanteras med försiktighet. En förlorad laptop utan kryptering kan leda till dataintrång, även om den aldrig kopplas upp mot ett nätverk.

9.2.1 Användarsäkerhet

Lösenord – varför längd och variation spelar roll

Ett lösenords styrka beror på:

Hur långt det är

Vilka tecken det innehåller

Om det är lätt att gissa (t.ex. "password123")

Ett vanligt sätt att förstå styrkan hos lösenord är att räkna hur många möjliga kombinationer som finns. Det görs med formeln:

Möjliga kombinationer = antal möjliga teckenⁿ, där n = lösenordets längd

Exempel:

Och med 8 tecken?

96⁸ ≈ 7 213 895 789 838 336 kombinationer – över 7 biljarder

Detta är varför ett lösenord på bara 6 tecken kan knäckas på sekunder vid en bruteforce-attack – medan ett starkt lösenord på 12 tecken kan ta flera tusen år att knäcka, även med kraftfull hårdvara.

Tips till eleverna: Ett säkert lösenord bör vara minst 12 tecken långt, gärna en "lösenordsfras" (t.ex. KorvMedBröd!2025) som är både stark och lätt att komma ihåg.

Flerfaktorsautentisering (MFA) – vad det är och hur det funkar

Att ha ett starkt lösenord är bra – men det räcker inte alltid. Därför använder man ofta flerfaktorsautentisering (MFA), som kräver minst två olika typer av bevis på att du är du.

De tre autentiseringsfaktorerna:

För att räknas som MFA måste du kombinera minst en från två olika kategorier
 (Två lösenord är inte MFA – det är bara två saker du vet)

Exempel på MFA-lösningar:

MFA skyddar användarkonton även om lösenordet skulle bli stulet – eftersom angriparen saknar din telefon eller ditt fingeravtryck.

9.2.2 Programvarusäkerhet – Antivirus och uppdateringar

Ett vanligt misstag bland användare är att tro att ett installerat antivirusprogram automatiskt gör datorn "osårbar". Så är det inte. Antivirus är en viktig del av säkerheten – men bara om det hålls uppdaterat och används tillsammans med andra säkerhetsåtgärder.

Antivirusprogram fungerar ungefär som ett vaccin: de letar efter och blockerar kända hot, baserat på en databas med virusdefinitioner. Därför är det avgörande att dessa viruslistor uppdateras regelbundet, annars blir skyddet snabbt föråldrat. Ett antivirusprogram som inte uppdateras ger bara en falsk trygghet.

Det är också viktigt att själva programmet uppdateras, eftersom även antivirus kan innehålla sårbarheter som måste rättas till.

🛡️ Exempel på vanliga antivirusprogram (kommersiella och gratis):

1. Bitdefender – Känt för hög upptäcktsgrad och låg systempåverkan. Finns i både gratis- och betalversion.
2. Avast – Populärt gratisprogram med tilläggsfunktioner som brandvägg och lösenordshanterare.
3. Kaspersky – Ryskt ursprung men tekniskt välrenommerat. Används både av privatpersoner och företag.
4. ESET NOD32 – Lättviktigt program med god realtidsövervakning och låg påverkan på prestanda.
5. Windows Defender – Inbyggt i Windows 10/11 och ger ett grundskydd direkt ur lådan. Har förbättrats kraftigt de senaste åren och är numera ett fullvärdigt alternativ.

Att ha ett antivirusprogram betyder dock inte att man kan klicka på vad som helst eller surfa in på okända sidor utan risk. Antivirus är bara en del av ett större skydd. Det viktigaste skyddet är användaren själv – och det sunda förnuftet.

Alla antivirusprogram är inte bara skydd. I vissa fall har de visat sig själva vara en risk.

Ett uppmärksammat exempel är Avast, som under flera år samlade in stora mängder användardata via sitt antivirusprogram. Informationen såldes sedan vidare till tredjepartsföretag genom ett dotterbolag – något som ledde till stämningar, kraftig kritik och till slut att bolaget stängde ner verksamheten för datainsamlingen.

Även andra antivirusprogram samlar in telemetridata, alltså information om hur programmet används, vilka webbplatser som besöks, vilka filer som analyseras etc. Detta sker ofta "i bakgrunden" och finns ibland nämnt i användarvillkoren eller integritetspolicyn.

💡 Tips: Innan du installerar ett antivirusprogram – läs på! Kontrollera hur programmet hanterar din data, om det går att stänga av datainsamling, och hur företaget tjänar pengar på sin produkt (särskilt om den är gratis).

9.2.3 Nätverkssäkerhet

Nätverkssäkerhet handlar om att skydda all data som färdas mellan enheter – oavsett om det är inom ett lokalt nätverk eller över internet. Eftersom nätverket är den digitala motsvarigheten till en motorväg är det också ett favoritmål för angripare. Därför är det avgörande att övervaka, begränsa och skydda trafiken på olika nivåer.

Brandväggar – nätverkets väktare

En brandvägg är en säkerhetsmekanism som kontrollerar vilken trafik som får komma in eller ut ur ett nätverk eller en dator. Det finns två huvudtyper:

Nätverksbrandväggar: Skyddar hela nätverk, ofta placerade i routrar eller dedikerade säkerhetsenheter.

Host-baserade brandväggar: Körs direkt på en enhet, t.ex. Windows Firewall.

Regler kan skapas för att:

Blockera eller tillåta specifika portar (t.ex. blockera FTP om det inte används)

Begränsa trafik till vissa IP-adresser eller nätverk

Förhindra oönskad inkommande trafik från internet

Ett vanligt misstag är att öppna för mycket. "Allow all" är bekvämt – men livsfarligt.

VPN – Krypterad tunnel för säker anslutning

Ett Virtual Private Network (VPN) krypterar trafiken mellan en användare och ett nätverk. Det är särskilt användbart för:

Fjärrarbete (hemifrån, resa)

Att skydda data i osäkra nätverk (t.ex. offentligt Wi-Fi)

Att dölja IP-adressen eller plats (används både av privatpersoner och företag)

Med VPN skapas en "tunnel" där trafik inte kan läsas av obehöriga. Det är som att färdas i en privat, ogenomskinlig rörpost i det öppna internet.

IDS/IPS – Larmsystem i nätverket

Intrusion Detection Systems (IDS) och Intrusion Prevention Systems (IPS) är säkerhetslösningar som:

IDS övervakar trafiken och larmar om misstänkta mönster upptäcks

IPS försöker stoppa angreppet i realtid

De är särskilt effektiva mot:

Portscanningar

Brute-force-attacker

Försök att utnyttja kända sårbarheter (exploit kits)

Moderna lösningar kombinerar IDS och IPS, ibland kallade NIDS/NIPS (Network-based Intrusion Detection/Prevention System).

Segmentering – att inte lägga alla ägg i samma korg

Ett vanligt nybörjarmisstag är att lägga alla enheter i samma nätverk. Genom att segmentera nätverket – t.ex. med VLAN (Virtual LAN) – kan man begränsa skadorna vid en attack.

Exempel:

Gästenheter får endast internetåtkomst, inte till servrar eller skrivare

IoT-enheter isoleras i ett eget nät

Administration hanteras i ett separat segment

Segmentering bygger på principen om minsta möjliga åtkomst och gör det mycket svårare för en angripare att röra sig fritt inom nätverket.

9.2.4 Kontrollfrågor

Vad är skillnaden mellan en host-baserad brandvägg och en nätverksbrandvägg?

Varför är det viktigt att ha brandväggsregler som endast tillåter nödvändig trafik?

Vad gör ett VPN?

När kan ett VPN vara extra användbart?

Vad är ett IDS och vad är dess syfte?

Hur skiljer sig ett IPS från ett IDS?

Ge ett exempel på en typ av attack som IDS/IPS kan upptäcka.

Vad menas med nätverkssegmentering?

Ge ett exempel på hur VLAN kan öka säkerheten i ett nätverk.

Vad innebär principen om "minsta möjliga åtkomst"?

9.2.5 Fördjupningslänkar

Cisco – Vad är en brandvägg?

Cloudflare – Vad är VPN och hur fungerar det?

Fortinet – Vad är IDS och IPS?

Palo Alto – Network Segmentation

MSB – Segmentera ditt nätverk

9.2.6 Egna anteckningar

(Lämna plats för egna reflektioner och fördjupningar här.)

9.3 Trådlös säkerhet

Trådlösa nätverk – som Wi-Fi – har blivit standard i både hem och företag. De är enkla att sätta upp, men också lätta att attackera om man inte tänker på säkerheten. Eftersom signalerna sprids genom luften, räcker det att befinna sig inom räckvidd för att kunna försöka avlyssna eller manipulera trafiken. Därför krävs särskilda skyddsåtgärder.

9.3.1 Historik – från WEP till WPA3

WEP – Wired Equivalent Privacy (1997)

När Wi-Fi började användas på 90-talet var WEP det första säkerhetsprotokollet. Namnet antydde att det skulle ge samma säkerhet som ett trådbundet nätverk. I verkligheten var det katastrofalt svagt.

Problem:

Använde statiska krypteringsnycklar (ofta 64 eller 128 bitar)

Byggde på RC4, en sårbar algoritm

Kunde knäckas på några minuter med enkla verktyg

WPA och WPA2 (2003–2004)

När sårbarheterna i WEP blev kända utvecklades WPA (Wi-Fi Protected Access) som en tillfällig lösning. Sen kom WPA2, som använde AES-kryptering – mycket starkare än RC4.

WPA använde TKIP, vilket var bättre än WEP men fortfarande inte perfekt.

WPA2 införde CCMP (AES-baserad kryptering) och blev snabbt branschstandard.

WPA3 (2018)

Efter flera attacker mot WPA2 (bl.a. KRACK-attacken) kom WPA3, som:

Använder SAE istället för PSK (förhindrar bruteforce offline)

Har förbättrad kryptering för öppna nätverk

Ger framåtsekretess (t.ex. skyddar gamla sessioner om lösenordet läcker)

❗ OBS: Alla routrar stöder inte WPA3 ännu. Ibland måste det aktiveras manuellt i inställningarna.

9.3.2 Skyddsåtgärder för trådlösa nätverk

Att bara "ha ett lösenord på Wi-Fi" räcker inte. Här är några centrala skyddsåtgärder:

9.3.3 Vanliga attacker mot Wi-Fi

Evil Twin / Rogue Access Point

Angriparen sätter upp ett falskt nätverk med liknande namn som ditt riktiga – t.ex. "Skola_Guest" → "Sk0la_Guest". Om en användare ansluter kan all trafik avlyssnas eller manipuleras.

Deauthentication attacks

Med verktyg som aireplay-ng kan en angripare tvinga bort användare från nätverket, i hopp om att de ska återansluta – till ett falskt nätverk (Evil Twin).

Packet sniffing

Med t.ex. Wireshark kan trafik över ett öppet eller dåligt säkrat nätverk analyseras – och ibland även avlyssnas. Krypterad trafik skyddas, men metadata (vilka sidor som besöks, DNS-frågor etc.) kan fortfarande avslöjas.

Brute-force/WPS-attacker

Om WPS (Wi-Fi Protected Setup) är aktiverat, kan en angripare försöka gissa PIN-koden som används för att koppla upp sig – en funktion som bör stängas av.

🛡 Tips: Ha som regel att alltid stänga av WPS. Det är sällan värt bekvämligheten.

9.3.4 Kontrollfrågor

Vad stod WEP för och varför var det osäkert?

Vad är skillnaden mellan WPA och WPA2?

Vilken typ av kryptering använder WPA2?

Vad gör WPA3 mer säkert än tidigare versioner?

Vad är en "Evil Twin"-attack?

Hur kan man upptäcka eller skydda sig mot en rogue access point?

Vad innebär en deauthentication-attack?

Vad kan verktyg som Wireshark användas till?

Varför bör man undvika att använda WPS?

Ge tre konkreta tips på hur man säkrar ett trådlöst nätverk.

9.3.5 Fördjupningslänkar

Wikipedia – WEP

Comparitech – WPA vs WPA2 vs WPA3

Wireshark – Official Site

Aircrack-ng Suite – Verktyg för trådlösa tester

MSB – Säker användning av trådlösa nätverk

9.3.6 Egna anteckningar

(Lämna plats för egna reflektioner och fördjupningar här.)

9.4 Säkerhet i Windowsmiljö

9.4.1 Windows Security Center

Windows Security Center (eller Säkerhetscenter) är den centrala platsen där användare och administratörer får en översikt över datorns säkerhetsstatus. Det introducerades redan i Windows XP Service Pack 2 och har utvecklats rejält i senare versioner, särskilt i Windows 10 och 11 där det numera heter Windows Security (Windows-säkerhet).

Här samlas flera viktiga funktioner i ett enda gränssnitt:

Virus- och hotskydd (Windows Defender)

Kontoskydd (UAC, inloggning, MFA)

Brandvägg och nätverksskydd

App- och webbläsarkontroll (SmartScreen, isolering)

Enhetssäkerhet (t.ex. SecureBoot, TPM)

Enhetsprestanda och hälsa

Familjealternativ (föräldrakontroll)

Syfte: Att ge användaren ett tydligt, samlat läge där man snabbt ser om något är fel – t.ex. om antivirus är inaktiverat, om brandväggen är avstängd eller om det saknas viktiga uppdateringar.

👉 Tips för användare: Du hittar det via Inställningar → Uppdatering och säkerhet → Windows-säkerhet eller genom att söka på "Windows Security" i Start-menyn.

Fun fact: Om du installerar ett annat antivirusprogram (t.ex. Norton eller Avast), ersätts ofta vissa funktioner i Windows Security – men det fortsätter ändå att visa status och meddela om något saknas.

9.4.2 UAC – User Account Control

User Account Control (UAC) är en säkerhetsfunktion som kontrollerar vem som får göra vad i systemet – särskilt när det gäller att ändra inställningar som påverkar hela datorn.

Vad gör UAC?
 När du försöker göra något som kräver administratörsrättigheter (t.ex. installera program, ändra systemfiler, starta kommandotolk som admin), dyker det upp en UAC-ruta som frågar:
 ”Vill du tillåta att den här appen gör ändringar på din enhet?”

Om du är inloggad som standardanvändare måste du ange ett adminlösenord. Om du redan är admin måste du bekräfta ditt val.

Varför finns det?
Innan UAC (t.ex. i Windows XP) kördes de flesta användare som administratörer hela tiden – vilket gjorde det enkelt för virus och skadlig kod att göra ändringar i systemet.
Med UAC körs program som vanliga användare tills du aktivt godkänner att de får göra större förändringar. Det är ett slags digital spärr – som en säkerhetsvakt vid dörren.

UAC-nivåer (Windows 10/11):

🟥 Alltid meddela – Frågar även om du gör ändringar via kommandorad

🟧 Meddela endast vid appar från tredje part – Standardnivå

🟨 Meddela inte – Riskabelt, bör undvikas

👀 Typiska scenarier där UAC dyker upp:

UAC skyddar även mot skadlig kod som försöker köra i bakgrunden utan att du vet om det – eftersom programmet måste få godkännande innan det får högre rättigheter.

9.4.3 Windows Defender (Microsoft Defender)

Windows Defender, numera kallat Microsoft Defender Antivirus, är Microsofts inbyggda antiviruslösning i Windows 10 och 11. Det är gratis, automatiskt aktiverat och ger ett grundskydd direkt efter installation av operativsystemet.

Funktioner i Microsoft Defender:

Realtidsskydd – söker efter och blockerar virus, trojaner, spyware m.m.

Molnskydd – använder Microsofts molntjänster för att snabbt identifiera nya hot

Ransomware-skydd – övervakar känsliga mappar mot kryptering

SmartScreen-filter – varnar för farliga webbsidor och nedladdningar

Offline-genomsökning – kan köras utanför Windows för att ta bort svårupptäckta hot

Utveckling: När det först lanserades hade det relativt dåligt rykte – men idag presterar Microsoft Defender på samma nivå som många kommersiella alternativ (enligt oberoende tester som AV-Test.org).

Konfiguration och översikt:
Du hittar Defender via Inställningar → Uppdatering och säkerhet → Windows-säkerhet → Virus- och hotskydd.

Bra att veta:
Om du installerar ett annat antivirusprogram, t.ex. Kaspersky eller Bitdefender, stängs Defender automatiskt av för att undvika konflikt. Du kan då behöva manuellt aktivera det igen om du tar bort det andra programmet.

Defender är mer än antivirus: I företagsmiljö används Microsoft Defender for Endpoint, som innehåller avancerad hotdetektion, analys, och integration med Azure och andra Microsoft 365-tjänster.

Tips: Defender räcker gott för de flesta elever och privatpersoner – så länge man har försiktigt surfande, starka lösenord och regelbundna uppdateringar.

9.4.4 Gruppolicy och säkerhetsmallar (Group Policy & Security Templates)

Group Policy (gruppolicy) är ett kraftfullt verktyg i Windows – särskilt i företagsmiljöer – för att centralt styra hur datorer, konton och säkerhetsinställningar fungerar.

Tänk dig en skola med 100 datorer. Istället för att sitta och manuellt konfigurera varje dator kan man använda en gruppolicy för att bestämma allt från skrivbordsbakgrund till vilka program som får köras – och vad eleverna inte får göra.

Exempel på vad du kan styra med Group Policy:

Tvinga starka lösenord och lösenordsbyte var 90:e dag

Blockera åtkomst till Kontrollpanelen

Förhindra att USB-minnen används

Tvinga uppdateringar av antivirus eller system

Automatisk inloggning av program

Begränsa internetanvändning

Säkerhetsmallar (Security Templates)
 Det finns färdiga mallar som innehåller rekommenderade säkerhetsinställningar. Dessa kan importeras via Group Policy för att snabbt säkra t.ex. arbetsstationer, servrar eller elevernas datorer.

Gruppolicy Editor (gpedit.msc)
 Verktyget används lokalt på datorer för att visa och redigera policys. Dock endast tillgängligt i Pro- eller Enterprise-versionerna av Windows (inte Home).

Domänmiljö och Active Directory (AD)
 I större nätverk hanteras Group Policies via Group Policy Management Console (GPMC) och tillämpas automatiskt på alla datorer i domänen. Då kan man ha olika policies beroende på användargrupp, avdelning, datorrum m.m.

9.4.5 NTFS-behörigheter – vem får göra vad?

NTFS (New Technology File System) är det filsystem som används i moderna Windows-versioner, och det innehåller stöd för avancerad behörighetskontroll. Det gör att du kan styra exakt vem som får läsa, skriva, ändra eller ta bort filer och mappar.

Varför är detta viktigt?
Tänk dig en skoldator där vem som helst kan radera andras filer – eller en server där elever kan läsa betygsfiler. Rätt behörigheter är en grundpelare i IT-säkerhet.

De vanligaste NTFS-behörigheterna:

Behörigheter kan sättas på individer eller grupper – t.ex. att alla i gruppen Lärare får läsa en mapp, men bara Admin får ändra.

Ärvda behörigheter:
Mappar ärver ofta rättigheter från sin överordnade mapp. Det går att bryta ärvningen om man vill ha särskilda regler.

Tips:

Använd minsta nödvändiga behörighet – användare bör inte ha mer rättigheter än de behöver.

Använd grupper istället för att sätta rättigheter på varje användare. Det gör administrationen enklare.

Undvik att ge "Alla" fullständig åtkomst till något – det är som att lämna dörren olåst.

9.4.6 BitLocker – kryptera hårddisken

BitLocker är Windows inbyggda verktyg för att kryptera hela hårddisken. Det gör att ingen kan läsa datan utan rätt nyckel, inte ens om de fysiskt stjäl datorn.

Hur fungerar det?
När BitLocker är aktiverat krypteras all data automatiskt i bakgrunden. Vid uppstart kontrolleras att systemet inte har manipulerats. För att låsa upp krävs en av följande:

TPM (Trusted Platform Module) – en hårdvarumodul som lagrar krypteringsnyckeln säkert

PIN-kod

USB-nyckel

Microsoft-konto eller domäninloggning

Varför använda BitLocker?

Skyddar känsliga filer även om datorn blir stulen

Krävs i många företag p.g.a. lagkrav och GDPR

Kan användas tillsammans med Windows Hello och/eller TPM för smidig inloggning

BitLocker To Go – Kryptera även USB-stickor och externa diskar!

Återställningsnyckel:
Vid aktivering skapas en återställningsnyckel. Den kan sparas i molnet, på ett USB-minne eller skrivas ut. Tappa inte bort den! Utan den är det omöjligt att komma åt datan om något går fel.

Tips till elever:
 BitLocker är enkelt att slå på i Windows Pro. Gå till Kontrollpanelen → BitLocker Drive Encryption. På skolans datorer bör detta dock skötas centralt via IT.

9.4.7 Windows Firewall – skyddet mellan dig och internet

Windows Firewall är en inbyggd brandvägg som styr vilken trafik som får passera in och ut från din dator. Den fungerar som en väktare som säger “ja” eller “nej” till olika typer av anslutningar.

Två huvudtyper av brandväggsregler:

Exempel:

Du vill tillåta att Spotify hämtar musik från internet (utgående)

Du vill inte tillåta att någon fjärransluter till din dator (inkommande)

Lägen i Windows Firewall:

Viktigt: När du kopplar upp dig på ett nytt nätverk får du frågan om du vill klassa det som privat eller offentligt – detta påverkar vilka regler brandväggen använder!

Tips:

Stäng aldrig av brandväggen helt – det är som att lämna dörren olåst.

För avancerade regler, gå till “Windows Defender Firewall med avancerad säkerhet” – där kan du t.ex. tillåta eller blockera specifika portar eller IP-adresser.

Många program lägger automatiskt till undantag i brandväggen – dubbelkolla alltid att du litar på programmet!

9.4.8 Autentisering: Kerberos och NTLM

När du loggar in på en Windows-dator i ett nätverk (särskilt i en domän), används ett autentiseringsprotokoll för att kontrollera att du verkligen är den du säger att du är. Windows använder främst Kerberos eller NTLM.

Vad är NTLM?

NTLM står för NT LAN Manager och är ett äldre autentiseringsprotokoll.

Enkelt att använda

Osäkert idag – bygger på hashbaserade lösenord

Sårbart för "pass-the-hash"-attacker

Vad är Kerberos?

Kerberos är ett modernt och säkrare protokoll, baserat på biljetter som delas ut av en Key Distribution Center (KDC) – vanligtvis din domänkontrollant.

Fördelar:

Krypterad kommunikation

Inga lösenord skickas direkt

Snabbare och säkrare än NTLM

Hur det funkar i korthet:

Du loggar in → KDC bekräftar att du är du

Du får en biljett (TGT – Ticket Granting Ticket)

När du vill nå en tjänst (t.ex. en filserver) använder du biljetten

Tjänsten litar på biljetten utan att be om lösenord igen

NTLM används fortfarande som backup om Kerberos inte fungerar (t.ex. om du inte är med i en domän).

Tips:

I företagssammanhang bör Kerberos alltid användas som standard

NTLM bör avaktiveras i moderna miljöer om det är möjligt

9.4.9 Skydd mot malware och phishing

Malware (skadlig kod) och phishing (nätfiske) är två av de vanligaste hoten mot både privatpersoner och organisationer. De kan stjäla information, låsa datorer, eller till och med ta över hela nätverk.

Vad är malware?

Malware är ett samlingsnamn för olika typer av skadlig programvara:

Vad är phishing?

Phishing handlar om att lura användare att ge ifrån sig känslig information – t.ex. lösenord eller kortuppgifter. Det sker ofta via:

E-post ("Din faktura är sen – klicka här")

Fejkade inloggningssidor (ser ut som t.ex. banken)

Sms ("Verifiera din leverans via länken")

Direktmeddelanden i sociala medier

Skydd mot malware och phishing – vad du kan göra:

Använd ett uppdaterat antivirusprogram (t.ex. Windows Defender)

Aktivera realtidsskydd – programmet varnar direkt om något misstänkt sker

Håll operativsystem och program uppdaterade – många attacker sker via gamla sårbarheter

Använd webbläsartillägg som varnar för misstänkta sajter (t.ex. Microsoft Defender SmartScreen)

Tänk efter innan du klickar – är det rimligt att du får ett mejl från Skatteverket kl. 02:48?

Aktivera e-postfiltrering – de flesta system (t.ex. Microsoft 365) har inbyggt skydd

Tips:

Om ett mejl känns konstigt – dubbelkolla avsändaren

Håll muspekaren över en länk innan du klickar, så ser du vart den leder

Rapportera misstänkt phishing till din IT-avdelning eller Skatteverket om det gäller ekonomiskt bedrägeri

Fakta:
 Microsofts säkerhetsrapporter visar att över 90 % av dagens cyberattacker börjar med phishing!

9.4.10 Group Policy och säkerhetsmallar

I en Windows-domänmiljö (t.ex. i skolor eller företag) används Group Policy (GPO) för att styra inställningar på datorer och användarkonton – centralt, från en domänkontrollant.

Det kan handla om allt från att:

Tvinga användare att ha säkra lösenord

Förhindra åtkomst till vissa inställningar

Automatisk installation av program

Blockera USB-enheter

Sätta skärmsläckare med lösenord

Hur funkar det?

GPO:er appliceras på:

Användare

Datorer

Grupper

OU (Organizational Units)

Dessa regler skickas ut varje gång en användare loggar in, eller en dator startas om.

Säkerhetsmallar (Security Templates)

Windows erbjuder färdiga mallar med rekommenderade säkerhetsinställningar. Dessa kan:

Aktivera UAC

Stänga av gamla protokoll (t.ex. SMBv1)

Begränsa administrativa rättigheter

Ställa in lösenordspolicy

Exempel: "SECUREWS.INF" är en mall för säkra arbetsstationer som kan importeras direkt i Group Policy.

Tips:

Group Policy Editor = gpedit.msc (för lokala inställningar)

För domänstyrda miljöer används Group Policy Management Console (GPMC)

Varför är det viktigt?

Utan centralt styrda policies blir det svårt att ha kontroll på säkerheten. Användare kan stänga av skydd, installera olämpliga program, eller ändra inställningar. Med GPO:er får du ordning och reda.

Exempel från skolmiljö:

Elever kan inte öppna Inställningar

Lärarkonton får administratörsrättigheter

USB-portar är avstängda på elevdatorer

9.4.11Kontrollfrågor – Säkerhet i Windowsmiljö

Vad är syftet med Windows Security Center?

Hur fungerar User Account Control (UAC) och varför är det viktigt?

Vad är skillnaden mellan Microsoft Defender och tredjeparts antivirus?

Vad kan man göra med Group Policy i en domänmiljö?

Vad är NTFS-rättigheter och hur skiljer de sig från delningsrättigheter?

Vad skyddar BitLocker mot – och när är det verkningslöst?

Hur fungerar Windows-brandväggen på applikationsnivå?

Vad är skillnaden mellan Kerberos och NTLM?

Hur skyddar Windows mot phishingförsök och skadlig kod?

Varför är det viktigt att kombinera flera skydd (antivirus, brandvägg, UAC etc.)?

9.4.12 Fördjupningslänkar – Säkerhet i Windowsmiljö

Microsoft – Windows Security Center

Microsoft Learn – UAC Overview

Microsoft Defender Antivirus Documentation

Microsoft – BitLocker Overview

Kerberos vs. NTLM – Microsoft Docs

9.4.13 Egna anteckningar

(Plats för elevens egna reflektioner, minnesregler eller fördjupningar.)

9.5 Säkerhet i Linuxmiljö

Linux används i allt från webbservrar och IoT-enheter till superdatorer och molntjänster. Därför är det avgörande att förstå hur man skyddar dessa system mot attacker. Många attacker mot Linux-system handlar inte om att bryta sig in via lösenord, utan om att utnyttja konfigurationsmissar, öppna portar, gamla versioner eller brist på loggning.

Viktigt! Denna del kommer i första hand utgå från Debian-baserade system såsom Ubuntu m.m. så vissa av kommandona kommer inte att stämma mot andra distributioner.

9.5.1 Grundläggande säkerhetsprinciper

När man arbetar med Linux, särskilt i serversammanhang, är det viktigt att inte bara tänka på vad systemet kan göra – utan också hur man minimerar riskerna. Det finns ett antal principer som utgör grunden för hur vi tänker kring säkerhet i Linuxmiljöer.

Minsta möjliga behörighet (Least Privilege)

Detta är kanske den allra viktigaste principen inom IT-säkerhet – och i Linux är det inbyggt i systemets design. Alla kommandon behöver inte köras som root. Tvärtom: ju färre kommandon som körs med hög behörighet, desto mindre risk att en attack lyckas.

Exempel:
 Om du installerar ett paket som vanlig användare, händer inget. Det kräver sudo. Detta är ett medvetet hinder – och ett skydd.

Tips:
Skapa hellre specifika användare för olika uppgifter än att ge root-access till allt. En webbtjänst ska t.ex. inte kunna skriva till /etc eller läsa andras hemkataloger.

Defense in Depth – Flera lager av skydd

En brandvägg är bra. Men det räcker inte. Vad händer om någon lyckas ta sig förbi den? Då vill du ha en logg som visar vad som hände. Kanske ett IDS-system som larmar. Och kryptering som förhindrar åtkomst till känslig information.

Tänk på det som en lök – säkerheten byggs i lager.

Minska attackytan

Ju mer som körs, desto mer kan gå fel. Linux-servrar installeras ofta med så lite som möjligt – just för att minska risken.

Exempel på onödiga risker:

Öppna portar för tjänster du inte använder (ex: FTP, Telnet)

Användarkonton som inte används längre

Programvara som inte uppdateras

Tips:
Kör ss -tuln för att se vilka portar som är öppna. Avinstallera tjänster du inte behöver. Inaktivera oanvända användare och konton.

Standardinställningar är inte alltid säkra

Linux är kraftfullt – men ibland lämnas konfigurationen i ett osäkert tillstånd efter installation. Exempel:

SSH tillåter root-login

Loggar roteras inte

Systemd-tjänster kör med onödiga rättigheter

Att härda systemet är en viktig del av driften – inte ett engångsjobb.

Säkerhet är en process – inte en produkt

Det går inte att installera ett "säkerhetsprogram" och sen luta sig tillbaka. Säkerheten måste underhållas:

Patcha regelbundet

Följa med i CVE-flöden

Testa din miljö då och då

9.5.2 Kontrollfrågor

Vad innebär principen "minsta möjliga behörighet"?

Varför är det viktigt att undvika att köra kommandon som root i onödan?

Vad menas med "defense in depth"?

Ge tre exempel på olika säkerhetslager du kan använda på en Linux-server.

Vad är en "attackyta" i ett operativsystem?

Varför är det en dålig idé att ha onödiga tjänster igång?

Vad kan kommandot ss -tuln användas till?

Varför kan standardinställningar vara osäkra?

Vad är risken med att tillåta SSH-login som root?

Varför är säkerhet en process, inte en engångsåtgärd?

9.5.3 Fördjupningslänkar

NIST – Least Privilege

RedHat – Security Best Practices

Ubuntu Hardening Wiki

Linux Foundation – Defense in Depth

CIS Benchmarks – General Linux Guidance

9.5.4 Egna anteckningar

(Lämna plats för egna reflektioner och fördjupningar här.)

9.6 OS-härdning (Operating System Hardening)

Att ”härda” ett operativsystem betyder att minska dess sårbarheter genom att ta bort onödiga tjänster, stänga oanvända portar, aktivera säkerhetsfunktioner och kontrollera åtkomst. I Linuxmiljö handlar det om att ställa in systemet så säkert som möjligt, utan att påverka dess funktion.

Grundregeln: Ju färre funktioner som är aktiva – desto mindre finns att attackera.

CIS Benchmarks – säkerhetsstandard att följa

Center for Internet Security (CIS) publicerar detaljerade guider för hur man säkrar olika operativsystem, inklusive Ubuntu, Debian och andra Linux-distributioner.

CIS-benchmarks innehåller:

Rekommenderade inställningar för användarkonton, loggning, nätverkstjänster

Tips på filbehörigheter, bootloader-skydd, m.m.

Kommandon för att kontrollera och verifiera säkerhetsnivån

Exempel på verktyg:

lynis – säkerhetsscanner som kan jämföra ditt system mot t.ex. CIS

cis-cat – ett Java-baserat verktyg från CIS som kontrollerar compliance

AppArmor & SELinux – kontrollera vad processer får göra

AppArmor (Ubuntu, Debian) och SELinux (Red Hat, Fedora, CentOS) är så kallade Mandatory Access Control (MAC)-system. De fungerar som extraskydd ovanpå vanliga filrättigheter (typ chmod).

AppArmor:

Lättare att förstå och administrera

Har profiler för vanliga program (ex. apache2, mysql, ping)

Status kollas med sudo aa-status

SELinux:

Mer avancerat men svårare att felsöka

Används ofta i enterprisemiljöer

Status: sestatus

Tips: Håll dig till AppArmor i Ubuntu-miljöer om du är nybörjare – det är tillräckligt kraftfullt men mer pedagogiskt.

Secure Boot – skydda redan vid uppstart

Secure Boot är ett UEFI-baserat säkerhetsläge som gör att datorn endast startar operativsystem och program som är signerade. Det hindrar t.ex. att angripare lägger in en rootkit i bootkedjan.

I Linux:

Måste vara aktiverat i BIOS/UEFI

Kräver ofta att kärnmoduler är signerade (t.ex. vid custom-kärnor eller externa drivrutiner)

Kryptera diskar och partitioner

Fysisk säkerhet är inte alltid nog – särskilt inte för bärbara enheter. Kryptering ser till att data inte kan läsas utan rätt nyckel, även om hårddisken plockas ur datorn.

Alternativ:

LUKS – (Linux Unified Key Setup), standard i t.ex. Ubuntu

Aktiveras ofta under installation (”Kryptera hela disken”)

Verktyg: cryptsetup

eCryptfs – tidigare populärt för att kryptera hemmakataloger

ZFS native encryption – för avancerade användare

Tips: Använd alltid fullständig diskkryptering på bärbara datorer. För stationära system kan det räcka att kryptera specifika kataloger (t.ex. /home, /var).

Partitionering som säkerhetsåtgärd

Att dela upp disken i flera partitioner gör att ett fel (t.ex. loggar som växer) inte tar ner hela systemet. Det kan också minska skadan vid ett intrång.

Rekommenderade separata partitioner:

/home – användardata

/var – loggar och dynamiskt innehåll

/tmp – tillfälliga filer

/boot – ibland, om du behöver separera uppstartsdata

Mount-alternativ:

noexec – inga körbara filer tillåtna (bra för /tmp)

nosuid – förhindrar setuid-program

nodev – inga enhetsfiler tillåtna

Tipsruta:

Vill du snabbt se vilka mount-alternativ som används?
 Kör: mount | grep "^/" eller findmnt

9.6.1 Kontrollfrågor

Vad menas med att "härda" ett operativsystem?

Vad är CIS Benchmarks och varför är de användbara?

Vad är skillnaden mellan AppArmor och SELinux?

Vad gör Secure Boot, och varför är det viktigt?

Vad är LUKS och när används det?

Vad är fördelen med att ha flera partitioner i Linux?

Vad betyder mount-alternativen noexec, nosuid och nodev?

Vad är skillnaden mellan fysisk säkerhet och systemhärdning?

Vilka Linux-kommandon kan användas för att kontrollera AppArmor-status?

Varför bör /tmp monteras med begränsningar?

9.6.2 Fördjupningslänkar

CIS Benchmarks –

AppArmor Guide (Ubuntu) –

SELinux Project –

Ubuntu LUKS Encryption –

Red Hat – Linux Partitioning and Mount Options –

9.6.3 Egna anteckningar

(Här kan du som elev skriva ned viktiga reflektioner, kommandon du vill minnas, eller egna exempel på säkerhetsåtgärder du använder i dina system.)

9.7 Paketuppdatering och patchhantering

Att hålla systemet uppdaterat är en av de viktigaste säkerhetsåtgärderna i Linux – och ändå är det något som ofta förbises. Ett opatchat system är som att lämna dörren på glänt – oavsett hur bra låset är.

De flesta sårbarheter som utnyttjas av angripare är redan kända – men systemen de angriper är inte uppdaterade. Det är alltså inte hacker-magi som krävs – bara en ignorans från administratören.

Varför är patchar så viktiga?

Patchar åtgärdar bland annat:

Kända säkerhetshål

Buggar som kan utnyttjas för att eskalera behörigheter

Kompatibilitetsproblem

Nya hot (t.ex. zero-day exploits som snabbt måste åtgärdas)

I ett större nätverk kan en sårbar server bli en inkörsport för angripare. Genom att hålla systemet uppdaterat stänger man dessa portar innan de utnyttjas.

Verktyg i Debian-baserade system

I Debian och Ubuntu använder man främst följande kommandon för uppdatering:

Man kan även använda apt-get, men apt är numera standard för interaktivt bruk.

Automatisk uppdatering med unattended-upgrades

På servrar där man inte loggar in så ofta kan det vara bra att automatisera vissa uppdateringar.

Installation:

sudo apt install unattended-upgrades

Aktivera:

sudo dpkg-reconfigure --priority=low unattended-upgrades

Detta aktiverar automatiska säkerhetsuppdateringar. Vill du justera vilka paket som uppdateras eller få loggar, kan du redigera:

/etc/apt/apt.conf.d/50unattended-upgrades

Det går också att sätta upp notifiering via mail eller loggfiler om något uppdateras automatiskt.

Tips för patchhantering

Kör apt update && apt upgrade minst en gång i veckan om du inte har automatisk hantering.

Kontrollera /var/log/apt/history.log för att se vad som installerats.

Följ med i säkerhetsflöden för din distribution – Ubuntu har ett eget säkerhetsflöde på

Undvik att köra uppdateringar utan att läsa vad som uppdateras – speciellt på produktionsservrar.

Tänk på att vissa uppdateringar kräver omstart (ex. kernel).

9.7.1 Kontrollfrågor

Vad är syftet med en patch?

Vad är skillnaden mellan apt update och apt upgrade?

Vilket kommando visar vilka paket som har uppdateringar tillgängliga?

Vad innebär apt full-upgrade?

Varför är det farligt att inte uppdatera ett Linux-system?

Vad är unattended-upgrades och vad används det till?

Hur installerar man unattended-upgrades?

Var hittar du loggar över vad som uppdaterats på ett system?

Varför bör man vara försiktig med uppdateringar på en produktionsserver?

Hur ofta bör du uppdatera systemet om du inte har aktiverat automatisk uppdatering?

9.7.2 Fördjupningslänkar

Ubuntu Security Notices

Debian Security Information

Ubuntu Wiki – Unattended Upgrades

APT Command Reference (Debian Wiki)

Linux Handbook – How to Update Ubuntu

9.7.3 Egna anteckningar

(Lämna plats för egna reflektioner och anteckningar här.)

9.8 Systemövervakning och loggning (journald, rsyslog, AIDE)

Att övervaka och logga vad som händer på ett Linux-system är avgörande för att kunna upptäcka intrångsförsök, spåra fel eller följa upp vad som gjorts. Loggar är som systemets minne – de berättar vem som gjorde vad, när och hur. Utan loggar blir felsökning och säkerhetsanalys i stort sett omöjlig.

Journald – systemd:s loggsystem

De flesta moderna Linux-distributioner använder systemd som init-system. Tillsammans med journald hanterar det systemets kärnloggar, tjänstmeddelanden och andra systemrelaterade loggar.

Exempel på kommandon:

journalctl           # Visa alla loggar
journalctl -b        # Visa loggar från senaste boot
journalctl -u ssh    # Visa loggar för SSH-tjänsten
journalctl --since "1 hour ago"  # Visa loggar från senaste timmen

Tips: Använd less för att bläddra, eller grep för att filtrera specifika meddelanden.

journald lagrar loggar binärt, vilket gör dem svårare att manipulera än vanliga textloggar – men du kan också exportera till text om du vill.

rsyslog – klassisk textbaserad logghantering

Utöver journald används ofta rsyslog för att skicka loggar till olika filer, vanligtvis under /var/log. Det här systemet är fortfarande vanligt och kan också användas för att:

Centralisera loggar från flera servrar

Skicka loggar till externa logghanteringsverktyg

Definiera egna regler för vad som loggas och hur

Vanliga loggfiler:

/var/log/auth.log – inloggningar, sudo-användning

/var/log/syslog – allmän systemlogg

/var/log/kern.log – kernel-meddelanden

/var/log/apt/history.log – paketinstallationer

/var/log/faillog – misslyckade inloggningar

Konfigurationen sker via /etc/rsyslog.conf och eventuella filer i /etc/rsyslog.d/.

AIDE – Advanced Intrusion Detection Environment

AIDE är ett kraftfullt verktyg för filintegritetskontroll – alltså att hålla koll på om något på filsystemet ändras, till exempel:

Om ett systembinär modifieras

Om en konfigurationsfil skrivs om

Om någon lagt till en fil i /bin eller /etc

Det fungerar som ett "före-efter"-system. Först skapar man en databas över hur systemet ska se ut. Sen jämför man regelbundet systemets aktuella tillstånd med denna databas.

Exempel:

sudo aideinit               # Initiera databas
sudo aide.wrapper --check   # Kontrollera om något förändrats

Det är viktigt att den ursprungliga databasen sparas på ett säkert ställe – annars kan en angripare även manipulera den.

Tips: Schemalägg AIDE via cron eller systemd timers, så att kontroller sker automatiskt varje dag.

Varför är detta viktigt?

Loggar ger spårbarhet – vem gjorde vad, när?

Loggar används vid incidentutredningar.

Ett förändrat system (utan din vetskap) är ett starkt tecken på intrång.

Automatiserad övervakning sparar tid och ökar säkerheten.

9.8.1 Kontrollfrågor

Vad är journald och vilken typ av loggar hanterar det?

Vad gör kommandot journalctl -u ssh?

Nämn två skillnader mellan journald och rsyslog.

Var sparas vanligen klassiska loggfiler i Linux?

Vad används /var/log/auth.log till?

Vad är AIDE och vilket säkerhetssyfte fyller det?

Vad händer vid ett AIDE-check om en systemfil har ändrats?

Varför är det viktigt att spara AIDEs databas på ett säkert ställe?

Hur kan AIDE automatiseras för daglig kontroll?

Hur kan loggar användas vid säkerhetsincidenter?

9.8.2 Fördjupningslänkar

Red Hat – Introduction to journalctl

Ubuntu – Log Files Explained

rsyslog – Officiell dokumentation

AIDE Project

Loggning i Linux – Comparitech

9.8.3 Egna anteckningar

(Lämna plats för egna reflektioner och kompletterande information här.)

9.9 Root, sudo och användarbehörighet

I Linux är säkerheten starkt knuten till användarbehörigheter. Den mest kraftfulla användaren är root, som har obegränsad tillgång till hela systemet. Att förstå hur root, sudo, och användarbehörigheter fungerar är en grundpelare i att säkra ett Linuxsystem.

Root – superanvändaren

Root-användaren är den administrativa användaren i Linux. Den har full tillgång till alla filer, processer och kommandon. Inloggning som root är sällan en bra idé, eftersom:

Alla kommandon körs utan begränsningar – ett misstag kan bli katastrofalt.

Root-inloggning loggas ofta inte separat, vilket försvårar spårning.

Om en angripare får root-access är systemet helt komprometterat.

Därför är det bättre att använda sudo – ett verktyg som tillfälligt ger administrativ behörighet till vanliga användare.

sudo – tillfällig superkraft

Med sudo kan en vanlig användare köra specifika kommandon med root-rättigheter. Exempel:

sudo apt update

Första gången (eller efter ett tag) krävs lösenord, vilket loggas i systemet. Detta gör det möjligt att:

Säkerställa vem som körde vad

Minimera risken för misstag

Begränsa rättigheter till specifika kommandon

Konfigurationen av sudo sker i /etc/sudoers, och bör alltid redigeras med visudo för att undvika syntaxfel:

sudo visudo

Där kan man t.ex. sätta att en användare endast får köra vissa kommandon som root:

student ALL=(ALL) NOPASSWD: /usr/sbin/service apache2 restart

Användar- och grupphantering

Varje användare i Linux har ett UID (User ID), och varje grupp har ett GID (Group ID). Fil- och katalogbehörigheter baseras på tre kategorier:

Exempel från ls -l:

-rwxr-xr-- 1 robin admin  4200 jul 18 10:00 script.sh

Här betyder det:

rwx = ägaren (robin) får läsa, skriva och köra

r-x = gruppen (admin) får läsa och köra

r-- = andra får bara läsa

Byta ägare och rättigheter

chown – byt ägare:

sudo chown robin:admin fil.txt

chmod – ändra rättigheter (t.ex. 755):

chmod 755 script.sh

usermod – lägg till användare i grupp:

sudo usermod -aG sudo student

Sudoers-fällor att undvika

Låt inte alla användare få full sudo-access utan eftertanke.

Använd NOPASSWD endast om det är absolut nödvändigt.

Håll reda på vem som kan köra vad via loggar (/var/log/auth.log).

Tips: Ett vanligt säkerhetsråd är att inte logga in som root, utan alltid använda sudo. På många system (som Ubuntu) är root-användaren t.o.m. avaktiverad som standard.

9.9.1 Kontrollfrågor

Vad är root-användarens roll i Linux?

Varför bör man undvika att arbeta direkt som root?

Vad gör kommandot sudo, och varför används det istället för root-inloggning?

Vad gör visudo, och varför bör man använda det istället för att direkt redigera /etc/sudoers?

Vad innebär rättigheterna r, w och x för filer och kataloger?

Vad gör kommandot chown, och vad betyder syntaxen robin:admin?

Vad är skillnaden mellan chmod 755 och chmod 700?

Hur lägger man till en användare i en grupp, t.ex. sudo-gruppen?

Vad är syftet med att begränsa vilka kommandon en användare får köra med sudo?

Var kan man hitta loggar över användning av sudo?

9.9.2 Fördjupningslänkar

Ubuntu – Users and Groups:

DigitalOcean – How To Use Sudo on Ubuntu:

Linuxize – Linux File Permissions Explained:

Red Hat – Introduction to the sudo Command:

Ubuntu Manpages – visudo:

9.9.3 Egna anteckningar

(Lämna plats för egna reflektioner, exempel och kommandon)

9.10 Loggning och övervakning i Linux

Loggning är en av de viktigaste delarna i ett säkert Linux-system. Utan loggar vet du inte vad som har hänt – eller vad som händer just nu. Loggar kan visa allt från inloggningsförsök till programkrascher, ändrade filer, tjänstestarter, nätverksproblem och attacker. Övervakning handlar om att i realtid hålla koll på systemets hälsa, resursförbrukning och potentiella hot.

Viktiga loggsystem

journald (systemd journal)

De flesta moderna Linux-system (inklusive Ubuntu) använder systemd som init-system, vilket inkluderar journald som loggtjänst.

Visar loggar med: journalctl

Exempel: journalctl -xe för senaste händelser med extra info

Loggar i binärt format – inte direkt läsbara med cat

rsyslog (traditionellt loggsystem)

Klassiskt loggsystem som skriver till textfiler i /var/log/, t.ex.:

/var/log/auth.log – inloggningar, sudo

/var/log/syslog – systemmeddelanden

/var/log/kern.log – kärnloggar

/var/log/dmesg – hårdvarumeddelanden från boot

De flesta Ubuntu-system använder både rsyslog och journald.

Övervakningsverktyg

top / htop

Visar realtidsinformation om CPU-, RAM- och processanvändning.

top – inbyggt, konsolbaserat

htop – mer visuellt och användarvänligt (kan installeras med sudo apt install htop)

uptime och load average

Visar systemets drifttid och belastning:

uptime

vmstat, iostat, netstat (för mer avancerad analys)

Ger information om minnesanvändning, I/O och nätverkstrafik.

fail2ban – skydd mot brute-force

Övervakar loggar (t.ex. /var/log/auth.log) och blockerar IP-adresser som misslyckas med inloggningar upprepade gånger.

Installera med:

sudo apt install fail2ban

AIDE – Advanced Intrusion Detection Environment

Skapar en databas över filsystemets tillstånd (storlek, rättigheter, innehåll) och kan sedan jämföra om något har ändrats (t.ex. attacker som ändrar konfigfiler eller skadlig kod som lägger till bakdörrar).

Installera:

sudo apt install aide

Initiera databas:

sudo aideinit

Verifiera ändringar:

sudo aide --check

Tips: Loggning är inte bara för forensik. Bra loggar = snabbare felsökning och upptäckt av problem innan de blir allvarliga.

9.10.1 Kontrollfrågor

Vad är syftet med loggning i ett Linux-system?

Vilken kommandorad används för att visa systemd-journalen?

Vad är skillnaden mellan rsyslog och journald?

Nämn tre vanliga loggfiler i /var/log/.

Vad gör top respektive htop?

Hur kan du kontrollera hur länge ett system har varit igång?

Vad är fail2ban, och hur fungerar det?

Vad är AIDE och hur används det?

Hur kontrollerar man om AIDE har upptäckt några ändringar?

Varför är övervakning viktig även i system som fungerar "som de ska"?

9.10.2 Fördjupningslänkar

Ubuntu – Log Files Explained

journalctl manpage

DigitalOcean – Fail2Ban Tutorial

AIDE – Officiell webbplats

Ubuntu – Monitor System Performance

9.10.3 Egna anteckningar

(Här kan du skriva ner egna exempel, kommandon du testat eller viktiga lärdomar om loggning och övervakning.)

9.11 Härdning av tjänster (t.ex. SSH, brandvägg, TLS/SSL)

Härdning innebär att minska attackytan för ett system genom att stänga av onödiga funktioner, säkra konfigurationer och begränsa åtkomst. Målet är att göra det så svårt som möjligt för en angripare att ta sig in – och så lätt som möjligt att upptäcka försök.

Här tittar vi närmare på några vanliga tjänster och hur du säkrar dem.

SSH – Secure Shell

SSH används för att fjärransluta till Linux-system. Det är kraftfullt, men också ett vanligt mål för attacker.

Rekommenderade inställningar:

Byt standardport från 22 till något annat (för att undvika skriptade attacker)

sudo nano /etc/ssh/sshd_config
# Port 2222 (t.ex.)

Stäng av inloggning för root:

PermitRootLogin no

Aktivera endast inloggning med SSH-nycklar:

PasswordAuthentication no

Begränsa inloggning till specifika användare:

AllowUsers robin adminuser

Efter ändring:

sudo systemctl restart ssh

Tips: Använd fail2ban för att blockera upprepade felaktiga inloggningsförsök via SSH.

Brandvägg – ufw (Uncomplicated Firewall)

En brandvägg begränsar nätverkstrafik in och ut från systemet. ufw är ett enkelt gränssnitt till iptables.

Kom igång:

sudo apt install ufw
sudo ufw enable

Vanliga kommandon:

Tillåt SSH (t.ex. port 22):

sudo ufw allow 22/tcp

Blockera all inkommande trafik som inte är tillåten:

sudo ufw default deny incoming
sudo ufw default allow outgoing

Visa status:

sudo ufw status verbose

Tips: Lägg till regler FÖRE du aktiverar brandväggen, annars kan du låsa ute dig själv från SSH.

TLS/SSL – Krypterad kommunikation

TLS/SSL används för att kryptera webbtrafik (https), e-post (smtps/imaps) m.m. Att använda korrekt konfigurerade certifikat är avgörande.

Gratiscertifikat med Let's Encrypt:

sudo apt install certbot python3-certbot-apache
sudo certbot --apache

För Nginx, byt --apache mot --nginx.

Fördelar med TLS/SSL:

Skyddar data från att avlyssnas

Möjliggör identitetsverifiering via certifikat

Ger tillgång till HTTPS (vilket är ett krav för moderna webbläsare)

Tänk på:

Ställ in automatisk förnyelse:

sudo systemctl status certbot.timer

9.11.1 Kontrollfrågor

Vad innebär det att "härda" ett system?

Varför är det bra att byta port för SSH från 22?

Vad gör inställningen PermitRootLogin no?

Hur fungerar SSH-nycklar som autentisering?

Vad är ufw, och vad används det till?

Hur ser du vilka regler som är aktiva i ufw?

Vad innebär ufw default deny incoming?

Vad är TLS/SSL och vad används det till?

Hur skaffar man ett gratis SSL-certifikat i Ubuntu?

Varför är det viktigt att förnya TLS-certifikat?

9.11.2 Fördjupningslänkar

SSH Hardening Guide (Ubuntu)

UFW Firewall Tutorial

Let's Encrypt (gratis TLS-certifikat)

Mozilla SSL Configuration Generator

OWASP – TLS Best Practices

9.11.3 Egna anteckningar

(Här kan du skriva ner egna exempel på härdning du testat, vilka regler du satt upp i ufw, eller inställningar du gjort i sshd_config.)

9.12 Backup och återställning

Att göra regelbundna säkerhetskopior (backuper) är en av de viktigaste säkerhetsåtgärderna du kan ta – men också en av de mest bortglömda. I Linux är det extra viktigt eftersom många servrar är kritiska för verksamheten och inte har något grafiskt gränssnitt som påminner om att "säkerhetskopiera nu".

Backup handlar inte bara om att skydda sig mot hårddiskkrascher – utan även mot ransomware, oavsiktlig radering, konfigurationsfel och attacker.

Typer av backup

Verktyg i Linux

Här är några vanliga verktyg för backup i Linux:

rsync – Kopierar filer och kataloger effektivt (lokalt eller över nätverk)

tar – Används för att skapa arkivfiler (.tar/.gz)

cron – Schemalägger backupjobb

Deja Dup – Enkel GUI-lösning för Ubuntu Desktop

Bacula / Duplicity / BorgBackup – Mer avancerade backup-lösningar

Exempel på enkel backup med rsync

Säkerhetskopiera en hemkatalog till en extern disk:

rsync -avh --delete /home/robin /media/backupdisk/

Beskrivning:

-a: Arkivläge (bevarar rättigheter, ägarskap)

-v: Verbos (visa vad som görs)

-h: Mänskligt läsbart format

--delete: Tar bort filer på backupmål som inte längre finns på källan (för att spegla exakt)

Schemalägga backup med cron

Redigera crontab:

crontab -e

Lägg till en rad för att köra backup varje natt kl 03:00:

0 3 * * * rsync -avh /home/robin /media/backupdisk/

Återställning – vad gör du när det smäller?

En backup är bara användbar om du vet hur du återställer den. Testa därför återställning regelbundet!

Återställningsexempel:

rsync -avh /media/backupdisk/robin /home/

Tips: Dokumentera alltid var backuper sparas, hur de återställs och vem som ansvarar för dem.

Offsite & molnbackup

Om backuper endast sparas lokalt riskerar de att förstöras i brand, stöld eller översvämning.

Lösning:

Synka till en annan fysisk plats

Använd molnlagring (ex. rclone med Google Drive, S3, etc.)

Kryptera känslig data innan molnuppladdning

Vanliga misstag

Backupen sparas på samma disk som originalet

Backupen körs – men återställning testas aldrig

Backupen innehåller bara data – men inte konfiguration

Backupskriptet loggar inte något

Bästa praxis: Full backup + inkrementell + offsite + återställningstest

9.12.1 Kontrollfrågor

Vad är skillnaden mellan full och inkrementell backup?

Vilket verktyg i Linux används för effektiv filsynkronisering?

Hur används cron för backup?

Vad gör flaggan --delete i rsync?

Varför är det viktigt att även göra backup på konfigurationsfiler?

Vad innebär offsite-backup?

Vad är risken med att bara ha backup lokalt?

Varför är återställningstester viktiga?

Ge ett exempel på en molnlösning som kan användas med rclone.

Vad kan gå fel om du inte loggar dina backupjobb?

9.12.2 Fördjupningslänkar

Ubuntu rsync guide

Linux tar command guide

Cron syntax explained

BorgBackup (säkert och komprimerat backupverktyg)

Rclone (synka till molnet)

9.12.3 Egna anteckningar

(Här kan du skriva hur du konfigurerat dina egna backupscript, vilka kataloger du prioriterar, eller testa att återskapa ett gammalt tar-arkiv.)

9.13 Automatisering av säkerhetsuppgifter (cron, script, loggning)

Att automatisera återkommande uppgifter i Linux är en av de största fördelarna med systemet – och det gäller särskilt när det handlar om säkerhet. Genom att schemalägga uppgifter som uppdateringar, loggrensning, säkerhetskopiering eller övervakning kan du minimera risken för den mänskliga faktorn och säkerställa att skyddet är aktivt dygnet runt.

cron – Linux inbyggda schemaläggare

cron används för att köra kommandon vid återkommande tidpunkter.

Struktur i crontab:

* * * * * kommando
│ │ │ │ │
│ │ │ │ └─ dag i veckan (0-6, söndag=0)
│ │ │ └─── månad (1-12)
│ │ └───── dag i månaden (1-31)
│ └─────── timme (0-23)
└───────── minut (0-59)

Exempel:
 Kör ett script varje natt kl 02:00:

0 2 * * * /home/admin/scripts/update-check.sh

Tips: Använd crontab -e för att redigera användarens schema.

Bash-script – Automatisering i praktiken

Script låter dig skapa anpassade säkerhetsrutiner.

Exempel: Automatiserat uppdateringsscript

#!/bin/bash
echo "Uppdatering startade: $(date)" >> /var/log/uppdatering.log
apt update && apt upgrade -y >> /var/log/uppdatering.log 2>&1
echo "Färdigt: $(date)" >> /var/log/uppdatering.log

Spara som /home/admin/scripts/update-check.sh och gör körbar:

chmod +x update-check.sh

Lägg till i cron:
 0 3 * * * /home/admin/scripts/update-check.sh

Loggning – Sätt att hålla koll på vad som händer

I Linux loggas det mesta, särskilt sådant som rör systemet och säkerhet.

Viktiga loggfiler:

/var/log/auth.log – inloggningar och sudo-kommandon

/var/log/syslog – generell systemlogg

/var/log/ufw.log – brandväggsloggar (om UFW används)

/var/log/apt/history.log – installationshistorik

Visa senaste 20 rader i auth.log:

tail -n 20 /var/log/auth.log

Övervaka logg i realtid:

tail -f /var/log/syslog

Automatiserad övervakning (med t.ex. fail2ban)

fail2ban är ett verktyg som automatiskt blockerar IP-adresser som upprepat försöker logga in felaktigt – t.ex. via SSH.

Installation:

sudo apt install fail2ban

Starta och aktivera:

sudo systemctl enable --now fail2ban

Logg:

sudo cat /var/log/fail2ban.log

fail2ban använder loggfiler som auth.log för att identifiera attacker.

Rekommenderade säkerhetsrutiner att automatisera

9.13.1 Kontrollfrågor

Vad är cron och vad används det till?

Vad betyder 0 3 * * * i crontab?

Hur gör man ett script körbart?

Vad gör kommandot tail -f /var/log/syslog?

Varför är loggning viktigt för säkerheten?

Vad gör fail2ban?

Var loggas SSH-inloggningar?

Vad är skillnaden mellan apt update och apt upgrade?

Varför är det bra att automatisera säkerhetsuppgifter?

Nämn tre säkerhetsuppgifter du kan schemalägga med cron.

9.13.2 Fördjupningslänkar

Cron syntax och guide

Linux Bash Scripting Tutorial

Fail2ban – officiell dokumentation

Ubuntu Log files explained

Automatiserad säkerhet i Linux

9.13.3 Egna anteckningar

(Här kan du skriva vilka säkerhetsuppgifter du har automatiserat, lägga in utdrag från din egen crontab, eller testa att skapa ett eget säkerhetsscript.)

9.14 Säkerhetsverktyg i Linux

Att skydda ett Linuxsystem kräver mer än bara bra konfigurationer – det kräver också rätt verktyg. I denna del samlar vi några av de mest använda säkerhetsverktygen i Linuxvärlden. Vissa har vi redan introducerat tidigare, men här får de en gemensam överblick tillsammans med nya alternativ som kompletterar bilden.

Översikt: Verktyg för olika ändamål

Exempel på verktyg

1. fail2ban – Skydd mot bruteforce

Bevakar loggar (t.ex. SSH) och blockerar IP-adresser med för många inloggningsförsök.
 Redan konfigurerat i många Debian-baserade system med /etc/fail2ban/jail.conf.

sudo apt install fail2ban
sudo systemctl enable --now fail2ban

2. ufw – Enkel brandväggshantering

Wrapper för iptables/nftables. Bra för mindre miljöer eller snabb konfigurering.

sudo apt install ufw
sudo ufw enable
sudo ufw allow ssh

3. chkrootkit och rkhunter – Rootkitsökning

Söker efter tecken på att systemet har blivit komprometterat. De har olika signaturbaser så de kompletterar varandra.

sudo apt install chkrootkit rkhunter
sudo chkrootkit
sudo rkhunter --check

4. Lynis – Sårbarhetsanalys

Gör en säkerhetsgenomgång och listar potentiella risker i ett rapportformat.

sudo apt install lynis
sudo lynis audit system

Lynis används ofta som en del av hårdvaru- och säkerhetsrevisioner.

5. ClamAV – Antivirusscanner för Linux

Bra för att analysera exempelvis e-postservrar eller användarkataloger. Inte realtid, men kan schemaläggas.

sudo apt install clamav
sudo freshclam  # uppdatera virussignaturer
sudo clamscan -r /home

6. AIDE – Övervakning av filsystemets integritet

Jämför aktuella filer mot en sparad databas för att upptäcka oväntade förändringar.

sudo apt install aide
sudo aideinit
sudo cp /var/lib/aide/aide.db.new /var/lib/aide/aide.db
sudo aide --check

7. auditd – Systemgranskning på kernel-nivå

Skapar detaljerade loggar över användaraktiviteter, ändringar i filer och program som körs.

sudo apt install auditd
sudo systemctl start auditd

Loggar sparas i /var/log/audit/.

9.14.1 Kontrollfrågor

Vad gör fail2ban och vilket typ av angrepp skyddar det mot?

Hur skiljer sig chkrootkit från rkhunter?

Vad är syftet med Lynis och hur används det?

Vilket verktyg använder du för att kontrollera integriteten hos filer i ett Linuxsystem?

Hur fungerar ClamAV och vad är det bra på?

Vad är skillnaden mellan realtidsskydd och schemalagda skanningar?

Vad är auditd och vad loggar det?

Varför kan det vara bra att använda både chkrootkit och rkhunter?

När är det lämpligt att använda AIDE eller Tripwire?

Hur kan dessa verktyg kombineras för att ge ett heltäckande skydd?

9.14.2 Fördjupningslänkar

CIS – "Linux Security Best Practices":

Debian Wiki – Hardening and Security Tools:

ClamAV – Official Documentation:

RKHunter – Rootkit Hunter Project:

Lynis GitHub Repository:

9.14.3 Egna anteckningar

(Lämna utrymme för reflektioner, kommandon du vill testa eller egna tips.)

9.15 IT-säkerhet ur ett verksamhetsperspektiv

9.15.1 Säkerhetspolicy och rutiner

IT-säkerhet handlar inte bara om brandväggar, lösenord och antivirusprogram. För att säkerheten verkligen ska fungera i en organisation krävs tydliga riktlinjer, regler och ansvar. Här kommer säkerhetspolicyn in – ett dokument som fungerar som ett ramverk för hur en verksamhet hanterar sina resurser och skyddar sin information.

En säkerhetspolicy är ofta ett övergripande dokument som beskriver hur organisationen ser på säkerhet, vilka mål som finns, och vilka krav som ställs på medarbetare, system och processer. Den fungerar lite som ett säkerhetskontrakt: så här jobbar vi, det här förväntar vi oss av dig, och det här händer om något går fel.

Till policyn kopplas ofta rutiner, instruktioner och riktlinjer. Dessa går mer på detaljnivå och svarar på frågor som:

Hur ofta ska vi ta backup?

Hur skapar vi nya användare?

Vad händer om någon tappar bort sin dator?

En vanlig missuppfattning är att det räcker att ha en policy – men det är först när policyn är känd, förstådd och efterlevd som den gör nytta. En policy som ligger i en mapp någonstans på intranätet och aldrig uppdateras är i praktiken värdelös.

Exempel på vanliga policytyper:

Lösenordspolicy – regler för längd, komplexitet, giltighetstid

Användarpolicy – vad får du göra (och inte göra) med din jobbmail eller jobbdator?

Backup-policy – hur ofta tas backup, var lagras den, vem ansvarar?

Mobilpolicy – hur hanteras bärbara enheter och BYOD (Bring Your Own Device)?

En viktig poäng är att policyn måste anpassas till verksamheten. Ett stort företag med många system och roller behöver andra regler än en mindre förening. Det finns ingen universallösning – säkerhetspolicyn måste spegla organisationens behov, risknivå och tekniska miljö.

Slutligen bör varje säkerhetspolicy följas upp: är den fortfarande relevant? Följs den? Och vad kan förbättras? En bra policy är ett levande dokument, inte ett dammigt Word-dokument från 2013.

9.15.1.1 Kontrollfrågor

Vad är syftet med en säkerhetspolicy?

Vad är skillnaden mellan en policy, en rutin och en instruktion?

Varför räcker det inte att bara ha en policy?

Vad innebär det att en policy måste vara känd och efterlevd?

Nämn tre exempel på vanliga typer av IT-säkerhetspolicys.

Vad är en lösenordspolicy till för?

Vad är en backup-policy och varför är den viktig?

Vad menas med BYOD och hur påverkar det säkerhetspolicyn?

Varför är det viktigt att anpassa säkerhetspolicyn till verksamheten?

Hur bör en organisation följa upp och förbättra sin säkerhetspolicy?

9.15.1.2 Fördjupningslänkar

MSB – Säkerhetspolicy – grunder och exempel

DIGG – Informationssäkerhet för offentlig sektor

PTS – Informationssäkerhet och policyarbete

NIST – Security Policies and Implementation Issues (eng)

SANS Institute – Creating a Security Policy (eng)

9.15.1.3 Egna anteckningar

(Här kan du anteckna egna reflektioner, exempel eller frågor kring säkerhetspolicys och rutiner.)

9.15.2 Användarutbildning och medvetenhet

När man pratar om IT-säkerhet är det lätt att fokusera på teknik – brandväggar, kryptering, antivirusprogram. Men en av de största riskerna i ett IT-system är inte teknik. Det är människor.

Användaren är ofta den svagaste länken i säkerhetskedjan. Det spelar ingen roll hur avancerad säkerhetslösning du har, om någon klickar på en phishing-länk, lämnar sitt lösenord på en post-it-lapp, eller tar med jobbdatorn på semester och glömmer den på tåget.

Därför är utbildning och medvetenhet en central del av säkerhetsarbetet. Syftet är inte att göra alla till IT-experter – utan att ge dem tillräcklig kunskap för att känna igen hot, förstå konsekvenser och agera ansvarsfullt i vardagen.

Exempel på vad utbildning bör täcka:

Vad är ett starkt lösenord?

Hur känner man igen phishing-mejl?

Vad innebär social engineering?

Hur hanteras USB-minnen och bärbara enheter?

Varför är det viktigt att låsa datorn när man går därifrån?

Utbildningen ska vara återkommande. Det räcker inte att ha en timmes föreläsning en gång om året. Det bör finnas korta påminnelser, interna kampanjer, tester och gärna exempel från verkligheten. Målet är att skapa en säkerhetskultur – där säkerhet är något alla tänker på, hela tiden.

Ett vanligt misstag:

Att tro att användare borde fatta. Det gör de inte alltid – inte för att de är dumma, utan för att de inte fått rätt förutsättningar. Att skälla på någon för att de klickade på fel länk är som att bli arg på någon som inte kan cykla – det är bättre att lära dem cykla.

Tips: Låt gärna användarutbildning innehålla lite humor, storytelling och interaktivitet. Människor minns känslor och berättelser bättre än listor med regler.

9.15.2.1 Kontrollfrågor

Varför anses användaren ofta vara den svagaste länken i säkerhetskedjan?

Vad är målet med användarutbildning inom IT-säkerhet?

Nämn tre ämnen som bör ingå i en säkerhetsutbildning för användare.

Vad är social engineering?

Varför är det inte tillräckligt med en engångsutbildning i säkerhet?

Vad menas med säkerhetskultur?

Varför är det bättre att utbilda än att skälla?

Ge ett exempel på hur man kan öka säkerhetsmedvetenhet i vardagen.

Vad bör man göra om man misstänker att man klickat på något farligt?

Vad är poängen med att använda humor eller storytelling i utbildning?

9.15.2.2 Fördjupningslänkar

MSB – Säkerhetskultur i praktiken

CERT-SE – Vanliga säkerhetshot mot användare

Phishing.org – What is Phishing? (eng)

KnowBe4 – Security Awareness Training (eng)

BleepingComputer – Security Tips for Users (eng)

9.15.2.3 Egna anteckningar

(Här kan du skriva ner egna reflektioner, idéer för utbildning, eller exempel på incidenter som hade kunnat undvikas med rätt kunskap.)

9.15.3 Roller, ansvar och säkerhetsorganisation

En säker IT-miljö uppstår inte av sig själv – den måste byggas, underhållas och kontrolleras. Därför krävs tydligt definierade roller och ansvar. Alla i en organisation – från vd till supportpersonal – har en roll att spela i säkerhetsarbetet.

Centrala roller inom IT-säkerhet:

En tydlig ansvarsfördelning minskar risken för att något glöms bort eller faller mellan stolarna. Det bör också finnas dokumentation som klargör:

Vem får göra vad?

Vem ansvarar för säkerhetskopiering?

Vem får ändra brandväggsregler?

Tips: Roller och ansvar kan anpassas efter organisationens storlek – i ett mindre företag kan samma person ha flera roller, men det får aldrig råda oklarhet om vem som har vilket ansvar.

9.15.3.1 Kontrollfrågor

Varför är det viktigt med tydligt definierade roller i IT-säkerhetsarbetet?

Vad har en systemadministratör för ansvar inom säkerhet?

Vad gör en CISO?

Varför är supportpersonal viktiga i säkerhetskedjan?

Vad kan hända om ingen har ansvar för t.ex. säkerhetskopiering?

Ge ett exempel på hur ansvarsfördelning kan se ut i ett mindre företag.

Varför är det viktigt att dokumentera vem som får göra vad?

Vad är användarens ansvar i en säkerhetsorganisation?

Hur kan ansvarsfördelning bidra till bättre incidenthantering?

Kan en person ha flera roller? Vad krävs då för att det ska fungera?

9.15.3.2 Fördjupningslänkar

MSB – Ansvarsfördelning inom informationssäkerhet

CISO Role Explained – Techtarget (eng)

SANS Institute – Security Roles and Responsibilities (eng)

IT Governance – Building a Security Team (eng)

CERT-SE – Säkerhetsfunktioner i organisationer

9.15.3.3 Egna anteckningar

(Skriv ner exempel från skolan, företagsmiljöer eller projekt du deltagit i. Har ni tydliga roller?)

9.15.4 Rutiner och beredskap vid incidenter

Förr eller senare händer det – en incident. Det kan vara ett virus, ett konto som blivit kapat, en förlorad dator, eller en DDoS-attack. Frågan är inte om något händer, utan hur väl förberedd man är när det gör det.

Därför måste det finnas rutiner och beredskap. Att veta i förväg hur man ska agera sparar tid, minskar skada och kan förhindra spridning.

Några grundläggande rutiner:

Incidentrapportering: Vem ska man kontakta? Hur snabbt? Vad ska rapporteras?

Första åtgärder: Koppla ur från nätverket? Informera andra?

Loggning: Vad har hänt, när, och vem var inblandad?

Eskaleringsvägar: När går ärendet från support till säkerhetsansvarig?

Det bör finnas en incidentplan, gärna som en del av en större säkerhetspolicy. I större organisationer har man ofta en CSIRT – Computer Security Incident Response Team – som hanterar allvarliga incidenter.

En bra incidenthantering innehåller också lärdomar. Efter varje incident bör man fråga:

Vad gick fel?

Vad kunde ha gjorts bättre?

Hur kan vi förhindra att det händer igen?

💡 Tips: Det kan vara smart att göra en “brandövning” för IT – en simulerad incident där man tränar personalens reaktion och ser om rutinerna fungerar.

9.15.4.1 Kontrollfrågor

Vad menas med en IT-incident?

Varför är det viktigt att ha rutiner innan något händer?

Vad bör en incidentrapport innehålla?

Vad är det första man bör göra vid en allvarlig incident?

Vad är en CSIRT och vad gör de?

Vad menas med “eskalering” i incidenthantering?

Varför är loggning viktig under och efter en incident?

Vad bör man göra efter att en incident är löst?

Vad är syftet med att göra en “IT-brandövning”?

Ge exempel på en mindre och en allvarlig IT-incident.

9.15.4.2 Fördjupningslänkar

MSB – Hantering av IT-incidenter

CERT-SE – Rapportera IT-incident

CISA – Incident Response Playbook (eng)

ENISA – Guidelines for Incident Management (eng)

NIST – Computer Security Incident Handling Guide (eng)

9.15.4.3 Egna anteckningar

(Har du varit med om ett IT-problem? Hur löstes det? Vad lärde du dig?)

9.15.5 Säkerhetspolicy och dokumentation

En säkerhetspolicy är inte bara ett dokument man skriver för att lägga i en pärm. Det är ett levande styrdokument som beskriver hur organisationen tänker kring säkerhet – vad som är tillåtet, förbjudet, rekommenderat och krävs.

En bra säkerhetspolicy innehåller:

Syfte och mål: Varför behövs denna policy?

Roller och ansvar: Vem gör vad?

Regler för användning: Vad gäller för lösenord, nätverk, fjärranslutning, e-post m.m.?

Incidenthantering: Hur ska problem rapporteras?

Dokumentation och uppföljning: Hur kontrolleras efterlevnad?

Alla policies ska vara begripliga, tillgängliga och uppdaterade. Ingen ska behöva gissa vad som gäller – det ska stå i klartext.

Det bör också finnas loggar, rapporter och checklistor. Inte för att “övervaka” i första hand, utan för att säkerställa att man gör det man sagt att man ska göra.

Tips: Gör säkerhetspolicyn synlig – prata om den, ta upp den på möten, och se till att nya användare får läsa och förstå den direkt vid anställning eller skolstart.

9.15.5.1 Kontrollfrågor

Vad är en säkerhetspolicy?

Varför är det viktigt att den är uppdaterad och tydlig?

Vad bör en säkerhetspolicy innehålla?

Hur används en policy i det dagliga arbetet?

Vad menas med att en policy ska vara ett “levande dokument”?

Varför är det viktigt att alla användare känner till policyn?

Vad innebär uppföljning och hur kan den göras?

Ge exempel på något som kan stå i en policy.

Hur kan dokumentation hjälpa vid en incident?

När ska en policy revideras?

9.15.5.2 Fördjupningslänkar

MSB – Exempel på säkerhetspolicy

Internetstiftelsen – IT-policy mall

NIST – Policy Frameworks (eng)

GDPR och dokumentation

IT Governance – How to write an Information Security Policy (eng)

9.15.5.3 Egna anteckningar

(Finns det en policy där du är? Har du läst den? Vad skulle du vilja ändra eller lägga till?)

9.15.6 Juridik och regelverk

IT-säkerhet är inte bara en teknisk fråga – det är också en juridisk skyldighet. Organisationer måste förhålla sig till ett antal lagar och regelverk som styr hur information hanteras, skyddas och rapporteras. Att inte följa dessa kan få allvarliga konsekvenser, både ekonomiskt och juridiskt.

En av de mest centrala lagarna är GDPR – Dataskyddsförordningen – som styr hur personuppgifter får behandlas. Enligt GDPR måste organisationer ha tydliga syften med insamling av personuppgifter, de får bara lagras så länge som det är nödvändigt, och de måste skyddas från obehörig åtkomst. Dessutom har individen rättigheter – som att få ut sin data, få den rättad eller raderad.

En annan viktig lagstiftning är NIS2-direktivet, som är en uppföljare till det första NIS-direktivet. Det gäller särskilt för samhällsviktiga verksamheter som energi, transporter, sjukvård och digital infrastruktur. NIS2 ställer krav på både förebyggande säkerhetsåtgärder och incidentrapportering. Organisationer som omfattas måste rapportera allvarliga IT-incidenter till myndighet inom 24 timmar.

För verksamheter som hanterar känslig eller säkerhetsskyddad information – till exempel kommuner, statliga myndigheter eller företag med försvarsanknytning – gäller även Säkerhetsskyddslagen. Denna lag reglerar hur man skyddar information som kan vara viktig för Sveriges säkerhet, och omfattar bland annat behörighetskontroller, klassificering av information och säkerhetsprövningar.

En annan viktig juridisk aspekt är ansvarsfördelningen: vem är ansvarig för vad? I dataskyddssammanhang skiljer man på personuppgiftsansvarig (t.ex. en skola eller ett företag som samlar in data) och personuppgiftsbiträde (t.ex. en molntjänstleverantör som behandlar datan åt någon annan). Det är alltid den personuppgiftsansvarige som har det yttersta ansvaret för att reglerna följs – även om själva behandlingen sker hos någon annan.

Att bryta mot dessa regelverk kan få allvarliga konsekvenser. Inom ramen för GDPR kan till exempel sanktionsavgifter på flera miljoner kronor utdelas, även för mindre verksamheter. Utöver det kan bristande efterlevnad leda till förlorat förtroende, rättsprocesser eller utestängning från samarbeten och upphandlingar.

Att ha koll på juridiken är alltså inte en bonus – det är ett grundkrav för varje verksamhet som vill arbeta seriöst med IT-säkerhet.

9.15.6.1 Kontrollfrågor

Vad är syftet med GDPR?

Vilka typer av organisationer omfattas av NIS2-direktivet?

Vad reglerar Säkerhetsskyddslagen?

Vad är skillnaden mellan en personuppgiftsansvarig och ett personuppgiftsbiträde?

Vilka konsekvenser kan det få om man bryter mot lagar inom IT-säkerhet?

9.15.6.2 Fördjupningslänkar

IMY – Dataskyddsförordningen (GDPR)

EU – NIS2-direktivet (engelska)

Säkerhetspolisen – Säkerhetsskyddslagen

MSB – Juridik och informationssäkerhet

GDPR.eu – Guide till dataskyddsförordningen (engelska)

9.15.6.3 Egna anteckningar
 (Har du stött på situationer där juridiken kring IT var viktig? Kände du till rollerna enligt GDPR innan? Skriv ner exempel eller frågor du har.)

9.16 Moderna hot och skydd

IT-hot förändras ständigt. Nya tekniker, arbetssätt och angripare gör att säkerhetsarbetet måste vara proaktivt och ständigt uppdaterat. I detta avsnitt går vi igenom några av de mest aktuella hoten mot IT-miljöer – och hur man kan skydda sig mot dem.

9.16.1 Social engineering och phishing

Det spelar ingen roll hur stark brandväggen är – om en användare frivilligt släpper in angriparen. Social engineering handlar om att lura människor snarare än att bryta sig igenom tekniska skydd.

Den vanligaste formen är phishing – falska mejl eller meddelanden som försöker lura mottagaren att klicka på en länk, lämna ifrån sig lösenord eller installera skadlig kod.

Exempel på phishing:
 – Du får ett mejl från "Skatteverket" som ber dig logga in med BankID.
 – Du får ett SMS från "PostNord" med en länk till en falsk spårningssida.
 – Du blir uppringd av någon som påstår sig vara från IT-avdelningen och ber dig ge bort ditt lösenord.

Phishing kan vara massutskick, men också riktade attacker, t.ex. spear phishing (mot en viss person) eller CEO-fraud (där bedragaren utger sig för att vara chef och ber om en snabb överföring).

Skydd:
 – Utbildning är nyckeln – användare måste veta hur angreppen ser ut.
 – Använd e-postfilter, multifaktorsautentisering och varna för ovanliga språk eller avsändare.
 – Tänk efter innan du klickar. Fråga: "Verkar detta rimligt?"

9.16.2 Ransomware – utpressningsprogram

Ransomware är skadlig kod som krypterar filer på en dator eller ett nätverk. Därefter kräver angriparen en lösensumma (ofta i kryptovaluta) för att återställa filerna.

Ransomware kan komma via phishingmejl, sårbarheter i tjänster eller via oskyddade RDP-portar. Vissa varianter (s.k. double extortion) stjäl först filerna och hotar sedan att publicera dem om man inte betalar.

Exempel på kända ransomware: WannaCry, REvil, LockBit.

Skydd:
 – Uppdatera programvara och operativsystem regelbundet
 – Ta offline-backuper – krypterade filer kan inte återställas om även backuperna påverkas
 – Använd minst MFA och starka lösenord
 – Öva på incidenthantering – vet ni vad ni ska göra om det händer?

9.16.3 Zero-day exploits

En zero-day är en sårbarhet som är okänd för programvarans tillverkare – och som därför inte har någon patch. Den är alltså oskyddad från dag ett.

När sådana sårbarheter upptäcks av angripare, används de ofta i avancerade attacker – innan tillverkaren ens hunnit skapa ett skydd.

Exempel: Log4Shell (2021), en allvarlig zero-day i Java-loggning, drabbade miljontals system.

Eftersom zero-days inte kan blockeras via traditionella patchar krävs andra försvar:

Skydd:
 – Minimera exponerad yta (öppna portar, onödiga tjänster)
 – Använd IDS/IPS-system och loggning för att upptäcka konstig trafik
 – Använd säkerhetsprinciper som Least Privilege – begränsa vad en användare/process kan göra
 – Håll dig uppdaterad via säkerhetsflöden (t.ex. CERT-SE)

9.16.4 Honeypots – lura angriparen

En honeypot är en fälla. Den ser ut som ett riktigt system – t.ex. en SSH-server eller webbserver – men är till för att bli attackerad. Syftet är att:

Locka angripare så att de avslöjar sina metoder

Hålla dem borta från riktiga system

Samla information om vilka hot som finns

Tänk så här: Istället för att jaga angriparen – låt dem komma till dig.

I skolmiljö eller labbar används ofta verktyg som Cowrie (SSH/Telnet-honeypot) eller Dionaea (för att fånga malware).

En honeypot måste isoleras från produktionsnätverket – annars riskerar den att bli en språngbräda.

9.16.5 Penetrationstester – simulerade attacker

Ett penetrationstest (eller "pentest") är en kontrollerad attack där en etisk hackare försöker bryta sig in i ett system – på uppdrag av systemägaren. Målet är att hitta svagheter innan någon illvillig gör det.

Pentest kan vara manuella eller automatiserade och omfatta t.ex.:

– Sårbarhetsscanning
 – Försök att utnyttja brister (exploits)
 – Social engineering-tester
 – Fysisk intrångstest

Exempel på verktyg:
 – Kali Linux
 – Metasploit
 – Nmap
 – Burp Suite

Juridik: Ett pentest får aldrig ske utan godkännande. Etiska hackare följer lagar, dokumenterar allt och lämnar rapport till uppdragsgivaren.

9.16.6 Säkerhet i molnet och vid distansarbete

I takt med att fler arbetar hemifrån och system flyttas till molnet, har även hotbilden förändrats. Säkerhet måste nu fungera utanför företagets väggar.

Utmaningar i molnet:
 – Oklar ansvarsfördelning (vem skyddar vad?)
 – Dålig konfiguration (t.ex. öppna S3-buckets)
 – Felaktig hantering av användarbehörigheter

Utmaningar vid distansarbete:
 – Osäkra Wi-Fi-nät
 – Privata enheter
 – Brist på övervakning

Skyddsåtgärder:
 – Använd Zero Trust-modellen: Ingen är "automatiskt betrodd"
 – Se till att MFA används överallt
 – Använd central identitetshantering
 – VPN + Endpoint-skydd
 – Loggning och övervakning även utanför kontorsnätet

Molntjänster kan vara säkra – men bara om de konfigureras rätt och om användarna förstår sitt ansvar.

9.16.7 Kontrollfrågor

Vad är skillnaden mellan phishing och spear phishing?

Hur fungerar ransomware, och varför är det farligt?

Vad är en zero-day-sårbarhet?

Varför är honeypots användbara inom IT-säkerhet?

Vad är syftet med ett penetrationstest?

Vilka verktyg kan användas vid ett pentest?

Vad innebär "Zero Trust"-modellen?

Nämn två risker med dåligt konfigurerade molntjänster.

Hur kan man skydda sig vid distansarbete?

Varför är MFA extra viktigt vid molnanvändning?

9.16.8 Fördjupningslänkar

– CERT-SE – Aktuella säkerhetshot
  – KnowBe4 – Träning mot phishing
  – NoMoreRansom – Hjälp mot ransomware
  – OWASP – Honeypot-projekt
  – NIST – Zero Trust Architecture

9.16.9 Egna anteckningar

(Lämna plats för egna reflektioner, case eller exempel.)

9.17 Verktyg, övervakning och loggning

Att ha brandväggar, antivirus och uppdateringar är viktigt – men det räcker inte. För att kunna upptäcka angrepp, analysera intrång och förstå vad som händer i ett system behövs övervakning och loggning. Detta kapitel går igenom verktygen och tankesätten bakom ett effektivt övervakningssystem.

9.17.1 Varför loggning är avgörande

Loggfiler är systemets minne. De registrerar allt från inloggningar och systemfel till nätverkstrafik och misstänkta aktiviteter. Om något går fel – en server kraschar, ett konto kapas eller en ransomware-attack inträffar – är det loggarna som hjälper oss att förstå vad som hänt.

Utan loggar blir felsökning ofta en gissningslek.

Exempel på viktiga loggfiler i olika miljöer:

Windows: Event Viewer (t.ex. Security, System, Application)

Linux: /var/log/auth.log, /var/log/syslog, /var/log/apache2/*

Nätverk: brandväggsloggar, routrar, accesspunkter

Applikationer: databasservrar, webbservrar, e-postservrar

Tips: Att logga är inte nog – du måste också samla in, analysera och spara loggar på ett säkert sätt.

9.17.2 Centrala loggverktyg – Syslog, journald, Event Viewer

I moderna IT-miljöer är det vanligt att loggar från många olika enheter samlas på ett ställe. Detta kallas central logghantering, och gör att man lättare kan upptäcka mönster och hot.

Linux

Syslog: Ett äldre men fortfarande vanligt system som skriver loggar till /var/log/. Verktyg som rsyslog eller syslog-ng används ofta för att samla in och skicka loggar.

journald: Nyare loggsystem i systemd-baserade distributioner (t.ex. Ubuntu). Kommandot journalctl används för att visa loggar.

Windows

Event Viewer: Inbyggt verktyg där systemet grupperar loggar i t.ex. System, Security, och Application.

För central hantering används ofta Event Forwarding eller verktyg som Graylog, Wazuh eller Elastic Stack (ELK).

Loggformaten skiljer sig, men budskapet är detsamma: “Vad hände, när hände det – och varför?”

9.17.3 Övervakningsverktyg – Wazuh, Zabbix, Nagios

Loggning är passivt – det skriver ner vad som händer. Övervakning är mer aktivt – den säger till om något händer i realtid.

Exempel på verktyg:

Wazuh: Open source XDR/EDR och SIEM-lösning. Samlar in loggar, upptäcker hot och varnar.

Zabbix: Kraftfullt övervakningssystem som mäter allt från CPU-användning till nätverkstrafik.

Nagios: Klassiker inom serverövervakning. Kan användas för att hålla koll på driftstatus, nätverksresurser, m.m.

De här verktygen kan:

Skicka e-post eller SMS vid fel

Rita grafer över trender (t.ex. CPU-belastning)

Identifiera attacker och ovanlig aktivitet

Dokumentera SLA och tillgänglighet

Använd flera nivåer: Loggar + övervakning + larm = bäst skydd.

9.17.4 SIEM – Samlad analys av säkerhetsloggar

SIEM står för Security Information and Event Management. Det är en lösning för att:

Samla in loggar från många system

Korrelera händelser (”logga A + logga B = attack”)

Upptäcka ovanlig aktivitet

Ge översikt i realtid

Ett SIEM-system fungerar som säkerhetens kontrollrum. Du ser attacker medan de händer, och kan agera direkt.

Exempel på SIEM-verktyg:

Wazuh – inkluderar SIEM-funktionalitet

Graylog – fokuserar på logganalys

Splunk – kommersiellt kraftpaket

ELK Stack (Elasticsearch, Logstash, Kibana) – flexibel och populär i open source-världen

SIEM är särskilt viktigt i större nätverk, skolor, företag och organisationer där många användare och system interagerar.

9.17.5 Att tänka på vid övervakning – etik och lagstiftning

Med stora möjligheter kommer också ansvar. Att övervaka användare, logga trafik och lagra data innebär att man måste:

Följa GDPR och andra lagar

Informera användare om att loggning sker

Inte spara mer än nödvändigt

Skydda loggarna mot manipulation

Etik handlar också om tillit. Om elever, anställda eller användare vet att de övervakas, måste det ske med transparens och goda skäl.

En grundregel: Logga för att skydda systemet – inte för att spionera på människor.

9.17.6 Kontrollfrågor

Varför är loggfiler viktiga vid IT-säkerhetsarbete?

Vad är skillnaden mellan loggning och övervakning?

Vad gör ett verktyg som Wazuh?

Vad står SIEM för och vad används det till?

Nämn två loggverktyg i Linux och två i Windows.

Vad innebär central logghantering?

Vad är fördelen med att ha övervakning i realtid?

Hur kan GDPR påverka hur man hanterar loggar?

Vad är syftet med korrelation i ett SIEM-system?

Varför är det viktigt att informera användare om övervakning?

9.17.7 Fördjupningslänkar

– Wazuh – Officiell webbplats

– Graylog – Logghantering

– Zabbix – Övervakning

– Splunk – SIEM-lösning

– MSB – Loggning och incidenthantering

9.17.8 Egna anteckningar

(Lämna plats för reflektioner, egna verktygstips eller exempel.)

9.18 Säkerhet i skarpa miljöer och incidenthantering

Att förstå teorin bakom IT-säkerhet är en sak – men i verkligheten är miljöer ofta röriga, användarna slarviga och hoten ständigt föränderliga. Det är i dessa skarpa miljöer som säkerhet sätts på prov. Här måste man inte bara förebygga attacker – utan också upptäcka, begränsa skadan och återställa systemen efter incidenter.

9.18.1 Vad menas med ”skarp miljö”?

En ”skarp” miljö innebär att systemet används i drift, med riktiga användare, data och affärsprocesser. Det kan vara ett företag, en skola, ett sjukhus – vilket som helst system där driftstopp eller dataintrång får verkliga konsekvenser.

Exempel:

En skola där elevregister läcks

Ett företag som får sin webshop nedsläckt av ransomware

En kommun som tappar tillgång till sina e-postservrar

Säkerhetskraven är ofta högre i skarpa miljöer än i utvecklings- eller testmiljöer. Här krävs:

Backupstrategier

Rutiner för uppdatering

Övervakning

Incidentplaner

9.18.2 Vad gör man när det händer något?

Det spelar ingen roll hur bra skydd du har – incidenter inträffar ändå. Det kan vara:

Skadlig kod

Obehöriga inloggningar

System som slutar svara

Dataintrång

Då är frågan: Vad gör du?

De flesta företag (och skolor) bör ha en incidenthanteringsplan. Den består ofta av fem steg:

Identifiera – Vad har hänt?

Meddela – Informera rätt personer (IT, chef, juridik)

Isolera – Begränsa skadan (koppla bort nätverk, stäng ner system)

Analysera – Undersök hur det hände

Återställ – Få igång systemen igen, med bättre skydd

Tips: Ha kontaktvägar och ansvarsfördelning klara i förväg. I en kris är det inte läge att börja gissa vem som gör vad.

9.18.3 Att kommunicera i kris – vem säger vad till vem?

När något går fel är kommunikationen ofta lika viktig som tekniken. Otydlig eller sen information kan leda till:

Panik bland användare

Dåligt rykte i media

Bristande förtroende hos kunder, elever eller personal

En bra kommunikationsplan innehåller:

Vem ansvarar för att informera?

Vilka ska få information? (interna, externa)

Vad ska sägas – och vad ska inte sägas?

Hur ska det sägas? (e-post, möte, pressmeddelande?)

Exempel från skola:
Om en elev har laddat ner ransomware till en dator i datasalen – vem informerar lärarna? Rektor? Eleverna? Vårdnadshavarna?

9.18.4 Dokumentation, bevis och återställning

När incidenten hanterats är jobbet inte över. Nu börjar det viktiga efterarbetet:

Dokumentera allt: Tider, IP-adresser, konton, åtgärder

Spara loggar och filer (kan behövas som bevis)

Analysera vad som gick fel – tekniskt och organisatoriskt

Förbättra rutiner, uppdatera system och träna personal

I vissa fall kan man behöva kontakta:

Datainspektionen (vid personuppgiftsläckor)

Försäkringsbolag

Polisen (vid brott)

Om du inte kan återställa systemen – var finns backupen? Och hur snabbt kan du återställa den?

9.18.5 Vanliga misstag vid incidenthantering

Ingen övning – Många har en plan på papper, men ingen vet vad de ska göra i praktiken.

Ingen loggning – Utan loggar finns inget att analysera.

För sent agerande – Många attacker kan stoppas om man reagerar direkt.

Kommunikationskaos – "IT säger en sak, lärarna en annan – vem har rätt?"

Ingen analys efteråt – Problemen kommer tillbaka om man inte lär sig något.

Gör gärna en övning per år: "Vad gör vi om någon installerar ransomware?" – och låt olika roller spela igenom scenariot.

9.18.6 Kontrollfrågor

Vad innebär en "skarp miljö"?

Vad är de fem stegen i en typisk incidenthanteringsplan?

Varför är det viktigt att ha en kommunikationsplan vid incidenter?

Vad bör dokumenteras efter en säkerhetsincident?

Nämn två externa parter som kan behöva kontaktas vid ett intrång.

Varför är övning viktig för incidenthantering?

Vad är ett vanligt misstag vid incidenter?

Vad innebär det att isolera ett system?

Ge exempel på vad som kan ingå i en återställning.

Hur kan man använda en incident som lärotillfälle?

9.18.7 Fördjupningslänkar

– MSB – Hantera informationssäkerhetsincidenter

– CERT-SE – Nationell incidenthantering

– Datainspektionen – Anmäl personuppgiftsincident

– NIST – Computer Security Incident Handling Guide (PDF)

– European Union Agency for Cybersecurity – Incident Response

9.18.8 Egna anteckningar

(Plats för reflektioner, rutiner ni har på skolan, eller saker du vill testa i praktiken.)

9.19 Social engineering, phishing och mänskliga misstag

De flesta säkerhetsproblem i IT-världen orsakas inte av supersmarta hackare som utnyttjar avancerade kodbuggar. De orsakas av… människor. Vi klickar på fel länk, luras att lämna ifrån oss information, eller glömmer uppdatera system i tid. Det är här social engineering kommer in.

Social engineering handlar om att utnyttja människors beteenden, vanor och tillit – inte att hacka datorer, utan att manipulera personer.

9.19.1 Vad är social engineering?

Social engineering är en form av psykologisk manipulation. Syftet är att få någon att göra något de inte borde – t.ex. klicka på en länk, lämna ut ett lösenord eller installera skadlig kod.

Det bygger ofta på:

Stress

Auktoritet (”Jag ringer från IT”)

Nyfikenhet (”Se bifogade dokument”)

Rädsla (”Ditt konto stängs om du inte loggar in nu!”)

Exempel: Någon ringer till receptionen och låtsas vara tekniker. De ber om fjärråtkomst till en dator för att "installera en uppdatering". I själva verket tar de kontroll över systemet.

9.19.2 Vanliga sociala attacker

Här är några vanliga metoder som används för att lura människor:

9.19.3 Varför fungerar det så ofta?

Vi människor är ofta den svagaste länken i säkerhetskedjan – inte för att vi är dumma, utan för att vi:

Vill hjälpa till

Tänker inte alltid efter

Har ont om tid

Litar på andra

Är ovana vid digitala hot

En välformulerad bluff kan lura både nybörjare och erfarna användare.

Faktum: Enligt flera studier är över 90 % av alla cybersäkerhetsincidenter relaterade till mänskligt beteende.

9.19.4 Träning och medvetenhet

Att förhindra social engineering handlar mer om kultur än teknik.

Det viktigaste skyddet är att människor:

Vet att hoten finns

Lär sig känna igen varningssignaler

Vågar säga nej

Vet vem de ska kontakta vid tveksamheter

Bra metoder för skolor och arbetsplatser:

Falska phishing-test (skicka egna bluffmejl som träning)

Genomgångar av riktiga exempel

Rollspel (”Hur reagerar du om någon ringer från IT?”)

Synliga rutiner för att rapportera incidenter

9.19.5 Att skapa en stark säkerhetskultur

Säkerhet börjar inte i brandväggen – den börjar med hur vi tänker.

Ett låst serverrum skyddar inte om någon släpper in en främling "för att de ser ut att jobba här".

En bra säkerhetskultur kännetecknas av:

Låg tröskel för att rapportera misstänkta händelser

Tydlighet: Vad gäller och vad gäller inte?

Uppmuntran istället för skam (”Bra att du rapporterade”)

Att säkerhet tas upp ofta – inte bara vid kris

9.19.6 Kontrollfrågor

Vad är social engineering?

Ge exempel på tre vanliga metoder inom social engineering.

Vad skiljer spear phishing från vanlig phishing?

Vad menas med vishing?

Varför fungerar social engineering ofta så bra?

Hur kan man träna människor att stå emot bluffar?

Vad är pretexting?

Vad menas med att ha en "säkerhetskultur"?

Varför är det viktigt att rapportera misstänkta händelser?

Ge ett exempel på en enkel men effektiv säkerhetsåtgärd.

9.19.7 Fördjupningslänkar

– CSO Online – What is Social Engineering?

– KnowBe4 – Social Engineering Explained

– Phishing.org – What is Phishing?

– MSB – Phishing och bluffmejl

– Naked Security by Sophos – Real-life social engineering cases

9.19.8 Egna anteckningar

(Plats för egna reflektioner, exempel från skolan eller egna erfarenheter.)

9.20 Loggning, övervakning och revision

I takt med att hotbilden mot IT-system växer, blir det allt viktigare att inte bara skydda systemen – utan också att kunna upptäcka, spåra och analysera incidenter när de inträffar. Här spelar loggning, övervakning och revision en avgörande roll.

Att "ha loggning" är inte detsamma som att "använda loggarna". Många företag sparar automatiskt loggfiler men saknar rutiner för att läsa av dem, analysera dem eller agera på det som upptäcks. Detta kapitel fördjupar sig i hur och varför loggning bör integreras i säkerhetsarbetet.

9.20.1 Varför loggning är en säkerhetsfråga

Loggning handlar om att skapa spårbarhet. När något går fel, eller när en attack upptäcks i efterhand, är loggfiler ofta det enda sättet att ta reda på vad som hände, hur det gick till, och vem som var inblandad.

Exempel:

Inloggningsförsök (både lyckade och misslyckade)

Filsystemsåtkomst

Programinstallationer

Systemuppdateringar

Brandväggsregler som ändrats

Trafik som blockeras eller släpps igenom

Loggar blir därmed en "svart låda" för IT-system, ungefär som i ett flygplan. Ju mer detaljerad loggning – desto bättre analysmöjlighet vid en incident.

9.20.2 Vad som bör loggas

Att logga "allt" kan snabbt bli opraktiskt, dels p.g.a. lagringskostnader, men också för att det kan försvåra analysen. Fokus bör ligga på viktiga händelser och mönster som är relevanta för säkerhet:

Inloggningar (särskilt felaktiga)

Ändringar i användarbehörigheter

Konfigurationsändringar

Start/stopp av tjänster

Brandväggsändringar

Systemfel och kraschloggar

Anrop till känsliga API:er eller databaser

Åtkomst till känsliga filer

I domänmiljöer bör Active Directory-aktiviteter (Group Policy-ändringar, kontoskapande etc.) loggas noga.

För webbtjänster är det viktigt att logga:

IP-adress

Användaragent

Sessions-ID

Begärd URL

Statuskod (200, 403, 404 osv.)

Men det är också viktigt att inte logga för mycket persondata, vilket vi kommer till nedan.

9.20.3 Övervakning i realtid

Det räcker inte alltid att spara loggar – ibland krävs aktiv övervakning i realtid för att upptäcka hot innan de blir till attacker.

Verktyg som kan användas:

Wazuh – kombinerar logginsamling, regler och incidentrespons

Fail2ban – reagerar på mönster i loggar (t.ex. många felinloggningar)

SIEM-system (Security Information and Event Management) – exempelvis Splunk, ELK eller Microsoft Sentinel

IDS/IPS-system – ofta integrerade med loggning och övervakning

Övervakning i realtid är särskilt viktigt i miljöer med:

Exponering mot internet

Fjärrinloggning via SSH eller RDP

Känslig data (t.ex. personuppgifter eller affärshemligheter)

9.20.4 Revision och efteranalys

Revision är processen att granska loggar i efterhand, antingen i syfte att förstå en inträffad incident eller för att kontrollera efterlevnad av policyer och lagar.

Det kan handla om att:

Kontrollera vem som ändrade i en databas

Spåra när ett konto skapades och av vem

Granska hur många gånger någon försökt logga in med fel lösenord

Kontrollera vilka IP-adresser som haft åtkomst till ett system

Revision är också viktigt för att visa att man följer lagar och regler, t.ex. inom GDPR, ISO 27001 eller NIS2.

9.20.5 Juridiska aspekter på loggning

Att logga innebär ofta att man behandlar personuppgifter – särskilt om IP-adresser, användarnamn eller aktivitet sparas. Därför är det viktigt att:

Informera användare om loggning sker

Begränsa loggtiden (t.ex. radera efter 30 dagar om inte längre krävs)

Undvika att logga t.ex. lösenord, kreditkortsnummer eller andra känsliga uppgifter

Skydda loggfiler mot obehörig åtkomst

En loggfil är alltså inte bara en teknisk resurs – den är också ett register enligt dataskyddslagstiftningen.

9.20.6 Vanliga misstag

Att inte kontrollera att loggning verkligen är aktiverad.
 Många system kräver att loggning manuellt slås på.

Att spara loggar lokalt utan backup.
 Vid t.ex. ransomware-angrepp är lokala loggar ofta bland det första som raderas.

Att inte läsa loggar förrän något går fel.
 Loggar ska analyseras förebyggande, inte bara i efterhand.

Att inte tänka på integriteten.
 För mycket detaljer i loggar kan utgöra ett riskmoment i sig.

9.20.7 Kontrollfrågor

Varför är loggning en viktig del av IT-säkerhet?

Ge tre exempel på vad som bör loggas i ett serversystem.

Vad menas med "övervakning i realtid"?

Vilka verktyg kan användas för att upptäcka mönster i loggfiler?

Vad är ett SIEM-system?

Hur används revision i säkerhetsarbetet?

Vilken roll spelar loggning i efterlevnad av GDPR?

Vad är en risk med att logga för mycket information?

Ge exempel på en juridisk åtgärd man bör vidta vid loggning.

Varför är det ett problem att spara loggar endast lokalt?

9.20.8 Fördjupningslänkar

Wazuh – Open Source Security Platform

Logghantering och GDPR (Integritetsskyddsmyndigheten)

Introduction to SIEM – Microsoft

Graylog – Open source log management

EU GDPR – What is considered personal data?

9.20.9 Egna anteckningar

(Lämna plats för egna reflektioner och anteckningar här.)

9.21 Backup och återställning

Att ha en bra backup är inte bara en teknisk åtgärd – det är en försäkring mot dataförlust, ransomware, hårddiskhaverier, mänskliga misstag och katastrofer. Trots det är backup ofta något som prioriteras först efter att något gått fel. I detta kapitel går vi igenom varför backup är livsviktigt, vilka metoder som finns, hur man testar återställning och vanliga misstag att undvika.

9.21.1 Varför backup?

Alla som någon gång har tappat bort viktiga filer vet hur frustrerande det kan vara. Men när det handlar om en hel servermiljö, kritisk verksamhetsdata eller en databas med kundinformation – då kan förlusten bli förödande.

Några vanliga orsaker till dataförlust:

Ransomware (filer krypteras av skadlig kod)

Oavsiktlig radering

Haveri i hårdvara (t.ex. SSD-dödsfall)

Brand, översvämning eller elfel

Sabotage eller stöld

Felaktiga uppdateringar

En säkerhetskopia är inte bara till för återställning efter katastrof – det är också ett verktyg för att ångra misstag, återställa tidigare versioner av filer, och möjliggöra experimentering utan rädsla.

9.21.2 Typer av backup

Det finns flera typer av backup – varje med fördelar och nackdelar beroende på miljö och behov:

Full backup
 En komplett kopia av allt som ska säkerhetskopieras. Långsammare, men enkel att återställa.

Inkrementell backup
Säkerhetskopierar endast det som ändrats sedan senaste backupen (inkrementell eller full). Snabb och platsbesparande – men kräver fler steg vid återställning.

Differentiell backup
Säkerhetskopierar allt som ändrats sedan senaste fullständiga backup. En kompromiss mellan hastighet och återställningskomplexitet.

Snapshot
En ögonblicksbild av ett system – ofta använd inom virtualisering (t.ex. Proxmox eller Hyper-V). Bra för snabb återställning men bör inte ersätta traditionell backup.

Molnbaserad backup
Data skickas till en extern molntjänst (exempel: Backblaze, Wasabi, Azure, AWS). Bra vid fysiska katastrofer men kräver stabil uppkoppling och dataskyddsavtal.

Offline-backup
 Backup lagras på fristående media (ex. USB-diskar) som sedan kopplas bort från nätverket. Extra skydd mot ransomware.

9.21.3 3-2-1-regeln

En tumregel för säker backup är:

3 kopior av data
2 olika typer av lagringsmedia
1 kopia offsite (t.ex. i moln eller annan byggnad)

Exempel:

Original på server

Kopia till lokal NAS

Molnkopia till Backblaze

Denna metod skyddar mot både tekniska, fysiska och mänskliga fel.

9.21.4 Återställning – ofta glömd men avgörande

Att kunna återställa är viktigare än att kunna ta backup. Det är lätt att tro att en backup fungerar – tills man behöver den. Därför bör återställningstest göras regelbundet.

Bra vanor:

Dokumentera hur återställning går till (steg-för-steg)

Testa återställning varje kvartal eller halvår

Återställ både filer och hela system (inkl. databaser)

Kontrollera integriteten hos backupfiler (t.ex. med checksummor)

Återställningen bör även testas i tid – om det tar 10 timmar att återställa ett system i drift, kan konsekvenserna bli dyra.

9.21.5 Kryptering och integritet

Backup är också ett säkerhetsproblem. Om en backup innehåller känslig data (t.ex. personuppgifter, lösenord, medicinsk information) och hamnar i fel händer, kan det bli en katastrof.

Skyddsåtgärder:

Kryptera backupfiler (t.ex. med VeraCrypt eller inbyggd lösning)

Skydda backupservrar med brandväggar och stark autentisering

Kontrollera loggar – så att ingen obehörig läser eller laddar ner backup

En komprometterad backup är värre än ingen backup alls – då ger den angriparen tillgång till hela ditt system.

9.21.6 Vanliga misstag

Bara en backup – Om den skadas eller blir stulen finns inget skydd kvar.
Backup på samma disk/server – Om den kraschar är allt borta.
Ingen testad återställning – Det fungerar bara i teorin.
Okrypterade backupfiler – Risk för dataläckor.
Manuella backuprutiner – Människor glömmer. Automatisera!

9.21.7 Kontrollfrågor

Varför är backup viktigt för säkerhet?

Vad är skillnaden mellan en inkrementell och en differentiell backup?

Förklara 3-2-1-regeln för backup.

Varför räcker det inte att bara ta backup – varför måste man testa återställning?

Vad är en snapshot och när kan det användas?

Vilka risker finns med att inte kryptera sina säkerhetskopior?

Vad menas med offline-backup?

Hur kan molnbaserad backup vara både en fördel och en risk?

Vilken backupstrategi skulle du föreslå för ett mindre företag?

Vad är de vanligaste misstagen vid backuphantering?

9.21.8 Fördjupningslänkar

Veeam – What is 3-2-1 Backup?

CrashPlan for Small Business

Backblaze Blog – Real World Backup Strategies

Linux Handbook – rsync command explained

MSB – Råd för backup och återställning

9.21.9 Egna anteckningar

(Lämna plats för egna reflektioner och anteckningar här.)

9.22 Säkerhetskopiering i molnet

I takt med att allt mer data lagras digitalt har behovet av säkerhetskopiering blivit viktigare än någonsin. Molnbackup har vuxit fram som ett kraftfullt alternativ till traditionell lokal backup. Det ger tillgång till backup oavsett plats – men medför också nya risker och krav. Det här kapitlet går igenom hur molnbackup fungerar, vad man bör tänka på och vanliga fallgropar.

9.22.1 Vad innebär molnbackup?

Molnbackup innebär att man säkerhetskopierar sin data till en server på internet – ett så kallat moln. Det kan vara en dedikerad tjänst som Backblaze eller ett bredare ekosystem som Google Drive eller Microsoft OneDrive. Syftet är detsamma som vid lokal backup: att skydda data vid förlust, skada, stöld eller attack.

Fördelar med molnbackup:

Åtkomst från olika platser och enheter

Automatisk synkronisering och versionering

Skydd mot lokala katastrofer (t.ex. brand, stöld)

Skalbarhet – du kan växa med mängden data

Nackdelar:

Kräver stabil internetanslutning

Kostar pengar vid större volymer

Integritetsrisk – data lagras hos tredje part

Mindre kontroll än vid lokal backup

Att förstå var och hur datan lagras är avgörande – särskilt ur integritets- och GDPR-perspektiv.

9.22.2 Olika typer av molnbackup

Alla molnbackuper fungerar inte likadant. Här är några vanliga modeller:

Molnet som primär backup
 Hela säkerhetskopieringen sker i molnet, t.ex. med tjänster som Backblaze, iCloud eller iDrive. Bra för hemanvändare eller småföretag.

Hybridbackup
 Data sparas både lokalt (t.ex. på extern hårddisk) och i molnet. Ger det bästa av två världar: snabb återställning lokalt + extern säkerhet.

SaaS-backup
 Backup av molnbaserade tjänster som Microsoft 365, Google Workspace eller Dropbox. Viktigt att förstå att Microsoft/Google inte automatiskt ansvarar för all din data – du är själv ansvarig för backup.

Backup i molninfrastruktur (IaaS/PaaS)
 Företag som kör servrar i Azure, AWS eller Google Cloud behöver ofta externa backup-lösningar. Inbyggda funktioner räcker sällan för full återställning.

9.22.3 Kryptering och integritet i molnbackup

Säkerhetskopiering är inte säkert utan kryptering. Det finns två huvudmodeller:

Klientsidans kryptering
 Datan krypteras på användarens dator innan den skickas upp. Endast användaren har nyckeln – högsta säkerhetsnivå, men kräver att du själv hanterar nycklarna säkert.

Serversidans kryptering
 Datan skickas okrypterad och krypteras av molnleverantören. Enklare, men leverantören har tillgång till innehållet.

Vem har nyckeln?

Om du själv har nyckeln (end-to-end encryption): bättre säkerhet.

Om leverantören har nyckeln: större risk för intrång, dataläckor eller statlig insyn.

Rättsliga krav att tänka på:

GDPR: Du ansvarar för hur persondata behandlas – även i molnet.

Schrems II: Personuppgifter i moln utanför EU kräver särskilda skyddsåtgärder.

Dataplacering: Kontrollera om datan lagras inom EU eller i tredje land.

9.22.4 Återställning från molnet – utmaningar och tips

Att skapa en backup är inte svårt – det är återställningen som avslöjar om systemet fungerar. Flera utmaningar uppstår först när det verkligen gäller.

Vanliga problem:

Nedladdningshastighet: Återställning av flera hundra GB kan ta timmar eller dagar.

Bandbreddsgränser: Vissa molntjänster stryper trafiken vid hög användning.

Filversionsproblem: Råkade du radera en fil för tre veckor sedan? Kanske finns den inte kvar längre.

Krypterade backuper: Om du har tappat bort nyckeln är datan oåtkomlig – för alltid.

Tips:

Testa återställning regelbundet (även om det bara är en liten mapp).

Dokumentera exakt hur återställningen går till.

Överväg leverantörer som erbjuder "data shuttle" – fysisk leverans av backup på hårddisk.

9.22.5 Exempel på populära molnbackup-tjänster

För privatpersoner kan även iCloud och OneDrive fungera som backup – men de har ofta begränsad kontroll och automatisering jämfört med dedikerade tjänster.

9.22.6 Fallgropar och rekommendationer

Molnet är inte magi. Många tror att bara för att data ligger i molnet så är den säker – men det stämmer inte. Du måste själv:

Säkerställa att backup faktiskt sker (och inte bara en synkning!)

Verifiera versionshantering – hur länge sparas gamla versioner?

Se till att rätt mappar/filer inkluderas (ibland måste de väljas manuellt)

Testa återställning regelbundet

Vanliga misstag:

Synkronisering förväxlas med backup – om du raderar en fil i Dropbox så raderas den överallt

Retention är för kort – gamla raderade filer går inte att återställa

Kryptering glöms bort – data lagras i klartext hos leverantören

Rekommendation: Använd en hybridlösning (lokalt + moln), välj en tjänst med stark kryptering och dokumentera både backup- och återställningsprocess.

9.22.7 Kontrollfrågor

Vad är skillnaden mellan molnbackup och lokal backup?

Nämn två fördelar och två nackdelar med molnbackup.

Vad menas med SaaS-backup och varför behövs det?

Vad är skillnaden mellan klientsidans och serversidans kryptering?

Vilka rättsliga krav måste beaktas vid lagring av data utanför EU?

Varför är det viktigt att testa återställning regelbundet?

Vad menas med hybridbackup?

Nämn tre exempel på molnbackup-tjänster.

Vad är problemet med att bara använda synkronisering som backup?

Vad innebär begreppet ”retention” i samband med backup?

9.22.8 Fördjupningslänkar

Backblaze – How Backup Works

Wasabi – Cloud Storage Overview

GDPR och molntjänster (IMY)

CrashPlan for Business

Veeam – SaaS Backup for Microsoft 365

9.22.9 Egna anteckningar

(Lämna plats för reflektioner, exempel från undervisningen eller egna molnerfarenheter.)

9.23 Etisk hacking och hackingkultur

I dagens digitala värld är det viktigt att förstå både hur attacker går till och varför de sker. Men det är minst lika viktigt att förstå skillnaden mellan att utföra en attack – och att förstå den för att kunna försvara sig. Det är här begreppet etisk hacking kommer in i bilden.

En etisk hackare (även kallad white hat) använder sina kunskaper om cybersäkerhet för att upptäcka sårbarheter innan någon illasinnad hinner utnyttja dem. Detta sker med tillstånd och i syfte att skydda. Etisk hacking är därför inte bara acceptabel – den är en central del av dagens IT-säkerhetsarbete.

Men för att förstå försvar måste man förstå angrepp. I detta kapitel går vi därför igenom vanliga angreppstyper, hotaktörer, verktyg, och hur den etiska hackaren arbetar.

Hattfärger – olika typer av hackers

Inom säkerhetsvärlden används färger för att beskriva olika roller och avsikter:

Vit hatt – Etiska hackers. Arbetar för att hitta och rapportera säkerhetshål innan någon annan utnyttjar dem. Ofta anställda inom IT-säkerhet.

Svart hatt – Illasinnade hackers. Bryter sig in i system för personlig vinning eller förstörelse.

Grå hatt – Ligger mittemellan. Upptäcker sårbarheter utan tillstånd, men rapporterar dem ofta – ibland efter att ha demonstrerat sin poäng.

Grön hatt – Nybörjare i hackingvärlden. Ofta nyfikna, med ambitionen att lära sig, men utan stor erfarenhet.

Röd hatt – En ovanligare beteckning. Används ibland för att beskriva aggressiva "hack-back"-aktörer som inte bara försvarar sig utan går till motattack. Också ett litet skämt, eftersom Red Hat är ett Linux-företag.

Att förstå hacking handlar alltså inte bara om teknik, utan även om avsikt, etik och lagstiftning.

Operativsystem för penetrationstester

Professionella penetrationstestare använder särskilda operativsystem som är fullpackade med verktyg för att testa säkerheten i system:

Kali Linux – Det mest kända OS:et för penetrationstester. Innehåller hundratals förinstallerade verktyg för nätverksscanning, analys, brute force, social engineering och mer.

Parrot Security OS – Ett alternativ till Kali som fokuserar mer på anonymitet, forensik och prestanda. Också Debian-baserat.

BackBox – Ett lättviktsalternativ till Kali, baserat på Ubuntu.

Tails – Inte för hacking direkt, men används av aktivister och journalister för att surfa anonymt och säkert via Tor.

Dessa system används i utbildningssyfte, på testmiljöer – aldrig mot verkliga system utan tillstånd.

Verktyg för etisk hacking – exempel och funktion

Wireshark – Nätverkssniffer för att analysera trafik. Vanligt för att avslöja klartextlösenord och förstå nätverksprotokoll.

Nmap – Skannar nätverk efter öppna portar och tjänster.

Metasploit Framework – Ramverk för att utveckla och köra exploits mot sårbara system.

Hydra – Brute force-verktyg som testar lösenord mot olika tjänster.

John the Ripper / Hashcat – Verktyg för att knäcka hashade lösenord.

Burp Suite – Verktyg för att testa webbapplikationers säkerhet (XSS, SQLi m.m.).

Syftet med etisk hacking

Målet med etisk hacking är inte att förstöra – utan att förbättra. Genom att tänka som en angripare kan man identifiera svagheter i system innan de utnyttjas av någon med onda avsikter. Etisk hacking används bland annat för:

Penetrationstester

Sårbarhetsbedömningar

Utbildning och träning

Säkerhetsgranskningar

Bug bounty-program

Men det viktigaste verktyget är alltid etik och ansvar.

Vanliga attacker

Man-in-the-middle (MITM) – Avlyssning och manipulering av trafik mellan två parter.

Man-on-the-side – Passiv avlyssning och snabba svar innan legitima servrar hinner svara.

Maid attack – Fysisk tillgång till datorer utnyttjas (t.ex. hotellrum).

Drive-by attack – Webbsidor infekterar besökare utan att de klickar.

Cyber Kill Chain – Struktur för att förstå steg i en attack: Recon → Weaponize → Deliver → Exploit → Install → C2 → Act.

Spoofing – Falsk identitet (e-post, IP, DNS etc).

Squatting – Domännamn som liknar kända sajter, ofta för phishing.

Zero-day exploits – Okända sårbarheter som utnyttjas innan de patchas.

Privilege escalation – Att få högre rättigheter än man ska ha.

Pivoting – Att använda en komprometterad maskin för att ta sig vidare i ett nätverk.

Backdoors – Dolda åtkomstvägar skapade av utvecklare eller angripare.

Sätt att få tag på information

Utöver social engineering och tekniska attacker finns olika sätt att få tag på lösenord och autentiseringsuppgifter:

Brute force – Testar alla möjliga kombinationer.

Dictionary attack – Testar vanliga lösenord från en ordlista.

Rainbow tables – Förgenererade hash-tabeller för att knäcka lösenord snabbare.

Credential stuffing – Testar läckta lösenord från andra sajter.

Keylogging – Loggar tangenttryckningar.

Sniffing – Avlyssnar oskyddad trafik.

MITM / Man-on-the-side – Kan användas för att få tag på inloggningar.

Shoulder surfing – Tittar över någons axel.

Alla dessa metoder är olika varianter av informationsinsamling – och måste förstås för att byggas skydd mot dem.

9.23.1 Kontrollfrågor

Vad är skillnaden mellan en vit hatt och en svart hatt?

Vad används Kali Linux till?

Hur fungerar ett brute force-angrepp?

Vad är en drive-by-attack?

Hur fungerar pivoting?

Vad gör Metasploit?

Vad är en zero-day-sårbarhet?

Vad innebär spoofing?

Ge exempel på hur en hacker kan använda ett keylogger.

Vad är syftet med bug bounty-program?

9.23.2 Fördjupningslänkar

OWASP – Cyber Kill Chain Explained

Cloudflare – What is a Man-in-the-Middle Attack?

HackerOne – Bug Bounty Programs

Comparitech – What is Typosquatting?

IBM – What is privilege escalation?

9.23.3 Egna anteckningar

(Lämna plats för egna reflektioner och fördjupningar här.)

9.24 Grundläggande säkerhetsprinciper

Att förstå IT-säkerhet handlar inte bara om att förstå hur attacker går till – utan också hur man skapar en kultur och struktur för försvar. Det finns ett antal grundläggande principer som ofta återkommer i all säkerhetsdesign, oavsett om det handlar om att säkra en webbserver, ett Wi-Fi-nätverk eller en hel myndighets IT-system.

9.24.1 Least Privilege (minsta privilegium)

Principen om minsta privilegium handlar om att varje användare, program eller process endast ska ha de rättigheter som absolut behövs för att utföra sin uppgift. Inget mer.

Exempel:

En IT-tekniker behöver kanske tillfälligt administratörsåtkomst för att installera en drivrutin – men bör sedan arbeta med ett vanligt användarkonto.

Ett backup-program bör endast ha läsrättigheter till källfiler – inte rätt att ändra eller ta bort dem.

Syftet är att minimera skada vid intrång. Om en angripare lyckas ta över ett konto eller ett program, ska skadan begränsas av det faktum att kontot/programmet inte hade full behörighet.

9.24.2 Defense in Depth (försvar i flera lager)

Defense in depth handlar om att aldrig förlita sig på ett enda skydd. Istället skapar man flera lager av försvar som samverkar.

Tänk dig en borg: den har murar, vallgravar, vakter, fällor och utrymningsvägar. Samma tänk gäller i IT-säkerhet:

Krypterade hårddiskar

Brandväggar

Antivirus

Intrusion Detection Systems (IDS)

Tvåfaktorsautentisering

Backup

Om ett lager brister ska det finnas fler som tar vid. Detta tänkande är centralt i alla professionella säkerhetsmiljöer.

9.24.3 Security by Design

Security by Design betyder att säkerhet inte ska läggas till i efterhand – den ska vara inbyggd från början. Programvara, system och rutiner ska designas med säkerhet som en naturlig del av arkitekturen.

Exempel:

En webbapplikation ska från start validera all input för att undvika t.ex. SQL-injection.

Ett operativsystem ska vara säkert i standardkonfigurationen, inte först efter timmars justering.

Denna princip har blivit allt viktigare i takt med DevSecOps-modellen, där utveckling, säkerhet och drift samverkar.

9.24.4 Fail Secure / Fail Safe

Vad händer om ett system kraschar? Ska det bli helt öppet – eller helt stängt?

Fail Secure: Systemet går i lås. Ingen kommer in. Prioriterar skydd före tillgänglighet.

Fail Safe: Systemet tillåter viss tillgång. Prioriterar tillgänglighet före skydd.

Båda har sin plats. Ett brandskyddssystem ska vara "fail safe" (alla dörrar öppnas vid brand). Ett bankvalv ska vara "fail secure".

IT-säkerhet behöver båda perspektiven beroende på systemets syfte.

9.24.5 Separation of Duties

Denna princip handlar om att dela upp ansvar mellan olika personer eller roller för att minska risken för missbruk eller fel.

Exempel:

En person får konfigurera backup.

En annan får återställa data.

Ingen ska kunna styra hela kedjan själv, för då kan den personen exempelvis ta bort loggar, dölja spår eller förstöra bevis.

Separation of Duties är vanligt inom ekonomi, revision och nu även inom IT.

9.24.6 Kontrollfrågor

Vad innebär principen om minsta privilegium?

Ge ett exempel på Defense in Depth i praktiken.

Vad menas med Security by Design?

Vad är skillnaden mellan "fail secure" och "fail safe"?

Varför är Separation of Duties viktig inom IT-säkerhet?

Hur kan principen om minsta privilegium förhindra större skador vid ett intrång?

Hur fungerar Defense in Depth i en vanlig hemrouter?

Vad är DevSecOps?

Vilka risker finns med att inte bygga in säkerhet från start?

Vad kan hända om en person har ensam kontroll över alla säkerhetsfunktioner?

9.24.7 Fördjupningslänkar

National Cybersecurity Alliance – Least Privilege Explained

OWASP – Defense in Depth

IBM – Security by Design

Microsoft Learn – Fail Safe vs Fail Secure

SANS Institute – Separation of Duties

9.24.8 Egna anteckningar

(Lämna utrymme för reflektion, minnesanteckningar eller egna exempel.)

9.25 IT-säkerhet på arbetsplatsen – framtid och ansvar

IT-säkerhet är inte längre en fråga för bara IT-avdelningen. I dagens digitala samhälle är varje individ – oavsett yrkesroll – en del av försvarslinjen. Från att klicka på länkar i e-post till att hantera känsliga kunduppgifter på ett korrekt sätt: var och en har ett ansvar.

I det här sista kapitlet ska vi sätta all kunskap i kontext. Hur omsätter man säkerhetsprinciper i vardagen? Vad betyder det att vara en ansvarsfull användare – och en framtida IT-tekniker? Och vad väntar runt hörnet när det gäller hot och teknik?

9.25.1 Praktisk tillämpning av säkerhet

Teori i all ära – men vad innebär det i praktiken?

Lösenordshantering
 Använd starka, unika lösenord – helst med lösenordshanterare. Dela aldrig lösenord, inte ens med kollegor.
Många intrång sker fortfarande på grund av svaga eller återanvända lösenord.

E-postetikett och phishingmedvetenhet
 Granska avsändare, håll muspekaren över länkar innan du klickar, rapportera misstänkt e-post.

Inloggning och sessioner
 Lås datorn när du lämnar arbetsplatsen – även om det bara är för en fika. Logga ut från fjärrsessioner och stäng ned system du inte använder.

Uppdateringar och patchar
 Säkerhetshål lagas hela tiden – men fungerar bara om uppdateringar faktiskt installeras. Detta gäller allt från operativsystem till appar och tillägg i webbläsaren.

9.25.2 Det personliga ansvaret

I många fall är det mänskliga misstag – inte tekniska brister – som leder till dataintrång. Därför måste säkerhetskultur vara levande.

Alla som arbetar med IT eller digitala system har ett ansvar:

Att följa policys och rutiner

Att rapportera avvikelser och misstänkta händelser

Att inte klicka “bara för att det går”

Att säga ifrån vid dålig praxis

Ett exempel: Om du ser att en kollega använder en post-it med lösenord – säg till! Det är inte att vara besvärlig – det är att vara proffsig.

9.25.3 Vanliga misstag – och hur man undviker dem

Några klassiker som fortfarande dyker upp:

Samma lösenord överallt

Dela konto för att det är "lättare"

Inaktiva konton som aldrig tas bort

USB-stickor som tappas bort utan kryptering

Slumpmässig användning av molntjänster utan IT-avdelningens vetskap (s.k. Shadow IT)

Tips: Se alltid till att det finns en balans mellan användarvänlighet och säkerhet – inte ett motsatsförhållande.

9.25.4 Etik, lagstiftning och professionellt ansvar

IT-säkerhet är inte bara teknik – det är också lag och moral. I arbetslivet gäller:

GDPR – du får inte behandla personuppgifter hur som helst.

Säkerhetslagen – vissa verksamheter är samhällsviktiga och omfattas av särskilda krav.

Offentlighetsprincipen – i myndigheter är mycket dokumentation tillgänglig för allmänheten.

Sekretessavtal – många arbetsplatser kräver att du skriver under sekretessklausuler.

Men även där lagen är tyst – finns etiken. Vad är rimligt? Vad är rätt?
En duktig tekniker ställer frågan: "Bara för att jag kan – betyder det att jag bör?"

9.25.5 Framtidens säkerhet – nya hot och möjligheter

IT-säkerhet står aldrig stilla. Här är några områden att hålla ögonen på:

AI (Artificiell Intelligens)
AI används både för att upptäcka attacker snabbare – men också av angripare för att skapa mer avancerade phishingmejl eller bryta mönster.

IoT (Internet of Things)
Från kaffemaskiner till industrimaskiner – alla är uppkopplade, men få är säkrade.

Kvantdatorer
Inte ett hot i dag – men kan i framtiden knäcka dagens krypteringsalgoritmer. Post-quantum-krypto är redan under utveckling.

Smarta städer
 När trafikljus, elnät och vattenförsörjning blir digitala – måste säkerheten följa med.

9.25.6 Riktiga incidenter – vad kan vi lära oss?

Här är tre verkliga händelser att reflektera kring:

Maersk och NotPetya (2017)
 Ett ransomwareangrepp lamslog logistikjätten Maersk. Orsak: En ouppdaterad programvara i ett kontor i Ukraina. Totalkostnad: Uppemot 10 miljarder kronor.

Sony Pictures (2014)
 Angrepp från en nationell aktör (Nordkorea) efter en film. Stora mängder interna dokument läckte. Lärdom: Säkerhet är också geopolitik.

MyFitnessPal (Under Armour, 2018)
 150 miljoner konton läckte. Användarnas e-postadresser, hashade lösenord och användarnamn kom ut. Lärdom: Även "oskyldiga" appar bär ansvar för dataskydd.

9.25.7 Sammanfattning – säkerhet är allas ansvar

När eleverna lämnar skolbänken för att börja arbeta kommer de att ha en nyckelroll: som användare, tekniker, utvecklare – och försvarare av information.

Det räcker inte med brandväggar och antivirus. Det krävs människor som förstår, ifrågasätter och agerar.

Så fråga dig själv:
Vad tar du med dig från det här kapitlet? Från hela kursen?

Ditt ansvar börjar här.

9.25.8 Kontrollfrågor

Vad menas med “säkerhetskultur” på en arbetsplats?

Vad är ett exempel på Shadow IT och varför är det ett problem?

Vilka lagar påverkar dig som IT-ansvarig i en organisation?

Vad är risken med att använda samma lösenord överallt?

Vad är skillnaden mellan GDPR och Säkerhetslagen?

Hur kan AI användas både för och emot IT-säkerhet?

Vad innebär begreppet “etiskt ansvar” i IT-sammanhang?

Vad lärde vi oss av Maersk-attacken?

Hur påverkar IoT vår syn på säkerhet?

Varför är det viktigt att även “småsaker” som USB-stickor hanteras säkert?

9.25.9 Fördjupningslänkar

MSB – Informationssäkerhet i praktiken

European Union Agency for Cybersecurity (ENISA)

Cybersecurity & Infrastructure Security Agency (CISA) – Tips för arbetsplatser

CNIL (Frankrike) – GDPR Explained

OWASP – Future Threats

9.25.10 Egna anteckningar

(Lämna plats för reflektion, tankar och exempel från egna erfarenheter.)

