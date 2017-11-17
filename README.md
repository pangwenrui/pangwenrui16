

1.下面是简单的例子，它打开一个文件，在该文件中的内容写入内容，且并未发生异常：
#!/usr/bin/python
# -*- coding: UTF-8 -*-

try:
    fh = open("testfile", "w")
    fh.write("这是一个测试文件，用于测试异常!!")
except IOError:
    print "Error: 没有找到文件或读取文件失败"
else:
    print "内容写入文件成功"
    fh.close()
    
以上程序输出结果：
$ python test.py 
内容写入文件成功
$ cat testfile       # 查看写入的内容
这是一个测试文件，用于测试异常!!

2.

import urllib2
 
requset = urllib2.Request('http://www.xxxxx.com')
try:
    urllib2.urlopen(request)
except urllib2.URLError, e:
    print e.reason
我们利用了 urlopen方法访问了一个不存在的网址，运行结果如下：
[Errno 11004] getaddrinfo failed
它说明了错误代号是11004，错误原因是 getaddrinfo fai



3.
import urllib2
 
req = urllib2.Request('http://blog.csdn.net/cqcre')
try:
    urllib2.urlopen(req)
except urllib2.HTTPError, e:
    print e.code
    print e.reason
运行结果如下

403
Forbidden

错误代号是403，错误原因是Forbidden，说明服务器禁止访问。


4.
import urllib2 
req = urllib2.Request('http://blog.csdn.net/cqcre')
try:
    urllib2.urlopen(req)
except urllib2.HTTPError, e:
    print e.code
except urllib2.URLError, e:
    print e.reason
else:
    print "OK"
