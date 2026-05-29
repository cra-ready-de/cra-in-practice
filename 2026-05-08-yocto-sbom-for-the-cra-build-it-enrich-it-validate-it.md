---
title: "Yocto SBOM for the CRA: Build It. Enrich It. Validate It."
author: "Rouhollah Hosseini"
published: "2026-05-08 06:26"
created: "2026-05-08 06:10"
source: "LinkedIn Newsletter — CRA in Practice"
source_url: "https://www.linkedin.com/in/rouhollah-hosseini-cra/"
lang: "de-en"
---

# Yocto SBOM for the CRA: Build It. Enrich It. Validate It.

Yocto SBOM for the CRA: Build It. Enrich It. Validate It.

CRA Annex I, Part II, Section 1 requires every product with digital elements to be accompanied by a software bill of materials in a commonly used, machine-readable format covering at least all top-level dependencies.

For teams building embedded Linux with the Yocto Project, the tooling to meet this requirement is already in the build system. The question is whether the output it produces by default is sufficient — and the honest answer is: partially.

What the CRA actually requires from an SBOM

The CRA mandates SBOMs for every product with digital elements. Accepted formats include CycloneDX and SPDX. The SBOM must cover all dependencies — direct and transitive — not just top-level components.

CMS Blog

The regulation does not mandate a specific format version, tool, or field set beyond "commonly used and machine-readable." The practical compliance target for the field content is BSI TR-03183-2, currently at version 2.1.0, which describes formal and technical requirements for SBOMs. It is not binding or mandatory, and it cannot be used as a presumption of conformity — but it is the most detailed and authoritative guidance currently available for CRA SBOM implementation.

Advant-beiten

Step 1 — Generate: what create-spdx produces

The OpenEmbedded build system generates SBOM information by default in recent releases by inheriting the create-spdx class in INHERIT_DISTRO. The output is an SPDX JSON file at .

European Commission

For older releases or custom distros, enable it explicitly:

The create-spdx class offers additional options:  adds source file descriptions,  exports kernel configuration parameters,  attaches supplier information to the image SBOM, and  attaches it to individual packages.

Wikipedia

The supplier field matters for CRA compliance — BSI TR-03183-2 requires manufacturer identification in the SBOM. Set it:

What the default output includes: package names and versions, SPDX license identifiers, SHA-256 checksums per package, DESCRIBES and CONTAINS relationships, and a unique document namespace.

Step 2 — Enrich: what you need to add

The SPDX generation process captures recipe metadata including name, version, license, and source dependencies. CPE identifiers are generated through the separate cve-check class.

WKO

Enable CVE enrichment alongside SBOM generation:

This populates CPE identifiers for packages where Yocto's CVE database has matches. Verify coverage — not every package will receive a CPE automatically, particularly custom or proprietary components.

On PURL: BSI TR-03183-2 lists Package URL (purl) as an additional field that must be provided if it exists and satisfies the requirements of the SBOM format specification. This is a conditional SHOULD requirement, not an unconditional MUST. Yocto does not generate PURLs by default. Where PURLs are meaningful for your component set, add them via recipe metadata or post-processing.

Openkritis

A known gap in the current TR-03183 guidance is that the methodology for computing SHA-256 hashes of source code remains unspecified, and relationship requirements between transitive components — while required to be enumerated — are not explicitly mandated in terms of their type. Document your approach to both in your Technical Dossier.

European Commission

Step 3 — Validate: before the SBOM enters the Technical Dossier

A build-time SBOM is evidence only if it has been validated. Before filing it in the Annex VII Technical Dossier, check the following against BSI TR-03183-2 v2.1.0:

Mandatory fields per component:

component name, version, supplier/originator, cryptographic hash of the binary, SPDX license identifier or expression, and the relationship to parent components.

License identifiers:

Licences must be referred to by their appropriate SPDX licence identifier or licence expression. Licence text must not be used as a substitute for a licence identifier.

Dr. Datenschutz

Transitive dependencies:

Recursive dependency resolution must be performed at least until the first out-of-scope component on each path. This means resolving dependencies recursively for every component delivered. Yocto's create-spdx class handles this for build-system-managed dependencies. Review any statically linked or manually included components.

CMS

SBOM update obligations:

BSI TR-03183-2 requires generating new SBOMs to accompany each new software version, and updating SBOMs even without a new software release if component information changes. Integrate SBOM generation into your CI/CD pipeline so it is automatic and not manual.

CMS

What this means for the Technical Dossier

Your Technical Dossier under CRA Annex VII must contain documentation of your product's components. The validated SBOM is that documentation. A Yocto-generated SBOM that has been enriched with CPE identifiers, reviewed for license identifier completeness, and validated against TR-03183-2 satisfies this requirement.

BSI TR-03183 will be gradually developed further and replaced by the corresponding harmonised European standards as soon as they become available. Until harmonised standards are published under the CRA, TR-03183-2 v2.1.0 is the practical reference. Build your SBOM process against it now.

Advant-beiten

𝑰 𝒂𝒎 𝑹𝒖𝒉𝒐𝒍𝒍𝒂𝒉 — sharing my experience around open-source software, embedded products and the practical challenges of the Cyber Resilience Act.

#CRA #SBOM #Yocto #SPDX #EmbeddedLinux #CyberResilienceAct #BSI #TR03183 #ProductSecurity #TechnicalDossier #OpenEmbedded

---
*Originally published in [CRA in Practice](https://www.linkedin.com/newsletters/cra-in-practice/) by Rouhollah Hosseini — [cra-ready.de](https://www.cra-ready.de)*
