# Realtime Live Insights Latency Report

## Benchmark Summary
- **Runs Executed**: 100 calls
- **Chunks Processed**: 100
- **P50 Latency**: 9.25 ms
- **P95 Latency**: 9.25 ms
- **Mean Latency**: 6.04 ms

## Component Breakdown (Per Chunk)
1. **Simulated ASR Ingestion**: ~4.0 ms (`time.sleep(0.004)`)
2. **Signal Detection / Rule Evaluation**: < 1.0 ms (`llm_ms` in code)
3. **Simulated Delivery Delay**: ~1.0 ms (`time.sleep(0.001)`)
4. **Total Per-Chunk Latency**: ~5.0 - 7.5 ms

## Simulation Disclosure
> [!IMPORTANT]
> The latency figures reported here represent the execution of the existing **simulation pipeline** (`realtime_analytics/src/pipeline.py`). The pipeline uses fixed micro-delays (`time.sleep`) to mimic real-time ASR streaming and UI nudge delivery without calling remote LLM endpoints.
