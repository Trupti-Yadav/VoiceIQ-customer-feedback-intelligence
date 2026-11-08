# VoiceIQ – AI-Powered Customer Feedback Intelligence

**An AI Product Management Portfolio Project**

VoiceIQ is an AI-powered Voice of Customer (VoC) solution designed to help e-commerce product teams transform unstructured customer feedback into actionable product insights.

This project demonstrates how AI can support product teams in understanding customer sentiment, identifying recurring pain points, consolidating feedback themes and prioritising product improvement opportunities.

It is designed as a practical demonstration of AI Product Management concepts, combining product thinking, AI capabilities, workflow automation and data-driven decision-making.

## 1. About This Project

Customer feedback is an important input for product decisions. However, manually analysing feedback from multiple channels can make it difficult for product teams to identify recurring problems, understand customer sentiment and prioritise improvements.

VoiceIQ explores how an AI-assisted solution can help address this challenge by converting unstructured customer feedback into structured insights that support product decision-making.

## 2. Product Vision

To help product teams make more customer-centric decisions by transforming unstructured customer feedback into structured, prioritised and actionable insights.

## 3. Key Product Capabilities

### AI-Powered Feedback Analysis
- Sentiment classification: Positive, Negative and Neutral.
- Sentiment scoring.
- Customer pain point identification.
- Feedback theme classification.
- Feature request extraction.
- Severity assessment.
- Recommended actions.
- Confidence scoring and human review indicators.

### Consolidated Customer Insights
- Grouping similar feedback into common themes.
- Identifying recurring customer issues.
- Analysing feedback frequency and sentiment.
- Summarising customer pain points and feature requests.
- Generating illustrative prioritisation scores.

### Product Prioritisation

VoiceIQ uses a weighted prioritisation framework to evaluate customer issues and improvement opportunities.

| Prioritisation Factor | Weight |
|---|---:|
| Customer Impact | 30% |
| Frequency | 25% |
| Urgency / Severity | 20% |
| Business Alignment | 15% |
| Implementation Feasibility | 10% |
| **Total** | **100%** |

The framework provides a consistent way to compare opportunities. AI-generated recommendations support product judgement rather than replace human decision-making.

## 4. Solution Architecture

The solution follows an integrated workflow:

```text
Google Sheets
(Customer Feedback Input)
        |
        v
Make.com
(Workflow Automation)
        |
        v
OpenAI API
(AI Feedback Analysis)
        |
        v
Google Sheets
(AI Analysis & Consolidated Insights)
        |
        v
Power BI Desktop
(Interactive Product Insights Dashboard)
```

### Technology Stack

| Technology | Purpose |
|---|---|
| Google Sheets | Customer feedback input and AI output storage |
| Make.com | Workflow automation and orchestration |
| OpenAI API | AI-powered feedback analysis and insight generation |
| Power BI Desktop | Interactive data visualisation and reporting |
| GitHub | Product documentation and portfolio showcase |

## 5. AI Automation Workflows

### Workflow 1: Individual Feedback Analysis

Processes individual customer feedback records using the OpenAI API.

Key outputs include:
- Sentiment and sentiment score.
- Experience category and feedback type.
- Main customer pain point.
- Feature request.
- Severity and scoring factors.
- Recommended action.
- Confidence score and human review indicator.

### Workflow 2: Consolidated Customer Insights

Processes individual AI analysis outputs to identify common themes and recurring customer issues.

Key outputs include:
- Consolidated customer themes.
- Feedback frequency and sentiment distribution.
- Customer pain point summaries.
- Feature request summaries.
- Weighted prioritisation scores.
- Priority classification.
- Recommended actions.

Both workflows write their outputs back to Google Sheets for further analysis and reporting.

## 6. Interactive Power BI Dashboard

The VoiceIQ dashboard contains three pages:

1. **Customer Feedback Overview** – Feedback volume, sentiment distribution and experience area breakdown.
2. **Sentiment Analysis** – Sentiment by experience area, feedback type, negative feedback and customer pain points.
3. **Customer Pain Points & Prioritisation** – Consolidated themes, priority distribution and weighted priority scores.

## 7. Demonstration Dataset

The project uses synthetic customer feedback representing an Amazon-like multi-category e-commerce marketplace.

- Original dataset: 50 synthetic customer feedback records.
- AI-analysed dataset: 30 records.
- Experience areas represented in the AI-analysed sample: 4.
- Consolidated customer themes: 15.

The four experience areas represented in the analysed sample are:
- Product Search and Discovery.
- Product Information and Reviews.
- Checkout and Payments.
- Delivery and Tracking.

The 30-record AI analysis sample was intentionally selected to keep the demonstration manageable.

## 8. Product Management Perspective & My Role

As a Senior Scrum Master with 5 years of Agile experience and over 20 years in the IT industry, I am expanding my experience towards AI Product Management.

VoiceIQ is a practical portfolio project through which I am applying my existing Agile delivery and stakeholder management experience to product-focused problem-solving and AI-enabled solutions.

My contributions to this project include:

- **Product Discovery:** Identified the customer feedback analysis problem and defined the product vision.
- **Product Requirements:** Developed the Product Requirements Document (PRD), personas, use cases and functional requirements.
- **AI Product Design:** Defined the AI capabilities, feedback classification requirements and expected outputs.
- **Workflow Design:** Designed two AI automation workflows connecting Google Sheets, Make.com and the OpenAI API.
- **Product Prioritisation:** Established a weighted framework to evaluate customer pain points and improvement opportunities.
- **Responsible AI:** Incorporated confidence scoring and human review considerations into the proposed workflow.
- **Product Analytics:** Defined customer insight KPIs and designed a three-page Power BI dashboard.
- **Stakeholder Communication:** Translated AI-generated outputs into visual insights that can support product discussions and decisions.

The focus is on demonstrating product thinking, AI solution design and the ability to connect customer problems with practical AI-enabled solutions.

## 9. Responsible AI and Limitations

VoiceIQ is a portfolio demonstration using synthetic data and illustrative AI-generated outputs.

Important considerations:
- AI classifications and recommendations may require human validation.
- Demonstration prioritisation scores are illustrative and have not been independently validated for production decision-making.
- The current analysed sample covers 30 of the original 50 records and four experience areas.
- The solution is not a production-ready customer feedback platform.

Human review is an important part of the proposed product approach, particularly before acting on AI-generated recommendations.

## 10. Project Deliverables

This repository will include:

- Product Requirements Document (PRD).
- Product case study.
- Solution architecture.
- AI workflow design.
- Prioritisation framework.
- Synthetic demonstration datasets.
- Power BI dashboard.
- Dashboard screenshots.

---

**Project:** VoiceIQ – AI-Powered Customer Feedback Intelligence  
**Portfolio Focus:** AI Product Management | Product Discovery | Voice of Customer | AI Workflow Design | Product Prioritisation | Customer Insights

**Professional Background:** Senior Scrum Master | Agile Delivery | Transitioning towards AI Product Management