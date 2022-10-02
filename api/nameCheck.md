# 名称鉴敏接口

### 功能描述

用户修改自己的昵称或空间名称前, 会把名称信息以 x-www-form-urlencoded 的方式 POST 至您的服务器进行鉴黄鉴敏。

检查通过后可以根据当前类型更新对应记录的名称, 以实现名称同步功能。

<table width="100%">
    <tr>
      <th width="25%">项目</th>
      <th>值</th>
    </tr>
    <tr>
      <td>接口地址</td>
      <td>https://{you_api_server}/api/v1/space/auth/nameCheck</td>
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
      <td>type</td>
      <td>类型: nickname(昵称), spacename(空间名称)</td>
    </tr>
    <tr>
      <td>name</td>
      <td>名称</td>
    </tr>
    <tr>
      <td>email</td>
      <td>用户邮箱, 已登录用户修改昵称时有此值</td>
    </tr>
    <tr>
      <td>hub_id</td>
      <td>空间ID, type=spacename时有此值</td>
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
      <td>result.risk</td>
      <td>是否有风险: 0或1</td>
    </tr>
</table>

#### 成功返回示例

```json
{
  "code": 200,
  "msg": "OK",
  "result": {
    "risk": 0
  }
}
```

#### 失败返回示例

```json
{
  "code": 400,
  "msg": "敏感内容, 请勿使用",
  "result": {
    "risk": 1
  }
}
```
