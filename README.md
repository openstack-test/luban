## 项目简介

<p align="center">
  <a href="https://golang.google.cn/">
    <img src="https://img.shields.io/badge/Golang-1.17-green.svg" alt="golang">
  </a>
  <a href="https://gin-gonic.com/">
    <img src="https://img.shields.io/badge/Gin-1.7.4-red.svg" alt="gin">
  </a>
  <a href="https://gorm.io/">
    <img src="https://img.shields.io/badge/Gorm-1.21-orange.svg" alt="gorm">
  </a>
  <a href="https://redis.io/">
    <img src="https://img.shields.io/badge/redis-3.2.100-brightgreen.svg" alt="redis">
  </a>
  <a href="https://vuejs.org/">
    <img src="https://img.shields.io/badge/Vue-3.0.0-orange.svg" alt="vue">
  </a>
  <a href="https://antdv.com/docs/vue/introduce-cn/">
    <img src="https://img.shields.io/badge/Ant%20Design-2.2.x-blue.svg" alt="Ant Design">
  </a>
</p>

> LuBan 鲁班运维平台3.0， 本项目使用Go1.15.x、 Gin、Gorm开发， 前端使用的是Vue3+Ant Design2.2.x框架。


#### 项目源码
|     |   后端源码  |   前端源码  |
|---  |--- | --- |
|  github   |  https://github.com/dnsjia/luban   |  https://github.com/dnsjia/luban/luban_fe   |


## 使用说明
1. 启动后端
安装编译
```shell script
# 拉取代码
git clone https://github.com/dnsjia/luban.git
cd luban

# 启动服务前先创建etc/config.yaml，其中数据库部分配置如下所示
mysql:
  path: '192.168.1.96:3306'
  db-name: 'luban'
  username: 'root'
  password: '123456'

# 打包
go build main.go -o ./luban

# 启动
./luban
```

2. 初始化数据库
```bash
# windows执行以下脚本初始化数据库
init_db.bat

手动导入sql/luban_init.sql文件
```

3. 启动前端
```bash
cd luban_fe
npm install
npm run dev
```

4. 登录
初始账号: luban@qq.com 密码: test1234

#### 目前已经实现的功能
* 用户登录
  * LDAP/Email
  * 钉钉扫码登录(开源版暂未开放)
* 权限管理
* 用户注册登录
  * [如何配置LDAP](.)
  * [配置钉钉扫码](.)
- K8S多集群管理
  * [集群管理](.)
  * [节点管理](.)
  * [工作负载](.)
  * [存储管理](.)
  * [网络管理](.)
  * [配置管理](.)

- 资产管理
  * [远程连接](.)


## License
Everything is Apache License 2.0.

