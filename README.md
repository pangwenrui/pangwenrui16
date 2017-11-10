

访问列表中的值

list1 = ['physics', 'chemistry', 1997, 2000];
list2 = [1, 2, 3, 4, 5, 6, 7 ];

print "list1[0]: ", list1[0]
print "list2[1:5]: ", list2[1:5]
以上实例输出结果：
list1[0]:  physics
list2[1:5]:  [2, 3, 4, 5]


更新列表

list = ['physics', 'chemistry', 1997, 2000];

print "Value available at index 2 : "
print list[2];
list[2] = 2001;
print "New value available at index 2 : "
print list[2];
以上实例输出结果：
Value available at index 2 :
1997
New value available at index 2 :
2001

删除列表元素
可以使用 del 语句来删除列表的的元素，如下实例：

#!/usr/bin/python

list1 = ['physics', 'chemistry', 1997, 2000];

print list1;
del list1[2];
print "After deleting value at index 2 : "
print list1;
以上实例输出结果：
['physics', 'chemistry', 1997, 2000]
After deleting value at index 2 :
['physics', 'chemistry', 2000]
