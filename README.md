#LegendSock2.2Happy版#

#用法#

LegendSock 2.2 开心版 授权码 LegendSock-7c88c80c90e05999 whmcs ss 插件 破解无 授权

#授权#

下面这代码，是一个简易的签发域名授权SS的

<?php
$domain = $_GET["domain"];
$beginChars = substr($domain, 0, 4);
$endChars = substr($domain, 0 - 4, 4);
$reversal = strrev($domain);
$md5 = md5(md5(md5($domain . $reversal) . md5($beginChars) . md5($endChars)));
?>
<html>
<head>
<meta charset="utf-8">
<title>Shadowsocks授权</title>
</head>
<body>
<p>神奇海螺Shadowsocks授权</br>WHMCS对接SS插件</p>
<form method="get">
域名: <input type="text" name="domain">
<input type="submit" value="提交">
</form>
<pre>
授权域名：<?php echo $_GET["domain"];?> 
授权密钥： <input type="text" value="<?php echo $md5; ?> ">
只能在PHP5.6下使用，7.0不可用。
</pre>
</body>
</html>
