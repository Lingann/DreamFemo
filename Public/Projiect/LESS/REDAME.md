## LESS使用指南


### 1. 简介
Less 是一门 CSS 预处理语言，它扩展了 CSS 语言，增加了变量、Mixin、函数等特性，使 CSS 更易维护和扩展。

Less 可以运行在 Node 或浏览器端。

### 2. 安装

**通过npm安装**

```
$ npm install -g less
```

**检测版本**

```
$ lessc -v
```

**可以为less编译后的css进行压缩**
需要安装一个插件

```
$ npm install -g less-plugin-clean-css
```

### 3. 在sublime中使用less

- 打开sublime ctrl+shift+p>install Package
- 搜索选择 Less2css 之后Enter
- 新建style.less,保存，会发现同目录下有一个style.css文件，这就是使用less编译好的css文件。在style.less进行更改会同步到style.css上。

### 4. sublime插件，less代码高亮和提示
1. 打开sublime>Preference>Browse Packages
2. 安装LESS-Sublime插件到sublime本地的Packages中
git bush:
```
git clone git://github.com/danro/LESS-sublime.git LESS
```
3. 打开sublime，在Preferences > Package Setting > LESS > Settings-User
进行如下配置
```
{
  // Boolean setting to auto-insert a semicolon after a ":" is typed.
  "auto_insert_semicolon": false
}
```
4. 在sublime右下角的语言编码(就在最右下角Tab-size的旁边)列表中选择LESS
5. 开始进行LESS之旅

**插件地址**
- [LESS syntax for Sublime Text](https://packagecontrol.io/packages/LESS)
- [less高亮插件github地址](https://github.com/danro/LESS-sublime)

### 5. 把编译LESS加入Windows右键菜单
创建一个批处理文件名`makeless.bat`
```
@echo off
cd /d %~dp1
lessc %1 > %~n1.css
```


### 参考
* [Less官方参考手册](http://less.bootcss.com/)
* [在前端使用和编译LESS——冰翼博客](https://icewing.cc/less-to-contextmenu.html)
* [Less介绍及与Sass的差异——菜鸟教程](http://www.w3cplus.com/css/an-introduction-to-less-and-comparison-to-sass.html)
* [LESS编写技巧分享，快乐编写CSS——轩枫阁](http://www.xuanfengge.com/less-writing-skills-sharing-happy-to-write-css.html)
* [Less is More](https://github.com/Urinx/SomeCodes/tree/master/Web/less.demo)
* [Sublime Text 3 LESS、SASS、SCSS高亮插件、提示插件](http://www.qdfuns.com/notes/24473/e8ff9935aac562c07f634c080d1cb787:storey-3.html)