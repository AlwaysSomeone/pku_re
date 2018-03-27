# pku_re
## 概览
- train.txt:一共20万条数据,训练10个epoch,每一个step喂入50个数据,200000/50*10=40000,一共训练40000次
- test.txt:一共55610条数据,解释了test_GRU.py里的big_num为5561,一次送入十分之一
## train
### 统计
- unknow 75056
- 夫妻 35193
- 父母 27555
- 好友 3111
- 合作 13399
- 亲戚 1898
- 情侣 7854
- 上下级 2591
- 师生 8002
- 同门 2613
- 兄弟姐妹 11620
- 祖孙 1943
### 其他
- 对两实体及关系去重(实体1，实体2，关系三个均相同则删去),剩下48212条
- 也存在一个句子包含多个实体对且实体对不同种关系的情况
- 也存在很多内容与结构相似的句子
- 同一对实体，有多个实例句子，但同一对实体间的关系是一致的
## test
### 统计
- uknow 21434
- 夫妻 9977
- 父母 7853
- 好友 875
- 合作 3727
- 亲戚 519
- 情侣 2248
- 上下级 691
- 师生 2367
- 同门 755
- 兄弟姐妹 3350
- 祖孙 582
### 其他
- 其他特征与训练数据基本一致
## bug
- ValueError: Found input variables with inconsistent numbers of samples: [285252, 244684]
