# Awesome List Builder Skill

A [Claude Code](https://claude.ai/claude-code) skill for building [sindresorhus/awesome](https://github.com/sindresorhus/awesome)-compliant GitHub repos with MkDocs Material companion sites from scratch.

## What It Does

Give Claude Code a research topic and this skill walks through a structured 7-phase pipeline to produce:

- A curated **awesome list** (README.md) organized around a thesis, not just a link dump
- A **MkDocs Material companion site** with concept explainers, method comparisons, paper deep reads, and synthesis essays
- **CI/CD workflows** for awesome-lint and automatic GitHub Pages deployment

## Pipeline

| Phase | Mode | Output |
|-------|------|--------|
| 0. Thesis Discovery | Interactive | One-sentence thesis and target reader |
| 1. Structure Design | Interactive | Categories, entry format, nav tree |
| 2. Scaffold | Autonomous | Boilerplate files, CI, mkdocs.yml |
| 3. README | Autonomous | Awesome list with curated entries |
| 4. MkDocs Site | Autonomous | Full companion site (concepts, methods, deep reads, synthesis, glossary) |
| 5. Verification | Autonomous | Coverage audit against benchmarks, existing lists, reviews |
| 6. Deploy | Autonomous | Live GitHub repo + Pages site |

## Built With This Skill

| Project | Thesis | Links |
|---------|--------|-------|
| **Awesome Virtual Cell** | Foundation models promise to simulate cells but benchmarks say otherwise. | [GitHub](https://github.com/LiudengZhang/awesome-virtual-cell) · [Site](https://liudengzhang.github.io/awesome-virtual-cell/) |
| **Awesome Spatial Omics Niche** | Every method defines "niche" differently. This list tells you how. | [GitHub](https://github.com/LiudengZhang/awesome-spatial-omics-niche) · [Site](https://liudengzhang.github.io/awesome-spatial-omics-niche/) |
| **Awesome Pan-Cancer Phosphoproteomics** | Without knowing which kinase, which pathway, and which drug, a phosphosite catalog is not a map. | [GitHub](https://github.com/LiudengZhang/awesome-pan-cancer-phosphoproteomics) · [Site](https://liudengzhang.github.io/awesome-pan-cancer-phosphoproteomics/) |
| **Awesome Spatial Omics** | Spatial omics has more tools than any analyst can evaluate. This list organizes them by question and technology. | [GitHub](https://github.com/LiudengZhang/awesome-spatial-omics) · [Site](https://liudengzhang.github.io/awesome-spatial-omics/) |

## Installation

Copy `SKILL.md` into your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/awesome-list-builder
cp SKILL.md ~/.claude/skills/awesome-list-builder/SKILL.md
```

Claude Code will automatically detect and use the skill when you ask it to build an awesome list, curate resources for a topic, or create a knowledge repo with a documentation site.

## Design Principles

- **Thesis-first**: Every list needs a point of view. "A list of all X" is a red flag.
- **Honest assessments**: Entry descriptions include limitations alongside strengths. No marketing copy.
- **Coverage verification**: Cross-reference against benchmarks, existing lists, review papers, and citation counts before publishing.
- **README = index, site = depth**: The awesome list provides the curated index; the companion site adds concept pages, method comparisons, and paper analyses that the README format cannot support.
- **Inline review**: Every companion site ships with [Hypothesis](https://web.hypothes.is/) for inline text annotation — select any sentence and leave a comment, just like Google Docs.

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)
