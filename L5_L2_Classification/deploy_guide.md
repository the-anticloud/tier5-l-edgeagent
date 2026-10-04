# Deploy Guide — L_EDGEAGENT
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, llama.cpp (C extension), ONNX Runtime, Raspberry Pi/Jetson, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, llama.cpp (ARM build), ONNX Runtime 1.17+. 4GB RAM minimum (Raspberry Pi 4).

## Environment
Raspberry Pi 4 (4GB), Jetson Nano, or similar ARM/x86 edge device. No GPU required for <7B models.

## AIOSS Integration
```bash
aioss init --module L_EDGEAGENT --output ./l_edgeagent.aioss
aioss append --chain ./l_edgeagent.aioss --payload ./output.bin --module L_EDGEAGENT
aioss verify --chain ./l_edgeagent.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_EDGEAGENT",
    aioss_chain="./L_EDGEAGENT.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_EDGEAGENT.aioss --verbose
python -m L_EDGEAGENT.tests.smoke
```
