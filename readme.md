# openai-java
- github地址: https://github.com/TheoKanning/openai-java
- 最新的Maven仓库: https://mvnrepository.com/search?q=com.theokanning.openai
    - 这个仓库有三个包(api、client、service)
    - ```xml
         <dependency>
           <groupId>com.theokanning.openai-gpt3-java</groupId>
           <artifactId>{api|client|service}</artifactId>
           <version>version</version>       
         </dependency>
      ```
        - **api**: 包含与实际的 API 请求和响应模型有关的类。这可能包括请求参数、响应结构等。(OpenAI GPT API 的基本 java 对象)
        - **client**: 通常包含用于与 API 进行通信的客户端类。这些类可能负责创建请求、发送请求到 API，并将响应转换为 Java 对象。(OpenAI GPT API的基本客户端)
        - **service**: 包含更高层次的服务或封装，提供更易用的接口来调用 API。这些服务可能会处理一些通用的功能，如身份验证、错误处理等。(创建和使用OpenAI客户端的基本服务。)
    - 可以通过依赖观察到，**service**依赖于**client**，而**client**依赖于**api**,只需要引入**Service**依赖即可。
    - openai-java maven依赖
    - ```xml
        <dependency>
            <groupId>com.theokanning.openai-gpt3-java</groupId>
            <artifactId>service</artifactId>
            <version>0.15.0</version>
        </dependency>
      ```
## openai-java(api)
这里都是一些实体类，pojo类。
目录结构：
```text
openai(api)
    ├─audio             音频所需POJO                                                                                      
    ├─billing           计费                                                                                                 
    ├─completion        完成
    │  └─chat           聊天
    ├─edit              编辑
    ├─embedding         嵌入
    ├─engine            GPT引擎
    ├─file              文档
    ├─finetune          微调
    ├─image             图片
    ├─model             模型
    ├─moderation        适度
    └─utils             工具
```
## openai-java(client)
这里是chatGPT基本客户端





