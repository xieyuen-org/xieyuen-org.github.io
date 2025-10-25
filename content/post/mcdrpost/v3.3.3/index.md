---
title: "MCDRpost v3.3.3"
description: MCDRpost 3.3.3 正式版发布
date: 2025-10-25T17:59:10Z
image: 
math: 
license: 
hidden: false
comments: true
draft: false
categories:
  - MCDR-Plugin
tags:
    - MCDRpost
    - Release
---

> [!IMPORTANT]
> 此版本强烈建议更新！除非你没有更新3.3.2

## ChangeLog

### Added

- 提供自定义音效的 API
  - 删除了原本的 play_sound 模块
  - 添加抽象类: AbstractSoundPlayer
  - 添加实现类: NewSoundPlayer 并暴露至 API
  - 添加实现类: OldSoundPlayer 并暴露至 API
  - 添加 property: AbstractVersionHandler.play_sound
- 添加了一些注释和类型注解

### Changed

- 新的翻译使用方式
  - 原来的 `tr(Tags.xxx)` 使用方法还是不够方便，换成 `TranslationKeys.xxx.tr()` 就不用再在外面套一层 `tr()` 了
- 修改了部分变量/属性的名称

### Fixed

- 修复了 player 命令没有回复的问题
- （**严重**）修复了无法发送/接受物品的 BUG

### Removed

- 放弃对 1.9~1.13 的支持，当服务器使用此区间的版本时只使用外界注册的 Handler
