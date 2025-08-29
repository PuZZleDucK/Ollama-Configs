
# Ollama model configurations
- my collection of ollama configs and notes on model performance during use
- mostly to add context and set known params
- collection of scripts and notes on configuration
- models_config.md contains the complete list, gpt research and current todos
- Template.Modelfile contains paramater examples and clarifications


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


