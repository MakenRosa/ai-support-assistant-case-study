# AI Support Assistant - Case Study

## Overview
This repository documents the architecture and delivery decisions behind an AI-powered Level 1 support assistant.

## Context
The assistant was designed to reduce repetitive support load by automatically resolving common tickets before human escalation.

## Business outcomes
- Up to **50%** of incoming support tickets resolved before human handoff
- Monthly inference cost maintained under **US$15**
- Better response consistency and faster first response time

## Architecture (high level)
1. Ingestion of support messages/events
2. Classification and routing
3. Retrieval step (RAG) for contextual grounding
4. LLM response generation
5. Confidence/rules gate before automated reply
6. Telemetry for cost, latency, and resolution metrics

See `docs/architecture.md` and `docs/sequence.md`.

## Tech used
- AWS Bedrock
- Pinecone (RAG)
- AWS Lambda
- AWS Step Functions
- AWS SAM
- Jenkins

## Non-goals
- No proprietary code
- No customer data
- No internal model prompts or private infra details

## Security
See `SECURITY.md`.

## ADRs
- `adr/0001-automation-threshold.md`
- `adr/0002-rag-over-fine-tuning.md`
