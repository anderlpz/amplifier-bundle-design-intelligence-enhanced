# Design Research Capability - Usage Instructions

This document explains how to use the design research capability for creative, purpose-driven trend analysis.

---

## Overview

The design research capability operates on two layers:

**Layer 1: Lightweight Index (automated, periodic)**
- RSS feed collection from Awwwards, Siteinspire, The FWA
- Structured archive with 30-day rolling trend summary
- Near-zero token cost — no site visits, no analysis

**Layer 2: Targeted Analysis (on-demand, scoped)**
- Purpose-driven research by cognitive task across domains
- Selective site visits via browser-tester with nano-banana visual analysis
- Research-question-specific analysis — not generic site descriptions
- Knowledge curation — learnings saved to the knowledge base with user confirmation

The index keeps you aware of what's winning awards. The analysis goes deep only when you have a real research question. This means you learn from sites instead of hoarding data about them.

---

## What's New: Creative Research Methodology

**Design-intelligence now researches by PURPOSE, not CATEGORY.**

### The Old Way (Category-Matching)
```
User: "Design a healthcare dashboard"
Research: Healthcare dashboard examples
Output: Competent remix of existing healthcare UIs
```

### The New Way (Purpose-Driven)
```
User: "Design a healthcare dashboard"
Decompose: Cognitive tasks > "rapid assessment", "anomaly detection", "decision support"
Map: Analogous domains > medical monitors, trading platforms, security ops, gaming HUDs
Research: 20% healthcare + 50% purpose-driven + 30% divergent
Extract: Level 3-4 patterns (interaction/cognitive, not just visual)
Output: Creative work grounded in proven patterns from unexpected sources
```

**Result**: Designs that feel fresh and innovative while being grounded in proven patterns — just from unexpected places.

---

## Core Methodology

Design research follows **Creative Research Methodology**:

See: `@design-intelligence:context/research-methodology/creative-research-methodology.md`

### Key Resources
- **Creative Research Methodology** - Purpose-driven research approach
- **Cognitive Task Catalog** - Common tasks + analogous domains
- **Pattern Abstraction Guide** - Extracting Level 3-4 patterns
- **Cognitive Discovery Enhancement** - Bridging discovery to research

All in: `context/research-methodology/`

---

## Components

### Agents

**research-analyst** - Creative research specialist
- Conducts purpose-driven research by cognitive task
- Extracts Level 3-4 patterns from unexpected sources
- Synthesizes with explicit reasoning
- Conversational interface for design insights
- **Targeted site analysis** via browser-tester + nano-banana
- **Knowledge curation** — proposes saving learnings with user confirmation
- **Uses**: Creative research methodology (multi-vector research)

**research-runner** - Lightweight collection agent
- Fetches design trend data from RSS feeds
- Generates trend summaries and updates archive index
- Does NOT visit or analyze sites — that's the research-analyst's job
- Used via the weekly-design-research recipe or direct invocation

### Recipe

**weekly-design-research** - Automated research workflow
- Fetches RSS feeds from Awwwards, Siteinspire, The FWA
- Generates monthly summary
- Updates 30-day archive index
- Takes 2-5 minutes to complete

### Tools Used (On-Demand)

**browser-tester** - Site visits during targeted analysis (research-analyst Mode B)
- Visits sites and captures full-page screenshots as working artifacts

**nano-banana** - Visual analysis of screenshots through research-question-specific prompts
- Analyzes screenshots with targeted prompts, not generic descriptions

---

## Usage Patterns

### Pattern 1: Creative Project Research

**When**: Starting a new design project

**What you get**: Cross-domain inspiration with explicit reasoning

**How**:
```
In a design-intelligence session:

> I need to design a launch status dashboard for rocket missions

Research-analyst will:
1. Ask about cognitive tasks ("What is the user's brain doing?")
2. Map to analogous domains (medical monitors, trading platforms, gaming HUDs)
3. Conduct multi-vector research (domain-specific, purpose-driven, divergent)
4. Extract Level 3-4 patterns (interaction/cognitive, not visual)
5. Synthesize with reasoning about WHY each source is relevant
```

**Output**: Research report with unexpected sources and transferable patterns

---

### Pattern 2: Current Trend Analysis

**When**: Need to know "what's trending now?"

**What you get**: Recent patterns from award-winning sites

**How**:
```
In a design-intelligence session:

> What are current trends in web animation?
> Show me examples of dark mode with vibrant accents
> How have grid layouts evolved in the last 3 months?
```

**Output**: Trend analysis from archive with specific examples

---

### Pattern 3: Running Periodic Research Updates

**When**: Weekly or bi-weekly to maintain current data

**Prerequisites**: Recipes tool required (included in foundation)

**Option 1: Using the Recipe (Recommended)**

Conversational:
```
execute design-intelligence:recipes/weekly-design-research.yaml with year=2026 month=01 month_name=january date=2026-01-27
```

CLI:
```bash
amplifier tool invoke recipes \
  operation=execute \
  recipe_path=design-intelligence:recipes/weekly-design-research.yaml \
  context='{"year": "2026", "month": "01", "month_name": "january", "date": "2026-01-27"}'
```

The recipe automatically:
- Creates directory structure
- Fetches RSS feeds from all sources (Awwwards, Siteinspire, The FWA)
- Generates summaries
- Updates archive index

**Option 2: Manual Execution**

Use the task tool to invoke research-runner:
```
Use the research-runner agent to fetch RSS feeds from Awwwards for this week
Use the research-runner agent to generate the monthly summary
```

---

### Pattern 4: Knowledge Curation

**When**: After a research session surfaces valuable design learnings

**What you get**: Persistent design knowledge that compounds over time

**How**:
```
After any research session, the research-analyst offers to save learnings:

> "From this research, I found a pattern worth saving:
>
> Typography as hierarchy signal in dense dashboards: Condensed bold
> sans-serifs create scannable headers without competing with data values.
>
> Save to .design/observed-expression/typography-personalities.md?"

If you confirm, the learning is written to your project's local knowledge base.
If you decline, the insight was still useful in the research synthesis.
```

**Output**: Growing knowledge base in `.design/observed-expression/` that informs future research

---

## Example Workflows

### Workflow 1: Purpose-Driven Project Research

**Goal**: Get creative inspiration for a new project

**Steps**:
```
1. Start design-intelligence session

2. Request research:
   > I need to design a mission launch dashboard

3. Answer cognitive task questions:
   - What is the user's brain doing? (rapid assessment, anomaly detection)
   - What decisions do they make? (go/no-go, investigate, share)
   - What's their emotional state? (focused monitoring with alert-driven urgency)

4. Receive multi-vector research:
   - Domain-specific: NASA, SpaceX dashboards (know the conventions)
   - Purpose-driven: Medical monitors, trading platforms, gaming HUDs (proven patterns)
   - Divergent: Game studios, luxury brands, physical analogs (breakthrough ideas)

5. Get pattern synthesis with reasoning:
   - "From hospital monitors: Gestalt assessment principle - design for 200ms comprehension"
   - "From trading platforms: Real-time anomaly highlighting with confidence indicators"
   - "From gaming HUDs: Critical info hierarchy without disrupting flow state"
```

---

### Workflow 2: Weekly Research Update

**Goal**: Maintain current trend data

**Steps**:
```bash
# 1. Run RSS feed collection (takes 2-5 min)
amplifier tool invoke recipes \
  operation=execute \
  recipe_path=design-intelligence:recipes/weekly-design-research.yaml \
  context='{"year": "2026", "month": "01", "month_name": "january", "date": "2026-01-27"}'

# 2. Review results
amplifier tool invoke recipes operation=list

# 3. Query insights (in a session)
> What trends emerged from this week's research?
```

---

### Workflow 3: Competitive Analysis

**Goal**: Understand patterns in a specific domain

**Steps**:
```
In a design-intelligence session:

> Show me all e-commerce sites from the last 2 months
> How do they handle product galleries?
> What's the most common navigation pattern?

Analyst searches archive and synthesizes patterns.
```

---

## Research Modes Available

### Mode A: Archive Analysis (Current Trends)
Query the design archive for recent visual patterns.

**Use when**: "What's trending now?" or examples from award-winning sites

### Mode B: Targeted Site Analysis
Visit and analyze specific sites through a research-question-specific lens using browser-tester for screenshots and nano-banana for visual analysis.

**Use when**: User shares a URL and wants pattern extraction, or the research-analyst identifies archive sites worth analyzing deeply during Mode C research. The analysis prompt is tailored to the active research question — not a generic "describe this site."

### Mode C: Cross-Domain Research (Purpose-Driven)
Multi-vector research by cognitive task.

**Use when**: Starting a design project, need creative inspiration

**This is the breakthrough mode** - produces genuinely creative work.

---

## Archive Structure

```
archive/
+-- 2026/
|   +-- 01-january/
|   |   +-- raw/
|   |   |   +-- awwwards-2026-01-27.json
|   |   |   +-- siteinspire-2026-01-27.json
|   |   |   +-- thefwa-2026-01-27.json
|   |   +-- summary.md
|   +-- 02-february/
|       +-- ...
+-- archive-index.md
```

### File Descriptions

**raw/*.json** - Structured project data from RSS feeds (titles, URLs, categories, tags)
**summary.md** - Monthly trend summary (LLM-optimized)
**archive-index.md** - 30-day rolling summary (<500 tokens, pre-loaded in every session)

The archive is intentionally lightweight. No screenshots, no visual analysis artifacts. Visual analysis happens on-demand during research sessions — screenshots are working artifacts that exist only for the duration of the analysis.

---

## Best Practices

### For Creative Research

1. **Clarify cognitive tasks** before researching visuals
2. **Research outside obvious categories** (purpose over category)
3. **Extract Level 3-4 patterns** (interaction/cognitive, not visual)
4. **Synthesize with reasoning** (WHY each source is relevant)
5. **Challenge assumptions** from domain-specific research

### For Running Research Updates

1. **Run weekly** to maintain current data
2. **Review summary.md** after each update to verify quality
3. **Monitor archive size** - consider archiving old months after 6 months
4. **Validate outputs** before relying on summaries

### For Querying Insights

1. **Start with archive-index.md** for quick trends
2. **Ask specific questions** for better responses
3. **Request examples** to see real implementations
4. **Compare across time** to understand evolution
5. **Load monthly summaries** only when needed for deep dives

---

## Cognitive Task Examples

Common cognitive tasks that map to analogous domains:

| Cognitive Task | User is... | Analogous Domains |
|----------------|-----------|-------------------|
| **Rapid Gestalt Assessment** | Determining system health at a glance | Medical monitors, trading platforms, automotive dashboards |
| **Anomaly Detection** | Identifying what requires attention | Security ops, fraud detection, quality control |
| **Timeline/Progress** | Understanding sequence and what's next | Sports broadcasts, delivery tracking, video editing |
| **Progressive Disclosure** | Drilling from overview to detail | Developer tools, maps, email threads |
| **Decision Support** | Making a choice with confidence | Trading platforms, emergency dispatch, medical treatment |

Full catalog: `context/research-methodology/cognitive-task-catalog.md`

---

## Troubleshooting

### Research Quality Issues

**Problem**: Research feels generic or obvious
- Ensure cognitive tasks were identified (not just features)
- Verify multi-vector approach was used (not just category-matching)
- Check that Level 3-4 patterns were extracted (not just visual)
- Request more divergent sources

### RSS Feed Issues

**Problem**: Feed data is empty or incomplete
- Verify network connectivity
- Check that feed URLs are still valid (sites occasionally change feed paths)
- Review raw/*.json files to confirm data was captured
- Try running the recipe again — transient failures are common with feeds

**Known feed quirks:**
- **Awwwards**: Use the FeedBurner URL (`feeds.feedburner.com/awwwards-sites-of-the-day`), not the old `/websites/rss/` path which now returns HTML
- **Siteinspire**: Use `/websites/feed` not the old `/websites.rss` (returns 429)
- **The FWA**: Use `/rss` not `/rss/awards` (the old endpoint returns 500)

---

## Configuration

### Archive Retention

Default: 30-60 day rolling window for the lightweight index
Learnings persist in `.design/observed-expression/` indefinitely

---

## Additional Resources

### Core Methodology
- **Creative Research Methodology**: `context/research-methodology/creative-research-methodology.md`
- **Cognitive Task Catalog**: `context/research-methodology/cognitive-task-catalog.md`
- **Pattern Abstraction Guide**: `context/research-methodology/pattern-abstraction-guide.md`
- **Cognitive Discovery Enhancement**: `context/research-methodology/cognitive-discovery-enhancement.md`

### Agents & Tools
- **Research Analyst Agent**: `agents/research-analyst.md`
- **Research Runner Agent**: `agents/research-runner.md`
- **Weekly Research Recipe**: `recipes/weekly-design-research.yaml`
- **Archive Index**: `context/archive-index.md`

### Tools (On-Demand Analysis)
- **browser-tester**: Site visits and screenshot capture during targeted analysis
- **nano-banana**: Visual analysis with research-question-specific prompts

---

**The Key Difference**: Design-intelligence now produces breakthrough creative work by researching PURPOSE (cognitive tasks) across domains, not just matching categories. This is the innovation that sets it apart.