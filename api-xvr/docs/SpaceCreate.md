# 创建空间

#### 接口地址

{api_gateway}/v1/space/create

#### 业务参数
<table width="100%">
    <tr>
      <th width="25%">参数</th>
      <th>说明</th>
    </tr>
    <tr>
      <td>hub_sid</td>
      <td>空间SID, varying(255), 唯一, 不传入则会自动生成</td>
    </tr>
    <tr>
      <td>created_by_account_id</td>
      <td>所属用户, bigint, 即用户的 account_id</td>
    </tr>
    <tr>
      <td>scene_id</td>
      <td>场景ID, bigint</td>
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
      <td>room_size</td>
      <td>房间大小, integer, 即可以同时容纳多少人, 范围: 1-50</td>
    </tr>
    <tr>
      <td>entry_mode</td>
      <td>状态, 可选值: allow/deny</td>
    </tr>
    <tr>
      <td>member_permissions</td>
      <td>成员权限, integer, 默认0, 从权限列表中选取项目, 按位或 (空间主人不受此权限限制)</td>
    </tr>
</table>

#### 权限列表

<table width="100%">
    <tr>
      <th width="25%">权限</th>
      <th>值(二进制)</th>
    </tr>
    <tr>
      <td>创建和移动物品</td>
      <td>000001</td>
    </tr>
    <tr>
      <td>创建相机</td>
      <td>000010</td>
    </tr>
    <tr>
      <td>创建手绘</td>
      <td>000100</td>
    </tr>
    <tr>
      <td>固定对象</td>
      <td>001000</td>
    </tr>
    <tr>
      <td>发送表情</td>
      <td>010000</td>
    </tr>
    <tr>
      <td>创建和移动物品</td>
      <td>100000</td>
    </tr>
</table>


#### 成功返回示例

```json
{
    "code": 0,
    "msg": "OK",
    "result": {
        "hub_id": 1339681349329485911,
        "hub_sid": "LoFkjN1"
    }
}
```
