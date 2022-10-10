# 获取空间列表

### 接口地址

https://{host}/v1/space/list

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
            "hub_sid": "FXBrZCd",
            "name": "Youthful Vicious Zone",
            "max_occupant_count": 0,
            "entry_mode": "allow",
            "scene_id": null,
            "host": "localhost",
            "last_active_at": null,
            "embed_token": "1a8e3f4e7b2e9cf6ea2e9a2acdea68eb",
            "embedded": false,
            "description": null,
            "room_size": null,
            "created_by_account_id": 1266348169189392386
        },
        {
            "hub_sid": "vVPV7nC",
            "name": "Vital Charming Outing",
            "max_occupant_count": 0,
            "entry_mode": "allow",
            "scene_id": 1266457025731100701,
            "host": "localhost",
            "last_active_at": null,
            "embed_token": "7f913485183e2c8f27210c0ec55c28db",
            "embedded": false,
            "description": null,
            "room_size": null,
            "created_by_account_id": null
        }
    ]
}
```
