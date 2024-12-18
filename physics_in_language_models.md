<a href="https://www.youtube.com/watch?v=yBL7J0kgldU">ICLR 2024 Tutorials链接</a>
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



## Physics of Language Models: 
* <a href="https://arxiv.org/search/cs?searchtype=author&query=Allen-Zhu">Allen Zhu (Arxiv)</a>
* <a href="http://zeyuan.allen-zhu.com/index.php">Allen Zhu's Homepage</a>

关键字约定
* CFGs: Context-Free Grammers

### Part 1: Learning Hierarchical Language Structures
* <a href="https://arxiv.org/abs/2305.13673">Arxiv链接</a>
* <a href="./physics_in_language_models/2305.13673v3.pdf">查看PDF</a>
#### 摘要提取

1. **研究背景**：
   - Transformer语言模型效果显著但结构复杂，理解其内部机制面临挑战。现有研究主要集中于模型如何处理简单任务（如名称复制或选择）。

2. **研究目标**：
   - 扩展现有研究，探究Transformer模型如何处理复杂的递归语言结构，特别是由上下文无关文法（CFG）定义的结构。

3. **方法与数据集**：
   - 引入一个生成分层规则的合成CFG族，可以产生长度较长、局部模糊且需要动态规划解析的句子（如数百个词的句子）。
   
4. **主要发现**：
   - 生成式模型（如GPT）能够准确学习CFG语言并基于该结构生成句子。
   - 研究模型内部状态，发现其隐藏状态能够精确捕捉CFG结构，注意力模式也类似于动态规划算法中的信息传递过程。
   - **相关结论**：
     - 位置嵌入比相对注意力或旋转嵌入效果较差。
     - 编码器模型（如BERT、deBERTa）在处理深层嵌套的CFG结构上不如生成模型（如GPT）有效。
     - 在预训练数据中加入结构性和句法性错误可以提高模型对破损语言前缀的鲁棒性。

5. **研究意义**：
   - 该研究为理解Transformer模型在复杂结构上的表现提供了洞见，有助于进一步优化模型的结构和训练策略。

### Part 2.1, Grade-School Math and the Hidden Reasoning Process
* <a href="https://arxiv.org/abs/2407.20311">Arxiv链接</a>
* <a href="./physics_in_language_models/2407.20311v1.pdf">查看PDF</a>
#### 摘要提取

1. **研究背景**：
   - 语言模型（LLMs）在数学推理问题上表现出色，在GSM8K等小学数学基准上接近完美准确率。

2. **研究目标**：
   - 系统性地研究语言模型解决数学问题的内在机制，探讨模型是否真正具备推理能力或只是模板记忆。

3. **研究问题**：
   - **推理能力**：模型是否具备真实的推理能力，或只是依赖模板？
   - **隐藏推理过程**：模型在解决问题时的内部推理过程是什么？
   - **与人类的推理差异**：模型解决数学问题的方式是否与人类相似？
   - **泛化能力**：在GSM8K类数据集上训练的模型是否能超出该基准，发展出更广泛的推理能力？
   - **错误原因**：模型在推理错误时的内在原因是什么？
   - **模型规模需求**：解决GSM8K级别数学问题需要多大的模型规模或深度？

4. **研究发现**：
   - 研究揭示了语言模型在数学问题上的多种隐性机制，提供了关于语言模型推理能力的新见解，扩展了对当前语言模型的理解。

### Part 2.2, How to Learn From Mistakes on Grade-School Math Problems
* <a href="https://arxiv.org/abs/2408.16293">Arxiv链接</a>
* <a href="./physics_in_language_models/2408.16293v1.pdf">查看PDF</a>
#### 摘要提取

1. **研究背景**：
   - 语言模型在推理任务中表现优异，但仍会出现推理错误。当前研究多关注于通过多轮提示引导模型自我纠正，以提升推理准确性。

2. **研究目标**：
   - 探讨将“错误纠正”数据直接融入预训练阶段的效果，即预训练数据包含错误步骤和紧随其后的纠正步骤，以提高模型推理准确性。

3. **方法与实验**：
   - 使用合成的数学数据集，包含错误步骤及其后续纠正步骤的预训练数据。结果显示，这类数据在简单自回归模式下比使用无错误数据的预训练表现更高的推理准确性。

4. **关键分析**：
   - 进一步分析了多个因素的影响，包括：
     - 该方法与束搜索（beam search）的区别。
     - 错误纠正数据的准备方法。
     - 是否需要对错误部分进行掩码。
     - 所需的错误数据量。
     - 该方法是否适合推迟到微调阶段。

5. **研究意义**：
   - 研究表明，将错误纠正数据直接用于预训练，可以有效提升语言模型的推理能力，为模型改进提供新的思路。


###  Part 3.1, Knowledge Storage and Extraction
* <a href="https://arxiv.org/abs/2309.14316">Arxiv链接</a>
* <a href="./physics_in_language_models/2309.14316v3.pdf">查看PDF</a>

#### 摘要提取
1. **研究背景**：
   - 大型语言模型（LLMs）可以存储大量世界知识，通常可以通过问答的方式提取。然而，问题在于：模型是通过训练时遇到的相似问题“作弊”式回答，还是通过真正学习知识来源（如Wikipedia）来回答？

2. **研究方法**：
   - 使用控制的传记数据集，分析训练数据多样性与知识提取能力的关系。

3. **主要发现**：
   - 模型准确提取知识需要在预训练时进行充分的多样化（例如，通过改写、句子重排、翻译等），否则知识可能会被记住但无法提取，导致准确率为0%。
   - 几乎线性的探测分析表明，模型的知识编码方式会影响其知识提取能力：知识可以线性编码在实体名称的隐藏表示中，也可以分散在其他训练文本的词嵌入中。

4. **建议**：
   - 为增强知识提取能力，建议在预训练阶段：
     1. 使用小型辅助模型对预训练数据进行知识增强改写。
     2. 在预训练初期增加指令微调数据，以确保模型获得有效的知识编码。

### Part 3.2, Knowledge Manipulation
* <a href="https://arxiv.org/abs/2309.14402">Arxiv链接</a>
* <a href="./physics_in_language_models/2309.14402v2.pdf">查看PDF</a>
#### 摘要提取

1. **研究背景**：
   - 尽管语言模型存储了大量事实知识，但其在灵活应用这些知识（如通过指令微调用于下游任务）方面能力有限。

2. **研究目标**：
   - 分析四种知识操作任务对语言模型的要求，包括：
     - **知识检索**（直接提取信息，如“某人的属性X是什么？”）
     - **分类**（判断信息属性，如“属性X是奇数还是偶数？”）
     - **比较**（属性大小比较，如“某人属性X大于某人B的属性X吗？”）
     - **逆向搜索**（反向查找信息，如“哪个人的属性X等于T？”）

3. **主要发现**：
   - **知识检索**：语言模型在直接知识检索上表现良好。
   - **分类和比较**：模型在分类和比较任务上表现不佳，除非在训练和推理时使用连锁推理（Chain of Thoughts, CoTs）。
   - **逆向搜索**：模型在逆向知识搜索任务中的准确率几乎为0%，即使更改提示（prompts）也无明显改善。

4. **研究贡献**：
   - 通过合成数据集进行的受控实验表明，这些弱点是语言模型的固有缺陷，即使在知识已完全存储的情况下，模型仍难以高效操作知识。
   - 这些发现适用于包括GPT-4在内的现代预训练语言模型，并提示了设计新的图灵测试以区分人类与现代人工智能的必要性。

### Part 3.3, Knowledge Capacity Scaling Laws
* <a href="https://arxiv.org/abs/2404.05405">Arxiv链接</a>
* <a href="./physics_in_language_models/2404.05405v1.pdf">查看PDF</a>

#### 摘要提取

1. **研究背景**：
   - 扩展定律描述了语言模型规模与其能力的关系。不同于通过损失或基准测试来评估模型能力的研究，该研究通过**估算模型所存储的知识比特数量**来分析模型的知识存储容量。

2. **研究方法**：
   - 以Wikipedia等数据源中的事实知识元组（如(USA, capital, Washington D.C.)）为基础，通过多个控制数据集验证语言模型的知识存储上限。

3. **主要发现**：
   - **知识存储上限**：语言模型每个参数最多存储2比特的知识，甚至在量化至int8的情况下也是如此，且这些知识可以灵活地用于下游应用。
   - **知识容量**：例如，一个拥有70亿参数的模型可以存储140亿比特的知识量，理论上超过整个英文维基百科和教科书的知识总量。

4. **其他关键结果**：
   - **影响因素**：12项结果揭示了训练时长、模型架构、量化、稀疏性约束（如MoE）以及数据信噪比如何影响模型的知识存储容量。
   - **模型架构影响**：GPT-2架构结合旋转嵌入，在较短训练时间下匹配或超过LLaMA和Mistral架构的知识存储表现，主要原因是后者的GatedMLP结构较不稳定、训练难度更大。
   - **数据优化策略**：在训练数据前加入域名标签（如“wikipedia.org”）可显著提升模型的知识存储能力，模型可以自主识别和优先处理含有丰富知识的域，从而优化存储效率。


