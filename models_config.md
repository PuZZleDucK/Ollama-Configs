


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

[x] goekdenizguelmez/JOSIEFIED-Qwen3:14b
goekdenizguelmez-JOSIEFIED-Qwen3-14b
[x] goekdenizguelmez/JOSIEFIED-Qwen3:30b
goekdenizguelmez-JOSIEFIED-Qwen3-30b


[x] granite4:micro
template?
[x] granite4:micro-h
[x] granite4:small-h
[X] granite4:tiny-h

[x] instruct: ollama run JollyLlama/GLM-4-32B-0414-Q4_K_M
[x] reasoning: ollama run JollyLlama/GLM-Z1-32B-0414-Q4_K_M

[ ] ollama run hf.co/TheBloke/MythoMax-L2-13B-GGUF:Q8_0

[-] qwq quant/sloth/ablate

[x] https://huggingface.co/allenai/Olmo-3-1125-32B

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


[x] glm-4.7-flash:q4_K_M - prerelease
[x] https://ollama.com/library/rnj-1
[x] https://ollama.com/library/lfm2.5-thinking
[x] Dolphin 2.9.3 (Yi-1.5-34B-32k) — uncensored + function calling
[x] Airoboros 33B 2.1 — function/args JSON/YAML friendly, mild de-alignment
[x] Qwen2.5-Coder-32B-Instruct (abliterated) — uncensored-ish + strong JSON (good for tools)
[x] qwen3-coder-next


Models from dundee:
NAME                                                              ID              SIZE      MODIFIED      
qwen3:4b                                                          359d7dd4bcda    2.5 GB    3 months ago     
gemma3:12b                                                        f4031aab637d    8.1 GB    4 months ago     
gemma3:4b                                                         a2af6cc3eb7f    3.3 GB    4 months ago     
granite4:micro                                                    4235724a127c    2.1 GB    4 months ago     
gemma3:270m                                                       e7d36fb2c3b3    291 MB    4 months ago     
gemma2:9b                                                         ff02c3702f32    5.4 GB    17 months ago    
phi3:latest                                                       4f2222927938    2.2 GB    17 months ago    
phi3:3.8b                                                         4f2222927938    2.2 GB    17 months ago    
phi3:instruct                                                     4f2222927938    2.2 GB    17 months ago    
phi3:mini                                                         4f2222927938    2.2 GB    17 months ago    
llava-phi3:latest                                                 c7edd7b87593    2.9 GB    17 months ago    
llava-phi3:3.8b-mini-q4_0                                         c7edd7b87593    2.9 GB    17 months ago    
llava-phi3:3.8b-mini-fp16                                         39ed50ad5b22    8.3 GB    17 months ago    
llava-llama3:latest                                               44c161b1f465    5.5 GB    17 months ago    
llava-llama3:8b-v1.1-q4_0                                         44c161b1f465    5.5 GB    17 months ago    
falcon2:latest                                                    d8c09dbc67c3    6.4 GB    17 months ago    
llama3:text                                                       870a5d02cfaf    4.7 GB    17 months ago    
llama3:instruct                                                   365c0bd3c000    4.7 GB    17 months ago    
dbrx:132b-instruct-q2_K                                           e2554a95cc76    47 GB     17 months ago    
llama3-gradient:latest                                            5d1398df5b8b    4.7 GB    17 months ago    
llama3-gradient:instruct                                          5d1398df5b8b    4.7 GB    17 months ago    
llama3-gradient:8b                                                5d1398df5b8b    4.7 GB    17 months ago    
moondream:latest                                                  55fc3abd3867    1.7 GB    17 months ago    
moondream:v2                                                      55fc3abd3867    1.7 GB    17 months ago    
dolphin-llama3:latest                                             613f068e29f8    4.7 GB    17 months ago    
dolphin-llama3:70b                                                39cf3e48a702    39 GB     17 months ago    
dolphin-llama3:v2.9                                               613f068e29f8    4.7 GB    17 months ago    
dolphin-mixtral:latest                                            cfada4ba31c7    26 GB     17 months ago    
dolphin-phi:latest                                                c5761fc77240    1.6 GB    17 months ago    
tinydolphin:latest                                                0f9dd11f824c    636 MB    17 months ago    
tinydolphin:1.1b-v2.8-fp16                                        adb3e462abb8    2.2 GB    17 months ago    
snowflake-arctic-embed:335m                                       21ab8b9b0545    669 MB    17 months ago    
snowflake-arctic-embed:137m                                       12616299a158    274 MB    17 months ago    
snowflake-arctic-embed:110m                                       8a0d86a3ca1d    218 MB    17 months ago    
snowflake-arctic-embed:33m                                        e8db018629b4    67 MB     17 months ago    
snowflake-arctic-embed:22m                                        bf75350e1752    45 MB     17 months ago    
nomic-embed-text:latest                                           0a109f422b47    274 MB    17 months ago    
mxbai-embed-large:latest                                          468836162de7    669 MB    17 months ago    
dolphin-mistral:latest                                            5dc8c5a2be65    4.1 GB    17 months ago    
codegemma:latest                                                  0c96700aaada    5.0 GB    17 months ago    
codestral:latest                                                  fcc0019dcee9    12 GB     17 months ago    
granite-code:20b                                                  31d8bc61e506    11 GB     17 months ago    
granite-code:8b                                                   998bce918de0    4.6 GB    17 months ago    
granite-code:3b                                                   63bedbdffbf0    2.0 GB    17 months ago    
deepseek-coder:latest                                             3ddd2d3fc8d2    776 MB    17 months ago    
starcoder2:latest                                                 f67ae0f64584    1.7 GB    17 months ago    
starcoder2:15b                                                    20cdb0f709c2    9.1 GB    17 months ago    
wizardcoder:python                                                de9d848c1323    3.8 GB    17 months ago    
wizardcoder:33b-v1.1-q3_K_M                                       a10f6bc2ea74    16 GB     17 months ago    
stable-code:latest                                                37681d29a55a    1.6 GB    17 months ago    
dolphincoder:7b                                                   677555f1f316    4.2 GB    17 months ago    
dolphincoder:15b                                                  1102380927c2    9.1 GB    17 months ago    
qwen2:7b                                                          e0d4e1163c58    4.4 GB    17 months ago    
command-r:35b-v0.1-q2_K                                           ebf190a244cd    13 GB     17 months ago    
deepseek-coder-v2:latest                                          8577f96d693e    8.9 GB    17 months ago    
deepseek-v2:latest                                                7c8c332f2df7    8.9 GB    17 months ago    
gemma2:27b                                                        53261bc9c192    15 GB     17 months ago    
llama3-groq-tool-use:latest                                       36211dad2b15    4.7 GB    17 months ago    
mathstral:latest                                                  4ee7052be55a    4.1 GB    17 months ago    
codegeex4:latest                                                  867b8e81d038    5.5 GB    17 months ago    
internlm2:latest                                                  5050e36678ab    4.5 GB    17 months ago    
llama3:latest                                                     365c0bd3c000    4.7 GB    17 months ago    
llava-maid-7b-dpo.Q5_K_M.gguf:latest                              3bea4552819c    5.1 GB    17 months ago    
ggml-model-f16.gguf:latest                                        02bffb368afe    14 GB     17 months ago    
llava-v1.6-vicuna-7b.Q8_0.gguf:latest                             6783dc5fa001    7.2 GB    17 months ago    
unsloth.Q4_K_M.gguf:latest                                        144f14d13abc    4.9 GB    17 months ago    
llava-v1.5-7b-Q4_K.gguf:latest                                    e5ab7a836c31    4.1 GB    17 months ago    
Llama-3.1-8B-Instruct-abliterated_via_adapter.Q8_0.gguf:latest    c78a183fadd9    8.5 GB    17 months ago    
llama3.1:latest                                                   a23da2a80395    4.7 GB    18 months ago    
adult-script-writer:latest                                        c971ea383d20    4.1 GB    20 months ago    
dolphin-2.9-llama3-8b-q8_0.gguf:latest                            26e610f72900    8.5 GB    20 months ago    
dolphin-2.5-mixtral-8x7b.Q2_K.gguf:latest                         cef1421426c3    15 GB     20 months ago    
Fimbulvetr-11B-v2.q4_K_S.gguf:latest                              171dcd2b6d99    6.1 GB    20 months ago    
Daredevil-8B-abliterated.Q8_0.gguf:latest                         fd0e137c8a86    8.5 GB    20 months ago    
Smaug-Llama-3-70B-Instruct-IQ2_XXS.gguf:latest                    5b73c03fc1be    19 GB     20 months ago    
unholy-v2-13b.Q4_K_S.gguf:latest                                  b6a690aec8a3    7.4 GB    20 months ago    
u-amethyst-20b.Q3_K_L.gguf:latest                                 45d3ef263a85    10 GB     20 months ago    
u-amethyst-20b.Q5_0.gguf:latest                                   3129965baf4e    13 GB     20 months ago    
smaug-34b-v0.1.Q2_K.gguf:latest                                   52cf1b5aa832    12 GB     20 months ago    
nous-hermes-2-mistral-7b-dpo.Q2_K.gguf:latest                     964b2decb382    2.7 GB    20 months ago    
alphamonarch-7b.Q4_K_M.gguf:latest                                8b7fdccbd3b2    4.4 GB    20 months ago    
stablebeluga2-70B.Q2_K.gguf:latest                                262d1539b91c    29 GB     20 months ago    
alphamonarch-7b.Q8_0.gguf:latest                                  a332bec2ed06    7.7 GB    20 months ago    
unholy-v2-13b.Q2_K.gguf:latest                                    17414560edc7    5.4 GB    20 months ago    
unholy-v2-13b.Q8_0.gguf:latest                                    b135876824de    13 GB     20 months ago    
yarn-mistral-7b-128k.Q5_K_M.gguf:latest                           e33fde8b7e89    5.1 GB    20 months ago    
yarn-mistral-7b-128k.Q2_K.gguf:latest                             7808706ad31e    2.7 GB    20 months ago    
neural-chat-7b-v3-16k-q8_0.gguf:latest                            3e9f89313f96    7.7 GB    20 months ago    
nous-hermes-2-mistral-7b-dpo.Q4_K_M.gguf:latest                   c04052b097fe    4.4 GB    20 months ago    
neural-chat-7b-v3-16k-f16.gguf:latest                             f6d4b7bf1c45    14 GB     20 months ago    
DaringMaid-20B-V1.1-Q3_K_M.gguf:latest                            57c95716e57b    9.7 GB    20 months ago    
dolphinhermes-120b.Q2_K.gguf:latest                               18a4e2acc316    44 GB     21 months ago    
fimbulvetr.f16.gguf:latest                                        c6550f4dcb1a    21 GB     21 months ago    
Kunoichi-7B.f16.gguf:latest                                       8b62894defae    14 GB     21 months ago    
nous-hermes-2-mistral-7b-dpo.Q8_0.gguf:latest                     5a975b6094bf    7.7 GB    21 months ago    
yarn-mistral-7b-128k.Q8_0.gguf:latest                             0d9ca2f32f65    7.7 GB    21 months ago    
alphamonarch-7b.Q2_K.gguf:latest                                  c0c91e4cd098    2.7 GB    21 months ago    
phi3:3.8b-mini-instruct-4k-fp16                                   157684aa81ad    7.6 GB    21 months ago    
phi3:3.8b-mini-instruct-4k-q4_K_M                                 a2c89ceaed85    2.3 GB    21 months ago    





