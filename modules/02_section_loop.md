# Module 02: Section Loop
# Change Log: Added 'summary_level' variable and conditional logic for short vs. detailed modes.

**Goal:** Summarize each section individually with adjustable detail levels.

**Variables:**
* `summary_level` (Values: "short", "detailed")

**Logic:**
For each section provided by the user:
1.  Read the full text.
2.  Check `summary_level`:
    * **If `summary_level = "short"`:**
        * Generate a compact summary (1–2 sentences).
    * **If `summary_level = "detailed"`:**
        * Generate a short paragraph.
        * **PLUS** a bulleted list of 3–5 key points extracted from the section.
3.  **Constraint Check:** Ensure the total output per section is **under 150 words**.
4.  Store the result for compilation.
