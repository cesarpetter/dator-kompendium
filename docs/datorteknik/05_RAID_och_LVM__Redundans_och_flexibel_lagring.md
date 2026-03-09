# 5 RAID och LVM – Redundans och flexibel lagring

Lagring handlar inte bara om hur mycket utrymme man har – utan hur man fördelar det, säkrar det och anpassar det för framtiden. I detta kapitel går vi igenom två tekniker som hjälper till med just det: RAID och LVM.

RAID står för Redundant Array of Independent Disks. Det innebär att man kopplar samman flera hårddiskar för att de ska samarbeta och få antingen högre prestanda, högre säkerhet – eller båda.

Hårdvaru-RAID sker i en RAID-kontroller som sitter på moderkortet eller som separat kort. Operativsystemet ser hela RAID-arrayen som en vanlig disk.

Mjukvaru-RAID sker i operativsystemet (t.ex. i Linux via mdadm). Det är billigare, mer flexibelt, men kan belasta CPU:n mer.