# Dataset Sources

LaYRA was trained using publicly available agriculture datasets from the Hugging Face Hub. Different datasets were used at each stage of the fine-tuning pipeline.

---

# 1. Domain-Adaptive Pretraining (DAPT)

## Dataset

**AnmolNimmala0/agri-slm-corpus**

### Hugging Face Repository

https://huggingface.co/datasets/AnmolNimmala0/agri-slm-corpus

### Purpose

Used for Domain-Adaptive Pretraining (DAPT) to adapt the TinyLlama base model to agricultural language, terminology, and domain knowledge.

### Data Used

- 10,000 randomly sampled documents

---

# 2. Instruction Fine-Tuning (SFT)

## Dataset

**KisanVaani/agriculture-qa-english-only**

### Hugging Face Repository

https://huggingface.co/datasets/KisanVaani/agriculture-qa-english-only

### Purpose

Used for supervised instruction fine-tuning to improve agricultural question answering and instruction-following capabilities.

### Data Used

- 15,000 question-answer pairs

---

# 3. Direct Preference Optimization (DPO)

## Dataset

**Preference pairs generated from KisanVaani/agriculture-qa-english-only**

### Source Dataset

https://huggingface.co/datasets/KisanVaani/agriculture-qa-english-only

### Purpose

Used to create preference pairs for Direct Preference Optimization (DPO), enabling the model to learn preferred responses over less preferred alternatives.

### Data Used

- 908 preference pairs

### Pair Structure

Each preference pair consists of:

- Prompt
- Chosen Response
- Rejected Response

---

# Dataset Usage Summary

| Training Stage | Dataset | Samples |
|----------------|---------|---------:|
| Domain-Adaptive Pretraining (DAPT) | AnmolNimmala0/agri-slm-corpus | 10,000 |
| Instruction Fine-Tuning (SFT) | KisanVaani/agriculture-qa-english-only | 15,000 |
| Direct Preference Optimization (DPO) | Preference pairs generated from KisanVaani/agriculture-qa-english-only | 908 preference pairs |
