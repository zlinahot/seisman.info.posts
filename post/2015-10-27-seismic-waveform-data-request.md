---
title: 地震数据申请
date: 2015-10-27
author: SeisMan
categories:
  - 地震学基础
tags:
  - 数据申请
slug: seismic-waveform-data-request
---

申请地震波形数据，按照具体的需求，大致可以分为两大类，即事件波形数据和连续波形数据。

这两者的主要区别在于如何确定要申请的数据时间窗，前者需要震相到时信息，后者则不需要。

<!--more-->

## 事件波形数据

1.  筛选事件
    1.  获取地震目录，比如 GCMT、USGS PDE、ISC
    2.  从地震目录中获取某个特定事件的信息
    3.  或根据条件筛选出需要的事件信息，筛选条件包括：
        1.  经纬度范围
        2.  深度范围
        3.  时间范围
        4.  震级范围

2.  筛选台站，筛选条件包括：
    1.  台站位置
    2.  仪器类型（宽频带、长周期、短周期等）
    3.  分量类型（三分量或只要 Z 分量）

3.  波形起始和结束时间

    需要根据发震时刻和震中距信息，计算理论到时，由此确定要申请的数据时间窗。

    波形起始时间可以取发震时刻或相对于某震相的时刻（比如 P 波前 5 分钟）等等。波形结束时间可以通过数据长度指定，也可以直接指定相对于某震相到时的时刻（比如 S 波之后 10 分钟）。

4.  选择数据格式，比如 SAC 或 SEED

事件波形数据又可以进一步分成两类：以事件为中心的事件波形数据和以台站为中心的事件波形数据。

像地震定位、地震震源机制等问题，一般都需要以事件为中心的事件波形数据。此类情况下，通常先筛选地震事件再筛选台站。在筛选台站时，可以额外加上震中距范围和方位角范围的限制。

像接收函数等问题，一般需要以台站为中心的事件波形数据。此类情况下，通常先筛选台站再筛选事件。在筛选事件时，可以额外加上震中距范围和反方位角范围的限制。

## 连续波形数据

连续波形数据中没有地震事件的信息，因而都是以台站为中心的，比如背景噪声相关。

1.  选择台站，筛选条件：
    1.  台站位置
    2.  仪器类型（宽频带、长周期、短周期等）
    3.  分量类型（三分量或只要 Z 分量）

2.  确定时间范围：选择合适的时间范围
3.  选择数据格式，比如 SAC 或 SEED

根据地震事件的信息以及震中距信息，计算震相的理论走时，再根据事件发震时刻得到震相的绝对时刻，进而确定要申请数据的绝对时间范围。本质上，事件波形数据是连续波形数据的一个子集。