# 실전! Querydsl
[실전! Querydsl - 인프런 | 강의](https://www.inflearn.com/course/Querydsl-%EC%8B%A4%EC%A0%84#)

# Related Information
[Querydsl - Unified Queries for Java](http://querydsl.com/)

# Trouble
문제:
`compileQuerydsl` gradle 실행 시

error log:
```
Unable to load class 'com.mysema.codegen.model.Type'.

This is an unexpected error. Please file a bug containing the idea.log file.
```
해법: `querydsl-apt` 추가
```groovy
...
buildscript {
    ext {
        queryDslVersion = "5.0.0"
    }
}
...

    annotationProcessor "com.querydsl:querydsl-apt:${queryDslVersion}"
```
설명:

