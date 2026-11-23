`cmake -S . -B build -G Ninja`

`cmake --build build && ./build/engine/linfer`

## Proposed milestones

1. Phase 1 — Basic tensor library
   
   Implement contiguous tensors, shape/stride handling, matrix multiplication, elementwise operations, softmax, and normalization.
   
   Deliverable: Small numerical tests match a PyTorch reference.
2. Phase 2 — Model loading
   
   Read .safetensors, parse configuration, map weights, and support FP32 or convert FP16/BF16 to FP32.
   
   Deliverable: Print every tensor's shape and inspect weights.
3. Phase 3 — First token
   
   Implement a specific model architecture, its tokenizer, and the full forward pass.
   
   Deliverable: Correct next-token logits and greedy token generation.
4. Phase 4 — Autoregressive generation
   
   Add the KV cache, incremental decoding, sampling, EOS stopping, and output streaming.
   
   Deliverable: Generate complete text responses.
5. Phase 5 — CPU optimization
   
   Add SIMD, parallel kernels, cache-aware memory layouts, and benchmark individual operations.
   
   Deliverable: Measure prefill throughput, tokens/sec, and peak memory.
6. Phase 6 — Advanced inference
   
   Explore quantization, GPU acceleration, batching, paged KV caches, or speculative decoding.
   
   Deliverable: A more competitive inference runtime.