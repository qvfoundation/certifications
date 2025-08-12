# Qverify Certifications

**Qverify** is an independent nonprofit dedicated to certifying blockchain projects for **Post-Quantum Security**.  
We publish all certifications openly on GitHub to ensure **transparency, verifiability, and public trust**.

---

## 📜 Certification Process

1. **Code-level audit** against NIST post-quantum cryptography (PQC) standards and Qverify methodology.
2. **Verification** of algorithm correctness, parameter selection, and entropy sources.
3. **Publication** of:
   - PDF audit report
   - SHA3-512 checksum
   - PGP detached signature
   - Machine-readable metadata (`certification.json`)

---

## 🔍 How to Verify a Certification

Every Qverify report is published with:
- **SHA3-512 checksum** — ensures file integrity
- **PGP signature (`.asc`)** — ensures authenticity

### 1. Verify the SHA3-512 Checksum
**Linux/macOS**
```bash
sha3sum -a 512 Qverify_Certification_Report.pdf
```
**Python**
```python
import hashlib

with open("Qverify_Certification_Report.pdf", "rb") as f:
    print(hashlib.sha3_512(f.read()).hexdigest())

### 2. PGP Signature Verification
```bash
gpg --import Qverify-public-key.asc
gpg --verify signature.asc Qverify_Certification_Report.pdf
