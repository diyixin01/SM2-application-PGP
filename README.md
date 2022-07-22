# SM2-application-PGP
内含简单实验报告




通话双方提前协商好一对SM2公私钥对（pk_r,sk_r），消息发送方生成一个随机AES对称加密密钥K，用K加密消息M，同时用pk_r加密K，和加密后的消息一并发送给接收方。 接收方收到后，用sk_r解密得到K后，再解密得到消息M。其中（pk_r,sk_r）的生成直接调用ECMH_project.py中的定义。





![image](https://user-images.githubusercontent.com/75195549/180394343-b0b60317-1527-4465-bdc7-136696d22849.png)






实验结果如图：




![image](https://user-images.githubusercontent.com/75195549/180399808-d8e17d1b-1435-4bfb-a3c0-33e96de74314.png)




