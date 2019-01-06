# thinkphp-migration

```
composer require ke/thinkphp-migration
```


## Breakpoint 命令

> Breakpoint 命令用来设置断点，可以使你对回滚进行限制。你可以调用 breakpoint 命令不带任何参数，即将断点设在最新的迁移脚本上

```
php think migrate:breakpoint -e development
```

> 可以使用 -t 来指定断点打到哪个迁移版本上

```
php think migrate:breakpoint -e development -t 20120103083322
```

> 可以使用 -r 来移除所有断点

```
php think migrate:breakpoint -e development -r
```

> 当你运行 status 命令时可以看到断点信息

## Create 命令

> create 命令用来创建迁移脚本文件。需要一个参数：脚本名。迁移脚本命名应该保持 驼峰命名法

```
php think migrate:create MyNewMigration
```

## Run 命令

> Run 命令默认运行执行所有脚本，可选指定环境

```
php think migrate:run -e development
```

> 可以使用 -t 来指定执行某个迁移脚本

```
php think migrate:run -e development -t 20110103081132
```

## Rollback 命令

> Rollback 命令用来回滚之前的迁移脚本。与 Run 命令相反。
> 你可以使用 rollback 命令回滚上一个迁移脚本。不带任何参数

```
php think migrate:rollback -e development
```

> 使用 -t 回滚指定版本迁移脚本

```
php think migrate:rollback -e development -t 20120103083322
```

> 指定版本如果设置为0则回滚所有脚本

```
php think migrate:rollback -e development -t 0
```

> 可以使用 -d 参数回滚指定日期的脚本

```
php think migrate:rollback -e development -d 2012
php think migrate:rollback -e development -d 201201
php think migrate:rollback -e development -d 20120103
php think migrate:rollback -e development -d 2012010312
php think migrate:rollback -e development -d 201201031205
php think migrate:rollback -e development -d 20120103120530
```
