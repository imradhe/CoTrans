# CoTrans: Colloquial Machine Translation with Fine-Tuning on Spoken Dialogue

## 🎯 Objective

**CoTrans** is a machine translation model fine-tuned on real-world colloquial Indic speech transcripts. By pairing informal speech-style text from the **IndicVoices** dataset with formal translations from **IndicTrans2**, we develop a robust MT system that better reflects everyday speech. The model is benchmarked against existing systems using **BLEU, COMET, ChrF**, **LLM-based evaluation**, **human evaluation**, and a **custom colloquiality metric**.

---

## 🌐 Languages Covered

| Language   | Team Member                      |
|------------|----------------------------------|
| **Hindi**  | Kishan Pipariya (PDEU BTech CS 2025)   |
| **Telugu** | Radhe Shyam Salopanthula (AI4Bharat, Speech Researcher) |
| **Malayalam** | Prof. Manju K (CS Professor, MEC CUSAT, Cochin)      |

---

## 👥 Team & Roles

| Name                         | Role                                                      |
|------------------------------|-----------------------------------------------------------|
| **Radhe Shyam Salopanthula** | Project Lead, Telugu Language Specialist, Speech-NLP Research |
| **Kishan Pipariya**          | Hindi Language Specialist, Dataset Ops & Model Tuning     |
| **Prof. Manju K**            | Pipeline Engineering (MT & LLM Evaluation), Evaluation Feedback from Casual User Perspective |

---

## 🔁 Project Pipeline

### 🗂️ 1. Data Preparation
- ✅ Download and extract data from **IndicVoices**
- ✅ Clean & normalize transcripts per language
- ✅ Generate parallel pairs using **IndicTrans2**: `(colloquial speech → formal English)`
- ✅ Visualize token distribution, sentence length, etc.

### ⚙️ 2. Model Fine-Tuning
- Train/test split (stratified by speaker and sentence type)
- Fine-tune **IndicTrans2** per language
- Build and integrate custom test set:
  - Expressive & emotional utterances
  - Conversational phrases
  - Commands (UMANG, DIGI, Alexa, BigBasket, etc.)
  - Proper nouns, named entities

### 📊 3. Evaluation

#### 🔹 Automatic Metrics
- BLEU
- TER
- ChrF
- COMET

#### 🔹 LLM-based Evaluation
- Use GPT-4 / Claude / Gemini
- Evaluate:
  - Fluency (1–5)
  - Adequacy (1–5)
  - Colloquiality/Naturalness (1–5)

#### 🔹 Human Evaluation
- Multi-rater setup per language
- Criteria:
  - Fluency
  - Semantic adequacy
  - Register match
  - Casual tone realism

#### 🔹 Custom Colloquiality Metric
- % contractions and informal forms
- Discourse marker preservation
- Lexical and syntactic divergence from standard text

---

## 📦 Deliverables

| Artifact                        | Description                                 |
|--------------------------------|---------------------------------------------|
| CoTrans Models (Hindi, Telugu, Malayalam) | Fine-tuned IndicTrans2 checkpoints       |
| Dataset Release                | Cleaned, aligned, and split parallel corpus |
| Evaluation Suite               | BLEU/COMET scripts, LLM prompts, annotation templates |
| Error Analysis                 | Human-curated examples + model deltas       |
| Conference Paper               | Submission to AACL 2025                     |

---

## 📆 Timeline

| Week | Milestone                                             |
|------|-------------------------------------------------------|
| 1    | Dataset download, cleaning, segmentation              |
| 2    | Translation (Colloquial → English), visualization     |
| 3    | Train/val/test split + baseline setup                 |
| 4    | Fine-tune IndicTrans2 models                          |
| 5    | Integrate evaluation metrics (BLEU, LLM, Human)       |
| 6    | Error analysis, result compilation                    |
| 7    | Draft paper + review by advisors                      |
| 8    | Submit to AACL 2025 Main Track                        |

---

## 🎯 Submission Target

| Venue              | Deadline    | Track       | Type                     |
|--------------------|-------------|-------------|--------------------------|
| **AACL 2025 (ARR)**| July 28     | Main Track  | Full Paper (6–8 pages)   |

---

## 💡 Novel Contributions

- First colloquial MT model trained on **speech-aligned Indic transcripts**
- Proposes a **multi-dimensional evaluation suite** for colloquial MT
- Includes a **custom test set** with commands, emotions, and conversational content
- Moves beyond BLEU: LLM + human + custom metrics for colloquiality
- Strong multilingual focus on under-resourced Indic languages

---

## 🚀 Future Work

- **Indic → Indic (Code-Mixed)** translation
- **Indic → Indic (Colloquial)** translation
- **Indic → Indic (Roman Script)** translation
- **Indic → Indic (Standard)** translation
- Full speech-to-speech colloquial MT integration
- Scale to 10+ Indian languages
- Public-facing APIs and benchmarks
