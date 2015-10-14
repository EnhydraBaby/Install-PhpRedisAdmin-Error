# Install-PhpRedisAdmin
安装phpRedisAdmin可视化工具，在配置phpRedisAdmin,访问远程redis时报错
报错信息：
Fatal error: Uncaught exception 'Predis\Response\ServerException' with message 'ERR unknown command 'SCAN'' in ....../vendor/src/Client.php on line 365
Predis\Response\ServerException: ERR unknown command 'SCAN' in ....../vendor/src/Client.php on line 365
报错原因：
是由于你所用的redis版本不支持SCAN命令，redis版本低所导致的
解决方法：
在config.inc.php文件中
将'keys' => false改为'keys' => true即可

