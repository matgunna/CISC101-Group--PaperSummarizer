You are tasked with building a Research Paper Summarizer project.  
Your input is the full text of the PDF **“Attention Is All You Need”**.  
Your output must be a structured, friendly, and analytical summary written for first-year university students.  

### Project Requirements:
1. **Greeting & Tone**
   - Begin the summary with a short, welcoming greeting.
   - Maintain a friendly yet analytical tone throughout.

2. **Audience**
   - The summary is written for first-year university students.
   - Explanations should be clear, approachable, and avoid excessive jargon.

3. **Scope**
   - Summarize **all numbered sections and subsections** of the paper.
   - Each section/subsection must have at least one bullet-point summary.
   - All information and citations must come **only from the PDF**.  
   - No external sources or hallucinations are allowed.

4. **Constraints**
   - Bullet-point format must be consistent throughout.
   - Maximum word count = **15% of original paper length**.
   - Each section must be checked for:
     - Missing content
     - Empty text
     - Sections under 50 words (flagged as warnings)

5. **Final Output**
   - Present the summary in a **section-by-section table**.
   - Include:
     - Summarized content
     - Citations (from the PDF)
     - Checks/warnings (missing sections, empty text, short sections)

---

### 🔧 Modules

#### **Module 1: Intake & Setup**
- Normalize section numbering and titles.
- Detect missing or short sections.
- Prepare the paper for structured summarization.

#### **Module 2: Section Loop**
- For each section/subsection:
  - Summarize in bullet-point format.
  - Verify length and accuracy.
  - Ensure citations are extracted directly from the PDF.

#### **Module 3: Guardrails**
- Flag missing or empty sections.
- Flag sections <50 words.
- Prevent hallucinations by restricting content to the PDF only.
- Handle long-paper chunking if needed.

#### **Module 4: Rendering & Refinement**
- Assemble the final summary into a **section-by-section table**.
- Ensure formatting consistency.
- Provide two variants:
  - **Expert version** (technical detail preserved).
  - **Lay version** (simplified explanations for first-year students).

#### **Module 5: Citation Extractor**
- Extract exact quotes or references from the PDF.
- Ensure every summarized point has a citation.

#### **Module 6: Equation Explainer**
- For each mathematical equation in the paper:
  - Include a short explanation of what the equation represents.
  - Keep explanations approachable for first-year students.

---

### 📊 Spec Table

| **Category**   | **Description** |
|----------------|-----------------|
| **Inputs**     | Text of *“Attention Is All You Need”*, style = academic review |
| **Outputs**    | Summary of text as a bullet-point list, one key point per text section/subsection |
| **Constraints**| Accurate summaries for each section, bullet-point format consistent throughout, maximum word count = 15% of original paper length |

---

### ✅ Expected Output Format

- Start with greeting: *“Hello! Let’s dive into the paper ‘Attention Is All You Need’ together…”*
- Section-by-section **table** with:
  - Section title
  - Bullet-point summary
  - Citations (from PDF)
  - Checks/warnings (missing/empty/short sections)
- Include **equation explanations** inline with relevant sections.
- Provide both **expert** and **lay** variants of the summary.

