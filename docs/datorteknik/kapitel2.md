---
title: 2 – Uppstart
nav_order: 2
---

# 2 – Uppstart

2.1 Introduktion

När vi slår på en dator startar en noga planerad kedja av steg som till slut laddar operativsystemet i minnet. Den här processen kallas uppstart eller boot och är avgörande för att en dator överhuvudtaget ska fungera.

I det här kapitlet går vi igenom vad som händer tekniskt när datorn startar. Vi tittar på traditionell BIOS och den modernare UEFI, vad de gör, varför de finns och hur bootloaders som GRUB och Windows Boot Manager fungerar.

Vi avslutar med en fördjupning som tar upp historik, detaljerad teknik och Secure Boot.

2.2 Översikt av uppstartssekvensen

När du trycker på strömknappen händer följande i korthet:

Strömförsörjning (PSU) aktiveras och skickar stabil spänning till moderkortet.

CPU:n startar vid en definierad adress och söker efter startkod i firmware.

POST (Power-On Self Test) körs för att testa grundläggande hårdvara.

Firmware (BIOS/UEFI) letar efter en boot-enhet enligt boot-ordningen.

Bootloader från boot-enheten laddas in i minnet.

Bootloadern hittar och laddar operativsystemets kärna.

Operativsystemet tar över och fortsätter startsekvensen.

2.3 Strömförsörjning och CPU-start

2.3.1 Power Supply Unit (PSU)

När strömknappen trycks ned skickar PSU ström till moderkortet. Den skickar en Power Good-signal när spänningen är stabil. Detta signalerar att moderkortet kan starta CPU:n.

2.3.2 CPU:s första steg

En x86-baserad CPU börjar alltid på en välkänd adress. Vid kallstart rensas registren och CPU:n ställs in på:

CS (Code Segment) Selector: 0xF000

IP (Instruction Pointer): 0xFFF0

Adderat som fysisk adress:

CS base: 0xFFFF0000
IP:      0x0000FFF0
---------------------
= 0xFFFFFFF0

Detta är den sista delen av adressrymden – här ligger en jump-instruktion till BIOS/UEFI. CPU:n börjar alltså med att hoppa in i firmware.

2.4 BIOS

2.4.1 Vad är BIOS?

BIOS står för Basic Input/Output System och är firmware lagrad på moderkortets ROM-chip. Den är låg-nivåkod som lever kvar oavsett om hårddisken är tom eller trasig.

2.4.2 Varför finns BIOS?

Syftet är att ge en minimal uppstartsmiljö som kan:

Testa hårdvaran (POST)

Initiera grundläggande I/O (tangentbord, skärm)

Leta upp en startbar enhet (HDD, SSD, USB, CD)

Ladda och överlåta kontrollen till en bootloader

2.4.3 POST – Power-On Self Test

POST är det första som BIOS gör. Det är en serie tester som säkerställer att:

RAM fungerar

CPU fungerar

Grafikkort är åtkomligt

Tangentbord svarar

Eventuella fel signaleras med pipkoder eller blinkande lysdioder. Vid godkänd POST går systemet vidare till nästa steg: att hitta bootenheten.

2.5 Det tekniska bakom BIOS

BIOS är traditionellt lagrat i ROM eller Flash på moderkortet.

Den innehåller bootstrapkod som alltid är tillgänglig.

Den har en boot order som kan konfigureras av användaren för att prioritera exempelvis HDD, SSD, USB eller nätverk.

BIOS använder MBR (Master Boot Record) som partitionstabell på diskar upp till 2 TB.

MBR har en 512-byte bootsektor där en liten del av bootloadern ligger.

2.6 UEFI

2.6.1 Vad är UEFI?

Unified Extensible Firmware Interface (UEFI) är en modernare ersättare för BIOS.

Lagrad i flashminne på moderkortet.

Har grafiskt gränssnitt, musstöd.

Kan läsa större diskar (>2 TB) via GPT (GUID Partition Table).

Har nätverksstöd i firmware.

Kan köra drivrutiner direkt.

2.6.2 Historia och utveckling

UEFI utvecklades från Intel EFI och blev en industristandard i början av 2010-talet. Syftet var att överkomma BIOS-begränsningar:

Större diskar via GPT

Moderna drivrutiner

Modulär design

Snabbare uppstart

2.6.3 Varför är UEFI bättre?

Stöd för >2 TB-diskar

Säkerhetsfunktioner som Secure Boot

Bättre konfigurationsmöjligheter

Stöd för mus och GUI

Snabbare POST och uppstart

2.7 Secure Boot

2.7.1 Vad är Secure Boot?

Secure Boot är en UEFI-funktion som kontrollerar att operativsystemets bootloader är kryptografiskt signerad. Den hindrar obehörig kod från att köras vid uppstart.

2.7.2 Fördelar

Skydd mot rootkits och bootkits

Säker kedja från firmware till OS

Förhindrar obehörig manipulation av bootloadern

2.7.3 Nackdelar

Kan hindra installation av osignerade operativsystem

Kräver certifikatunderhåll (tillverkare kan dra tillbaka certifikat)

Kan behöva inaktiveras för vissa Linux-distributioner eller specialsystem

2.8 Bootloaders

2.8.1 Vad är en bootloader?

En bootloader är ett litet program som firmware laddar från disken. Dess uppgift är att:

Initiera hårddiskläsning

Ladda operativsystemets kärna i RAM

Ge kontrollen till kärnan

2.8.2 Exempel på bootloaders

Windows Boot Manager (BCD-store)

GRUB (Grand Unified Bootloader) för Linux

boot.efi för macOS

2.8.3 Bootloaderns plats

BIOS: MBR (512 byte bootstrap + ~31 KB VBR) pekar vidare

UEFI: EFI-systempartition (ESP) innehåller .efi-filer

2.9 Uppstartssekvenser – exempel

2.9.1 Windows (UEFI)

Ström på → UEFI POST

UEFI läser EFI-partitionen

Laddar bootmgfw.efi

Läser BCD-databas

Laddar winload.efi → Kernel

2.9.2 macOS

UEFI POST

Laddar boot.efi

Laddar XNU-kärnan

2.9.3 Linux (GRUB)

UEFI POST

Laddar grubx64.efi från ESP

GRUB visar meny

Användaren väljer kernel

GRUB laddar vmlinuz och initramfs

Kernel startar

2.10 Vanliga problem

"No bootable device found" – fel boot order

Korrupt bootloader – behöver repareras

Secure Boot-blockering av osignerade OS

Felaktiga partitionstabeller (MBR/GPT-konflikter)

2.11 Fördjupning

2.11.1 BIOS och MBR – tekniskt

MBR är alltid första 512 bytes på disken

Innehåller bootstrap-kod (440 bytes), partitionsschema (64 bytes)

Kan bara ha fyra primära partitioner

Använder CHS/LBA-adressering: CHS (Cylinder-Head-Sector) beskriver disken med dess fysiska geometri, medan LBA (Logical Block Addressing) använder sekventiella blocknummer för att enklare adressera stora diskar.

2.11.2 UEFI och GPT – tekniskt

GPT använder GUID-identifierare

Stöd för nästan obegränsat antal partitioner

ESP (EFI System Partition) lagrar .efi-bootloaders

Variabel lagring i NVRAM

2.11.3 Secure Boot

Microsofts nycklar är förinstallerade på många system

Linux-distributioner signerar bootloaders med dessa nycklar

Kan stängas av i UEFI-inställningar

2.12 Fördjupningslänkar

2.13 Diskussions- och kontrollfrågor

Vad är syftet med POST?

Vad gör BIOS/UEFI för att hitta ett operativsystem?

Vilka tekniska begränsningar har MBR jämfört med GPT?

Vad är skillnaden mellan BIOS och UEFI?

Vad är Secure Boot och vilka för- respektive nackdelar har det?

Hur skiljer sig en bootloader i UEFI från den i ett MBR-system?

Hur fungerar boot-sekvensen i Linux med GRUB?

2.14 Egna anteckningar

(Här kan du som elev skriva egna anteckningar om uppstartsprocessen, BIOS/UEFI, bootloaders eller reflektioner.)

3 Virtualisering

3.1 Vad innebär virtualisering

Virtualisering betyder att man skapar en virtuell version av något som annars är fysiskt. Oftast handlar det om att köra flera virtuella datorer (VM – Virtual Machines) på en och samma fysiska server. Varje VM fungerar som en egen dator med operativsystem och program, men delar resurser som CPU, minne och disk med andra VM på samma hårdvara.

Virtualisering styrs av ett lager som kallas hypervisor. Hypervisorn gör det möjligt att starta, stoppa och hantera virtuella maskiner på ett kontrollerat sätt.

3.2 Varför använder man virtualisering

Virtualisering är en central teknik inom IT-drift och utveckling. Några vanliga anledningar till att använda virtualisering är:

Bättre resursutnyttjande: Flera VM på en fysisk maskin gör att hårdvaran används mer effektivt.

Kostnadsbesparing: Färre fysiska servrar ger lägre kostnader för inköp, el och kyla.

Flexibilitet: Lätt att skapa, ändra eller ta bort VM efter behov.

Isolering: Problem i en VM påverkar inte andra VM.

Test och utveckling: Möjlighet att snabbt skapa testmiljöer.

3.3 Bare-metal hypervisorer

En bare-metal hypervisor (även kallad typ 1-hypervisor) körs direkt på serverns hårdvara, utan att först installera ett värdoperativsystem. Den blir i princip serverns "operativsystem".

3.3.1 Fördelar och nackdelar

Fördelar:

Mycket bra prestanda eftersom hypervisorn har direkt åtkomst till hårdvaran.

Bättre säkerhet och isolering.

Vanligt val i datacenter.

Nackdelar:

Kan vara mer komplex att installera och administrera.

Mindre bra för småskaligt bruk eller på klientdatorer.

3.3.2 Exempel på plattformar

VMware ESXi

Microsoft Hyper-V (Server-installation)

KVM (Linux-baserad)

Proxmox (som vi kommer att arbeta med i kursen)

3.4 Hosted hypervisorer

En hosted hypervisor (typ 2-hypervisor) installeras som ett program på ett vanligt operativsystem (som Windows, macOS eller Linux).

3.4.1 Fördelar och nackdelar

Fördelar:

Enkel att installera och använda.

Bra för labb, utveckling och utbildning.

Kan köras på en vanlig dator.

Nackdelar:

Lite sämre prestanda än bare-metal.

Dubbla lager (värd-OS + hypervisor) kan ge fler attackytor.

3.4.2 Exempel på plattformar

Oracle VirtualBox

VMware Workstation / Fusion

Parallels (för macOS)

3.5 Koppling mot molnet

Många molntjänster bygger på virtualisering i grunden. Stora molnleverantörer som Microsoft Azure, Amazon AWS och Google Cloud Platform använder virtualisering för att kunna erbjuda:

Virtuella servrar (t.ex. Azure Virtual Machines)

Containerplattformar (t.ex. Google Kubernetes Engine)

Serverless-tjänster (t.ex. AWS Lambda)

För kunden betyder det att man inte behöver köpa egen hårdvara utan "hyr" resurser som är virtualiserade i leverantörens datacenter.

3.6 Containrar (kort introduktion)

Containrar är ett annat sätt att paketera och isolera applikationer. Till skillnad från virtuella maskiner delar containrar operativsystemets kärna, vilket gör dem mycket lättare och snabbare att starta.

Exempel på containerplattformar:

Docker

Podman

Kubernetes (för att hantera många containrar)

Containrar används ofta tillsammans med virtualisering eller i molnmiljöer. Det är bra att känna till skillnaden:

Virtuella maskiner emulerar hela hårdvaran och kör ett eget OS.

Containrar delar värd-OS men isolerar applikationen.

3.7 Fördjupande länkar

Här är några länkar för dig som vill läsa mer om virtualisering:

VMware – Vad är virtualisering?

Microsoft Learn – Hyper-V översikt

Proxmox VE – Officiell dokumentation

Oracle VirtualBox – User Manual

Docker – Vad är en container?

3.8 Kontrollfrågor

Vad menas med virtualisering inom IT?

Vad är en hypervisor?

Nämn två fördelar med att använda virtualisering.

Vad är skillnaden mellan en bare-metal hypervisor och en hosted hypervisor?

Ge ett exempel på en bare-metal hypervisor.

Ge ett exempel på en hosted hypervisor.

Vilka är några fördelar med att använda virtualisering i molnet?

Vad är en container, och hur skiljer den sig från en virtuell maskin?

Varför är isolering viktigt när man kör flera system på samma hårdvara?

Nämn en plattform eller tjänst som använder virtualisering i molnet.

3.9 Egna anteckningar

(Lämna plats här i kompendiet för eleverna att själva skriva)

