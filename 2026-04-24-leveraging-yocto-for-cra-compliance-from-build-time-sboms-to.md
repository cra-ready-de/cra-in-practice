---
title: "Leveraging Yocto for CRA Compliance: From Build-Time SBOMs to Technical Dossiers"
author: "Rouhollah Hosseini"
published: "2026-04-24 07:01"
created: "2026-04-23 21:21"
source: "LinkedIn Newsletter — CRA in Practice"
source_url: "https://www.linkedin.com/in/rouhollah-hosseini-cra/"
lang: "de-en"
---

# Leveraging Yocto for CRA Compliance: From Build-Time SBOMs to Technical Dossiers

Leveraging Yocto for CRA Compliance: From Build-Time SBOMs to Technical Dossiers

The introduction of the 𝑪𝒚𝒃𝒆𝒓 𝑹𝒆𝒔𝒊𝒍𝒊𝒆𝒏𝒄𝒆 𝑨𝒄𝒕 (𝑪𝑹𝑨) has sent many manufacturers searching for expensive third-party tools to generate a Software Bill of Materials (SBOM). However, if your stack is built on 𝒀𝒐𝒄𝒕𝒐 𝑷𝒓𝒐𝒋𝒆𝒄𝒕 (𝑲𝒊𝒓𝒌𝒔𝒕𝒐𝒏𝒆 𝒐𝒓 𝒍𝒂𝒕𝒆𝒓), the core engine for compliance is already at your fingertips.

🛠️ 𝐓𝐡𝐞 𝐈𝐧𝐭𝐞𝐫𝐧𝐚𝐥 𝐏𝐚𝐭𝐡: 𝒄𝒓𝒆𝒂𝒕𝒆-𝒔𝒑𝒅𝒙

Generating an SBOM doesnt require manual dependency tracking or external scanners for the basics. By simply adding 𝑰𝑵𝑯𝑬𝑹𝑰𝑻 += "𝒄𝒓𝒆𝒂𝒕𝒆-𝒔𝒑𝒅𝒙" to your configuration, the BitBake build process generates a comprehensive 𝑺𝑷𝑫𝑿 2.3 𝑱𝑺𝑶𝑵 output at build time.

𝐊𝐞𝐲 𝐓𝐞𝐜𝐡𝐧𝐢𝐜𝐚𝐥 𝐂𝐚𝐩𝐚𝐛𝐢𝐥𝐢𝐭𝐢𝐞𝐬:

🟠 𝐀𝐮𝐭𝐨𝐦𝐚𝐭𝐞𝐝 𝐌𝐞𝐭𝐚𝐝𝐚𝐭𝐚: Captures package names, versions, licenses, and checksums directly from the build recipes.

🟢 𝐎𝐮𝐭𝐩𝐮𝐭 𝐓𝐫𝐚𝐧𝐬𝐩𝐚𝐫𝐞𝐧𝐜𝐲: Files are systematically deployed to 𝒕𝒎𝒑/𝒅𝒆𝒑𝒍𝒐𝒚/𝒔𝒑𝒅𝒙/.

🟣 𝐒𝐨𝐮𝐫𝐜𝐞 𝐈𝐧𝐜𝐥𝐮𝐬𝐢𝐨𝐧: Using 𝑺𝑷𝑫𝑿_𝑰𝑵𝑪𝑳𝑼𝑫𝑬_𝑺𝑶𝑼𝑹𝑪𝑬𝑺 = "1" ensures that source code data is documented, fulfilling deep transparency requirements.

🔵 𝐀𝐮𝐝𝐢𝐭-𝐑𝐞𝐚𝐝𝐲 𝐅𝐨𝐫𝐦𝐚𝐭𝐭𝐢𝐧𝐠: Setting 𝑺𝑷𝑫𝑿_𝑷𝑹𝑬𝑻𝑻𝒀 = "1" ensures the JSON is human-readable for internal validation.

⚠️ 𝐁𝐫𝐢𝐝𝐠𝐢𝐧𝐠 𝐭𝐡𝐞 𝐂𝐑𝐀 𝐆𝐚𝐩

It is a common misconception that a build-time SBOM is the final step. While Yocto provides the foundation, the output must be enriched to meet the rigorous BSI TR-03183-2 standards required for a formal Technical Dossier.

𝐖𝐡𝐚𝐭 𝐢𝐬 𝐦𝐢𝐬𝐬𝐢𝐧𝐠 𝐟𝐫𝐨𝐦 𝐚 𝐬𝐭𝐚𝐧𝐝𝐚𝐫𝐝 𝐨𝐮𝐭𝐩𝐮𝐭?

🟠 𝐂𝐏𝐄 𝐈𝐝𝐞𝐧𝐭𝐢𝐟𝐢𝐞𝐫𝐬: Vital for cross-referencing vulnerabilities (CVEs).

🟢 𝐒𝐇𝐀-𝟓𝟏𝟐 𝐇𝐚𝐬𝐡𝐞𝐬: The BSI standard requires higher cryptographic assurance than basic checksums.

🔵 𝐑𝐞𝐥𝐚𝐭𝐢𝐨𝐧𝐬𝐡𝐢𝐩 𝐌𝐚𝐩𝐩𝐢𝐧𝐠: Explicitly defining how dependencies interact within the system.

🚀 𝐒𝐭𝐫𝐚𝐭𝐞𝐠𝐲 𝐟𝐨𝐫 𝐌𝐚𝐧𝐮𝐟𝐚𝐜𝐭𝐮𝐫𝐞𝐫𝐬

A build-time SBOM is a 𝐬𝐭𝐚𝐫𝐭𝐢𝐧𝐠 𝐩𝐨𝐢𝐧𝐭, not the finish line. To remain compliant:

🟠 𝐀𝐮𝐭𝐨𝐦𝐚𝐭𝐞 the baseline using Yocto’s native tools.

🟢 𝐄𝐧𝐫𝐢𝐜𝐡 the data with CPEs and relationship enumerations.

🔵 𝐕𝐚𝐥𝐢𝐝𝐚𝐭𝐞 your final SBOM against 𝐁𝐒𝐈 𝐓𝐑-𝟎𝟑𝟏𝟖𝟑-𝟐 before filing your documentation.

𝗕𝘆 𝘂𝘁𝗶𝗹𝗶𝘇𝗶𝗻𝗴 𝗬𝗼𝗰𝘁𝗼’𝘀 𝗯𝘂𝗶𝗹𝘁-𝗶𝗻 𝗳𝗲𝗮𝘁𝘂𝗿𝗲𝘀, 𝘆𝗼𝘂 𝗰𝗮𝗻 𝘀𝗶𝗴𝗻𝗶𝗳𝗶𝗰𝗮𝗻𝘁𝗹𝘆 𝗿𝗲𝗱𝘂𝗰𝗲 𝘁𝗵𝗲 𝗰𝗼𝗺𝗽𝗹𝗲𝘅𝗶𝘁𝘆 𝗼𝗳 𝗖𝗥𝗔 𝗰𝗼𝗺𝗽𝗹𝗶𝗮𝗻𝗰𝗲 𝗮𝗻𝗱 𝗳𝗼𝗰𝘂𝘀 𝗼𝗻 𝗯𝘂𝗶𝗹𝗱𝗶𝗻𝗴 𝘀𝗲𝗰𝘂𝗿𝗲, 𝗿𝗲𝘀𝗶𝗹𝗶𝗲𝗻𝘁 𝗽𝗿𝗼𝗱𝘂𝗰𝘁𝘀.

𝑰 𝒂𝒎 𝑹𝒖𝒉𝒐𝒍𝒍𝒂𝒉 — sharing my experience around open-source software, embedded products and the practical challenges of the Cyber Resilience Act.

#EmbeddedLinux #YoctoProject #SBOM #CyberResilienceAct #CyberSecurity #BSI

---
*Originally published in [CRA in Practice](https://www.linkedin.com/newsletters/cra-in-practice/) by Rouhollah Hosseini — [cra-ready.de](https://www.cra-ready.de)*
