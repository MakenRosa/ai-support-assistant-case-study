# Sequence

1. User message enters support queue.
2. Orchestrator starts workflow.
3. Classifier detects category and urgency.
4. Retrieval pulls nearest knowledge chunks.
5. LLM returns candidate response.
6. Policy checks evaluate confidence/risk.
7. If approved, response is sent automatically.
8. If not approved, ticket is escalated to human support.
9. Metrics and traces are persisted.
