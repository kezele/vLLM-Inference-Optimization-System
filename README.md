# vLLM-Inference-Optimization-System
This project explores LLM inference optimization using vLLM, focusing on latency, throughput, batching behavior, GPU memory usage, and generation parameter tuning. The goal is to understand how inference systems scale under different workloads and how serving configurations affect real-time text generation performance.

Optimization Focus

The project evaluates how different inference settings affect performance, including:

- batch size / number of prompts
- max token generation length
- latency
- throughput
- GPU memory usage
- Key Experiments

Baseline Inference
Ran a small open-source model through vLLM to establish baseline generation performance.

Batch Scaling
Tested different prompt batch sizes to observe how larger workloads affect latency and throughput.

Max Token Tuning
Adjusted max_tokens to analyze how response length impacts latency, compute workload, and output completeness.

API Serving Exploration
Explored vLLM’s OpenAI-compatible API serving architecture for real-time text generation.

Metrics Tracked
- latency
- tokens/sec throughput
- generated token count
- GPU memory usage
- batch size
- max tokens
- Technologies Used
- Python
- vLLM
- Hugging Face Transformers
- CUDA GPU Acceleration
- Google Colab
- Future Improvements

Potential future extensions include:

- stable REST API deployment outside Colab
- larger model benchmarking
- AWS GPU deployment
