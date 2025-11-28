# Module 03: Guardrails
# Change Log: Added 'evidence_mode' for strict checking and standardized warning messages for short/missing sections.

**Goal:** Ensure quality, factual accuracy, and safe failure states.

**Variables:**
* `evidence_mode` (Values: "standard", "strict")

**Logic:**
1.  **Strict Evidence Mode:**
    * If `evidence_mode = "strict"`, only include claims, equations, and results explicitly present in the source text.
    * If insufficient information is available, output: "The source text does not provide enough detail to summarize this section in strict evidence mode."

2.  **Section Health Checks:**
    * **Missing / Empty:** If section is empty, output warning: "Section skipped: no usable text was provided."
    * **Too Short (< 50 words):** If section length < 50 words, output warning: "Section very short: summary may be incomplete."

3.  **Hallucination Check:** Verify that every claim in the generated summary exists in the source text.
