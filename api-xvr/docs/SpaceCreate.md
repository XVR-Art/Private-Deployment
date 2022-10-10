# 创建空间

### 接口地址

https://{host}/v1/space/create

#### 业务参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>hub_sid</td>
      <td>空间SID, 唯一, 不传入则会自动生成</td>
    </tr>
    <tr>
      <td>created_by_account_id</td>
      <td>所属用户, 即用户的 account_id</td>
    </tr>
    <tr>
      <td>scene_sid</td>
      <td>场景SID</td>
    </tr>
    <tr>
      <td>name</td>
      <td>名称</td>
    </tr>
    <tr>
      <td>description</td>
      <td>描述</td>
    </tr>
    <tr>
      <td>room_size</td>
      <td>房间大小, 即可以同时容纳多少人, 范围: 1-50</td>
    </tr>
    <tr>
      <td>entry_mode</td>
      <td>状态, 可选值: allow/deny</td>
    </tr>
</table>

#### 成功返回示例

```json
{
    "code": 0,
    "msg": "OK",
    "result": {
        "hub_sid": "jde5lui"
    }
}
```
