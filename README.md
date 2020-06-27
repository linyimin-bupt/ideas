## 使用内置命令测试网速

使用`ip route get 1 | awk '$5!="" {print $5}' | xargs ifconfig`可以获取网卡接收、上传的字节数。
分别上传和下载大文件或者大量的小文件，然后每隔一秒调用一次，计算差值即可得到网速。（需要确认这样的方式计算出来的网速是否准确）

使用`cat /proc/net/dev | sed 's/://' | awk 'NR>2 {printf "{interface: %s, tx: %s, rx: %s}\n", $1, $2, $10}'`也可以获取网卡（包含虚拟网卡）接收。上传的字节数

两种方式分别计算出结果，然后进行比较，看哪种方式的结果更加准确，为什么？


## 使用Netty实现内网穿透功能

- 学习netty的使用
- 熟悉内网穿透原理

## 在Bash下输出彩色的文本

[研究一下](http://utensil.github.io/tech/2007/09/10/colorful-bash.html)

## API接口自动生成Swagger文档