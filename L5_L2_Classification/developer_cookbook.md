# Developer Cookbook — L_EDGEAGENT
**Stack:** Python 3.11, llama.cpp (C extension), ONNX Runtime, Raspberry Pi/Jetson, AIOSS_FORMAT
**Domain:** EdgeAgent: ultra-lightweight PAX-compatible inference agent for edge/IoT hardware

## Edge inference
```python
from l_edgeagent import EdgeAgent

agent = EdgeAgent(
    model="./raven-draft-1.5b-q4.gguf",  # small model for edge
    max_tokens=64,
    aioss_chain="./edge_agent.aioss"
)

# Classify sensor reading
result = agent.classify(
    input_data=sensor_reading,
    task="Is this temperature reading anomalous?",
    schema={"anomalous": "bool", "severity": "low|medium|high"}
)
print(f"Anomalous: {result.anomalous}, Severity: {result.severity}")
print(f"Latency: {result.latency_ms:.0f}ms")
```

## Report to PAX 27B server (LAN)
```python
agent.report_to_server(
    server_url="http://192.168.1.100:8080",
    report_interval_s=60
)
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
