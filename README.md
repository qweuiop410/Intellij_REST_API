### Intellij로만든 REST API 기본형입니다.

+ 빠르고 편리한 SpringBoot를 사용했습니다
+ build.gradle에 아래 코드를 작성, 추가해 spring boot를 사용가능하게 해줍니다
+ 이후 External Libraries에 springframework 관련 라이브러리가 보이면 정상입니다.
  + -build.gradle
```
apply plugin: 'java'
apply plugin: 'eclipse'
apply plugin: 'org.springframework.boot'

buildscript {
    ext {
        springBootVersion = '1.5.8.RELEASE'
    }
    repositories {
        mavenCentral()
    }
    dependencies {
        classpath("org.springframework.boot:spring-boot-gradle-plugin:${springBootVersion}")
    }
}

group = 'com.sample.springboot'
version = '0.0.1-SNAPSHOT'
sourceCompatibility = 1.8

repositories {
    mavenCentral()
}

dependencies {
    compile('org.springframework.boot:spring-boot-starter-web')
    testCompile('org.springframework.boot:spring-boot-starter-test')
}
```

+ 요청
   + localhost:8080/hello
+ 결과
 ``` json
 {
   "code":0,
   "msg":"Hello Spring Boot!"
}
 ```
 

