# GDPval Task Performance Analysis

**Source:** OpenAI GDPval Benchmark (September 2025)

## Overview

GDPval measures AI model performance on 1,320 real-world tasks across 44 occupations in 9 economic sectors. The gold open-source subset contains 220 tasks.

**Dataset:** https://huggingface.co/datasets/openai/gdpval
**Paper:** https://cdn.openai.com/pdf/d5eb7428-c4e9-4a33-bd86-86dd4bcf12ce/GDPval.pdf

## Top Performing AI Model

**Claude Opus 4.1** (Anthropic) - Best overall performer
- 47.6% of tasks completed at or above human expert level
- 100x faster and 100x cheaper than human experts

**GPT-5-high** (OpenAI)
- 40.6% of tasks at or above expert level

## Performance by Occupation (Highest to Lowest)

### Tier 1: Exceptional Performance (75%+ Win/Tie Rate)

**Counter and Rental Clerks** - 81%
- Highest AI performance across all occupations
- Tasks: Rental agreements, customer service, inventory tracking

**Shipping, Receiving, and Inventory Clerks** - 76%
- Second highest performance
- Tasks: Shipment coordination, inventory management, logistics

### Tier 2: Strong Performance (50-75%)

**Software Developers** - High performance (exact % not disclosed)
- Code review, bug triage, documentation
- Test generation, security auditing

**Private Detectives and Investigators** - Strong performance
- Research and analysis tasks
- Information gathering and verification

**Order Clerks** - High performance in government/retail
- Order processing and validation
- Customer communication

### Tier 3: Moderate Performance (40-50%)

**Financial Advisors**
- Investment analysis and recommendations
- Portfolio management

**Lawyers**
- Legal research and contract review
- Case analysis (e.g., 3,500-word legal memos)

**Accountants**
- Financial analysis and audit preparation
- Tax planning

**Registered Nurses**
- Patient assessment and care planning
- Medical documentation

**Pharmacists**
- Drug interaction checking
- Prescription verification

### Tier 4: Weak Performance (<40%)

**Industrial Engineers** - 17%
- Complex manufacturing and process optimization

**Film and Video Editors** - 17%
- Creative editing and storytelling

**Audio and Video Technicians** - 2%
- Lowest performance
- Technical production work

**Producers and Directors**
- Creative direction and production management

## Performance by Sector

### Best Performing Sectors

1. **Government** - Highest overall performance
2. **Retail Trade** - Strong clerical task performance
3. **Wholesale Trade** - High logistics and operations performance

### Moderate Performing Sectors

4. **Information** - Mixed results (software strong, A/V weak)
5. **Finance and Insurance** - Moderate professional services
6. **Healthcare** - Moderate clinical tasks
7. **Real Estate**
8. **Professional Services**

### Weakest Performing Sector

9. **Manufacturing** - Lowest overall performance
   - Complex engineering tasks
   - Physical process optimization

## Task Characteristics

### High Performance Tasks

- **Structured clerical work**: Order processing, inventory tracking
- **Data analysis**: Financial analysis, legal research
- **Document generation**: Reports, documentation, contracts
- **Pattern recognition**: Fraud detection, risk assessment
- **Information synthesis**: Research, summarization

### Low Performance Tasks

- **Creative work**: Video editing, production direction
- **Physical coordination**: Manufacturing engineering, A/V technical work
- **Complex spatial reasoning**: Industrial engineering, blueprint design
- **Subjective judgment**: Creative direction, artistic decisions

## Task Complexity

Unlike traditional benchmarks, GDPval tasks:
- Include reference files and context
- Require multiple document types (Word, Excel, PowerPoint, diagrams)
- Span 30+ tasks per occupation (1,320 total, 220 in gold set)
- Created by experts with 14+ years average experience
- Represent real work products (legal briefs, engineering blueprints, care plans)

## Example Tasks

1. **Legal**: 3,500-word legal memo on Delaware law standard of review
2. **Customer Service**: Email response to dissatisfied customer requesting return
3. **Operations**: Optimize table layout for Spring vendor fair
4. **Finance**: Audit price inconsistencies in purchase orders

## Implications for Business-as-Code

### Prioritize High-Performance Occupations

1. **Clerks and Operations** (75-81% AI performance)
   - Immediate ROI potential
   - Clear automation opportunities
   - High volume, repeatable tasks

2. **Software Development** (50-75%)
   - Code generation and review
   - Testing and quality assurance
   - Documentation automation

3. **Professional Services** (40-50%)
   - Augment rather than replace
   - Research and analysis tasks
   - Document preparation

### De-prioritize Low-Performance Occupations

- Manufacturing engineering (<20%)
- Creative A/V production (<20%)
- Focus on tool assistance rather than full automation

## References

- OpenAI GDPval Announcement: https://openai.com/index/gdpval/
- Hugging Face Dataset: https://huggingface.co/datasets/openai/gdpval
- O*NET Database: https://www.onetcenter.org/database.html
