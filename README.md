# Dataset and Experimental Results
## Evaluating the Contributions of RAG, Prompt-based MoE, and Chain-of-Thought in a Sequential LLM-based Pipeline for Indonesian Elementary School Mathematics Question Generation

**Author:** Diana Febrina Lumbantoruan  
**Institution:** Universitas Sumatera Utara, Master's Program in Informatics Engineering  
**Contact:** febrinalt123@gmail.com

---

## Overview

This dataset contains generated question outputs and DeepEval evaluation results from a systematic ablation study across eight pipeline configurations (C0–C7), along with extended baseline comparisons with Qwen2.5-7B-INT4 and GPT-4o-mini.

**Base model:** Qwen2.5-3B-Instruct (no fine-tuning)  
**Evaluation framework:** DeepEval (GPT-4o-mini as judge)  
**Total questions:** 400 (50 × 8 configurations) + 100 (extended baseline)

---

## Folder Structure

```
dataset-pipeline-math-sd/
├── 01_knowledge_base/
│   └── [Indonesian SD mathematics textbooks - PDF]
│
├── 02_ablation_study_C0-C7/
│   ├── c0_output.csv
│   ├── c1_output.csv
│   ├── c2_output.csv
│   ├── c3_output.csv
│   ├── c4_output.csv
│   ├── c5_output.csv
│   ├── c6_output.csv
│   ├── c7_output.csv
│   └── deepeval_all.csv
│
├── 03_extended_baseline/
│   ├── qwen7b_output.csv
│   ├── gpt4omini_output.csv
│   ├── deepeval_extended.csv
│   └── comparison_full.csv
│
└── README.md
```

---

## Key Results

| Config | de_overall |
|--------|------------|
| C0 (3B, no pipeline) | 0.5886 |
| C1 (3B + RAG) | 0.8151 |
| C2 (3B + MoE) | 0.5923 |
| C3 (3B + CoT) | 0.5931 |
| C4 (3B + RAG + MoE) | 0.8340 |
| C5 (3B + RAG + CoT) | 0.7737 |
| C6 (3B + MoE + CoT) | 0.5864 |
| C7 (3B, full pipeline) | 0.7893 |
| Qwen2.5-7B-INT4 (no pipeline) | 0.5534 |
| GPT-4o-mini (no pipeline) | 0.6293 |

---

## License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)

---

## Citation

> Paper currently under review. Citation will be updated upon publication.
