# Scrapy_xpath_null_Problem
scrapy爬虫xpath自动跳过值为空的元素问题（对item进行处理）
scrapy爬虫xpah自动跳过值为空的问题
问题：要爬此页面的数据，结果球衣号不全，造成各列数据爬取后不对齐的问题。
 ![Alt Text](
     https://github.com/appliance/Scrapy_xpath_null_Problem/blob/master/1.png
    )
解决方法：
1、	利用xpath将html结构数据获取保存在一个集合中
2、	利用for循环遍历，再利用xpath从其中获取想要的数据内容
a)	注，此处要利用from lxml import etree
b)	etree.HTML(str)	将str类型的html语句转化为html形式，此形式可以使用xpath
c)	创建一个集合，保存所有的值
d)	最后用item[]字典保存刚刚保存的集合
3、	代码如下
 

