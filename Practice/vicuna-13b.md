
### Reference
- https://huggingface.co/helloollel/vicuna-13b
- https://www.youtube.com/watch?v=F_pFH-AngoE
- https://colab.research.google.com/drive/1KlgMCJvZKD8Gnmll1tugF6xAD-Qv51ww?usp=sharing#scrollTo=_LPmr_8e-zf7
- https://github.com/lm-sys/FastChat/issues/1543
- https://github.com/lm-sys/FastChat/issues/244
- https://github.com/lm-sys/FastChat/blob/main/fastchat/serve/model_worker.py
- https://github.com/lm-sys/FastChat


#### Step 1
Install [fastchat](https://github.com/lm-sys/FastChat), and use method 2. Method 1 seems useless at least in my several tries.

#### Step 2
Get LLaMA model and weights


#### Step 3
Get vicuna model and weights

#### Step 4
convert llama model into huggingface format
```python
python ./convert_llama_weights_to_hf.py  --input_dir /path/to/downloaded/llama/weights --model_size 13B --output_dir ./path
```

#### Step 5
conbime llama-hf and vicuva-13b delta weight to get whole complete model
```python
python3 -m fastchat.model.apply_delta --base /root/autodl-tmp/model/llama-13b-hf --delta /root/autodl-tmp/vicuna_data/vicuna-13b-delta-v1.1 --target /root/autodl-tmp/vicuna-13b 
```
#### Step 6
### Deploy
controller
```python
python3 -m fastchat.serve.controller --host "127.1.1.1"
```
worker
```python
python -m fastchat.serve.model_worker --model-path /root/autodl-tmp/vicuna-13b --controller-address http://127.1.1.1:21001 --port 21002 --worker-address "http://127.1.1.1:21002" --num-gpu 2 --host 127.1.1.1
```
web ui
```python
python -m  fastchat.serve.gradio_web_server --controller-url http://127.1.1.1:21001 --host 127.1.1.1  --port 21004
```
### Overall File Structure
```
.File
|--vicuna-13b (final model from vicuna-13b-delta-v1.1 and llama-13-hf)
|--pyllama
    |-- 13B (raw data)
        |--consolidated.00.pth
        |--consolidated.01.pth
        |--..
    |-- 7B (raw data)
    |--tokenizer.model
|-- vicuna-13b-delta-v1.1 (delta weights)
|-- llama-13-hf (huggingface data from 13B raw data)
    |--pytorch_model-00000-of-00041.bin
```
