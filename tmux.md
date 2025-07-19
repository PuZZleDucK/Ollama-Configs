docker container stop open-webui && docker container start open-webui && \
tmux new-session -d -s dev "cd ~/x/tts/Chatterbox-TTS-Server/ && source venv/bin/activate && python server.py" && \
# 1) Split above for nvtop (7 lines), landing it at the top
tmux split-window -t dev -v -b -l 7 "nvtop" && \
# 2) Focus back down to the TTS pane, then split above it for watch (5 lines)
tmux select-pane -t dev -D && \
tmux split-window -t dev -v -b -l 5 "watch ollama ps" && \
# 3) Focus down to the TTS pane again, then split above it for ComfyUI (remaining height)
tmux select-pane -t dev -D && \
tmux split-window -t dev -v -b "cd /media/puzzleduck/Data/ComfyUI && python main.py --listen 0.0.0.0" && \
# 4) Jump into your beautifully ordered dashboard
tmux attach -t dev
