---
uid: 20230623182930
title: 一种实用新型 Obsidian 实践之构建我的第二大脑
tags: [任务管理]
description: 林宜丙分享的基于Obsidian的第二大脑构建
author: 林宜丙
type: practice
draft: false
editable: false
modified: 20230623193242
---

# 一种实用新型 Obsidian 实践之构建我的第二大脑

> [!note] 声明
> 本文转自：[一种实用新型 Obsidian 实践之构建我的第二大脑 🧠 - 林宜丙的博客 (quanru.github.io)](https://quanru.github.io/2023/06/18/%E4%B8%80%E7%A7%8D%E5%AE%9E%E7%94%A8%E6%96%B0%E5%9E%8B%20Obsidian%20%E5%AE%9E%E8%B7%B5%E4%B9%8B%E6%9E%84%E5%BB%BA%E6%88%91%E7%9A%84%E7%AC%AC%E4%BA%8C%E5%A4%A7%E8%84%91%20%F0%9F%A7%A0/)，已获得作者林宜丙
 的转载许可

## 前言

### 什么是 Obsidian？

![image.png](https://cdn.pkmer.cn/images/202306231834629.png!pkmer)

官网上它是这么自我介绍的：

- [Obsidian](https://obsidian.md/) is the private and flexible note‑taking app that adapts to the way you think.
- [Obsidian](https://obsidian.md/) 是一款私密且灵活的笔记应用程序，可以适应您的思维方式。

我主要看中它丰富的插件生态，你如果喜欢 Vscode，那你大概率也会喜欢 Obsidian，只不过 Vscode 用于写代码，而 Obsidian 用于记笔记。

### 第一大脑 VS 第二大脑

第一大脑即我们的真实大脑，只要我们还活着，那这个大脑就不停地在运转，执行的任务比如知识管理、任务管理、目标管理等，大多数时候我们并不能一脑多用，因此第一大脑更像是一个 CPU，各式各样的任务在抢占 CPU 分片。当需要处理的任务多起来的时候，大脑将不堪重负，因为大脑既要处理当前的任务，又要保持其它任务的上下文，用以切换任务，使得我们无法专注于当前任务的执行，此时需要一个外置的系统来辅助第一大脑，它就是第二大脑。

第二大脑即一个外置的系统，如果把第一大脑比作 CPU 的话，第二大脑更像是存储系统，它就像第一大脑与真实世界之间的一道缓存，减轻了第一大脑的负担，使其能够专注于当前事项。它可以类比为内存和硬盘，只不过内存相对于硬盘，它与 CPU（第一大脑）沟通更加频繁，读取速度也更快。这个存储系统存放当前第一大脑无需时刻关注的事物，当然，这些事物得由第一大脑思考决 - 定是否有存放的必要，内容可以是记录、待办、流程，载体可以是文本、图片、视频。

举一个例子，当我们使用第二大脑进行任务管理的时候，重要紧急的事项存放在内存，不重要不紧急的事项存放在硬盘；本周任务存放在内存，本月任务可能就存放在硬盘；因此通过借助第二大脑，我们就能够无压力专注在当下，在有必要的时候再切换上下文。

本文将以 Obsidian 为例，分享我构建第二大脑的实践！你说它是第二大脑，但是从不同角度审视这个大脑，我也可以称它为『LifeOS』，因为无论从生活还是工作，我都记录在上面；我也可以称它为『可编程个人生产力系统』，我在上面写了不少代码，用来做一些查询和自动化的事情，也是我用来管理任务和目标的生产力系统；甚至它还有点像『Monorepo 工程』，每个文件夹就是一个项目，项目中的 README.md 就像是 Package.json 一样描述了当前项目的元信息。

📢 注意：这套系统不是那种自上而下、先有这套流程而去实现的，是我在使用 Obsidian 过程中逐渐形成的，而且也一直在迭代中，姑且把当前的版本定为 1.0，现在分享出来是想给大家一点点灵感，去完善自己的系统！此外，可能需要有编程基础，因为我写了不少自定义的 JavaScript 脚本（不排除抽成插件的可能），但是你如果完全遵循我这套系统，那也不需要懂代码，下载使用即可！

## 我的实践

我采用两套系统，一个是知识管理系统，另一个是周期笔记，前者以项目/领域/资源为维度，进行知识管理，后者以时间为维度，进行任务/目标/时间管理。

### 两套系统

![image.png](https://cdn.pkmer.cn/images/202306231834481.png!pkmer)

- 知识管理：采用 [PARA](https://fortelabs.com/blog/para/) 系统
  - Projects -> 项目是与目标相关的一系列任务，有截止日期
  - Areas -> 领域是一种活动领域，需要在一定时间内保持一定的标准
  - Resources -> 资源是持续感兴趣的话题或主题
  - Archives -> 存档是来自上述三个类别的非活动条目
- 周期笔记
  - 长期：自顶向下，专注于长期的目标
    - 三年记
    - 年记
    - 季记
  - 短期：自底向上，专注于短期的任务
    - 月记
    - 周记
  - 日常：捕捉想法洞见，实现自我觉察；耗时统计，确保聚焦于项目
    - 日记

其中 PARA 越靠近 Projects，它的可操作性就越高；周期笔记越长期，它的可预测性就越低；

这两套系统相当于制造了两个上下文，让我保持聚焦

- 一个是基于时间的（周期笔记），即我到达某个时间节点，我就基于对应周期笔记作业，且笔记中有足够的上下文；
- 另一个是基于主题的（PARA），即我想对某个主题进行调查研究的时候，我就基于对应主题的索引（README.md）作业，且笔记中已经收集了不少上线文；

### 切面子系统

在上述两套系统之下，隐藏着任务/目标/时间管理子系统，我主要通过『周期笔记』来管理：

- 任务管理
  - 通过日记/周记来收集
  - 通过周记/月记来整理
- 目标管理
  - 通过年记规划年度目标
  - 通过季记分拆年度目标
  - 通过月记拆解待办事项
    - 自上而下整理（通过目标拆解）
    - 自下而上整理（通过收集拆解 -> 日记/周记）
- 时间管理
  - 通过日记手动统计各个项目的耗时和占比，反馈和调整时间开销
  - 通过日记、周记、月记、季记、年记使用脚本自动统计各个项目的耗时和占比，用于复盘时间开销

你也许会好奇，上述子系统似乎只使用了『周期笔记』，实际上两个父系统之间通过两种方式将各个子系统连接起来。

### 连接

> 系统之间如何关联

#### 标签连接

![image.png](https://cdn.pkmer.cn/images/202306231834380.png!pkmer)

将 PARA 下的一级文件夹作为一种特殊的标签（不一定要与文件名完全一致），在『周期笔记』中使用，那么便可在各个一级文件夹中，以相同的方式进行统一的索引。这样能保证每个 PARA 文件夹下的 README.md 索引有当前主题的所有上下文：

![image.png](https://cdn.pkmer.cn/images/202306231834165.png!pkmer)

#### 项目连接

通过在『知识管理』中立项来生成项目，为了增加对项目的关注，在每类『周期笔记』中均设置有『要事列表』或『项目列表』，比如

- 日记中的『项目列表』，它是一份当前项目列表的快照，用于统计当天花费在各个项目中的耗时及其占比，确保把足够的时间花在项目上
- 周记和月记中的『要事维度』，是从本周和本月的日记中自动合并去重得到的一个列表，用于安排项目维度的任务和后续的复盘
- 季记的『要事维度』，它是一份当前领域列表的快照，用于安排要事维度的目标和后续的复盘
- 年记中的『要事维度』，是从本年的季记中自动合并去重得到的一个列表，用于设置领域维度的目标和后续的复盘

![image.png](https://cdn.pkmer.cn/images/202306231835507.png!pkmer)

### 检索

- 标签
  - 比如，日记的 [节日](https://github.com/quanru/obsidian-example-LifeOS/blob/main/PeriodicNotes/2023/Daily/06/2023-06-01.md#L3)、[休假](https://github.com/quanru/obsidian-example-LifeOS/blob/main/PeriodicNotes/2023/Daily/06/2023-06-11.md#L4) 标签
- 索引文件
  - 比如，每个项目的 [README.md](https://github.com/quanru/obsidian-example-LifeOS/blob/main/1.%20Projects/%E5%88%86%E4%BA%AB-2023%20WOT%20%E5%88%86%E4%BA%AB%E4%BC%9A/README.md) 索引本项目的任务、日志、上下文
- 文件夹
  - 比如，每个 PARA 目录使用一致的目录结构

### 复盘

- 复盘主要针对本周期内的项目，复盘的同时规划下个周期的任务
- 周记复盘本周日记，月记复盘每周复盘，季记复盘每月复盘

## 演示说明

### 『日记』与『项目 README』

- 用于日常管理，包括项目列表、日常记录、习惯打卡、精力分配、今日完成等模块
- 日记中的『项目列表』是一份当前项目（即 Projects 目录下）的快照

![image.png](https://cdn.pkmer.cn/images/202306231835943.png!pkmer)

### 『周记』与『月记』

- 用于安排周度和月度任务，包括任务和复盘模块
- 在周记和月记中，『要事维度』是一份本周期日记『项目列表』的快照合集（自动生成）
- 在周记和月记中，『复盘』主要针对本周期内的项目进行

![image.png](https://cdn.pkmer.cn/images/202306231835009.png!pkmer)

### 『季记』与『年记』

- 用于制定季度和年度目标，包括目标和复盘模块
- 在季记中，『要事维度』是一份当前领域（即 Areas 目录下）的快照
- 在年记中，『要事维度』是一份本周期季记『要事维度』的快照合集（自动生成）
- 在季记和年记中，『复盘』主要针对本周期内的领域进行

![image.png](https://cdn.pkmer.cn/images/202306231835139.png!pkmer)

### 『PARA 索引』与『任务索引』

![image.png](https://cdn.pkmer.cn/images/202306231836202.png!pkmer)

## 如何打造？

> 拉取 [Demo](https://github.com/quanru/obsidian-example-LifeOS) 工程，即可体验

- 插件安装
  - 周期笔记
    - <https://github.com/liamcain/obsidian-calendar-plugin>
    - <https://github.com/liamcain/obsidian-periodic-notes>
  - 任务管理：<https://github.com/obsidian-tasks-group/obsidian-tasks>
  - 查询工具：<https://github.com/blacksmithgu/obsidian-dataview>
  - 自定义逻辑：<https://github.com/saml-dev/obsidian-custom-js>
  - 笔记模版：<https://github.com/SilentVoid13/Templater>
- 脚本编写 - <https://github.com/saml-dev/obsidian-custom-js>
  - [date](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Scripts/date.js)
    - 根据周期笔记的文件名，解析出日期
    - 根据解析出的日期，获取日期范围
    - 根据解析出的日期，获取文件列表
  - [task](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Scripts/task.js)
    - 根据日期范围，获取任务列表
  - [project](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Scripts/project.js)
    - 获取当前项目列表的快照
    - 根据日期范围内，获取项目列表
    - 计算日期范围内，项目的耗时及其占比
  - [area](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Scripts/area.js)
    - 获取当前领域列表的快照
    - 根据日期范围内，获取领域列表
- Dataview 视图 - <https://github.com/blacksmithgu/obsidian-dataview>
  - [taskDoneList](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Templates/PeriodicNotes/views/taskDoneList.js)
    - 放到周期笔记中，可获取当前日期范围内完成的任务列表
  - [taskRecordList](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Templates/PeriodicNotes/views/taskRecordList.js)
    - 放到周期笔记中，可获取当前日期范围内收集的任务列表
  - [projectList](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Templates/PeriodicNotes/views/projectList.js)
    - 放到周期笔记中，可获取当前日期范围内项目耗时的占比
  - [areaList](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Templates/PeriodicNotes/views/areaList.js)
    - 放到周期笔记中，可获取当前日期范围内领域列表
- 周期笔记模版 - <https://github.com/SilentVoid13/Templater>
  - [Daily](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Templates/PeriodicNotes/Daily.md)
  - [Weekly](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Templates/PeriodicNotes/Weekly.md)
  - [Monthly](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Templates/PeriodicNotes/Monthly.md)
  - [Quarterly](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Templates/PeriodicNotes/Quarterly.md)
  - [Yearly](https://github.com/quanru/obsidian-example-LifeOS/blob/main/Templates/PeriodicNotes/Yearly.md)

## 实践中的小 Tips

### 缓存区机制

把不重要不紧急的事情，通过创建任务，快速放到缓存区，把大部分注意力保持在『项目』中

### 任务列表

任务的记录不要有太大的心里压力，记下的不代表一定要做；记下了能够减轻你的心里负担，不用老想着这个事，也不怕忘记这个事；我有非常多的任务记下来了，后续经过评估也确实没实现。

我们只要保证一定的机制能回顾到这些被记下的任务即可，比如

- 使用 tasks 插件来做一些任务列表的 [查询视图](https://github.com/quanru/obsidian-example-LifeOS/blob/main/TASK.md)
- 每份周期笔记中都有当前周期收集的 [任务列表](https://github.com/quanru/obsidian-example-LifeOS/blob/main/PeriodicNotes/2023/Weekly/2023-W22.md#%E6%9C%AC%E5%91%A8%E6%94%B6%E9%9B%86)
- 项目索引文件中的 [任务列表](https://github.com/quanru/obsidian-example-LifeOS/blob/main/1.%20Projects/%E5%88%86%E4%BA%AB-2023%20WOT%20%E5%88%86%E4%BA%AB%E4%BC%9A/README.md#%E4%BB%BB%E5%8A%A1)

### 任务提醒

我认为任务有三种提醒方式

- 强提醒，比如抢茅台、抢演唱会门票这种，到点就要进行，就需要强提醒
- 弱提醒，某天需要完成，比如信用卡还款、贷款还款之类的，通过 GTD 软件设置提醒即可
- 列表类，用于记录任务，让你后续统筹安排的，根据需要可以转成强提醒或者弱提醒事件，有点类似 GTD 里的收件箱

### 微习惯

![image.png](https://cdn.pkmer.cn/images/202306231836136.png!pkmer)

- 我会在日记中列一些微习惯，切记不是任务，完不完成都行，主要用来提醒『这些微习惯，你今天考虑做一下吗？』，即在我有『能力』和『动机』的时候，起到『提示』的作用，比如：
  - 微习惯
    - 一听到闹钟响就起床喝水
    - 一下车就戴耳机听小宇宙
    - 一上地铁就打开微信读书
    - 一到工位就写下三件待办
    - 一到十点半就开始干正事

### 易于重构

在每份周期笔记中，相同功能的模块都使用同一个语句，比如『本周期收集的任务』，都是通过插入如下查询语句，而『本周期』的变量是当前的文件名提供，这就使得批量重构所有周期文件变得十分方便，只需要批量替换即可：

```js
await dv.view("Templates/PeriodicNotes/views/taskRecordList")
```

### 善用快捷键

设置全局一致的快捷键，使得无论在哪个软件都能使用同一个快捷键唤起同一个功能，如下是我的部分设置：

- 光标移动
  - 规律：Control + 方向首字母/VIM 方向
  - 示例：
    - A: Head of line
    - E: End of line
    - F/L: Forward
    - B/H: Backward
    - N/J: Next line
    - P/K: Previous line
    - W: Delete a word(Backward)
    - D: Delete a character(Forward)
- 窗口管理
  - 规律：Command + Option + 首字母
  - 示例：
    - L: 左侧半屏
    - R: 右侧半屏
    - C: 居中
    - M: 最大化
    - `[`: 显示/隐藏左侧栏
    - `]`: 显示隐藏右侧栏
    - ': 显示/隐藏底栏
    - T: 新建 Tab(更具体的窗口下，顶层 Tab 使用 Command + T)
    - W: 关闭 Tab(更具体的窗口下，顶层 Tab 使用 Command + W)
    - J: 下一个 Tab
    - K: 上一个 Tab
- 文档编辑
  - 规律 1：Command + Option + 数字/符号
  - 示例：
    - 1: Markdown 一级标题
    - 2: Markdown 二级标题
    - 3: Markdown 三级标题
    - 4: Markdown 四级标题
    - 5: Markdown 五级标题
    - 6: Markdown 六级标题
    - 无序列表: ~
    - 删除线: -
- 功能类
  - 规律：Control + 首字母
  - 示例：
    - C: Copy link(Obsidian block link, Arc browser link, Vscode git link)
    - D: Download
    - I: Add to inbox
    - K: Quick Search