---
layout: post
title: sublime 安装 markdown 插件
categories: HGE
description: sublime 安装 markdown 插件解后的学习笔记。
keywords: 应用软件
---

## 安装Package Control 

The simplest method of installation is through the Sublime Text console. The console is accessed via the ctrl+` shortcut or the View > Show Console menu. Once open, paste the appropriate Python code for your version of Sublime Text into the console.

sublime text3
```import urllib.request,os,hashlib; h = '261dd1222b4693ce6d4f85f9c827ac06' + '6d5ab8ebdd020086947172a8a1356bb6'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)```


sublime text2
```import urllib2,os,hashlib; h = '261dd1222b4693ce6d4f85f9c827ac06' + '6d5ab8ebdd020086947172a8a1356bb6'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
```

## 安装markdown editing和markdown preview
* ```shift+command+p```  
后输入install package 回车 等。。。
* ```makrdown editing```  
回车 等。。。
* ```makrdown preview``` 
回车 等。。。
* 重启sublime 即可
