


Jeff Beck
preprocessing with vae - take data set - run pca on it then run through vae
- principal component analysis



model voting - weight smarter model results
	- model presents arguments anon
	- rates other arguments anon
	- best rated model gets weight boost
	- arguments sorted by weighted scores and trimmed to top 50%









[x] # command-r7b:7b
- Author: Cohere
- max_new_tokens: 100
- temperature: 0.3
- do_sample: true
- stop: ["<|START_OF_TURN_TOKEN|>", "<|END_OF_TURN_TOKEN|>", "<|END_RESPONSE|>"]
- context_length: 128k
  - Optional: top_k=40, top_p=0.95, min_p=0.05, typical_p=1.0, temperature=0.0

[x] # command-r7b:7b-12-2024-fp16
- Author: Cohere
- temperature: 0.3
- stop: ["<|START_OF_TURN_TOKEN|>", "<|END_OF_TURN_TOKEN|>", "<|END_RESPONSE|>"]
- context_length: 128k
  - Optional: top_k=40, top_p=0.95, min_p=0.05, typical_p=1.0, temperature=0.0

[x] # deepcoder:14b
- Author: Agentica
- temperature: 0.6
- top_p: 0.95
- max_tokens: 64000
- avoid_system_prompt: true
- context_length: 32k
  - Optional: top_k=50, temperature=0.2, repetition_penalty=1.03, max_new_tokens=256, stop=["\nUser:", "<|endoftext|>", "</s>"]

[x] # deepcoder:1.5b
- Author: Agentica
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=50, repetition_penalty=1.03, max_new_tokens=256

[x] # deepseek-r1:1.5b
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[x] # deepseek-r1:7b
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[x] # deepseek-r1:8b
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[x] # deepseek-r1:14b
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[x] # deepseek-r1:32b
- Author: DeepSeek AI
- temperature: 0.6
- avoid_system_prompt: true
- context_length: 128k
  - Optional: top_p=0.95

[-] # deepseek-r1-distill-qwen-1.5b - hallucinated?
- Author: DeepSeek AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[-] # deepseek-r1-distill-qwen-7b
- Author: DeepSeek AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[-] # deepseek-r1-distill-qwen-14b
- Author: DeepSeek AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[-] # deepseek-r1-distill-qwen-32b
- Author: DeepSeek AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:0.5b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:1.5b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:3b - NEW - added by agent?
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:7b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:14b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5:32b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:0.5b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:1.5b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:3b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:7b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:14b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5-coder:32b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5vl:3b - ERROR
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5vl:7b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen2.5vl:32b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # qwen3:0.6b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:1.7b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:4b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:8b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:14b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwen3:32b
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

# qwen3:latest - used? - which one?
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.8
- repetition_penalty: 1.05
- context_length: 128k
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # qwq:latest
- Author: Alibaba (Qwen Team)
- temperature: 0.7
- top_p: 0.85
- context_length: 32k
  - Optional: None specified by community

[x] # smollm:135m
- Author: Hugging Face Smol Models Team
- temperature: 0.6
- top_p: 0.9
- max_new_tokens: 512
  - Optional: None specified by community

[x] # smollm:360m
- Author: Hugging Face Smol Models Team
- temperature: 0.6
- top_p: 0.9
- max_new_tokens: 512
  - Optional: None specified by community

[x] # smollm:1.7b
- Author: Hugging Face Smol Models Team
- temperature: 0.6
- top_p: 0.9
- max_new_tokens: 512
  - Optional: None specified by community

[x] # wizard-vicuna-uncensored:7b - not there
- Author: Eric Hartford & TheBloke
- temperature: 0.7
- top_p: 0.9
- context_length: 2k
- memory_requirement: ≥8GB
  - Optional: None specified by community

[x] # wizard-vicuna-uncensored:13b
- Author: Eric Hartford & TheBloke
- temperature: 0.7
- top_p: 0.9
- context_length: 2k
- memory_requirement: ≥16GB
  - Optional: None specified by community

[x] # wizard-vicuna-uncensored:30b
- Author: Eric Hartford & TheBloke
- temperature: 0.7
- top_p: 0.9
- context_length: 2k
- memory_requirement: ≥32GB
  - Optional: None specified by community


[x] # eris_primev3-vision-7b-gguf - not there
- Author: Lewdiculous
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 512
  - Optional: top_p=1, top_k=0, top_a=0, tfs=1, epsilon_cutoff=0, eta_cutoff=0, typical_p=1, min_p=0.1, repetition_penalty=1

[x] # exaone-deep:2.4b
- Author: NAVER
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # exaone-deep:7.8b
- Author: NAVER
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # exaone-deep:32b
- Author: NAVER
- temperature: 0.6
- top_p: 0.95
- context_length: 128k
  - Optional: None specified by community

[x] # falcon3:7b
- Author: Technology Innovation Institute (TII)
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: None specified by community

[x] # falcon3:10b
- Author: Technology Innovation Institute (TII)
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: None specified by community

[x] # gemma3:1b
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
- context_length: 32k
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3:4b
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
- context_length: 128k
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3:12b
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
- context_length: 128k
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3:27b
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
- context_length: 128k
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3n:e2b
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # gemma3n:e4b
- Author: Google
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[-] # gemma-the-writer-n-restless-quill-10b-uncensored-gguf-q8_0
- Author: Bartowski
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[-] # hf.co/bartowski/phi-3.5-mini-instruct_uncensored-gguf:f16
- Author: Bartowski
- temperature: 0.7
- top_p: 0.9
- repetition_penalty: 1.05
- max_new_tokens: 1024
  - Optional: None specified by community

[x] # hf.co/davidau/gemma-the-writer-n-restless-quill-10b-uncensored-gguf:q8_0`config-hf-co-davidau-gemma-the-writer-n-restless-quill-10b-uncensored-gguf-q8_0`
- Author: DavidAU
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # hf.co/davidau/l3.2-rogue-creative-instruct-uncensored-abliterated-7b-gguf:q8_0`config-hf-co-davidau-l3-2-rogue-creative-instruct-uncensored-abliterated-7b-gguf-q8_0`
- Author: DavidAU
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # hf.co/davidau/llama-3.2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18.4b-gguf:q2_k`config-hf-co-davidau-llama-3-2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18-4b-gguf-q2_k`
- Author: DavidAU
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # hf.co/davidau/llama-3.2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18.4b-gguf:q6_k`config-hf-co-davidau-llama-3-2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18-4b-gguf-q6_k`
- Author: DavidAU
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # hf.co/davidau/llama-3.2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18.4b-gguf:q8_0`config-hf-co-davidau-llama-3-2-8x3b-moe-dark-champion-instruct-uncensored-abliterated-18-4b-gguf-q8_0`
- Author: DavidAU
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # hf.co/devsdocode/llama-3-8b-uncensored-q4_k_m-gguf:q4_k_m
- Author: DevsDoCode
- temperature: 0.6
- top_p: 0.9
  - Optional: None specified by community

[x] # hf.co/lewdiculous/eris_primev3-vision-7b-gguf-iq-imatrix:latest`config-hf-co-lewdiculous-eris_primev3-vision-7b-gguf-iq-imatrix-latest`
- Author: Lewdiculous
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 512
  - Optional: top_p=1, top_k=0, top_a=0, tfs=1, epsilon_cutoff=0, eta_cutoff=0, typical_p=1, min_p=0.1, repetition_penalty=1

[x] # hf.co/mlabonne/daredevil-8b-abliterated-gguf:latest
- Author: MLabonne
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # hf.co/mlabonne/gemma-3-27b-it-abliterated-gguf:q4_k_m
- Author: MLabonne
- temperature: 1.0
- top_p: 0.95
- top_k: 64
  - Optional: min_p=0.0, repetition_penalty=1.0

[x] # hf.co/mradermacher/deepseek-r1-distill-qwen-32b-uncensored-gguf:q4_k_m`config-hf-co-mradermacher-deepseek-r1-distill-qwen-32b-uncensored-gguf-q4_k_m`
- Author: Mradermacher
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # hf.co/mradermacher/deepseek-r1-distill-qwen-32b-uncensored-gguf:q8_0`config-hf-co-mradermacher-deepseek-r1-distill-qwen-32b-uncensored-gguf-q8_0`
- Author: Mradermacher
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # hf.co/mradermacher/josiefied-deepseek-r1-0528-qwen3-8b-abliterated-v1-gguf:q8_0`config-hf-co-mradermacher-josiefied-deepseek-r1-0528-qwen3-8b-abliterated-v1-gguf-q8_0`
- Author: Mradermacher
- temperature: 0.6
- top_p: 0.95
  - Optional: top_k=20, min_p=0.0, presence_penalty=1.5

[x] # hf.co/mradermacher/magistral-small-2506-abliterated-i1-gguf:q2_k`config-hf-co-mradermacher-magistral-small-2506-abliterated-i1-gguf-q2_k`
- Author: Mradermacher
- temperature: 0.7
- top_p: 0.9
- context_length: 32k
  - Optional: top_p=0.95, temperature=0.7, max_tokens=40960

[x] # hf.co/mradermacher/nyan_chaos-vision-7b-gguf:q8_0
- Author: Mradermacher
- temperature: 0.7
- top_p: 0.9
- context_length: 32k
  - Optional: None specified by community

[x] # hf.co/mungert/josiefied-qwen3-8b-abliterated-v1-gguf:latest
- Author: Mungert
- temperature: 0.7
- top_p: 0.9
  - Optional: use thinking-mode config (temperature=0.6, top_p=0.95, top_k=20, min_p=0.0, presence_penalty=1.5) or non-thinking config (temperature=0.7, top_p=0.8, top_k=20, min_p=0.0)

[x] # hf.co/orenguteng/llama-3.1-8b-lexi-uncensored-v2-gguf:latest`config-hf-co-orenguteng-llama-3-1-8b-lexi-uncensored-v2-gguf-latest`
- Author: Orenguteng
- temperature: 0.6
- top_p: 0.95
  - Optional: None specified by community

[x] # hf.co/thebloke/wizard-vicuna-13b-uncensored-gguf:q4_k_m
- Author: TheBloke
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # hf.co/thebloke/wizard-vicuna-13b-uncensored-gguf:q8_0
- Author: TheBloke
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # llama3.2-vision:11b
- Author: Meta
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # llama3.3:70b
- Author: Meta
- temperature: 0.6
- top_p: 0.95
- max_new_tokens: 32768
  - Optional: None specified by community

[x] # llava:7b
- Author: LLaVA Team
- temperature: 0.7
- top_p: 0.9
- context_length: 8k
  - Optional: None specified by community

[x] # llava:13b
- Author: LLaVA Team
- temperature: 0.7
- top_p: 0.9
- context_length: 8k
  - Optional: None specified by community

[x] # llava:34b
- Author: LLaVA Team
- temperature: 0.7
- top_p: 0.9
- context_length: 8k
  - Optional: None specified by community

[x] # magistral:24b
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.9
- context_length: 32k
  - Optional: top_p=0.95, temperature=0.7, max_tokens=40960

[x] # minicpm-v:latest
- Author: OpenBMB
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 512
  - Optional: None specified by community

[x] # mistral-small3.1:24b
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: temperature=0.15

[x] # mistral-small3.2:24b
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: temperature=0.15

[-] # mistral-small3.2:latest - dupe
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.9
- max_new_tokens: 4096
  - Optional: temperature=0.15

[-] # nyan_chaos-vision-7b-gguf:q8_0 - dupe
- Author: Mradermacher
- temperature: 0.7
- top_p: 0.9
  - Optional: None specified by community

[x] # opencoder:1.5b
- Author: OpenCoder Team
- temperature: 0.7
- top_p: 0.95
- context_length: 32k
  - Optional: None specified by community

[x] # opencoder:8b
- Author: OpenCoder Team
- temperature: 0.7
- top_p: 0.95
- context_length: 32k
  - Optional: None specified by community

[x] # phi4-mini-reasoning:3.8b
- Author: Microsoft Research
- temperature: 0.8
- top_p: 0.95
- do_sample: true
- max_new_tokens: 4096
  - Optional: top_k=50

[x] # phi4-reasoning:plus
- Author: Microsoft Research
- temperature: 0.8
- top_p: 0.95
- do_sample: true
- max_new_tokens: 4096
  - Optional: top_k=50

[x] # yi-coder:1.5b
- Author: 01.AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: None specified by community

[x] # yi-coder:9b
- Author: 01.AI
- temperature: 0.6
- top_p: 0.95
- context_length: 32k
  - Optional: None specified by community

[x] # devstral:24b
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.95
- max_tokens: 40960
- context_length: 40k
  - Optional: top_k=64, min_p=0.01, repetition_penalty=1.0

[-] # devstral:latest - dupe
- Author: Mistral AI
- temperature: 0.7
- top_p: 0.95
- max_tokens: 40960
- context_length: 40k
  - Optional: top_k=64, min_p=0.01, repetition_penalty=1.0

[x] # dolphin3:8b
- Author: Eric Hartford
- temperature: 0.6
- top_p: 0.9
- do_sample: true
- context_length: 8k
  - Optional: None specified by community

[x] # granite3.2-vision:2b
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3.3:2b
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3.3:8b
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3-dense:2b
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3-dense:8b
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3-moe:1b
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # granite3-moe:3b
- Author: IBM
- temperature: 0.7
- top_p: 0.9
- context_length: 128k
  - Optional: None specified by community

[x] # hermes3:3b
- Author: Nous Research
- temperature: 0.6
- top_p: 0.9
- do_sample: true
- context_length: 8k
  - Optional: top_k=50, repetition_penalty=1.1, temperature=0.8

[x] # hermes3:8b
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


replace daredevil with:
[x] closex/neuraldaredevil-8b-abliterated
and
[x] closex/neuraldaredevil-8b-abliterated:q2_0


gosu coder:
ollama run hf.co/unsloth/gpt-oss-20b-GGUF:Q8_K_XL
[x] https://huggingface.co/unsloth/gpt-oss-20b-GGUF

smaller than recomended:
ollama run hf.co/unsloth/Qwen3-Coder-30B-A3B-Instruct-GGUF:Q3_K_XL
[x] https://huggingface.co/unsloth/Qwen3-Coder-30B-A3B-Instruct-GGUF

ollama run hf.co/unsloth/Devstral-Small-2507-GGUF:Q3_K_XL
[x] https://huggingface.co/unsloth/Devstral-Small-2507-GGUF?show_file_info=Devstral-Small-2507-UD-Q3_K_XL.gguf




Sept 2025
[x] ollama run hf.co/mradermacher/Josiefied-Qwen3-30B-A3B-abliterated-v2-GGUF:Q4_K_M
Josiefied-Qwen3-30B-A3B-abliterated-v2-GGUF-Q4_K_M
[ ] ollama run hf.co/mradermacher/Josiefied-Qwen3-30B-A3B-abliterated-v2-GGUF:Q5_K_M
context_length 	40960
feed_forward_length 	6144

template:
<|system|>
{system_message}</s>
<|user|>
{prompt}</s>
<|assistant|>

[x] ollama run hf.co/unsloth/Qwen3-30B-A3B-Instruct-2507-GGUF:Q3_K_XL 
unsloth-Qwen3-30B-A3B-Instruct-2507-GGUF-Q3_K_XL
[-] ollama run hf.co/unsloth/Qwen3-30B-A3B-Instruct-2507-GGUF:Q5_K_XL
context_length 	262144
feed_forward_length 	6144
Number of Experts: 128
Number of Activated Experts: 8
Context Length: 262,144 natively.
non-thinking
suggest using Temperature=0.7, TopP=0.8, TopK=20, and MinP=0.
output length of 16,384

[x] ollama run hf.co/BasedBase/Qwen3-30B-A3B-Thinking-2507-Deepseek-v3.1-Distill-V2:Q3_K_M
Qwen3-30B-A3B-Thinking-2507-Deepseek-v3-1-Distill-V2-Q3_K_M
[x] ollama run hf.co/BasedBase/Qwen3-30B-A3B-Thinking-2507-Deepseek-v3.1-Distill-V2:Q5_K_M
context_length 	262144
Teacher Model: deepseek-ai/DeepSeek-V3.1.
Student Model: Qwen/Qwen3-30B-A3B-Thinking-2507.
Temperature = 0.6
Min_P = 0.00
Top_P = 0.95
TopK = 20


[x] huihui_ai/qwen3-abliterated:16b
huihui_ai-qwen3-abliterated-16b
[x] huihui_ai/qwen3-abliterated:30b
{
    "repeat_penalty": 1,
    "stop": [
        "<|im_start|>",
        "<|im_end|>"
    ],
    "temperature": 0.6,
    "top_k": 20,
    "top_p": 0.95
}

[x] goekdenizguelmez/JOSIEFIED-Qwen3:14b
goekdenizguelmez-JOSIEFIED-Qwen3-14b
[x] goekdenizguelmez/JOSIEFIED-Qwen3:30b
goekdenizguelmez-JOSIEFIED-Qwen3-30b
{
    "repeat_penalty": 1,
    "stop": [
        "<|im_start|>",
        "<|im_end|>"
    ],
    "temperature": 0.6,
    "top_k": 20,
    "top_p": 0.95
}


[x] granite4:micro
template?
[x] granite4:micro-h
[x] granite4:small-h
[X] granite4:tiny-h

[ ] instruct: ollama run JollyLlama/GLM-4-32B-0414-Q4_K_M
[ ] reasoning: ollama run JollyLlama/GLM-Z1-32B-0414-Q4_K_M

[ ] ollama run hf.co/TheBloke/MythoMax-L2-13B-GGUF:Q8_0
MythoMax-L2-13B-GGUF-Q8_0
temp 0.7 --repeat_penalty 1.1
4096 to the desired sequence

together.ai models to test:
review docs test:
- [ ] zai-org/GLM-4.5-Air-FP8
- [ ] Qwen/QwQ-32B
- [ ] mistralai/Magistral-Small-2506 - custom endpoint?
- [ ] openai/gpt-oss-120b - api fail?
- [ ] moonshotai/Kimi-K2-Instruct-0905 - searching - thrown off by mcps
- [ ] deepseek-ai/DeepSeek-V3.1 - difficulties with provided tools
- [ ] Qwen/Qwen3-Coder-480B-A35B-Instruct-FP8
- [ ] Qwen/Qwen3-235B-A22B-Thinking-2507 - multi file access - looking good - edit fails

- [ ] cognitivecomputations/dolphin-2.5-mixtral-8x7b (32768)
- [ ] databricks/dbrx-instruct (32768)
- [ ] Qwen/Qwen2.5-72B-Instruct-Turbo
- [ ] arcee-ai/maestro-reasoning
- [ ] zero-one-ai/Yi-34B-Chat
- [ ] databricks/dbrx-instruct
- [ ] garage-bAInd/Platypus2-70B-instruct
- [ ] togethercomputer/RedPajama-INCITE-Chat-3B-v1
- [ ] togethercomputer/RedPajama-INCITE-7B-Chat
- [ ] togethercomputer/StripedHyena-Nous-7B
- [ ] black-forest-labs/FLUX.1-krea-dev


[-] qwq quant/sloth/ablate



[x] https://huggingface.co/allenai/Olmo-3-1125-32B
hf.co/allenai/Olmo-3-1125-32B - nope
unsloths:
ollama run hf.co/unsloth/Olmo-3-32B-Think-GGUF:Q5_K_XL


[x] qwen3-vl:30b
[x] qwen3-vl:8b
[x] qwen3-vl:4b
[x] qwen3-vl:2b


[x] granite4:350m
[x] granite4:1b
[x] granite4:3b



[x] ollama run hf.co/backyardai/L3-Umbral-Mind-RP-v3.0-8B-GGUF:Q8_0 - L3-Umbral-Mind-RP-v3.0-8B-GGUF-Q8_0

[x] chenzo/notConfucius.v2.qwen3-14b:latest
[x] olmo-3.1:32b
[x] functiongemma:270m
[x] nemotron-3-nano:30b

[ ] glm-4.7-flash:q4_K_M - prerelease
slug: glm-4-7-flash-q4_K_M
https://ollama.com/library/glm-4.7-flash:q4_K_M
context: 198K
{
    "temperature": 1
}


[ ] https://ollama.com/library/rnj-1
slug: rnj-1
Essential AI
agentic capabilities
rnj-1:8b
context: 32K
{
    "stop": [
        "<|start_header_id|>",
        "<|end_header_id|>",
        "<|eot_id|>"
    ],
    "temperature": 0.2
}

[ ] https://ollama.com/library/lfm2.5-thinking
slug: lfm2-5-thinking
Liquid AI
lfm2.5-thinking:1.2b
context: 125K
{
    "temperature": 0.05,
    "top_k": 50
}



[ ] Dolphin 2.9.3 (Yi-1.5-34B-32k) — uncensored + function calling
slug: dolphin-2-9-3-yi-1-5-34b-32k-q8_0
HF: https://huggingface.co/dphn/dolphin-2.9.3-Yi-1.5-34B-32k
Ollama: rjmalagon/dolphin-2.9.3-yi-1.5-34b-32k-q8_0

- Maker: Eric Hartford / Cognitive Computations (dphn)
- Base model: 01-ai/Yi-1.5-34B-32k
- Weights: 34B parameters (Yi-34B class)
- License: Apache-2.0
- Context: base supports 32K; finetune trained with seq len 8192 (still generally used at 32K)
- Prompt format: ChatML
  - stop tokens to consider: <|im_end|> / <|im_start|>

Recommended params (tool use / structured outputs):
{
    "temperature": 0.2,
    "top_p": 0.9,
    "num_ctx": 32768,
    "stop": [
        "<|im_end|>",
        "<|im_start|>"
    ]
}


[ ] Airoboros 33B 2.1 — function/args JSON/YAML friendly, mild de-alignment
slug: Airoboros-33B-2-1-GGUF-Q4_K_M
HF: hf.co/TheBloke/Airoboros-33B-2.1-GGUF:Q4_K_M
GGUF: https://huggingface.co/TheBloke/Airoboros-33B-2.1-GGUF

- Maker: Jon Durbin
- Base model family: LLaMA 30B-class (repo name calls it “33B”)
- License (per HF metadata): CC-BY-NC-4.0
- Context: rope scaled to 4096 (author notes limited long-context data; YMMV)
- Prompt format: "A chat. USER: {prompt} ASSISTANT:" (or newline variant)
  - strongly recommended stop: "USER:" (prevents it roleplaying multi-turn chat forever)


Recommended params (tool use / keep it on-rails):
{
    "temperature": 0.2,
    "top_p": 0.9,
    "num_ctx": 4096,
    "repeat_penalty": 1.1,
    "stop": [
        "USER:"
    ]
}


[ ] Qwen2.5-Coder-32B-Instruct (abliterated) — uncensored-ish + strong JSON (good for tools)
slug: qwen2-5-coder-abliterate-32b
HF: https://huggingface.co/huihui-ai/Qwen2.5-Coder-32B-Instruct-abliterated
Base: https://huggingface.co/Qwen/Qwen2.5-Coder-32B-Instruct
Ollama: huihui_ai/qwen2.5-coder-abliterate:32b

- Maker: huihui-ai (abliteration), based on Alibaba Qwen2.5-Coder
- Weights: 32.5B parameters (per base model card)
- License: Apache-2.0
- Context: base supports up to 131,072 tokens (and typically generates up to ~8192 tokens); model card notes config.json defaults to 32,768 and uses YaRN rope_scaling for longer contexts (Ollama builds may vary)

Recommended params (tool use / JSON):
{
    "temperature": 0.1,
    "top_p": 0.9,
    "num_ctx": 32768
}

[ ] qwen3-coder-next
qwen3-coder-next:q4_K_M
context: 256K
{
    "temperature": 1,
    "top_k": 40,
    "top_p": 0.95
}

