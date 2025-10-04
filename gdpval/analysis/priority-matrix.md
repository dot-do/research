# GDPval-Based Example Priority Matrix

**Purpose:** Prioritize Business-as-Code example creation based on AI performance data

## Priority Scoring

**Formula:** Priority = AI Performance × Economic Impact × Task Volume

### Factors

1. **AI Performance** (0-100): GDPval win/tie rate
2. **Economic Impact** (1-5): Contribution to GDP/wages
3. **Task Volume** (1-5): Repeatability and scale

## Priority Tiers

### Tier 1: HIGHEST PRIORITY (Score 300+)

**Target: 12-15 examples**

| Occupation | AI % | Economic | Volume | Score | Examples |
|------------|------|----------|--------|-------|----------|
| Counter/Rental Clerks | 81 | 4 | 5 | 405 | 4 |
| Shipping/Inventory Clerks | 76 | 4 | 5 | 380 | 4 |
| Order Clerks | 70 | 4 | 5 | 350 | 4 |

**Why Prioritize:**
- Highest AI success rates (75-81%)
- High-volume, repeatable tasks
- Clear automation ROI
- Proven AI capability

**Example Categories:**
- Agents: InventoryClerk, OrderProcessor, RentalAgent, ShippingCoordinator
- Workflows: processOrder, trackShipment, handleReturn, manageInventory
- Functions: validateOrder, calculateShipping
- Integrations: ShopifyOrders, UPSTracking

---

### Tier 2: HIGH PRIORITY (Score 200-299)

**Target: 15-18 examples**

| Occupation | AI % | Economic | Volume | Score | Examples |
|------------|------|----------|--------|-------|----------|
| Software Developers | 65 | 5 | 4 | 260 | 6 |
| Private Investigators | 60 | 3 | 3 | 180 | 2 |
| Sales Representatives | 55 | 5 | 4 | 220 | 3 |
| Customer Service Reps | 55 | 4 | 5 | 275 | 4 |

**Why Prioritize:**
- Strong AI performance (55-65%)
- High economic value
- Knowledge work automation
- Scalable applications

**Example Categories:**
- **Software Development:**
  - Agents: CodeReviewer, BugTriager, TestGenerator, SecurityAuditor, DocumentationWriter
  - Workflows: deployApplication, reviewPullRequest, fixBug, releaseVersion, runTests
  - Functions: parseCode, generateDocs, analyzePerformance
  - Sources: GitHubActivity, JiraTickets

---

### Tier 3: MODERATE PRIORITY (Score 150-199)

**Target: 18-20 examples**

| Occupation | AI % | Economic | Volume | Score | Examples |
|------------|------|----------|--------|-------|----------|
| Financial Advisors | 45 | 5 | 3 | 180 | 3 |
| Lawyers | 45 | 5 | 2 | 180 | 3 |
| Accountants | 45 | 5 | 3 | 180 | 3 |
| Pharmacists | 42 | 4 | 4 | 168 | 3 |
| Registered Nurses | 40 | 5 | 4 | 200 | 3 |
| Real Estate Agents | 50 | 4 | 3 | 200 | 3 |

**Why Prioritize:**
- Moderate AI performance (40-50%)
- High economic value
- Augmentation over replacement
- Professional services market

**Example Categories:**
- **Financial Services:**
  - Agents: FinancialAdvisor, TaxAdvisor
  - Workflows: analyzeInvestment, prepareAudit, generateTaxReturn
  - Functions: calculateROI, assessRisk
  - Schemas: InvestmentPortfolio

- **Legal:**
  - Agents: LegalResearcher, ContractReviewer
  - Workflows: reviewContract
  - Schemas: LegalCase

- **Healthcare:**
  - Agents: MedicalTriager, PharmacyChecker
  - Workflows: assessPatient, dispenseMedication
  - Schemas: PatientRecord

---

### Tier 4: LOW PRIORITY (Score <150)

**Target: 0-5 examples (tool assistance only)**

| Occupation | AI % | Economic | Volume | Score | Examples |
|------------|------|----------|--------|-------|----------|
| Industrial Engineers | 17 | 4 | 2 | 68 | 0 |
| Film/Video Editors | 17 | 3 | 2 | 51 | 0 |
| Audio/Video Technicians | 2 | 3 | 2 | 6 | 0 |
| Producers/Directors | 20 | 3 | 1 | 20 | 0 |
| Mechanical Engineers | 25 | 4 | 2 | 100 | 1 |

**Why De-prioritize:**
- Low AI performance (<25%)
- Creative or physical work
- Better suited for tool assistance
- Limited automation potential

**Approach:**
- Focus on tool plugins rather than full automation
- Asset management and organization
- Template generation
- Quality checks

---

## Implementation Plan

### Phase 1: Clerks & Operations (Tier 1)
**12 examples** - Highest ROI
- 4 Agents
- 4 Workflows
- 2 Functions
- 2 Integrations

**Rationale:** 75-81% AI performance, immediate business value

### Phase 2: Software Development (Tier 2)
**15 examples** - High developer demand
- 5 Agents
- 5 Workflows
- 3 Functions
- 2 Sources

**Rationale:** 65% AI performance, strong tool ecosystem

### Phase 3: Professional Services (Tier 3)
**18 examples** - Professional market
- 6 Agents
- 6 Workflows
- 3 Functions
- 3 Schemas

**Rationale:** 40-50% AI performance, augmentation use cases

### Phase 4: Specialized (As Needed)
**5-10 examples** - Fill gaps
- Sales and marketing automation
- Real estate workflows
- Social workers and case management
- Journalists and content creation

---

## Total Example Count

- **Current:** 9 examples (baseline)
- **Phase 1:** +12 = 21 total
- **Phase 2:** +15 = 36 total
- **Phase 3:** +18 = 54 total
- **Phase 4:** +9 = **63 total examples**

---

## Success Metrics

### Coverage Goals

- ✅ 20+ occupations from GDPval's 44
- ✅ All 9 economic sectors represented
- ✅ 3-5 examples per category folder
- ✅ 80%+ examples in Tier 1-2 occupations

### Quality Standards

- ✅ All examples follow mdxld pattern
- ✅ Proper naming conventions (camelCase verbs, TitleCase nouns)
- ✅ Cross-references using Obsidian links
- ✅ TypeScript functions only for complex logic (5-20%)
- ✅ Real-world task basis from GDPval/O*NET

### Business Value

- ✅ Focus on highest AI performance tasks
- ✅ Clear automation ROI potential
- ✅ Scalable and repeatable workflows
- ✅ Industry-standard integrations

---

## References

- [[task-performance.md]] - Detailed performance analysis
- [[example-categories.md]] - Complete taxonomy
- GDPval Dataset: https://huggingface.co/datasets/openai/gdpval
