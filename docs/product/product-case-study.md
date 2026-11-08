# VoiceIQ – Product Case Study
## AI-Powered Customer Feedback Intelligence

**Project Type:** AI Product Management Portfolio Project  
**Industry:** E-commerce  
**Product Category:** Voice of Customer (VoC) Analytics

---

## 1. Executive Summary

VoiceIQ is an AI-assisted customer feedback intelligence solution designed to help e-commerce product teams transform unstructured customer feedback into structured and prioritised product insights.

The project explores how Generative AI and workflow automation can support sentiment analysis, customer pain point identification, feedback theme consolidation and product prioritisation.

The solution integrates Google Sheets, Make.com, the OpenAI API and Power BI Desktop.

The primary objective is to demonstrate how an AI-enabled product can address a real-world customer experience problem and support more informed product decisions.

## 2. Business Problem

E-commerce businesses receive customer feedback across multiple channels, including product reviews, complaints, delivery experiences and customer service interactions.

Product teams may find it challenging to:

- Analyse large volumes of unstructured feedback manually.
- Identify recurring customer pain points.
- Understand the sentiment behind customer experiences.
- Recognise emerging product improvement opportunities.
- Prioritise issues based on customer impact and business value.
- Convert customer feedback into actionable product insights.

**Product opportunity:** Introduce an AI-assisted workflow that automatically analyses feedback, consolidates recurring themes and supports product prioritisation.

## 3. Product Vision and Objectives

**Vision**

Enable product teams to make more customer-centric decisions by converting unstructured customer feedback into actionable product intelligence.

**Objectives**

1. Automate individual customer feedback analysis.
2. Identify sentiment, pain points and feature requests.
3. Consolidate similar feedback into meaningful customer themes.
4. Introduce a structured product prioritisation framework.
5. Present customer insights through an interactive dashboard.
6. Incorporate human review into AI-assisted decision-making.

## 4. Target Users

**Primary persona: Product Manager**

Needs to understand customer problems, identify product opportunities and prioritise improvements.

**Secondary persona: Product Analyst**

Needs structured feedback data, sentiment trends and recurring customer themes to support product analysis.

**Stakeholder persona: Business and Product Leadership**

Needs a consolidated view of customer experience issues, priority areas and potential improvement opportunities.

## 5. Product Scope – MVP

The VoiceIQ MVP focuses on five capabilities.

| Capability | Description |
|---|---|
| Feedback ingestion | Read customer feedback from Google Sheets |
| AI analysis | Classify sentiment, themes, pain points and feature requests |
| Theme consolidation | Group similar feedback into recurring themes |
| Product prioritisation | Generate illustrative weighted priority scores |
| Insight visualisation | Present findings through Power BI dashboards |

## 6. AI Product Design

The solution uses two AI automation workflows.

### Workflow 1: Individual Feedback Analysis

Each feedback record is sent to the OpenAI API through Make.com.

The AI analysis produces:

- Sentiment classification and score.
- Experience category.
- Feedback type.
- Main customer theme.
- Customer pain point.
- Feature request.
- Severity and severity rationale.
- Customer impact, urgency, business alignment and implementation feasibility scores.
- Recommended action.
- Confidence score.
- Human review indicator.

### Workflow 2: Consolidated Customer Insights

The individual analysis outputs are consolidated to identify common themes.

The workflow generates:

- Consolidated customer themes.
- Feedback frequency.
- Positive, negative and neutral counts.
- Average sentiment score.
- Customer pain point summaries.
- Feature request summaries.
- Prioritisation scores.
- Priority classification.
- Recommended actions.

Both workflows store their results in Google Sheets.

## 7. Product Prioritisation Framework

A weighted scoring framework was defined to help evaluate customer issues and improvement opportunities.

| Factor | Weight |
|---|---:|
| Customer Impact | 30% |
| Frequency | 25% |
| Urgency / Severity | 20% |
| Business Alignment | 15% |
| Implementation Feasibility | 10% |
| **Total** | **100%** |

Each factor is evaluated on a scale of 1–5.

The weighted score is converted into a percentage for easier comparison.

Priority classification:

| Score | Priority |
|---|---|
| 80–100 | Critical |
| 60–79 | High |
| 40–59 | Medium |
| Below 40 | Low |

The framework is intended to support product discussions. AI-generated scores and recommendations require human validation before being used for actual product decisions.

## 8. Technology and Solution Architecture

The solution uses the following technology stack:

- Google Sheets – Feedback input and AI output storage.
- Make.com – Workflow automation and orchestration.
- OpenAI API – Feedback analysis and insight generation.
- Power BI Desktop – Interactive dashboards.
- GitHub – Project documentation and portfolio presentation.

**End-to-end workflow**

```text
Customer Feedback
       |
       v
Google Sheets
       |
       v
Make.com
       |
       v
OpenAI API
       |
       v
AI Analysis
       |
       v
Google Sheets
       |
       v
Consolidated Insights
       |
       v
Power BI Dashboard
```

## 9. Dashboard and Product Insights

The final Power BI dashboard contains three pages.

**Page 1 – Customer Feedback Overview**

Provides an overview of feedback volume, sentiment distribution and experience areas.

**Page 2 – Sentiment Analysis**

Explores sentiment across experience areas, feedback types, negative feedback and customer pain points.

**Page 3 – Customer Pain Points & Prioritisation**

Highlights consolidated customer themes, priority distribution and weighted priority scores.

## 10. Demonstration Results

The project uses 50 synthetic customer feedback records representing an Amazon-like multi-category e-commerce marketplace.

For the AI automation demonstration:

- 30 feedback records were processed.
- Four experience areas were represented in the analysed sample.
- 15 consolidated customer themes were generated.
- Two AI automation workflows were executed successfully.
- AI analysis and consolidated insights were stored in Google Sheets.
- A three-page Power BI dashboard was created.

These results demonstrate the end-to-end workflow rather than production-scale performance or validated business impact.

## 11. Responsible AI Considerations

The project incorporates several considerations for responsible AI product design:

- Confidence scoring for AI-generated classifications.
- Human review indicators for potentially uncertain outputs.
- Human validation before acting on AI-generated recommendations.
- Synthetic demonstration data instead of real customer information.
- Recognition that AI-generated prioritisation scores are illustrative and require validation.

## 12. My Role and Product Management Learnings

I am currently working as a Senior Scrum Master, with five years of Agile experience and over 20 years in the IT industry. This project represents my practical exploration of AI Product Management.

Through VoiceIQ, I applied product-oriented thinking to:

- Identify a customer problem and define a product vision.
- Translate the problem into product requirements and use cases.
- Define AI capabilities and expected outputs.
- Design AI-enabled workflow automation.
- Establish a weighted prioritisation framework.
- Consider human oversight and responsible AI.
- Define product insight KPIs and dashboard requirements.
- Communicate the solution through product documentation and visual reporting.

**Key learning:** AI Product Management requires more than selecting an AI model. It involves understanding customer problems, defining the right AI capabilities, designing workflows, evaluating outputs, considering risks and connecting insights to product decisions.

## 13. Limitations and Future Opportunities

VoiceIQ is an MVP portfolio demonstration and is not a production-ready customer feedback platform.

Potential future enhancements include:

- Processing the remaining 20 synthetic feedback records.
- Testing the solution with larger and more diverse datasets.
- Improving AI classification evaluation and accuracy measurement.
- Validating prioritisation scores with product stakeholders.
- Integrating additional feedback channels.
- Introducing feedback trend monitoring over time.

---

**VoiceIQ – AI-Powered Customer Feedback Intelligence**  
*An AI Product Management portfolio project demonstrating customer-centric product thinking and AI-enabled product workflows.*