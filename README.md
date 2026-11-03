<div align="center">
  <h1>google-search-clone</h1>
  <p>Pixel-perfect frontend specification of Google Search, Image Search, and Advanced Search interfaces built with semantic HTML5 and responsive CSS3.</p>

  <p>
    <a href="LICENSE"><img src="https://img.shields.io/github/license/itsgoharrehman/google-search-clone?style=flat-square&logo=opensourceinitiative&logoColor=white" alt="License"></a>
    <img src="https://img.shields.io/badge/HTML5-Semantic_Markup-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
    <img src="https://img.shields.io/badge/CSS3-Flexbox_&_Grid-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3">
    <img src="https://img.shields.io/badge/Architecture-Zero_JS_Pure_CSS-0969da?style=flat-square&logo=w3c&logoColor=white" alt="Pure CSS">
    <a href="https://github.com/itsgoharrehman/google-search-clone/stargazers"><img src="https://img.shields.io/github/stars/itsgoharrehman/google-search-clone?style=flat-square&logo=github&logoColor=white" alt="Stars"></a>
    <a href="https://github.com/itsgoharrehman/google-search-clone/issues"><img src="https://img.shields.io/github/issues/itsgoharrehman/google-search-clone?style=flat-square&logo=github&logoColor=white" alt="Issues"></a>
  </p>
</div>

---

A responsive, pixel-accurate frontend implementation recreating the core user interfaces of Google Search, Google Image Search, and Google Advanced Search.

Engineered entirely with semantic HTML5 markup and modern CSS3 (Flexbox, CSS Grid, and custom variables) with zero JavaScript execution dependencies. The project faithfully replicates Google's native HTTP GET form submission workflows, directing search parameters directly to live Google endpoints.

---

## Architectural Principles and UI Architecture

```mermaid
flowchart TD
    User([User]) --> Navigation{Interface Selector}

    subgraph Interfaces["Zero-JS Pure CSS Frontend"]
        Navigation -->|Standard Search| Index["index.html (Google Web Search)"]
        Navigation -->|Image Search| Image["image.html (Google Image Search)"]
        Navigation -->|Advanced Search| Adv["advanced.html (Google Advanced Search)"]
    end

    subgraph QueryDispatches["Direct HTTP GET Form Actions"]
        Index -->|form action='https://google.com/search' name='q'| GSearch["Google Web Engine"]
        Index -->|form action='https://google.com/search' btnI='1'| Lucky["I'm Feeling Lucky Direct Redirect"]
        Image -->|form action='https://google.com/search' tbm='isch'| GImages["Google Images Engine"]
        Adv -->|as_q, as_epq, as_oq, as_eq| GAdv["Google Advanced Query Engine"]
    end
```

---

## Implemented Pages and Parameter Specifications

| Page | File | Form Action | Key Query Parameters |
| :--- | :--- | :--- | :--- |
| **Google Search** | `index.html` | `https://google.com/search` | `q` (Search terms), `btnI=1` (I'm Feeling Lucky) |
| **Image Search** | `image.html` | `https://google.com/search` | `q` (Search terms), `tbm=isch` (Image mode) |
| **Advanced Search** | `advanced.html` | `https://google.com/search` | `as_q` (all words), `as_epq` (exact phrase), `as_oq` (any words), `as_eq` (none of these words) |

---

## Key Features

* **Zero-JavaScript Execution**: All search functionality operates entirely via standard HTML5 `<form method="GET">` mechanics.
* **Pixel-Accurate Typography and Layout**: Implements Google's exact font hierarchy, search bar box-shadow transitions, pill buttons, and responsive navbar alignment.
* **Advanced Search Grid**: Structured multi-input form replicating Google's four-tier search criteria with right-column contextual guidance.
* **Accessible and Semantic**: Structured with proper `<header>`, `<main>`, `<footer>`, and accessible ARIA attributes.
* **Lightweight**: Minimal asset footprint loading in single-digit milliseconds.

---

## Directory Structure

```
google-search-clone/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.yml          # Structured bug report form
│   │   └── feature_request.yml     # Structured feature request form
│   ├── PULL_REQUEST_TEMPLATE.md    # Pull request review checklist
│   └── dependabot.yml              # Weekly automated npm scanner
├── advanced.html                   # Google Advanced Search implementation
├── image.html                      # Google Image Search implementation
├── index.html                      # Core Google Web Search interface
├── styles.css                      # Unified stylesheet for all three interfaces
├── package.json                    # Local dev scripts and tooling metadata
├── LICENSE                         # MIT License
├── SECURITY.md                     # Security policy and form action boundaries
├── CONTRIBUTING.md                 # Contribution guidelines
└── CODE_OF_CONDUCT.md             # Contributor Covenant v2.1
```

---

## Local Development

### Prerequisites

* Any modern web browser (Chrome, Firefox, Safari, Edge)
* Node.js v18+ (optional, for local HTTP static preview)

### Setup and Running

1. Clone the repository:
   ```bash
   git clone https://github.com/itsgoharrehman/google-search-clone.git
   cd google-search-clone
   ```

2. Launch local static server:
   ```bash
   npx serve .
   ```
   Or open `index.html` directly in your browser.

---

## Security Policy

See [SECURITY.md](SECURITY.md) for details regarding the static frontend security model and safe URL target invariants.

---

## License

This project is licensed under the terms of the [MIT License](LICENSE).
