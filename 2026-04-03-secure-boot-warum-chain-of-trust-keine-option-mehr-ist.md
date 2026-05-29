---
title: "Secure Boot — warum Chain of Trust keine Option mehr ist"
author: "Rouhollah Hosseini"
published: "2026-04-03 07:30"
created: "2026-04-02 20:09"
source: "LinkedIn Newsletter — CRA in Practice"
source_url: "https://www.linkedin.com/in/rouhollah-hosseini-cra/"
lang: "de-en"
---

# Secure Boot — warum Chain of Trust keine Option mehr ist

Secure Boot — warum Chain of Trust keine Option mehr ist

Secure Boot wird oft als Feature behandelt. Eine Einstellung im Bootloader, die man aktiviert — oder auch nicht.

Der Cyber Resilience Act behandelt es anders. Anhang I, Teil I beschreibt Security by Design als Grundanforderung — und Chain of Trust ist eines der konkretesten Beispiele dafür, was das in Embedded-Systemen bedeutet.

Was Secure Boot wirklich bedeutet

Secure Boot ist kein einzelner Schalter. Es ist eine Kette kryptografischer Vertrauensanker — vom ersten ausgeführten Code bis zum laufenden Betriebssystem.

Jede Stufe dieser Kette verifiziert die nächste:

ROM Bootloader

→ prüft U-Boot mit öffentlichem Schlüssel aus eFuse oder TPM

U-Boot / SPL

→ prüft den Linux Kernel mit Herstellersignatur

Linux Kernel

→ verifiziert das Root Filesystem vor dem Mount

Root Filesystem

→ nur signierte, integere Software wird ausgeführt

Bricht eine Stufe die Verifikation — stoppt das System. Kompromittierter Code kommt nicht in den Betrieb.

Die vier Säulen einer CRA-konformen Implementierung

Erstens:

Hardware Root of Trust.

TPM, eFuse oder HSM als Vertrauensanker — nicht Software, sondern Hardware, die nicht überschrieben werden kann.

Zweitens:

Kryptografische Signierung.

Jede Boot-Stufe wird mit einem privaten Schlüssel des Herstellers signiert. Nur was verifiziert werden kann, wird ausgeführt.

Drittens:

Schlüsselmanagement.

Die Signing-Keys müssen sicher verwaltet werden — mit Zugangskontrolle, Rotation und Widerrufsmöglichkeit. Kompromittierte Keys bedeuten kompromittierte Produkte.

Viertens:

Rollback Protection.

Downgrade-Angriffe müssen verhindert werden. Ein Angreifer, der ein Gerät auf eine unsichere ältere Version zurücksetzen kann, umgeht alle neueren Patches.

Yocto — Secure Boot in der Praxis

Die Werkzeuge existieren. Was oft fehlt: ein dokumentierter Prozess für Schlüsselgenerierung, -verwaltung und -rotation — der beim CRA-Audit vorgelegt werden muss.

Was der CRA konkret verlangt

Anhang I, Teil I fordert nicht nur die Implementierung von Secure Boot — sondern den Nachweis, dass Security by Design im Entwicklungsprozess verankert ist. Das bedeutet: Dokumentation der Schlüsselinfrastruktur, Testprotokolle für jede Boot-Stufe, und ein nachvollziehbarer Update-Prozess für Signing-Keys.

Wer Secure Boot heute als Checkbox behandelt, wird beim Audit scheitern. Wer es als Prozess versteht, hat eine belastbare Grundlage.

𝐈𝐜𝐡 𝐛𝐢𝐧 𝐑𝐮𝐡𝐨𝐥𝐥𝐚𝐡 — und hier teile ich meine Erfahrungen rund um Open-Source-Software, Embedded-Produkte und die praktischen Herausforderungen des Cyber Resilience Act.

#CRA #SecureBoot #EmbeddedLinux #Yocto #SecurityByDesign #ChainOfTrust #ProductSecurity #CyberResilienceAct

---
*Originally published in [CRA in Practice](https://www.linkedin.com/newsletters/cra-in-practice/) by Rouhollah Hosseini — [cra-ready.de](https://www.cra-ready.de)*
