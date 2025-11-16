# weixin447-springboot线上租房平台

## 前言

欢迎来到我们的线上租房平台项目——weixin447-springboot。这是一个集响应式、三端（PC、小程序、移动端）于一体的租房平台。通过这个项目，我们希望能够帮助用户便捷、高效地找到心仪的住房，同时也为房东提供了一个管理房源、发布租房信息的平台。

## 内容介绍

本项目主要包括以下几个功能模块：房源展示、房源搜索、租房申请、用户中心、房东中心等。房源展示模块提供了详细的房源信息，包括房屋图片、租金、地理位置等；房源搜索模块支持多种筛选条件，帮助用户快速找到合适的房源；租房申请模块简化了租房流程，提高了租房效率；用户中心和房东中心分别提供了用户和房东相关的功能，如个人信息管理、房源管理等。

## 技术介绍

本项目采用以下技术栈：

- 语言：Java
- 使用框架：Spring Boot、Spring MVC、MyBatis、微信小程序
- 前端技术：JS、Vue、CSS3、Uniapp
- 开发工具：IDEA/Eclipse、Uniapp
- 数据库：MySQL 5.7/8.0
- 数据库管理工具：phpstudy/Navicat
- JDK版本：jdk1.8
- Maven：apache-maven 3.8.1-bin
- 前端环境：Node.Js 12/14/16

## 核心代码

以下为房源展示模块的部分核心代码：

```java
// 查询房源列表
public List<House> listHouses(HouseQuery query) {
    PageHelper.startPage(query.getPageNum(), query.getPageSize());
    return houseMapper.listHouses(query);
}
```

```html
<!-- 房源列表页面 -->
<template>
  <div>
    <van-pull-refresh v-model="isLoading" @refresh="onRefresh">
      <van-list
        v-model="loading"
        :finished="finished"
        finished-text="没有更多了"
        @load="loadHouses"
      >
        <house-item
          v-for="house in houses"
          :key="house.id"
          :house="house"
        ></house-item>
      </van-list>
    </van-pull-refresh>
  </div>
</template>
```

## 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

## 项目截图
