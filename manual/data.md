# 数据
位置：/data/universal_dependency/udpipe/dcteng/  
格式：  
```cpp
- dcteng
	+ ud-treebanks-conll2017 （原始数据）
	+ e2e （End To End 结果）
	+ ppos（预测词性）
```
## 原始数据
位置：/data/universal_dependency/udpipe/dcteng/ud-treebanks-conll2017  
内容：64个数据集。  
格式：  
```cpp
- ud-treebanks-conll2017
	- UD_Ancient_Greek(数据集名称)
    	- grc-ud-train.conllu （conllu 格式训练数据）
        - grc-ud-train.txt    （训练数据的文本格式）
        - grc-ud-dev.conllu   （conllu 格式开发集数据）
        - grc-ud-dev.txt      （开发集数据的文本格式）
        - README.txt          （数据来源说明、日志等）
        - LICENSE.txt
        - stats.xml
	+ UD_Ancient_Greek-PROIEL
	+ UD_Arabic
	...
```

## End To End 结果
位置：/data/universal_dependency/udpipe/dcteng/e2e  
内容：从开发集生文本开始，完成分词和词性标注的结果，conllu 格式。  
格式：  
```cpp
- e2e
	- ar(数据集简写)
		- ar-ud-dev-e2e.conll （分词和词性标注后的结果）
		- evaluation.log （e2e 的结果）
	+ bg
	+ ca
	+ cs
	...
```

## 预测词性
位置：/data/universal_dependency/udpipe/dcteng/ppos  
内容：训练集和开发集的自动词性。
- 训练集的自动词性：使用 jackknifing 方法得到的预测词性。
- 开发集的自动词性：使用在训练集上得到的模型预测开发集的词性。

格式：  
```cpp
- ppos
	- dev
		- ar-ud-dev-ppos.conll
		- bg-ud-dev-ppos.conll
		...
	- train
		- ar-ud-train-ppos.conll
		- bg-ud-train-ppos.conll
		...
```
