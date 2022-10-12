# 更新场景

#### 接口地址

{api_gateway}/v1/scene/update

#### 业务参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>scene_id</td>
      <td>场景ID, bigint, 指定要更新的场景</td>
    </tr>
    <tr>
      <td>scene_sid</td>
      <td>场景SID, varying(255), 用于URL, 不建议更新此字段</td>
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
      <td>状态, 可选: active/delisted</td>
    </tr>
</table>

#### 成功返回示例

```json
{
    "code": 0,
    "msg": "OK"
}
```
