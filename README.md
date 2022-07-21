# 简介
其中ConstParameters.py存储sm3常量 main.py实现sm3以及长度扩展攻击
# sm3_Length_Attack
   1.随机生成一个secret，算出secret的hash值  
   2.根据hash值推出第一次压缩之后各个寄存器里的值  
   3.在secret+padding之后附加一段消息，用上一步寄存器里的值作为IV去加密附加的那段消息，得到hash  
   4.用sm3去加密secret+padding+m'，得到hash  
   5.第3步和第4步得到的hash值应该相等  
# 代码中有思路和解释
![image](https://user-images.githubusercontent.com/105531474/180178703-615f95c3-e14b-4e1a-8587-200d89e746bd.png)
# 实验结果
![image](https://user-images.githubusercontent.com/105531474/180178981-57447d62-6ded-4de3-b541-34b3daee36ae.png)
