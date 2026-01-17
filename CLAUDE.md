# nuLLM - Development Plan

Building a custom large language model from scratch to understand transformer architecture and modern AI.

## What We're Building
1. Neural network foundations - linear layers, activations, tokenizer (BPE)
2. Transformer architecture - multi-head attention, position encodings, FFN, layer norm, residuals
3. Training infrastructure - data loading, training loop, gradient accumulation, checkpointing
4. Optimization - mixed precision (FP16), gradient checkpointing, Flash Attention
5. Inference - sampling strategies (top-k, top-p, temperature), KV-cache, quantization

## Target: GPT-2 style decoder-only, ~100M-500M params, 512-2048 token context
## Tech: PyTorch, custom training loop, W&B tracking
