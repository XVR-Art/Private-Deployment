<p align="center">
    <a href="https://xvr.art/?ref=github" target="_blank">
        <img src="https://xvr.oss-cn-hangzhou.aliyuncs.com/common/logo-dark-icon.png" height="100px">
    </a>
    <h1 align="center">XVR元宇宙 - API接口文档</h1>
    <br>
    <p>XVR元宇宙致力于提供虚拟数字空间服务，为数字藏品赋能元宇宙，同时支持教育培训，会议空间，画廊展馆等空间。私有化部署的客户可以通过接口深度整合。</p>
    <br>
</p>

## API列表

1. 场景
   1. [场景列表](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/SceneList.md)
   2. [场景详情](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/SceneDetail.md)
   3. [更新场景](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/SceneUpdate.md)
2. 空间
   1. [空间列表](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/SpaceList.md)
   2. [空间详情](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/SpaceDetail.md)
   3. [创建空间](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/SpaceCreate.md)
   4. [更新空间(转移/启用/停用)](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/SpaceUpdate.md)
3. 账号
   1. [账号列表](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/AccountList.md)
   2. [账号详情](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/AccountDetail.md)
   3. [创建账号](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/AccountCreate.md)
   4. [更新账号(启用/停用)](https://github.com/XVR-Art/Private-Deployment/blob/master/api-xvr/AccountUpdate.md)


### 接口调用说明

1. 参数分为公共参数和业务参数, 公共参数带在URL上以GET方式传入, 业务参数使用 POST 方式提交 raw json

2. 接口返回内容默认为JSON

### 关键参数

<table width="100%">
    <tr>
        <th width="20%">参数</th>
        <th>说明</th>
    </tr>
    <tr>
        <td>API接口网关</td>
        <td>私有化部署后联系业务人员获取</td>
    </tr>
    <tr>
        <td>access_token</td>
        <td>令牌, 私有化部署后联系业务人员获取或重置</td>
    </tr>
    <tr>
        <td>secret_key</td>
        <td>密钥, 私有化部署后联系业务人员获取或重置</td>
    </tr>
</table>

### 公共参数列表

<table width="100%">
    <tr>
        <th width="20%">参数</th>
        <th>说明</th>
    </tr>
    <tr>
        <td>access_token</td>
        <td>令牌</td>
    </tr>
    <tr>
        <td>timestamp</td>
        <td>调用接口时的时间戳</td>
    </tr>
    <tr>
        <td>format</td>
        <td>响应内容的格式，默认为json，可选值：xml，json</td>
    </tr>
    <tr>
        <td>v</td>
        <td>API版本，目前只能是1.0，请传入1.0</td>
    </tr>
    <tr>
        <td>sign_method</td>
        <td>签名方法，目前只支持md5，请传入md5</td>
    </tr>
    <tr>
        <td>sign</td>
        <td>32位小写字符串，见下面的签名算法</td>
    </tr>
</table>

### 签名算法

所有提交的参数(公共参数和业务参数), 除了 sign 全部需要加入签名。

参数按键升序排列后，然后把键值拼接, 首位再拼接上sk(系统分配的接口密钥), MD5后小写处理即可。

```php
# 伪代码
sign = strtolower(md5(secret_key . k1 . v1 . k2 . v2 . secret_key))
```

```php
# 签名的PHP实现
function makeSign(array $params, string $secret_key): string
{
    ksort($params);
    $string = $secret_key;
    foreach ($params as $key => $val) {
        $string .= $key . $val;
    }
    $string .= $sesecret_keycret;
    
    return strtolower(md5($string));
}
```

### SDK支持

目前官方提供PHPSDK, 可以直接安装使用

[https://github.com/XVR-Art/phpsdk](https://github.com/XVR-Art/phpsdk)
