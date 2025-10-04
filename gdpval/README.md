# GDPval Research Repository

**Purpose:** Research and analysis of OpenAI's GDPval benchmark to guide Business-as-Code example creation

## Overview

GDPval (GDP Evaluation) is OpenAI's benchmark measuring AI model performance on 1,320 real-world tasks across 44 occupations in 9 economic sectors. This research informs our example prioritization strategy.

## Folder Structure

```
research/gdpval/
├── README.md (this file)
├── papers/          # Research papers and PDFs
├── datasets/        # Hugging Face dataset info
├── onet-data/       # O*NET occupational data
└── analysis/        # Our analysis documents
    ├── task-performance.md     # Performance by occupation/sector
    ├── priority-matrix.md      # Example prioritization scoring
    └── example-categories.md   # Taxonomy and templates
```

## Key Findings

### Top Performing Occupations
1. **Counter/Rental Clerks** - 81% AI performance
2. **Shipping/Inventory Clerks** - 76% AI performance
3. **Software Developers** - 65% AI performance

### Best Performing Sectors
1. Government
2. Retail Trade
3. Wholesale Trade

### Weakest Performers
- Industrial Engineers: 17%
- Film/Video Editors: 17%
- Audio/Video Technicians: 2%

## Example Strategy

Based on this research, we prioritize examples in three tiers:

### Tier 1: Clerks & Operations (12 examples)
- **Why:** 75-81% AI performance
- **Focus:** Inventory, orders, shipping, rentals
- **ROI:** Immediate automation value

### Tier 2: Software Development (15 examples)
- **Why:** 65% AI performance
- **Focus:** Code review, testing, deployment, docs
- **ROI:** High developer demand

### Tier 3: Professional Services (18 examples)
- **Why:** 40-50% AI performance
- **Focus:** Finance, legal, healthcare
- **ROI:** Augmentation over replacement

**Target:** 63 total examples across all categories

## Data Sources

### Primary Sources

**GDPval Paper**
- URL: https://cdn.openai.com/pdf/d5eb7428-c4e9-4a33-bd86-86dd4bcf12ce/GDPval.pdf
- Size: Large (>10MB, download manually if needed)
- Content: Full methodology, results, task examples

**Hugging Face Dataset**
- URL: https://huggingface.co/datasets/openai/gdpval
- Size: 342KB (download size), 597KB (dataset size)
- Content: 220 tasks across 44 occupations
- Format: JSON with task_id, sector, occupation, prompt, reference_files

**O*NET Database**
- URL: https://www.onetcenter.org/database.html
- Version: 30.0
- Content: 923 occupations, tasks, skills, work activities
- Files: Tasks.txt, Skills.txt, Work Activities.txt
- API: https://services.onetcenter.org

### Secondary Sources

- OpenAI Blog: https://openai.com/index/gdpval/
- Fortune Article: https://fortune.com/2025/09/30/ai-models-are-already-as-good-as-experts-at-half-of-tasks-a-new-openai-benchmark-gdpval-suggests/
- TechCrunch Coverage: https://techcrunch.com/2025/09/25/openai-says-gpt-5-stacks-up-to-humans-in-a-wide-range-of-jobs/

## Analysis Documents

### 1. [[analysis/task-performance.md]]

Complete breakdown of GDPval performance results:
- Performance by occupation (81% to 2%)
- Performance by sector (government to manufacturing)
- Task characteristics (what works vs what doesn't)
- Example tasks from the benchmark
- Implications for automation

### 2. [[analysis/priority-matrix.md]]

Scoring system for example prioritization:
- Priority = AI Performance × Economic Impact × Task Volume
- Tier 1-4 classification
- Implementation phases
- Target example counts
- Success metrics

### 3. [[analysis/example-categories.md]]

Complete taxonomy for Business-as-Code examples:
- 6 category types (Agents, Workflows, Functions, Schemas, Sources, Integrations)
- Naming conventions (camelCase verbs, TitleCase nouns)
- mdxld pattern requirements
- Occupational mapping
- Templates for each category
- Quality checklist

## How to Use This Research

1. **Prioritize Examples:**
   - Start with [[analysis/priority-matrix.md]]
   - Focus on Tier 1-2 occupations first
   - Use scoring system to justify decisions

2. **Create Examples:**
   - Follow [[analysis/example-categories.md]] taxonomy
   - Use templates provided
   - Base tasks on real GDPval/O*NET work activities
   - Apply proper naming conventions

3. **Validate Quality:**
   - Check against [[analysis/task-performance.md]]
   - Ensure examples match high-performance tasks
   - Verify real-world applicability

## Downloads (Manual)

Due to file sizes, manual download may be required:

```bash
# GDPval paper (if WebFetch fails)
# Visit: https://cdn.openai.com/pdf/d5eb7428-c4e9-4a33-bd86-86dd4bcf12ce/GDPval.pdf
# Save to: research/gdpval/papers/GDPval.pdf

# Hugging Face dataset (via huggingface-cli or web)
# Install: npm install -g @huggingface/hub
# Download: huggingface-cli download openai/gdpval
# Or visit: https://huggingface.co/datasets/openai/gdpval/tree/main

# O*NET database files
# Visit: https://www.onetcenter.org/database.html
# Download: O*NET 30.0 Database (Excel format)
# Files: Tasks.xlsx, Skills.xlsx, Work Activities.xlsx
```

## Next Steps

1. ✅ Research complete (this folder)
2. ⏳ Reorganize existing 9 examples
3. ⏳ Create Tier 1 examples (clerks/operations)
4. ⏳ Create Tier 2 examples (software development)
5. ⏳ Create Tier 3 examples (professional services)

## References

- OpenAI GDPval: https://openai.com/index/gdpval/
- O*NET Center: https://www.onetcenter.org
- Examples Repository: [[../../examples/]]
- Project CLAUDE.md: [[../../CLAUDE.md]]

---

**Last Updated:** 2025-10-04
**Status:** Research complete, ready for implementation
**Maintained By:** Claude Code
