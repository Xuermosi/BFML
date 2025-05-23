# 基于 Tape-Bert 的蛋白质多标签分类模型

**描述**：该项目旨在构建一个用于蛋白质多标签分类的深度学习模型，基于 Tape-Bert 架构进行设计与优化，具体包含以下内容：
- 蛋白质语言模型模块：以蛋白质序列作为输入，通过嵌入层将序列转化为低维向量，再经 12 个编码器层堆叠提取特征，输出特定维度的向量表示，为后续处理奠定基础。
- TextCNN 模块：接收蛋白质语言模型输出的向量，运用多个不同卷积核大小的卷积操作，高效提取文本特征，进一步挖掘数据中的关键信息。
- Transformer 解码器模块：以蛋白质语言模型输出作为 Value 和 Key，并结合可学习的标签嵌入，通过多头自注意力、多头交叉注意力、相加与归一化及前馈神经网络等操作，输出与标签数量相关的特征向量。
- 分类模块：将 TextCNN 模块与 Transformer 解码器模块的输出进行拼接，再通过两个全连接层逐步映射，最终输出对应批量大小和标签数量的分类结果，实现蛋白质的多标签分类任务。

**技术栈**：
1. 基于 Tape-Bert 架构进行深度学习模型搭建，充分利用其在蛋白质序列处理方面的优势。
2. 运用卷积神经网络（TextCNN）进行特征提取，增强模型对文本特征的捕捉能力。
3. 采用 Transformer 架构的解码器部分，结合多头注意力机制等，有效处理特征信息，提升模型性能。
4. 通过全连接层实现最终的分类任务，将特征映射到具体的分类标签上 。 
