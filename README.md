免费部署:

serv00免费搭建pixiv反代

[Tawerの博客](https://blg.tawertwtc.xyz/2024/05/18/%E7%AE%80%E5%8D%95%E7%9A%84pixiv%E5%8F%8D%E4%BB%A3.html)

<div align="center">

<img src="https://user-images.githubusercontent.com/36563862/175779656-fbd1bd56-e0e1-46db-b028-0e33d018792e.png" width="200" height="200" alt="排队姬">

# go-pixiv-proxy
_✨ 一个简单易懂的p站图片代理！ ✨_

</div>

<p align="center">
  <a href="https://raw.githubusercontent.com/Akegarasu/go-pixiv-proxy/master/LICENSE">
    <img src="https://img.shields.io/github/license/Akegarasu/go-pixiv-proxy" alt="license">
  </a>
  <a href="https://github.com/Akegarasu/go-pixiv-proxy/releases">
    <img src="https://img.shields.io/github/v/release/Akegarasu/go-pixiv-proxy?color=blueviolet&include_prereleases" alt="release">
  </a>
  <a href="https://goreportcard.com/report/github.com/Akegarasu/go-pixiv-proxy">
    <img src="https://goreportcard.com/badge/github.com/Akegarasu/go-pixiv-proxy" alt="GoReportCard">
  </a>
</p>

<p align="center">
  <a href="https://github.com/Akegarasu/go-pixiv-proxy/releases">下载</a>
  ·
  <a href="https://github.com/Akegarasu/go-pixiv-proxy/blob/main/README.md">文档</a>
</p>

# 简介

一个简单易懂的p站图片代理！

# 使用说明

## 部署

### 直接部署

从 [release](https://github.com/Akegarasu/go-pixiv-proxy/releases) 下载对应系统的可执行文件直接运行

### 启动参数

`-h`: host 默认 127.0.0.1

`-p`: 端口 默认 18090

`-d`: 指定域名（用于主页展示示例图片可以不填）

### 环境变量

注意：环境变量会 **默认覆盖** 启动参数

`GPP_HOST`: host

`GPP_PORT`: 端口

`GPP_DOMAIN`: 域名


## 代理图片

提供了两种代理的方法

### 替换 `i.piximg.net` 为你的域名

https://i.pximg.net/img-original/img/2022/05/21/22/35/46/98505703_p0.jpg

替换为

http://example.com/img-original/img/2022/05/21/22/35/46/98505703_p0.jpg

### url 后接 pid

http://example.com/98505703

## 图片质量选择

针对 **url 后接 pid** 的使用方法，提供了图片质量选择的参数

使用方法：添加参数 `t`

支持

- original
- regular
- small
- thumb
- mini

例子: http://example.com/98505703?t=original


## 代理 api

http://example.com/api/pid

## 其他示范用例

```
1. http://example.com/$path
- http://example.com/img-original/img/0000/00/00/00/00/00/12345678_p0.png

2. http://example.com/$pid[/$p][?t=original|regular|small|thumb|mini]
- http://example.com/12345678 (p0)
- http://example.com/12345678/0 (p0)
- http://example.com/12345678/1 (p1)
- http://example.com/12345678?t=small (small image)
```
