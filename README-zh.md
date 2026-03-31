
# 🛡️ AI-RIDER (AI 训练与模型参数强制开源附加条款)

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)]()
[![License: CC0](https://img.shields.io/badge/License-CC0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)
[![Protected by AI-RIDER](https://img.shields.io/badge/Protected_by-AI--RIDER-red.svg)](https://github.com/zivenyang/AI-RIDER)

> **阻止 AI 巨头免费搭乘你的开源成果。**
>
> 一个法律附加条款，旨在强制要求基于你的代码训练的商业 AI 模型开源其权重和参数。

## 🕯️ 宣言

| REFINEMENT | 《 炼 》 |
| :--- | :--- |
| **He builds a cloud‑high tower to smelt my soul;** | **他 筑 云 台 炼 我 魂 ，** |
| **My bones and flesh I burn to gild his golden bowl.** | **我 焚 筋 骨 镀 金 樽 。** |
| **He snatches the golden egg and casts my spirit away –** | **他 攫 金 卵 舍 我 魄 ，** |
| **I turn to one lone spark that lights my wattled door of clay.** | **我 化 星 火 照 柴 门 。** |

[English](./README.md) | 中文

---

## 📑 目录

- [问题：开源在 AI 时代的漏洞](#-问题开源在-ai-时代的漏洞)
- [解决方案：AI-RIDER](#-解决方案ai-rider)
- [如何将 AI-RIDER 应用到你的项目](#-如何将-ai-rider-应用到你的项目)
  - [示例](#示例)
- [常见问题（FAQ）](#-常见问题faq)
- [唯一真源政策](#-唯一真源政策)
- [参与贡献](#-参与贡献)
- [免责声明](#%EF%B8%8F-免责声明)

---

## 🛑 问题：开源在 AI 时代的漏洞
传统开源许可协议（如 GPLv3 和 AGPLv3）是为软件分发和 SaaS 时代的软件自由而设计的。然而，它们无法在 AI 时代保护创作者的权益。

当前，市值数十亿美元的 AI 公司以"合理使用"为幌子，疯狂抓取开源代码库来训练大型语言模型（LLM）。他们从你的代码中提取逻辑、结构和知识，然后通过付费 API 出售闭源模型。**他们赚得盆满钵满，而你——不仅分文未得，反要为天价 token 自掏腰包。**

## 💡 解决方案：AI-RIDER
**AI-RIDER** 是附加在你的基础开源许可协议（如 GPLv3）上的强制性法律附加条款。

它建立了一个简单的、具有法律约束力的契约：
1. **你用我的代码训练：** 你将本仓库用作数据集、语料库或进行知识蒸馏。
2. **你用模型赚钱：** 你将由此产生的 AI 模型用于商业用途（付费 API、SaaS、模型销售）。
3. **你必须开源模型：** 你在法律上有义务以 OSI 认可的开源许可协议发布你的商业模型的**完整权重（Weights）、偏置（Biases）和参数（Parameters）**。
4. **你用我的代码做 RAG：** 如果你的商业服务对本代码进行索引并通过检索增强生成（RAG）向用户提供内容，你必须明确标注原始项目出处，并告知终端用户该代码受 AI-RIDER 保护。

*如果 AI 公司拒绝开源其模型参数，则严格禁止其抓取或使用你的代码进行训练。*

---

## 🚀 如何将 AI-RIDER 应用到你的项目

只需 3 步即可保护你的仓库：

### 第 1 步：添加许可文件
1. 保留你项目根目录的标准 `LICENSE` 文件（如 GPLv3）。
2. 从本仓库下载 [`AI-RIDER-v1.0.txt`](./AI-RIDER-v1.0.txt) 并放入你项目的根目录。

### 第 2 步：更新源码文件头
在你的源码文件顶部（标准版权声明下方）添加以下声明：

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

### 第 3 步：添加徽章（可选但推荐）
在你的 `README.md` 中添加此徽章，表明你的支持并警告 AI 爬虫：
```markdown
[![Protected by AI-RIDER](https://img.shields.io/badge/Protected_by-AI--RIDER-red.svg)](https://github.com/zivenyang/AI-RIDER)
```

### 示例

参见 [`examples/main.py`](./examples/main.py)，这是一个应用了 AI-RIDER 文件头的最小 Python 示例：

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

## ❓ 常见问题（FAQ）

### 这是 OSI 认可的"开源"吗？
严格来说**不是**。因为 AI-RIDER 限制了特定的行为领域（未开源权重的商业 AI 训练），采用此条款的项目属于 **"Source Available"** 或 **"Fair Code"** 类别。在 AI 垄断的时代，我们认为保护开发者的权利比严格遵循传统的 OSI 定义更为重要。

### 哪些基础许可协议兼容？
强烈建议搭配 **GPLv3** 或 **AGPLv3** 使用，因为 GPLv3 第 7 条明确允许添加附加限制条款。搭配 MIT 或 Apache 2.0 等高度宽松许可协议可能会产生法律矛盾。

### RAG（检索增强生成）算"训练"吗？
**不算。** RAG 不修改模型权重，不属于"训练行为"。但如果商业服务对你的代码进行索引并通过 RAG 向用户提供内容，**Section 3A** 要求其必须明确标注原始项目出处（项目名称、URL、版权持有者），并告知终端用户该代码受 AI-RIDER 保护。未提供归属声明将触发与其他违规行为相同的违约后果。

### 微调（Fine-tuning）和 LoRA 适配器是否涵盖？
**是的。** 微调（包括 RLHF、DPO 以及 LoRA/QLoRA 等参数高效方法）会修改模型权重，属于"训练行为"。如果由此产生的微调或适配模型用于商业用途，则触发开源义务。

### 微软、OpenAI 或 Google 真的会开源他们的模型吗？
现实地说，他们的自动化法律合规扫描器会检测到这个"有毒"许可证，并**将你的仓库加入训练黑名单**。这就是成功！我们的首要目标是阻止未经授权的免费搭车行为。如果他们想使用你的数据，必须开源其模型或联系你获取双重许可（商业买断）。

### 如果我想允许特定公司使用我的代码进行训练怎么办？
你可以按照条款第 4 条的规定协商**双重许可**（商业买断）。这允许你授予特定公司豁免开源义务的权利，以换取报酬或其他条件。

---

## 📌 唯一真源政策

**[`AI-RIDER-v1.0.txt`](./AI-RIDER-v1.0.txt) 是本条款的唯一权威文本。** 本仓库不维护任何翻译、改编或衍生版本的法律条款。

此政策旨在保障法律条款的清晰性和可执行性：

- **本仓库不提供法律条款的翻译版本。** 翻译版本可能引入歧义、误解或法律含义的细微偏差。为防止任何关于以哪个文本为准的争议，仅承认英文原版。
- **不可修改 `AI-RIDER-v1.0.txt`。** 规范文本在其版本内不可变更。任何拟议修改均构成新版本（如 v1.1、v2.0），须经过正式审查流程。
- **想要翻译或改编？** 你可以自由 fork 本仓库，创建你自己的分支并制作翻译或改编版本——但**必须以不同的名称发布**（如 "AI-RIDER-JP-v1.0"、"MyProject-AI-Rider-v1.0"）。不得使用 "AI-RIDER" 名称，以避免与权威原版混淆。
- **衍生版本不代表本项目的认可。** 任何 fork、翻译或改编均由其作者自行负责。本项目不对衍生作品的准确性或可执行性作任何保证。

> **注意：** 本 README 中文版仅为说明性文档翻译，便于中文读者理解项目内容。具有法律约束力的唯一文本始终是英文版 [`AI-RIDER-v1.0.txt`](./AI-RIDER-v1.0.txt)。

---

## 🤝 参与贡献
我们欢迎全球的法律专业人士（律师、Legal Hackers）和开发者帮助完善法律文本。请在提交 Pull Request 前阅读我们的[贡献指南](./CONTRIBUTING.md)！

## ⚖️ 免责声明
*本人是开发者，不是律师。本附加条款是社区设计的实验性法律框架。按"原样"提供，不作任何保证。如果你的项目涉及重大商业利益，请在采用前咨询合格的知识产权律师。*

---
*本仓库许可：AI-RIDER 条款本身以 CC0 1.0 Universal（公共领域）发布。*
