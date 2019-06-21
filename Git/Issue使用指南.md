和TFS的DIM系统类似，Git中用于bug追踪的系统叫做BTS(Bug Tracking System)，即Issue。利用Issue，我们可以实现以下需求。

# 问题追踪

## 如何创建？
点击`New issue`按钮即可进入创建界面，一些关键字段如下：

- Title: 问题简要描述
- Description：问题详细描述，支持MD语法
- Assignee：问题指定人
- Due date：问题截止日期
- Milestone：该问题隶属里程碑
- Label：标签，可设置多个标签

## 创建原则
BTS中最细小最基本的问题或需求


# 任务管理（Labels）
Label通常为Issue的标签，这里可以利用这一点进行bug分类，任务归档等操作，基于Issue列表进行工作

## 创建原则
通常一些细小的功能或是进度可采用Label来进行管理，然后利用搜索功能进行数据的统计


# 时间节点管理（Milestones）

## 如何创建？
时间节点管理通常采用创建Milestones的方式，一些关键字段如下：
- Title: 里程碑名称
- Description：里程碑详细描述，支持MD语法
- Start Date：里程开始日期
- Due Date：里程截止日期

## 创建原则
Milestone通常是指大的时间节点，比如R10节点，R11节点之类的
