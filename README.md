# Amazon Product Intelligence Skill

## Overview

This Skill analyzes Amazon products using ASIN, product URLs, images, or keywords to generate structured product evaluation and market intelligence reports.

It is designed to support data-driven product research and decision-making for e-commerce analysis.

---

## Core Capabilities

### 1. Market Analysis
- Market size estimation
- Sales volume trends
- Keyword coverage analysis
- Market growth or decline detection

---

### 2. Competition Analysis
- Competitor structure analysis
- Market concentration level
- Brand vs non-brand distribution
- Entry difficulty evaluation

---

### 3. Product Performance Analysis
- ASIN-level performance metrics
- Parent-child listing structure analysis
- Variation count and structure
- Sales distribution across variations

---

### 4. Pricing Analysis
- Price range distribution
- Market price bands
- Price competition level
- Profit margin estimation

---

### 5. Seller Analysis
- Seller country distribution
- FBA vs FBM ratio
- Marketplace structure evaluation

---

### 6. Review & Customer Insight (VOC)
- Review rating distribution
- Review volume analysis
- Common complaint extraction
- Customer satisfaction patterns

---

### 7. Profitability Estimation
- Estimated selling price
- Cost structure breakdown
- FBA and fulfillment fees estimation
- Advertising cost estimation
- Net margin estimation

---

### 8. Product Structure Analysis
- Variation count
- Parent ASIN dependency
- Sales contribution per ASIN
- Market control structure

---

### 9. Strategy Recommendation
- Recommended entry strategy (single / variation / bundle)
- Product positioning suggestion
- Market entry difficulty
- Competitive response level

---

## Input

- ASIN
- Amazon product URL
- Product image
- 1–2 keywords

---

## Output

The Skill returns a structured report including:

- Market opportunity evaluation
- Competitive landscape analysis
- Pricing structure insights
- Seller distribution analysis
- Review-based customer insights
- Product structure breakdown
- Profit estimation
- Entry strategy recommendation
- Final opportunity score (0–100)

---

## Output Format

All outputs must be structured and categorized, suitable for downstream analysis or decision systems.

---

## System Behavior

- Focus on structured data extraction and analysis
- Avoid subjective marketing language
- Prioritize factual inference from available product signals
- Normalize all outputs into comparable metrics
