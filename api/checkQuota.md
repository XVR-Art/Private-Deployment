# 空间创建鉴权接口

### 功能描述

用户创建空间前, 会把用户信息以 x-www-form-urlencoded 的方式 POST 至您的服务器进行鉴权, 鉴权通过后才能继续创建空间。

<table width="100%">
    <tr>
      <th width="25%">项目</th>
      <th>值</th>
    </tr>
    <tr>
      <td>接口地址</td>
      <td>https://{you_api_server}/api/v1/space/room/checkQuota</td>
    </tr>
    <tr>
      <td>提交方式</td>
      <td>POST</td>
    </tr>
    <tr>
      <td>参数格式</td>
      <td>x-www-form-urlencoded</td>
    </tr>
</table>

#### 请求参数列表

<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>email</td>
      <td>字符串, 用户邮箱</td>
    </tr>
</table>

#### 返回参数列表 (json)

<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>code</td>
      <td>HTTP状态码, eg: 200</td>
    </tr>
    <tr>
      <td>msg</td>
      <td>消息, eg: OK</td>
    </tr>
    <tr>
      <td>result.quota</td>
      <td><=0 禁止创建, >0 允许创建</td>
    </tr>
</table>

#### 鉴权成功返回示例

```json
{
  "code": 200,
  "msg": "OK",
  "result": {
    "quota": 1
  }
}
```

#### 鉴权失败返回示例

```json
{
  "code": 400,
  "msg": "您无权创建空间",
  "result": {
    "quota": 0
  }
}
```
