
1.
# !/usr/bin/python
# -*- coding: UTF-8 -*-


class student:

    stu_count=0
    stu_count_wl163 = 0
    stu_count_wl161 = 0

    def __init__(self, stu_no, name, stu_class, male):
        self.stu_no = stu_no
        self.name = name
        self.stu_class = stu_class
        self.male = male
        student.stu_count += 1
        if self.stu_class == 'wl163':
            student.stu_count_wl163 +=1
        elif self.stu_class == 'wl161':
            student.stu_count_wl161 +=1

    def displaystudent(self):
        print "student number :",self.stu_no

    def displaycount(self):
        print "count :",student.stu_count



s = studen()
s = student('22','st','wl151','0')
>>> s.displaystudent()
student number : 22
>>> s.displaycount()
count : 1

s = student('222','sauntao','wl163','0')
>>> g .stu_count_wl163
g = student('333','sdffd','wl163','0')
>>> g .stu_count_wl163
2




2.调用子类

#!/usr/bin/python
# -*- coding: UTF-8 -*-
 
class Parent:        # 定义父类
   parentAttr = 100
   def __init__(self):
      print "调用父类构造函数"
 
   def parentMethod(self):
      print '调用父类方法'
 
   def setAttr(self, attr):
      Parent.parentAttr = attr
 
   def getAttr(self):
      print "父类属性 :", Parent.parentAttr
 
class Child(Parent): # 定义子类
   def __init__(self):
      print "调用子类构造方法"
 
   def childMethod(self):
      print '调用子类方法'
 
c = Child()          # 实例化子类
c.childMethod()      # 调用子类的方法
c.parentMethod()     # 调用父类方法
c.setAttr(200)       # 再次调用父类的方法 - 设置属性值
c.getAttr()          # 再次调用父类的方法 - 获取属性值
以上代码执行结果如下：
调用子类构造方法
调用子类方法
调用父类方法
父类属性 : 200


3.创建中小学生类

class Student:

    stuCount = 0

    def __init__(self,name,stu_no,class_no,gender):
        self.name = name
        self.stu_no = stu_no
        self.class_no = class_no
        self.gender = gender
        Student.stuCount +=1

    def study(self):
        print "Student can study"

    def getStuCount(self):
        return Student.stuCount

class PrimaryStudent(Student):

    primaryStuCount=0

    def canRecite(self):
        print"primary student can recite"

    def canOral(self):
         print"primary student can oral"


class MiddleStudent(Student):

    middleStuCount=0

    def canChemistry(self):
        print"primary student can Chemistry "

    def canPyhics(self):
         print"primary student can Pyhics"
         
        
========================= RESTART: C:/Python27/1.py =========================

>>> m = MiddleStudent('middleSt1','213','1211','female')

>>> m.canPyhics()

primary student can Pyhics

>>> m.canPyhics()

primary student can Pyhics

>>> MiddleStudent.middleStuCount
0
>>> 


