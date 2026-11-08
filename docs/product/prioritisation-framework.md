# VoiceIQ – Product Prioritisation Framework

## 1. Purpose

The VoiceIQ prioritisation framework helps product teams evaluate customer pain points and improvement opportunities identified through AI-powered feedback analysis.

The objective is to provide a structured approach for comparing opportunities based on customer value, frequency, urgency, business alignment and implementation feasibility.

AI-generated scores are intended to support product discussions, not replace human judgement.

## 2. Prioritisation Factors and Weights

VoiceIQ uses five evaluation factors.

| Factor | Weight | Description |
|---|---:|---|
| Customer Impact | 30% | How significantly does the issue affect the customer experience? |
| Frequency | 25% | How often is the issue reported across customer feedback? |
| Urgency / Severity | 20% | How urgently does the issue need attention? |
| Business Alignment | 15% | How closely does addressing the issue support business and product objectives? |
| Implementation Feasibility | 10% | How feasible is the proposed improvement to implement? |
| **Total** | **100%** | |

## 3. Scoring Scale

Each factor is evaluated on a scale of 1 to 5.

| Score | Interpretation |
|---|---|
| 1 | Very Low |
| 2 | Low |
| 3 | Moderate |
| 4 | High |
| 5 | Very High |

The scoring criteria provide a common reference for evaluating customer issues.

## 4. Weighted Scoring Calculation

The weighted prioritisation score is calculated using:

**Weighted Score =**

(Customer Impact × 30%) +  
(Frequency × 25%) +  
(Urgency × 20%) +  
(Business Alignment × 15%) +  
(Implementation Feasibility × 10%)

The weighted result is converted into a percentage by multiplying it by 20.

This produces a score between 20 and 100 when factor scores range from 1 to 5.

## 5. Frequency Scoring

Frequency is evaluated at the consolidated customer theme level rather than at the individual feedback level.

| Number of Feedback Records | Frequency Score |
|---|---:|
| 1 | 1 |
| 2–3 | 2 |
| 4–6 | 3 |
| 7–9 | 4 |
| 10 or more | 5 |

This approach helps distinguish isolated feedback from recurring customer problems.

## 6. Priority Classification

The weighted percentage score is mapped to four priority levels.

| Weighted Score | Priority | Interpretation |
|---|---|---|
| 80–100 | Critical | Requires urgent product attention |
| 60–79 | High | Significant customer or business impact |
| 40–59 | Medium | Worth considering in product planning |
| Below 40 | Low | Lower relative priority |

Priority classifications are intended to support roadmap discussions and should be reviewed against actual product strategy and business context.

## 7. Example of Prioritisation

Consider a hypothetical recurring customer issue: inaccurate search results.

A product team might evaluate it as follows:

| Factor | Score | Weight | Weighted Contribution |
|---|---:|---:|---:|
| Customer Impact | 5 | 30% | 1.50 |
| Frequency | 4 | 25% | 1.00 |
| Urgency / Severity | 4 | 20% | 0.80 |
| Business Alignment | 5 | 15% | 0.75 |
| Implementation Feasibility | 3 | 10% | 0.30 |
| **Total** | | | **4.35** |

Weighted percentage:

4.35 × 20 = **87**

Priority classification: **Critical**

This example is illustrative and is not presented as a validated result from the VoiceIQ dataset.

## 8. Human Review and AI Governance

AI-generated scoring should not be treated as an automatically approved product decision.

The proposed approach includes:

- AI-generated initial scoring.
- Confidence indicators for AI-generated outputs.
- Human review flags where additional validation may be required.
- Product stakeholder validation of customer impact and business alignment.
- Human ownership of final prioritisation and roadmap decisions.

This helps reduce the risk of prioritising issues solely based on AI-generated interpretations.

## 9. Limitations and Considerations

The framework is a demonstration model and has not been validated against real business outcomes.

Important considerations include:

- Factor scores may involve subjective judgement.
- Frequency depends on the available feedback sample.
- Implementation feasibility requires technical and operational input.
- AI-generated scores may need correction.
- Priority classifications should be considered alongside product strategy, dependencies and available resources.

The scores generated in the VoiceIQ demonstration are illustrative AI outputs and are not independently validated production decisions.

## 10. Product Management Perspective

The prioritisation framework demonstrates how customer feedback can be translated into structured product opportunities.

From an AI Product Management perspective, it highlights the importance of:

1. Defining transparent evaluation criteria.
2. Balancing customer value and business objectives.
3. Considering frequency and urgency rather than sentiment alone.
4. Using AI to assist analysis without surrendering product judgement.
5. Maintaining human ownership of prioritisation decisions.

**Key takeaway:** AI can help product teams identify and evaluate opportunities, but product prioritisation remains a human-led decision informed by customer evidence, business strategy and implementation constraints.

---

**VoiceIQ – AI-Powered Customer Feedback Intelligence**  
*Weighted prioritisation framework for customer-centric product decision-making.*