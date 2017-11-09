匹配字符
>>> import re

>>> line = "Cats are smarter than dogs"
>>> re.match(r'Cats',line,re.M|re.I)
>>> matchObje = re.match(r'Cats',line, re.M|re.I)
>>> matchObje.group()
'Cats'


>>> line ="Cats are dogs smarter than dogs"
>>> matchObje = re.search(r'dogs',line)
>>> matchObje
<_sre.SRE_Match object at 0x022F93D8>
>>> matchObje.group()
'dogs'
>>> matchObje = re.search(r'Cats',line)
>>> matchObje
<_sre.SRE_Match object at 0x0052A988>
>>> matchObje.group()
'Cats'
>>> 

>>> matchObje = re.search(r'dogs',line,re.I)
>>> matchObje.group()
'dogs'
>>> matchObje = re.search(r'dogs$',line,re.I)
>>> matchObje
<_sre.SRE_Match object at 0x022F9330>

查找邮件

>>> 
>>> y='123@qq.comaaa@163.combbb@126.comasdfasfs33333@adfcon'
>>> import re
>>> re.findall('\w',y)
['1', '2', '3', 'q', 'q', 'c', 'o', 'm', 'a', 'a', 'a', '1', '6', '3', 'c', 'o', 'm', 'b', 'b', 'b', '1', '2', '6', 'c', 'o', 'm', 'a', 's', 'd', 'f', 'a', 's', 'f', 's', '3', '3', '3', '3', '3', 'a', 'd', 'f', 'c', 'o', 'n']
>>> re.findall('\w+',y)
['123', 'qq', 'comaaa', '163', 'combbb', '126', 'comasdfasfs33333', 'adfcon']
>>> re.findall('\w+@',y)
['123@', 'comaaa@', 'combbb@', 'comasdfasfs33333@']
>>> re.findall('\w+@\w+\.com',y)
['123@qq.com', 'aaa@163.com', 'bbb@126.com']
>>> 
>>> 
查找电话号码
>>> y='tel:010-12345678 address:changanRoad'
>>> re.findall('\d+-\d+',y)
['010-12345678']
>>> y='tel:010-12345678 address:changanRoad other tel: 0371-1234567'
>>> re.findall('\d{3}-\d{8}',y)
['010-12345678']
>>> re.findall('\d{3,4}-\d{7,8}',y)
['010-12345678', '0371-1234567']
>>> 





