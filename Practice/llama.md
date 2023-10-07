

#### Why should we or must we finetune our model?

Steer the output

reduce hallucination

 



#### Data Preparation



#### Computation consuming calculation





#### Finetuning

- Full training
- PEFT
- Lora



#### Evaluation

#### Benchmark





#### Open source model

#### Meta Llama Series

- Llama
- Llama2
- CodeLlma





### Deployment

#### LLaMA

- 模型的推理

  - text-generation-webui

    - ```python
      python server.py --model llama1_13b_hf --api --listen --public-api --gpu-memory 20 20 20
      ```

  - fastchat

  - vLLM

  - transformer libs

#### LLaMA 2

- 数据准备
- GPU和内存准备
  - 7B 13G
  - 13B 
- 模型的转换，因为使用text-gui-
  - [huggingface/transformers: 🤗 Transformers: State-of-the-art Machine Learning for Pytorch, TensorFlow, and JAX. (github.com)](https://github.com/huggingface/transformers)
  - [LLama 2干货部署教程+模型分发 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/645142694)	

```python
	python src/transformers/models/llama/convert_llama_weights_to_hf.py --input_dir ../13B --model_size 13B --output_dir ../llama1_13b_hf
```

- 模型的推理

  - transformer library

    - 选取本地文件

  - text-generation-webui

    - [text-generation-webui](https://link.zhihu.com/?target=https%3A//github.com/oobabooga/text-generation-webui.git)
  
    - [oobabooga/text-generation-webui: A Gradio web UI for Large Language Models. Supports transformers, GPTQ, llama.cpp (GGUF), Llama models. (github.com)](https://github.com/oobabooga/text-generation-webui)

    - 
  
    - ```python
      python server.py --model  --api --listen --public-api
      ```
  
  - fastchat
  







#### library

> - lamini
> - pytorch
> - huggingface
> - [使用 FastChat 部署 LLM - Hacker and Geeker's Way (zhaozhiming.github.io)](https://zhaozhiming.github.io/2023/08/22/use-fastchat-deploy-llm/)



[使用 FastChat 部署 LLM - Hacker and Geeker's Way (zhaozhiming.github.io)](https://zhaozhiming.github.io/2023/08/22/use-fastchat-deploy-llm/)

https://github.com/oobabooga/text-generation-webui/blob/main/docs/LLaMA-v2-model.md

https://zhuanlan.zhihu.com/p/645142694

https://github.com/ggerganov/llama.cpp#prepare-data--run

https://huggingface.co/blog/llama2#using-transformers

[huggingface AutoTokenizer.from_pretrained流程 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/621106604)

[功能超全的强化学习画图脚本 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/362677143#:~:text=可以直接在pycharm或者vscode执行，也可以用命令行传参； 按exp_name排序，而不是按时间排序；,固定好每个exp_name的颜色； 可以调节曲线的线宽，便于观察； 保存图片到本地，便于远程ssh画图~)

#### Reference



> - https://ai.meta.com/llama/
> - https://huggingface.co/meta-llama
> - https://ai.meta.com/blog/code-llama-large-language-model-coding/?utm_source=twitter&utm_medium=organic_social&utm_campaign=codellama&utm_content=image
> - https://openrouter.ai/playground
> - https://github.com/openai/openai-cookbook/blob/main/examples/How_to_stream_completions.ipynb
> - https://medium.com/@alonso.silva/how-to-access-gpt-4-gpt4-32k-right-now-for-4-dollars-pay-as-you-go-1ce4b0d7cee6
> - https://gptgod.site/#/forgot
> - https://github.com/lamini-ai/lamini
> - https://app.lamini.ai/account

