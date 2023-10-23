# 后端SpringBoot配置流程

### 前期配置

由于我们使用的是maven项目。因此在创建spring boot项目之前要配置好maven

参考：[【精选】Maven超细致史上最全Maven下载安装配置教学（2023更新...全版本）建议收藏...赠送IDEA配置Maven教程_神兽汤姆猫的博客-CSDN博客](https://blog.csdn.net/MSDCP/article/details/127680844)

### 初始化SpringBoot框架

1. 打开[SringBoot官方链接](https://spring.io/)
2. 在上方导航栏找到**Projects——Spring Initializer**

![image-20231022171206563](C:\Users\Jaker\AppData\Roaming\Typora\typora-user-images\image-20231022171206563.png)

3. 打开Spring Initializer，得到以下界面![image-20231022171640455](C:\Users\Jaker\AppData\Roaming\Typora\typora-user-images\image-20231022171640455.png)

   左边为设置板块，右边是给spring boot添加的依赖

4. 相关设置

   ```mark
   Project —— Maven
   Language —— Java
   SpringBoot —— 3.1.5
   Project Metadata:
   	Group  —— 	TeachPlatform
   	Artifact ——  Run
   Packaging —— jar
   Java —— 21
   ```

   ![image-20231023141210124](C:\Users\Jaker\AppData\Roaming\Typora\typora-user-images\image-20231023141210124.png)

5. 导入依赖

   ```markdown
   Spring Web 
   MySQL Driver 
   Spring Data JDBC 
   MyBatis Framework 
   ```

   ![image-20231022175233805](C:\Users\Jaker\AppData\Roaming\Typora\typora-user-images\image-20231022175233805.png)

6. 点击generate 生成压缩包

7. 然后将其解压到本地，修改文件夹名称为**Competition**

8. 打开IDEA，选择项目——打开——Competition项目文件夹

![image-20231022175719848](C:\Users\Jaker\AppData\Roaming\Typora\typora-user-images\image-20231022175719848.png)

此为编辑代码文件夹

---

打开项目中的pom.xml文件查看是否相关依赖已配置

有时候会出现如下情况：

![image-20231023141605369](C:\Users\Jaker\AppData\Roaming\Typora\typora-user-images\image-20231023141605369.png)

**解决方案**

使用 `dependencyManagement` ，将所有的 `snakeyaml` 统一改成没有隐患的版本

```xml
    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>org.yaml</groupId>
                <artifactId>snakeyaml</artifactId>
                <version>2.0</version>
            </dependency>
        </dependencies>
    </dependencyManagement>

```

点击maven的重新配置即可
