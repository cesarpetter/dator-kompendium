---
title: 8 – OSI-modellen
nav_order: 6
---

# 8 – OSI-modellen

8.1 Uppkomst – Bakgrunden till OSI

När datornätverk började växa fram på 1970-talet fanns det ett stort problem: olika tillverkare och organisationer skapade sina egna sätt att kommunicera mellan datorer. Det fanns inga gemensamma regler eller standarder. En dator från IBM kunde inte självklart prata med en från DEC, och alla skapade sina egna protokoll. Det blev snabbt rörigt.

För att lösa detta började man på 1970-talet att diskutera behovet av en gemensam modell som alla kunde utgå från. Organisationen ISO (International Organization for Standardization) tog initiativet, och 1984 publicerade de vad som kom att kallas OSI-modellen – en förkortning för Open Systems Interconnection. Modellen skulle inte vara ett faktiskt protokoll eller mjukvara, utan en teoretisk referensmodell. Den delade upp nätverkskommunikation i sju lager, där varje lager ansvarar för en specifik del av kommunikationen.

8.2 Syfte – Varför finns OSI-modellen?

OSI-modellen har flera syften, men det främsta är att:

Standardisera kommunikationen mellan olika system och tillverkare

Förenkla felsökning och nätverksdesign genom att tydligt separera olika funktioner

Underlätta utveckling av nätverksprotokoll, eftersom utvecklare kan fokusera på ett lager i taget

Modellen fungerar som ett gemensamt språk. Den hjälper tekniker att beskriva vad som händer i ett nätverk utan att behöva prata om specifika produkter. I stället för att säga "fel på filöverföring via TCP", kan man säga "problemet ligger troligen i transportlagret".

Den ger också en modulär struktur – om ett lager uppdateras (exempelvis ett nytt protokoll), behöver inte övriga lager påverkas. Det möjliggör en mer flexibel och framtidssäker nätverksdesign.

8.3 Användningsområde – Hur används OSI-modellen?

Trots att OSI-modellen är teoretisk, används den dagligen i IT-branschen. Den är ett verktyg för felsökning, utbildning och analys. Exempel på användningsområden är:

Felsökning av nätverk: En tekniker kan börja analysera var ett fel uppstår – är det i applikationen (lager 7), i nätverket (lager 3), eller i kabeln (lager 1)?

Kommunikation mellan IT-personal: Modellen ger en gemensam struktur som gör det lättare att beskriva och förstå problem.

Utbildning: OSI används som pedagogiskt verktyg för att förklara hur data rör sig genom ett nätverk.

Utveckling av protokoll och system: När man designar nya lösningar kan man definiera exakt vilket lager man jobbar med (exempelvis HTTPS som verkar på lager 7).

De sju lagren i OSI-modellen:

Ett vanligt sätt att minnas lagren är med hjälp av minnesregler, exempelvis:

"All People Seem To Need Data Processing" (uppifrån och ner)

"Please Do Not Throw Sausage Pizza Away" (nerifrån och upp)

Exempel: Hur en webbsida skickas via OSI-modellen

När du skriver in en webbadress och trycker Enter i webbläsaren:

Lager 7: Webbläsaren (applikationen) genererar en begäran om en webbsida.

Lager 6: Data kan krypteras med TLS/SSL.

Lager 5: En session skapas mellan dig och webbservern.

Lager 4: Begäran delas upp i segment, och TCP ser till att allt kommer fram i rätt ordning.

Lager 3: IP-protokollet lägger på avsändar- och mottagaradress.

Lager 2: Ethernet lägger till MAC-adresser.

Lager 1: Data skickas som elektriska signaler i nätverkskabeln.

När informationen når mottagaren går den uppåt igen genom lagren, tills webbsidan visas.

8.4 Diskussions- och kontrollfrågor

Vad står OSI för och vilken organisation utvecklade modellen?

Varför behövdes en standardmodell för nätverkskommunikation på 1970-talet?

Nämn tre fördelar med att använda OSI-modellen.

Hur många lager innehåller OSI-modellen och vad heter det översta lagret?

Vad är syftet med transportlagret?

Vad innebär det att OSI-modellen är en "referensmodell"?

Hur används OSI-modellen i felsökning av nätverk?

Vilket lager ansvarar för att hantera IP-adresser?

Ge ett exempel på ett protokoll som verkar på applikationslagret.

Vad är skillnaden mellan lager 1 och lager 2?

8.5 Fördjupningslänkar

Cisco – OSI Model Explained

Cloudflare – What is the OSI Model?

GeeksForGeeks – OSI Model

IBM – OSI Model Overview

CompTIA – OSI Reference Model

8.6 Egna anteckningar

