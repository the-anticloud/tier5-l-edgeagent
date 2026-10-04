# Radon_Complexity_Lab_Results
**Project:** `L_EDGEAGENT` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'A', 'score': 2.4705882352941178}`
- **complexity_grade:** `A`
- **complexity_score:** `2.4705882352941178`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_EDGEAGENT\UPSTREAM\examples\agent_from_any_llm.py - A (86`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_EDGEAGENT\UPSTREAM\examples\agent_from_any_llm.py
    F 43:0 get_weather - A (1)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_EDGEAGENT\UPSTREAM\examples\multiple_tools.py
    F 16:0 get_weather - A (5)
    F 119:0 get_joke - A (5)
    F 88:0 get_news_headlines - A (4)
    F 52:0 convert_currency - A (3)
    F 148:0 get_time_in_timezone - A (2)
    F 174:0 get_random_fact - A (2)
    F 195:0 search_wikipedia - A (2)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_EDGEAGENT\UPSTREAM\examples\rag.py
    C 29:0 RetrieverTool - A (3)
    M 44:4 RetrieverTool.forward - A (3)
    M 40:4 RetrieverTool.__init__ - A (1)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_EDGEAGENT\UPSTREAM\examples\rag_using_chromadb.py
    C 71:0 RetrieverTool - A (3)
    M 88:4 RetrieverTool.forward - A (3)
    M 84:4 RetrieverTool.__init__ - A (1)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_EDGEAGENT\UPSTREAM\examples\structured_output_tool.py
    F 22:0 weather_server_script - A (1)
    F 55:0 main - A (1)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_EDGEAGENT\UPSTREAM\examples\text_to_sql.py
    F 51:0 sql_engine - A (2)

17 blocks (classes, functions, methods) analyzed.
Average complexity: A (2.4705882352941178)
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_