### Sql代码生成器 支持 Oracle 以及 Mysql

项目取自mybatis-plus提供的代码生成器（ [sample地址](https://github.com/baomidou/mybatis-plus-samples)）并做对oracle数据库的优化。

开箱即用，无需过多配置!

usage:

1. 将项目clone到本地工程

2. 修改application.properties文件中的配置

     2.1 使用mysql, 只需要修改mysql下的配置

     2.2 使用oracle, ***注意***： 如果使用oracle,配置文件中需要设置 `system.oracle-schema`的值，否则可能出现		只生成目录，不生成文件的现象！Mysql可以不设置该值。

3. 运行 `com.immango.generator` 包下的CodeGenerator.java

4. 其他进阶配置请参考Mybatis-plus代码生成器 ( [配置文档](https://mp.baomidou.com/guide/generator.html) )