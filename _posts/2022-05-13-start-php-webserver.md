## php 命令启动 www 服务

> https://www.php.net/manual/zh/features.commandline.webserver.php

php已经支持内置的webserver。也就是说：可以不使用apache，也不使用nginx，只要你的命令行能够识别php这个命令，那么就可以通过这个php命令，来启动一个www服务

```shell
cd <www_root>/
php -S localhost:8000
```