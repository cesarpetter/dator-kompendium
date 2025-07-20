# Dator-kompendium

Kursmaterial för IT-elever på gymnasiet – skrivet av Robin Bräck.

Syftet med detta material är inte att täcka kursen fullständigt utan som ett teoretiskt komplement. Mycket av undervisningen inom it bör utföras genom learning by doing
varvid det kommer att kompletteras med ett antal olika labbar och övningar per kapitel.
Dessa kommer vara en separat bok.

Allt material är ursprungligen mina antecningar och kompendier som jag har delat ut till eleverna. Allt detta matades in i Chat GPT och detta är resultatet

👉 https://github.com/cesarpetter/dator-kompendium/blob/main/docs/datorteknik/datorteknik-draft-med%20kommentarer.pdf

# Swisha till mig 🙌

Vill du stötta mitt arbete eller visa uppskattning? Då kan du enkelt swisha genom att klicka på länken nedan – eller scanna QR-koden med din mobil. Alla bidrag kommer oavkortat gå till kaffe...

## 📱 Direktlänk till Swish

[👉 Klicka här för att öppna Swish swish://payment?payee=0735008888&message=Tack%20för%20ditt%20jobb

> _OBS: Länken fungerar bara på enheter med Swish installerat._


## 🔍 Scanna QR-koden

Om du hellre vill använda QR-kod – scanna bilden nedan i din Swish-app:

![Swish QR-kod](swish.png)


## 📥 Ladda ner QR-koden

Vill du spara QR-koden till mobilen eller skriva ut den?

[📎 Klicka här för att ladda ner QR-koden](swish.png)

---

_Tack för ditt stöd!_

# To-do list
1. En uppsjö av bilder och diagram kommer att kompletteras
   
# Avklarat
<s>2. Uppdateringar som skall göras till innehållet (Chat GPT:s feedback)

  Kapitel 1. Förbättringspotential:
Några avsnitt är något repetitiva i uttryck, t.ex. beskrivningar av CPU- eller GPU-egenskaper som överlappar (t.ex. cache nämns flera gånger).
Ibland blandas faktapresentation med tips/förslag ("satsa på 20–30 % mer effekt i PSU") – det är bra, men kan markeras tydligare som praktiskt tips.
I GPU-avsnittet hade det varit bra att särskilt markera att SLI/CrossFire idag är mer historiskt – eventuellt kortare för att inte överbetona utdaterad teknik.

  Kapitel 2. Förbättringspotential:
Flera tekniska begrepp förklaras noggrant, men vissa avsnitt (t.ex. CS/IP-registret i CPU:n) kanske går lite djupt för en genomsnittlig elev – kan kortas eller märkas som fördjupning.
Inga exempelbilder eller visualiseringar av boot-sekvens nämns – det hade varit ett fint komplement (kan läggas till senare i layoutfas).
Några meningar är långa och skulle kunna delas upp för tydligare läsrytm (exempel i 2.11.2).

  Kapitel 3. Förbättringspotential:
Skillnaden mellan VM och container är viktig – kanske förtjänar 1–2 meningar extra eller en jämförande tabell/bullet-rad i text.
Avsnittet om hosted hypervisors kan lyfta tydligare att dessa är utmärkta för elevernas egen praktik (t.ex. VirtualBox hemma).
Ingen visuell översikt över skillnader mellan typ 1 och typ 2 – ett diagram eller bildstöd kan vara ett bra tillägg framöver.

  Kapitel 4. Förbättringspotential:
Skillnaden mellan volym och partition är rätt svår för många elever – det skulle kunna förtydligas med en konkret jämförelse eller mini-exempel (t.ex. "en partition kan vara 100 GB, men den formateras till en NTFS-volym").
Avsnittet om NVMe och M.2 är tekniskt korrekt men kunde dra nytta av ett litet "så här ser det ut på moderkortet"-stycke eller beskrivning i ord.
Det saknas (än så länge) exempel på användningsområden i skolans miljö – t.ex. varför du kanske vill ha SSD i elevernas datorer men HDD i backupservrar.

  Kapitel 5. Förbättringspotential:
Vissa delar (t.ex. 5.5) kan upplevas lite korta jämfört med övriga kapitel – kanske kunde innehålla fler exempel eller övningsförslag (t.ex. konfigurera nätverk, aktivera SMB, installera WSL).
I installationsdelen vore det bra att nämna skillnaden mellan Home/Pro (vilken version som är vanligast i skolmiljö).
Ett tydligare stycke om säkerhet i Windows (utöver IT-säkerhetskapitlet) hade kunnat finnas här, särskilt om t.ex. brandvägg, kontohantering eller UAC.

  Kapitel 6. Förbättringspotential:
Arbetsmiljöexemplet med Bob som stänger av sin dator (från tidigare diskussion) bör kanske bakas in här om det inte redan är gjort – det illustrerar skillnaden mot domän väldigt bra.
AD-avsnittet skulle kunna lyftas med ett diagram eller punktlista som visar ett typiskt AD-träd (med domän, OU, användare, datorer, grupper).
Värt att nämna kort att elever ibland arbetar med lokala användarkonton på klienter även i domänmiljöer, särskilt vid felsökning.

  Kapitel 7. Förbättringspotential:


  Kapitel 8. Förbättringspotential:
Kapitlet är lite kortare än de andra – inte fel i sig, men ett till stycke om "hur man använder OSI vid felsökning" (t.ex. ex: "kan jag pinga?", "ser jag MAC-adressen?", "nås DNS?") hade kunnat ge ytterligare praktisk koppling.
Lager 1–7 nämns inte som lista eller strukturerat begrepp, vilket vissa elever kan sakna – detta kommer kanske i din arbetsbok, men ett kort avsnitt med exempel (lager 1: kabel – lager 7: webbläsare) hade varit lätt att lägga in här.
Det vore fint att illustrera OSI-modellen med en bild senare i layouten – det gör den mer konkret för visuell inlärning.

  Kapitel 9. Förbättringspotential:
Stycket om "säkerhetsprinciper" kunde kompletteras med CIA-triaden (Confidentiality, Integrity, Availability) – även om det förklaras senare vore det värt att nämna redan här.
Lite repetition i vissa meningar kring varför det är viktigt (”för att skydda…”, ”så att inte…”).

Avsnittet om nätverkssäkerhet är korrekt men lite ytligt – kanske nämna segmentering (t.ex. gästnätverk) eller "minimalt öppna portar" för att visa praktisk tillämpning.
Applikationssäkerhet kunde kompletteras med exempel från skolans värld – t.ex. att inte installera okända plugins i webbläsare.

Övergången mellan protokollbeskrivning och praktiska råd kunde förstärkas – exempelvis: "Hur vet jag vilket skydd jag har hemma?" eller "Hur stänger jag av WPS i routern?"
Kort förklaring av TKIP kontra AES vore välkommen även om det nämns.

En tabell eller punktöversikt över kontotyper (Standard / Admin / Gäst / Microsoft-konto) skulle göra det mer konkret.
Avsnittet nämner ”group policy” men går inte in i detalj – kanske en mening om vad man kan styra, t.ex. lösenordspolicy, programblockering etc.

Skulle vinna på att visa ett konkret exempel på chmod, chown eller ufw allow 22/tcp – om inte här så i arbetsboken.
Övergången mellan grundläggande rättigheter och tjänstloggning kunde kanske förtydligas med underrubrik eller övergångsmening.

Kunde kompletteras med ett kort exempel på ett känt exploit som berodde på en missad uppdatering (ex: WannaCry).
En kort sektion om risker med automatiska uppdateringar i servermiljöer hade också varit ett bra tillskott.

Exempel på rollbaserad åtkomstkontroll (RBAC) kan kort nämnas som "nästa nivå".
Att visa exempel på vad som händer utan sudo (t.ex. "Permission denied") hade gjort det ännu mer praktiskt.

Möjligen kunde sambandet mellan loggning och incidenthantering förstärkas.
Ett skärmutklipp eller exempel på en journalctl -xe-logg i arbetsboken skulle höja kapitlet ytterligare.

Kunde kort nämna fail2ban igen här, om det inte redan gjorts.
En ordlista för begrepp som "TLS-handshake", "cipher suite", "diffie-hellman" i arbetsboken vore klockrent.

Under juridik/regelverk vore det fint att nämna svensk lagstiftning tydligare (ex: brottsbalken, GDPR och NIS2).
Ett case-exempel på en incident (t.ex. virusinfektion på en elevdator) kunde vara ett konkret tillägg till 9.15.5.

Skulle kunna nämna supply chain-attacker som ett växande problem (ex: SolarWinds).

En jämförelse mellan IDS och IPS kunde hjälpa till att konkretisera skillnaden.

Om det inte redan finns, så skulle ett incidentprotokoll som exempel i arbetsboken vara perfekt här.

Kunna koppla till riktiga exempel från Sverige (ex: Vårdguiden, Transportstyrelsen) för att öka trovärdigheten.

Skulle kunna nämna "log retention" – hur länge man får spara loggar enligt t.ex. GDPR.

Kanske kunde lyfta red team / blue team som koncept?

Möjligen kort nämna framtidens lagstiftning (t.ex. AI Act eller cybersäkerhetsdirektiv inom EU).</s>
  
## Licens

Detta material är licensierat under [Creative Commons BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

📄 Du får:
- Dela och använda materialet fritt
- Anpassa innehållet

Men du måste:
- Ange källan
- Inte använda det kommersiellt
- Dela vidare med samma licens


