

#!/usr/bin/python
# -*- coding: UTF-8 -*-
import urllib2
import re

headers = {'User-Agent':' Mozilla/5.0 (Windows NT 6.1)AppleWebKit/537.36(KHTML,like Gecko)Chrome/60.0.3112.113 Safari/537.36'}

url = 'http://quotes.toscrape.com/'
req = urllib2.Request(url, headers=headers)
response = urllib2.urlopen(req)
with open('D:/test.html','wb') as f:
 f.write(response.read())
job_name_pattern = re.compile('<div class="col-md-8">.*?="text">(.*?)</span>',re.S)


