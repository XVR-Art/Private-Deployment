# 获取场景列表

### 接口地址

https://{host}/v1/scene/list

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
            "scene_id": 1266457025731100701,
            "scene_sid": "5fi3HzB",
            "name": "测试修改",
            "description": null,
            "state": "active"
        }
    ]
}
```
