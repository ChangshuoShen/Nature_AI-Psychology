我们可以探究大模型的哪些能力？
* 知识广度和信息整合——这点条过
* 推理与决策——现在一直在攻关的事情,Chain of Thought等技术的提出
* 语言理解与生成——理解专指一些复杂的语言情境、隐喻、幽默等方面
* 情感识别与共情——情感识别可能已经有不错的进展，但是回应情感需求呢？
* 适应性和自我改进、自我学习——能否像人类一样灵活适应新环境？“自主学习”新知识和策略？
* 伦理和价值判断——LLM在应用于敏感场景的局限性

* LLM是否具有`心智`？
* LLM是否具有拟人的情感？
* LLM是否具有记忆能力，推理能力，情感感知能力

从这一篇“nature human behavior”出发
### Testing `theory of mind` in large language models and humans
在LLM和人类中检测心理理论
- [./papers/s41562-024-01882-z](./papers/s41562-024-01882-z.pdf)
#### 摘要提取
1. **研究主题**：探索大语言模型（LLMs），如ChatGPT和LLaMA2，在心智理论(Theory of Mind)任务中的表现，研究其与人类在理解他人心理状态上的可比性。
2. **测试内容**：研究中使用了两个不同的LLM模型(GPT-4和LLaMA2)进行了一系列理论推理测验并和人类参与者做比较，研究选择了四个理论心理学测试：
    * 错误观念
    * 间接请求
    * 讽刺
    * 社交失误(faus pas)
3. **研究结果**：
   - GPT-4在间接请求、错误信念和误导理解方面的表现与人类相当，甚至在某些方面优于人类。
   - LLaMA2在辨别社交失误的测试中优于人类，但这种优势可能是由于其偏向于将情境解读为无知而产生的假象。
   - GPT模型在推理时较为保守，表现出一种“超保守”倾向，导致其在一些推理任务中不愿轻易得出结论。
4. **研究意义**：研究表明，LLMs的推理输出与人类推理相似，但要确保两者的比较具有实质性，需要进行系统化的测试和深入分析。

#### 一句话
这篇是在探索现有的大模型在做判断的时候(思维理论方面)“像不像人”，结果是一些方面差不多，但是一些方面因为模型本身的特质，比如“GPT-4推理时超保守”，“LLaMA2可能偏向将情景解读为无知而在辨别社交失误的测试中优于人类”？得到这些模型比较像人，但是有偏？
#### 细读
Theory of Mind: The ability for tracking other people's mental states
theory of mind refers to an interconnected set of notions that are combined to explain, predict, and justify the behaviour of others.

In the service of the broader multidisciplinary study of machine behaviour, there have been recent calls for a ‘machine psychology’ that have argued for using tools and paradigms from experimental psychology to systematically investigate the capacities and limits of LLMs. 

检索的一些结果
* A large-scale examination of inductive biases shaping high-level visual representation in brains and machines
    * 对塑造大脑和机器高级视觉表示的归纳偏差进行大规模检查
    * <a href="https://www.nature.com/articles/s41467-024-53147-y">链接</a>
    * <a href="./llm_and_human_papers/s41467-024-53147-y.pdf">查看PDF</a>


* Larger and more instructable language models become less reliable
    * 更大、更易指导的语言模型变得不太可靠
    * <a href="https://www.nature.com/articles/s41586-024-07930-y">链接</a>
    * <a href="./llm_and_human_papers/s41586-024-07930-y.pdf">查看PDF</a>

* Brains and algorithms partially converge in natural language processing
    * 大脑和算法在自然语言处理中部分融合
    * <a href="https://www.nature.com/articles/s42003-022-03036-1?fromPaywallRec=false">链接</a>
    * <a href="./llm_and_human_papers/s42003-022-03036-1.pdf">查看PDF</a>

* Unmasking and quantifying racial bias of large language models in medical report generation
    * 揭露和量化医疗报告生成中大型语言模型的种族偏见
    * <a href="https://www.nature.com/articles/s43856-024-00601-z"></a>
    * <a href="./llm_and_human_papers/s43856-024-00601-z.pdf"></a>

* Large pre-trained language models contain human-like biases of what is right and wrong to do
    * 大型预训练语言模型包含类似人类的正确和错误行为偏见
    * <a href="https://www.nature.com/articles/s42256-022-00458-8">链接</a>
    * <a href="./llm_and_human_papers/s42256-022-00458-8.pdf">查看PDF</a>

* Strategic behavior of large language models and the role of game structure versus contextual framing
    * 大语言模型的策略行为以及游戏结构与上下文框架的作用
    * <a href="https://www.nature.com/articles/s41598-024-69032-z">链接</a>
    * <a href="./llm_and_human_papers/s41598-024-69032-z.pdf">查看PDF</a>

* Emergent analogical reasoning in large language models
    * 大型语言模型中的紧急类比推理
    * <a href="https://www.nature.com/articles/s41562-023-01659-w">链接</a>
    * <a href="./llm_and_human_papers/s41562-023-01659-w.pdf">查看PDF</a>

* Testing the limits of natural language models for predicting human language judgements
    * 测试自然语言模型预测人类语言判断的极限
    * <a href="https://www.nature.com/articles/s42256-023-00718-1">链接</a>
    * <a href="./llm_and_human_papers/s42256-023-00718-1.pdf">查看PDF</a>

* Comparing human text classification performance and explainability with large language and machine learning models using eye-tracking
    * 使用眼动追踪将人类文本分类性能和可解释性与大型语言和机器学习模型进行比较
    * <a href="https://www.nature.com/articles/s41598-024-65080-7">链接</a>
    * <a href="./llm_and_human_papers/s41598-024-65080-7.pdf">查看PDF</a>

* Shared computational principles for language processing in humans and deep language models
    * 人类语言处理和深度语言模型的共享计算原理
    * <a href="https://www.nature.com/articles/s41593-022-01026-4">链接</a>
    * <a href="./llm_and_human_papers/s41593-022-01026-4.pdf">查看PDF</a>

* Strong and weak alignment of large language models with human values
    * 大语言模型与人类价值观的强对齐和弱对齐
    * <a href="https://www.nature.com/articles/s41598-024-70031-3">链接</a>
    * <a href="./llm_and_human_papers/s41598-024-70031-3.pdf">查看PDF</a>

* A clarification of the conditions under which Large language Models could be conscious
    * 澄清大语言模型可以有意识的条件
    * <a href="https://www.nature.com/articles/s41599-024-03553-w">链接</a>
    * <a href="./llm_and_human_papers/s41599-024-03553-w.pdf">查看PDF</a>

* Building machines that learn and think with people
    * 构建与人一起学习和思考的机器
    * <a href="https://www.nature.com/articles/s41562-024-01991-9">链接</a>
    * <a href="./llm_and_human_papers/s41562-024-01991-9.pdf">查看PDF</a>

* Experimental narratives: A comparison of human crowdsourced storytelling and AI storytelling
    * 实验叙事：人类众包讲故事和人工智能讲故事的比较
    * <a href="https://www.nature.com/articles/s41599-024-03868-8">链接</a>
    * <a href="./llm_and_human_papers/s41599-024-03868-8.pdf">查看PDF</a>

* Language models and linguistic theories beyond words
    * 超越语言的语言模型和语言理论
    * <a href="https://www.nature.com/articles/s42256-023-00703-8">链接</a>
    * <a href="./llm_and_human_papers/s42256-023-00703-8.pdf">查看PDF</a>

* Two-faced AI language models learn to hide deception
    * 双面人工智能语言模型学习隐藏欺骗(这是一篇新闻)
    * <a href="https://www.nature.com/articles/d41586-024-00189-3">链接</a>

* Large-scale AI language systems display an emergent ability to reason by analogy
    * 大规模人工智能语言系统显示出类比推理的新兴能力(只有一页，之前看过)
    * <a href="https://www.nature.com/articles/s41562-023-01671-0">链接</a>
    * <a href="./llm_and_human_papers/s41562-023-01671-0.pdf">查看PDEF</a>

* Three reasons why AI doesn’t model human language
    * 人工智能没有模拟人类语言的三个原因(特别短，且是通讯文章)
    * <a href="https://www.nature.com/articles/d41586-024-00824-z">链接</a>
    * <a href="./llm_and_human_papers/d41586-024-00824-z.pdf">查看PDF</a>


<!-- https://www.nature.com/articles/s42256-022-00534-z 这是一篇大模型做基因注释的工作-->
<!-- https://www.nature.com/articles/s41433-023-02842-z 这个是Meta眼镜，也没关系 -->