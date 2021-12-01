随着日趋复杂的海洋权益保护行动的进行，海面态势感知显得尤为重要，舰船舷号识别就是其关键技术之一，然而目前没有公开数据提供支持，主要由于（1）舰船舷号属于海洋领域相关内容，数据获取难度较大；（2）当前相关的自然场景文本数据集均与舰船舷号数据存在较大偏差，很难泛化到舰船舷号识别任务中；（3）对舰船舷号识别的研究尚不多，相关数据相对较少。为此，本文构建了一个真实场景下的稀疏舰船舷号数据集(sparse ship hull number dataset in real scene，SSHN-RS)，包含3004张舰船图像，共计11328个舷号字符，覆盖了多国、各类、水平、倾斜、简单背景、复杂背景、光线不佳和被遮挡等多样且复杂的舰船舷号，是一个具有挑战性的数据集。下列为SSHN-RS多样性文本样例：

<img src="https://github.com/Bingchuan897/SSHN-RS/blob/main/Dataset/%E5%A4%9A%E6%A0%B7%E6%80%A7.png" width="800" height="600">

SSHN-RS数据库构建主要分为如下步骤：

1.数据采集和处理：本文从互联网视觉数据库中进行了数据采集，但在数据采集的过程中遇到了很多问题：(1)部分舰船图像不包含舷号文本；(2)多数图片含有水印和网站等干扰噪声；(3)较多图片像素过低，舷号极度模糊，如下图所示。因此为了确保数据质量，本文通过手动调整的方式对收集的数据进行了精细筛选，主要剔除不含舷号和像素过低的图像，并去除干扰噪声。

<img src="https://github.com/Bingchuan897/SSHN-RS/blob/main/Dataset/%E9%87%87%E9%9B%86%E9%97%AE%E9%A2%98%E5%9B%BE%E7%89%87.png" width="700" height="150">

2.数据标注：按照COCO数据集的格式进行标注。如下图所示。使用开源标注工具LabelMe对36个舰船舷号子类进行语义标注，标注方式为人工标记，标注结果保存文件为json格式。

<img src="https://github.com/Bingchuan897/SSHN-RS/blob/main/Dataset/%E6%A0%87%E6%B3%A8%E6%B5%81%E7%A8%8B.png" width="700" height="120">

同时，根据所有样本属性，定义了8类样本，分别为小舷号样本、正常舷号样本、大舷号样本、倾斜舷号样本、模糊舷号样本、近岸舷号样本、远海舷号样本、被遮挡舷号样本。并对其进行分类标注。标注结果如下图所示。

<img src="https://github.com/Bingchuan897/SSHN-RS/blob/main/Dataset/%E6%A0%87%E6%B3%A8%E6%A0%B7%E4%BE%8B.png" width="500" height="150">

3 数据集配置与统计
SSHN-RS数据集包含3004张舰船舷号图片，训练集分配898个舷号的图像，测试集分配2106张舷号的图像，各字符分布如下图所示。

<img src="https://github.com/Bingchuan897/SSHN-RS/blob/main/Dataset/%E5%AD%97%E7%AC%A6%E7%BB%9F%E8%AE%A1.png" width="900" height="300">




该数据集不仅可以作为舰船舷号识别研究的数据支撑，也可用于舰船检测和三维位姿估计等方面的研究，促进相关领域的发展。
如果需要进行相关研究，请联系：cbcbingchuan@sina.com获取。




