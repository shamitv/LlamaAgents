# LlamaAgents
Llama 3.1 now supports Function calling. With Functions/Tools and 128k context, Agents should work. Exploratory project to try SQL and few other Agents

Steps to bring up OpenAI Compatible web server :

1. Ensure that llama-cpp-python library is installed with sever module . With pip : pip install "llama-cpp-python[all]"
2. Set path to Model File
3. Bring up the server on given port 

export MODEL_FILE=~/work/models/Meta-Llama-3.1-8B-Instruct_Q4_K_M.gguf
python3 -m llama_cpp.server --n_gpu_layers -1  --port 8000 --n_threads -1 --n_ctx 8096 --seed 4632    --model $MODEL_FILE

Reference : https://github.com/abetlen/llama-cpp-python/blob/main/examples/notebooks/Functions.ipynb