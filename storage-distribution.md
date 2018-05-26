# Storage Distribution

发布版本：1.0

作者邮箱：703632667@qq.com

日期：2018-05-26

------

**前言**

适用于tiny210。

**修订记录**

| 日期       | 版本 | 作者      | 修改说明 |
| ---------- | ---- | --------- | -------- |
| 2018-05-26 | V1.0 | Jason Zhu |          |

------

[TOC]

## 1. 固件在存储中的分布

| Partition| Start Sector | Number of Sectors| size | Requirements |
| ---------- | ---- | --------- | -------- | -------- |
| MBR | 0 | 1 |  |  |
| BL1 | 1 | 32 |  |  |
| Vendor Storage | 4097 | 8192 |  |  |
| uboot | 8193 | 12288 |  |  |
| dtb | 12289 | 16384 |  |  |
| rootfs | 16385 | ----- |  |  |