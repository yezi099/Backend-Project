# 通讯录后端

这是一个基于 Spring Boot 的通讯录后端项目，提供联系人管理的相关功能，包括增删改查、登入注销账号等。

## 技术栈

- Java 8+
- Spring Boot
- Spring Data JPA
- MySQL

## 目录结构

- `com.example.Application` - 启动类
- `com.example.controller.UserController` - 用户管理的 RESTful API 控制器
- `com.example.service.UserService` - 业务逻辑处理层
- `com.example.dao.UserRepository` - 数据访问层，使用 Spring Data JPA 操作数据库
- `com.example.entity.User` - 用户实体类

## 安装与运行

1. **克隆项目**：
   ```bash
   git clone https://github.com/yezi099/Backend-Project.git
2. **进入项目目录**
  在 `application.yml` 中设置 MySQL 数据库连接信息。

    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name?useSSL=false&serverTimezone=UTC
    spring.datasource.username=your_username
    spring.datasource.password=your_password
    spring.jpa.hibernate.ddl-auto=update

3. **运行项目:**
   mvn spring-boot:run
4. **API 访问：**
   项目启动后，访问 http://localhost:8888 进行接口调用。

## 接口说明

1. **新增联系人**  
   - **URL**：`POST /user`  
   - **请求体**：User 对象，JSON 格式  
   - **示例**：
   ```json
   {
     "姓名": "张三",
     "登入密码": 123456,
     "联系电话": "12312341234",
     "电子邮件": "123456789@qq.com"
   }

2. **更新联系人**
- **URL**：`PUT /user`  
- **请求体**：User 对象，包含 id  
- **示例**：
  ```json
  {
     "姓名": "张三",
     "登入密码": 123456,
     "联系电话": "11111111111",
     "电子邮件": "111111111@qq.com"
  }

3. **删除联系人**
- **URL**：`DELETE /user/{id}`  
- **参数**：id - 联系人 ID  

4. **获取用户信息**
- **URL**：`/user/info?token=xxx`  

5. **登录**
- **URL**：`/user/login`  

6. **注销**
- **URL**：`/user/logout`  
  

## 联系方式
 如有任何问题，请联系848587789@qq.com


