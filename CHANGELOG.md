# Changelog

All notable changes to the AI-RIDER legal text will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.0] - 2026-04-01

### Added
- Initial release of AI-RIDER v1.0 legal text (English) — the sole authoritative version
- README (English) and README-zh (Chinese documentation translation) with usage instructions, FAQ, and Single Source of Truth policy
- CONTRIBUTING.md with contribution guidelines, derivative works policy, and naming conventions
- CC0 1.0 Universal LICENSE file
- GitHub Issue templates for legal concerns and documentation fixes

### Legal Text Sections
- **Section 1: Definitions** — Six defined terms drafted in technology-neutral language:
  - 1.1 Artificial Intelligence Model (AI Model)
  - 1.2 Training Activities (pre-training, fine-tuning, RLHF, DPO, LoRA, and any functionally equivalent methodology)
  - 1.3 Knowledge Distillation (teacher-student, self-distillation, synthetic data, and any equivalent methodology)
  - 1.4 Model Parameters (architecture, weights, biases, embeddings, adapters, tokenizers, configs)
  - 1.5 Commercial Use (APIs, SaaS, PaaS, embedded systems, cost reduction, and any economic exploitation)
  - 1.6 Retrieval Use (indexing, vectorizing, embedding into retrieval systems for commercial RAG or equivalent)
- **Section 2: Trigger Conditions**
  - 2.1 Training & Distillation → triggers Section 3 obligations
  - 2.2 Retrieval Use → triggers Section 3A obligations
  - Academic research exception
- **Section 3: Mandatory Open-Source Obligations** (full disclosure, license compatibility, viral flow-through for distillation chains)
- **Section 3A: Retrieval Use — Attribution and Notice Obligations** (attribution, license notice, presentation requirements, scope)
- **Section 4: Exemptions & Dual Licensing**
- **Section 5: Breach & Termination** (automatic termination, remedial actions including eradication from retrieval systems)
- **Section 6: Severability & Legal Effect**
- **Section 7: Governing Language, Applicable Law & Dispute Resolution** (English as authoritative, copyright holder's domicile law, negotiation then arbitration/litigation)

### Design Principles
- **Technology-neutral drafting**: All definitions use "includes, but is not limited to" with catch-all clauses covering "any functionally equivalent or successor methodology, regardless of the terminology used"
- **RAG is NOT a Training Activity**: RAG and analogous retrieval mechanisms that do not modify model parameters are explicitly excluded from "Training Activities" (Section 1.2); however, commercial Retrieval Use triggers attribution obligations under Section 3A
- **Single Source of Truth**: Only the English legal text (`AI-RIDER-v1.0.txt`) is authoritative; no translations are maintained in this repository
- **Recommended base licenses**: GPLv3 or AGPLv3 (per GPLv3 Section 7 allowing additional terms)
- **SPDX identifier**: CC0-1.0 included in legal text header for automated compliance tooling
