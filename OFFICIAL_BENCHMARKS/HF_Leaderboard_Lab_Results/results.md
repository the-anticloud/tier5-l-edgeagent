# HF_Leaderboard_Lab_Results

**Project:** `L_EDGEAGENT`  
**Tier:** `TIER_5_WORLD_NEURO_EMBODIED`  
**Slug:** `huggingface/smolagents`  
**Commit:** `c30b115286e0`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **51.31 ms** |
| Min latency | 47.51 ms |
| Max latency | 53.48 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **40** |
| Tokenization latency | 3.51 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5874 |
| Classification latency | 74.52 ms |
| Status | **PASS** |

**Input text tokenized:**
```
L_EDGEAGENT (huggingface/smolagents) — 185 files, 30691 source lines, licence Apache-2.0, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'l', '_', 'edge', '##age', '##nt', '(', 'hugging', '##face', '/', 'sm', '##ola', '##gent', '##s', ')', '—', '185', 'files', ',', '306']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_