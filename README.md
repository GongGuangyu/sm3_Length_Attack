# sm3_Length_Attack
   1.随机生成一个secret，算出secret的hash值
   2.根据hash值推出第一次压缩之后各个寄存器里的值
   3.在secret+padding之后附加一段消息，用上一步寄存器里的值作为IV去加密附加的那段消息，得到hash
   4.用sm3去加密secret+padding+m'，得到hash
   5.第3步和第4步得到的hash值应该相等
