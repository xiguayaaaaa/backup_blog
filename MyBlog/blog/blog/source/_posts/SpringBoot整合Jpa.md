---
title: SpringBoot整合Jpa
date: 2022-07-05 13:17:33
tags:
- 知识
categories:
- SpringBoot
cover: https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg2020.cnblogs.com%2Fblog%2F2331630%2F202107%2F2331630-20210721141158611-538846916.png&refer=http%3A%2F%2Fimg2020.cnblogs.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1659501639&t=2f8efd79e607e9df171c317efc448f26
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from:
---
SpringBoot整合Jpa
<!-- more -->


1.添加依赖

```SQL
<dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-jpa</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-jdbc</artifactId>
        </dependency>
```

2.配置数据源

```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/student?serverTimezone=Asia/Shanghai
    username: root
    password: root
    driver-class-name: com.mysql.cj.jdbc.Driver
  jpa:
    #打印SQL语句
    show-sql: true
    #使用测试用例时需要配置该项
    properties:
      hibernate:
        enable_lazy_load_no_trans: true
```

3.新建实体类，并建立映射关系

```java
@Table(name = "student")
@Entity
@Data
public class Student {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer studentId;
    @Column(name = "student_name")
    private String studentName;
    @Column(name = "student_gender")
    private String studentGender;
    @Column(name = "student_age")
    private String studentAge;
}

```

@Table：用于表明该实体类对应的是数据库中的哪张表，name属性用于配置表名。

@Entity：JPA要求实体类上需要标注该注解

@Id：在标注了@Entity的类上必须有一个字段标注该注解，该注解用于表明标注了此注解的字段是主键。

@GeneratedValue：用于表明该主键的生成策略，通常和@Id同时出现

@Column：该注解并不是必须的，通常用于表明该变量对应的数据库表字段，如果字段名称使用经典命名法，而变量名称使用了驼峰命名法，则此注解可以省略

### JpaRepository接口详解

```sql
public interface JpaRepository<T, ID> extends PagingAndSortingRepository<T, ID>, QueryByExampleExecutor<T> {
	//查询所有的数据
    List<T> findAll();
	//查询所有的数据，并排序，排序的字段及排序方式通过Sort对象指定
    List<T> findAll(Sort sort);
	//根据ID批量查询
    List<T> findAllById(Iterable<ID> ids);
	//批量保存
    <S extends T> List<S> saveAll(Iterable<S> entities);
	//刷新缓存
    void flush();
	//保存并刷新缓存
    <S extends T> S saveAndFlush(S entity);
	//批量保存并刷新缓存
    <S extends T> List<S> saveAllAndFlush(Iterable<S> entities);
	//批量删除
    void deleteAllInBatch(Iterable<T> entities);
	//通过ID批量删除
    void deleteAllByIdInBatch(Iterable<ID> ids);
	//等价于删除全部数据
    void deleteAllInBatch();
	//通过ID查询
    T getById(ID id);
	//通过示例批量查询
    <S extends T> List<S> findAll(Example<S> example);
	//通过示例批量查询
    <S extends T> List<S> findAll(Example<S> example, Sort sort);
}

```
