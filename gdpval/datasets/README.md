# GDPval Dataset Information

## Overview

**Source:** https://huggingface.co/datasets/openai/gdpval
**Paper:** https://cdn.openai.com/pdf/d5eb7428-c4e9-4a33-bd86-86dd4bcf12ce/GDPval.pdf

### Dataset Characteristics

- **Total Tasks:** 220 real-world knowledge tasks
- **Number of Occupations:** 44
- **Number of Sectors:** 9
- **Subset:** Gold subset for evaluation
- **Format:** Parquet files
- **Modalities:** Audio, Document, Image, Text, Video

### Dataset Structure

- **Split:** train
- **Total Rows:** 220
- **Fields:** Each task includes a text prompt and supporting reference files

### Access Methods

```python
# Using Hugging Face datasets library
from datasets import load_dataset

dataset = load_dataset("openai/gdpval")
```

### Key Features

1. **Real-World Tasks:** Professionally validated tasks from actual occupations
2. **Multi-Modal:** Includes various input types (audio, video, documents, images, text)
3. **Economically Valuable:** Tasks represent genuine work activities with economic value
4. **Diverse Sectors:** Covers 9 major economic sectors

### Important Notes

- Some tasks may include sensitive content (NSFW themes)
- Tasks are professionally validated
- Gold subset provides 220 high-quality evaluation tasks

## Dataset Files

The dataset can be downloaded using the Hugging Face datasets library. Files are stored in Parquet format on Hugging Face servers.

### Local Storage

- **Location:** `/Users/nathanclevenger/Projects/.do/research/gdpval/datasets/`
- **Paper PDF:** `../papers/GDPval.pdf` (11.2MB)

## Related Resources

- **O*NET Database:** https://www.onetcenter.org/database.html
- **O*NET Version:** 30.0
- **License:** Creative Commons Attribution 4.0 International
