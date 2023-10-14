# <div align="center"> ChatGLM Series</div>

- ChatGLM
- ChatGLM2

## ChatGLM
### Introduction



## ChatGLM2
### New features and techniques




### Deployment



### Dataset
#### ADGEN
JSON format with content and summary pairs. Train and test partition = 100000 : 1000.
``` 
{
  content:"类型#裙*材质#蕾丝*风格#宫廷*图案#刺绣*图案#蕾丝*裙型#大裙摆*裙下摆#花边*裙袖型#泡泡袖",
  summary:"宫廷风的甜美蕾丝设计，清醒的蕾丝拼缝处，刺绣定制的贝壳花边，增添了裙子的精致感觉。超大的裙摆，加上精细的小花边设计，上身后既带着仙气撩人又很有女人味。泡泡袖上的提花面料，在细节处增加了浪漫感，春日的仙女姐姐。浪漫蕾丝布满整个裙身，美丽明艳，气质超仙。"
}
```

### Finetuning
- P-tuning v2 on ADGEN Dataset [[Link]](https://www.heywhale.com/mw/project/64984a7b72ebe240516ae79c/content)







### Reference
- ChatGLM Official [[bilibili]](https://space.bilibili.com/3493270982232856)
  - 从GLM-130B到ChatGLM：大模型预训练与微调
  - ChatGLM2-6B 部署与微调
- https://www.heywhale.com/mw/project/64984a7b72ebe240516ae79c/content
- https://zhuanlan.zhihu.com/p/643276738
- https://github.com/THUDM/ChatGLM2-6B
- https://huggingface.co/THUDM/chatglm2-6b
