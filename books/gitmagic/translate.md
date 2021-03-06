# 附录 B: 本指南的翻译 

我推荐如下步骤翻译本指南，这样我的脚本就可以快速生成HTML和PDF版本，并且所有翻译也可以共存于同一个仓库。

克隆源码，然后针对不同目标[语言的IETF tag](http://www.iana.org/assignments/language-subtag-registry)创建一个目录。参见[ W3C在国际化方面的文章 ](http://www.w3.org/International/articles/language-tags/Overview.en.php)。例如，英语是“en”，日语是“ja”，正体中文是“zh-Hant”。

然后在新建目录，翻译这些来自“en”目录的 +txt+ 文件。

例如，将本指南译为 [ 克林贡语 ](http://en.wikipedia.org/wiki/Klingon_language)，你也许键入：

	$ git clone git://repo.or.cz/gitmagic.git
	$ cd gitmagic
	$ mkdir tlh  # "tlh" 是克林贡语的IETF语言码。
	$ cd tlh
	$ cp ../en/intro.txt .
	$ edit intro.txt  # 翻译这个文件

对每个文件都一样。

打开Makefile文件，把语言码加入`TRANSLATIONS`变量，现在你可以时不时查看你的工作：

	$ make tlh
	$ firefox book-tlh/index.html

经常提交你的变更，然后然我知道他们什么时候完成。GitHub.com提供一个便于fork“gitmatic”项目的界面，提交你的变更，然后告诉我去合并。

但请按照最适合你的方式做：例如，中文译者就使用Google Docs。只要你的工作使更多人看到我的工作，我就高兴。

