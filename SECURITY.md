# Security Policy

## Supported Versions

| Version | Supported | Security Maintenance |
| :--- | :--- | :--- |
| Default Branch (main) | Yes | Active maintenance |

---

## Vulnerability Disclosure Protocol

If you identify a security issue, improper external redirect, or header manipulation defect in this repository, please disclose it privately:

* **Security Contact**: goharrehmanfsd260@gmail.com
* **Repository Maintainer**: Gohar Rehman (@itsgoharrehman)
* **Response SLA**: Acknowledgment within 48 hours; assessment within 5 business days.

---

## Security Invariants

### 1. Form Action Destination Invariants
* All HTML forms must submit queries strictly via HTTPS to official Google endpoints (`https://google.com/search` or `https://www.google.com/search`).
* Forms must never forward user queries, keystrokes, or search terms to intermediate proxy servers, telemetry endpoints, or third-party loggers.

### 2. Zero Client-Side Scripting Policy
* This repository is deliberately engineered with zero client-side JavaScript.
* No inline `<script>` tags, external JavaScript libraries, or dynamic script injections are permitted. This completely eliminates Cross-Site Scripting (XSS) and client-side token harvesting vectors.

### 3. Static Asset Security
* All assets, stylesheets, and SVG graphics must be hosted locally or loaded via verified, secure CDNs.
