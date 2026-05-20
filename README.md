# SOLO Skill: Literature Deep Analysis

A reusable SOLO skill for deep paragraph-by-paragraph analysis of scientific literature, with bilingual (English-Chinese) comparison, figure/subfigure interpretation, and structured reporting.

## Features

- **Paragraph-by-paragraph comparison**: Original text + Chinese translation + terminology glossary
- **Deep figure analysis**: Every subfigure (a, b, c...) analyzed with experimental content and result interpretation
- **Method summary**: Structured tables for preparation methods, animal models, and detection techniques
- **Conclusion & significance**: Key findings, clinical translation potential, limitations
- **Terminology glossary**: Core terms with bilingual definitions
- **Output**: Professional Word document (.docx)

## Repository Structure

```
solo-skill-literature-analysis/
├── README.md                          # This file
├── skill.md                           # Core skill prompt (SOLO skill format)
├── config.json                        # Skill metadata
├── examples/
│   └── sample-output.md               # Example output structure
└── variants/
    ├── quick-analysis.md              # Quick analysis variant (abstract + figures only)
    ├── full-analysis.md               # Full analysis variant (all sections)
    └── batch-analysis.md              # Batch analysis variant (multiple papers)
```

## How to Use

### Option 1: Direct Prompt Copy

1. Open `skill.md`
2. Copy the entire content under `## Skill Prompt`
3. Upload your PDF literature to SOLO
4. Paste the prompt and send

### Option 2: As a SOLO User Skill

If SOLO supports custom user skills:

1. Place `skill.md` in your SOLO skills directory
2. Invoke with: "Use the literature-analysis skill to analyze this paper"
3. SOLO will automatically load the skill prompt

### Option 3: GitHub Integration

1. Push this repository to your GitHub account
2. Reference the raw URL of `skill.md` in your SOLO configuration
3. SOLO can fetch and use the skill prompt remotely

## Customization

### Analysis Scope

Edit the prompt in `skill.md` to adjust:

- **Sections to analyze**: Add/remove sections (Abstract, Introduction, Methods, Results, Discussion)
- **Figure depth**: Brief (1-2 sentences) vs. detailed (full experimental description)
- **Language**: Change translation language (default: Chinese)
- **Additional sections**: Add innovation scoring, relevance analysis, etc.

### Variants

| Variant | File | Description |
|---------|------|-------------|
| Quick | `variants/quick-analysis.md` | Abstract + key figures only, ~5 min per paper |
| Full | `variants/full-analysis.md` | All sections, ~15 min per paper |
| Batch | `variants/batch-analysis.md` | Multiple papers in one report |

## Requirements

- SOLO with PDF reading capability
- PDF literature file (English recommended)
- Output: .docx format

## License

MIT License - Free to use, modify, and distribute.

## Author

Created for scientific literature analysis workflow.
