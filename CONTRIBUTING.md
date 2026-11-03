# Contributing Guidelines

Thank you for your interest in contributing to google-search-clone. We welcome contributions that improve CSS fidelity, responsive behavior across new device breakpoints, and accessibility standards.

---

## Code of Conduct

All contributors and participants must adhere to our [Code of Conduct](CODE_OF_CONDUCT.md).

---

## Architectural Principles

1. **Strict Zero-JS Policy**: Do not introduce JavaScript files, client-side frameworks, or npm runtime dependencies. All functionality must be executed purely via semantic HTML5 forms and modern CSS3.
2. **Pixel Fidelity**: Replicate Google's genuine spacing, hover transitions, focus rings, and typography as closely as possible.
3. **Accessibility**: Form controls must maintain accessible labels, correct `aria-label` attributes, and clear keyboard focus states.
4. **Target URL Safety**: Form actions must strictly target official Google search endpoints over HTTPS.

---

## Development Workflow

1. Fork and clone the repository:
   ```bash
   git clone https://github.com/<your-username>/google-search-clone.git
   cd google-search-clone
   ```

2. Create a focused branch:
   ```bash
   git checkout -b fix/advanced-search-mobile-alignment
   ```

3. Verify changes across multiple viewport sizes and browsers (Chrome, Firefox, Safari, Edge).

4. Submit a Pull Request targeting `main` and complete the pull request template checklist.
