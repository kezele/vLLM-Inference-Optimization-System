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

Technologies Used
- Python
- vLLM
- Hugging Face Transformers
- CUDA GPU Acceleration
- Google Colab


Challenges Faced During API Deployment in Google Colab

While experimenting with vLLM’s API serving capabilities, several deployment limitations were encountered due to the nature of the Google Colab environment.

Key challenges included:

- Colab runtimes not handling persistent background inference servers reliably
- GPU memory conflicts when attempting to keep API servers and inference workloads active simultaneously
- Runtime interruptions and forced session resets during prolonged server execution
- Difficulties maintaining stable local API endpoints within Colab’s temporary notebook infrastructure
- Additional startup overhead caused by repeatedly initializing inference servers after runtime resets

These limitations highlighted the tradeoff between rapid prototyping environments like Colab and more production-oriented infrastructure such as dedicated GPU servers, Docker containers, or cloud-based deployments on AWS/Kubernetes.

Future Improvements 

Potential future extensions include:

- stable REST API deployment outside Colab
- larger model benchmarking
- AWS GPU deployment
