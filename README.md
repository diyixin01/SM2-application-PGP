# SM2-application-PGP



# PGP简介

PGP(Pretty Good Privacy)，是一个基于RSA公钥和对称加密相结合的邮件加密软件。该系统能为电子邮件和文件存储应用过程提供认证业务和保密业务。


PGP是个混合加密算法，它由一个对称加密算法、一个非对称加密算法、与单向散列算法以及一个随机数产生器（从用户击键频率产生伪随机数序列的种子）组成。



# 实验过程

通话双方提前协商好一对SM2公私钥对（pk_r,sk_r），消息发送方生成一个随机AES对称加密密钥K，用K加密消息M，同时用pk_r加密K，和加密后的消息一并发送给接收方。 接收方收到后，用sk_r解密得到K后，再解密得到消息M。其中（pk_r,sk_r）的生成直接调用ECMH_project.py中的定义。





![image](https://user-images.githubusercontent.com/75195549/180394343-b0b60317-1527-4465-bdc7-136696d22849.png)






实验结果如图：




![image](https://user-images.githubusercontent.com/75195549/180399808-d8e17d1b-1435-4bfb-a3c0-33e96de74314.png)



用SM2进行PGP比用RSA快很多（即使不计时也能感觉出来）


这是用RSA利用口令实现的PGP通讯，比SM2的要慢：




![image](https://user-images.githubusercontent.com/75195549/180400546-3055c3b3-9ef0-4cda-8df0-549a69869143.png)





