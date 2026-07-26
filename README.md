# LaYRA-Language-model-for-Yield-Reasoning-in-Agriculture
LaYRA: Language Model for Yield Reasoning in Agriculture - a TinyLlama-based model fine-tuned using domain-adaptive training, instruction tuning, and preference alignment for agricultural applications.


````markdown
<div align="center">

# 🌾 LaYRA
### *Language Model for Yield Reasoning in Agriculture*
> **A TinyLlama-based Agriculture Large Language Model specialized for agricultural reasoning and question answering.**

<img src="docs/Architecture.png" width="95%">

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red?style=for-the-badge&logo=pytorch)
![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow?style=for-the-badge)
![PEFT](https://img.shields.io/badge/PEFT-LoRA-success?style=for-the-badge)
![TRL](https://img.shields.io/badge/TRL-DPO-orange?style=for-the-badge)
![Apache 2.0](https://img.shields.io/badge/License-Apache--2.0-blue?style=for-the-badge)

</div>

---

# 🌱 Overview

**LaYRA (Language Model for Yield Reasoning in Agriculture)** is a domain-specific Large Language Model developed by fine-tuning **TinyLlama-1.1B** using a three-stage training pipeline:

- 🌾 Domain-Adaptive Pretraining (DAPT)
- 💬 Instruction Fine-Tuning (SFT)
- ⭐ Direct Preference Optimization (DPO)

The model is designed to understand agricultural terminology, farming practices, crop management, soil science, irrigation, fertilizers, pests, diseases, and agricultural question answering.

---

# ✨ Features

- 🌾 Agriculture-specific Large Language Model
- 🧠 TinyLlama-1.1B based architecture
- 📚 Domain-Adaptive Pretraining (DAPT)
- 💬 Instruction Fine-Tuning (SFT)
- ⭐ Direct Preference Optimization (DPO)
- 🌱 Agricultural Question Answering
- 🌾 Crop & Soil Knowledge
- 🐛 Pest & Disease Understanding
- 💧 Irrigation & Fertilizer Guidance
- 📊 BLEU & BERTScore Evaluation
- 🚀 Built using Hugging Face, PEFT (LoRA), and TRL

---

# 🏗 Model Architecture

<div align="center">
<img src="docs/Architecture.png" width="100%">
</div>

LaYRA extends **TinyLlama-1.1B** with agriculture-specific knowledge through domain adaptation and supervised alignment, enabling better reasoning and response generation for agricultural tasks.

---

# ⚙ Training Pipeline
<div align="center">
<img src="docs/LaYRA_Training_Pipeline.png" width="100%">
</div>

| Stage | Dataset | Samples |
|--------|---------|---------:|
| 🌾 DAPT | AnmolNimmala0/agri-slm-corpus | 10,000 |
| 💬 SFT | KisanVaani/agriculture-qa-english-only | 15,000 |
| ⭐ DPO | Generated Preference Dataset | 908 Preference Pairs |

---

# 🔄 Model Workflow
<div align="center">
<img src="docs/Model_Workflow.png" width="100%">
</div>
The workflow begins with a farmer's query, followed by prompt processing, tokenization, agricultural reasoning using LaYRA, and response generation.

---

# 📁 Repository Structure
```text
LaYRA
│
├── notebooks/
│   ├── 01_domain_adaptive_pretraining.ipynb
│   ├── 02_instruction_finetuning.ipynb
│   ├── 03_preference_alignment_dpo.ipynb
│   ├── 04_model_evaluation.ipynb
│   └── 05_inference_demo.ipynb
│
├── metrics/
│
├── visualizations/
│
├── docs/
│
├── data/
│
├── examples/
│
├── requirements.txt
├── LICENSE
└── README.md
```

---
# 📂 Datasets

| Stage | Dataset |
|--------|---------|
| Domain-Adaptive Pretraining | **AnmolNimmala0/agri-slm-corpus** |
| Instruction Fine-Tuning | **KisanVaani/agriculture-qa-english-only** |
| Direct Preference Optimization | Generated preference pairs from **KisanVaani/agriculture-qa-english-only** |

More details are available in:
- `data/dataset_description.md`
- `data/dataset_sources.md`
---

# 🛠 Technology Stack
| Category | Tools |
|-----------|------|
| Programming | Python |
| Deep Learning | PyTorch |
| LLM Framework | Hugging Face Transformers |
| Fine-Tuning | PEFT (LoRA) |
| Alignment | TRL (DPO) |
| Dataset Library | Hugging Face Datasets |
| Evaluation | BLEU, BERTScore |
| Notebook | Jupyter | Kaggle |

---
# 📊 Evaluation
The model was evaluated using standard Natural Language Generation metrics.
- BLEU Score
- BERTScore
Evaluation files are available in:
```text
metrics/
visualizations/
```

---
# 📒 Notebooks
| Notebook | Description |
|----------|-------------|
| 01_domain_adaptive_pretraining.ipynb | Domain Adaptive Pretraining |
| 02_instruction_finetuning.ipynb | Supervised Fine-Tuning |
| 03_preference_alignment_dpo.ipynb | Direct Preference Optimization |
| 04_model_evaluation.ipynb | Evaluation |
| 05_inference_demo.ipynb | Model Inference |

---
# 🚀 Installation
```bash
git clone https://github.com/<YOUR_USERNAME>/LaYRA.git
```

---

# 💡 Future Improvements
- Retrieval-Augmented Generation (RAG)
- Multilingual Agricultural Support
- Agricultural Agent Integration
- Mobile Deployment
- Quantized Inference
- Larger Agriculture Corpus
- Reinforcement Learning from Human Feedback (RLHF)

---

# 📜 Citation
```bibtex
@misc{layra2026,
  title={LaYRA: Language Model for Yield Reasoning in Agriculture},
  author={Deepak Kumar},
  year={2026},
  howpublished={GitHub Repository}
}
```

---
# 📄 License
This project is licensed under the **Apache License 2.0**.
---

# 👨‍💻 Author

**Deepak Kumar**

AI/ML Engineer | Large Language Models | NLP | Deep Learning

---

<div align="center">

### ⭐ If you found this project useful, consider giving it a Star!

Made with ❤️ for Agriculture and Open Source.

</div>
````
