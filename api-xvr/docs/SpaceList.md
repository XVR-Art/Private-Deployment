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
            "hub_id": 1339677009332142166,
            "hub_sid": "hsgsQeR",
            "name": "测试空间-1665407985",
            "max_occupant_count": 0,
            "entry_mode": "allow",
            "scene_id": 1266457025731100701,
            "last_active_at": null,
            "embed_token": "e1b481ceaddb4768bba13ef78cd60571",
            "embedded": false,
            "description": "又一个全新的VR空间",
            "room_size": 10,
            "created_by_account_id": 1338662375435272265
        },
        {
            "hub_id": 1338817089216970834,
            "hub_sid": "jde5lui",
            "name": "测试空间-1665305475",
            "max_occupant_count": 0,
            "entry_mode": "allow",
            "scene_id": 1266457025731100701,
            "last_active_at": null,
            "embed_token": "26bdb2bead43fa194f269ee973040c54",
            "embedded": false,
            "description": "又一个全新的VR空间",
            "room_size": 10,
            "created_by_account_id": 1338662375435272265
        }
    ]
}
```
