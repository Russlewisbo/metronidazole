# Miscellaneous Agents: Metronidazole & the Urinary Tract Agents — Lecture Package

A ~1.5-hour lecture for postgraduate ID specialists pairing **metronidazole** (condensed) with the
**urinary tract agents** — nitrofurantoin, fosfomycin, methenamine. Polymyxins are deliberately
excluded (covered in a separate lecture).

## Contents

- `misc-uti-agents-slides.qmd` — Quarto RevealJS deck: 55 content slides + section dividers, speaker notes on every slide, 4 teaching cases
- `misc-uti-agents-webpage.qmd` — Quarto HTML lecture-notes page covering both halves
- `misc-uti-agents-references.bib` — 42 BibTeX entries (metronidazole subset + UTI-agent refs)
- `misc-uti-agents-images/` — institutional logo (DMM_newlogo.png)
- `custom.scss`, `diagnostic-microbiology-and-infectious-disease.csl`, `_extensions/fontawesome/` — rendering dependencies

## Sources

- Part I (metronidazole): Nagel & Aronoff, "Metronidazole," Ch. 27, *Mandell, Douglas, and Bennett's
  Principles and Practice of Infectious Diseases*. Entries adapted from the existing metronidazole lecture.
- Part II (UTI agents): Horton & Drekonja, "Urinary Tract Agents: Nitrofurantoin, Fosfomycin, and
  Methenamine," Ch. 36 (attached PDF; OCR'd — see note below).

Landmark/modern citations verified against PubMed and flagged `% VERIFIED (PubMed)` in the `.bib`:
Gupta 2011 (IDSA/ESCMID cystitis guideline; source of the efficacy table), Huttner 2018 (JAMA —
5-day nitrofurantoin superior to single-dose fosfomycin), and ALTAR 2022 (BMJ — methenamine
non-inferior to daily antibiotic prophylaxis).

## Unifying theme

**Pharmacology, not spectrum, determines clinical fate.** Metronidazole's complete absorption became a
liability in luminal gut infection (its CDI demotion); the urinary agents work in cystitis precisely
because they concentrate in urine and nowhere useful else — which is also why none treats pyelonephritis.

## To render

```
quarto render misc-uti-agents-slides.qmd
quarto render misc-uti-agents-webpage.qmd
```

Quarto was not available in the build sandbox, so a first render in RStudio/Quarto is recommended to
confirm layout. Structural checks passed: BibTeX parses (36 unique keys, balanced braces), YAML valid,
and every `[@key]` used resolves to a bib entry.

## Notes / to verify

- **Ch. 36 had no text layer** (image/print export) and was OCR'd. Body content is reliable; the
  reference list OCR captured only entries ~82–101 cleanly. The high-value citations (Gupta, Huttner,
  ALTAR) were verified via PubMed. A handful of chapter refs were reconstructed from in-text citations
  (`Muller2017`, `Santos2016`, `Falagas2016`) and should be spot-checked against the printed chapter
  before publishing.
- Three `<!-- IMAGE NEEDED -->` placeholders (metronidazole activation pathway). Source figures are
  copyrighted — redraw rather than reproduce.
- Metronidazole material is a **condensed** adaptation of your existing full metronidazole deck; the
  fuller version lives in the metronidazole-polymyxins package if you want more depth on any point.
- The chapter is US-centric on fosfomycin (oral cystitis only). A dedicated **IV fosfomycin** block was
  added for the European/Italian context — systemic combination therapy for MDR gram-negatives and the
  daptomycin+fosfomycin MRSA option. It covers the **salt/water overload** liability (disodium salt,
  ~11–14 mmol Na⁺/g; ~175–220 mmol Na⁺/day at 16 g/day) and a **balanced supporting-vs-not-supporting**
  evidence summary — supporting: ZEUS (Kaye 2019), SIMIT/SPILF 2024 guidance (Meschiari); not/weakly
  supporting: FOREST (Sojo-Dorado 2022, failed non-inferiority), Pujol 2021 (MRSA, primary endpoint NS),
  low-quality non-UTI data (Grabein 2017; Zayyad/Paul 2017). All PubMed-verified with DOIs.
