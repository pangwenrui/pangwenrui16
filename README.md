
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
