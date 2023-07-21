# Azukisan API - 一个简单的用来随机获取可爱小豆泥图片的网络API

[EN](https://github.com/SuperLangdon/azukisan-api/README_EN.md) | 简体中文

## 介绍

《世界，就是绕着猫打转：暹罗猫小豆泥是世界的中心》（シャム猫あずきさんは世界の中心）是日本漫画家Nobeko创作的作品。故事中的暹罗猫小豆泥是作者养的宠物，它常常向饲主撒娇，喜欢独占注意力，还会嫉妒其他人。小豆泥的行为经常引发令人捧腹大笑的事件，漫画中收录了它奇妙又可爱的举动，如喜欢下雨但不喜欢洗澡，喜欢烤鲭鱼但不吃鲭鱼猫罐头等。这个作品深受爱猫人士的喜爱，围绕着“暹罗猫小豆泥”这个形象，产生了许多衍生内容和同人（同猫？）创作。

<img src="https://cdn.jsdelivr.net/gh/SuperLangdon/image-hosting/202306161507360.webp" alt="《世界，就是绕着猫打转：暹罗猫小豆泥是世界的中心》" width="25%" />

本API即是基于这些作品而创建。


## 版权

本API的图片来源于日本漫画家Nobeko创作的作品《世界，就是绕着猫打转：暹罗猫小豆泥是世界的中心》（シャム猫あずきさんは世界の中心），及其同人作品，其版权归Nobeko及同人作品相关权利人所有。

## 用途

当你请求这个API时，随机返回一张暹罗猫小豆泥相关的图片。

## 基本信息

Base URL：https://api.example.com/azukisan

请求方式：GET

返回格式：JSON

## 参数

| 字段   | 描述                                         |
| ------ | -------------------------------------------- |
| type   | 302 (默认)<br>json（支持跨域）                 |
| site   | 施工中，暂未完成支持。 |
| size   | large（大尺寸图片，500\*500及以上分辨率）<br>small（小尺寸图片，500*500及以上分辨率）<br>all（全部）-（默认） |
| proxy  | 1（使用反向代理）-（默认）<br>0（302返回源站链接） |
| tag    | 无默认值<br>筛选指定分类的图片。<br>施工中，暂未完成支持。

## 错误处理
当 API 请求出错时，将返回适当的 HTTP 状态码和错误消息。

| HTTP状态码 | 错误消息                                        |
| ----------- | ----------------------------------------------- |
| 400         | 请求无效或缺少必需参数。                         | 
| 404         | 请求的资源不存在。                               |
| 500         | 服务器发生错误。                                 |

## 响应示例

```python
import requests

base_url = "https://api.example.com/azukisan"

# 设置请求参数
params = {
    "type": "302",
    "size": "large",
    "proxy": "1",
    "tag": ""
}

# 发起 GET 请求
response = requests.get(base_url, params=params)

# 获取 JSON 响应内容
json_data = response.json()

# 处理返回的 JSON 数据
print(json_data)

```
