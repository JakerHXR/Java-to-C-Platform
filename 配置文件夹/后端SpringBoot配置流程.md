# 后端SpringBoot配置流程

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

   ![image-20231022174609724](C:\Users\Jaker\AppData\Roaming\Typora\typora-user-images\image-20231022174609724.png)

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

##### 



