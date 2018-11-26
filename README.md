### Shell-Frameworkd
____
* 简介:
    > 插件化批量URL漏洞扫描器

* 参数说明

        Usage: framework.py -k "inurl:/news/shownews.php?lang=cn&id=" -p 2 -e baidu -l metinfo_sql

        Options:
          -h, --help            show this help message and exit
          -k KEYWORD, --keyword=KEYWORD
                                Waiting for collection's command.
          -p PAGE, --page=PAGE  Collected pages.
          -e ENGINE, --engine=ENGINE
                                Spider Engine
          -l LOAD, --load=LOAD  Load Plugin Script Name
          -s SCRIPTS, --scripts=SCRIPTS
                                List Plugin
          -o OUTPUT, --output=OUTPUT
                                Output file
          -f FILENAME, --filename=FILENAME
                                Read file

* 实例
> 使用baidu语法爬虫从搜索baidu搜索引擎抓取链接, 
定义爬行1-10页,并使用插件metinfo_sql来对每个链接进行漏洞检测,
并输出保存到metinfo_pass.txt
![frameworkpng01](/png/01.png)

> 使用本地已保存的txt里的url进行漏洞检测
![frameworkpng02](/png/02.png)

___
* 说明: oshadan接口已废弃, 后采用zoomeye(开发ing)
* 说明: 插件格式如下
```
# coding:utf-8

class Exploit:

    def attack(self, url):
        '''do something'''
        return "format in the terminal."
```
* 说明: 我搜集的插件之后将会放到另一个项目下.
