---
layout: post
title: sublime 安装 markdown 插件
categories: 应用
description: sublime 安装 markdown 插件解后的学习笔记。
keywords: 应用软件
---
<!-- MarkdownTOC -->

- [安装Package Control](#安装package-control)
- [安装markdown editing和markdown preview](#安装markdown-editing和markdown-preview)

<!-- /MarkdownTOC -->
***
## 安装Package Control 

The simplest method of installation is through the Sublime Text console. The console is accessed via the ctrl+` shortcut or the View > Show Console menu. Once open, paste the appropriate Python code for your version of Sublime Text into the console.

* sublime text3:
```
import urllib.request,os,hashlib; h = '261dd1222b4693ce6d4f85f9c827ac06' + '6d5ab8ebdd020086947172a8a1356bb6'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```


* sublime text2:
```
import urllib2,os,hashlib; h = '261dd1222b4693ce6d4f85f9c827ac06' + '6d5ab8ebdd020086947172a8a1356bb6'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
```

## 安装markdown editing和markdown preview
* 运行pacage install
shift+command+p
后输入install package 回车 等。。。
* Markdown Extended
回车 等。。。
* makrdown editing 回车 等。。。
    在 Sublime 中编写 Markdown 还有一个直观的不适就是缺少辅助提示，比如输入 *，编辑器应当自动补上一个 *，并使光标保持在两 * 之间，又比如应当支持选中一段文字快捷键添加链接。
Markdown Editing 提供了这些支持，它也提供配色方案（略丑）。
个人常用的三个快捷键是：
Option + Command + K - 插入链接；
Option + Command + V - 粘贴为链接格式；
Shift + Command + K - 插入图片。

* makrdown preview
回车 等。。。
* markdownTOC
* 重启sublime 即可
