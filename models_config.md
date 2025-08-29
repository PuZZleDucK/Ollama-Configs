
[x] # command-r7b:7b
- Slug: `config-command-r7b-7b`
- Author: Cohere
- max_new_tokens: 100
- temperature: 0.3
- do_sample: true
- stop: ["<|START_OF_TURN_TOKEN|>", "<|END_OF_TURN_TOKEN|>", "<|END_RESPONSE|>"]
- context_length: 128k
  - Optional: top_k=40, top_p=0.95, min_p=0.05, typical_p=1.0, temperature=0.0

[x] # command-r7b:7b-12-2024-fp16
- Slug: `config-command-r7b-7b-12-2024-fp16`
- Author: Cohere
- temperature: 0.3
- stop: ["<|START_OF_TURN_TOKEN|>", "<|END_OF_TURN_TOKEN|>", "<|END_RESPONSE|>"]
- context_length: 128k
  - Optional: top_k=40, top_p=0.95, min_p=0.05, typical_p=1.0, temperature=0.0

[x] # deepcoder:14b
- Slug: `config-deepcoder-14b`
- Author: Agentica
- temperature: 0.6
- top_p: 0.95
- max_tokens: 64000
- avoid_system_prompt: true
- context_length: 32k
  - Optional: top_k=50, temperature=0.2, repetition_penalty=1.03, max_new_tokens=256, stop=["\nUser:", "<|endoftext|>", "</s>"]

[x] # deepcoder:1.5b
- Slug: `config-deepcoder-1-5b`
- Author: Agentica
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=50, repetition_penalty=1.03, max_new_tokens=256

[x] # deepseek-r1:1.5b
- Slug: `config-deepseek-r1-1-5b`
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[x] # deepseek-r1:7b
- Slug: `config-deepseek-r1-7b`
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[x] # deepseek-r1:8b
- Slug: `config-deepseek-r1-8b`
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[x] # deepseek-r1:14b
- Slug: `config-deepseek-r1-14b`
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[x] # deepseek-r1:32b
- Slug: `config-deepseek-r1-32b`
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[-] # deepseek-r1-distill-qwen-1.5b - hallucinated?
- Slug: `config-deepseek-r1-distill-qwen-1-5b`
- Author: DeepSeek AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[-] # deepseek-r1-distill-qwen-7b
- Slug: `config-deepseek-r1-distill-qwen-7b`
- Author: DeepSeek AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[-] # deepseek-r1-distill-qwen-14b
- Slug: `config-deepseek-r1-distill-qwen-14b`
- Author: DeepSeek AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[-] # deepseek-r1-distill-qwen-32b
- Slug: `config-deepseek-r1-distill-qwen-32b`
- Author: DeepSeek AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:0.5b
- Slug: `config-qwen2-5-0-5b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:1.5b
- Slug: `config-qwen2-5-1-5b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:3b - NEW - added by agent?
- Slug: `config-qwen2-5-3b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:7b
- Slug: `config-qwen2-5-7b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:14b
- Slug: `config-qwen2-5-14b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:32b
- Slug: `config-qwen2-5-32b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:0.5b
- Slug: `config-qwen2-5-coder-0-5b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:1.5b
- Slug: `config-qwen2-5-coder-1-5b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:3b
- Slug: `config-qwen2-5-coder-3b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:7b
- Slug: `config-qwen2-5-coder-7b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:14b
- Slug: `config-qwen2-5-coder-14b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:32b
- Slug: `config-qwen2-5-coder-32b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5vl:3b - ERROR
- Slug: `config-qwen2-5vl-3b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5vl:7b
- Slug: `config-qwen2-5vl-7b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5vl:32b
- Slug: `config-qwen2-5vl-32b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen3:0.6b
- Slug: `config-qwen3-0-6b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:1.7b
- Slug: `config-qwen3-1-7b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:4b
- Slug: `config-qwen3-4b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:8b
- Slug: `config-qwen3-8b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:14b
- Slug: `config-qwen3-14b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:32b
- Slug: `config-qwen3-32b`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

# qwen3:latest - used? - which one?
- Slug: `config-qwen3-latest`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwq:latest
- Slug: `config-qwq-latest`
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.85
- context_length: 32k
  - Optional: None specified by community

[x] # smollm:135m
- Slug: `config-smollm-135m`
- Author: Hugging Face Smol Models Team
- temperature: 0.6
- top_p: 0.9
- max_new_tokens: 512
  - Optional: None specified by community

[x] # smollm:360m
- Slug: `config-smollm-360m`
- Author: Hugging Face Smol Models Team
- temperature: 0.6
- top_p: 0.9
- max_new_tokens: 512
  - Optional: None specified by community

[x] # smollm:1.7b
- Slug: `config-smollm-1-7b`
- Author: Hugging Face Smol Models Team
- temperature: 0.6
- top_p: 0.9
- max_new_tokens: 512
  - Optional: None specified by community

[x] # wizard-vicuna-uncensored:7b - not there
- Slug: `config-wizard-vicuna-uncensored-7b`
- Author: Eric Hartford & TheBloke
- temperature: 0.7
- top_p: 0.9
- context_length: 2k
- memory_requirement: ≥8GB
  - Optional: None specified by community

[x] # wizard-vicuna-uncensored:13b
- Slug: `config-wizard-vicuna-uncensored-13b`
- Author: Eric Hartford & TheBloke
- temperature: 0.7
- top_p: 0.9
- context_length: 2k
- memory_requirement: ≥16GB
  - Optional: None specified by community

[x] # wizard-vicuna-uncensored:30b
- Slug: `config-wizard-vicuna-uncensored-30b`
- Author: Eric Hartford & TheBloke
- temperature: 0.7
- top_p: 0.9
- context_length: 2k
- memory_requirement: ≥32GB
  - Optional: None specified by community


[x] # eris_primev3-vision-7b-gguf - not there
- Slug: `config-eris_primev3-vision-7b-gguf`
- Author: Lewdiculous
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 512
  - Optional: top_p=1, top_k=0, top_a=0, tfs=1, epsilon_cutoff=0, eta_cutoff=0, typical_p=1, min_p=0.1, repetition_penalty=1

[x] # exaone-deep:2.4b
- Slug: `config-exaone-deep-2-4b`
- Author: NAVER
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # exaone-deep:7.8b
- Slug: `config-exaone-deep-7-8b`
- Author: NAVER
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # exaone-deep:32b
- Slug: `config-exaone-deep-32b`
- Author: NAVER
- temperature: 0.6
- top_p: 0.95
- context_length: 128k
  - Optional: None specified by community

[x] # falcon3:7b
- Slug: `config-falcon3-7b`
- Author: Technology Innovation Institute (TII)
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: None specified by community

[x] # falcon3:10b
- Slug: `config-falcon3-10b`
- Author: Technology Innovation Institute (TII)
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: None specified by community

[x] # gemma3:1b
- Slug: `config-gemma3-1b`
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
- context_length: 32k
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3:4b
- Slug: `config-gemma3-4b`
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
- context_length: 128k
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3:12b
- Slug: `config-gemma3-12b`
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
- context_length: 128k
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3:27b
- Slug: `config-gemma3-27b`
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
- context_length: 128k
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3n:e2b
- Slug: `config-gemma3n-e2b`
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3n:e4b
- Slug: `config-gemma3n-e4b`
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[-] # gemma-the-writer-n-restless-quill-10b-uncensored-gguf-q8_0
- Slug: `config-gemma-the-writer-n-restless-quill-10b-uncensored-gguf-q8_0`
- Author: Bartowski
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[-] # hf.co/bartowski/phi-3.5-mini-instruct_uncensored-gguf:f16
- Slug: `config-hf-co-bartowski-phi-3-5-mini-instruct_uncensored-gguf-f16`
- Author: Bartowski
- temperature: 0.7
- top_p: 0.9
- repetition_penalty: 1.05
- max_new_tokens: 1024
  - Optional: None specified by community

[x] # hf.co/davidau/gemma-the-writer-n-restless-quill-10b-uncensored-gguf:q8_0
- Slug: `config-hf-co-davidau-gemma-the-writer-n-restless-quill-10b-uncensored-gguf-q8_0`
- Author: DavidAU
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # hf.co/davidau/l3.2-rogue-creative-instruct-uncensored-abliterated-7b-gguf:q8_0
- Slug: `config-hf-co-davidau-l3-2-rogue-creative-instruct-uncensored-abliterated-7b-gguf-q8_0`
- Author: DavidAU
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # hf.co/davidau/llama-3.2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18.4b-gguf:q2_k
- Slug: `config-hf-co-davidau-llama-3-2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18-4b-gguf-q2_k`
- Author: DavidAU
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # hf.co/davidau/llama-3.2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18.4b-gguf:q6_k
- Slug: `config-hf-co-davidau-llama-3-2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18-4b-gguf-q6_k`
- Author: DavidAU
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # hf.co/davidau/llama-3.2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18.4b-gguf:q8_0
- Slug: `config-hf-co-davidau-llama-3-2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18-4b-gguf-q8_0`
- Author: DavidAU
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # hf.co/devsdocode/llama-3-8b-uncensored-q4_k_m-gguf:q4_k_m
- Slug: `config-hf-co-devsdocode-llama-3-8b-uncensored-q4_k_m-gguf-q4_k_m`
- Author: DevsDoCode
- temperature: 0.6
- top_p: 0.9
  - Optional: None specified by community

[x] # hf.co/lewdiculous/eris_primev3-vision-7b-gguf-iq-imatrix:latest
- Slug: `config-hf-co-lewdiculous-eris_primev3-vision-7b-gguf-iq-imatrix-latest`
- Author: Lewdiculous
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 512
  - Optional: top_p=1, top_k=0, top_a=0, tfs=1, epsilon_cutoff=0, eta_cutoff=0, typical_p=1, min_p=0.1, repetition_penalty=1

[x] # hf.co/mlabonne/daredevil-8b-abliterated-gguf:latest
- Slug: `config-hf-co-mlabonne-daredevil-8b-abliterated-gguf-latest`
- Author: MLabonne
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # hf.co/mlabonne/gemma-3-27b-it-abliterated-gguf:q4_k_m
- Slug: `config-hf-co-mlabonne-gemma-3-27b-it-abliterated-gguf-q4_k_m`
- Author: MLabonne
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # hf.co/mradermacher/deepseek-r1-distill-qwen-32b-uncensored-gguf:q4_k_m
- Slug: `config-hf-co-mradermacher-deepseek-r1-distill-qwen-32b-uncensored-gguf-q4_k_m`
- Author: Mradermacher
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # hf.co/mradermacher/deepseek-r1-distill-qwen-32b-uncensored-gguf:q8_0
- Slug: `config-hf-co-mradermacher-deepseek-r1-distill-qwen-32b-uncensored-gguf-q8_0`
- Author: Mradermacher
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # hf.co/mradermacher/josiefied-deepseek-r1-0528-qwen3-8b-abliterated-v1-gguf:q8_0
- Slug: `config-hf-co-mradermacher-josiefied-deepseek-r1-0528-qwen3-8b-abliterated-v1-gguf-q8_0`
- Author: Mradermacher
- temperature: 0.6
- top_p: 0.95
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # hf.co/mradermacher/magistral-small-2506-abliterated-i1-gguf:q2_k
- Slug: `config-hf-co-mradermacher-magistral-small-2506-abliterated-i1-gguf-q2_k`
- Author: Mradermacher
- temperature: 0.7
- top_p: 0.9
- context_length: 32k
  - Optional: top_p=0.95, temperature=0.7, max_tokens=40960

[x] # hf.co/mradermacher/nyan_chaos-vision-7b-gguf:q8_0
- Slug: `config-hf-co-mradermacher-nyan_chaos-vision-7b-gguf-q8_0`
- Author: Mradermacher
- temperature: 0.7
- top_p: 0.9
- context_length: 32k
  - Optional: None specified by community

[x] # hf.co/mungert/josiefied-qwen3-8b-abliterated-v1-gguf:latest
- Slug: `config-hf-co-mungert-josiefied-qwen3-8b-abliterated-v1-gguf-latest`
- Author: Mungert
- temperature: 0.7
- top_p: 0.9
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # hf.co/orenguteng/llama-3.1-8b-lexi-uncensored-v2-gguf:latest
- Slug: `config-hf-co-orenguteng-llama-3-1-8b-lexi-uncensored-v2-gguf-latest`
- Author: Orenguteng
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # hf.co/thebloke/wizard-vicuna-13b-uncensored-gguf:q4_k_m
- Slug: `config-hf-co-thebloke-wizard-vicuna-13b-uncensored-gguf-q4_k_m`
- Author: TheBloke
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # hf.co/thebloke/wizard-vicuna-13b-uncensored-gguf:q8_0
- Slug: `config-hf-co-thebloke-wizard-vicuna-13b-uncensored-gguf-q8_0`
- Author: TheBloke
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # llama3.2-vision:11b
- Slug: `config-llama3-2-vision-11b`
- Author: Meta
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # llama3.3:70b
- Slug: `config-llama3-3-70b`
- Author: Meta
- temperature: 0.6
- top_p: 0.95
- max_new_tokens: 32768
  - Optional: None specified by community

[x] # llava:7b
- Slug: `config-llava-7b`
- Author: LLaVA Team
- temperature: 0.7
- top_p: 0.9
- context_length: 8k
  - Optional: None specified by community

[x] # llava:13b
- Slug: `config-llava-13b`
- Author: LLaVA Team
- temperature: 0.7
- top_p: 0.9
- context_length: 8k
  - Optional: None specified by community

[x] # llava:34b
- Slug: `config-llava-34b`
- Author: LLaVA Team
- temperature: 0.7
- top_p: 0.9
- context_length: 8k
  - Optional: None specified by community

[x] # magistral:24b
- Slug: `config-magistral-24b`
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.9
- context_length: 32k
  - Optional: top_p=0.95, temperature=0.7, max_tokens=40960

[x] # minicpm-v:latest
- Slug: `config-minicpm-v-latest`
- Author: OpenBMB
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 512
  - Optional: None specified by community

[x] # mistral-small3.1:24b
- Slug: `config-mistral-small3-1-24b`
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: temperature=0.15

[x] # mistral-small3.2:24b
- Slug: `config-mistral-small3-2-24b`
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: temperature=0.15

[-] # mistral-small3.2:latest - dupe
- Slug: `config-mistral-small3-2-latest`
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: temperature=0.15

[-] # nyan_chaos-vision-7b-gguf:q8_0 - dupe
- Slug: `config-nyan_chaos-vision-7b-gguf-q8_0`
- Author: Mradermacher
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # opencoder:1.5b
- Slug: `config-opencoder-1-5b`
- Author: OpenCoder Team
- temperature: 0.7
- top_p: 0.95
- context_length: 32k
  - Optional: None specified by community

[x] # opencoder:8b
- Slug: `config-opencoder-8b`
- Author: OpenCoder Team
- temperature: 0.7
- top_p: 0.95
- context_length: 32k
  - Optional: None specified by community

[x] # phi4-mini-reasoning:3.8b
- Slug: `config-phi4-mini-reasoning-3-8b`
- Author: Microsoft Research
- temperature: 0.8
- top_p: 0.95
- do_sample: true
- max_new_tokens: 4096
  - Optional: top_k=50

[x] # phi4-reasoning:plus
- Slug: `config-phi4-reasoning-plus`
- Author: Microsoft Research
- temperature: 0.8
- top_p: 0.95
- do_sample: true
- max_new_tokens: 4096
  - Optional: top_k=50

[x] # yi-coder:1.5b
- Slug: `config-yi-coder-1-5b`
- Author: 01.AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: None specified by community

[x] # yi-coder:9b
- Slug: `config-yi-coder-9b`
- Author: 01.AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: None specified by community

[x] # devstral:24b
- Slug: `config-devstral-24b`
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.95
- max_tokens: 40960
- context_length: 40k
  - Optional: top_k=64, min_p=0.01, repetition_penalty=1.0

[-] # devstral:latest - dupe
- Slug: `config-devstral-latest`
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.95
- max_tokens: 40960
- context_length: 40k
  - Optional: top_k=64, min_p=0.01, repetition_penalty=1.0

[x] # dolphin3:8b
- Slug: `config-dolphin3-8b`
- Author: Eric Hartford
- temperature: 0.6
- top_p: 0.9
- do_sample: true
- context_length: 8k
  - Optional: None specified by community

[x] # granite3.2-vision:2b
- Slug: `config-granite3-2-vision-2b`
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3.3:2b
- Slug: `config-granite3-3-2b`
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3.3:8b
- Slug: `config-granite3-3-8b`
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3-dense:2b
- Slug: `config-granite3-dense-2b`
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3-dense:8b
- Slug: `config-granite3-dense-8b`
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3-moe:1b
- Slug: `config-granite3-moe-1b`
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3-moe:3b
- Slug: `config-granite3-moe-3b`
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # hermes3:3b
- Slug: `config-hermes3-3b`
- Author: Nous Research
- temperature: 0.6
- top_p: 0.9
- do_sample: true
- context_length: 8k
  - Optional: top_k=50, repetition_penalty=1.1, temperature=0.8

[x] # hermes3:8b
- Slug: `config-hermes3-8b`
- Author: Nous Research
- temperature: 0.8
- top_p: 0.9
- repetition_penalty: 1.1
- do_sample: true
- max_new_tokens: 2500
- context_length: 8k
  - Optional: top_k=50



# todo
[-] Phi-4-flash
[x] qwen3-update
[x] qwen3-coder
[-] qwen3-think

https://allenai.org/olmo
instruct
evaluated them on the Tülu 3 evaluation suite implemented in OLMES, which consists of benchmarks assessing models’ instruction-following, knowledge recall, and math and general reasoning
[x] olmo2:7b
[x] olmo2:13b
instruction following model family, offering fully open-source data, code, and recipes
[x] tulu3:8b
[x] qwen3-coder:30b
qwen3-coder-30b
[x] gpt-oss:20b - gpt-oss-20b
#  replace daredevil with:
#  [x] closex/neuraldaredevil-8b-abliterated
#  and
#  [x] closex/neuraldaredevil-8b-abliterated:q2_0


gosu coder:
ollama run hf.co/unsloth/gpt-oss-20b-GGUF:Q8_K_XL
[x] https://huggingface.co/unsloth/gpt-oss-20b-GGUF

smaller than recomended:
ollama run hf.co/unsloth/Qwen3-Coder-30B-A3B-Instruct-GGUF:Q3_K_XL
[x] https://huggingface.co/unsloth/Qwen3-Coder-30B-A3B-Instruct-GGUF

ollama run hf.co/unsloth/Devstral-Small-2507-GGUF:Q3_K_XL
[x] https://huggingface.co/unsloth/Devstral-Small-2507-GGUF?show_file_info=Devstral-Small-2507-UD-Q3_K_XL.gguf






