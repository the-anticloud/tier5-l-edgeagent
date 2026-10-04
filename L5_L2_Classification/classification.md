# L5 Narrow / L2 General Classification — L_EDGEAGENT
**Platform:** Anticloud | **Tier:** TIER_5_WORLD_NEURO_EMBODIED | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
L_EDGEAGENT is an ultra-lightweight inference agent for edge hardware: Raspberry Pi, Jetson Nano, embedded ARM. Narrow scope: quantized 1.5B-7B models (not full PAX 27B) for edge IoT tasks. PAX 27B runs on the central server; L_EDGEAGENT handles local inference.

## L2 General
L2 General: L_EDGEAGENT extends Anticloud to edge hardware. TIER_9 IoT sensors and TIER_8 mesh radio nodes both run L_EDGEAGENT for local inference without needing PAX 27B's full resources.

## PAX 27B Integration
PAX 27B on the server supervises L_EDGEAGENT models: periodically evaluating edge agent decisions and sending correction signals for continuous edge model improvement.

## AIOSS Audit Chain
Every edge inference (model hash + input hash + output hash + device ID + latency_ms) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
IEC 62443-4-2 (IoT component security). IEC 61508 (safety in embedded systems).
