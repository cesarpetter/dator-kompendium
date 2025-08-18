# TODO – Dator-kompendier
_Senast uppdaterad: 2025-08-18_

## Gemensamt
- [ ] **Bildreferenslista** (alla bilder, källa/URL, licens) för båda böckerna.
- [ ] **Bildtexter** under varje bild.
- [ ] Skapa en tydlig **“Downloads”**-sektion på sajten (Robin gör).
- [ ] Lägga in ett kort avsnitt om hur materialet får användas (CC BY-NC-SA) på respektive startsida.

---

## Datorteknik (bok)
- [ ] **Kapitel 1 – Hårdvara**
  - [ ] Minska upprepningar (CPU/GPU, cache nämns flera gånger).
  - [ ] Märk praktiska råd som **Tips** (t.ex. PSU 20–30 % marginal).
  - [ ] Förtydliga att SLI/CrossFire är mest **historik** idag.

- [ ] **Kapitel 2 – Uppstart/CPU m.m.**
  - [ ] Kortare nivå på detaljer (t.ex. CS/IP-register) eller markera som *Fördjupning*.
  - [ ] Lägg in **visualisering av boot-sekvens**.
  - [ ] Dela upp några längre meningar (t.ex. 2.11.2) för bättre läsrytm.

- [ ] **Kapitel 3 – Virtualisering**
  - [ ] Tydlig jämförelse **VM vs container** (ev. mini-tabell).
  - [ ] Poängtera att **hosted hypervisors** är bra för elevdatorer hemma (VirtualBox).
  - [ ] En enkel **figur**: Typ 1 vs Typ 2.

- [ ] **Kapitel 4 – Lagring**
  - [ ] Förtydliga **partition vs volym** med konkret exempel.
  - [ ] Kort stycke om **NVMe/M.2 på moderkortet** (var sitter det?).
  - [ ] Fler **skolnära exempel** (SSD på klienter, HDD i backupservrar).

- [ ] **Kapitel 5 – Windows**
  - [ ] Fler **hands-on-exempel** (aktivera SMB, WSL, nätverk).
  - [ ] Skillnad **Home vs Pro** (vilken används i skolmiljö).
  - [ ] Kort stycke **Windows-säkerhet** (brandvägg, konton, UAC).

- [ ] **Kapitel 6 – Nätverk i Windowsmiljö**
  - [ ] Ta med **Workgroup-exemplet** (Bob stänger av sin dator ⇒ resurser otillgängliga).
  - [ ] **AD-diagram** (domän, OU, användare, datorer, grupper).
  - [ ] Nämn att lokala konton ibland används även i domän (felsökning).

- [ ] **Kapitel 7 – Linux (placeholder)**
  - [ ] (Fyll på när du går igenom kapitel 7.)

---

## Nätverk (bok)
- [ ] **Bilder** (några kvar).
- [ ] **Bildreferenslista**.
- [ ] **Bildtexter**.

- [ ] **Kapitel 8 – OSI**
  - [ ] Extra stycke: “**Använd OSI i felsökning**” (ping? syns MAC? når jag DNS?).
  - [ ] Kort lista med **lager 1–7** med exempel.
  - [ ] Lägg till **figur av OSI-modellen**.

- [ ] **Kapitel 9 – IT-säkerhet**
  - [ ] Nämn **CIA-triaden** tidigt.
  - [ ] Ta upp **segmentering** (gästnät, minimalt öppna portar).
  - [ ] Exempel på **applikationssäkerhet** i skolan (webb-plugins).
  - [ ] Praktiska råd: **stäng av WPS**, hur man vet vilket skydd man har hemma.
  - [ ] Kort förklaring **TKIP vs AES**.
  - [ ] Tabell över **kontotyper** (Standard/Admin/Gäst/Microsoft-konto).
  - [ ] Kort om **Group Policy** och vad man kan styra (lösenordspolicy, programblockering).
  - [ ] Exempel på **chmod/chown** och `ufw allow 22/tcp`.
  - [ ] Exempel på känd exploit p.g.a. missade uppdateringar (**WannaCry**).
  - [ ] Kort stycke: **risker med automatiska uppdateringar** i servermiljö.
  - [ ] Nämn **RBAC** som nästa nivå.
  - [ ] Visa vad som händer **utan sudo** (“Permission denied”).
  - [ ] Förstärk koppling **loggning ↔ incidenthantering**.
  - [ ] Litet exempel på `journalctl -xe`.
  - [ ] Nämn **fail2ban** där det passar.
  - [ ] Mini-ordlista: **TLS-handshake**, **cipher suite**, **Diffie-Hellman**.
  - [ ] Tydligare **svensk lagstiftning**: Brottsbalken, **GDPR**, **NIS2**.
  - [ ] **Case-exempel**: virusinfektion på elevdator (incidentflöde).
  - [ ] Kort om **supply chain-attacker** (SolarWinds).
  - [ ] **IDS vs IPS** – tydlig jämförelse.
  - [ ] Exempel på **incidentprotokoll** (mall).
  - [ ] Svenska incidentexempel (Vårdguiden, Transportstyrelsen).
  - [ ] **Log retention** och GDPR-perspektiv.
  - [ ] Nämn **Red team / Blue team**.
  - [ ] Framtid: **EU AI Act**, kommande cybersäkerhetsdirektiv.
