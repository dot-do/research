# Business-as-Code Example Categories

**Based on:** GDPval occupational task analysis and O*NET work activities

## Category Taxonomy

### 1. 🤖 Agents (AI Entities)

**Pattern:** TitleCase nouns
**Naming:** `{Occupation}{Role}.mdx` or `{Function}Agent.mdx`

**Examples:**
- `SalesAgent.mdx`, `SupportAgent.mdx`
- `InventoryClerk.mdx`, `OrderProcessor.mdx`
- `CodeReviewer.mdx`, `FinancialAdvisor.mdx`

**Structure:**
```yaml
$type: Agent
name: AgentName
description: Brief description
capabilities: [list]
model: {provider, model, temperature}
systemPrompt: |
  Instructions
functions: [list]
memory: {type, config}
```

---

### 2. 🔄 Workflows (Business Processes)

**Pattern:** camelCase verbs
**Naming:** `{verb}{Object}.mdx` or `{action}Process.mdx`

**Examples:**
- `processPayment.mdx`, `onboardCustomer.mdx`
- `processOrder.mdx`, `trackShipment.mdx`
- `reviewContract.mdx`, `deployApplication.mdx`

**Structure:**
```yaml
$type: Workflow
name: workflowName
description: Brief description
trigger: {type, config}
input: {fields}
steps: [array of steps]
output: {fields}
timeout: number
```

---

### 3. ⚡ Functions (Reusable Logic)

**Pattern:** camelCase verbs
**Naming:** `{verb}{Object}.mdx` or `{action}.mdx`

**Examples:**
- `sendEmail.mdx`, `calculateShipping.mdx`
- `validateOrder.mdx`, `parseCode.mdx`
- `assessRisk.mdx`, `checkCompliance.mdx`

**Structure:**
```yaml
$type: Function
name: functionName
description: Brief description
input: {fields with descriptions}
output: {fields with descriptions}
config: {settings}
```

**Optional TypeScript:** For complex transformations (5-20% of cases)

---

### 4. 💾 Schemas (Database Structures)

**Pattern:** TitleCase nouns
**Naming:** `{Entity}Database.mdx` or `{Domain}Schema.mdx`

**Examples:**
- `CustomerDatabase.mdx`, `InvestmentPortfolio.mdx`
- `PatientRecord.mdx`, `LegalCase.mdx`

**Structure:**
```yaml
$type: Schema
name: SchemaName
description: Brief description
tables:
  tableName:
    field: Description (type if not string)
indexes: [list]
queries: [named queries with SQL]
```

---

### 5. 📊 Sources (Data Import)

**Pattern:** TitleCase nouns
**Naming:** `{System}Data.mdx` or `{Source}Import.mdx`

**Examples:**
- `WeatherData.mdx`, `CensusDemographics.mdx`
- `GitHubActivity.mdx`, `JiraTickets.mdx`

**Structure:**
```yaml
$type: Source
name: sourceName
description: Brief description
provider: domain.com
api: {baseUrl, authentication, rateLimit}
extract: {config}
refresh: {schedule, strategy}
schema: {fields}
load: {table, strategy}
```

**Optional TypeScript:** For complex ETL transformations

---

### 6. 🔌 Integrations (Third-Party APIs)

**Pattern:** TitleCase nouns
**Naming:** `{Service}Integration.mdx` or `{Platform}Webhooks.mdx`

**Examples:**
- `StripeWebhooks.mdx`, `ShopifyOrders.mdx`
- `UPSTracking.mdx`, `SlackNotifications.mdx`

**Structure:**
```yaml
$type: Integration
name: integrationName
description: Brief description
provider: domain.com
authentication: {config}
webhooks: {endpoint, events}
rateLimit: {config}
handlers: {event: function mapping}
```

**Optional TypeScript:** For event handlers and complex business logic

---

## Example Distribution by Category

### Current (9 examples)

- Agents: 2 (22%)
- Workflows: 2 (22%)
- Functions: 1 (11%)
- Schemas: 1 (11%)
- Sources: 2 (22%)
- Integrations: 1 (11%)

### Target (63 examples)

- Agents: 20 (32%)
- Workflows: 20 (32%)
- Functions: 10 (16%)
- Schemas: 5 (8%)
- Sources: 4 (6%)
- Integrations: 4 (6%)

---

## Occupational Mapping

### Tier 1: Clerks & Operations (12 examples)

**Occupations:** Counter clerks, shipping clerks, inventory clerks, order clerks

| Category | Count | Examples |
|----------|-------|----------|
| Agents | 4 | InventoryClerk, OrderProcessor, RentalAgent, ShippingCoordinator |
| Workflows | 4 | processOrder, trackShipment, handleReturn, manageInventory |
| Functions | 2 | validateOrder, calculateShipping |
| Integrations | 2 | ShopifyOrders, UPSTracking |

**O*NET Tasks:**
- Receive and process orders
- Track inventory levels
- Coordinate shipping and receiving
- Handle customer transactions
- Manage rental equipment

---

### Tier 2: Software Development (15 examples)

**Occupations:** Software developers, QA analysts, DevOps engineers

| Category | Count | Examples |
|----------|-------|----------|
| Agents | 5 | CodeReviewer, BugTriager, TestGenerator, SecurityAuditor, DocumentationWriter |
| Workflows | 5 | deployApplication, reviewPullRequest, fixBug, releaseVersion, runTests |
| Functions | 3 | parseCode, generateDocs, analyzePerformance |
| Sources | 2 | GitHubActivity, JiraTickets |

**O*NET Tasks:**
- Write and review code
- Test software applications
- Debug and fix issues
- Deploy applications
- Create documentation

---

### Tier 3: Professional Services (18 examples)

**Occupations:** Financial advisors, lawyers, accountants, pharmacists, nurses

#### Finance & Accounting (6 examples)

| Category | Count | Examples |
|----------|-------|----------|
| Agents | 2 | FinancialAdvisor, TaxAdvisor |
| Workflows | 2 | analyzeInvestment, prepareAudit, generateTaxReturn |
| Functions | 1 | calculateROI, assessRisk |
| Schemas | 1 | InvestmentPortfolio |

#### Legal (5 examples)

| Category | Count | Examples |
|----------|-------|----------|
| Agents | 2 | LegalResearcher, ContractReviewer |
| Workflows | 2 | reviewContract, prepareCase |
| Functions | 0 | checkCompliance |
| Schemas | 1 | LegalCase |

#### Healthcare (7 examples)

| Category | Count | Examples |
|----------|-------|----------|
| Agents | 2 | MedicalTriager, PharmacyChecker |
| Workflows | 3 | assessPatient, dispenseMedication, scheduleAppointment |
| Functions | 1 | checkDrugInteractions |
| Schemas | 1 | PatientRecord |

**O*NET Tasks:**
- **Finance:** Analyze investments, prepare tax returns, audit financials
- **Legal:** Research case law, review contracts, prepare legal documents
- **Healthcare:** Assess patients, dispense medications, document care

---

## Cross-References Pattern

Use Obsidian-style wiki links for related examples:

**Within same folder:**
```mdx
[[SalesAgent|Sales Agent]]
```

**Cross-folder:**
```mdx
[[../workflows/processPayment|Process Payment Workflow]]
[[../../agents/SupportAgent|Support Agent]]
```

**Common patterns:**
- Agents → Workflows (agent uses workflow)
- Workflows → Functions (workflow calls functions)
- Workflows → Integrations (workflow triggers webhooks)
- Sources → Schemas (source populates schema)

---

## Example Templates by Category

### Agent Template
```mdx
---
$type: Agent
name: AgentName
description: One-line description

capabilities:
  - capability-1
  - capability-2

model:
  provider: anthropic
  model: claude-3-5-sonnet-20241022
  temperature: 0.2

systemPrompt: |
  You are a helpful agent that...

functions:
  - function-1
  - function-2

memory:
  type: conversation
  maxTokens: 10000
---

# Agent Name

Detailed description...

## Capabilities

## Usage

## Related

- [[RelatedExample]]
```

### Workflow Template
```mdx
---
$type: Workflow
name: workflowName
description: One-line description

trigger:
  type: api
  method: POST
  path: /endpoint

input:
  field1: Description
  field2: Description (type)

steps:
  - name: step-1
    function: function-name
    input:
      field: ${input.field1}

output:
  result: Description
---

# Workflow Name

Detailed description...

## Flow

## Steps

## Related

- [[RelatedExample]]
```

### Function Template
```mdx
---
$type: Function
name: functionName
description: One-line description

input:
  field1: Description
  field2: Description (type)

output:
  result: Description
  status: Description
---

# Function Name

Detailed description...

## Usage

## Related

- [[RelatedExample]]
```

---

## Quality Checklist

For each example:

- [ ] Follows mdxld pattern
- [ ] YAML frontmatter starts with `$type`
- [ ] Proper naming convention (camelCase verbs, TitleCase nouns)
- [ ] Field descriptions in values (types in parentheses if not string)
- [ ] Cross-references use Obsidian-style `[[links]]`
- [ ] YAML blocks for data examples (not JSON)
- [ ] TypeScript functions only where needed (5-20%)
- [ ] Based on real GDPval/O*NET tasks
- [ ] Related examples linked
- [ ] Complete documentation section

---

## References

- [[task-performance.md]] - GDPval performance data
- [[priority-matrix.md]] - Example prioritization
- O*NET Database: https://www.onetcenter.org/database.html
- GDPval Dataset: https://huggingface.co/datasets/openai/gdpval
