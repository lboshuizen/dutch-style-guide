---
layout: default
title: Dutch Style Guide - 37 Rules for Clear Dutch Writing
description: Practical writing guide for developers and technical writers. Includes Claude Code skill and Fabric pattern.
---

# Professional Dutch Writing Guidelines

## 37 Practical Rules for Clear, Effective Dutch

A concise style guide for technical writers and developers—condensed from official sources into actionable rules.

[View on GitHub](https://github.com/lboshuizen/dutch-style-guide) • [Download v1.0.0](https://github.com/lboshuizen/dutch-style-guide/releases/tag/v1.0.0)

---

## Key Features

| **37 Rules** | **3 Official Sources** | **Open Source** |
|:---:|:---:|:---:|
| Practical and concise | Taalunie, Rijksoverheid, EC | CC BY 4.0 License |

---

## Overview

This guide condenses official Dutch writing standards into 37 practical rules. It focuses on common violations rather than linguistic theory, providing clear before-and-after examples for immediate application.

**Built from authoritative sources:**
- [Taaladvies.net](https://taaladvies.net) — Nederlandse Taalunie
- [Rijksoverheid Schrijfwijzer](https://www.rijksoverheid.nl/onderwerpen/rijksoverheidstijl) — Dutch government style guide
- [EC Stijlgids Nederlands](https://commission.europa.eu/system/files/2023-10/Stijlgids-DGT-NL.pdf) — European Commission

---

## Target Audience

This guide serves professionals who write in Dutch:

- **Software developers** writing documentation, commit messages, and release notes
- **Technical writers** creating user guides and API documentation
- **Content teams** reviewing AI-generated Dutch text
- **Non-native speakers** seeking clear, authoritative guidelines

---

## Implementation Tools

### Claude Code Integration

Automated checking for Dutch text in Claude Code:

```bash
claude plugin install https://github.com/lboshuizen/dutch-style-guide
```

The skill applies all 37 rules automatically when you write Dutch text.

### Fabric Pattern

Command-line analysis for existing documents:

```bash
# Copy to Fabric patterns directory
cp -r fabric-pattern ~/.config/fabric/patterns/improve_dutch_writing

# Analyze Dutch text
echo "Your text here" | fabric --pattern improve_dutch_writing
```

[View full installation instructions →](https://github.com/lboshuizen/dutch-style-guide/tree/main/fabric-pattern)

---

## Example Transformations

### Rule 4: Use Active Voice

| Before | After |
|--------|-------|
| De applicatie wordt geüpdatet door het systeem. | Het systeem updatet de applicatie. |

**Impact:** Clearer subject-action relationship, more direct communication.

### Rule 1: Omit Needless Words

| Before | After |
|--------|-------|
| Het is belangrijk om te vermelden dat deze functie beschikbaar is. | Deze functie is beschikbaar. |

**Impact:** 12 words reduced to 4 words—75% more concise.

### Rule 12: Use Concrete Language

| Before | After |
|--------|-------|
| De performance is aanzienlijk verbeterd. | De laadtijd daalde van 2s naar 0.5s. |

**Impact:** Vague claim replaced with measurable data.

---

## Complete Documentation

[Read the full guide →](https://github.com/lboshuizen/dutch-style-guide/blob/main/dutch-style-guide.md)

The complete guide includes all 37 rules with detailed examples, explanations, and application guidelines for technical writing, documentation, and business communication.

---

## Contributing

We welcome contributions to improve the guide:

- **Report errors:** [Open an issue](https://github.com/lboshuizen/dutch-style-guide/issues/new?template=bug_report.yml)
- **Suggest rules:** [Submit a suggestion](https://github.com/lboshuizen/dutch-style-guide/issues/new?template=rule_suggestion.yml)
- **Improve examples:** [Create a pull request](https://github.com/lboshuizen/dutch-style-guide/pulls)

View our [contribution guidelines](https://github.com/lboshuizen/dutch-style-guide/blob/main/CONTRIBUTING.md) for details.

---

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to use, share, and adapt this guide with proper attribution.
