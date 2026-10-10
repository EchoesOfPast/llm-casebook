# N002 “一读就知道是 AI 写的”：那种说不出的别扭是什么

> 笔记记录的是讨论中形成的想法和假设，并对照了已有研究。标 ✅ 的有研究支持，⚠️ 的被研究修正，❓ 的尚无证据。

## 现象

作者和小说平台的编辑都有同样的体验：AI 写的东西，读一下就能感觉出来。但要说具体哪里不对，说不上来，只觉得“玄之又玄”。这种感觉更像身体上的别扭，而不是对照某个标准得出的判断。

## 一、说不出来，不等于神秘

认得出一张熟悉的脸，却说不出它和别的脸差在哪；听得出外地口音，却列不出哪个音发得不对。哲学家波兰尼称之为“默会知识”：我们知道的，比我们说得出的多。

长期大量阅读的人，已经把“人写的文字是什么样”沉淀进了感觉里。文字一偏离，身体先察觉，语言还没跟上。

这也有点像“恐怖谷”：很像人、又不完全像人的东西，会让人本能地不舒服。❓ 这只是类比，目前没有找到直接研究文字的“恐怖谷”证据。

## 二、这种感觉是练出来的 ✅

Russell、Karpinska、Iyyer（ACL 2025）让人阅读 300 篇英文非虚构文章，判断是人写的还是 AI 写的，并写下理由：

- 经常用 AI 写作的人，不需要专门训练就能认得很准。5 位这样的“专家”多数投票，300 篇只判错 1 篇；文本经过改写、“人性化”处理后依然准确。
- 他们大量依赖“AI 词汇”，也会注意正式程度、原创性、清晰度等更复杂的特征，而这些正是自动检测器难以把握的。

所以这种感觉是可以习得的感知，接触得越多越准。局限：研究对象是英文非虚构文章，不是中文小说。

## 三、它察觉到的是什么：两个假设

### 假设 A：所有 AI 共享同一个声音 ✅

人写坏的文字各有各的坏法，AI 的坏法都一样。看得多了，一眼就能认出来。

同质化研究支持这一点：
- Moon 等（2025）分析 2,200 篇大学申请文书，每多一篇人写的文书带来的新想法，多于每多一篇 GPT-4 写的文书。
- Anderson 等（2024）发现，用 ChatGPT 的人各自产出的想法更多，但整个群体更趋同。
- 多项研究发现，模型写的故事彼此之间比人写的故事更相似。

### 假设 B：单篇文字处处“均匀” ⚠️

人写东西是不均匀的：在乎的地方写很多，不在乎的一笔带过；句子长短参差；会反复用偏爱的词。AI 的文字则处处均匀：每个句子都完整，每个人物分到差不多的笔墨。[失败模式清单](../../scenarios/fiction/failure-modes.md) 里的流水账（F17）、死细节（F06）、无功能修饰（F18），本质上都是“均匀用力”。所以那种别扭，可能是身体在说：这里没有人在乎。

**但这一点证据很弱：**
- 常被引用的检测指标 perplexity（可预测度）和 burstiness（句子长短的起伏），GPTZero 从 2023 年起就不再作为主要检测手段；以句长变化区分人机写作，目前没有找到同行评审的验证。
- Liang 等（2023）发现，检测器把非英语母语者的作文误判为 AI 的比例平均达 61.3%，因为他们的语言本来就更简单、更可预测。可见“规整、可预测”并不只属于 AI。

## 四、这种感觉也会出错

本身写得规整、平均的人类文字，可能被当成 AI；人们也更容易记住认出来的那几次。

## 五、待做：不用说出来，只要能指出来

直觉说不清，但可以被定位：

1. 取一段让人别扭的 AI 文字。
2. 生成若干变体，每个只改一个维度（只改节奏、只改用力是否均匀、只改用词等），其余不动。
3. 读者不需要解释，只标出哪个版本还别扭、哪个不别扭了。
4. 多轮之后，统计哪些维度的改动最能消除别扭感。

这个实验可以直接检验假设 B。

## 参考

- Russell, Karpinska & Iyyer (2025). [People who frequently use ChatGPT for writing tasks are accurate and robust detectors of AI-generated text](https://aclanthology.org/2025.acl-long.267). ACL 2025.
- Moon et al. (2025). [Homogenizing Effect of Large Language Models on Creativity](https://scale.stanford.edu/ai/repository/homogenizing-effect-large-language-models-llms-creative-diversity-empirical).
- Anderson, Shah & Kreminski (2024). Homogenization Effects of Large Language Models on Human Creative Ideation. Creativity & Cognition 2024.
- [Do Large Language Models Always Tell The Same Stories?](https://arxiv.org/abs/2606.17350) (2026 预印本).
- Liang et al. (2023). GPT detectors are biased against non-native English writers. *Patterns*.
- GPTZero. [How do I interpret burstiness or perplexity?](https://support.gptzero.me/hc/en-us/articles/15130070230551-How-do-I-interpret-burstiness-or-perplexity)
