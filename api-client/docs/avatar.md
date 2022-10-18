# 获取自定义头像接口

### 功能描述

客户侧可以实现自定义用户3D头像, 提供此接口供空间调用。

<table width="100%">
    <tr>
      <th width="25%">项目</th>
      <th>值</th>
    </tr>
    <tr>
      <td>接口地址</td>
      <td>https://{you_api_server}/api/v1/space/assets/avatar</td>
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
      <td>邮箱</td>
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
      <td>result.avatar</td>
      <td>头像地址, 例如: https://{assets_gateway}/xxx.glb</td>
    </tr>
</table>

#### 成功返回示例

```json
{
  "code": 200,
  "msg": "OK",
  "result": {
    "avatar": "https://{assets_gateway}/xxx.glb"
  }
}
```
