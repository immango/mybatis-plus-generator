### Sql代码生成器 支持 Oracle 以及 Mysql

项目取自mybatis-plus提供的代码生成器（ [sample地址](https://github.com/baomidou/mybatis-plus-samples)）并做对oracle数据库的优化。

开箱即用，无需过多配置!

usage:

1. 将项目clone到本地工程

2. 修改application.properties文件中的配置

     2.1 使用mysql, 只需要修改mysql下的配置

     2.2 使用oracle, ***注意***： 如果使用oracle,配置文件中需要设置 `system.oracle-schema`的值(在oracle数据库中，使用查询语句查询某张表的信息，其中的owner属性就是对应这张表的oracle-schema的值)，否则可能出现		只生成目录，不生成文件的现象！Mysql可以不设置该值。
     
     2.3 同时，使用oracle数据库时，输入表名称的时候注意大小写（"TABLE_NAME" 和 "table_name" 可能会导致不一样的结果），小写的表名可能会导致只生成目录，不生成entity等文件。同时，如果发生只生成目录的情况，可以在数据库中执行如下语句 `SELECT * FROM ALL_TAB_COMMENTS WHERE OWNER='表所属用户' AND TABLE_NAME IN ('你的表名')` 如果该条语句执行为空值，则需要检查一下用户和表名是否完全正确，只有这条语句有输出，才能正确生成文件。

3. 运行 `com.immango.generator` 包下的CodeGenerator.java

4. 其他进阶配置请参考Mybatis-plus代码生成器 ( [配置文档](https://mp.baomidou.com/guide/generator.html) )
