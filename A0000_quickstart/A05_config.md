# 平台配置管理

## 业务线管理

业务线是用例属性的一级分类，需与模块关联,本系统中用例可拥有共两级分类，以区分用例所属的团队、功能、范围等信息

## 模块管理

模块是用例属性的二级分类，需与业务线关联,本系统中用例可拥有共两级分类，以区分用例所属的团队、功能、范围等信息

## 业务线模块关联关联

多对多关系管理业务线与模块

## 来源管理

标记HTTP接口来源

## 数据服务器管理

发送请求的数据服务器配置，一个数据服务器可关联多个环境，可配置服务器的 DB、Redis ,且可配置多个 主键值分别为 [DB] / [REDIS]

数据服务器 Key值 与 名称 添加后不可修改

例：

[DB]
host = 0.0.0.0
port = 3306

[DB-test]
host = 192.168.0.1
port = 3305

## 环境配置管理

请求的环境，多个环境可指向同一个数据服务器，与数据服务器是多对一的关系

环境配置 key值 与 名称 添加后不可修改

执行时是否显示： 在执行时是否显示此环境

## uri管理

系统中使用uri来管理服务器的域名，此处只是添加一个空的uri，在前台中配置各环境的uri

优先级：数字越小，默认显示的uri排序越靠前

uri管理 key值 与 名称 添加后不可修改

## 服务管理

分布式中对slave的管理，服务在启动时根据根目录config.ini 注册到master，注册后自动在此页面新增slave信息，
默认执行任务进程最大数和调试进程最大数为0，在此页面配置进程数。

## 执行Python代码管理

关于执行Python代码的时间以及默认引入库的配置，建议使用初始值，超过限定时间会强制停止线程执行，返回超时提示。

在使用三方库时需先在服务器上安装库











