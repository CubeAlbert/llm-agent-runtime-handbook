# 为什么要学习LLM

## 时代的转折点

如果说 LLM 正在改变世界，那么这一切的起点可以追溯到一篇论文和一个思想。

2017 年 6 月，Ashish Vaswani 等八位谷歌研究者提交了 *Attention Is All You Need*[^1]。这篇论文提出了 Transformer 架构，彻底抛弃了当时主流的 RNN 等递归结构以及 CNN 等层级结构，转而使用纯粹的 Attention 机制。这一决定的工程意义极其深远：RNN 的计算必须一步一步进行，而 Transformer 可以天然并行计算，因此模型规模不再受制于串行计算的瓶颈，可以训练到前所未有的大小。没有这一步，后面所有的故事都无法发生。

紧接着的 2018 年 6 月，OpenAI 的 Alec Radford 发表了一篇博客——*Improving Language Understanding with Unsupervised Learning*[^2]。这篇博客提出了两个核心思想。第一，**走无监督学习路线**：不依赖昂贵的人工标注，直接在海量文本上训练语言模型，再把预训练好的模型在小规模监督数据上微调。第二，**一个模型做所有事**——"can we develop one model, train it in an unsupervised way on a large amount of data, and then fine-tune the model to achieve good performance on many different tasks?" 实验给出了肯定的回答：同一个核心模型在常识推理（COPA、ROCStories）、阅读理解（RACE）等差异极大的任务上，只需极少的适配就能达到当时的最好成绩。OpenAI 自己也在这篇博客的 "Future" 章节中预言了接下来的方向："using the well-validated approach of more compute and data"——他们从一开始就知道，这条路本质上是规模问题。

在 GPT 路线确立之后，OpenAI 又回答了另一个关键问题：模型究竟能不能一直做大？2020 年发表的《Scaling Laws for Neural Language Models》[^3] 给出了答案。研究发现，随着模型参数、训练数据和计算量不断增加，模型性能的提升并不是随机发生的，而是遵循一种可以预测的规律。这意味着，大模型的发展更像是一条可以持续延伸的曲线，而不是等待下一次算法革命。从此以后，“更多的数据、更多的算力、更大的模型”不再只是一个大胆的设想，而成为整个行业共同遵循的发展路线。

沿着这条路，OpenAI 进一步验证了这一判断。同年发布的 GPT-3 将参数规模提升到 1750 亿，并展示了另一种令人惊讶的能力：很多任务不再需要重新训练模型，只需要在 Prompt 中给出几个示例（Few-shot），甚至不给示例（Zero-shot），模型就能够完成任务。对于许多任务来说，Prompt 更像是在激活模型已经学到的能力，而不是重新教会它如何完成任务。

2022 年 1 月，Google 的 Jason Wei 等人发表了 *Chain-of-Thought Prompting Elicits Reasoning in Large Language Models*[^4]。这篇论文揭示了一个重要现象：**如果要求模型把思考过程一步一步写出来，而不是直接给答案，它解决复杂问题的能力会显著提升**。一个拥有 540B 参数的模型，仅凭 8 个推理示例，就在 GSM8K 数学题集上超过了经过专门微调的 GPT-3 系统。它意味着，Prompt 不仅是在告诉模型“做什么”，还可以影响模型“怎么思考”。推理开始从一个需要重新训练的目标，变成了一个可以通过 Prompt 激发出来的能力。

2025 年初，DeepSeek 推出了 R1 推理模型[^5]，成为这一方向的重要引爆点。如果说 Chain-of-Thought 证明了合理的 Prompt 可以激发模型的推理过程，那么 R1 所代表的新一代推理模型，则进一步尝试把这种推理方式通过训练内化到模型本身。模型不再依赖用户提供完整的推理示例，而是在面对数学、编程和科学等复杂任务时，能够主动生成长链条的思考过程，并利用强化学习不断优化这种能力。从 Transformer 到 GPT-3，从 Few-shot 到 Chain-of-Thought，再到 Reasoning Model，一条清晰的线索贯穿始终：LLM 的能力，正在从“学习语言”走向“学习思考”。

[^1]: Vaswani et al., "Attention Is All You Need", arXiv:1706.03762, 2017.  
[^2]: Alec Radford, "Improving Language Understanding with Unsupervised Learning", OpenAI Blog, 2018.  
[^3]: Kaplan et al., "Scaling Laws for Neural Language Models", arXiv:2001.08361, 2020.  
[^4]: Wei et al., "Chain-of-Thought Prompting Elicits Reasoning in Large Language Models", arXiv:2201.11903, 2022.  
[^5]: DeepSeek-AI, "DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning", arXiv:2501.12948, 2025.  

## LLM不是魔法

## 从使用者到构建者

## 工程能力的代际跃迁
