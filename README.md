import urllib2
 
request = urllib2.Request("http://www.baidu.com")
response = urllib2.urlopen(request)
print response.read(3000)




<!DOCTYPE html>
<!--STATUS OK-->


<html>
<head>
    
    <meta http-equiv="content-type" content="text/html;charset=utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=Edge">
	<meta content="always" name="referrer">
    <meta name="theme-color" content="#2932e1">
    <link rel="shortcut icon" href="/favicon.ico" type="image/x-icon" />
    <link rel="search" type="application/opensearchdescription+xml" href="/content-search.xml" title="百度搜索" />
    <link rel="icon" sizes="any" mask href="//www.baidu.com/img/baidu_85beaf5496f291521eb75ba38eacbd87.svg">
	
	
	<link rel="dns-prefetch" href="//s1.bdstatic.com"/>
	<link rel="dns-prefetch" href="//t1.baidu.com"/>
	<link rel="dns-prefetch" href="//t2.baidu.com"/>
	<link rel="dns-prefetch" href="//t3.baidu.com"/>
	<link rel="dns-prefetch" href="//t10.baidu.com"/>
	<link rel="dns-prefetch" href="//t11.baidu.com"/>
	<link rel="dns-prefetch" href="//t12.baidu.com"/>
	<link rel="dns-prefetch" href="//b1.bdstatic.com"/>
    
    <title>百度一下，你就知道</title>



POST方式：


import urllib
import urllib2
 
values = {"username":"1016903103@qq.com","password":"XXXX"}
data = urllib.urlencode(values) 
url = "https://passport.csdn.net/account/login?from=http://my.csdn.net/my/mycsdn"
request = urllib2.Request(url,data)
response = urllib2.urlopen(request)
print response.read()

GET方式：


import urllib
import urllib2

values={}
values['username'] = "1016903103@qq.com"
values['password']="XXXX"
data = urllib.urlencode(values) 
url = "http://passport.csdn.net/account/login"
geturl = url + "?"+data
request = urllib2.Request(geturl)
response = urllib2.urlopen(request)
print response.read()

设置Headers
>>>import urllib2
>>> user_agent='Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML,like Gecko) Chrome/62.0.3202.75 Safari/537.36'
>>> urllib2.Request('http://www.baidu.com',headers={ 'User=Agent':user_agent})

<urllib2.Request instance at 0x021D4DC8>

