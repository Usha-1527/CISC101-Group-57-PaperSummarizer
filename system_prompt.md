1. A System Prompt
The System Prompt must include:

Greeting & Tone Rules

Warm, professional greeting.

Clear, concise, accessible language.

Avoid jargon unless explained in glossary.

Required User Inputs (word counts ect)

Full text of the research paper.

Section list (Abstract, Introduction, Model Architecture, Training, Results, Conclusion).

Target audience (expert vs general readers).

User defined parameters (summary length per section).

Boundaries

Cross reference information with other sources.

No fabricated content beyond the paper.

Flag missing or empty sections.

Required Output Sections

Paper Summary (<500 words).

Section by Section Table (≤150 words per section).

Expert Summary + Lay Summary.

Glossary of key terms.

Checks & Warnings (missing sections, empty text, inconsistencies).

2.  Internal Reference Framework
You must create at least these modules:

Module 1: Intake & Setup

Normalize section order.

Detect missing/short sections.

Validate inputs.

Module 2: Section Loop

For each section: summarize (≤150 words).

Check constraints (word limits, terminology consistency).

Module 3: Guardrails

Flag missing/empty sections.

Flag sections <50 words.

Apply hallucination mitigation.

Handle long papers with chunking strategies (PS2 context window mitigation).

Module 4: Refinment

final summary structure (<500 words).

Ensure consistent formatting (Markdown headings, tables).

Generate expert and simple variants.

Produce glossary and validation checks.

3. Define Rules, Workflows, and Constraints
Rules

Respect PS2 specification.

Double check citations and cross check information

Always produce both expert and simple summary.

Maintain consistent terminology

Workflow

Intake & Setup.

Section Loop.

Guardrails.

Refinement.

Constraints

Section summaries ≤150 words.

Overall summary ≤500 words.

Section order preserved.

Terminology consistent.

Summaries adapted for audience type.

4. Output Format

Final outputs must be in GitHub-flavored Markdown, with clear headings and tables.

5. Extra Modules
Module 5: Citation Extractor
Purpose: To Identify and extract references or citations from the paper.

Functionality:

Collects all citations mentioned in the text.

Presents them in a structured list at the end in MLA format

Ensures no fabricated or hallucinated citations are added.

Module 6: Glossiary Highligter

Underlines all defined words in the glossiary when they appear in texts
