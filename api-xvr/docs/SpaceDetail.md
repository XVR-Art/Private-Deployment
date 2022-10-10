# 获取空间详情

### 接口地址

https://{host}/v1/space/detail

#### 业务参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>hub_sid</td>
      <td>空间SID</td>
    </tr>
</table>

#### 成功返回示例

```json
{
    "code": 0,
    "msg": "OK",
    "items": {
        "hub_sid": "56hBqY9",
        "name": "Magnificent Spicy Cosmos",
        "max_occupant_count": 0,
        "entry_mode": "allow",
        "scene_id": null,
        "host": null,
        "last_active_at": null,
        "embed_token": "7ba34f915c5cf00ebb9a5972fa3d1931",
        "embedded": false,
        "description": null,
        "room_size": null,
        "created_by_account_id": 1266348169189392386
    }
}
```
