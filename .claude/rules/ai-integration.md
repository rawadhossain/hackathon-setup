# AI and external integration rule

Add AI, model, multimodal, retrieval, speech, vision, tool-calling, workflow, or external API capabilities only when a requirement demands them. Research official APIs/SDKs, libraries, pretrained models, availability, limits, credentials, and fallback before selection.

Use direct SDK/API calls unless a lightweight orchestration abstraction is demonstrably insufficient; do not introduce LangChain, LangGraph, or equivalent by habit. Record selection and rationale in research and an ADR. Contract inputs, structured outputs, validation, timeouts, retries, rate-limit behavior, cost/availability, and user-safe failure paths.
