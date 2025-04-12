## 프론트엔드 프로젝트 생성

프론트 스터디 코드를 깃 풀 받거나,

``` bash
# 1. 프로젝트 생성
npm create vite@latest study-deploy-frontend -- --template vue-ts

# 2. 프로젝트 디렉토리로 이동
cd study-deploy-frontend

# 3. 의존성 설치
npm install

# 4. 개발 서버 실행
npm run dev
```

![image](https://github.com/user-attachments/assets/ad659e30-e84a-4a3d-b36c-8dfa98caf433)


## 백엔드엔드 Spring Boot (Gradle, Java 17) 프로젝트 생성

Spring Initializr 사용

Project: Gradle (Groovy OK)
Language: Java 20
Spring Boot: 3.4.x

Dependencies
  - Spring Web
  - Spring Security
  - Spring Data JPA
  - Spring Boot DevTools
  - Lombok
  - MySQL Driver


## Docker 로 MySQL 띄우기
``` bash
version: '3.8'

services:
  mysql:
    image: mysql:8.0
    container_name: demo-mysql
    restart: always
    ports:
      - "3306:3306"
    environment:
      MYSQL_ROOT_PASSWORD: root
      MYSQL_DATABASE: demo_db
      MYSQL_USER: admin
      MYSQL_PASSWORD: 1234
    command:
      [
        "--character-set-server=utf8mb4",
        "--collation-server=utf8mb4_unicode_ci",
        "--default-time-zone=UTC"
      ]
    volumes:
      - mysql_data:/var/lib/mysql

volumes:
  mysql_data:

```


