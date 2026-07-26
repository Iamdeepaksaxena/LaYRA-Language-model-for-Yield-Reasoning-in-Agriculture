# Dataset Description

LaYRA (Language Model for Yield Reasoning in Agriculture) was developed through a three-stage fine-tuning pipeline consisting of Domain-Adaptive Pretraining (DAPT), Instruction Fine-Tuning (SFT), and Direct Preference Optimization (DPO). Each training stage utilizes agriculture-specific datasets to progressively enhance the model's domain knowledge, instruction-following capability, and response quality.

---

## Training Pipeline

| Stage | Dataset | Samples | Purpose |
|--------|----------|---------:|---------|
| Domain-Adaptive Pretraining (DAPT) | **AnmolNimmala0/agri-slm-corpus** | 10,000 | Adapt TinyLlama to agricultural language and terminology |
| Instruction Fine-Tuning (SFT) | **KisanVaani/agriculture-qa-english-only** | 15,000 | Improve instruction following and agricultural question answering |
| Direct Preference Optimization (DPO) | **Preference pairs generated from KisanVaani/agriculture-qa-english-only** | 908 preference pairs | Align model responses with preferred human-like answers |

---

## Stage 1: Domain-Adaptive Pretraining (DAPT)

### Dataset

**AnmolNimmala0/agri-slm-corpus**

The first stage adapts the base TinyLlama model to the agriculture domain by exposing it to agriculture-specific text collected from the **AnmolNimmala0/agri-slm-corpus** dataset.

This stage enables the model to learn:

- Agricultural terminology
- Crop management concepts
- Soil science
- Pest and disease information
- Farming practices
- Agricultural publications and literature

**Dataset Size Used**

- 10,000 randomly sampled documents

---

## Stage 2: Instruction Fine-Tuning (SFT)

### Dataset

**KisanVaani/agriculture-qa-english-only**

After domain adaptation, the model is instruction fine-tuned using agricultural question-answer pairs from the **KisanVaani/agriculture-qa-english-only** dataset.

The objective of this stage is to improve:

- Question answering
- Instruction following
- Context understanding
- Natural language generation
- Agricultural reasoning

**Dataset Size Used**

- 15,000 instruction-response pairs

---

## Stage 3: Direct Preference Optimization (DPO)

### Dataset

**Preference pairs generated from KisanVaani/agriculture-qa-english-only**

To further improve response quality, preference pairs were generated from the **KisanVaani/agriculture-qa-english-only** dataset and used for Direct Preference Optimization (DPO).

Each preference pair contains:

- Prompt
- Preferred (Chosen) response
- Less preferred (Rejected) response

The model learns to generate responses that better align with preferred outputs.

**Preference Pairs Used**

- 908 preference pairs

---

## Data Preprocessing

The datasets were preprocessed before training.

The preprocessing pipeline included:

- Text cleaning
- Duplicate removal (where applicable)
- Tokenization using the TinyLlama tokenizer
- Sequence truncation
- Formatting for supervised fine-tuning
- Preference pair generation for DPO

---

## Final Training Summary

| Stage | Training Objective |
|--------|-------------------|
| DAPT | Learn agricultural domain knowledge from **AnmolNimmala0/agri-slm-corpus** |
| SFT | Learn instruction following using **KisanVaani/agriculture-qa-english-only** |
| DPO | Improve response preference and answer quality using generated preference pairs |

---

## Base Model

**TinyLlama/TinyLlama-1.1B-intermediate-step-1431k-3T**

LaYRA was developed by progressively fine-tuning the TinyLlama base model through DAPT, SFT, and DPO.

---

This multi-stage training pipeline transforms the **TinyLlama-1.1B** base model into **LaYRA**, a domain-specialized Large Language Model designed for agricultural reasoning, knowledge understanding, and question answering.

