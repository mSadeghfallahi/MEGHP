# MEGHP
MEG Harry Potter: Can an LLM understand fictioanl text Like Us?
Investigating **brain–model alignment** in literary comprehension using **Magnetoencephalography (MEG)** and **GPT-2 XL** embeddings on *Harry Potter and the Sorcerer’s Stone*.

---

## ✨ Project Overview

Do large language models (LLMs) understand stories the way humans do?
This project explores whether LLM representations align with human brain activity during natural reading of **Harry Potter**.

We recorded MEG signals while participants read the novel and compared them with contextual embeddings from GPT-2 XL. The results highlight where and why models diverge from human narrative processing.

---

## 🧩 Research Question

> **Can an LLM’s internal representations align with our neural processing of a narrative (Harry Potter)?**

---

## 🛠️ Methods

### 📊 Data Collection
* **Source: https://arxiv.org/abs/2311.09308 
* **Participants**: 12
* **Stimulus**: Chapters 9 & 10 (*9,651 words*)
* **Presentation**: Each word shown for *500 ms*
* **Modality**: Magnetoencephalography (MEG, 1 kHz)
* **Preprocessing**: Signal Space Separation (with temporal extension)

### 🤖 Language Model

* **Model**: GPT-2 XL (1.5B parameters)
* **Context window**: 19 preceding words
* **Embeddings**: Word-level contextual vectors

### 🔎 Analysis Pipeline

1. Ridge regression → Identify model layers with strongest (mis)alignment
2. Compare **MEG activity (Y)** vs **LM embeddings (X)**
3. Regional divergence analysis across MEG channels
4. Word-category annotation: *Action, Emotion, Description, Dialogue, Magic*

---

## 📈 Key Findings

### ✅ Convergence

* Simple actions & descriptive sentences aligned well

  * *“They were in a corridor.”*
  * *“I heard something.”*

### ❌ Divergence

* Emotionally & physically charged contexts diverged strongly

  * *“No!” shouted Hermione Granger.*
  * *Madam Hooch was bending over Neville, her face as white as his.*

### 🧠 Brain Regions of Divergence

* **Midline Parietal** → memory, imagination, scene construction
* **Midline Frontal** → emotional evaluation, social inference
* **Left Temporal** → deep semantic abstraction, discourse integration

---

## 📜 Discussion

* **Action words**: High divergence due to sensorimotor grounding → LLMs lack embodied experience.
* **Emotion & tension**: LLMs underperform in capturing rich emotional/social contexts.
* **Takeaway**: LLMs can mirror certain aspects of narrative processing, but diverge in **emotionally charged** and **embodied cognition** contexts.

---

## 🚧 Limitations & Future Work

* 📌 **Limitations**: Word meanings shaped by culture & personal experience.
* 🔮 **Future Work**:

  * Larger & more diverse participant populations
  * Comparison across different LLM architectures
