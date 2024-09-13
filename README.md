# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 11140ssm玩转保定旅游系统

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Kp48e9EtU?p=30)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

玩转保定旅游系统工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。玩转保定旅游系统的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示用户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、酒店门票信息实体图如图4-3所示：

![](/md/blog.014.png)

图4-3酒店门票信息实体图

2、飞机火车信息实体图如图4-4所示：

![](/md/blog.015.png)

`   `图4-4 飞机火车信息实体图

3、订单信息实体图如图4-5所示：

![](/md/blog.016.png)

`   `图4-5订单信息实体图

#########

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1 allusers表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|username|varchar|50|` `default NULL|
|pwd|varchar|50|` `default NULL|
|cx|varchar|50|` `default NULL|


表4-2 feijihuoche表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|addtime|varchar|50|default NULL|
|leixing|varchar|50|default NULL|
|chufadi|varchar|50|default NULL|
|zhongdiandi|varchar|50|default NULL|
|chufashijian|varchar|50|default NULL|
|daodashijian|varchar|50|default NULL|
|jiage|varchar|50|default NULL|
|zhaopian|varchar|50|default NULL|

表4-3：jingdianmeishi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|meishimingcheng|varchar|50|default NULL|
|meishishuliang|varchar|50|default NULL|
|meishixiangqing|varchar|50|default NULL|
|meishitupian|varchar|50|default NULL|
|jifenduihuan|varchar|50|default NULL|


表4-4：jingquxianlu表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|jingqumingcheng|varchar|50|default NULL|
|jingqudidian|varchar|50|default NULL|
|jingquxianlu|varchar|50|default NULL|
|jingquxiangqing|varchar|50|default NULL|
|zhaopian|varchar|50|default NULL|

表4-5：jiudianmenpiao表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|jiudianmingcheng|varchar|50|default NULL|
|jiudiandidian|varchar|50|default NULL|
|menpiaoshuliang|varchar|50|default NULL|
|zhaopian|varchar|50|default NULL|
|menpiaoleixing|varchar|50|default NULL|

# 5统详细设计
## 5.1前台首页功能模块
玩转保定旅游系统，在系统首页可以查看首页、景区线路、飞机火车、酒店门票、景点美食、论坛信息、我的、跳转到后台、购物车、客服等内容，如图5-1所示。

![](/md/blog.017.png)

图5-1前台首页功能界面图



`    `用户注册，在注册页面可以填写账号、密码、姓名、邮箱、手机等信息进行注册，如图5-2所示。

![](/md/blog.018.png)

图5-2 用户注册界面图

用户登录，在登录页面通过填写账号、密码、类型等信息完成登录，如图5-3所示。在

景区线路页面通过查看景区名称、景区地点、景区线路、景区详情等信息进行提交操作，如图5-4所示。

![](/md/blog.019.png)

图5-3用户登录界面图

![](/md/blog.020.png)

图5-4景区线路界面图

## 5.2管理员功能模块
管理员登录，通过填写用户名、密码进行登录，如图5-5所示。

![](/md/blog.021.png)

图5-5管理员登录界面图

管理员登录进入玩转保定旅游系统可以查看个人中心、用户管理、景区线路管理、飞机火车管理、酒店门票管理、门票类型管理、景点美食管理、旅游论坛、系统管理、订单管理等信息。

用户管理，在用户管理页面中可以通过查看账号、姓名、性别、邮箱、手机、照片、余额等内容进行修改、删除，如图5-6所示。还可以根据需要对景区线路管理进行详情，修改等详细操作，如图5-7所示。

![](/md/blog.022.png)

图5-6用户管理界面图

![](/md/blog.023.png)

图5-7景区线路管理界面图

飞机火车管理，在飞机火车管理页面中可以查看类型、出发地、终点地、出发时间、到达时间、价格、照片等信息，并可根据需要对已有飞机火车管理进行修改或删除等操作，如图5-8所示。

![](/md/blog.024.png)

图5-8 飞机火车管理界面图

酒店门票管理，在酒店门票管理页面中可以查看酒店名称、酒店地点、门票数量、照片、门票类型、价格等信息，并可根据需要对已有酒店门票管理进行修改或删除等详细操作，如图5-9所示。

![](/md/blog.025.png)

图5-9酒店门票管理界面图

景点美食管理，在景点美食管理页面中可以查看美食名称、美食数量、美食详情、美食图片、价格等内容，并且根据需要对已有景点美食管理进行详情，修改或删除等详细操作，如图5-10所示。

![](/md/blog.026.png)

图5-10景点美食管理界面图

旅游论坛，在旅游论坛页面中可以查看帖子标题、帖子内容、父节点id、用户id、用户名、状态等内容，并且根据需要对已有旅游论坛进行详情，修改或删除等详细操作，如图5-11所示。

![](/md/blog.027.png)

图5-11旅游论坛界面图

订单管理，在订单管理页面中可以查看订单编号、商品表名、用户id、商品id、商品名称、商品图片、购买数量、价格/积分、折扣价格、总价格/总积分、折扣总价格、支付类型、状态、地址等内容，并且根据需要对已有订单管理进行详情，修改或删除等详细操作，如图5-12所示。

![](/md/blog.028.png)

图5-12订单管理界面图


## 5.3用户功能模块
用户登录进入玩转保定旅游系统可以查看个人中心、旅游论坛、我的收藏管理、订单管理等内容。

订单管理，在订单管理页面中通过查看订单编号、商品表名、用户id、商品id、商品名称、商品图片、购买数量、价格/积分、折扣价格、总价格/总积分、折扣总价格、支付类型、状态、地址等信息，还可以根据需要对订单管理进行查看、删除，如图5-13所示。

![](/md/blog.029.png)

图5-13订单管理界面图













