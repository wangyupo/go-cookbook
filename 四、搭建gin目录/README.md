## 搭建gin目录

安装ORM依赖 gorm

```
go get -u gorm.io/gorm
go get -u gorm.io/driver/msyql
```

安装从.env加载环境变量依赖 godotenv

```
go get github.com/joho/godotenv
```

创建数据库，字符集选 `utf8mb4`，排序规则选 `utf8mb4_general_ci`

model 结构体字段声明必须是 “大写驼峰”