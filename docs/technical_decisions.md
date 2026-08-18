# Technical Decisions

## Current Stack

- Python
- LangGraph
- Gemini API
- Streamlit
- FastAPI
- Pydantic
- Docker

## Decision Status

This document will evolve throughout development and will record all architectural and technology decisions.

## Decision: Structured Agent Communication

### Problem

Multiple agents need to exchange information reliably.

### Alternatives Considered

1. Free-form text
2. Structured Pydantic models

### Decision

Structured Pydantic models.

### Rationale

Structured outputs provide:

- Consistent schemas
- Type safety
- Validation
- Easier debugging
- Better agent interoperability

Free-form text will only be used for user-facing presentation within the Streamlit interface.

## Decision: Metadata-Enriched State

### Problem

Agent outputs need to support debugging, evaluation, and future scalability.

### Alternatives Considered

1. Store only output data
2. Store output data and metadata

### Decision

Store output data together with metadata.

### Rationale

Metadata provides:

- Source tracking
- Confidence scoring
- Processing metrics
- Error diagnostics
- Future observability support

This design improves maintainability and enables evaluation-driven AI workflows.

## Decision: Dedicated Fact-Checking Models

### Problem

Claims require verification metadata that must be preserved throughout the workflow.

### Alternatives Considered

1. List[str]
2. Structured VerifiedClaim model

### Decision

Structured VerifiedClaim model.

### Rationale

Provides:

- Verification status
- Confidence scores
- Source traceability
- Better evaluation support
- Easier UI rendering
- Future extensibility

This design aligns with the project's goal of producing trustworthy and explainable AI outputs.