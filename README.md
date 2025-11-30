
# Ollama model configurations
- my collection of ollama configs and notes on model performance during use
- mostly to add context and set known params
- collection of scripts and notes on configuration
- models_config.md contains the complete list, gpt research and current todos
- Template.Modelfile contains paramater examples and clarifications



# Codex config for ollama models

check for tool use support via ollama:
```
for m in $(ollama list | grep config- | awk '{print $1}' | tail -n +2); do   echo -n "$m: ";   curl -s http://localhost:11434/v1/chat/completions     -H 'Content-Type: application/json'     -d "{
      \"model\": \"$m\",
      \"messages\": [{\"role\":\"user\",\"content\":\"hi\"}],
      \"tools\": [{
        \"type\":\"function\",                                                 
        \"function\": {\"name\":\"ping\",\"parameters\":{\"type\":\"object\",\"properties\":{}}}
      }]
    }" | jq -r '.error.message // "tools supported"'; done
```


add ollama provider and model(s) the codex config file (~/.codex/config.toml):
```
[model_providers.ollama]
name     = "Ollama"
base_url = "http://localhost:11434/v1"

[profiles.ollama-gpt-oss-20b]
model_provider = "ollama"
model = "config-gpt-oss-20b"
```


running codex cli usually requires `--sandbox danger-full-access` or `--yolo` to not trip up the model with permissions.
```
codex exec --skip-git-repo-check --sandbox danger-full-access --profile config-gpt-oss-20b "describe the current codebase"
```

working profiles:
- ollama-gpt-oss-20b
- ollama-josiefied-qwen3 (mungert)
- ollama-qwen2-5-7b, ollama-qwen2-5-14b
- ollama-qwen3-1-7b, ollama-qwen3-4b, ollama-qwen3-8b, ollama-qwen3-8b, ollama-qwen3-14b
- 


# Other Useful Ollama Stuff

### sort models alpha
```
ollama list | tail -n +2 | sort -k1,1
```


### show current config for model
handy for migrating from a chat config to file
```
ollama show my‑model‑tag
ollama show --modelfile my-model-tag > Modelfile
```


### bash idea for updates to custom models
was trying to avoid having all the base models cluttering up the model list but it might be more trouble than it's worth
```
    #!/usr/bin/env bash
    set -e
    MODEL_BASE="qwen3" # pass as params from list?
    CUSTOM_TAG="qwen3-ctx"
    FILE="./Modelfile"

    ollama pull "$MODEL_BASE"          # refresh upstream tag

    # Regenerate the derived model (delete‑and‑create is idempotent)
    if ollama list | grep -q "^$CUSTOM_TAG"; then
    ollama rm "$CUSTOM_TAG"
    fi
    ollama create "$CUSTOM_TAG" -f "$FILE"
```
... might noot be required, updates seem to pass through to config during update


