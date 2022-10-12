# 创建账号

### 接口地址

{api_gateway}/v1/account/create

#### 业务参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>email</td>
      <td>邮箱, varying(255)</td>
    </tr>
    <tr>
      <td>state</td>
      <td>状态, 可选值: enabled/disabled</td>
    </tr>
</table>

#### 成功返回示例

```json
{
    "code": 0,
    "msg": "OK",
    "result": {
        "account_id": 1339481558767108179,
        "email": "test1@xvr.art"
    }
}
```
