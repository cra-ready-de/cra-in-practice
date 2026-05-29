---
title: "PSIRT Under the CRA: What Management Needs to Own Before September"
author: "Rouhollah Hosseini"
published: "2026-05-15 06:50"
created: "2026-05-15 06:06"
source: "LinkedIn Newsletter — CRA in Practice"
source_url: "https://www.linkedin.com/in/rouhollah-hosseini-cra/"
lang: "de-en"
---

# PSIRT Under the CRA: What Management Needs to Own Before September

PSIRT Under the CRA: What Management Needs to Own Before September

Your IR plan covers your network. Who covers your products?

Most manufacturers selling connected devices in Europe have some form of incident response capability. Almost none have configured it to meet what CRA Article 14 requires — and the gap between the two is not a process gap. It is a legal gap that opens on

11 September 2026

.

For the CRA timeline and all key deadlines:

https://www.cra-ready.de/help/cra-grundlagen/zeitplan-fristen

[Available in

English, German, French, Dutch, Italian, and Polish

. Choose your

preferred language

.]

What Article 14 actually demands

A manufacturer shall notify any actively exploited vulnerability contained in a product with digital elements simultaneously to the CSIRT designated as coordinator and to ENISA, via the Single Reporting Platform under Article 16.

The reporting timeline is staged. Full details on each deadline and what each report must contain:

https://www.cra-ready.de/help/schwachstellenmanagement/meldepflichten-art14

24 hours:

Early warning — confirm active exploitation is occurring. Product identity and affected member states if known. No root cause required at this stage.

72 hours:

Full vulnerability notification — severity, affected versions, initial mitigation if available.

14 days:

Final report after a corrective measure becomes available — root cause, fix details, preventive measures.

Three things about this that management needs to understand:

"Simultaneously."

The notification goes to your national CSIRT and ENISA at the same time, through one platform. Submit once; routing is automatic. The ENISA Single Reporting Platform will be operational by 11 September 2026, with a testing period before then.

"Becomes aware."

The clock starts when your organisation knows — not when you have confirmed root cause, not when a patch is ready.

"All products."

Article 69(3) is explicit: these obligations apply to all products with digital elements placed on the market before 11 December 2027. A product shipped in 2015 is in scope from September 2026.

What a minimal compliant PSIRT looks like

A PSIRT for CRA purposes is not a team. It is a documented process with named owners and a tested pipeline. Six elements are non-negotiable:

1. A vulnerability intake channel.

CRA Article 13(6) requires manufacturers to have a publicly accessible contact address for vulnerability reports. The standard implementation is a  file combined with a dedicated  address. Without this, you cannot start the 24-hour clock in a defensible way.

How to implement security.txt under Art. 13(6):

https://www.cra-ready.de/help/schwachstellenmanagement/security-txt

2. A triage process with documented severity criteria.

The Article 14 obligation is triggered by two conditions: active exploitation, or a severe incident affecting product security. A severe incident is one that negatively affects the availability, authenticity, integrity, or confidentiality of important data or functions, or introduces malicious code into the product or a user's network. Your triage must distinguish these categories in writing, before an incident occurs.

3. Your designated CSIRT identified.

The manufacturer's main establishment in the Union is the Member State where decisions related to product cybersecurity are predominantly taken. For German manufacturers, that is BSI. This determines which endpoint you use on the Single Reporting Platform.

4. An ENISA SRP account and tested submission flow.

A testing period precedes the mandatory start date. Use it. A first submission under live conditions, with a 24-hour deadline running, is not the time to discover a configuration problem.

5. An affected-user notification process.

After becoming aware of an actively exploited vulnerability or severe incident, the manufacturer must inform affected users about the vulnerability and available corrective or mitigating measures. This obligation runs in parallel with the regulatory report — not after it.

6. Report templates prepared in advance.

The early warning is deliberately low-content. Prepare the template now. Hour 23 is not when you want to be deciding what format a compliance report takes.

The management accountability question

The CRA is product-centric, not organisation-centric. That is what makes it structurally different from NIS2 or GDPR. A PSIRT programme that lives entirely within an IT security team will not satisfy Article 14 — because the obligations attach to the product and its manufacturer, not to an internal IT system.

Who is in scope under the CRA:

https://www.cra-ready.de/help/cra-grundlagen/geltungsbereich

Someone in your organisation needs documented answers to these questions:

→ Which of our products are in scope under CRA Reg. 2024/2847? → Which product versions are currently on the EU market? → Who is the designated reporter for each product line? → Have we registered on the ENISA SRP? → What is our 24-hour escalation path for a discovery at 02:00 on a Saturday?

If those questions have no written answers today, the gap is a management gap — not an engineering one.

What this has to do with September

Article 14's vulnerability reporting obligations take effect from

11 September 2026

. CRA non-compliance can trigger administrative fines of up to €15 million or 2.5% of worldwide annual turnover. Micro-enterprises and small enterprises are exempt from fines for failures to meet the 24-hour deadline — but not from the reporting obligation itself. The process must exist regardless of company size.

The Dirty Frag disclosure last week illustrated what a bad week looks like without a PSIRT pipeline: a public PoC, an actively exploitable kernel vulnerability, and a 24-hour clock running before most embedded teams had opened a triage ticket.

That scenario is now the legal baseline.

Further reading on

cra-ready.de

:

[Available in

English, German, French, Dutch, Italian, and Polish

. Choose your

preferred language

.]

→ CRA timeline and deadlines:

https://www.cra-ready.de/help/cra-grundlagen/zeitplan-fristen

→ Art. 14 reporting obligations — full detail:

https://www.cra-ready.de/help/schwachstellenmanagement/meldepflichten-art14

→ security.txt under Art. 13(6):

https://www.cra-ready.de/help/schwachstellenmanagement/security-txt

→ Who is in scope:

https://www.cra-ready.de/help/cra-grundlagen/geltungsbereich

→ What is the CRA:

https://www.cra-ready.de/help/cra-grundlagen/was-ist-cra

𝑰 𝒂𝒎 𝑹𝒖𝒉𝒐𝒍𝒍𝒂𝒉 — sharing my experience around the practical challenges of the Cyber Resilience Act - CRA.

📩 Subscribe:

https://lnkd.in/ehbuzd3F

PS: ⚖️ The contents of this Page are for general information purposes only and do not constitute legal advice.

#CRA #PSIRT #Article14 #VulnerabilityManagement #CyberResilienceAct #ProductSecurity #ENISA #EmbeddedLinux #IndustrialSecurity #Compliance

---
*Originally published in [CRA in Practice](https://www.linkedin.com/newsletters/cra-in-practice/) by Rouhollah Hosseini — [cra-ready.de](https://www.cra-ready.de)*
