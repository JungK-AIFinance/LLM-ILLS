# LLM-ILLS
Large Language Model - Impromptu Language Learning Scripts

---

## 🎯 What is LLM‑ILLS?

LLM‑ILLS is an open-source framework that converts **any textual input**—articles, reports, domain-specific documents—into **high-impact audio drill scripts** generated via LLMs and informed by evidence-based learning principles (spaced recall, active retrieval, contextual embedding).

Rather than flashcards or translated lists, LLM‑ILLS delivers **multi-turn conversational drills** with deliberate pauses designed to compel learner responses and reinforce vocabulary within meaningful contexts.

---

## 🧩 Core Pipeline

1. **Keyword Extraction**  
   - Filters domain-relevant vocabulary using novelty and frequency rules.

2. **Contextualizer**  
   - Associates each word with existing or synthetic example sentences.

3. **Script Generator**  
   - Uses LLM (prompt-engineered or fine-tuned) to output structured drills:
     - **Intro**: Tutor prompts vocabulary → `<pause_xxs>`
     - **Repeat**: Learner response → `<pause_yys>`
     - **Extend**: Tutor prompts usage or synonyms

4. **Validator & Calibrator**  
   - Enforces:
     - 3-turn structure per word  
     - Correct pause tags (e.g., `<pause_3s>`)  
     - No direct translation—only context-based prompts

5. **Formatter**  
   - Serializes into **JSON** or **SSML** for use in TTS or playback UIs.

---

## 📊 Data & Timing Foundation

Grounded in a curated dataset of annotated tutor-learner scripts, featuring:

- **Turn-type labels** (`[INTRO]`, `[REPEAT]`, `[EXTEND]`)  
- **Pause durations** in seconds  
- **Vocabulary density statistics** (~10 words per 8-minute script)

These form the statistical priors that drive script pacing and structure during generation.

---

## 🚀 Roadmap

| Phase | Goal | Deliverable |
|------|------|-------------|
| **0** | Data Bootstrapping | Annotated dataset (50–100 vocab drills) |
| **1** | Prototype Generation | LLM-generated script for 1–2 vocabulary items |
| **2** | Pipeline Build | Full automated flow: input → script → formatted output |
| **3** | Pilot Evaluation | Measure learner recall (immediate & 24h) |
| **4** | Scale-Up | Domain-specific tuning + analytics dashboard |
| **5** | Open Release | Community-ready code, examples, and docs |

---

## ✅ Validation & QA

- **Script-level validation** ensures each word receives:
  - A 3-turn drill
  - Proper pause tags
  - Contextual usage only

- **Behavioral evaluation** compares recall efficacy with manual benchmarks.

---

## 📥 Contribution & Collaboration

We’re seeking collaboration on:

- **Annotated script examples**  
- **Prompt templates** or **fine-tuning workflows**  
- **Validation modules** or **simulation tools**  
- **Audio playback or TTS UI integrations**

Help build a rigorous, community-powered tool for retrieval-based language learning.

---

## 🧠 Why This Matters

LLM‑ILLS operationalizes **scientific audio pedagogy at scale**—delivering structured, context-driven learning experiences far beyond passive listening or flashcard drills. It encodes timing, dialog structure, and cognitive effort into a repeatable pipeline.

---

## 📄 License

Distributed under the **MIT License**—see [LICENSE](LICENSE) for details.
