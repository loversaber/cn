---
published: true
layout: post
title: "北京7月的气温"
author: Yu
categories: 数据分析
tags:
- 气温
- 北京
---

我所在的屋子没有空调，所以夏天会很热，但是我没要想到竟然会这么热。

由于热得是在是受不了了，所以找来了从我出生到现在，北京的每日气温数据，我想看一下今年究竟处于__我所经历的所有时间里__同期的什么水平。

经多简单的统计，我发现，在7月北京的最高平均气温是34.4摄氏度，最低气温是18.8摄氏度，而这两个温度都是进入新世纪（21世纪）后的温度。
最高气温是41.66度，进入2001年后，最高气温是41.11度。

(注意，这篇文章是我后补的，所以我获取了2016年七月份每天的数据。)

从下图可以看到，北京的平均气温在进入七月的第一个7天里会有一个小幅度的上升然后回落，在月末最后5天又会重复一次同样的过程。

![Beijing Average Temperature in July](http://i.imgur.com/4uhNRip.png)

值得注意的是7月9日，这一天的1st四分位数和3rd四分位数都非常接近中位数，说明这一天的温度差异非常的小。~~所以我可以预测，2017年的7月9日，北京的日平均气温应在26摄氏度左右（7月里最舒服的一天）。~~

我刚想“神棍”得预测一下7月9日的气温，但当我把2015和2016年的气温放到直方图上时，这两年的气温都高于历史同期水平，是图上的两个outlier!! 并且这两年的气温走势也不符合我刚才说的月初7天一个小坡，月末5天一个小坡。

![Beijing Average Temperature in July(2015-2016)](http://imgur.com/1tYr8fS.png)

近两年完全不按照历史规律来办事`(╯°Д°)╯︵ ┻━┻`。

2016年7月的平均气温，有3天是进入2001年以来的最高气温，这估计是我会觉得这么热的主要原因。

当然光考虑气温不代表人感受到的实际热度，还要考虑湿度的影响，湿度大，外加气温高，会让人感到更热。

我直接找到2016年7月的[日湿度数据](https://www.wunderground.com/history/airport/ZBAA/2016/7/20/MonthlyHistory.html?&reqdb.zip=&reqdb.magic=&reqdb.wmo=)，发现不下雨的时候平均湿度维持在50%～60%左右，下雨的时候，会维持在80%～90%。由于北京多为阵雨，并且经常出现海淀下雨，朝阳没雨的情况（一个城市竟然会按“城区”下雨），并且每天最高湿度都能达到80%～90%，所以整个7月内人们都会感到很闷热。


