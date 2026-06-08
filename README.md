LLM & Agent Runtime：从概率模型到可靠Agent

# Part 0 前言

- 撰写本书的原因
- 为什么要学习LLM
- LLM到底是什么
- 为什么AI看起来像会思考
- 本书阅读路线

---

# Part 1 数学与信息基础

## Chapter 1 计算机如何表示世界

- 信息数字化
- ASCII
- Unicode
- 图片表示
- 音频表示
- 视频表示
- 为什么最终都是0和1

## Chapter 2 概率是什么

- 随机事件
- 条件概率
- 联合概率
- 贝叶斯思想
- LLM实际上在计算什么

## Chapter 3 向量是什么

- 二维向量
- 高维向量
- 距离
- 方向
- 相似度

## Chapter 4 Embedding为什么有效

- Token Embedding
- Semantic Space
- Cosine Similarity
- Context决定意义
- 多义词问题

---

# Part 2 Transformer基础

## Chapter 5 NLP的发展历史

- Rule-based
- Statistical NLP
- RNN
- LSTM
- Attention
- Transformer
- GPT时代

## Chapter 6 Tokenizer

- Token是什么
- BPE
- SentencePiece
- 中文Token
- 英文Token

## Chapter 7 Transformer整体结构

- Input
- Embedding
- Position Encoding
- Attention
- Feed Forward
- Layer Stack
- Output

## Chapter 8 Attention机制

- 为什么需要Attention
- Query
- Key
- Value
- Self Attention
- Cross Attention

## Chapter 9 为什么叫Transformer

- Representation Transformation
- Feature Space
- 多层抽象

## Chapter 10 Auto-Regressive模型

- Next Token Prediction
- 为什么一步一步生成
- Chain of Probability

---

# Part 3 模型训练

## Chapter 11 Pretraining

- Corpus
- Tokenization
- Loss
- Gradient
- Optimization

## Chapter 12 Loss Function

- Loss是什么
- Cross Entropy
- 为什么Loss越低越好

## Chapter 13 Gradient与优化

- 梯度
- Gradient Descent
- 参数更新

## Chapter 14 GPU为什么重要

- Matrix Multiplication
- Parallel Computing
- Memory Bandwidth

## Chapter 15 Alignment

- SFT
- RLHF
- Preference Optimization
- DPO
- RLAIF

---

# Part 4 推理(Inference)

## Chapter 16 Prompt组成

- System Prompt
- Developer Prompt
- User Prompt
- Conversation History

## Chapter 17 Context Window

- Context长度
- Sliding Window
- Memory限制

## Chapter 18 Hallucination

- 为什么会幻觉
- 概率模型与事实
- 高概率≠真实性

## Chapter 19 Temperature

- Temperature
- Creativity
- Determinism

## Chapter 20 Sampling

- Top-k
- Top-p
- Beam Search（可选）

---

# Part 5 Tool Use

## Chapter 21 Function Calling

- Tool Calling
- Schema
- 参数生成

## Chapter 22 MCP

- MCP思想
- Tool协议
- Resource
- Prompt

## Chapter 23 Tool Selection

- Planner
- Tool Routing
- Tool Choice

## Chapter 24 Structured Output

- JSON
- XML
- Schema Validation
- Constraint

---

# Part 6 Agent

## Chapter 25 Chatbot vs Agent

- 回答问题
- 完成任务

## Chapter 26 Planning

- Goal
- Plan
- Execute
- Observe

## Chapter 27 ReAct

- Thought
- Action
- Observation

## Chapter 28 Memory

- Short Memory
- Long Memory
- Vector DB
- Summary Memory

## Chapter 29 Multi-Agent

- Manager
- Worker
- Reviewer
- Executor

## Chapter 30 Runtime Engineering

- State
- Context
- Retry
- Timeout
- Budget
- Guardrail
- Rollback
- Checkpoint

---

# Part 7 Reliability

## Chapter 31 为什么LLM不能负责稳定性

- Decision vs Execution
- Probabilistic Model
- Deterministic Runtime

## Chapter 32 Harness Engineering

- Harness
- Sandbox
- CI
- Git
- Docker

## Chapter 33 Eval Engineering

- Offline Eval
- Online Eval
- Regression
- Golden Dataset
- LLM Judge
- Tool Success
- Mission Success

## Chapter 34 为什么传统测试不足

- Input/Output
- Trajectory
- Outcome
- Non-determinism

## Chapter 35 Mission Lock

- Goal Drift
- Tool Drift
- Context Pollution
- Self-trajectory Lock-in

---

# Part 8 Future

## Chapter 36 Prompt Engineering的未来

- Prompt作为配置
- Runtime作为核心

## Chapter 37 Agent OS

- Agent调用Agent
- Skill
- Workflow
- Capability Graph

## Chapter 38 Runtime > Model

- Model
- Runtime
- Tool
- Data
- Eval

## Chapter 39 Eval-driven Development

- Eval First
- Continuous Eval
- Regression Prevention

## Chapter 40 总结

- LLM本质
- Agent本质
- Runtime本质
- 未来趋势
