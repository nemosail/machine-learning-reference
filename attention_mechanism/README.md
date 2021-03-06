# Attention Mechanism 论文选读

## 综述博客

- [Embed, encode, attend, predict: The new deep learning formula for state-of-the-art NLP models](https://explosion.ai/blog/deep-learning-formula-nlp)

---

## 近期论文

- [A Focused Dynamic Attention Model for Visual Question Answering](https://arxiv.org/abs/1604.01485)
    - 2016.04
    - Multimodal Representation Fusion, 动态 attention

- [Attention Correctness in Neural Image Captioning](https://arxiv.org/abs/1605.09553)
	- 2016.05
	- 对 NIC 的 attention 改进

- [Sequence to Sequence Learning as Beam-Search Optimization](https://arxiv.orCg/abs/1606.02960)
	- 2016.06
	- ?

- [Neural Machine Translation with Recurrent Attention Modeling](https://arxiv.org/abs/1607.05108)
	- 2016.07
	- 把历史的 attention activation 也考虑进去

- [Can Active Memory Replace Attention?](https://arxiv.org/abs/1610.08613)
	- 2016.10
	- 探讨了 attention mechanism 和 memory network 之间的关系

- [Paying More Attention to Attention: Improving the Performance of Convolutional Neural Networks via Attention Transfer](https://arxiv.org/abs/1612.03928)
    - CNN attention

- [A Structured Self-attentive Sentence Embedding](https://arxiv.org/abs/1703.03130)
	- 2017.03
	- 用 LSTM 做 sentence embedding 的时候，把所有的 hidden state 映射成一个 attention 
    - 权重，乘上后得到句子的 embedding 表示，这里的 attention 是一个矩阵

- [Visual Question Answering with Question Representation Updata(QRU)](https://papers.nips.cc/paper/6261-visual-question-answering-with-question-representation-update-qru)
    - 2017 NIPs Proceedings
    - attention?
    
- [Convolutional Sequence to Sequence Learning](https://arxiv.org/abs/1705.03122)
    - 2017.05, Facebook AI Research, FAIR
    - 替代 RNN 来做序列的建模，用卷积操作来抽取特征，效果和训练速度优于 RNN 模型

- [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
    - 2017.06, Google
    - 代码参考官方实现 [tensor2tensor](https://github.com/tensorflow/tensor2tensor)
    - 讲怎么实现 transformer 的好文章，[The Annotated Transformer](http://nlp.seas.harvard.edu/2018/04/03/attention.html)
    - 抛弃了 CNN 和 RNN，直接做 multi-head attention
    - Encoder 端是 self attention，即 Q=K=V；Decoder 端是 K=V 用的 Encoder 输出，Q 是解码到当前时刻的向量。

---

## 早期论文

- [Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473)
	- 2014.09, Bahdanau，重点文章
	- 最早把 attention 用到机器翻译中的论文，可以把翻译的英文和法文对其(align)
	- 参考对应的没有 attention 的模型 [google seq2seq NMT](https://arxiv.org/abs/1409.3215)

- [Show, Atten and Tell: Neural Image Caption Generation with Visual Attention](https://arxiv.org/abs/1502.03044)
	- 2015.02
	- 把 attention 用到 Image Caption 问题上

- [Deep Sentence Embedding Using LSTM Networks: Analysis and Application to Information Retrieval](https://arxiv.org/abs/1502.06922)
	- 2015.02
	- 用 LSTM 做 sentence embedding 的时候，用 attention 检测关键词

- [Describing Multimedia Content using Attention-based Encoder-Decoder Networks](https://arxiv.org/abs/1507.01053)
	- 2015.07
	- 系统总结 CNN + gated RNN + attention 在诸多课题上的应用

- [Effective Approaches to Attention-based Neural Machine Translation](https://arxiv.org/abs/1508.04025)
    - 2015.08, [Thang Luong](https://nlp.stanford.edu/~lmthang/), Stanford NLP 小组的工作
	- Luong 的[博士论文](https://github.com/lmthang/thesis)就是做 NMT，tensorflow 上的 [nmt 教程](https://github.com/tensorflow/nmt)也是他写的。
	- 和 Bahdanau 不同的是，Attention context 是用 decoder hidden state 算出来的，此外 score function 试了多种方法。总之很推荐读，重要论文！

- [ABCNN: Attention-Based CNN for Modeling Sentence Pairs](https://arxiv.org/abs/1512.05193)
	- 2015.12
	- CNN 上的 attention
