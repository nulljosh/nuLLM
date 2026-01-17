# nuLLM

A custom Large Language Model built from scratch to understand transformer architecture and modern AI systems.

## Project Goals

- Understand transformer architecture from first principles
- Implement attention mechanisms, tokenization, and training loops
- Train a small but functional language model
- Learn about optimization, distributed training, and inference

## Development Phases

### Phase 1: Foundations
- [ ] Implement basic neural network components (linear layers, activations)
- [ ] Build tokenizer (BPE or WordPiece)
- [ ] Data preprocessing pipeline

### Phase 2: Transformer Architecture
- [ ] Multi-head self-attention mechanism
- [ ] Position encodings (absolute or rotary)
- [ ] Feed-forward networks
- [ ] Layer normalization
- [ ] Residual connections

### Phase 3: Training Infrastructure
- [ ] Dataset loading and batching
- [ ] Training loop with gradient accumulation
- [ ] Learning rate scheduling
- [ ] Checkpointing and model saving
- [ ] Loss functions and metrics

### Phase 4: Optimization
- [ ] Mixed precision training (FP16/BF16)
- [ ] Gradient checkpointing
- [ ] Flash Attention
- [ ] Model parallelism (optional)

### Phase 5: Inference & Deployment
- [ ] Sampling strategies (greedy, top-k, top-p, temperature)
- [ ] KV-cache optimization
- [ ] Model quantization
- [ ] ONNX/TensorRT export

## Tech Stack

- **Framework**: PyTorch (or JAX for learning purposes)
- **Training**: Hugging Face Transformers (for reference), Weights & Biases
- **Data**: OpenWebText, The Pile, or custom datasets
- **Compute**: Local GPU or cloud (Lambda Labs, RunPod)

## Architecture Decisions

- Start with GPT-2 style decoder-only architecture
- Scale: ~100M-500M parameters for feasibility
- Context length: 512-2048 tokens
- Vocabulary size: ~50k tokens

## Resources

- [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)
- [nanoGPT by Karpathy](https://github.com/karpathy/nanoGPT)
- [minGPT by Karpathy](https://github.com/karpathy/minGPT)
- [Build GPT from Scratch](https://www.youtube.com/watch?v=kCc8FmEb1nY)

## Setup

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install torch transformers datasets tiktoken wandb

# Prepare data
python data/prepare.py

# Train model
python train.py --config configs/small.yaml

# Generate text
python generate.py --checkpoint checkpoints/model.pt --prompt "Once upon a time"
```

## License

MIT
