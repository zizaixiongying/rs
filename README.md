# rs
remote sensing image classification with deep learing on GEE
本项目主要测试深度学习在现实场景中对遥感图像的分类性能。
利用GEE平台提供的遥感数据，并在Google Colab利用其提供的GPU进行训练，不需要本地GPU环境和遥感数据。
基本思路：
1.为了获取更多的波段信息，将Landsat 8和Sentinel-2进行融合，每个像元有88各波段。
2.使用NLCD2016作为标签，去除分布很少的类别并对部分类别进行合并，最后对14种地物类别进行分类。
3.为了测试模型的泛化性能，训练样本和测试样本在美国本土不同的区域进行选择。并且各类的训练样本和测试样本数量规模基本一致。
4.随机选取四块区域用训练好的模型进行分类，与NLCD2016进行对比，查看分类效果。
代码使用流程：
1.注册GEE
2.在Google Colab中调用GEE编写代码（需要开通Google云存储功能，实验结果要保存在这里）
3.编写代码，选择GPU运行
4.在GEE中打开Coder Editer查看分类效果
