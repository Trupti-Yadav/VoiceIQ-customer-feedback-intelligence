# VoiceIQ – AI Workflow Design
## AI-Powered Customer Feedback Intelligence

**Document Type:** AI Workflow Design  
**Project:** VoiceIQ  
**Version:** 1.0

---

## 1. Purpose

This document describes how VoiceIQ uses Make.com and the OpenAI API to transform raw customer feedback into structured analysis and consolidated product insights.

The MVP contains two AI automation workflows:

1. Individual Feedback Analysis.
2. Consolidated Customer Insights.

Both workflows use Google Sheets as the data source and destination, with Make.com orchestrating the processing steps.

## 2. Workflow 1 – Individual Feedback Analysis

### Objective

Analyse individual customer feedback records and generate structured insights using the OpenAI API.

### Workflow Components

| Sequence | Make.com Module | Responsibility |
|---|---|---|
| 1 | Google Sheets – Search Rows | Retrieve feedback records from Raw_Feedback |
| 2 | OpenAI – Generate a Response | Analyse each feedback record |
| 3 | JSON – Parse JSON | Extract structured AI-generated fields |
| 4 | Google Sheets – Add a Row | Store the analysis in AI_Analysis |

### Workflow Process

**Step 1 – Retrieve Customer Feedback**

Make.com retrieves feedback records from the `Raw_Feedback` Google Sheets tab.

The input includes:
- Feedback ID.
- Feedback date.
- Feedback text.
- Feedback source.
- Experience area.
- Product name.
- Product category.
- Customer segment.

**Step 2 – AI Analysis**

The OpenAI API analyses each feedback record using a defined prompt and structured output requirements.

The AI is instructed to identify:
- Customer sentiment.
- Sentiment score.
- Experience category.
- Feedback type.
- Main theme.
- Customer pain point.
- Feature request.
- Severity and severity rationale.
- Customer impact.
- Urgency.
- Business alignment.
- Implementation feasibility.
- Recommended action.
- Confidence score.
- Human review requirement.

**Step 3 – Structured Output**

The AI response is returned in JSON format.

The JSON Parse module extracts the individual fields so they can be mapped into Google Sheets columns.

**Step 4 – Store AI Analysis**

The structured output is added as a new row in the `AI_Analysis` tab.

This creates a structured dataset that can be used by the second workflow.

### Workflow Diagram

```text
Google Sheets
Search Rows
     |
     v
OpenAI API
Generate a Response
     |
     v
JSON
Parse JSON
     |
     v
Google Sheets
Add a Row
     |
     v
AI_Analysis
```

### Expected Outcome

Each feedback record is converted into a structured analysis containing sentiment, themes, customer pain points, feature requests, severity, scoring factors and recommended actions.

---

## 3. Workflow 2 – Consolidated Customer Insights

### Objective

Consolidate individual AI analysis records into common customer themes and generate prioritisation insights.

### Workflow Components

| Sequence | Make.com Module | Responsibility |
|---|---|---|
| 1 | Google Sheets – Search Rows | Retrieve individual analysis records |
| 2 | Tools – Array Aggregator | Combine records for consolidated analysis |
| 3 | OpenAI – Generate a Response | Group similar feedback and generate theme-level insights |
| 4 | JSON – Parse JSON | Extract the consolidated themes array |
| 5 | Tools – Iterator | Process each consolidated theme |
| 6 | Google Sheets – Add a Row | Store each theme in VoiceIQ_Insights |

### Workflow Process

**Step 1 – Retrieve Individual AI Analysis**

Make.com retrieves the analysed records from the `AI_Analysis` tab.

**Step 2 – Aggregate Records**

The Array Aggregator combines the selected fields from individual analysis records into a collection for the next AI processing step.

**Step 3 – Consolidate Customer Themes**

The OpenAI API analyses the aggregated records and groups similar feedback into meaningful customer themes.

The instructions require:
- Each feedback ID to belong to one primary consolidated theme.
- No duplicate feedback IDs across themes.
- Similar customer pain points to be grouped together.
- Feedback frequency to be calculated at the consolidated theme level.
- Sentiment counts and average sentiment to be summarised.
- Customer pain points and feature requests to be consolidated.

**Step 4 – Generate Prioritisation Insights**

The AI generates theme-level scoring and recommendations using the defined weighted prioritisation framework.

| Factor | Weight |
|---|---:|
| Customer Impact | 30% |
| Frequency | 25% |
| Urgency / Severity | 20% |
| Business Alignment | 15% |
| Implementation Feasibility | 10% |

The resulting priority classification is:
- Critical: 80–100.
- High: 60–79.
- Medium: 40–59.
- Low: Below 40.

The scores and recommendations are illustrative outputs for the portfolio demonstration and require human validation.

**Step 5 – Parse and Iterate**

The AI returns a JSON object containing a `themes` array.

The JSON Parse module extracts the array, and the Iterator processes each theme separately.

**Step 6 – Store Consolidated Insights**

Each theme is written as a separate row in the `VoiceIQ_Insights` Google Sheets tab.

### Workflow Diagram

```text
Google Sheets
Search Rows
     |
     v
Tools
Array Aggregator
     |
     v
OpenAI API
Generate a Response
     |
     v
JSON
Parse JSON
     |
     v
Tools
Iterator
     |
     v
Google Sheets
Add a Row
     |
     v
VoiceIQ_Insights
```

### Expected Outcome

Individual customer feedback records are consolidated into meaningful themes, with associated frequency, sentiment, pain point summaries, prioritisation scores and recommended actions.

---

## 4. Data Flow Between Workflows

The two workflows are connected through Google Sheets.

| Data Layer | Google Sheets Tab | Description |
|---|---|---|
| Input | Raw_Feedback | Original customer feedback records |
| Intermediate Output | AI_Analysis | Structured AI analysis for individual records |
| Final Output | VoiceIQ_Insights | Consolidated customer themes and prioritisation insights |

The `Feedback_ID` field provides traceability between the original feedback and the individual AI analysis. Consolidated themes also retain their associated feedback IDs.

## 5. AI Prompt and Output Design

The AI processing instructions are designed around the product requirements rather than simply requesting a general summary.

The prompts define:

- The role of the AI in the feedback analysis process.
- The information to extract from each feedback record.
- The classification and scoring requirements.
- The expected JSON output structure.
- The rules for grouping similar feedback.
- The need to preserve feedback ID traceability.
- The need to flag outputs that require human review.

Structured output enables the results to be parsed and stored consistently for downstream processing.

## 6. Human-in-the-Loop Considerations

VoiceIQ is designed as an AI-assisted decision-support solution.

Human oversight is important because:
- Customer feedback can be ambiguous or context-dependent.
- AI sentiment and theme classifications may be inaccurate.
- Severity and prioritisation scores may require business context.
- Recommended actions should be reviewed before product decisions are made.

The workflow includes confidence scores and human review indicators to support this approach.

## 7. Execution Results

The demonstration workflows were successfully executed.

| Metric | Demonstration Result |
|---|---:|
| Original synthetic feedback records | 50 |
| Individual records processed through AI | 30 |
| Experience areas represented in analysed records | 4 |
| Consolidated customer themes generated | 15 |
| Individual feedback analysis workflow | Successful |
| Consolidated insights workflow | Successful |

The 30 analysed records were intentionally selected to keep the demonstration manageable in terms of processing time and API cost.

## 8. Operational Considerations and Limitations

The current workflows demonstrate the core processing logic, but additional controls would be required before production deployment.

Potential improvements include:

- Duplicate prevention and processing status tracking.
- Error handling and retry mechanisms.
- API usage and cost monitoring.
- AI output quality evaluation.
- Validation of prioritisation calculations.
- Secure credential management.
- Processing of new feedback records without reprocessing existing records.

The current workflows should not be treated as production-grade integrations.

## 9. Product Management Takeaways

The design of these workflows demonstrates important AI Product Management considerations:

1. Translating a customer problem into AI-enabled product capabilities.
2. Defining inputs, expected outputs and processing requirements.
3. Designing AI prompts around specific product use cases.
4. Structuring AI outputs for downstream workflows.
5. Maintaining traceability between original feedback and consolidated insights.
6. Incorporating human review into AI-assisted decision-making.
7. Considering cost, execution time, data quality and operational limitations.

**Key takeaway:** Effective AI product design requires more than connecting an AI model to an automation tool. It requires clear product requirements, well-defined AI outputs, workflow orchestration, validation and appropriate human oversight.

---

**VoiceIQ – AI-Powered Customer Feedback Intelligence**  
*AI workflow design for an AI-assisted Voice of Customer product.*