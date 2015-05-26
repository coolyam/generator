### maven plugins

            <!-- for install plugins-->
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-plugin-plugin</artifactId>
                <version>3.4</version>
            </plugin>

            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>cobertura-maven-plugin</artifactId>
                <version>2.7</version>
            </plugin>

            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-enforcer-plugin</artifactId>
                <version>1.4</version>
            </plugin>

            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>findbugs-maven-plugin</artifactId>
                <version>2.5.5</version>
            </plugin>

            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>jdepend-maven-plugin</artifactId>
                <version>2.0</version>
            </plugin>

            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>findbugs-maven-plugin</artifactId>
                <version>3.0.1</version>
            </plugin>

### mybatis-parent

    <dependency>
    	<groupId>org.mybatis</groupId>
    	<artifactId>mybatis-parent</artifactId>
    	<version>24</version>
    </dependency>

所有的 mybatis 组件都会要继承 mybatis-parent, 当前版本（1.3.3-SNAPSHOT）使用的是
24-SNAPSHOT ,现在可以直接使用 24

### maven-source-plugin
      
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-source-plugin</artifactId>
        <configuration>
          <skip>true</skip>
        </configuration>
      </plugin>
      
改为
  
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-source-plugin</artifactId>
        <configuration>
          <skipSource>true</skipSource>
        </configuration>
      </plugin>  
      
### build& install
      mvn clean install -Dmaven.test.skip=true
      
### misc
首次 build & install ，包括 test 在内的时间相当长（约50min），这里把log放在了 build_log_0.txt 中，备份
    