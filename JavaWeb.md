# 	JavaWeb

## JDBC（Java DataBase Connectivity）

JDBC是使用Java语言操作关系型数据库的一套API

![image-20230123103647261](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230123103647261.png)

### 快速入门

1.注册驱动

![image-20230123121132374](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230123121132374.png)

### JDBC的API

#### DriverManager

驱动管理类

* 注册驱动
* 获取数据库连接

![image-20230124095916485](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124095916485.png)

![image-20230124095952147](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124095952147.png)

#### Connection

![image-20230124100118233](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124100118233.png)

![image-20230124100139049](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124100139049.png)

#### Statement

![image-20230124100316824](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124100316824.png)

#### ResultSet

![image-20230124100442554](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124100442554.png)

![image-20230124104022010](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124104022010.png)

#### PreparedStatement

PreparedStatement继承自Statement，可以预防SQL注入问题

SQL注入：SQL注入是通过操作输入来修改事先定义好的SQL语句，用以达到执行代码对服务器进行攻击的方法

![image-20230124111309593](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124111309593.png)

***

![image-20230124112552985](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124112552985.png)

![image-20230124112950199](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124112950199.png)

***

**原理**

![image-20230124113228469](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124113228469.png)

#### 数据库连接池

![image-20230124115217080](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124115217080.png)

![image-20230124115502119](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124115502119.png)

Druid使用步骤

1. 导入jar包
2. 定义配置文件
3. 加载配置文件
4. 获取数据连接池
5. 获取连接

![image-20230124121047859](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124121047859.png)

## Maven

Maven是专门用于管理和构建Java项目的工具，主要功能有

* 提供了一套标准化的项目结构
* 提供了一套标准化的构建流程（编译，测试，打包，发布）
* 提供了一套依赖管理机制

解决了不同IDE之间，项目结构不一样，不通用的问题

![image-20230124163103056](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124163103056.png)

### 简介

![image-20230124163858706](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124163858706.png)

![image-20230124164523686](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124164523686.png)

### Maven常用命令

* compile：编译
* clean：清理
* test：测试
* package：打包
* install：安装

**Maven生命周期**

![image-20230124200721612](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124200721612.png)

![image-20230124200804269](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124200804269.png)

### IDEA配置Maven

1. 选择IDEA中File--->Settings
2. 搜索maven
3. 设置IDEA使用本地安装的Maven，并修改文件路径

#### Maven坐标

![image-20230124202626379](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124202626379.png)

#### IDEA创建Maven项目

* 创建模块，点击Maven

![image-20230124203620010](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124203620010.png)

#### IDEA导入Maven项目

![image-20230124203843581](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124203843581.png)

### 依赖管理

![image-20230124205611077](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124205611077.png)

快捷导入jar包：Alt+insert，选择Dependency，搜索对应坐标双击选中

#### 依赖范围

![image-20230124211027390](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230124211027390.png)

## Mybatis

优秀的持久层框架，用于简化JDBC开发

**持久层**

* 负责将数据保存到数据库的那一层代码
* JavaEE三层框架：表现层、业务层、持久层

**框架**

* 框架就是半成品软件，是一套可重用的、通用的、软件基础代码模型
* 在框架的基础之上构建软件编写更加高效、规范、通用、可扩展

### 快速入门

![image-20230126120654421](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230126120654421.png)

![image-20230126121125745](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230126121125745.png)



### Mapper代理开发

解决原生方式硬编码，简化后期执行SQL

创建同名的Mapper接口，并在resource下创建相同路径的文件夹（用 / 代替 . ，并将Mapper.xml文件放在文件夹中，编译后就会放在同一文件

![image-20230126124507536](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230126124507536.png)

![image-20230126124350420](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230126124350420.png)

<u>mybatis的mapper resource可以改成包名package name</u>

### Mybatis核心配置文件

- configuration（配置）
  - properties（属性）
  - settings（设置）
  - typeAliases（类型别名）
  - typeHandlers（类型处理器）
  - objectFactory（对象工厂）
  - plugins（插件）
  - environments（环境配置）
    - environment（环境变量）
      - transactionManager（事务管理器）
      - dataSource（数据源）
  - databaseIdProvider
  - mappers（映射器）

environment可以配置数据库连接环境信息，可以配置多个environment，通过default切换进行开发和测试等不同环境

typeAliases可以设置别名，可以设置包扫描，包下的所有实体类可以直接写名

配置各个标签需要遵循前后顺序

### MyBatisX插件

红色代表映射文件

蓝色代表mapper接口

### 配置文件完成增删改查

#### 查询所有数据

![image-20230127145719276](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127145719276.png)

* 数据库表中的字段名用下划线分开，实体类用驼峰命名法，二者名称不一样，不能实现自动封装
  * 可以通过起别名让别名和实体类属性名一样
  * 也可以使用sql片段

![image-20230127152028402](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127152028402.png)

但是不够灵活，可以使用resultMap作映射解决

1. 定义< resultMap >标签
2. 在< select > 标签中，使用resultMap属性替代resultType属性

![image-20230127161511364](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127161511364.png)

#### 查看详情

![image-20230127163039161](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127163039161.png)

* Test函数不能传递参数

参数占位符：

1. ${}：拼sql，会存在sql注入问题
2. #{}：会替换成？ ，防止sql注入

![image-20230127164648058](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127164648058.png)

特殊字符处理可以使用转义字符或CDTA区

| <    | &lt ;   |
| ---- | ------- |
| <=   | &lt ; = |
| >    | &gt ;   |
| >=   | &gt ; = |

#### 条件查询

![image-20230127173242565](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127173242565.png)

参数接收

1. 散装参数：如果方法中有多个参数，需要使用@Param("SQL参数占位符名称")
2. 对象参数：对象的属性名称要和参数占位符名称一致
3. Map集合，key对应参数占位符名称，value对应的值

#### 动态条件查询

![image-20230127201652647](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127201652647.png)

用if判断是否输入内容，用恒等式或< where >解决连接and问题

#### 单条件动态条件查询

从多个条件中选择一个< chose >	(when,otherwise)

![image-20230127203413846](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127203413846.png)

或者加otherwise 恒等式防止空搜索报错		

#### 添加和主键返回

![image-20230127205028852](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127205028852.png)

![image-20230127210153922](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127210153922.png)

insert后面加上useGeneratedKeys = "true" keyProperty = "id"添加后可以直接用getId()

#### 修改

修改全部字段

![image-20230127211045970](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127211045970.png)

修改动态字段

![image-20230127211444601](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230127211444601.png)

< set >解决逗号问题

#### 删除

![image-20230128111556976](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128111556976.png)

如果传入数组，mybatis默认会把数组封装为一个Map集合，key默认为array，value默认为数组，可以用@Param(别名)修改key的名字

### 参数传递

![image-20230128111957425](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128111957425.png)

多个参数会封装成Map集合，可以使用@Param注解，替换Map集合中的默认arg键名

![image-20230128112624891](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128112624891.png)

### 注解开发

![image-20230128112707224](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128112707224.png)

## HTML

### 入门

![image-20230128113028320](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128113028320.png)

![image-20230128114420446](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128114420446.png)

### 基本标签

![image-20230128115504124](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128115504124.png)

![image-20230128115858444](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128115858444.png)

### 图片、音频、视频标签

![image-20230128123119031](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128123119031.png)

尺寸单位：px（像素），%（原本图片的百分之多少）

### 超链接标签

![image-20230128123528560](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128123528560.png)

< a herf="网址" target="_blank"> xxxxx < /a >

### 列表标签

![image-20230128123912046](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128123912046.png)

有序标签： 1.xx 2.xx

无序标签：原点

### 表格标签

![image-20230128124147373](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128124147373.png)

如果多行单元格合成一个，则单元格属于第一行

### 布局标签

| 标签     | 描述                                                         |
| -------- | ------------------------------------------------------------ |
| < div >  | 定义HTML文档中的一个区域部分，经常与CSS一起使用，用来布局页面 |
| < span > | 用于组合行内元素                                             |

### 表单标签、表单项标签

![image-20230128133532186](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128133532186.png)

![image-20230128133823720](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128133823720.png)

## CSS

Cascading  Style Sheet:层叠样式表

### CSS导入方式

![image-20230128201255646](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128201255646.png)

![image-20230128204138706](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128204138706.png)

css文件：

```
p{
    color: red;
}
```

### CSS选择器

![image-20230128204251892](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128204251892.png)

## JavaScript

跨平台、面向对象的脚本语言，控制网页行为，使网页可交互

引入方式

1. 内部脚本：将JS代码定义在HTML页面中
2. 外部脚本：将JS代码定义在外部JS文件中，然后引入到HTML页面中

![image-20230128205602190](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128205602190.png)

![image-20230128205910446](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128205910446.png)

### 基础语法

#### 书写语法

![image-20230128221647182](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128221647182.png)

![image-20230128223349100](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230128223349100.png)

#### 变量

![image-20230129104527916](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129104527916.png)

var

* 作用域：全局变量
* 变量可以重复定义

let

* 作用域：局部变量
* 不能重复定义

const：只读常量

#### 数据类型

![image-20230129105152987](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129105152987.png)

#### 运算符

==：先判断类型是否一致，如果不一样，会先进行类型转换，再去比较值

===：判断类型是否一致，不一样直接返回false，再去比较值

#### 类型转换

其他类型转number：

1. string：按照字符串的字面值，转为数字，如果字面值不是数字，则转换为NAN，一般使用parseInt()
2. boolean：true为1，false为0

其他类型转boolean：

1. number：0和NAN转为false，其他数字转为true
2. string：空字符串转为false，其他转为true
3. null：false
4. undefined：false

#### 函数

![image-20230129111224803](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129111224803.png)

![image-20230129112628782](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129112628782.png)

传入参数多的不会被接受，如果少了对应的值变成NAN，与数字相加还是NAN

### 对象

#### Array

![image-20230129114221431](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129114221431.png)

splice可以删除元素，第一个参数从哪开始删除，第二个参数删除几个元素

#### String

![image-20230129115836600](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129115836600.png)

trim()去除字符串前后空白字符

#### 自定义对象

![image-20230129120128471](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129120128471.png)

### BOM

Browser Object Model 浏览器对象模型

组成

* Window：浏览器窗口对象
* Navigator：浏览器对象
* Screen：屏幕对象
* History：历史记录对象
* Location：地址栏对象

#### Window

![image-20230129145304126](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129145304126.png)

#### History

![image-20230129150034084](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129150034084.png)

#### Location

![image-20230129150101002](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129150101002.png)

location.herf = "https://www.xxxxx"

### DOM

![image-20230129151112217](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129151112217.png)

JavaScript通过DOM，能够对HTML进行操作

* 改变HTML元素的内容
* 改变HTML元素的样式（CSS）
* 对HTML DOM事件作出反应
* 添加和删除HTML元素

![image-20230129152203892](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129152203892.png)

#### Element对象

![image-20230129153119285](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129153119285.png)

#### Element对象的使用

得到的Element对象.innerHTML=“”可以改变文本内容

### 事件监听

事件：HTML事件是发生在HTML元素上的“事情”

* 按钮被点击
* 鼠标移动到元素之上
* 按下键盘按键

事件监听：JavaScript可以在事件被侦测到执行代码

#### 事件绑定

![image-20230129160556559](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129160556559.png)

#### 常见事件

onload()某个页面或图像被加载完成

onblur()失去焦点

onfocus()获得焦点

onchange()内容被改变

onclick()被点击

onkeydown()某个键盘按键被按下

onkeypress()某个键盘按键被按下并松开

onmouseout()鼠标从某元素离开

onmouseover()鼠标移到某元素之上

onsubmit()确认按钮被点击如果onsubmit()返回true，则表单被提交，吐过返回false，则表单不提交

### 表单验证

![image-20230129182155695](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129182155695.png)

### 正则表达式

![image-20230129182255326](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129182255326.png)

## Web核心

Web：全球广域网，也称为万维网（www），能够通过浏览器访问的网站

JavaWeb：使用Java技术来解决相关web互联网领域的技术栈

![image-20230129185423873](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129185423873.png)

## HTTP

![image-20230129185703516](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129185703516.png)

### HTTP请求数据格式

![image-20230129193900229](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129193900229.png)

### HTTP相应数据格式

![image-20230129201218073](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129201218073.png)

![image-20230129201529460](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230129201529460.png)

## Tomcat

Tomcat是一个轻量级Web服务器，也被称为Web容器，Servlet容器。Servlet需要依赖Tomcat才能运行

Web服务器可以封装HTTP协议操作，简化开发，可以将web项目部署到服务器中，对外提供网上浏览服务

启动：双击：bin\startup.bat

关闭：

1. 直接关掉窗口：强制关闭
2. bin\shutdown.bat：正常关闭
3. Ctrl+C：正常关闭

卸载：直接删除目录即可

bin：二进制可执行文件

conf：配置文件

lib：依赖jar包

logs：日志文件

temp：临时目录

webapps：Tomcat的web项目，写的web项目放到此目录下就完成了项目的部署

work：Tomcat运行过程中，项目中产生的临时的文件数据	

### 配置和部署项目

![image-20230130102814282](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230130102814282.png)

直接将项目放置到webapps目录下，即部署弯沉

一般JavaWeb项目会被打成war包，然后将war包放到webapps目录下，Tomcat会自动解压缩war文件

### Maven Web项目结构

![image-20230130105722598](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230130105722598.png)

pom.xml中package要改成war包

### IDEA中创建MavenWeb项目

![image-20230130105903924](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230130105903924.png)

![image-20230130112827104](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230130112827104.png)

创建项目facets创建web resource ， + type web.xml

### IDEA集成本地Tomcat

![image-20230130113811539](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230130113811539.png)

### Tomcat的Maven插件

![image-20230130133236088](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230130133236088.png)

## Servlet

Java提供的**动态**web资源开发技术（不同用户访问都不一样）

![image-20230131111218592](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131111218592.png)

provided只在编译和测试环境存在，运行的时候没有，打成war包的时候没有，因为tomcat自带了Servlet

### 执行流程

![image-20230131124137485](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131124137485.png)

### 生命周期

![image-20230131125301302](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131125301302.png)

### 方法介绍

![image-20230131125700365](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131125700365.png)

### 体系结构

![image-20230131133856720](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131133856720.png)

HttpServlet先获取请求方式，再根据不同的请求方式，调用不同的doXxxx方法

1. 继承HttpServlet
2. 重写doGet和doPost方法

### urlPattern配置

一个Servlet可以配置多个urlPattern

@WebServlet(urlPatterns = {"/demo1","/demo2"})

![image-20230131143505479](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131143505479.png)

### XML配置Servlet

![image-20230131144451115](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131144451115.png)

## Request&Respone

![image-20230131145051021](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131145051021.png)

### Request

#### 继承体系

![image-20230131150507002](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131150507002.png)

#### Request获取请求数据

![image-20230131151215405](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131151215405.png)

##### 通用方式获取请求参数

![image-20230131152843332](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131152843332.png)

![image-20230131152858402](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131152858402.png)

##### 请求参数中文乱码处理

![image-20230131180003681](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131180003681.png)

注意引用StandardCharsets的包是import java.nio.charset.StandardCharsets

#### Request请求转发

![image-20230131180829651](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131180829651.png)

### Response

#### Response设置响应数据功能

![image-20230131181608991](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131181608991.png)

#### Response完成重定向

![image-20230131183851564](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131183851564.png)

resp.sendRedirect()是前面两个语句的简化版

**路径问题**

![image-20230131184614598](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131184614598.png)

可以动态获取虚拟路径：request.getContextPath()

#### Response响应字符数据

![image-20230131185249012](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131185249012.png)

![image-20230131185156638](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131185156638.png)

#### Response响应字节数据

![image-20230131185318251](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131185318251.png)

![image-20230131201007129](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230131201007129.png)

## JSP

一种动态网页技术，既可以定义HTML、JS、CSS等静态内容，还可以定义Java代码的动态内容

![image-20230201113721255](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201113721255.png)

### JSP原理

![image-20230201114259517](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201114259517.png)

### JSP脚本

![image-20230201115249589](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201115249589.png)

### JSP缺点

![image-20230201121439026](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201121439026.png)

### EL表达式

![image-20230201122017973](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201122017973.png)

### JSTL标签

![image-20230201150622883](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201150622883.png)

![image-20230201151348113](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201151348113.png)

![image-20230201151426144](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201151426144.png)

c:forEach中可以用varStatus=”名字“，status.count代替编号

## MVC模式和三层架构

![image-20230201152657034](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201152657034.png)

![image-20230201153244526](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201153244526.png)

![image-20230201153405677](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201153405677.png)

## 会话跟踪技术

![image-20230201162050350](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230201162050350.png)

### Cookie

#### 基本使用

![image-20230203141221812](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230203141221812.png)

#### 原理

![image-20230203142757857](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230203142757857.png)

#### 使用细节

 ![image-20230203143550447](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230203143550447.png)

转码：URLEncoder.encode(value,"UTF-8")

解码：URLDecoder.decode(value,"UTF-8")

### Session

#### 基本使用

![image-20230203145005891](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230203145005891.png)

#### 原理

![image-20230203151948878](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230203151948878.png)

cookie携带session的id保证访问的都是同一个session

#### 使用细节

![image-20230203153242677](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230203153242677.png)

### 小结

![image-20230203154140957](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230203154140957.png)

![image-20230203200115938](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230203200115938.png)

## Filter

![image-20230204100812523](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204100812523.png)

![image-20230204101141683](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204101141683.png)

Filter是javax.servlet包下的servlet

#### 执行流程

![image-20230204102826815](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204102826815.png)

### 使用细节

![image-20230204103049931](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204103049931.png)

![image-20230204104537899](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204104537899.png)

​	

### 登录验证

![image-20230204110721786](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204110721786.png)

![image-20230204112811454](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204112811454.png)

## Listener

![image-20230204115219793](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204115219793.png)

### ServletContextListener

![image-20230204115421494](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204115421494.png)

## AJAX

![image-20230204121307565](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204121307565.png)

![image-20230204121227322](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204121227322.png)

### 基本使用

![image-20230204143248797](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204143248797.png)

### Axios

对原生的AJAX进行封装，简化书写

#### 基本使用

![image-20230204161307574](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204161307574.png)

#### 请求方式别名

![image-20230204163516388](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204163516388.png)

### JSON

JavaScript Object Notation，JavaScript对象表示法

语法简单，层次结构鲜明，多用于作为数据载体，在网络中进行数据传输

key值要带引号

#### 基础语法

![image-20230204170219312](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204170219312.png)

#### JSON数据和Java对象转换

请求数据：JSON字符串转为Java对象

相应数据：Java对象转为JSON字符串

![image-20230204171152659](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204171152659.png)

servlet读取axious的数据

```java
BufferedReader reader = request.getReader();
String line = reader.readLine();
Brand brand = JSON.parseObject(line, Brand.class);
service.addBrand(brand);
response.getWriter().write("success");
```

## Vue

### 基本使用

![image-20230204195147657](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204195147657.png)

el后的值跟div的id一致，v-model的值跟return的key一致

### 常用指令

![image-20230204202347195](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204202347195.png)

![image-20230204202408592](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204202408592.png)

![image-20230204202430157](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204202430157.png)

![image-20230204202454557](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204202454557.png)

![image-20230204202526595](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204202526595.png)

### 生命周期

![image-20230204202702253](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230204202702253.png)

## Element

![image-20230205122538923](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230205122538923.png)

### 布局

![image-20230205123159470](https://souln.oss-cn-guangzhou.aliyuncs.com/java/image-20230205123159470.png)

​	
