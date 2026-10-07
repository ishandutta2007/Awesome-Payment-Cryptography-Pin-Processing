# Awesome-Payment-Cryptography-Pin-Processing

## Top Payment Cryptography & PIN Processing Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Payment HSMs, PIN Translation & Self-Hosted Cryptography Libraries*

**Last updated: October 2026**



This repository tracks notable **commercial payment cryptography platforms** and **open-source projects** that secure card transactions — PIN block encoding, translation, verification, key management, and EMV cryptogram processing. These tools power card issuance, acquiring, switching, and ATM networks.



**Examples** include AWS Payment Cryptography, Thales payShield, Futurex VirtuCrypt, Utimaco Atalla HSM, MYHSM, Fiserv PIN Pad Solutions, Worldline Cryptographic Services, Euronet Electronic Payment Services, FIS Global, and TSYS (the category leaders).



**Open-source emphasis**: Payment cryptography is a domain where open-source provides strong **software libraries, protocol implementations, and testing tools** — but **production PIN translation requires certified HSMs** (PCI PIN Security, PCI P2PE). **jPOS**, **paysec**, **psec**, **isopace/vault**, and **tr31** deliver production-grade payment security primitives. **OpenEMV** and **emvpt** provide EMV tooling. This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[AWS Payment Cryptography](https://aws.amazon.com/payment-cryptography/)**  

  **AWS's managed payment HSM service** — PIN translation, CVV generation, and EMV processing without managing hardware . **Built on Futurex hardware** — native integration with AWS workloads . **Best for AWS-native payment processing**.



- **[Thales payShield](https://cpl.thalesgroup.com/encryption/payshield-10k)**  

  **The dominant payment HSM globally** — every Visa, Mastercard, and regional card scheme transaction touches a payShield-class HSM . **PCI HSM v3 and FIPS 140-3 Level 3 certified** — the reference implementation for card-issuing and acquiring infrastructure . **Best for enterprise payment HSMs**.



- **[Futurex VirtuCrypt](https://www.futurex.com/)**  

  **Cloud and on-premises payment HSM platform** — HSMaaS with managed key services included in PCI audits . **Native integration with AWS, Azure, and Google Cloud** — powers AWS Payment Cryptography . **PQC support (ML-KEM, ML-DSA, SLH-DSA)** — one of the few HSM vendors with full post-quantum support . **Best for hybrid cloud payment cryptography**.



- **[Utimaco Atalla HSM](https://utimaco.com/)**  

  **Enterprise payment HSM** — Atalla brand trusted in card issuance and acquiring. **PCI HSM certified** with legacy Atalla tool compatibility. **Best for Atalla migration**.



- **[MYHSM by Utimaco](https://www.myhsm.com/)**  

  **Payment HSM as a Service** — cloud-based payment cryptography with pay-per-use pricing. **PCI PIN and PCI DSS compliant**. **Best for OPEX-based payment security**.



- **[Fiserv PIN Pad Solutions](https://www.fiserv.com/)**  

  **PIN pad and payment terminal security** — end-to-end encryption and key management. **Best for merchant acquiring**.



- **[Worldline Cryptographic Services](https://worldline.com/)**  

  **Managed payment cryptography** — PIN processing, key management, and HSM services. **Best for European payment infrastructure**.



- **[Euronet Electronic Payment Services](https://www.euronet.com/)**  

  **Payment processing and cryptographic services** — ATM and POS networks. **Best for global payment networks**.



- **[FIS Global](https://www.fisglobal.com/)**  

  **Payment processing and cryptography** — card issuance, acquiring, and switching. **Best for enterprise payment processing**.



- **[TSYS](https://www.tsys.com/)**  

  **Payment processing and security** — tokenization, encryption, and PIN management. **Best for issuer and acquirer processing**.



## Open-Source GitHub Projects



### Payment Security Libraries



- **[jPOS](https://github.com/jpos/jPOS)**  

  **The most widely deployed open-source payment framework**, AGPL-3.0 licensed . **ISO-8583 protocol handling** — the standard for payment messaging . **ANS X9.24 and EMV encryption** with software security module and HSM interfaces . **PCI-grade configuration, metrics, profiling, distributed tracing, and structured logging** . **25+ years of production use** in payment gateways, acquirer, and issuer systems . **The de facto open-source payment switch framework** — trusted by industry giants and unicorn Fintechs . **Trade-off**: Production PIN handling requires HSM-backed security module . **Best for payment gateway and switch development**.



- **[paysec (Rust)](https://docs.rs/crate/paysec/0.0.2)**  

  **Rust library for payment security standards**, GPL-3.0 licensed . **ISO 9564 Format 4 PIN block** — encode and encipher PIN blocks with AES encryption binding PIN to PAN . **Future plans for TR-31 and TR-34 key block protection** . **Best for Rust-based payment cryptography**.



- **[psec (Python)](https://socket.dev/pypi/package/psec)**  

  **Python package for payment cryptography**, open-source . **TR-31 key block wrapping and unwrapping, CVV generation, Triple DES utilities, AES utilities, MAC generation, PIN generation, and PIN block encoding/decoding** . **PIN block ISO 4 support** contributed by David Schmid . **890 weekly downloads** with active maintenance . **Best for Python payment security**.



- **[isopace/vault (Go)](https://pkg.go.dev/github.com/teqpace-services/isopace/vault#1)**  

  **Go payment cryptography vault**, open-source . **PIN block encoding and translation** — ISO 9564 formats 0, 1, and 3 . **PINEncryptor for issuer-side PIN issuance** and **PINTranslator for acquirer/switch PIN translation** . **SealedVault for software key storage** — AES-GCM encrypted at rest with KEK, audit hooks, and key usage enforcement . **Critical contract**: A conforming HSM adapter MUST perform PIN translation atomically so clear PIN never leaves the device — stock PKCS#11 cannot satisfy this and MUST NOT implement PINTranslator . **Best for Go-based payment systems**.



- **[psec (Rust)](https://docs.rs/crate/psec)** — Rust payment security library .



### Key Management & TR-31



- **[openemv/tr31](https://github.com/openemv/tr31)**  

  **Key block library and tools for ANSI X9.143, ASC X9 TR-31 and ISO 20038**, open-source . **TR-31 key block wrapping and unwrapping** — the standard for key exchange in payment networks . **Part of the OpenEMV ecosystem** — actively maintained . **Best for TR-31 key block handling**.



- **[openemv/dukpt](https://github.com/openemv/dukpt)** — **ANSI X9.24 DUKPT libraries and tools** — the standard for deriving unique keys per transaction in POS and ATM networks . **Best for DUKPT key management**.



### EMV & Smart Card Tools



- **[OpenEMV](https://github.com/openemv)**  

  **Open-source EMV payments stack**, open-source . **EMV libraries and tools** — kernel, card implementation, and diagnostic tools . **Part of a broader ecosystem** including JavaCard EMV applets for terminal testing . **Best for EMV development and testing**.



- **[emvpt](https://github.com/mrautio/emvpt)**  

  **Minimum Viable Payment Terminal**, open-source . **EMV terminal implementation** for payment acceptance . **44 GitHub stars** with active development . **Best for EMV terminal development**.



- **[Smart Card Shell Script Collection](https://github.com/openemv/smartcard-shell)**  

  **Scripts for smart card inspection and EMV data extraction**, open-source . **83+ GitHub stars** — actively maintained . **Best for smart card debugging**.



### JavaCard & Terminal Implementations



- **[JavaCard EMV Implementation](https://github.com/openemv/emv-card)**  

  **JavaCard implementation of an EMV card for payment terminal testing**, open-source . **45 GitHub stars** — updated recently . **Best for terminal testing**.



- **[emv-tools](https://github.com/openemv/emv-tools)**  

  **Tools to work with EMV bank cards**, open-source . **74+ GitHub stars** — actively maintained . **Best for EMV card analysis**.



- **[learn-pos-tools](https://github.com/chuwuwang/learn-pos-tools)**  

  **POS payment, encryption, EMV tools**, open-source . **Lightweight toolkit for ISO8583, EMV, and secure key operations** . **Best for POS development**.



### Additional Strong Open-Source Options



- **jPOS-EE** — Extended edition with database, card, and settlement components .

- **jPOS-CMF** — Common Message Format for ISO-8583 v2003 .

- **JavaCard SDK** — Oracle's JavaCard development kit .

- **GlobalPlatform Pro** — JavaCard and smart card management .

- **emv-tools** — EMV card analysis tools .

- **psec** — Python payment security .

- **paysec** — Rust payment security .

- **isopace/vault** — Go payment vault .



**Frameworks for building custom payment cryptography solutions**: Combine **jPOS** for the most complete open-source payment framework with ISO-8583, EMV, and HSM interfaces . Use **psec (Python)** or **paysec (Rust)** for payment security primitives including PIN blocks and TR-31 . Deploy **isopace/vault (Go)** for PIN encoding and translation with sealed software key storage . Integrate **openemv/tr31** for TR-31 key block handling and **openemv/dukpt** for DUKPT key management . Use **OpenEMV** and **emvpt** for EMV development and terminal testing . **Critical**: Production PIN translation and key handling require a **certified HSM** — software vaults are suitable for development, testing, and non-PIN operations only .



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Payment cryptography handles PINs, keys, and cardholder data — **PCI PIN Security and PCI P2PE compliance require certified HSMs** for production PIN translation. Software vaults (isopace/vault SealedVault, jPOS software security module) are for **development, testing, and non-PIN operations only** .

- **Clear PIN must never exist in host memory during translation** — a conforming HSM adapter performs translation atomically inside the device. Stock PKCS#11 cannot satisfy this requirement and must not be used for PIN translation .

- **Fixed TDES PIN keys are prohibited since January 1, 2023** — use AES DUKPT (Format 4) inbound and ZPK AES outbound .

- **License considerations**: jPOS uses AGPL-3.0 with commercial licensing available ; paysec uses GPL-3.0 ; isopace/vault is open-source . Verify licensing against your use case.

- **Open-source payment libraries provide strong primitives but not compliance certification** — PCI validation requires certified hardware and audited processes.



---



**Made for payment engineers, security architects, and organizations seeking payment cryptography sovereignty.**

Let's make payment cryptography and PIN processing more open, transparent, and secure.
