# Agent Definitions

## Research Agent

### Purpose

Gather information and create a research briefing pack.

### Inputs

- Topic
- URL
- Uploaded document

### Outputs

- Executive summary
- Timeline
- Key stakeholders
- Source list

### Business Value

Provides reliable context for downstream agents.

---

## Fact Check Agent

### Purpose

Verify claims and identify unsupported statements.

### Inputs

- Research report
- Extracted claims

### Outputs

- Verification report
- Confidence scores
- Unsupported claims

### Business Value

Improves trustworthiness and transparency.

---

## Headline Agent

### Purpose

Generate multiple headline variations.

### Outputs

- SEO headline
- Editorial headline
- Breaking news headline
- Social media headline

### Business Value

Accelerates content publishing.

---

## Editorial Review Agent

### Purpose

Review generated content quality.

### Outputs

- Hallucination warnings
- Bias indicators
- Improvement recommendations

### Business Value

Acts as an AI-powered editorial assistant.

---

## Social Media Agent

### Purpose

Adapt content for social platforms.

### Outputs

- LinkedIn post
- X/Twitter post
- Instagram caption
- TikTok summary

### Business Value

Reduces manual content repurposing effort.

## Context Builder

### Purpose

Collect and normalize information from multiple sources before it is processed by AI agents.

### Supported Sources

- Tavily Search
- User URLs
- Uploaded PDFs

### Outputs

- Normalized Context
- Retrieved Content
- Source Metadata

### Why It Exists

Separates retrieval logic from reasoning logic, improving maintainability and scalability.