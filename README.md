# G-Research
Google research...

##ImageNet

## youtube-8M
8 million youtube URL, 0.5 million hours video, 1.9 billion frame Features.

解决了两个问题
###人工标注所需时间远远大于图像标注的时间
使用youtube video annotation system
###视频的处理和存储的计算成本非常高
为了让计算资源有限的研究者用上这个数据集，对视频进行了预处理并使用了在ImageNet上训练的公开可用的Inception-V3图像标注模型（一种目前最佳的深度学习模型）提取了帧层面的特征（frame-level features）。这些特征是按每秒一帧的时间分辨率从19亿个视频帧中提取的，然后被压缩到小于1.5TB。这使得可以在单个GPU上只用低于一天的时间全规模地下载该数据并完成基准的TensorFlow模型的训练。
