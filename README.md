随着日趋复杂的海洋权益保护行动的进行，海面态势感知显得尤为重要，舰船舷号识别就是其关键技术之一，然而目前没有公开数据提供支持，主要由于（1）舰船舷号属于海洋领域相关内容，获取难度较大；（2）当前相关的自然场景文本数据集均与舰船舷号数据存在较大偏差，很难泛化到舰船舷号识别任务中；（3）对舰船舷号识别研究的人还不多，相关数据相对不多。为此，本文构建了一个真实场景下的稀疏舰船舷号数据集(sparse ship hull number dataset in real scene，SSHN-RS)，包含3004张舰船图像，共计11328个舷号字符，覆盖了多国、各类、水平、倾斜、简单背景、复杂背景、光线不佳和被遮挡等多样且复杂的舰船舷号，是一个具有挑战性的数据集。下列为SSHN-RS多样性文本举例：
![image](Dataset/多样性.jpg)





详细的数据库构建如下：
1.数据采集和处理：从互联网视觉数据库中进行了数据采集。考虑到数据集的多样性，本文针对性地选择不同场景、不同视角、不同国家、不同类型和不同密集度的舰船舷号图片。然而，本文在数据采集的过程中遇到了很多问题：(1)部分舰船图像不包含舷号文本；(2)多数图片含有水印和网站等干扰噪声；(3)较多图片像素过低，舷号极度模糊。因此人工进行


如果需要进行相关研究，请联系：cbcbingchuan@sina.com

![image](Dataset/117.jpg)
