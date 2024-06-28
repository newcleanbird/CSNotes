# cmd指令

## 一、cmd简介

cmd是command的缩写,命令行。

> 虽然随着计算机产业的发展，Windows 操作系统的应用越来越广泛，DOS 面临着被淘汰的命运，但是因为它运行安全，稳定,有的用户还在使用,所以一般Windows 的各种版本都与其兼容，用户可以在Windows系统下运行DOS，中文版Windows XP 中的命令提示符进一步提高了与DOS 下操作命令的兼容性,用户可以在命令提示符直接输入中文调用文件。在9x系统下输入command就可以打开命令行。而在NT系统上可以输入cmd来打开，在windows2003后被cmd替代，利用CMD命令查询系统的信息或者是判断网络的好坏。

## 二、启动cmd并修改属性

### 1.启动cmd方式(CMD命令):

1.用户启动,``win + r``输入 ``cmd``,``Enter``
2.管理员启动,``win + r``输入 ``cmd``,``Ctrl``+``Shift``+``Enter``

### 1.修改属性、字体、背景

打开cmd，右击窗口点击属性，可以为cmd命令窗口设置文字与背景样式

## 三、命令集锦

### (一)文件夹命令

#### 1.进入文件夹

``cd D:\typora\file``

#### 2.返回上一级

``cd..``

#### 3.跳转到根目录

``cd \``

#### 4.跳转指定路径(假设现在在D:\typora跳转到D:\网页下载)

``cd D:\网页下载``

#### 5.打开文件夹或文件

``start 文件名字``

#### 6.新建文件夹

``md d:\typora\file``
``mkdir newtest 进入根目录后使用``

#### 7.新建空文件

```
cd.>file.txt
cd.>file.docx
cd.>file.ppt

type nul> newtest.txt 
type nul>.txt
```

#### 8.新建非空文件

``echo 文件中的内容>new.txt``

#### 9.删除文件(如果是del 文件夹A是删除文件夹A内的所有带后缀的文件，若文件夹A中有文件夹B，文件夹B不会被修改)

``del file.txt``

#### 10.删除指定后缀的文件

```
del *.txt
del *.docx
```

#### 11.删除名为file的空文件夹

``rd file``

#### 12.删除名为file的文件夹

``rd /s D:\file``

#### 13.删除file文件夹下的所有文件

``rd file /s``

#### 14.生成目录树,在文件少一些的路径尝试。要不会运行好久，ctrl+c可以停掉

```
tree
tree /f
```

#### 15.遍历当前路径下所有文件

``dir``

#### 16.显示当前目录及子文件

``dir /s``

#### 17.显示文件以及文件大小、个数

``dir /d``

#### 18.显示文件

``dir /b``

==对dir的组合使用：==

##### (1)查找文件。

只需要输入路径即可，无需cd返回到某个路径再执行命令(eg：D:\JAVA\eclipse\file和D:\eclipse效果相同)

```{.line-numbers}
dir/s/b d:\file
```

##### (2)查找文件以及文件大小、个数

```{.line-numbers}
dir/s/d d:\file
```

##### (3)查看隐藏文件夹

```{.line-numbers}
dir /?
```

##### (4)复制文件

```{.line-numbers}
copy 路径\文件名 路径\文件名
```

##### (5)移动文件

```{.line-numbers}
move 路径\文件名 路径\文件名
```

### (二)网络相关

#### 1.查看ip地址

```{.line-numbers}
ipconfig
```

#### 2.查询ip地址

```{.line-numbers}
ping www.csdn.net
```

#### 3.netstat 查看网络连接状态

```{.line-numbers}
netstat -help 获取命令行使用帮助信息
netstat -ano  //查看网络连接、状态以及对应的进程id
```

### (三)其他常用命令

#### 1.关机

```.{line-numbers}
shutdown -s
```

#### 2.关闭本地计算机，没有超时或警告

```{.line-numbers}
shutdown -p
```

#### 3.强制关闭正在运行的应用程序而不提前警告用户,可搭配 ``-p``

```{.line-numbers}
shutdown -f
```

#### 4.定时关机，定时60s,时间自定

```{.line-numbers}
shutdown -s -t 60
```

#### 5.关机并重启

```{.line-numbers}
shutdown -r
```

#### 6.一段时间后重启

``shutdown -r -t 秒数``

#### 7.注销当前用户

``shutdown -l　``

#### 8.休眠，可以搭配-f,shut down -h -f。不可以搭配-t

``shutdown -h ``

#### 9.解除命令

``shutdown -a``

#### 10.清除屏幕

``cls``

#### 11.使用help命令查看帮助

```{.line-numbers}
命令 -help    //第1种形式的使用帮助
命令  /?       //第2种形式的使用帮助
```

#### 12.终止命令

``ctrl+c``

#### 13.退出cmd

exit

#### 14.其他比较实用的，但使用频率不高的命令

```{.line-numbers}
notepad+路径	打开记事本
dxdiag	检查DirectX信息
winver	检查Windows版本
wmimgmt.msc		打开windows管理体系结构（WMI）
wupdmgr			windows	更新程序
wscript			windows脚本设置
write		写字板
winmsd		系统信息
wiaacmgr	扫描仪和相机
calc		计算器
mplayer2	打开windows media player
mspaint		画图板
mstsc		远程桌面连接
mmc			打开控制台
dxdiag		检查Directx信息
drwtsn32	系统医生
devmgmt.msc	设备管理器
notepad		记事本
ntbackup	系统备份和还原
sndrec32	录音机
Sndovl32	音量控制程序
tsshutdn	60秒倒计时关机
taskmgr		任务管理器
explorer	资源管理器
progman		程序管理器
regedit.exe	注册表
perfmon.msc	计算机性能监测
eventvwr	事件查看器
net user  	查看用户
whoami		查看当前用户
net user %username% 123456 		将电脑用户密码修改为123456，%%中填写用户名称
```

### (四)cmd快捷键

快速查看历史记录 ``↑`` ``↓``
查看完整记录 ``F7``
切换当前路径下文件 ``Tab``
反向选择文件和文件夹 ``Shift``+``Tab``
拖拽文件到窗口可以直接显示路径
``ESC``清除当前命令行
``F1``单字符输出上次输入的命令，如果已经是最后的一条的命令，则不进行任何切换操作。 （例：输入“dir”，按F1一次后自动输入d，按两次自动输入i,三次自动输入r）
``F2`` 可复制字符数量 , 输入上次命令中含有的字符,系统自动删除此字符后的内容. （例：输入 cd test ，按下F2 输入 e 后,系统自动输入 cd t 命令）
``F3`` 重新输入前一次输入的命令 或者按向上键
``F4`` 可删除字符数量,同于F2的功能 （例： 输入 cd test 将光标移动到d下面，按下F4 输入e后,系统自动删除t以后(包括d) e(不包括e)以前的字符 命令变为 cest）
``F5`` 自动切换到已经执行过的命令字符。可按下多次选择命令
``F6`` 相当按键盘上的Ctrl＋z 键
``F7`` 显示命令历史记录，按下后可用方向键上下选择之前输入过的命令
``F8`` 搜索命令的历史记录，循环显示所有曾经输入的命令，直到按下回车键为止
``F9`` 与 ``F7``配合使用。``F7``中选择的命令是有编号的，按下 ``F9``再输入命令的编号，就能快速执行命令
``Ctrl``+``Break`` 查看统计信息并按回车继续操作
``Ctrl``+``C`` 强行中止命令执行
``Ctrl``+``H`` 删除光标左边的一个字符
``Ctrl``+``M`` 表示回车确认键
``Alt``+``F7`` 清除所有曾经输入的命令历史记录
``Alt``+``PrintScreen`` 截取当前命令窗内容
``Tab`` 自动输入当前文件夹的子文件夹名。可按下多次选择文件夹，与cd命令配合使用可快速进入子文件夹

### (五)编译器

#### 1.Java/Javac

##### (1)查看JDK版本

``java -version``

##### (2)使用cmd运行JAVA程序

这里以提前写好的java程序为例，文件名"java"

```{.line-numbers}
public class java {
	public static void main(String[] args) {
		System.out.println("Zhang Shier 's CSDN");	}
}
```

###### i.首先使用cd进入指定路径

> 这里提供两种方法，第一中，运行结果输出在命令提示符窗口，第二种将运行结果输出到指定文件中

###### ii.第一种：输入 ``java java.java``

###### iii.第二种：输入 ``java java.java<in.txt>out.txt``

> 表示输入in.txt文件中的数据，将输出结果保存在out.txt中。(提前创建输入文本，输出文本不需要新建)

## 四、电脑快捷键

``win+E`` 打开文件管器

``win+D`` 显示桌面

``win+L`` 锁计算机

``alt+F4`` 关闭当前程序\文件

``ctrl+shift+Esc`` 打开任务管理器（或者ctrl+alt+delete）

``ctrl+F`` 在一个文本或者网页里面查找，相当实用（退出一般按ESC）

``ctrl+A`` 选中所有文本,或所有文件

``crtl+alt+tab`` 选中窗口但不打开，使用回车打开。按tab或←→切换

``alt+tab`` 选中窗口并打开

``win+tab`` 任务视图

``ctrl+tab`` 切换窗口(仅同一软件内多个窗口有效，如浏览器开了许多个网页)

## cmd快捷方式配置

### 1.cmd参数意义：

1. cmd /c dir 是执行完dir命令后关闭命令窗口。
2. cmd /k dir 是执行完dir命令后不关闭命令窗口。
3. cmd /c start dir 会打开一个新窗口后执行dir指令，原窗口会关闭。
4. cmd /k start dir 会打开一个新窗口后执行dir指令，原窗口不会关闭。

& 为cmd命令分割符号，也有用&&分隔的。至此，问题解决。


## 五、常用命令

1.查询g++ #include路径

g++ -v -E -x c++ -
