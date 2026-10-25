# 🦉 OASN1

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OASN1** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OASN1 decodes and checks ASN.1 data. It accepts DER, PEM, base64 or hex input, shows the full structure as a tree (including DER nested inside OCTET or BIT STRINGs), and runs a strict DER conformance linter. Its X.509 inspector reviews certificates, chains, keys, CSRs and CRLs and reports weaknesses.

---

## ✨ Features

- Auto-detects DER, multi-block PEM, base64 and hex input from a file, the command line or stdin
- Tree decoder with inline decoding of encapsulated DER and an openssl asn1parse-style view
- Strict DER linter: non-minimal lengths and tags, padded INTEGERs, SET ordering, time formats, string charsets
- X.509 inspector: chain order and signatures, validity, key strength, SAN, usages and fingerprints, with findings (expired, SHA-1/MD5, RSA < 2048, no SAN)
- Key / CSR / CRL inspector (PKCS#1, PKCS#8, SEC1, PKIX) and OID lookup
- BER → canonical DER re-encoder, extract by offset, an ASN.1 builder language and JSON tree export

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OASN1                                      # interactive menu
./OASN1 --decode cert.der --asn1parse
./OASN1 --cert fullchain.pem
./OASN1 --lint blob.der
./OASN1 --oid 1.2.840.113549.1.1.11
```

Run `./OASN1 --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
