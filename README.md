# Python 抽取word文档中的文本。

## 引言
  
   1、[python-docx](http://python-docx.readthedocs.io/en/latest/user/documents.html)    
   2、windows下的win32com    
   python-docx 只能处理docx的文件，我解析的是doc。     
   win32com,因没有windows电脑，不打算用这个库 

## 下面来分享一下是怎么在10分钟内搞定他一个星期搞不定的问题。

    归功于google 和独立思考，既然现有的库只支持docx文档，那么我就思考，linux下有不有工具软件
    处理这个事情，搜索一下，还真找到了这个[antiword](http://www.winfield.demon.nl)
    在mac下brew install antiword
    安装后再在终端antiword 出院记录.doc 文件，文本输出了，到这里就有谱了。

## Python 代码就只有几行。

	#!/usr/bin/env python
	# coding:utf-8
	'''黄哥Python'''
	
	import subprocess
	word = "出院记录.doc"
	output = subprocess.check_output(["antiword", word])
	print output


![](word.png)




