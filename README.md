#LegendSock2.2Happy��#

#�÷�#
LegendSock 2.2 ���İ� ��Ȩ�� LegendSock-7c88c80c90e05999 whmcs ss ��� �ƽ��� ��Ȩ

#��Ȩ#
��������룬��һ�����׵�ǩ��������ȨSS��
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
<title>Shadowsocks��Ȩ</title>
</head>
<body>
<p>���溣��Shadowsocks��Ȩ</br>WHMCS�Խ�SS���</p>
<form method="get">
����: <input type="text" name="domain">
<input type="submit" value="�ύ">
</form>
<pre>
��Ȩ������<?php echo $_GET["domain"];?> 
��Ȩ��Կ�� <input type="text" value="<?php echo $md5; ?> ">
ֻ����PHP5.6��ʹ�ã�7.0�����á�
</pre>
</body>
</html>