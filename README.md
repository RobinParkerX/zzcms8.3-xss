
## Component
zzcms 8.3 Download link:http://www.zzcms.net/download/zzcms83.zip
## Vulnerability location
**/uploadimg_form.php** line 67
![](https://github.com/RobinParkerX/zzcms8.3-xss/blob/master/image/1.png)
**imgid** parameter Directly from user input and no security filtering that cause a self_xss
## Vulnerability trigger condition
Triggered after user or admin login
![](https://github.com/RobinParkerX/zzcms8.3-xss/blob/master/image/2.png)
## POC
```
http://192.168.30.216/uploadimg_form.php?imgid="><script>alert(2)</script>"

```
![](https://github.com/RobinParkerX/zzcms8.3-xss/blob/master/image/3.png)
