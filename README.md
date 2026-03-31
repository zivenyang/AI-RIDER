
# 🛡️ AI-RIDER (AI Training & Model Parameter Open-Source Mandatory Rider)

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)]()
[![License: CC0](https://img.shields.io/badge/License-CC0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)
[![Protected by AI-RIDER](https://img.shields.io/badge/Protected_by-AI--RIDER-red.svg)](https://github.com/zivenyang/AI-RIDER)

> **Stop AI giants from free-riding on your open-source work.**
> 
> A legal addendum designed to force commercial AI models trained on your codebase to open-source their weights and parameters.

[English](#english) | [中文说明](#中文说明)

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

*If an AI company refuses to open-source their model parameters, they are strictly prohibited from scraping or using your code for training.*

---

## 🚀 How to Apply AI-RIDER to Your Project

It only takes 2 steps to protect your repository:

### Step 1: Add the License Files
1. Keep your standard `LICENSE` file (e.g., GPLv3) in the root directory.
2. Download [`AI-RIDER-v1.0.txt`](./AI-RIDER-v1.0.txt) from this repository and place it in the root directory of your project.

### Step 2: Update Your File Headers
Add the following notice to the top of your source code files (below your standard copyright notice):

```text
/*
 * Copyright (C) 2026[Your Name/Company]
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
 * See the included AI-RIDER.txt file for full legally binding details.
 */
```

### Step 3: Add the Badge (Optional but recommended)
Show your support and warn AI scrapers by adding this badge to your `README.md`:
```markdown
[![Protected by AI-RIDER](https://img.shields.io/badge/Protected_by-AI--RIDER-red.svg)](https://github.com/zivenyang/AI-RIDER)
```

---

## ❓ FAQ (Frequently Asked Questions)

### Is this OSI-Approved "Open Source"?
Strictly speaking, **No**. Because AI-RIDER restricts a specific field of endeavor (commercial AI training without open-sourcing weights), projects using this rider fall under the category of **"Source Available"** or **"Fair Code"**. In the era of AI monopolies, we believe protecting developer rights is more critical than strictly adhering to legacy OSI definitions.

### Which base licenses are compatible?
We strongly recommend attaching this rider to **GPLv3** or **AGPLv3**, as GPLv3 Section 7 explicitly allows adding further restrictions/terms. Attaching it to highly permissive licenses like MIT or Apache 2.0 may cause legal contradictions.

### Will Microsoft, OpenAI, or Google actually open-source their models?
Realistically, their automated legal compliance scanners will detect this "toxic" license and **add your repository to their training blacklists**. This is considered a success! Our primary goal is to stop unauthorized free-riding. If they want to use your data, they must either open-source their model or contact you for a Dual License (commercial buyout).

---

## 🤝 Contributing
We welcome contributions from legal professionals (Lawyers, Legal Hackers) and developers worldwide to help refine the legal text and translate it into more languages. Please submit a Pull Request!

## ⚖️ Disclaimer
*I am a developer, not a lawyer. This addendum is an experimental legal framework designed by the community. It is provided "as is" without any warranties. If your project involves significant commercial interests, please consult a qualified intellectual property attorney before adopting this license.*

---

<br>

<h2 id="中文说明">🇨🇳 中文说明</h2>

**AI-RIDER (AI 训练与模型参数强制开源附加条款)** 旨在修补传统开源协议（如 GPLv3）在 AI 时代的漏洞。

现在的 AI 巨头（如 OpenAI、Anthropic）以“合理使用”为借口，疯狂抓取开源代码进行大模型训练，然后将模型闭源牟取暴利。开发者付出了心血，却一无所获。

**AI-RIDER 的核心逻辑非常简单：**
如果你用我的代码作为语料去训练 AI 模型，并且你用这个模型去赚钱了（商业化），那么**你必须将该模型的所有参数和权重（Weights & Parameters）完全开源！** 否则，绝对禁止你抓取我的代码。

### 如何使用？
1. 将本仓库的 `AI-RIDER-v1.0.txt` 下载并放入你项目的根目录。
2. 在你的源码文件头部的 Copyright 声明下方，粘贴我们在 [Step 2](#step-2-update-your-file-headers) 中提供的全英文警告声明。
3. （可选）将红色的 AI-RIDER 徽章挂在你的 README 中，向爬虫和 AI 厂商宣示主权。

---
*License of this repository: The text of the AI-RIDER itself is released under CC0 1.0 Universal (Public Domain).*