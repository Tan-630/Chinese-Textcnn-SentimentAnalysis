## Textcnn 中文车评情感分类
在Colab上使用pytorch搭建textcnn网络实现中文评价情感分类

## 使用的库
* torchtext==0.6.1
* jieba==0.39

## 词向量
https://github.com/Embedding/Chinese-Word-Vectors<br>

## 训练
```bash
python3 main.py
```

## Colab上实现结果
- [x] CNN-rand 随机初始化Embedding
    ```bash
      python main.py
    ```
    >
        Batch[2900] - loss: 0.002291  acc: 100.0000%(128/128)
        Evaluation - loss: 0.000028  acc: 94.6143%(6623/7000)
        early stop by 1000 steps, acc: 94.6143%

## 不同词向量训练方式
- [x] CNN-static 使用预训练的静态词向量
    ```bash
      python main.py -static=true
    ```

- [x] CNN-non-static 微调预训练的词向量
    ```bash
      python main.py -static=true -non-static=true
    ```

- [x] CNN-multichannel 微调加静态
    ```bash
      python main.py -static=true -non-static=true -multichannel=true
    ```

