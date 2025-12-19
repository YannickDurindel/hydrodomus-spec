# Hydrodomus - Home Hydrogen Generation System

Technical specification and prototype requirements for a residential hydrogen generation system designed for fuel cell electric vehicle (FCEV) owners.

## Overview

**Hydrodomus** (from Latin *hydro* = water, *domus* = home) is a home-based hydrogen generation and storage system that enables FCEV owners to produce hydrogen fuel at their residence using water electrolysis, eliminating dependence on public hydrogen refueling infrastructure.

### Key Features

- **PEM Electrolysis**: Proton Exchange Membrane technology for clean hydrogen production
- **700 bar Storage**: Automotive-standard high-pressure storage
- **SAE J2601 Compliant**: Standard vehicle refueling interface
- **Residential Scale**: Designed for garage/utility room installation

## Document Contents

| Chapter | Title | Description |
|---------|-------|-------------|
| 1 | Introduction | Problem statement, market context, project objectives |
| 2 | Theoretical Background | Electrochemistry, thermodynamics, PEM technology, hydrogen storage physics |
| 3 | System Architecture | Process flow, subsystem design, P&ID diagrams |
| 4 | Component Specifications | Detailed specs for electrolyzer, compressor, storage, dispensing |
| 5 | Safety and Certifications | Hazard analysis, applicable standards (ISO, SAE, EC), certification pathway |
| 6 | Conclusions | Summary, economic analysis, prototype development plan |
| Appendix | Reference Data | Vehicle specs, physical constants, conversion factors |

## Technical Specifications

| Parameter | Value |
|-----------|-------|
| Production rate | 0.5 kg H₂/day |
| Storage pressure | 700 bar |
| Storage capacity | 10 L (~0.4 kg H₂) |
| System efficiency | 60-70% |
| Power consumption | 2-3 kW |

## Repository Structure

```
├── main.tex                 # Master LaTeX document
├── main.pdf                 # Compiled PDF (49 pages)
├── additionalFunctions.tex  # Custom LaTeX macros
├── symbols.tex              # List of symbols with units
├── acronyms.tex             # Abbreviations glossary
├── references.bib           # Bibliography
├── chapters/
│   ├── 00_titlepage.tex
│   ├── 00_abstract.tex
│   ├── 01_introduction.tex
│   ├── 02_theory.tex
│   ├── 03_architecture.tex
│   ├── 04_components.tex
│   ├── 05_safety.tex
│   ├── 06_conclusions.tex
│   └── appendixA.tex
├── images/
│   └── schemalist.jpeg      # Original concept sketch
└── figures/                 # Generated TikZ figures
```

## Building the Document

### Prerequisites

- LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- Required packages: `tikz`, `chemformula`, `siunitx`, `glossaries`, `biblatex`

### Compilation

```bash
# Full compilation with glossaries
pdflatex main.tex
makeglossaries main
biber main
pdflatex main.tex
pdflatex main.tex
```

Or use `latexmk` for automatic compilation:
```bash
latexmk -pdf main.tex
```

## Standards Referenced

- **ISO 19880**: Gaseous hydrogen fueling stations
- **ISO 22734**: Hydrogen generators using water electrolysis
- **ISO 17268**: Refueling connection devices
- **SAE J2601**: Fueling protocols for light duty hydrogen vehicles
- **EC 79/2009**: Type-approval of hydrogen-powered vehicles
- **ATEX 2014/34/EU**: Equipment for explosive atmospheres

## Target Vehicles

| Vehicle | Tank Capacity | Range |
|---------|---------------|-------|
| Toyota Mirai | 5.6 kg | 650 km |
| Hyundai Nexo | 6.3 kg | 666 km |
| BMW iX5 Hydrogen | 6.0 kg | 504 km |
| Honda CR-V e:FCEV | 4.3 kg | 435 km |

## License

This document is provided for research and development purposes.

## Author

Yannick Durindel - Hydrodomus

---

*"Bringing hydrogen home"*
