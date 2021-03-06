# ZumDown_docs

ZumDown，全称ZRY Universal MarkDwon，是一个Markdown方言，通用于swzry.com及其旗下分站。本Git仓库为该语言的文档。

该方言在基础功能上基本兼容标准的Markdown，但部分细节不同。此外，本方言对传统Markdown提供的blockcode（代码块，即使用一对\`\`\`包括的代码块）进行了重新定义，定义这种区块为superblock，提供更为丰富的复杂排版样式功能。值得注意的是，为了保证网站页面的版面整洁，以及防范XSS注入攻击，superblock只有部分功能几乎所有用户有权在绝大多数可以使用ZumDown发言的页面中使用，而部分功能仅对部分用户在部分页面开放。有另外部分页面可能不支持使用superblock。

该文档主要分以下几个部分：

* **基础语法：** 最基本的样式功能，即标准Markdown提供的功能，因为和标准Markdown有少量区别，为方便大家使用，故与标准Markdown教程一并整理成篇放入本文档。

* **超级块：** 即superblock，主要介绍superblock区块的基本功能，这些功能是大部分用户有权限使用的。

* **特殊功能：** 这些功能只对特定用户，比如小说平台作者在小说中、文档平台贡献者在文档中心使用等。这类功能如果滥用有可能会破坏版面整洁，请各位有权使用的用户使用时注意礼仪和用户友好性。

* **管理员功能：** 这些功能只对管理员开放，这类功能有可能用来在页面中直接插入HTML、CSS甚至JavaScript，仅允许网站管理人员使用。但由于ZumDown的渲染引擎是开放源代码的，其它网站或应用亦可采用，故本文档也将介绍这类功能。

* **开发者：** 这部分内容针对想将ZumDown语言标准或者渲染器源代码进行利用或二次开发的人员。

**友情提示：** 莫要把ZumDown打成ZunDown了←_←

**说明：** 本文档除README.md以外均用ZumDown书写，README.md为GitHub Markdown方言Sundown书写，为的是能在Git平台上正确显示，显然在Git平台上ZumDown显示效果会不正确，因为没有ZumDown渲染引擎。

## Reference

* [Markdown 语法说明 (简体中文版)](http://wowubuntu.com/markdown/)
* [Markdown——入门指南](http://www.jianshu.com/p/1e402922ee32/)
* [Misaka Documentation](http://misaka.61924.nl/)
* [Hoedown Examples](https://github.com/hoedown/hoedown/tree/master/test/MarkdownTest_1.0.3/Tests)
* [ZumDown测试练习平台](http://demo.9zry.com/SuwakoMethod/)