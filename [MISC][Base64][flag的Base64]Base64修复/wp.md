# Base64修复
## 题目
ZmmxhZ3t0aDE1MTU1bzBhc3l9
## 思路
`flag`的Base64是`ZmxhZ3=`，再看题目给的字符串多了一个m  
把m删去一个后再用base64解码直接得到flag  
```Python
import base64
str = "ZmxhZ3t0aDE1MTU1bzBhc3l9"
print(base64.b64decode(str).decode("utf-8"))
```