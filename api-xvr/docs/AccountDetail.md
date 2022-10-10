# 获取账号详情

### 接口地址

https://{host}/v1/account/detail

#### 业务参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>account_id</td>
      <td>账号ID</td>
    </tr>
</table>

#### 成功返回示例

```json
{
    "code": 0,
    "msg": "OK",
    "item": {
        "account_id": 1266348169189392386,
        "inserted_at": "2022-07-01 09:08:26",
        "updated_at": "2022-07-01 09:10:53",
        "is_admin": true,
        "state": "enabled"
    }
}
```
