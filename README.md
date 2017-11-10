访问元组
元组可以使用下标索引来访问元组中的值，如下实例:
#!/usr/bin/python

tup1 = ('physics', 'chemistry', 1997, 2000);
tup2 = (1, 2, 3, 4, 5, 6, 7 );

print "tup1[0]: ", tup1[0]
print "tup2[1:5]: ", tup2[1:5]
以上实例输出结果：
tup1[0]:  physics
tup2[1:5]:  (2, 3, 4, 5)

修改元组
元组中的元素值是不允许修改的，但我们可以对元组进行连接组合，如下实例:
#!/usr/bin/python
# -*- coding: UTF-8 -*-

tup1 = (12, 34.56);
tup2 = ('abc', 'xyz');


# 创建一个新的元组
tup3 = tup1 + tup2;
print tup3;
以上实例输出结果：
(12, 34.56, 'abc', 'xyz')

删除元组
tup = ('physics', 'chemistry', 1997, 2000);

print tup;
del tup;
print "After deleting tup : "
print tup;
以上实例元组被删除后，输出变量会有异常信息，输出如下所示：
('physics', 'chemistry', 1997, 2000)
After deleting tup :
Traceback (most recent call last):
  File "test.py", line 9, in <module>
    print tup;
NameError: name 'tup' is not defined
  
