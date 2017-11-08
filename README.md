
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
