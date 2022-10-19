# 空间访问鉴权接口

### 功能描述

用户在进入空间时, 会把用户信息以 x-www-form-urlencoded 的方式 POST 至您的服务器进行鉴权, 鉴权通过后用户才能进入此空间, 您需要实现自己的鉴权逻辑, 并按下面指定的格式返回鉴权结果。

<table width="100%">
    <tr>
      <th width="25%">项目</th>
      <th>值</th>
    </tr>
    <tr>
      <td>接口地址</td>
      <td>https://{you_api_server}/api/v1/space/auth/check</td>
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
      <td>字符串, 用户邮箱, 以此参数和自有业务系统的账号对接, 如果用户未登录则为空</td>
    </tr>
    <tr>
      <td>hub_id</td>
      <td>字符串, 空间SID, 注意: 此字段传入的其实是 hub_sid 的值</td>
    </tr>
    <tr>
      <td>hub_url</td>
      <td>字符串, 空间地址</td>
    </tr>
    <tr>
      <td>access_token</td>
      <td>(可选)一次性授权码, 如果当前页面地址上携带了此参数则原样传入, 客户侧系统可根据此值做更多的鉴权检测逻辑</td>
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
      <td>result.access</td>
      <td>是否允许进入: approved(允许), denied(拒绝)</td>
    </tr>
    <tr>
      <td>result.fallback_url</td>
      <td>access = denied 时的跳转地址</td>
    </tr>
    <tr>
      <td>result.logo_url</td>
      <td>当前空间的LOGO地址, 返回空则使用默认的LOGO</td>
    </tr>
</table>

#### 鉴权成功返回示例

```json
{
  "code": 200,
  "msg": "OK",
  "result": {
    "access": "approved",
    "fallback_url": "",
    "logo_url": ""
  }
}
```

#### 鉴权失败返回示例

```json
{
  "code": 400,
  "msg": "您无权进入空间",
  "result": {
    "access": "denied",
    "fallback_url": "http://your_fallback_url",
    "logo_url": "",
  }
}
```
