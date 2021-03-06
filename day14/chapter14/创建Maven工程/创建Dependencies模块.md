# 创建 Dependencies 模块

---

## POM

```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <parent>
        <groupId>com.lusifer</groupId>
        <artifactId>myshop</artifactId>
        <version>1.0.0-SNAPSHOT</version>
        <relativePath>../pom.xml</relativePath>
    </parent>

    <artifactId>myshop-dependencies</artifactId>
    <packaging>pom</packaging>

    <properties>
        <!-- 统一的依赖管理 -->
        <apache-httpclient.version>4.5.4</apache-httpclient.version>
        <cglib.version>3.2.5</cglib.version>
        <commons-beanutils.version>1.9.3</commons-beanutils.version>
        <commons-codec.version>1.10</commons-codec.version>
        <commons-fileupload.version>1.3.2</commons-fileupload.version>
        <commons-httpclient.version>3.1</commons-httpclient.version>
        <commons-email.version>1.2</commons-email.version>
        <commons-io.version>2.5</commons-io.version>
        <commons-lang.version>2.6</commons-lang.version>
        <commons-lang3.version>3.5</commons-lang3.version>
        <commons-pool.version>1.6</commons-pool.version>
        <fasterxml-classmate.version>1.3.3</fasterxml-classmate.version>
        <fasterxml-jackson.version>2.8.5</fasterxml-jackson.version>
        <google-gson.version>2.8.2</google-gson.version>
        <google-guava.version>23.0</google-guava.version>
        <javax-activation.version>1.1.1</javax-activation.version>
        <javax-mail.version>1.4.7</javax-mail.version>
        <javax-servlet-api.version>3.1.0</javax-servlet-api.version>
        <javax-servlet-jsp.version>2.2</javax-servlet-jsp.version>
        <javax-servlet-jstl.version>1.2</javax-servlet-jstl.version>
        <javax-validation-api.version>1.1.0.Final</javax-validation-api.version>
        <log4j.version>1.2.17</log4j.version>
        <mysql-connector-java.version>5.1.30</mysql-connector-java.version>
        <sitemesh.version>2.4.2</sitemesh.version>
        <slf4j.version>1.7.22</slf4j.version>
        <spring.version>4.3.13.RELEASE</spring.version>
        <taglibs.version>1.1.2</taglibs.version>
        <mybatis.version>3.4.5</mybatis.version>
        <mybatis-spring.version>1.3.1</mybatis-spring.version>
        <tk.mybatis.version>3.4.6</tk.mybatis.version>
        <junit.version>4.12</junit.version>
    </properties>

    <dependencyManagement>
        <dependencies>
            <!-- JUnit Begin -->
            <dependency>
                <groupId>junit</groupId>
                <artifactId>junit</artifactId>
                <version>${junit.version}</version>
            </dependency>
            <!-- JUnit End -->
        
            <!-- Apache Http Begin -->
            <dependency>
                <groupId>org.apache.httpcomponents</groupId>
                <artifactId>httpclient</artifactId>
                <version>${apache-httpclient.version}</version>
            </dependency>
            <dependency>
                <groupId>org.apache.httpcomponents</groupId>
                <artifactId>fluent-hc</artifactId>
                <version>${apache-httpclient.version}</version>
            </dependency>
            <dependency>
                <groupId>org.apache.httpcomponents</groupId>
                <artifactId>httpmime</artifactId>
                <version>${apache-httpclient.version}</version>
            </dependency>
            <!-- Apache Http End -->

            <!-- Apache Commons Begin -->
            <dependency>
                <groupId>commons-lang</groupId>
                <artifactId>commons-lang</artifactId>
                <version>${commons-lang.version}</version>
            </dependency>
            <dependency>
                <groupId>org.apache.commons</groupId>
                <artifactId>commons-lang3</artifactId>
                <version>${commons-lang3.version}</version>
            </dependency>
            <dependency>
                <groupId>commons-io</groupId>
                <artifactId>commons-io</artifactId>
                <version>${commons-io.version}</version>
            </dependency>
            <dependency>
                <groupId>commons-codec</groupId>
                <artifactId>commons-codec</artifactId>
                <version>${commons-codec.version}</version>
            </dependency>
            <dependency>
                <groupId>commons-fileupload</groupId>
                <artifactId>commons-fileupload</artifactId>
                <version>${commons-fileupload.version}</version>
            </dependency>
            <dependency>
                <groupId>commons-beanutils</groupId>
                <artifactId>commons-beanutils</artifactId>
                <version>${commons-beanutils.version}</version>
                <exclusions>
                    <exclusion>
                        <groupId>commons-logging</groupId>
                        <artifactId>commons-logging</artifactId>
                    </exclusion>
                </exclusions>
            </dependency>
            <dependency>
                <groupId>commons-pool</groupId>
                <artifactId>commons-pool</artifactId>
                <version>${commons-pool.version}</version>
            </dependency>
            <dependency>
                <groupId>commons-httpclient</groupId>
                <artifactId>commons-httpclient</artifactId>
                <version>${commons-httpclient.version}</version>
            </dependency>
            <!-- Apache Commons End -->

            <!-- Fasterxml Begin -->
            <dependency>
                <groupId>com.fasterxml</groupId>
                <artifactId>classmate</artifactId>
                <version>${fasterxml-classmate.version}</version>
            </dependency>
            <dependency>
                <groupId>com.fasterxml.jackson.core</groupId>
                <artifactId>jackson-core</artifactId>
                <version>${fasterxml-jackson.version}</version>
            </dependency>
            <dependency>
                <groupId>com.fasterxml.jackson.core</groupId>
                <artifactId>jackson-databind</artifactId>
                <version>${fasterxml-jackson.version}</version>
            </dependency>
            <dependency>
                <groupId>com.fasterxml.jackson.core</groupId>
                <artifactId>jackson-annotations</artifactId>
                <version>${fasterxml-jackson.version}</version>
            </dependency>
            <dependency>
                <groupId>com.fasterxml.jackson.module</groupId>
                <artifactId>jackson-module-jaxb-annotations</artifactId>
                <version>${fasterxml-jackson.version}</version>
            </dependency>
            <!-- Fasterxml End -->

            <!-- Google Begin -->
            <dependency>
                <groupId>com.google.guava</groupId>
                <artifactId>guava</artifactId>
                <version>${google-guava.version}</version>
            </dependency>
            <dependency>
                <groupId>com.google.code.gson</groupId>
                <artifactId>gson</artifactId>
                <version>${google-gson.version}</version>
            </dependency>
            <!-- Google End -->

            <!-- Javax Begin -->
            <dependency>
                <groupId>javax.servlet</groupId>
                <artifactId>jstl</artifactId>
                <version>${javax-servlet-jstl.version}</version>
                <type>jar</type>
            </dependency>
            <dependency>
                <groupId>javax.servlet</groupId>
                <artifactId>javax.servlet-api</artifactId>
                <version>${javax-servlet-api.version}</version>
            </dependency>
            <dependency>
                <groupId>javax.servlet.jsp</groupId>
                <artifactId>jsp-api</artifactId>
                <version>${javax-servlet-jsp.version}</version>
            </dependency>
            <dependency>
                <groupId>javax.mail</groupId>
                <artifactId>mail</artifactId>
                <version>${javax-mail.version}</version>
            </dependency>
            <dependency>
                <groupId>javax.activation</groupId>
                <artifactId>activation</artifactId>
                <version>${javax-activation.version}</version>
            </dependency>
            <dependency>
                <groupId>javax.validation</groupId>
                <artifactId>validation-api</artifactId>
                <version>${javax-validation-api.version}</version>
            </dependency>
            <dependency>
                <groupId>taglibs</groupId>
                <artifactId>standard</artifactId>
                <version>${taglibs.version}</version>
                <type>jar</type>
            </dependency>
            <!-- Javax End -->

            <!-- Logs Begin -->
            <dependency>
                <groupId>org.slf4j</groupId>
                <artifactId>slf4j-api</artifactId>
                <version>${slf4j.version}</version>
            </dependency>
            <dependency>
                <groupId>org.slf4j</groupId>
                <artifactId>slf4j-log4j12</artifactId>
                <version>${slf4j.version}</version>
            </dependency>
            <dependency>
                <groupId>org.slf4j</groupId>
                <artifactId>jcl-over-slf4j</artifactId>
                <version>${slf4j.version}</version>
            </dependency>
            <dependency>
                <groupId>org.slf4j</groupId>
                <artifactId>jul-to-slf4j</artifactId>
                <version>${slf4j.version}</version>
            </dependency>
            <dependency>
                <groupId>log4j</groupId>
                <artifactId>log4j</artifactId>
                <version>${log4j.version}</version>
            </dependency>
            <!-- Logs End -->

            <!-- Spring Framework Begin -->
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-context</artifactId>
                <version>${spring.version}</version>
            </dependency>
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-context-support</artifactId>
                <version>${spring.version}</version>
            </dependency>
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-jdbc</artifactId>
                <version>${spring.version}</version>
            </dependency>
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-orm</artifactId>
                <version>${spring.version}</version>
            </dependency>
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-tx</artifactId>
                <version>${spring.version}</version>
            </dependency>
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-test</artifactId>
                <version>${spring.version}</version>
            </dependency>
            <!-- Spring Framework End -->

            <!-- MySQL Begin -->
            <dependency>
                <groupId>mysql</groupId>
                <artifactId>mysql-connector-java</artifactId>
                <version>${mysql-connector-java.version}</version>
                <scope>runtime</scope>
            </dependency>
            <!-- MySQL End -->
            
            <!-- MyBatis Begin -->
            <dependency>
                <groupId>org.mybatis</groupId>
                <artifactId>mybatis</artifactId>
                <version>${mybatis.version}</version>
            </dependency>
            <dependency>
                <groupId>org.mybatis</groupId>
                <artifactId>mybatis-spring</artifactId>
                <version>${mybatis-spring.version}</version>
            </dependency>
            <dependency>
                <groupId>tk.mybatis</groupId>
                <artifactId>mapper</artifactId>
                <version>${tk.mybatis.version}</version>
            </dependency>
            <!-- MyBatis End -->

            <!-- Other Begin -->
            <dependency>
                <groupId>opensymphony</groupId>
                <artifactId>sitemesh</artifactId>
            </dependency>
            <dependency>
                <groupId>cglib</groupId>
                <artifactId>cglib</artifactId>
                <version>${cglib.version}</version>
            </dependency>
            <!-- Other End -->
        </dependencies>
    </dependencyManagement>

    <build>
        <plugins>
            <plugin>
                <artifactId>maven-help-plugin</artifactId>
                <version>2.2</version>
                <inherited>false</inherited>
                <executions>
                    <execution>
                        <id>generate-effective-dependencies-pom</id>
                        <phase>generate-resources</phase>
                        <goals>
                            <goal>effective-pom</goal>
                        </goals>
                        <configuration>
                            <output>${project.build.directory}/effective-pom/${project.artifactId}.xml</output>
                        </configuration>
                    </execution>
                </executions>
            </plugin>

            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>xml-maven-plugin</artifactId>
                <version>1.0</version>
                <inherited>false</inherited>
                <executions>
                    <execution>
                        <goals>
                            <goal>transform</goal>
                        </goals>
                    </execution>
                </executions>
                <configuration>
                    <transformationSets>
                        <transformationSet>
                            <dir>${project.build.directory}/effective-pom</dir>
                            <stylesheet>src/main/xslt/single-project.xsl</stylesheet>
                            <outputDir>${project.build.directory}/effective-pom</outputDir>
                        </transformationSet>
                    </transformationSets>
                </configuration>
            </plugin>

            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>build-helper-maven-plugin</artifactId>
                <version>1.10</version>
                <inherited>false</inherited>
                <executions>
                    <execution>
                        <id>attach-artifacts</id>
                        <phase>package</phase>
                        <goals>
                            <goal>attach-artifact</goal>
                        </goals>
                        <configuration>
                            <artifacts>
                                <artifact>
                                    <file>${project.build.directory}/effective-pom/${project.artifactId}.xml
                                    </file>
                                    <type>effective-pom</type>
                                </artifact>
                            </artifacts>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>
</project>
```

## 创建单体应用结构配置

在 `src/main/xslt` 目录下创建 `single-project.xsl` 文件

```
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" >
    <xsl:template match="/">
        <xsl:copy-of select="projects/*[1]" />
        <xsl:copy-of select="*[local-name()='project']" />
    </xsl:template>
</xsl:stylesheet>
```