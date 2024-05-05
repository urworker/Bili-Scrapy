# Bili-Scrapy(test)
抓取用户个人简介、视频、文章及关注粉丝等内容

## 使用到的工具有：
1、Mysql：用于存放爬取数据 \
2、Redis：用来存放爬虫的用户mid，这里使用Redis的原因是因为，可以随时停止，然后再随时从同一个mid开始爬取 \
3、Scrapy: Python爬虫框架 \


## 存储及爬取思路
简单说下整个爬取思路吧，由于B站的用户mid都是一串数字，所以可以在redis生成1000w个mid（具体想爬多少个，就生成多少个）；\
然后再将爬取的数据存入到数据库中（需要提取建好对应的表，代码中小编这边是放入了自已写的表及字段）


# 步骤
1、先在mysql或者其它类型的数据库创建好对应的表 \
2、在redis中发布好对应的需要爬取的用户mid\
3、开启Scrapy爬虫
