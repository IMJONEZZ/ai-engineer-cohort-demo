# Local models

Parts of the program run open-weights models on your own machine, so download
one before the cohort while your bandwidth is your own.

You need roughly 8 GB free disk and 16 GB RAM for the models we use.

## Windows

Install llama.cpp and pull a small instruct model:

```powershell
winget install ggml.llamacpp
llama-cli --hf-repo Qwen/Qwen2.5-7B-Instruct-GGUF --hf-file qwen2.5-7b-instruct-q4_k_m.gguf -p "Say hello in five words."
```

## macOS

LM Studio is the smoothest path on Apple silicon:

1. Install: `brew install --cask lm-studio`
2. In LM Studio, search for a 7B-class instruct model and download the
   `Q4_K_M` build.
3. Open the chat tab and send a test prompt.

## Linux

Build llama.cpp and pull the same model:

```bash
git clone https://github.com/ggml-org/llama.cpp && cd llama.cpp
cmake -B build && cmake --build build --config Release -j
./build/bin/llama-cli --hf-repo Qwen/Qwen2.5-7B-Instruct-GGUF --hf-file qwen2.5-7b-instruct-q4_k_m.gguf -p "Say hello in five words."
```

## Verify

Whatever the platform: a model answers a prompt locally, with Wi-Fi off.
That is the bar — Day 3+ labs assume it.
