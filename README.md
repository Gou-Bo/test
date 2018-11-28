## 查询工单统计报表 ##

* 接口调用请求说明
    http请求方式: POST
    URL:/ceo/report/work_order/get?access_token={{ceo_access_token}}

* 输入参数说明

|参数|描述|是否可为空|
|startTime|开始时间|是|
|endTime|结束时间 |是|
|level1CategoryId|所属一级分类 |否|
|level2CategoryId|所属二级分类 |否|

* 错误码集合：
|错误码|描述|
|----|--- |
|-1|系统异常！请联系系统管理员|

* 输出参数说明
|参数|描述|是否可为空|
|---|----|---------|
|resultCode|返回码|否|
|resultMesg|返回信息|否|
|data|返回数据|是|

正确返回：
{
  "resultCode": "000000",
  "resultMesg": "请求处理成功",
  "data": {
    "workOrderCount": 1039,
    "doneCount": 384,
    "doneRate": 615,
    "avgResponseTime": 28,
    "avgDoneTime": 0
  }
}
```
