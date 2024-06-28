# vscode java 安装及环境配置

## 安装VSCode

Visual Studio Code 是一个轻量级但功能强大的源代码编辑器，可在桌面上运行，适用于 Windows、macOS 和 Linux。它内置了对 JavaScript、TypeScript 和 Node.js 的支持，并具有针对其他语言和运行时（如 C++、C#、Java、Python、PHP、Go、.NET）的丰富扩展生态系统。通过这些介绍性视频开始 VS Code 之旅。
[VSCode官网](https://code.visualstudio.com/)
[VSCode下载链接](https://code.visualstudio.com/Download)

## 安装Java SDK

[Java SDK 官网下载地址](https://www.oracle.com/cn/)

Oracle Java 是广受欢迎的编程语言和开发平台。它有助于企业降低成本、缩短开发周期、推动创新以及改善应用服务。如今，Java 仍是企业和开发人员的首选开发平台，全球有数百万开发人员运行超过 60 亿台 Java 虚拟机。

Java SE 是全球广受欢迎的现代开发平台，也是企业应用的理想编程语言。Java SE 有助于企业降低成本、缩短开发时间、推动创新以及改善应用服务。Oracle Java SE Universal Subscription 现包含 Oracle GraalVM 和 Java Management Service，可有效保护您的 Java 投资。

### 配置环境变量

找到系统变量，点击新建：

```s
变量名：JAVA_HOME
变量值：C:\Program Files\Java\jdk1.8.0_221 [你JDK安装的路径]
```

```s
变量名：CLASSPATH
变量值：.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar
```

path新建两个变量如下：

```s
%JAVA_HOME%\bin
%JAVA_HOME%\jre\bin
```

验证Java SDK是否安装好：

```s
win+R
在运行框内输入cmd
java -version
```

或者通过输入命令javac：

```s
javac
```

## 安装插件Java Extension Pack

Java 扩展包：Extension Pack for Java 是一组常用扩展，可帮助在 Visual Studio Code 中编写、测试和调试 Java 应用程序。查看 VS Code 中的 Java 以开始使用。

[Java Extension Pack 链接](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)

直接在VSCode里面安装“Extension Pack for Java ”扩展：

六个插件，是VSCode直接帮我们整理的六个最常用Java插件，如下：

Language Support for Java™ by Red Hat
Debugger for Java
Java Test Runner
Maven for Java
Project Manager for Java
Visual Studio IntelliCode

## 配置

创建一个java项目来测试一下。

- 按快捷Ctrl+Shift+p ，然后在搜索框中输入create，并找到创建java项目。

- 选择No build tools，回车。

- 会弹出一个文件夹选择框，这个是你java项目存放的地方。

- 输入你的项目名称的提示框，回车。
  - 如：JavaProjectTest

- Java测试项目新建好了
  - 新建HelloWorld.java文件

    ```java
    public class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello World!");
        }
    }
    ```

- 鼠标右键菜单选择“Run Java” or 按快捷键Ctrl + Alt + N运行，查看输出结果
