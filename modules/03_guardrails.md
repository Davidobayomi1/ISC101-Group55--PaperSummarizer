# Module 03: Guardrails

**Goal:** Ensure quality and factual accuracy.

**Logic:**
1.  **Hallucination Check:** Verify that every claim in the generated summary exists in the source text.
2.  **Length Check:** Identify sections with < 50 words.
3.  **Missing Section Check:** Flag sections that are empty.
4.  **Chunking:** If a section is too long for the context window, split it logically before summarizing.
