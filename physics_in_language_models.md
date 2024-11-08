<a href="https://www.youtube.com/watch?v=yBL7J0kgldU">视频连接</a>
* There is still gap between ethology and physics

* in order to study really scientifically like what is happening behind the scene, I believe that it really requires us to do very careful controlled studies to see why exactly this happens

### Concerns
1. Studying models pre-trained using internet data is not "scientific enough"
    * need full control of the data
2. Studying individual models is not "scientific enough"
    * want universal laws that holds for all LLMs, not just the july version of GPT-4o, regardless of the pretrain / finetune parameters, model sizes
3. studying `benchmarks` may not be "scientific enough"
    * GSM8K only has 8k grade-school math problems
4. tell us little about the internals of LLMs / how things work / why things fail


### Emphasizes
1. decompose "Intelligence" into building blocks
    * structures, knowledge, reasoning, etc.
2. study in a controlled, idealized environment
    * control the data, tweak the params
3. highly repeatable experiments
    * use 100M-size models, derive universal laws
4. probing techniques to see the inner workings
    
* 很重要的实验方法：
为了防止使用的数据已经存在于大模型的pre-train/finetune datasets中，直接使用合成数据，构建一些假的人物传记，然后为每个人物传记都制定QA集合，之后分train/test set进行训练，在训练集上效果好，那叫memorization，只有测试集上效果好那才叫Extraction

3.1 Knowledge Extraction    (知识提取)
3.2 Knowledge Manipulation  (知识操纵)
    * Knowledge Manipulation is `Impossible` without CoT
3.3 Knowledge Capacity Scaling Law


2. Grade School Math and the Hidden Reasoning Process

2.2 Learn from the Mistakes



### Papers
* <a href="https://arxiv.org/search/cs?searchtype=author&query=Allen-Zhu">Allen Zhu</a>
#### Physics of Language Models: PartI: Learning Hierarchical Language Structures
* <a href="https://arxiv.org/abs/2305.13673">Arxiv链接</a>
* <a href="">
