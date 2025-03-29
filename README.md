
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
 
