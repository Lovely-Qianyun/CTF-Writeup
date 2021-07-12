# 藏在邮件头里的秘密
## 题目
flag{ichunqiu_=E6=8A=80=E6=9C=AF=E6=9C=89=E6=B8=A9=E5=BA=A6}
## 思路
里面是可打印字符编码，解码网站  
`http://www.mxcz.net/tools/QuotedPrintable.aspx`  
`http://web.chacuo.net/charsetquotedprintable/`  

Quoted-printable 可译为“可打印字符引用编码”、“使用可打印字符的编码”，我们**收邮件**，查看**信件原始信息**，经常会看到这种类型的编码，任何一个8位的字节值可编码为3个字符：一个等号后跟随两个十六进制数字(0–9或A–F)表示该字节的数值  
在所有邮件处理的各式各样的编码中，很多编码的目的都是通过编码手段使得七位字符的邮件协议体系可以传送八位的二进制文件、双字节语言文字等等。 Quoted-Printable也是这样一些编码中的一个， 它的目的同样是帮助非ASCII 编码的信件传输通过 SMTP。Quoted-Printable 编码是字符对应的编码，每个未编码的二进制字符被编码成三个字符，即一个等号和一个十六进制的数字，如“A8”。  

解密结果：  
技术有温度