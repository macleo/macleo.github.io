---
layout: post
title: Mac 常用资源
category: 资源
tags: Mac
keywords: Mac
description: 
---

## 常用软件

### Alfred

#### Alfred常用Workflow

- [Dash](http://kapeli.com/dash)
- [Dict - Lookup Word](https://github.com/liberize/alfred-dict-workflow)
- [Reminders](http://www.alfredforum.com/topic/917-reminders/)
- [Evernote](http://support.alfredapp.com/evernote)
- [Notes](http://www.alfredforum.com/topic/1009-notes/)

## 常用技巧

### 开启关闭dashboard

关闭

    defaults write com.apple.dashboard mcx-disabled -boolean YES
    killall Dock

开启

    defaults write com.apple.dashboard mcx-disabled -boolean NO
    killall Dock

### 设置iterm中option为alt(meta)键

![option-to-meta](http://yansu-uploads.stor.sinaapp.com/imgs/set-meta-to-alt.png)

### 删除dropbox冲突文件

    find . -type f -name "* conflicted *" -exec rm -f {} \;

### 清空Launchpad（删除掉）

    sqlite3 ~/Library/Application\ Support/Dock/*.db 'DELETE FROM apps;' && killall Dock

### 重置Launchpad

    rm -f ~/Library/Application\ Support/Dock/*.db && killall Dock

### 修改Finder中文件夹显示语言

    # 以Desktop为例
    touch ~/Desktop/.localized
    chmod 600 ~/Desktop/.localized