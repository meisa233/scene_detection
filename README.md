# Scene Detection

### Title: Optimally Grouped Deep Features Using Normalized Cost for Video Scene Detection
---
使用Normalized Cost优化分组的深度特征
#### ABSTRACT
>
目标：得到将连续镜头组合成场景的最优分组<br />
创新：提出了一种normalized cost function<br />
两个好处：(1)提供了从镜头到场景的时间一致性的分析；(2)parameter-free, eliminating the need for fine-tuning for different types of content.
#### INTRODUCTION
>
场景的定义：Formally, scenes are defined as a sequence of semantically related and temporally adjacent shots depicting a high-level concept or story.
聚类方法的坏处：忽略了时间一致性(temporal consistency)，容易将不连续的镜头聚类成一个场景
>
这篇论文将将场景分割问题看做最优分割任务（使用神经网络更好地捕捉语义）
>
Overview:给定视频，运行镜头边界检测算法，并且从每个镜头中提取到有表现力的特征向量(extract a representative feature vector from each shot)，从而能够计算镜头之间的距离。我们提出Normalized cost functionyong将其看做是一个优化问题。通过最小化cost function从而获得将场景的最优分割。
>
这个方法是**parameter-free**的，从而避免了需要根据不同内容微调的情况。
>
#### PREVIOUS WORK
>
聚类方法：使用标准聚类技术对镜头（描述符）进行聚类
>
图形方法：将视频看做连通图，并采用Graph Cuts或者Dominant sets的方法检测视频的场景边界。
TODO
>
