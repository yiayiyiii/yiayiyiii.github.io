
# 写在前面

最好在[这里](https://yiayiyiii.github.io/post/ruby-ru-men/)阅读
 
Ruby，一种简单快捷的**面向对象脚本**语言，在20世纪90年代由日本人松本行弘开发。他一直想发明一种语言，使你既能进行高效开发又能享受编程的快乐，于是Ruby应运而生。他也可以开发前端，Github、Twitter等网站早期都是用Ruby on rails开发的。

写$Ruby$的感觉就俩字：**快乐** 。
主要的快乐源泉来自于这几个特性：

### 1.完全面向对象
万物皆对象，变量没有类型，任何东西都有值。

### 2.超级灵活
非常灵活,糖衣很多。

### 3.超级简洁、优雅
c++一个小时的代码Ruby30分钟搞定，适合于快速开发，一般开发效率是JAVA的5倍。很优雅，不需要注释一般就可以读懂。

# 环境配置

点[这里](http://www.ruby-lang.org/zh_cn/downloads/)来下载，这里以windows系统来举例：
![](https://cdn.luogu.com.cn/upload/image_hosting/294miwmp.png)

不管是什么系统**都最好不要选底下的“从源代码编译”**，我也不会搞！
![](https://cdn.luogu.com.cn/upload/image_hosting/abjylk14.png)

点“download”。

![](https://cdn.luogu.com.cn/upload/image_hosting/jgkycsgz.png)

选择有“Devkit”的，最好用最新版的前一个版本。如您的计算机是32位的，选择“(×86)”的，反之选择“(×64)”的。

之后傻瓜式安装即可。

简单吧（至少比Go好）

# 开始编程

首先，打开你的集成终端，输入“irb”，回车,看到
	
   ```
irb(main):001:0>
```
就成功了。

这是一个Ruby交互平台，例如输入`1+1`

直接输出`2`

它之后十分有用，只要不嫌麻烦，您可直接在上面写代码了。
（ 按 Ctrl + D 可退出 irb 模式）

（之后操作会使用VScode来演示）

## 第一段代码

第一段代码当然是输出“Helloworld”啦！

在VScode建立一个Ruby文件（后缀名为.rb）

写上

`puts("Helloworld!")`

就ok了。

ps:插入代码时不能选择Ruby语言差评(•́へ•́╬)

## 怎么运行呢？

右键你的文件夹区，选择“在集成终端打开”，如图：

![](https://cdn.luogu.com.cn/upload/image_hosting/46si48yd.png)

打开后会看到多出一个这样的东西：

![](https://cdn.luogu.com.cn/upload/image_hosting/z0kwrdb8.png)

这时输入“ruby 文件名”（中间有空格！），就能运行啦QwQ

## 开始学习



### 定义变量


直接写变量名再赋值就行了，如
```
a=2333333
```
以"$"开头的变量为全局变量，以大写字母开头的为常量。


### 输出

相信聪明的你已经观察到了，`puts`就是输出的意思。（括号可加可不加 ，最好加上，不加之后可能出现问题）

与此同时，还有另一种输出方式`print`。他与`puts`格式相同，但是`puts`输出后自带回车，`print`没有。如实在想输出回车可以这样写：
```
print("我是yiayiayi\n")
```
"\n"就是回车的意思。

此外，如果输出的时候想插入一个东西怎么办？见下面代码：

```
a=354370
puts("我的洛谷Uid是：#{a}")
```

用`#{ }`的方式，在大括号中写出你想添加的。

### 输入

用`gets()`语句，输入的是一个字符串，如
```
a=gets()
```
这句话既定义了a，又输入了a，超级方便。

但是`gets()`语句在洛谷上做题时会有奇奇怪怪的错误，产生[灵异事件](https://www.luogu.com.cn/discuss/show/331945)，学到正确的输入方法前还是自己本地玩玩吧。


### 运算符

* 运算操作符
  + +：加法
  + -：减法
  + *：乘法
  + **：指数运算
  + /：除法
  + %：取余
* 比较操作符
  + ==：等于
  + !=：不等于
  + ＞：大于
  + ＞=：大于等于
  + ＜：小于
  + ＜=：小于等于
* 逻辑操作符
  + &&：逻辑与
  + ||：逻辑或
  + ！：逻辑非
* 位运算操作符(不常用)
  + &：与AND
  + |：或OR
  + ^：亦或
  + ＜＜：左移位
  + ＞＞：右移位
  
  
 **警告:** 由于Ruby完全面向对象特性，写如下的一段代码：
 
 ```
a=1
a+1
puts(a)
```

输出的值只会是1，而下面两段代码则会输出2：

代码一：

```
a=1
puts(a+1)
```


代码二

```
a=1
a=a+1
puts(a)
```

 ## 条件语句
 
 板子在这里：
 ```cpp
if (...) then
...
end
```
和
```cpp
if(...）then
...
else
...
end

```
还有
```cpp
if(...）then
...
elseif
...
else
...
end

```
用用就熟练了。

## 字符串

$Ruby$中的字符串也可以做适量的运算：

```
a="Hello"
b="world!"
```

此时
```
puts（a+" "+b）
```
会输出"Hello world!"（每种语言都有）

还有
```
a<<b
```
$a$的值此时成了"Helloworld!"（注意是值！），与`a=a+b`相等，此时输出$a$,会输出"Helloworld!"。

还有可以
```
a[0]="a"
```
这样数组中第一个元素就被替换成了"a"


还有诸如`puts(a*2333)`(输出2333次$a$)之类的骚操作，这里不细讲了。


字符串转整数是会` to_i `方法,例如：

```
a=gets(a)
a=a.to_i
```
当没有可转的时候会直接返回0。


字符串转浮点数是会` to_f `方法，和转整数差不多。




## 函数

有带参数的和不带参数的。

**不带参数的：**

像这样：
```cpp
def sayhello#定义函数
    puts"Helloworld"
end

sayhello#直接用
```

ps:用"#"做单行备注

**带参数的：**
```
def sayhello(name)#括号里写参数
    puts"Helloworld #{name}."#拼装成字符串,大括号引用
end

sayhello("Tom ")
```

**带默认参数的：**
```
def sayhello(name="Ruby")#默认参数，给了就覆盖，不给就用默认参数
    puts"Helloworld #{name}."#拼装成字符串,大括号引用
end

sayhello("Tom ")
```


## Class入门
Class是个挺~~好玩~~有用的结构，参考如下：
```
class Game
    attr_accessor :price, :title
    def initialize(title = "洛谷", price = 200)
        @title = title
        @price = price
    end
    def show()
        puts "标题: #{@title}"
        puts "价格: #{@price}"
    end
end
```

定义了一个叫Game的class，可理解为一个函数的组合包。（但其实里面打包的叫方法）看到`@title`和`@price`了没，你是不是一脸问号？

以`@`开头的变量为实例变量，定义实例变量后，整个类都可以使用此变量。

`attr_accessor :price, :title`这一句是让此class有两个可用的变量。

在`initialize`中定义实例变量是一个不错的注意，因为执行class时，`initialize`这个方法会自动执行。

之后想用？这样用：

```
mygame = Game.new()
mygame.show()
```

`Game.new()`为Game这个class的`.new`方法，由于完全面向对象，什么东西都有 “方法” ，类似于c++中的函数。如想查看一个对象的全部方法（拿1来举例），可以在Ruby交互平台中输入`对象.methods`,之后你就能看到一个对象的所有方法啦（如下图）

![](https://cdn.luogu.com.cn/upload/image_hosting/yl15xbna.png)

方法很多，截的图也没截全，有兴趣您可以自己探索。

回到正题，`Game.new`方法是创建一个名为$mygame$的class，有全部$Game$的方法，例如之后的`mygame.show()`（什么方法都是`对象 + . +  方法名  ` 欧）。

Class的知识有很多，毕竟我讲的是“Ruby入门”，所以就简单讲一下用法。

## 数组

定义：直接
```
a=["I","love","Luogu"]
```
输出不用循环，直接`puts(a)`

要真想循环也没有问题，
```
g.each do |a|#提取数组的每个元素到a中
    puts"我爱#{a}"
end
```

接下来是数组的连接：
```
puts a.join(",")#连接数组，用,隔开
```
就是把数组中的每个元素都用","隔开。

判断是否是一个数组：

这里可以检查有没有数组特有的$.each$方法：

```
if a.respond_to?("each")
```
有问号的方法返回的都是布尔值。

## 循环

常用的有两种：for循环和while循环

**for循环：**

1到4：
```
for num in 1...5 do
    puts num
end
```

循环1到5：
```
for num in 1..5 do
    puts num
end
```
你没看错、我没打错，就是少了个点！

**while循环：**
```
index = 0
while index < 5 do
    puts "while.index=" + index.to_s
    index+=1
end
```
都不难
QWQ

还有数组循环：
```
a = ["I", "love", "Luogu"]
for b in a do
    puts b
end
```
# 最后

这篇博客只是粗略地讲了讲如何写最最最最入门的Ruby，您可能感受到了便捷、快乐，甚至已经写出了最简单的程序了。但是，如果您想进阶学习的话，还是买本书学吧。

您也可以探索Ruby的有（qi）趣（guai）特性（如自己写个a-b problem然后输入0.4和0.3）

随着更深入的了解，Ruby可能就是您的快乐星球！

如有错误欢迎大佬指出！
