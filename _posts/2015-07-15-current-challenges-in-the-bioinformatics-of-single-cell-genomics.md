---
published: ture
layout: post
title: "目前单细胞基因组、转录组分析中产生的生物信息学问题"
author: Yu
categories: 论文笔记
tags:
- 单细胞
- 基因组
- 转录组
- 生物信息学
---

He Jiankui老师组在去年年初总结了一下目前单细胞基因组学、转录组学分析中的生物信息学问题。
<u>说白了，就是数据的去噪<\u>，如何在实验以及分析方法上进行改进。
做单细胞数据分析的人可以先从这篇文章入手，了解单细胞测序存在的问题，并在分析自己的数据时带着这些问题去研究，看看如何检测判断，或者发现、发明新的方法处理。

### 从单细胞中能看到什么

我们想知道毗连的细胞在遗传和表达层面有什么差异。在人类胚胎干细胞的不同发育阶段细胞之间有什么不同。这些都是单细胞的异质性情况。

### 现在什么研究中会用到单细胞测序

1. 人类胚胎干细胞分化特点
2. 稀有的转录本分析
3. 肿瘤CTC细胞
4. 肿瘤异质性和微进化
5. 在不好培养的微生物方面研究中

### 单细胞技术集中的两个问题

1. genome coverage低
2. 扩增有偏好性

## 第一部分：单细胞DNA测序

### Allele dropout 

测序数据在基因组覆盖率低会造成SNP脱扣（SNP Dropout）。

在某些文献中MDA的脱扣率高达65%[1]

### SNP假阳性

MALBAC假阳率比MDA高。

### 找寻SNP的算法需要做到什么

1. 需要将SNP和扩增错误分开
2. 能在低覆盖率的数据中找寻SNP

### CNV的扩增偏差

在单细胞CNV研究中要适当扩大bin的大小，这样可以减少mapping偏差带来计算不准确（用reads count来算CNV的时候）。

### 计算CNV的算法要注意什么

MDA方法在计算CNV时，会有序列重复问题，在染色体终端也有问题，GC高的地方也有偏差。（MDA-induced copy number biases were reported to associate with sequence repeats and proximity to chromosome ends, increased GC content and annotated CNVs）

对扩增产物的pairewise comparison可以帮助减少假的CNV。

## 第二部分： 单细胞RNA测序

可以用来研究CTC表达量。

**RSEM这个软件可以计算expression level of TPM(transcripts per million)**

在单细胞全转录本扩增时会产生的问题有：

1. 扩增无法得道完整的cDNA片段
2. 转录本的扩增效率不一致
3. 低表达量的转录本难以被检测到

文章中还说道FPKM/RPKM没有考虑转录本间的偏差，所以不适合用在单细胞的计算中。（<u>我没看明白这是为什么</u>）

对于单细胞转录本表达情况的定量分析，文章中提出了两点建议：由于在3'和5'端测序质量不好，所以在做标准化时不要根据转录本的长度计算而是根据覆盖度范围内的长度进行计算；用一些方法（机器学习之类的）研究扩增偏差和正常情况的区别，开发新的工具来减少计算时的扩增偏差。

## 第三部分：单细胞能研究哪些问题

说白了，还是开头说的那些内容，一个是肿瘤演化谱系，另一个是干细胞发育。