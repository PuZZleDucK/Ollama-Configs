

# sort alpha
ollama list | tail -n +2 | sort -k1,1



# agent info

create a text document with this model list in it:
...
then research each of the models on ollama or hugging face to find out the correct configuration parameters for running the model and add the required parameters to the document.


# show config
ollama show my‑model‑tag

# works?
ollama show --modelfile my-model-tag > Modelfile



# 1 — create or copy your locked‑down model
ollama create gemma3-ctx:7b -f ./Modelfile   # or: ollama cp gemma3:7b gemma3-ctx:7b

# save to 'update-list.md'
then during update restore these models, uupdate then remove again

# 2 — delete the base tag
ollama rm gemma3:7b


# update dependants
ollama pull qwen3
ollama rm qwen3-ctx
ollama create qwen3-ctx -f ./Modelfile





# bash idea
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



