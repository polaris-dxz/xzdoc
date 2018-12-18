xzdoc 不再为文档而发愁 [![Build Status](https://secure.travis-ci.org/JacksonTian/xzdoc.png?branch=master)](http://travis-ci.org/JacksonTian/xzdoc)
======================
## 来源
过去通常要自己维护API文档，这会是一件比较蛋疼的事情。所幸我们有[dox](https://github.com/visionmedia/dox)，dox可以帮我们解析注解。但是dox不能帮我们任意生成文档。于是就有了xzdoc，xzdoc基于dox的注解对象，加入模板。在遵循Github和CommonJS的约定后，xzdoc可以帮你的模块包快速生成文档。

## Installation
安装xzdoc为全局工具：

```
$ npm install xzdoc -g
```
## Usage

此处将以xzdoc项目自身作为例子：

```
// 签出xzdoc项目
$ git clone git://github.com/JacksonTian/xzdoc.git ~/git/xzdoc
// 去到项目目录
$ cd xzdoc
$ xzdoc build
// 在docs目录下将会得到文档
$ open ~/git/xzdoc/doc/index.html
// 或者 -o folder，可以将文档生成到指定的目录下
$ xzdoc build -o ~/output
```

### 选择模版

```
// 带上-s参数后，可以选择xzdoc提供的几种模板
$ xzdoc build -s wordpress
```

### 自定义模版
如果xzdoc提供的几个模板不能满足你的需求

```
// 查看xzdoc目前已有的模板
$ xzdoc theme list
// 在当前项目目录导出主题模板
$ xzdoc theme export
// 将会在当前目录下生成{xzdoc-templates/主题名}的目录
// 带上-s参数后，可以选择xzdoc提供的几种模板
$ xzdoc theme export -s pomelo
// 通过xzdoc build创建文档的时，优先读取该目录
// 导出主题模板后，自行修改，即可实现自定义模板的目的
```
## 查看文档效果
通过将生成的文档放到gh-pages分支中，可以通过链接<http://jacksontian.github.com/xzdoc>直接查看效果。

目前提供三种模板

### 默认风格
![defautl 默认风格](https://raw.github.com/JacksonTian/xzdoc/master/doc/default_style.png)

### wordpress风格
![wordpress](https://raw.github.com/JacksonTian/xzdoc/master/doc/wordpress_style.png)

### pomelo风格

## Github与CommonJS规范
- 每个github项目下应该有一个README.md文件
- CommonJS规范建议文档存在在`doc`目录下
- CommonJS规范建议代码存在在`lib`目录下

xzdoc将会扫描项目下的README.md和doc目录下的md文件，通过markdown渲染，生成页面。扫描lib目录下的文件，通过dox解析内容，生成API文档页面。

## 贡献者

以下数据由`git-summary`于2012-10-27生成：

```
 project  : xzdoc
 repo age : 11 months
 active   : 21 days
 commits  : 89
 files    : 94
 authors  : 
    71  Jackson Tian            79.8%
    10  youxiachai              11.2%
     5  Lei Zongmin             5.6%
     3  aleafs                  3.4%

```

## License (MIT)
MIT许可，请自由享用。

```
Copyright (c) 2012 Jackson Tian
http://weibo.com/shyvo

The MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this
software and associated documentation files (the "Software"), to deal in the Software
without restriction, including without limitation the rights to use, copy, modify,
merge, publish, distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to the
following conditions:

The above copyright notice and this permission notice shall be included in all copies
or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,
INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF
CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE
OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

## 捐赠
如果您觉得本模块对您有帮助，欢迎请作者一杯咖啡

[![捐赠xzdoc](https://img.alipay.com/sys/personalprod/style/mc/btn-index.png)](https://me.alipay.com/jacksontian)
