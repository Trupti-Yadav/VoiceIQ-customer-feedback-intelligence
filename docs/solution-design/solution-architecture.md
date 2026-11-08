# VoiceIQ – Solution Architecture
## AI-Powered Customer Feedback Intelligence

**Document Type:** Solution Architecture  
**Project:** VoiceIQ  
**Version:** 1.0

---

## 1. Architecture Overview

VoiceIQ follows an AI-assisted architecture that transforms unstructured customer feedback into structured customer insights and product prioritisation outputs.

The solution combines spreadsheet-based data management, workflow automation, Generative AI and business intelligence visualisation.

### Technology Components

| Component | Technology | Responsibility |
|---|---|---|
| Input Data Layer | Google Sheets | Stores raw customer feedback |
| Workflow Automation Layer | Make.com | Orchestrates AI processing workflows |
| AI Intelligence Layer | OpenAI API | Analyses feedback and consolidates insights |
| Output Data Layer | Google Sheets | Stores structured analysis and consolidated insights |
| Visualisation Layer | Power BI Desktop | Presents customer insights and prioritisation |
| Documentation Layer | GitHub | Maintains product and solution documentation |

## 2. High-Level Architecture

```text
             CUSTOMER FEEDBACK
                     |
                     v
             +---------------+
             | Google Sheets |
             | Raw_Feedback  |
             +---------------+
                     |
                     v
             +---------------+
             |    Make.com   |
             | Workflow 1    |
             +---------------+
                     |
                     v
             +---------------+
             |   OpenAI API  |
             | Individual    |
             | Feedback      |
             | Analysis      |
             +---------------+
                     |
                     v
             +---------------+
             | Google Sheets |
             | AI_Analysis   |
             +---------------+
                     |
                     v
             +---------------+
             |    Make.com   |
             | Workflow 2    |
             +---------------+
                     |
                     v
             +---------------+
             |   OpenAI API  |
             | Theme         |
             | Consolidation |
             +---------------+
                     |
                     v
             +---------------+
             | Google Sheets |
             | VoiceIQ_      |
             | Insights      |
             +---------------+
                     |
                     v
             +---------------+
             | Power BI      |
             | Interactive   |
             | Dashboard     |
             +---------------+
```

## 3. Workflow 1 – Individual Feedback Analysis

**Objective:** Convert individual unstructured customer feedback records into structured AI-generated analysis.

### Process Flow

1. Google Sheets provides customer feedback records from the `Raw_Feedback` tab.
2. Make.com retrieves the records for processing.
3. Each feedback record is sent to the OpenAI API.
4. OpenAI analyses the feedback using the defined instructions and output structure.
5. The response is parsed into structured fields.
6. Make.com writes the analysis into the `AI_Analysis` tab.

### AI Analysis Outputs

- Sentiment and sentiment score.
- Experience category.
- Feedback type.
- Main theme.
- Customer pain point.
- Feature request.
- Severity and severity rationale.
- Customer impact score.
- Urgency score.
- Business alignment score.
- Implementation feasibility score.
- Recommended action.
- Confidence score.
- Human review indicator.

### Workflow Architecture

```text
Google Sheets – Search Rows
          |
          v
OpenAI – Generate a Response
          |
          v
JSON – Parse JSON
          |
          v
Google Sheets – Add a Row
          |
          v
AI_Analysis
```

## 4. Workflow 2 – Consolidated Customer Insights

**Objective:** Identify recurring customer problems and consolidate individual feedback analysis into meaningful themes.

### Process Flow

1. Make.com retrieves AI analysis records from `AI_Analysis`.
2. An Array Aggregator combines the records for consolidated analysis.
3. The OpenAI API groups similar feedback into common themes.
4. JSON parsing extracts the structured theme-level outputs.
5. An Iterator processes each consolidated theme.
6. Make.com writes each theme and its associated insights into `VoiceIQ_Insights`.

### Consolidated Outputs

- Main customer theme.
- Experience area.
- Feedback count.
- Associated feedback IDs.
- Positive, negative and neutral counts.
- Average sentiment score.
- Customer pain point summary.
- Feature request summary.
- Average scoring factors.
- Frequency score.
- Weighted priority score.
- Priority classification.
- Recommended action.
- Human review indicator.

### Workflow Architecture

```text
Google Sheets – Search Rows
          |
          v
Tools – Array Aggregator
          |
          v
OpenAI – Generate a Response
          |
          v
JSON – Parse JSON
          |
          v
Tools – Iterator
          |
          v
Google Sheets – Add a Row
          |
          v
VoiceIQ_Insights
```

## 5. Data Architecture

VoiceIQ uses three Google Sheets tabs to manage the information flow.

| Sheet Tab | Purpose |
|---|---|
| Raw_Feedback | Original synthetic customer feedback |
| AI_Analysis | Individual feedback analysis outputs |
| VoiceIQ_Insights | Consolidated themes and prioritisation outputs |

The data is structured so that individual feedback analysis can be traced back to the consolidated customer themes through feedback IDs.

## 6. Power BI Integration

Power BI Desktop consumes exported CSV versions of the AI analysis and consolidated insights datasets.

The dashboard contains three pages:

1. Customer Feedback Overview.
2. Sentiment Analysis.
3. Customer Pain Points & Prioritisation.

The visualisation layer enables product stakeholders to explore customer sentiment, recurring pain points and relative product priorities.

## 7. AI and Human Oversight

VoiceIQ is designed as an AI-assisted decision-support solution.

Important considerations include:

- AI outputs are structured for consistency and downstream analysis.
- Confidence scores provide an indication of model certainty.
- Human review indicators highlight outputs that may require additional validation.
- Product teams retain responsibility for validating recommendations and making prioritisation decisions.

The current demonstration uses illustrative AI-generated scores, which should not be interpreted as validated production decisions.

## 8. Architecture Scope and Limitations

The current architecture is an MVP portfolio demonstration.

- Synthetic customer feedback is used.
- Only 30 of the original 50 records were processed through the AI analysis workflow.
- Four experience areas are represented in the analysed sample.
- Power BI uses exported CSV datasets rather than a live connection to Google Sheets.
- The automation workflows are demonstrated using Make.com and the OpenAI API.
- Production-scale monitoring, access controls, security hardening and operational governance are outside the current MVP scope.

## 9. Potential Future Enhancements

Future architecture improvements could include:

- Automated ingestion from multiple customer feedback channels.
- Scheduled or incremental feedback processing.
- Duplicate detection and processing status management.
- AI evaluation and classification quality monitoring.
- Secure role-based access and data governance.
- Live or scheduled dashboard refresh.
- Feedback trend analysis across multiple periods.

---

**VoiceIQ – AI-Powered Customer Feedback Intelligence**  
*Solution architecture for an AI-assisted Voice of Customer product.*