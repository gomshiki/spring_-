# 스프링 입문 강의 정리

<br>

### 1. build.gradle 

```java
plugins {
	id 'java'
	id 'org.springframework.boot' version '3.2.0'
	id 'io.spring.dependency-management' version '1.1.4'
}

group = 'hello'
version = '0.0.1-SNAPSHOT'

java {
	sourceCompatibility = '17' // java version
}

repositories {
	mavenCentral() 	// 라이브러리를 MavenCentral 이라는 공개된 사이트에서 받아옵니다.
					// 필요하다면 받아올 사이트 URL 을 추가할 수 도 있습니다.
}

dependencies {
	implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'
	implementation 'org.springframework.boot:spring-boot-starter-web'
	testImplementation 'org.springframework.boot:spring-boot-starter-test' // 테스트 라이브러리
}

tasks.named('test') {
	useJUnitPlatform()
}

```