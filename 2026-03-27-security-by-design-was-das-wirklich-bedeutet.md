---
title: "Security by Design — was das wirklich bedeutet"
author: "Rouhollah Hosseini"
published: "2026-03-27 09:01"
created: "2026-03-23 10:05"
source: "LinkedIn Newsletter — CRA in Practice"
source_url: "https://www.linkedin.com/in/rouhollah-hosseini-cra/"
lang: "de-en"
---

# Security by Design — was das wirklich bedeutet

Security by Design — was das wirklich bedeutet

„Security by Design" klingt wie ein Designprinzip aus einem Workshop-Flipchart.

Im Cyber Resilience Act ist es eine gesetzliche Anforderung — verankert in Anhang I, Teil I.

Und die meisten Teams wissen nicht, was das konkret bedeutet.

Was CRA unter Security by Design versteht

Anhang I, Teil I des CRA listet konkrete Anforderungen — keine abstrakten Ziele. Vier davon begegnen mir in der Praxis am häufigsten:

Minimale Angriffsfläche.

Nur Dienste, Ports und Schnittstellen aktivieren, die tatsächlich benötigt werden. Jeder unnötige Einstiegspunkt ist ein potenzieller Angriffsvektor.

Sichere Standardwerte.

Kein Default-Passwort. Kein offener Debug-Port im Produktivbetrieb. Das Produkt muss im Auslieferungszustand sicher sein — nicht erst nach manueller Konfiguration.

Defense in Depth.

Sicherheit darf nicht nur am Perimeter enden. Mehrere unabhängige Schutzebenen stellen sicher, dass ein einzelner Fehler nicht zum vollständigen Kompromiss führt.

Least Privilege.

Jede Komponente, jeder Prozess, jeder Dienst bekommt nur die Rechte, die er für seine Funktion braucht — nicht mehr.

Warum das für Embedded-Teams besonders relevant ist

In industriellen Embedded-Systemen sind diese Prinzipien oft schwerer umzusetzen als in klassischer Software. Legacy-Protokolle, eingeschränkte Hardware-Ressourcen, lange Produktlebenszyklen — all das erhöht den Aufwand.

Genau deshalb muss Security by Design von Anfang an in den Entwicklungsprozess integriert werden. Nachträglich lässt es sich kaum einbauen.

Der CRA macht das zur Nachweispflicht: Hersteller müssen dokumentieren, dass diese Prinzipien im Prozess verankert sind — nicht nur behaupten, dass sie existieren.

𝐈𝐜𝐡 𝐛𝐢𝐧 𝐑𝐮𝐡𝐨𝐥𝐥𝐚𝐡 — und hier teile ich meine Erfahrungen rund um Open-Source-Software, Embedded-Produkte und die praktischen Herausforderungen des Cyber Resilience Act.

#CRA #SecurityByDesign #EmbeddedLinux #ProductSecurity #CyberResilienceAct #IoT #Yocto

---
*Originally published in [CRA in Practice](https://www.linkedin.com/newsletters/cra-in-practice/) by Rouhollah Hosseini — [cra-ready.de](https://www.cra-ready.de)*
