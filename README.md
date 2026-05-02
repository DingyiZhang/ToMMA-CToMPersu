# ToMMA-CToMPersu

**Persuasion Should Be Double-Blind: A Multi-Domain Dialogue Dataset with Faithfulness Based on Causal Theory of Mind**

Dingyi Zhang, Linhai Zhang, Fanglei Qu, Ziqing Zhuang, and Deyu Zhou

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache--2.0-blue.svg)](LICENSE)
[![Dataset](https://img.shields.io/badge/Dataset-HuggingFace-yellow)](https://huggingface.co/datasets/KamijioTouma/ToMMA-CToMPersu)
[![Paper](https://img.shields.io/badge/Paper-PDF-red)](paper/Persuasion_Should_be_Double.pdf)

---

## 📌 Paper

This repository accompanies our paper:

> **Persuasion Should Be Double-Blind: A Multi-Domain Dialogue Dataset with Faithfulness Based on Causal Theory of Mind**

- 📄 **Paper PDF:** [View the author version](paper/Persuasion_Should_be_Double.pdf)
- 🤗 **Hugging Face Dataset:** [KamijioTouma/ToMMA-CToMPersu](https://huggingface.co/datasets/KamijioTouma/ToMMA-CToMPersu)
- 💬 **Prompt Design:** [PromptDesign/](PromptDesign/)
- 📁 **Dataset Files:** [dataset/](dataset/)

> **Version notice.** This repository hosts the author accepted / camera-ready author version of the paper.  
> The final published version will appear in IEEE Xplore once available. This repository will be updated with the DOI and official citation after publication.

---

## 🧠 Overview

Persuasive dialogue is central to human communication, but existing LLM-generated persuasion datasets often suffer from an important limitation: the same model may implicitly generate both the persuader and the persuadee, which can lead to information leakage and unrealistic interactions.

To address this issue, we propose **ToMMA**, a multi-agent framework guided by **Causal Theory of Mind**. ToMMA enforces role separation between the persuader and persuadee, supports double-blind dialogue generation, and encourages the persuader to infer and respond to the persuadee’s underlying beliefs and desires.

Using ToMMA, we construct **CToMPersu**, a large-scale, multi-turn, multi-domain persuasive dialogue dataset designed to capture more realistic persuasion dynamics.

---

## ✨ Highlights

- **Double-blind persuasion setting**  
  The persuader does not directly access the persuadee’s private mental state and must infer it through interaction.

- **Causal Theory-of-Mind guidance**  
  The framework models persuasion through belief and desire components, encouraging more faithful and logically consistent persuasive behavior.

- **Multi-agent dialogue generation**  
  ToMMA separates mental-state generation, dialogue generation, and observer-based quality control.

- **Large-scale multi-domain dataset**  
  CToMPersu contains persuasive dialogues across diverse domains, supporting research on realistic and cognitively grounded persuasion.

- **Evaluation and downstream utility**  
  Experiments show that CToMPersu improves persuasive dialogue generation when used as an external knowledge base for in-context learning.

---

## 📦 Dataset

You can load the dataset from Hugging Face:

```python
from datasets import load_dataset

dataset = load_dataset("KamijioTouma/ToMMA-CToMPersu")
