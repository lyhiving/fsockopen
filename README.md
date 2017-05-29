# fsockopen
 [fsockopen](http://www.php.net/manual/zh/function.fsockopen.php) 是 [socket](http://baike.baidu.com/link?url=vEfhjKHoJNnb5eN2qzUIUtviPBG8zeEv8-PSGBFv7YyVE0JoRVGv_APfOLXCsFVtjaf3h12OSLvUwJaUPn_Wmq) 套接字链接的封装函数,除了有基本的常用的 [TCP://](http://baike.baidu.com/item/TCP%2FIP%E5%8D%8F%E8%AE%AE) 通信功能以外, 它还有其它强大的通信功能 [UDP:// ](http://baike.baidu.com/link?url=NpRzddM-7gSodefpLJ3Y9CaoYirrM6UVsymQ2dnPBU_O_q9GwWSc7imxtSwEcb-8RlBMbzr6wVTbTpmOk_bglx6FX9q8VLlF3NVQs7Yi0xzz5NArvxQAZpQJtgYBIclosdU6AkrAM7n6oJs1K8LfL_) unix:// / udg:// 等等各种协议 可先用 [stream_get_transports](http://php.net/manual/zh/function.stream-get-transports.php) 当前服务器已注册的套接字传输协议列表
 
[![image](http://oauth.sinaapp.com/svg/image.svg?c=97CA00&k=Language&v=PHP)](https://github.com/yakeing/fsockopen/blob/master/fsockopen_class.php)

[![image](http://oauth.sinaapp.com/svg/image.svg?c=8892BF&k=License&v=MPL2.0)](https://github.com/yakeing/fsockopen/blob/master/fsockopen_class.php)

[![image](http://oauth.sinaapp.com/svg/image.svg?c=007ec6&k=version&v=1.2)](https://github.com/yakeing/fsockopen/blob/master/fsockopen_class.php)


### 初始化参数
-----
>示例：
```php
    $fs = new fsockopen();
    $ret = $fs->init(
        10, //运行时长(秒)(可选)
        tcp, //传输协议(可选)
        true //阻塞模式开关(可选)
        );
```

### GET 获取网络资源
-----
>示例：
```php
    $ret = $fs->GET(
        $Url , //目标地址
        $Referer , //伪造来源地址(可选)
        $Cookie //本地Cookie(可选)
    );
```


### POST 提交表单
-----
>示例：
```php
    $ret = $fs->POST(
        $Url , //目标地址
        $Content , //提交内容 key/vvalue&...
        $Referer , //伪造来源地址(可选)
        $Cookie, //本地Cookie(可选)
        $ContentType //提交方式(可选)
    );
```

### POST 发送文件
-----
>示例：
```php
    $ret = $fs->POST_FILE(
        $Url , //目标地址
        $File, //文件/图片地址 ['01.jpg','02.jpg',...]
        $Referer , //伪造来源地址(可选)
        $Cookie, //本地Cookie(可选)
        $ContentType //提交方式(可选)
    );
```

