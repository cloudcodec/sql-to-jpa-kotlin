# sql-to-jpa-kotlin
generate jpa's things

## structure
```
src
└── main
    └── kotlin
        ├── com.example (right click,input sql)
```
```
CREATE TABLE `tb_service_account`(
    `id` BIGINT  NOT NULL AUTO_INCREMENT COMMENT 'id comment',
    `name` VARCHAR(255) NOT NULL COMMENT 'name comment',
    `created_time` DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP COMMENT '创建时间',
    `updated_time` DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP COMMENT '更新时间',
    PRIMARY KEY(`id`)
)
```

## output
```
"com.example.entity.${entityName}PO",
"com.example.mapper.${entityName}Mapper",
"com.example.dao.${entityName}DAO",
```

# ref
https://mybatis.org/generator/running/runningWithJava.html
```
org.mybatis.generator.api.dom.kotlin.render.KotlinFileRenderer
```

https://github.com/Wohoo22/mapping-generator-intellij-plugin
