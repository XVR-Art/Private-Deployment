# 获取场景列表

#### 接口地址

{api_gateway}/v1/scene/list

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

#### 返回参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>scene_id</td>
      <td>场景ID, bigint</td>
    </tr>
    <tr>
      <td>scene_sid</td>
      <td>场景SID, varying(255), 唯一, 用于URL, 可拼接出场景详情页, 例如: {main_domain}/scenes/{scene_sid}</td>
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
      <td>state</td>
      <td>状态, active: 可用; delisted: 下架</td>
    </tr>
    <tr>
      <td>screenshot_uuid</td>
      <td>缩略图UUID, varying(255), 用于拼接出缩略图地址, 例如: {thumb_gateway}/files/{screenshot_uuid}</td>
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
            "state": "active",
            "screenshot_uuid": "24861671-e634-42a2-8920-11a501062284"
        }
    ]
}
```
