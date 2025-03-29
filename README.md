mq部署方案
1、rocketmq 顺序消费记录
一个master ，一个 brocker ，多个group ，多个topic，采用集群消费模式。
注意 一个group 对应一个 topic。 生产者 和 消费者 可以有多个，但是 主题和分组 都是一对一的。这样保证了 消息在集群模式下 的 顺序存储 和消费。

 spring-cloud-stream3.1.1 整合 rocketmq5.1.4
 
 <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.7.7</version>
 </parent>

 <dependency>
    <groupId>org.springframework.cloud</groupId>
        <artifactId>spring-cloud-dependencies</artifactId>
        <version>2021.0.5</version>
             <type>pom</type>
                <scope>import</scope>
 </dependency>

 <dependency>
    <groupId>com.alibaba.cloud</groupId>
        <artifactId>spring-cloud-alibaba-dependencies</artifactId>
        <version>2021.0.5.0</version>
             <type>pom</type>
                <scope>import</scope>
 </dependency>
 <plugin>
 <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-maven-plugin</artifactId>
        <version>2.7.7</version>
             <executions>
                    <execution>
                     <goals>
                            <!--可以把依赖的包都打包到生成的Jar包中-->
                            <goal>repackage</goal>
                        </goals>
                        </execution>
                </executions>
   
 </plugin>
 
