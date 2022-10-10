# 获取场景详情

### 接口地址

https://{host}/v1/scene/detail

#### 业务参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>scene_sid</td>
      <td>场景SID</td>
    </tr>
</table>

#### 成功返回示例

```json
{
    "code": 0,
    "msg": "OK",
    "items": {
        "scene_id": 1266457025731100701,
        "scene_sid": "5fi3HzB",
        "name": "测试修改",
        "description": null,
        "state": "active"
    }
}
```
