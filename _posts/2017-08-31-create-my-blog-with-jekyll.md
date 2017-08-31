---
layout: post
title:  "git回滚"
date:   2017-08-31 
categories: jekyll
tags: jekyll RubyGems
---

* content
{:toc}


## git回滚到之前的提交
开发中避免不了出现坏的提交，这个时候不要着急只需四部就可以让你之前的提交变成当前的提交：


* 首先两步保证当前工作区是干净的，并且和远程分支代码一致
* 备份当前的分支（如果必要）
* 恢复到指定的提交


```
$ git reset --hard resetVersionHash //将当前branch的HEAD指针指向commit hash
```

* 删除当前分支的远程分支


```
$ git push origin :currentBranch 
$ //或者这么写git push origin --delete currentBranch
```


* 把当前分支提交到远程


```
$ git push origin currentBranch
```






