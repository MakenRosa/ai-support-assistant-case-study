# Architecture

## Components
- Event source (support channel integrations)
- Ingestion service
- Classifier and intent detection
- Retrieval layer (vector search)
- LLM orchestration layer
- Guardrails + confidence checks
- Human handoff queue
- Observability (cost, latency, quality)

## Data flow
1. Ticket arrives.
2. Pipeline classifies issue and loads context.
3. RAG fetches relevant docs/snippets.
4. LLM generates draft answer.
5. Guardrails approve or route to human support.
6. Outcome and metrics are logged.
