# gradle
## 1、Gradle是什么？
   * 它不是用来开发项目的，而是用来对项目进行构建的。也就是说，Gradle是软件项目构建工具。可以非常简单地对项目进行编译、测试、打包、发布等。
   * Gradle是一个自动化的项目构建工具，它只是提供了一个构建项目的框架，真正起作用的是Plugin
*  Plugin向工程添加属性和任务(Task)，这些Task顺序执行为开发者构建项目
Gradle通常使用Groovy或Java语言编写构建脚本<br>

1、是个自动化构建工具<br>
2、有核心的概念 plugin task property project<br>
3、使用Groovy编写构建脚本<br>
4、方便打包js文件<br>
5、支持微服务<br>
6、把软件工程搬到构建中<br>
7、把制定个人的需求搬到构建中<br>
8、gradle包装器

## 2.建立自己的gradle项目
  标志性的文件就是build.gradle<br>
  提供了默认的文件目录结构<br>
    src/main/java <br>
    src/test/java <br>
    
    
   * 创建一个Java工程，包括一个src/main/java文件夹和一个build.gradle文件。Java源文件放在src/main/java中。build.gradle只有一条语句:apply plugin:’java’，说明要使用Java插件。<br>
打开命令窗口，命令提示符切换到该工程下，执行命令gradle build<br>
你就会看到Gradle为你做的构建了

 ### 在build.gradle配置文件中加入以下代码
    
  ```groovy
  plugins{
    id 'java'  //说明要使用Java插件
  }
  version="1.0" //定义版本
  sourceCompatibility=1.8  //设置Java版本编译兼容1.8
   jar{
       manifest{    //将Main-Class头添加到JAR文件清单中
         attributes 'Main-Class':  'com.lsf.PrintStr'
      }
   }

  ```
  
 *  通过java –jar build/libs/项目名-1.0.jar运行应用程序
 
 两只种构建Gradle项目的方法：一种是手动，另一种是使用gradle init 这个命令。





   

