# 🎓 From Language to Learning
### An LLM-Driven Framework for Multilingual Educational Content

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Datasets%20%26%20Models-blue)](https://huggingface.co/Kamyar-zeinalipour)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)

**Official Artifact Repository** for the PhD Thesis: *"From Language to Learning: An LLM-Driven Framework for Multilingual Educational Content."*

---

## 📖 Overview

This repository contains the **System Prompts**, **Filtering Scripts**, and **Reproducibility Artifacts** for the "From Language to Learning" framework. This work utilizes a two-stage distillation process (Teacher $\rightarrow$ Student) to generate high-quality educational content across **5 languages** (English, Italian, Turkish, Arabic, Persian) and **3 pedagogical domains**:

1.  🧩 **Gamified Learning:** Educational Crossword Generation.
2.  📝 **Formal Assessment:** Multiple-Choice & Short-Answer Quizzes.
3.  ✍️ **Pedagogical Intervention:** Automated Syntax Feedback.

---

## 🌍 Part I: Multilingual Crossword Generation

We release the **Instruct-Series** datasets (text-to-clue) and **Legacy** datasets (answer-to-clue), along with fine-tuned models.

### 🇺🇸 English (Chapter 4)
*   **Methodology:** Context-grounded clue generation via instruction tuning.
*   **Key Resources:**
    *   🤗 **Dataset (Clue-Instruct):** [link](https://huggingface.co/datasets/azugarini/clue-instruct)
    *   🤗 **Legacy Dataset (Answer-Only):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/EN_CW)
    *   **Prompts:** [View Prompts](Part_I_Crosswords/English/prompts.md)

### 🇮🇹 Italian (Chapter 5)
*   **Methodology:** Style-controlled generation (Bare Noun, Copular, Definite Determiner).
*   **Key Resources:**
    *   🤗 **Dataset (Italian-Clue-Instruct):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/ita_cw_text)
    *   🤗 **Legacy Dataset (Answer-Only):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/ITA_CW)
    *   🤖 **Model (Llama3-8B):** [link](https://huggingface.co/Kamyar-zeinalipour/Llama3-8B-Ita-Text-to-Cross)
    *   **Prompts:** [View Prompts](Part_I_Crosswords/Italian/prompts.md)

### 🇹🇷 Turkish (Chapter 6)
*   **Methodology:** Agglutination-aware generation to prevent stem leakage.
*   **Key Resources:**
    *   🤗 **Dataset (T4TAC):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/T4TAC)
    *   🤗 **Legacy Dataset (TAC):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/TAC)
    *   💻 **Code:** [GitHub Repo](https://github.com/KamyarZeinalipour/CW_Clue_Gen_tr)
    *   🤖 **Model (Llama-7B):** [link](https://huggingface.co/Kamyar-zeinalipour/llama7B_turkish_crossword_clue_gen)

### 🇸🇦 Arabic (Chapter 7)
*   **Methodology:** Validated generation for RTL scripts with diacritic normalization.
*   **Key Resources:**
    *   🤗 **Dataset (Arabic-Clue-Instruct):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/Arabic-Clue-Instruct)
    *   🤗 **Legacy Dataset (AR_CW):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/AR_CW)
    *   💻 **Code:** [GitHub Repo](https://github.com/KamyarZeinalipour/Arabic-Text-to-Crosswords)
    *   🤖 **Model (Llama3-8B):** [link](https://huggingface.co/Kamyar-zeinalipour/Llama3-8B-Ar-Text-to-Cross)

---

## 🧠 Part II: Question Generation (Quiz & MCQ)

Specialized models for generating assessment items in low-resource languages.

### 🇹🇷 Turkish Quiz Generation (Chapter 8)
*   **Scope:** Multiple-Choice (MCQ) and Short-Answer (SAQ) generation.
*   **Key Resources:**
    *   🤗 **Dataset (Turkish-Quiz-Instruct):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/Turkish-Quiz-Instruct)
    *   💻 **Code:** [GitHub Repo](https://github.com/KamyarZeinalipour/Turkish_Quiz_Generator)
    *   🤖 **Model (Simple Llama-7B):** [link](https://huggingface.co/Kamyar-zeinalipour/TR_QUIZ_GEN_SIMPLE_LLAMA7B)
    *   🤖 **Model (Multi Llama-13B):** [link](https://huggingface.co/Kamyar-zeinalipour/TR_QUIZ_GEN_MULTI_LLAMA13B)

### 🇮🇷 Persian MCQ Generation (Chapter 9)
*   **Scope:** 3-Stage Prompt Cascade (Augmentation $\to$ Generation $\to$ Refinement).
*   **Key Resources:**
    *   🤗 **Dataset (PersianMCQ-Instruct):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/PersianMCQ-instruct)
    *   💻 **Code:** [GitHub Repo](https://github.com/KamyarZeinalipour/Persian_MCQ)
    *   🤖 **Model (Gemma2-9B):** [link](https://huggingface.co/Kamyar-zeinalipour/PMCQ-Gemma2-9b)
    *   🤖 **Model (Llama3.1-8B):** [link](https://huggingface.co/Kamyar-zeinalipour/PMCQ-Llama3.1-8b)
    *   **Prompts:** [View Prompts](Part_II_Question_Generation/Persian/prompts.md)

---

## ✍️ Part III: Writing Assistance

### 🇬🇧 Automated Syntax Feedback (Chapter 10)
*   **Scope:** Category-structured syntax feedback for student essays (e.g., Modifiers, Articles, Punctuation).
*   **Key Resources:**
    *   🤗 **Dataset (Essay-Syntax-Instruct):** [link](https://huggingface.co/datasets/Kamyar-zeinalipour/Essay-Syntax-Instruct)
    *   🤖 **Model (Llama2-13B):** [link](https://huggingface.co/Kamyar-zeinalipour/Llama2-13B-Syntax-Instruct)
    *   🤖 **Model (Mistral-7B):** [link](https://huggingface.co/Kamyar-zeinalipour/Mistral7B-Syntax-Instruct)
    *   **Prompts:** [View Prompts](Part_III_Writing_Feedback/English_Syntax/prompts.md)

---

## 🛠️ Repository Structure

The repository mirrors the thesis structure. Each folder contains the specific system prompts (JSON templates) and sample I/O used to generate the **Instruct** datasets.

```text
From-Language-to-Learning/
├── Part_I_Crosswords/
│   ├── English/   # Clue-Instruct Prompts
│   ├── Italian/   # Style-Specific Prompts
│   ├── Turkish/   # Agglutination-Aware Prompts
│   └── Arabic/    # RTL & Diacritic Prompts
├── Part_II_Question_Generation/
│   ├── Turkish/   # Quiz Generation Prompts
│   └── Persian/   # 3-Stage Cascade Prompts
└── Part_III_Writing_Feedback/
    └── English_Syntax/ # Feedback Schema Prompts
```

### Reproducibility Note
The filtering logic (e.g., removing text < 50 words, filtering keywords 3-20 chars) and data processing scripts are documented in the methodology sections of the thesis and implemented in the linked GitHub repositories for each language.

---

## 📜 Citation

If you use these resources in your research, please cite the thesis or the relevant papers:

```bibtex
@phdthesis{Zeinalipour2025,
  author  = {Kamyar Zeinalipour},
  title   = {From Language to Learning: An LLM-Driven Framework for Multilingual Educational Content},
  school  = {University of Siena},
  year    = {2025}
}
```

*Individual paper citations can be found in the `CITATIONS.md` file.*

## License
The code and scripts in this repository are licensed under the **MIT License**. The datasets and prompts released as part of this thesis are licensed under **CC BY 4.0**.
```
