---
title: 4 – Lagring
nav_order: 3
---

# 4 – Lagring

4.1 Vad är lagring?

Lagring är grunden för hur vi sparar och organiserar data på datorer och andra enheter. All information – operativsystem, appar, dokument och bilder – behöver någon form av lagringsmedia. Det kan vara allt från hårddiskar och SSD:er till USB-minnen och SD-kort.

I det här kapitlet går vi igenom några viktiga begrepp:

Disk (fysisk enhet)

Partition och partitionstabell (MBR/GPT)

Volym och filsystem (FAT32, exFAT, ext4, NTFS, APFS)

Enhet i Windows (enhetsbokstäver)

4.2 Disk – den fysiska enheten

En disk är den faktiska hårdvaran som lagrar data. Det kan vara:

Mekanisk hårddisk (HDD)

Solid State Drive (SSD)

USB-minne

SD-kort

🗂️ Ikea-liknelsen

Disken är som själva garderoben (PAX-stommen). Det är det fysiska skalet som allt annat sitter i.

4.3 Partition och partitionstabell

En disk kan delas upp i partitioner. Partitionen är en avgränsad del av disken som kan användas som en separat enhet. För att datorn ska veta hur partitionerna är upplagda används en partitionstabell.

De två vanligaste partitionstabellerna är:

MBR (Master Boot Record)

Äldre standard

Max 4 primära partitioner

Max 2 TB per disk

Sårbar: all information om diskens struktur lagras i en liten MBR-del – blir den förstörd kan allt gå förlorat

GPT (GUID Partition Table)

Nyare standard

Nästan obegränsat antal partitioner

Stöd för mycket större diskar

Inbyggd redundans (lagrar flera kopior av partitionstabellen)

📚 Biblioteksliknelsen

MBR är som en ensam bibliotekarie som vet var alla böcker finns. Om hon blir sjuk (eller får "virus") blir det kaos – ingen annan har koll.

GPT är som ett bibliotek med många bibliotekarier. Även om några faller bort finns alltid fler som vet var allt finns.

4.4 Volym och filsystem

En volym är det som operativsystemet ser som en "disk". Volymen skapas ovanpå en partition och har ett filsystem som strukturerar hur filer och mappar sparas.

Vanliga filsystem:

FAT32

Stöd på nästan alla enheter

Max filstorlek: 4 GB

Bra för kompatibilitet, men begränsningar för stora filer

exFAT

Nyare variant

Inga praktiska filstorleksgränser för vanliga behov

Bra för USB-stickor mellan Windows och Mac

NTFS

Windows-standard

Stöd för stora filer

Rättigheter och journalföring

ext4

Vanligt i Linux

Stabilt, snabbt, bra för servrar

APFS

Apples filsystem för macOS

Modern funktionalitet: snapshot, kryptering

🗂️ Ikea-liknelsen – lådor och fack

Partitionen är som lådorna eller stången i garderoben. Du bestämmer hur du vill dela in din garderob.

Volymens filsystem är som insatser i lådan. Om lådan är uppdelad i små fack (FAT32) kan du inte lägga ner en enorm filt på 6 GB – den får inte plats. Men med större fack (exFAT, NTFS) går det bra.

4.5 Enhet i Windows – enhetsbokstav

I Windows får varje volym en enhetsbokstav (C:, D:, E: osv.). Det är Windows sätt att identifiera enheter. För att kunna användas måste enheten ha en bokstav tilldelad.

På Linux/macOS används istället monteringspunkter i filsystemsträdet, t.ex. /mnt/usb.

4.6 Sammanfattning

Disk: den fysiska lagringsenheten

Partition: en del av disken, definierad i partitionstabellen (MBR/GPT)

Volym: en partition med filsystem

Filsystem: bestämmer hur filer organiseras

Enhet (Windows): tilldelas enhetsbokstav

4.7 Fördjupningslänkar

Partitioning explained (How-To Geek):

MBR vs GPT (Microsoft Docs):

Filesystems explained (DigitalOcean):

NTFS vs FAT32 vs exFAT (Lifewire):

Apple's APFS Overview:

4.8 Diskussions- och kontrollfrågor

Vad är skillnaden mellan en disk och en partition?

Vad används en partitionstabell till?

Förklara med egna ord MBR:s begränsningar.

Vad är en fördel med GPT jämfört med MBR?

Ge ett exempel på när FAT32 kan vara ett dåligt val.

Vad är ett filsystem och varför behövs det?

Nämn två skillnader mellan exFAT och FAT32.

Vilket filsystem är standard på Windows-datorer?

Vad är enhetsbokstäver i Windows och varför behövs de?

Hur skiljer sig monteringspunkter i Linux/macOS från enhetsbokstäver i Windows?

4.9 Egna anteckningar

(Här kan du som elev skriva egna stödanteckningar, exempel eller frågor.)

4.10 RAID och LVM – Redundans och flexibel lagring

Lagring handlar inte bara om hur mycket utrymme man har – utan hur man fördelar det, säkrar det och anpassar det för framtiden. I detta kapitel går vi igenom två tekniker som hjälper till med just det: RAID och LVM.

4.10.1 Lagringsförluster och effektiv användning

För att förstå RAID och LVM är det viktigt att först greppa att det alltid finns en skillnad mellan fysisk kapacitet (den storlek som anges på en hårddisk, t.ex. 2TB) och den tillgängliga kapaciteten som faktiskt kan användas i operativsystemet. En del av utrymmet går förlorat på grund av metadata, filsystemets struktur och olika typer av overhead. I RAID-konfigurationer används dessutom delar av diskarna för redundans och felskorrigering, vilket ytterligare minskar det användbara utrymmet. Operativsystem och filsystem tar plats, och i redundanssystem som RAID förloras också diskar för att skapa säkerhet.

Ett tumregeln är att ca 15% försvinner till overhead. Den effektiva lagringen kan då beräknas med formeln:

Effektiv lagring (Ze):

X * Y * 0,85

Där:

X = storlek på varje disk

Y = antal diskar som används för lagring (ej paritet/spegling)

Om du vill veta hur mycket du behöver köpa för att få ett visst utrymme, använd: Ze / 0,85 = X * Y

4.10.2 Vad är RAID?

RAID står för Redundant Array of Independent Disks. Det innebär att man kopplar samman flera hårddiskar för att de ska samarbeta och få antingen högre prestanda, högre säkerhet – eller båda.

RAID med mjukvara eller hårdvara

Hårdvaru-RAID sker i en RAID-kontroller som sitter på moderkortet eller som separat kort. Operativsystemet ser hela RAID-arrayen som en vanlig disk.

Mjukvaru-RAID sker i operativsystemet (t.ex. i Linux via mdadm). Det är billigare, mer flexibelt, men kan belasta CPU:n mer.

4.10.3 RAID-nivåer

RAID 0

Striping utan redundans. Alla diskar skrivs till samtidigt, vilket ger hög prestanda, men om en disk går sönder förlorar du allt.

Effektiv lagring: n * X * 0,85

Fördelar: Snabbt

Nackdelar: Ingen säkerhet

RAID 1

Spegling. Varje disk har en exakt kopia. Om en disk går sönder tar den andra över.

Effektiv lagring: (n / 2) * X * 0,85

Fördelar: Säkerhet

Nackdelar: Hälften av utrymmet försvinner

RAID 5

Striping med paritet. En disk används för felskorrigeringsdata. Klarar att en disk kraschar.

Effektiv lagring: (n - 1) * X * 0,85

Fördelar: Bra balans mellan prestanda och säkerhet

Nackdelar: Kan vara segt vid återuppbyggnad

RAID 6

Som RAID 5, men med två paritetsdiskar. Klarar att två diskar kraschar samtidigt.

Effektiv lagring: (n - 2) * X * 0,85

Fördelar: Mer säkerhet

Nackdelar: Mindre lagringsyta, lägre skrivprestanda

RAID 10

Kombination av RAID 1 och 0 (först spegling, sedan striping). Hög prestanda och säkerhet, men kräver minst 4 diskar.

Effektiv lagring: (n / 2) * X * 0,85

Fördelar: Snabbt och säkert

Nackdelar: Dyrt

RAID-kombinationer (t.ex. RAID 50, RAID 55)

I vissa fall bygger man RAID "i flera lager". Exempelvis är RAID 50 en kombination av RAID 5 och RAID 0, vilket kan ge högre prestanda men fortfarande ha viss redundans. En typisk konfiguration kan vara två RAID 5-grupper med vardera fyra diskar (8 totalt), som sedan sätts ihop i RAID 0. Då används totalt två diskar till paritet, och sex diskar är tillgängliga för lagring. RAID 55 är två RAID 5-arrayer kopplade i spegling (ovanligt, men möjligt) vilket ger hög redundans men kräver många diskar. I vissa fall bygger man RAID "i flera lager". Exempelvis är RAID 50 en kombination av RAID 5 och RAID 0, vilket kan ge högre prestanda men fortfarande ha viss redundans. RAID 55 är två RAID 5-array kopplade i spegling (ovanligt, men möjligt).

🔹 Tips! RAID är inte en backup. Det skyddar mot diskkrasch, inte mot radering, virus eller brand.

4.10.4 Vad är ZFS?

ZFS är ett avancerat filsystem som också hanterar volymer och redundans, likt RAID. Det utvecklades av Sun Microsystems och används ofta i servrar och NAS:ar. En av de största fördelarna med ZFS är att det kan ersätta både traditionell RAID och LVM i ett och samma system.

ZFS använder "pools" och självreparerande block. Det har inbyggd checksumming, snapshot-funktioner och automatisk korrigering av bitfel.

Vanliga konfigurationer är:

ZFS RAID-Z1 = likt RAID 5

ZFS RAID-Z2 = likt RAID 6

ZFS RAID-Z3 = klarar tre diskkrascher

Fördelar:

Självreparerande

Snapshot-möjligheter

Skalbart och flexibelt

Kan ersätta både RAID och LVM

Nackdelar:

Resurskrävande (RAM!)

Komplicerat att sätta upp

4.10.5 Vad är LVM?

LVM står för Logical Volume Manager. Istället för att direkt skapa partitioner på en fysisk disk, lägger LVM till ett extra lager.

LVM består av:

Fysiska volymer (PV) = t.ex. /dev/sda1

Volymgrupper (VG) = flera PV bildar en VG

Logiska volymer (LV) = själva partitionerna man monterar

🔹 Metafor: Tänk dig ett LEGO-set där du kan bygga om huset (disken) utan att riva allt. Med LVM kan du ändra storlek, lägga till mer lagring och flytta runt utan att ominstallera.

LVM används ofta tillsammans med RAID eller ZFS för att ge ännu större flexibilitet och kontroll över lagringen.

Fördelar:

Flexibilitet

Kan ändra storlek på diskar live

Snapshot-funktioner

Nackdelar:

Lite mer komplext

4.10.6 Exempel från verkligheten

Ubuntu Server: Vid installation kan man välja LVM direkt. Kombinera med RAID via mdadm eller ZFS.

Proxmox: Använder ofta ZFS som grund, för snapshots, replikering och säker lagring.

NAS-lösningar (t.ex. TrueNAS): Använder ZFS som standard.

4.10.7 Kontrollfrågor

Vad står RAID för och vad är syftet?

Hur skiljer sig mjukvaru-RAID från hårdvaru-RAID?

Vad är för- och nackdelar med RAID 0?

Hur fungerar RAID 5 och vad händer om en disk går sönder?

Vad menas med att RAID inte är en backup?

Hur skiljer sig ZFS från traditionell RAID?

Vad är RAID-Z2?

Vad är LVM och vad är fördelen med att använda det?

Vad är en volymgrupp inom LVM?

Ge exempel på någon verklig situation där man använder ZFS.

4.10.8 Fördjupningslänkar

4.10.9 Egna anteckningar

...

