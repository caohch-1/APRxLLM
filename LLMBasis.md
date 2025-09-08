# Basic knowledge of LLM
## Phase 1: Code-Centric LLMs

### Code-specific Pretraining
Paper(s): CodeBERT, GraphCodeBERT, CodeT5, PolyCoder, StarCoder, Code Llama, DeepSeek-Coder  
Tool(s): Code LLMs (StarCoder, CodeLlama, DeepSeek-Coder), vLLM, TGI  
Main Purpose: Learn the landscape of code-focused LLMs and their strengths.

### Code Benchmarks
Paper(s): HumanEval, MBPP, CodeXGLUE, MULTI-PL-Bench  
Tool(s): OpenAI Evals, Hugging Face Evals, Docker sandbox  
Main Purpose: Learn how to evaluate code LLMs and repair tasks rigorously.

### Semantic & Structural Representations
Paper(s): code2vec, code2seq, Deep Graph Learning for Code  
Tool(s): tree-sitter, GumTree, srcML, Joern, Soot  
Main Purpose: Build structured representations (AST, CFG, PDG) to guide patch generation.

---

## Phase 2: Transformers & Pretraining

### Transformer Architecture
Paper(s): Attention Is All You Need  
Tool(s): Hugging Face Transformers, PyTorch  
Main Purpose: Master self-attention, positional encoding, encoder-decoder design.

### Pretraining Paradigms
Paper(s): BERT, GPT-3, T5  
Tool(s): Hugging Face Datasets, Tokenizers  
Main Purpose: Learn masked language modeling, causal language modeling, and sequence-to-sequence objectives.

### Scaling Laws & Efficient Training
Paper(s): Scaling Laws for Neural Language Models  
Tool(s): DeepSpeed, Megatron-LM  
Main Purpose: Understand how data, model size, and compute interplay.

---

## Phase 3: Post-training & Alignment

### Supervised Fine-tuning (SFT)
Paper(s): Instruction Tuning, FLAN  
Tool(s): Hugging Face PEFT, LoRA, QLoRA  
Main Purpose: Make pretrained LLMs follow instructions by supervised fine-tuning.

### Reinforcement Learning from Human Feedback (RLHF)
Paper(s): InstructGPT  
Tool(s): TRL (HF), PPO implementations  
Main Purpose: Learn preference modeling, reward models, and fine-tuning with human feedback.

### Direct Preference Optimization (DPO)
Paper(s): Direct Preference Optimization  
Tool(s): TRL DPO pipeline  
Main Purpose: Simplify preference alignment without reinforcement learning.

---

## Phase 4: Advanced Reasoning & Prompting

### Prompt Engineering
Paper(s): Language Models are Few-Shot Learners (GPT-3)  
Tool(s): OpenAI API, Guidance, LangChain  
Main Purpose: Learn zero-shot, few-shot, and chain-of-thought prompting.

### Chain-of-Thought & Self-Consistency
Paper(s): Chain-of-Thought Prompting, Self-Consistency Improves Reasoning  
Tool(s): LangChain agents, custom prompting scripts  
Main Purpose: Boost reasoning quality through intermediate steps and sampling.

### Tree-of-Thoughts & Self-Refinement
Paper(s): Tree of Thoughts, Reflexion  
Tool(s): LangGraph, AutoGen  
Main Purpose: Learn structured multi-step reasoning and self-reflective correction.

---

## Phase 5: Retrieval & Knowledge Integration

### Retrieval-Augmented Generation (RAG)
Paper(s): REALM, RAG  
Tool(s): FAISS, Chroma, LangChain RAG  
Main Purpose: Enhance LLMs with external knowledge bases.

### Tool-Augmented LLMs / Agents
Paper(s): Toolformer, AutoGPT, SWE-Agent  
Tool(s): LangGraph, AutoGen, OpenAI Function Calling  
Main Purpose: Enable LLMs to call APIs, search, and use external reasoning tools.

---

## Phase 6: Efficiency & Scaling

### Parameter-efficient Fine-tuning
Paper(s): LoRA, QLoRA  
Tool(s): PEFT (HF), bitsandbytes  
Main Purpose: Adapt large models to new tasks with limited compute.

### Efficient Inference
Paper(s): PagedAttention / vLLM, Speculative Decoding  
Tool(s): vLLM, TensorRT-LLM, GPTQ, AWQ  
Main Purpose: Reduce latency/cost when running LLMs at scale.

### Distillation & Smaller Models
Paper(s): DistilBERT, Alpaca, TinyLlama  
Tool(s): Hugging Face Distillation pipelines  
Main Purpose: Compress LLMs while keeping strong performance.

---

## Phase 7: Multimodality & Extensions

### Multimodal LLMs
Paper(s): CLIP, BLIP-2, LLaVA  
Tool(s): OpenCLIP, LLaVA, Hugging Face multimodal repos  
Main Purpose: Understand how LLMs integrate images, text, and other modalities.

### Code-specific LLMs (Specialization)
Paper(s): CodeBERT, CodeT5, StarCoder, Code Llama  
Tool(s): Hugging Face Code Models, DeepSeek-Coder  
Main Purpose: Learn differences between natural language and code-oriented LLM pretraining.

---

## Phase 8: Evaluation, Interpretability, and Ethics

### Evaluation Metrics
Paper(s): HELM, BIG-bench  
Tool(s): lm-eval-harness, HELM  
Main Purpose: Learn systematic benchmarking of LLM capabilities.

### Interpretability & Safety
Paper(s): Attention Is Not Explanation, Explaining LLMs survey  
Tool(s): Captum, SHAP, LIME  
Main Purpose: Develop methods to interpret model reasoning and ensure safe usage.

### Ethics & Responsible AI
Paper(s): Stochastic Parrots, Responsible AI Guidelines  
Tool(s): Data filtering pipelines, scancode for license scanning  
Main Purpose: Understand risks, bias, and compliance issues.

---

## Phase 9: Hands-on Mastery

### Build & Fine-tune a Small LLM
Tool(s): Hugging Face Transformers, PEFT, LoRA  
Main Purpose: Train on a small dataset to internalize the end-to-end workflow.

### Deploy & Optimize LLMs
Tool(s): vLLM, TGI, Docker, Kubernetes  
Main Purpose: Run and serve models efficiently in real-world environments.
