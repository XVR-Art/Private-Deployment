# 空间创建同步接口

### 功能描述

用户创建空间后, 会把空间信息以 x-www-form-urlencoded 的方式 POST 至您的服务器进行数据同步, 方便后续的管理维护。

<table width="100%">
    <tr>
      <th width="25%">项目</th>
      <th>值</th>
    </tr>
    <tr>
      <td>接口地址</td>
      <td>https://{you_api_server}/api/v1/space/room/create</td>
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
      <td>用户邮箱</td>
    </tr>
    <tr>
      <td>name</td>
      <td>空间名称</td>
    </tr>
    <tr>
      <td>scene_id</td>
      <td>场景ID</td>
    </tr>
    <tr>
      <td>hub_id</td>
      <td>空间ID</td>
    </tr>
    <tr>
      <td>hub_url</td>
      <td>空间地址</td>
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
      <td>result</td>
      <td>null</td>
    </tr>
</table>

#### 成功返回示例

```json
{
  "code": 200,
  "msg": "OK",
  "result": null
}
```

#### 失败返回示例

```json
{
  "code": 400,
  "msg": "保存失败",
  "result": null
}
```
