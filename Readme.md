##### Sql代码生成器 支持 Oracle 以及 Mysql

usage:

1. 将项目导入到本地工程

2. 修改application.properties文件中的配置

  2.1 使用mysql, 只需要修改mysql下的配置
  
  2.2 使用oracle, 注意： 如果使用oracle,配置文件中需要设置 `system.oracle-schema`的值，否则可能出现只生成目录，不生成文件的现象！Mysql可以不设置该值。

3. 其他的配置请参考Mybatis-plus官方文档