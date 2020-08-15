---
title: "基于Python-wechaty建立一个斗图机器人 POC 成果展示"
date: 2020-08-13 23:00 +0800
author: godkillerxiao
image: /assets/2020/meme-bot/08-13-wechaty-meme-bot-mid-term.png
tags:
  - python

---

> Author: [@MrZilinXiao](https://github.com/MrZilinXiao) Always dedicated to learn something brand new.
> Code: [@python-wechaty-meme-bot](https://github.com/MrZilinXiao/python-wechaty-meme-bot/)

<!--more-->

## 暑期2020 基于Python-wechaty建立一个斗图机器人 POC 成果展示

“开源软件供应链点亮计划-暑期2020”（以下简称 暑期2020）是由中科院软件所与 openEuler 社区共同举办的一项面向高校学生的暑期活动。
旨在鼓励在校学生积极参与开源软件的开发维护，促进国内优秀开源软件社区的蓬勃发展。
根据项目的难易程度和完成情况，参与者还可获取“开源软件供应链点亮计划-暑期2020”活动奖金和奖杯。
官网：[https://isrc.iscas.ac.cn/summer2020](https://isrc.iscas.ac.cn/summer2020) 官方新闻：[http://www.iscas.ac.cn/xshd2016/xshy2016/202004/t20200426_5563484.html](http://www.iscas.ac.cn/xshd2016/xshy2016/202004/t20200426_5563484.html)
本项目 基于Python-wechaty建立一个斗图机器人 系 暑期2020 支持的开源项目。

## [基于Python-wechaty建立一个斗图机器人]信息

- 导师：黄纯洪

- 学生：肖子霖

- 项目名称：基于Python-wechaty建立一个斗图机器人

- 方案描述：利用OCR、NLP等技术，提取出用户发送的表情包内容，并回复数据库中已有与之相关的表情；具体技术方案泳道图见下：

  ![mid-term](/assets/2020/meme-bot/08-13-wechaty-meme-bot-mid-term.png)

  更多细节可参见[项目README](https://github.com/MrZilinXiao/python-wechaty-meme-bot/blob/master/README.md).

- 时间规划（摘自项目申请书）：

  - Week1：仔细阅读python-wechaty项目源码，掌握项目大体框架和可用API；
  - Week2：收集表情包数据，选择合适的网络模型。
  - Week3~Week4：训练模型，调试参数；
  - Week5：开发核心模块，编写单元测试；
  - Week6：开发、配置表情包插件后端；
  - Week7~Week8：模块联调，编写测试样例，上线测试。

## 项目进度

- 已完成工作：

  - 利用peewee搭建数据库ORM框架；
  - 表情包爬取（BaseSpider）、收集框架
  - 引入、调试OCR模块
  - 调试Inception特征提取模型
  - 复现[*Deep Cosine Metric Learning for Person Re-identification*](https://ieeexplore.ieee.org/document/8354191/)一文中有关Metric Learning部分，编写好相关训练、验证、测试模块
  - 表情包导入模块
  - 前端回复模块
  - 后端回复逻辑
  - 前端、后端、Wechaty联调，效果见Demo Live视频中演示
  - 部署文档编写

  项目申请书`时间规划`所提及任务中除训练模型外的任务基本完成；

- 遇到的问题及解决方案：

  - python-wechaty文档尚未完成，遇到疑惑时需要翻阅issue列表或者深入源码查看；
  - 网络上没有关于将Metric Learning方法应用到表情包分类的先例，不确定Cosine Metric Learning能在表情包特征提取上起到较好效果，不过我认为勇于尝试是十分必要的！

- 后续工作安排：

  - 对比传统图像分类模型Inception、Metric Learning模型CosineMetricNet的特征提取效果，为用户提供多种选择。
  - 思考出性能优秀的cosine distance比较方法，为从数据库海量表情中提取出相似的表情提供便利。

## 中期PPT演示 & Demo Live 视频链接

PPT演示：

<iframe src="//player.bilibili.com/player.html?aid=371714000&bvid=BV1kZ4y1M7F6&cid=224034124&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

Demo Live视频：

<iframe src="//player.bilibili.com/player.html?aid=286675266&bvid=BV17f4y197ut&cid=224030905&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

## Reference

### Open-Source Reference

- [chineseocr_lite](https://github.com/ouyanghuiyu/chineseocr_lite/tree/master): Powerful Chinese OCR module with accurate results and fast inference speed.
- [HaNLP](https://github.com/hankcs/HanLP): Multilingual NLP library for researchers and companies, built on TensorFlow 2.0.

### Academic Citation

```bash
# in backend/cosine_metric_net.py
[1]N. Wojke and A. Bewley, “Deep Cosine Metric Learning for Person Re-identification,” in 2018 IEEE Winter Conference on Applications of Computer Vision (WACV), Lake Tahoe, NV, Mar. 2018, pp. 748–756, doi: 10.1109/WACV.2018.00087.
```

## 联系我们

- 项目链接：[@python-wechaty-meme-bot](https://github.com/MrZilinXiao/python-wechaty-meme-bot/)
- 联系方式：me#mrxiao.net  (# -> @)