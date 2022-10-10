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
      <td>hub_id</td>
      <td>空间ID</td>
    </tr>
</table>

#### 成功返回示例

```json
{
    "code": 0,
    "msg": "OK",
    "item": {
        "hub_id": 1266348286336303108,
        "hub_sid": "56hBqY9",
        "name": "测试空间",
        "max_occupant_count": 0,
        "entry_mode": "allow",
        "scene_id": 1266457025731100701,
        "last_active_at": null,
        "embed_token": "7ba34f915c5cf00ebb9a5972fa3d1931",
        "embedded": false,
        "description": "又一个全新的VR空间",
        "room_size": 24,
        "created_by_account_id": 1338662375435272265
    }
}
```
