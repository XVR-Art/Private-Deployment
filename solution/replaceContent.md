# 自定义空间资源和打开链接


### 需求描述

空间主人需要自定义图片/视频/音频和点击时的打开链接。

### 实现过程

1. 建立所需数据库模型: scene, scene_assets, room, room_assets
   
2. 和设计师沟通场景设计, 确定好可以替换资源的位置和大小, 以及是否可以点击打开链接

3. 手动将场景添加到 scene 表, 并为其初始化设置 scene_assets 记录

4. 设计师使用固定的资源链接和打开链接应用于场景内

5. 添加空间 (room), 如果开启创建同步功能, 可以自动同步到此表, 此时可从 scene_assets 初始化一份默认的资源到 room_assets

6. 提供替换功能给用户, 让用户自定义 room_assets.url

7. 访问这些固定链接时, 系统根据当前设定, 跳转到具体的资源地址

### 场景模型必要字段

<table width="100%">
    <tr>
      <th width="25%">字段</th>
      <th>描述</th>
    </tr>
    <tr>
      <td>scene_id</td>
      <td>场景ID</td>
    </tr>
    <tr>
      <td>name</td>
      <td>场景名称</td>
    </tr>
</table>

### 场景资源模型必要字段

<table width="100%">
    <tr>
      <th width="25%">字段</th>
      <th>描述</th>
    </tr>
    <tr>
      <td>id</td>
      <td>ID</td>
    </tr>
    <tr>
      <td>scene_id</td>
      <td>场景ID</td>
    </tr>
    <tr>
      <td>name</td>
      <td>资源名称</td>
    </tr>
    <tr>
      <td>type</td>
      <td>资源类型, 例如: image, video, audio, link</td>
    </tr>
    <tr>
      <td>position</td>
      <td>资源位置, 图片/视频/音频在空间内的位置, 自定义, 例如: 1</td>
    </tr>
    <tr>
      <td>dimensions</td>
      <td>资源尺寸, 自定义字符串, 用于用户自定义上传内容时提示, 例如: 800x600</td>
    </tr>
    <tr>
      <td>url</td>
      <td>资源地址, 真实资源地址, 请求当前模型的固定链接时跳转到的真实地址</td>
    </tr>
</table>

### 空间模型必要字段

<table width="100%">
    <tr>
      <th width="25%">字段</th>
      <th>描述</th>
    </tr>
    <tr>
      <td>user_id</td>
      <td>用户ID, 空间创建同步时会传入email, 可以据此将空间绑定到具体的用户</td>
    </tr>
    <tr>
      <td>scene_id</td>
      <td>场景ID</td>
    </tr>
    <tr>
      <td>hub_id</td>
      <td>空间ID</td>
    </tr>
    <tr>
      <td>name</td>
      <td>空间名称</td>
    </tr>
</table>

### 空间资源模型必要字段

<table width="100%">
    <tr>
      <th width="25%">字段</th>
      <th>描述</th>
    </tr>
    <tr>
      <td>id</td>
      <td>ID</td>
    </tr>
    <tr>
      <td>hub_id</td>
      <td>空间ID</td>
    </tr>
    <tr>
      <td>name</td>
      <td>资源名称</td>
    </tr>
    <tr>
      <td>type</td>
      <td>资源类型, 例如: image, video, audio, link</td>
    </tr>
    <tr>
      <td>position</td>
      <td>资源位置, 图片/视频/音频在空间内的位置, 自定义, 例如: 1</td>
    </tr>
    <tr>
      <td>dimensions</td>
      <td>资源尺寸, 自定义字符串, 用于用户自定义上传内容时提示, 例如: 800x600</td>
    </tr>
    <tr>
      <td>url</td>
      <td>资源地址, 真实资源地址, 请求当前模型的固定链接时跳转到的真实地址</td>
    </tr>
</table>


### 固定链接示例

https://assets.yourdomain.com/getter?scene_id=xxx&position=1

上面是设计师使用的固定链接, 此时可获得 scene_assets.url 来进行资源跳转

https://assets.yourdomain.com/getter?scene_id=xxx&position=1&hub_id=yyy

上面是用户访问空间时的链接地址, 此时可获得 room_assets.url 来进行资源跳转
