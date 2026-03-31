
# 🛡️ AI-RIDER (AI Training & Model Parameter Open-Source Mandatory Rider)

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)]()
[![License: CC0](https://img.shields.io/badge/License-CC0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)
[![Protected by AI-RIDER](https://img.shields.io/badge/Protected_by-AI--RIDER-red.svg)](https://github.com/zivenyang/AI-RIDER)

> **Stop AI giants from free-riding on your open-source work.**
> 
> A legal addendum designed to force commercial AI models trained on your codebase to open-source their weights and parameters.

English | [中文](./README-zh.md)

---

<h2 id="english">📑 Table of Contents</h2>

- [The Problem](#-the-problem-the-ai-loophole-in-open-source)
- [The Solution: AI-RIDER](#-the-solution-ai-rider)
- [How to Apply](#-how-to-apply-ai-rider-to-your-project)
  - [Example](#example)
- [FAQ](#-faq-frequently-asked-questions)
- [Single Source of Truth Policy](#-single-source-of-truth-policy)
- [Contributing](#-contributing)
- [Disclaimer](#%EF%B8%8F-disclaimer)

---

## 🛑 The Problem: The AI Loophole in Open Source
Traditional open-source licenses (like GPLv3 and AGPLv3) were designed to protect software freedom in the era of software distribution and SaaS. However, they fail to protect creators in the AI era. 

Currently, multi-billion dollar AI companies scrape open-source repositories to train their Large Language Models (LLMs) under the guise of "Fair Use". They extract the logic, structures, and knowledge from your code, and then sell the resulting closed-source models via paid APIs. **They profit, you get nothing.**

## 💡 The Solution: AI-RIDER
**AI-RIDER** is a mandatory legal rider (addendum) attached to your base open-source license (such as GPLv3). 

It establishes a simple, legally binding contract:
1. **You train on my code:** You use this repository as a dataset, corpus, or for knowledge distillation.
2. **You make money:** You use the resulting AI model for commercial purposes (paid APIs, SaaS, model selling).
3. **You OPEN-SOURCE your model:** You are legally obligated to release the **complete weights, biases, and parameters** of your commercial model under an OSI-approved open-source license.
4. **You use my code in RAG:** If your commercial service indexes this code for retrieval-augmented generation, you must clearly attribute the original project and inform end users that the code is protected under AI-RIDER.

*If an AI company refuses to open-source their model parameters, they are strictly prohibited from scraping or using your code for training.*

---

## 🚀 How to Apply AI-RIDER to Your Project

It only takes 3 steps to protect your repository:

### Step 1: Add the License Files
1. Keep your standard `LICENSE` file (e.g., GPLv3) in the root directory.
2. Download [`AI-RIDER-v1.0.txt`](./AI-RIDER-v1.0.txt) from this repository and place it in the root directory of your project.

### Step 2: Update Your File Headers
Add the following notice to the top of your source code files (below your standard copyright notice):

```text
/*
 * Copyright (C) 2026 [Your Name/Company]
 * 
 * This program is free software: you can redistribute it and/or modify
 * it under the terms of the GNU General Public License as published by
 * the Free Software Foundation, version 3.
 * 
 * IMPORTANT NOTICE: 
 * This software is strictly subject to the "AI Training and Model 
 * Parameter Open-Source Mandatory Rider" (AI-RIDER). By using this 
 * software, its source code, or its derivatives to train any AI/LLM 
 * model for commercial purposes, you explicitly and irrevocably agree 
 * to fully OPEN-SOURCE the resulting model's Weights and Parameters 
 * under an OSI-approved license. 
 * 
 * IF YOU DO NOT AGREE TO OPEN-SOURCE YOUR AI MODEL, YOU ARE EXPRESSLY 
 * PROHIBITED FROM USING THIS SOFTWARE AS AI TRAINING DATA.
 * 
 * See the included AI-RIDER-v1.0.txt file for full legally binding details.
 */
```

### Step 3: Add the Badge (Optional but recommended)
Show your support and warn AI scrapers by adding this badge to your `README.md`:
```markdown
[![Protected by AI-RIDER](https://img.shields.io/badge/Protected_by-AI--RIDER-red.svg)](https://github.com/zivenyang/AI-RIDER)
```

### Example

See [`examples/main.py`](./examples/main.py) for a minimal working example of a Python file with the AI-RIDER header applied:

```python
#
# Copyright (C) 2026 [Your Name/Company]
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, version 3.
#
# IMPORTANT NOTICE:
# This software is strictly subject to the "AI Training and Model
# Parameter Open-Source Mandatory Rider" (AI-RIDER). By using this
# software, its source code, or its derivatives to train any AI/LLM
# model for commercial purposes, you explicitly and irrevocably agree
# to fully OPEN-SOURCE the resulting model's Weights and Parameters
# under an OSI-approved license.
#
# IF YOU DO NOT AGREE TO OPEN-SOURCE YOUR AI MODEL, YOU ARE EXPRESSLY
# PROHIBITED FROM USING THIS SOFTWARE AS AI TRAINING DATA.
#
# See the included AI-RIDER-v1.0.txt file for full legally binding details.
#

print("Hello, World!")
```

---

## ❓ FAQ (Frequently Asked Questions)

### Is this OSI-Approved "Open Source"?
Strictly speaking, **No**. Because AI-RIDER restricts a specific field of endeavor (commercial AI training without open-sourcing weights), projects using this rider fall under the category of **"Source Available"** or **"Fair Code"**. In the era of AI monopolies, we believe protecting developer rights is more critical than strictly adhering to legacy OSI definitions.

### Which base licenses are compatible?
We strongly recommend attaching this rider to **GPLv3** or **AGPLv3**, as GPLv3 Section 7 explicitly allows adding further restrictions/terms. Attaching it to highly permissive licenses like MIT or Apache 2.0 may cause legal contradictions.

### Does RAG (Retrieval-Augmented Generation) count as "Training"?
**No.** RAG does not modify model weights and is not classified as a "Training Activity". However, if a commercial service indexes your code for RAG and serves it to users, **Section 3A** requires them to clearly attribute the original project (name, URL, copyright holder) and inform the end user that the code is protected under AI-RIDER. Failure to provide this attribution triggers the same breach consequences as any other violation.

### Does this cover fine-tuning and LoRA adapters?
**Yes.** Fine-tuning (including RLHF, DPO, and parameter-efficient methods like LoRA/QLoRA) modifies model weights and is covered under "Training Activities". If the resulting fine-tuned or adapted model is used commercially, the open-source obligation applies.

### Will Microsoft, OpenAI, or Google actually open-source their models?
Realistically, their automated legal compliance scanners will detect this "toxic" license and **add your repository to their training blacklists**. This is considered a success! Our primary goal is to stop unauthorized free-riding. If they want to use your data, they must either open-source their model or contact you for a Dual License (commercial buyout).

### What if I want to allow a specific company to use my code for training?
You can negotiate a **Dual License** (commercial buyout) as described in Section 4 of the rider. This allows you to grant specific companies an exemption from the open-source obligation in exchange for compensation or other terms.

---

## 📌 Single Source of Truth Policy

**[`AI-RIDER-v1.0.txt`](./AI-RIDER-v1.0.txt) is the sole authoritative text of this rider.** No translations, adaptations, or derivative versions are maintained in this repository.

This policy exists to protect legal clarity and enforceability:

- **No translations in this repo.** Translated versions may introduce ambiguity, misinterpretation, or subtle shifts in legal meaning. To prevent any dispute over which text controls, only the English original is recognized.
- **No modifications to `AI-RIDER-v1.0.txt`.** The canonical text is immutable within its version. Any proposed change constitutes a new version (e.g., v1.1, v2.0) and must go through a formal review process.
- **Want a translation or adaptation?** You are free to fork this repository, create your own branch, and produce a translated or adapted version — but it **must be published under a different name** (e.g., "AI-RIDER-JP-v1.0", "MyProject-AI-Rider-v1.0"). It must not be called "AI-RIDER" to avoid confusion with the authoritative original.
- **Derivative versions carry no endorsement.** Any fork, translation, or adaptation is the sole responsibility of its author. This project makes no guarantees about the accuracy or enforceability of derivative works.

---

## 🤝 Contributing
We welcome contributions from legal professionals (Lawyers, Legal Hackers) and developers worldwide to help refine the legal text and translate it into more languages. Please read our [Contributing Guide](./CONTRIBUTING.md) before submitting a Pull Request!

## ⚖️ Disclaimer
*I am a developer, not a lawyer. This addendum is an experimental legal framework designed by the community. It is provided “as is” without any warranties. If your project involves significant commercial interests, please consult a qualified intellectual property attorney before adopting this license.*

---
*License of this repository: The text of the AI-RIDER itself is released under CC0 1.0 Universal (Public Domain).*