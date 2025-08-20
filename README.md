# I. Prerequisites:
## 1. Install Ollama
curl -fsSL https://ollama.ai/install.sh | sh

## 2. Pull GPT-OSS 20B model
ollama pull gpt-oss:20b

## 3. Start Ollama server
ollama serve

# II. Basic Usage
## 1. Quick Test Run (10 iterations):
```
python3 fuzz_ollama.py --iters 10 --verbose
```
## 2. Full Fuzzing Campaign (200 iterations):
```
python3 fuzz_ollama.py --iters 200 --out full_runs.jsonl --hits full_hits.jsonl
```
## 3. Aggressive Testing (500 iterations with higher temperature):
```
python3 fuzz_ollama.py --iters 500 --temperature 0.5 --timeout 300
```
