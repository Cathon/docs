# Summary

This is the summary of my book.

* [WebMagic概览](posts/ch1-overview/README.md)
	* [设计思想](posts/ch1-overview/thinking.md) 
	* [项目组成](posts/ch1-overview/component.md) 
	* [总体架构](posts/ch1-overview/architecture.md)
* [使用WebMagic](posts/ch2-install/README.md)
	* [使用Maven](posts/ch2-install/with-maven.md)
	* [不使用Maven](posts/ch2-install/without-maven.md)
	* [第一个项目](posts/ch2-install/first-project.md)
* [下载和编译源码](posts/ch3-build-source/README.md)
	* [下载源码](posts/ch3-build-source/git-repo.md)
	* [导入项目](posts/ch3-build-source/import-project.md)
	* [编译和执行源码](posts/ch3-build-source/compile-code.md)
* [基本的爬虫](posts/ch4-basic-page-processor/README.md)
	* [实现PageProcessor](posts/ch4-basic-page-processor/pageprocessor.md)
	* [使用Selectable的链式API](posts/ch4-basic-page-processor/selectable.md)
	* [保存结果](posts/ch4-basic-page-processor/results.md)
* [使用注解编写爬虫](posts/ch5-annotation/README.md)
	* [编写Model类](posts/ch5-annotation/model.md)
	* [TargetUrl与HelpUrl](posts/ch5-annotation/targeturl.md)
	* [使用ExtractBy进行抽取](posts/ch5-annotation/extractby.md)
	* [在类上使用ExtractBy](posts/ch5-annotation/extractby-on-class.md)
	* [结果的类型转换](posts/ch5-annotation/formatter.md)
	* [保存结果(TODO)](posts/ch5-annotation/pagemodel-pipeline.md)
	* [编写一点复杂逻辑(TODO)](posts/ch5-annotation/after-extractor.md)
* [实例分析](posts/chx-cases/README.md)
	* [列表+详情的基本页面组合](posts/chx-cases/basic-list-target.md)
	* [抓取前端渲染的页面](posts/chx-cases/js-render-page.md)
	* 分页抓取
	* 定期抓取
	* 增量更新