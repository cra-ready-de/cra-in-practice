---
title: "CRA in der Praxis: Ein ganz normaler Dienstag!"
author: "Rouhollah Hosseini"
published: "2026-03-10 09:11"
created: "2026-03-10 08:59"
source: "LinkedIn Newsletter — CRA in Practice"
source_url: "https://www.linkedin.com/in/rouhollah-hosseini-cra/"
lang: "de-en"
---

# CRA in der Praxis: Ein ganz normaler Dienstag!

CRA in der Praxis: Ein ganz normaler Dienstag!

Es war ein ganz normaler Dienstag.

Ich bin auf eine neue CVE gestoßen. CVSS 9.x. Betrifft eine weit verbreitete Bibliothek — die Art, die man in Dutzenden von Embedded-Targets findet, ohne es genau zu wissen.

Die erste Frage war nicht „wie patchen wir das?" — sondern:

„In welchen Images ist diese Bibliothek überhaupt drin?"

Ohne ein gepflegtes SBOM: Stunden der Suche. Manuelles Durchforsten von Rezepten, Build-Logs, Paketlisten. Mit automatisiertem SBOM-Tracking: Minuten. Ein Befehl, eine Liste, ein klares Bild.

---

Was das mit dem Cyber Resilience Act zu tun hat

Genau das ist der Punkt, den viele beim CRA noch unterschätzen. Es geht nicht nur um Dokumentation für Auditoren oder um ein Häkchen in einer Compliance-Checkliste.

Es geht darum, im Ernstfall — wenn eine kritische CVE auftaucht, wenn ein Kunde fragt, wenn eine Behörde prüft —

handlungsfähig zu bleiben

.

Der CRA verpflichtet Hersteller von Produkten mit digitalen Elementen dazu, Schwachstellen aktiv zu verfolgen, zu melden und zu beheben. Und zwar über den gesamten Lebenszyklus des Produkts. Nicht einmalig beim Release.

---

Was Yocto heute schon kann

Wer Embedded Linux mit Yocto baut, hat die technischen Mittel bereits zur Hand:

— au

tomatischer Abgleich jeder Komponente mit der NVD-Datenbank beim Build.

— SPDX 2.3-konformes SBOM direkt aus dem Build-Prozess.

License Manifests werden ohnehin generiert — sie müssen nur strukturiert ausgewertet werden.

Die Werkzeuge existieren. Was oft fehlt, ist der

strukturierte Prozess drumherum

: Wer ist verantwortlich? Wie wird das SBOM versioniert? Wie fließen CVE-Updates in den laufenden Betrieb ein?

---

Was mich hier beschäftigt

Ich arbeite täglich mit Embedded Linux, Yocto und industriellen Systemen — in einem Umfeld, wo Produktlebenszyklen nicht in Monaten, sondern in Jahren gemessen werden.

Der CRA trifft genau diese Welt. Und er trifft sie härter als viele heute noch glauben.

In dieser Newsletter-Reihe möchte ich teilen, was ich in der Praxis sehe — Herausforderungen, Lösungsansätze, und manchmal auch offene Fragen, auf die es noch keine einfache Antwort gibt.

---

Ich bin Ruhollah — und hier möchte ich meine beruflichen Erfahrungen rund um Herausforderungen und Lösungsansätze bei Open-Source-Software in Embedded-Produkten und im Kontext des Cyber Resilience Act mit euch teilen.

\#CRA #EmbeddedLinux #Yocto #SBOM #CyberResilienceAct #ProductSecurity #OpenSource

---
*Originally published in [CRA in Practice](https://www.linkedin.com/newsletters/cra-in-practice/) by Rouhollah Hosseini — [cra-ready.de](https://www.cra-ready.de)*
