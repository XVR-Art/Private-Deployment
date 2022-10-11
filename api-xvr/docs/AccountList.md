# 获取账号列表

### 接口地址

{api_gateway}/v1/account/list

#### 业务参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>page</td>
      <td>页码, 默认1</td>
    </tr>
    <tr>
      <td>page_size</td>
      <td>每页条数, 默认20, 最大100</td>
    </tr>
</table>

#### 成功返回示例

```json
{
    "code": 0,
    "msg": "OK",
    "items": [
        {
            "account_id": 1338662375435272265,
            "inserted_at": "2022-10-09 03:43:51",
            "updated_at": "2022-10-09 03:43:51",
            "is_admin": false,
            "state": "enabled"
        },
        {
            "account_id": 1338654529888976968,
            "inserted_at": "2022-10-09 03:28:16",
            "updated_at": "2022-10-09 03:28:16",
            "is_admin": false,
            "state": "enabled"
        }
    ]
}
```
