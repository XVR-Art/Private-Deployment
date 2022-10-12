# 获取空间详情

### 接口地址

{api_gateway}/v1/space/detail

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

#### 返回参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>hub_id</td>
      <td>空间ID, bigint</td>
    </tr>
    <tr>
      <td>hub_sid</td>
      <td>空间SID, varying(255), 唯一, 用于URL, 可拼接出空间地址, 例如: {main_domain}/{hub_sid}</td>
    </tr>
    <tr>
      <td>name</td>
      <td>名称, varying(255)</td>
    </tr>
    <tr>
      <td>description</td>
      <td>描述, varying(255)</td>
    </tr>
    <tr>
      <td>entry_mode</td>
      <td>状态, allow: 允许; deny: 禁用</td>
    </tr>
    <tr>
      <td>scene_id</td>
      <td>场景ID, bigint</td>
    </tr>
    <tr>
      <td>room_size</td>
      <td>空间大小, integer, 可同时容纳的在线人数</td>
    </tr>
    <tr>
      <td>max_occupant_count</td>
      <td>最大在线人数(含大厅), integer</td>
    </tr>
    <tr>
      <td>created_by_account_id</td>
      <td>拥有者账号ID, bigint</td>
    </tr>
    <tr>
      <td>last_active_at</td>
      <td>最后活跃时间, timestamp(0) without time zone</td>
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
