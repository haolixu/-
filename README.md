# Java工程师笔试✊✌

### String类能不能被继承,为什么?
>  不可以，因为String类有final修饰符，而final修饰的类是不能被继承的，实现细节不允许改变。
### java支持的数据类型有哪些？什么是自动拆装箱？
>* 3种引用类型:`数组`,`类`,`接口`
>* 8种数据类型:`int`,`float`,`double`,`long`,`short`,`char`,`byte`,`boolean`
>* 是指基本数据类型和引用数据类型之间的自动转换
### Java中什么是重载,什么是构造函数,有何异同?
>* Java中的构造函数是为了初始化对象的，构造函数的函数名和类名一致，默认的构造函数没有参数，没有返回值，构造函数的函数体内，没有内容。 
>* 构造函数的重载是函数名与类名相同，参数类型不同，参数不同。同样的作用也是为了初始化对象的。重载的最直接作用是方便了程序员可以根据不同的参数个数，顺序，类型，自动匹配方法，减少写过个函数名或方法名的重复步骤。
### arraylist和linklist的区别
>*  1.ArrayList是实现了基于动态数组的数据结构，LinkedList基于链表的数据结构。 （LinkedList是双向链表，有next也有previous）
>* 2.对于随机访问get和set，ArrayList觉得优于LinkedList，因为LinkedList要移动指针。
>* 3.对于新增和删除操作，LinedList比较占优势，因为ArrayList要移动数据。 适合用来实现堆栈与队列,前者先进后出，后者是先进先出.
### &和&&有什么区别?
>* &&当第一个条件不成之后，后面的条件都不执行了，而&则还是继续执行，直到整个条件语句执行完为止。
### 在公司局域网上ping www.lixu666.cn没有涉及的网络协议是?
>* 1、因为ping的话 后面跟的是地址，所以要先将域名转换为ip地址，即用到了DNS
>* 2、获取到ip地址后，在数据链路层是根据MAC地址传输的，所以要用到ARP解析服务，获取到MAC地址
>* 3、ping功能是测试另一台主机是否可达，程序发送一份ICMP回显请求给目标主机，并等待返回ICMP回显应答，（ICMP主要是用于ip主机、路由器之间传递控制信息，控制信息是指网络通不通，主机是否可达）
>* 4、TCP的话，不涉及数据传输，不会用到
### 函数的参数值通常存储在进程的哪个区?
>* 1:`栈区`-由编译器自动释放分配,存放函数的参数值,局部变量的值.
>* 2:`堆区`-又称动态内存分配,一般由程序员释放分配.如果某动态内存不再使用需要将其释放掉,否则我们认为发生了内存泄漏现象.
>* 3:`代码区`-存放函数体的二进制代码.
>* 4:`文字常量区`-存放常量字符串.
>* 5:`静态存储区`-内存在程序编译的时候就已经分配好,主要用于存放静态数据,全局数据和常量.   
### 假设只有100m的内存,需要对1Gb的数据进行排序,最合适大的算法是?
> 首先内存只有100Mb，而数据却有1Gb，所以肯定没法一次性放到内存去排序，只能用外部排序，而外排序通常是使用多路归并排序，即将原文件分解成多个能够一次性装入内存的部分（如这里的100Mb），分别把每一部分调入内存完成排序（根据情况选取适合的内排算法），然后对已经排序的子文件进行多路归并排序（胜者树或败者树）。
### 如果某系统16*5=106成立,则系统采用的是多少进制?
> 设使用的是p进制，则$$15*4=112等价于：(p + 5) * 4 = p^2 + p + 2$$
>* 解出来p=-3（舍去）和p=6
### 接口和抽象类的异同?
> 接口和抽象类都是继承树的上层，他们的`共同点`如下：
>* 1)都是上层的抽象层。
>* 2)都不能被实例化.
>* 3)都能包含抽象的方法，这些抽象的方法用于描述类具备的功能，但是不比提供具体的实现.


> 他们的`区别`如下：
>* 1)在抽象类中可以写非抽象的方法，从而避免在子类中重复书写他们，这样可以提高代码的复用性，这是抽象类的优势；接口中只能有抽象的方法。
>* 2)一个类只能继承一个直接父类，这个父类可以是具体的类也可是抽象类；但是一个类可以实现多个接口。使用接口可以方便统一管理和方便调用.
### 事务的原子性是指?
>* 原子性指的是事务中包含的程序作为数据库的逻辑工作单位，它所做的对数据修改操作要么全部执行，要么完全不执行。
### 以下关于链表实现的堆中哪个表述是正确的?
> push操作如果更新节点插入在链表头中,则pop操作必须从链表尾移除节点
### 一种既有利于短小作业又兼顾到长作业的调度算法是?
>* `最高响应比优先算法`等待时间相同时，要求服务时间愈短，优先权愈高，因而该算法有利于短作业，对于长作业，作业的优先级可以随等待时间的增加而提高，当其等待时间足够长时，其优先级便可升到很高，从而获得处理机，因此该算法即有利于短作业又兼顾到了长作业。
### 以下关于cache控制的HTTP Header中那个意义为不允许代理服务器缓存内容?
>* `Cache-Control: private`:响应只能作为私有缓存,不能在用户之间共享
>* `Cache-Control:no-cache`:提醒浏览器要从服务器提取文档进行验证
>* `Cache-Control:no-store`:绝对禁止缓存（用于机密，敏感文件）
>* `Cache-Control: max-age=60`:60秒之后缓存过期（相对时间）
### 下面关于E-R图和E-R模型,哪个说法是错误的?
> E-R模型的构成成分是`实体集`、`属性`和`联系集`
>* 1） 实体集用矩形框表示，矩形框内写上实体名。
>* 2） 实体的属性用椭圆框表示，框内写上属性名，并用无向边与其实体集相连。
>* 3） 实体间的联系用菱形框表示，联系以适当的含义命名，名字写在菱形框中，用无向连线将参加联系的实体矩形框分别与菱形框相连，并在连线上标明联系的类型，即1—1、1—N或M—N。

### 下面关于进程和线程,说法正确的事?
> 多进程下，每个进程都有自己的独立地址空间，进程间的数据空间也相互独立，彼此通信以专门的通信方式进行。而多线程下，同一进程内的线程共享进程的地址空间，一个线程的数据可以直接提供给其他线程使用。有时候在对临界资源使用时，当临界资源被一个线程占有，如果它终止时不释放占有的临界资源，而这个临界资源仍然认为它还被这个退出的线程使用，因而永远得不到释放。如果另外一个线程也在等待这个临界资源，它就可能无限等待下去，从而形成死锁.

>* 进程的特征:`动态`,`独立`,`异步`,`并发`
### 当一台主机从一个网络移到另一个网络时,以下说法正确的是?
>* `mac地址`在你的网卡上本就是不会改变的；
>* ip地址要变化，否则无法与其他主机进行通信。
### 在一个单链表中,若删除P后续结果所指的后续结果,则执行
> 单链表中若要删除直接后继节点，自然就是要将P的后继节点指向P后继节点的节点
### 在子类的定义中有一个和父类同名的成员函数,这一现象称为函数的
>* 当子父类中出现成员函数一模一样的情况，会运行子类的函数。这种现象，称为`覆盖`操作。
>* `什么时候使用覆盖操作?`-保留父类功能的同时对父类功能进行更新、扩展。
>* 被覆盖的方法在子类中只能通过super调用。
>* 方法覆盖要求参数列表必须一致，而`方法重载`要求参数列表必须不一致。
>* 父类的一个方法只能被子类覆盖一次，而一个方法可以在所有的类中可以被重载多次。
### 一条sql语句中,group by处于什么位置?
> 在where子句之后
### 以下关于TCP/IP协议中,不正确的是?
>* `TCP`负责将信息拆分为数据包,并在数据包到达目的地后对其进行装配
>* `IP`负责为数据包选择路由以便将其传递到正确的目的地
>* IP,`IGMP`都是网络层的协议,TCP是传输层的协议
### 以下描述不正确的是?
>* 存取速度：寄存器 > Cache > 内存 > 硬盘 > 光盘 > 软盘
>* 随机访问的速度要比顺序访问慢很多,原因是因为磁头频繁的寻道，定位，磁头的移动消耗掉很多时间。

> 使用中断的好处:
>* 提高计算机系统效率。
>* 维持系统可靠正常工作。
>* 满足实时处理要求。
>* 提供故障现场处理手段。


>* 同一进程下的线程可以共享`data section`和`file fd`,`stack`和`register set`不能共享

### 堆栈溢出一般是由什么原因导致的？ 
>* 1.函数调用层次太深。
>* 2.动态申请空间使用之后没有释放。
>* 3.数组访问越界。
>* 4.指针非法访问。
### 如何减少换页错误？
>* 访问局部性（locality of reference）满足进程要求
>* 使用基于最短剩余时间（shortest remaining time）的调度机制
### 进程进入等待状态有哪几种方式?
>* cpu调度给更高级的线程是进入`就绪态`
>* 阻塞的线程获得资源或信号是进入`就绪态`
>* 时间片轮转的情况下,时间片到了是`就绪态`
>* 自旋锁（spinlock）是一种保护临界区最常见的技术。没有获得自旋锁的进程在获取锁之前处于忙等（`阻塞状态`）。
### 在UML类图中有以下几种常见的关系:
>* `泛化`:是对象之间耦合度最大的一种关系，子类继承父类的所有细节。在类图中使用带三角箭头的实线表示，箭头从子类指向父类。
>* `实现`:在类图中就是接口和实现的关系。使用带三角箭头的虚线表示，箭头从实现类指向接口。
>* `依赖`:对象之间最弱的一种关联方式，是临时性的关联。在类图使用带箭头的虚线表示，箭头从使用类指向被依赖的类。
>* `关联`:对象之间一种引用关系，比如客户类与订单类之间的关系。在类图使用带箭头的实线表示，箭头从使用类指向被关联的类。可以是单向和双向。
>* `聚合`:较强于一般关联,有整体与局部的关系,并且没有了整体,局部也可单独存在。在类图使用空心的菱形表示，菱形从局部指向整体。
>* `组合`:是一种强烈的包含关系。如公司和部门的关系，没有了公司，部门也不能存在了.在类图使用实心的菱形表示，菱形从局部指向整体。
>* `多重性`:通常在关联、聚合、组合中使用。就是代表有多少个关联对象存在。使用数字..星号（数字）表示。
### 函数x的定义如下,问x(x(8))需要调用多少次函数x(int n)?
```  
int x(int n) {
	if(n<=3)
	return 1;
	else
	return x(n-2)+x(n-4)+1;
}
```
> 我的理解是
```
x(8)=x(6)+x(4)+1
    =x(4)+x(2)+1+x(4)+1
    =x(2)+x(0)+1+x(2)+1+x(2)+x(0)+1+1
    =9
所以x(x(8))=18
```

### 已知g=14,则PHP表达式h=g+=10,运算后的结果是
>  h=g=24 
### 设计模式中属于结构模式的是?
>* 外观模式
>* 适配器模式
>* 代理模式
>* 桥模式
>* 组合模式

> 除了结构模式,还有创建型模式
>* 工厂模式
>* 原型模式
>* 单例模式
### 指令寄存器的作用是
> 指令寄存器是临时放置从内存里面取得的程序指令的寄存器，用于存放当前从主存储器读出的正在执行的一条指令。
### 表city1有两个字段name,num_person,请将city1中num_person字段根据人数进行重新编码
> `要求`:0≤x<500,000编码为1

> 500,000≤x<1,000,000编码为2

> 1,000,000≤x编码为3
```
select name,
case 
    when num_person>=0 and num_person<500000 then 1
    when num_person>=500000 and num_person<1000000 then 2
    when num_person>=1000000 then 3 end as mark  
from city1
```
### 内存有哪几种存储组织结构?
>* 1:可执行代码
>* 2:静态数据
>* 3:动态数据（堆）
>* 4:栈
### 内存越界和内存泄漏？
> 内存越界又叫内存溢出，指程序在申请内存时，没有足够的内存空间供其使用。
内存泄漏是指程序在申请内存后，无法释放已申请的内存空间，占用有用内存。
### 如何在linux多个进程间 进行通讯？给出三种？
> 管道，共享内存，信号量（又叫信号灯），套接口 （socket）。
### 运输层的两个主要协议是？ 
> CP和UDP。用户数据报协议UDP在传送数据之前不需要建立连接,UDP不提供可靠交付,UDP首部只有8个字节。
传输控制协议TCP在传送数据之前必须先建立连接,数据传送结束要释放链接,TCP提供可靠的，提供面向连接的服务,TCP首部的最小长度是20个字节。
### 结构化程序设计的三种基本逻辑结构？
> 顺序结构、选择结构和循环结构。采用结构化程序设计方法，程序结构清晰，易于阅读、测试、排错和修改。由于每个
模块执行单一功能，模块间联系较少，使程序编制比过去更简单，程序更可靠，而且增加了可维护性，每个模块可以独立编制、测试。
### 什么是死锁？如何避免死锁？
> 死锁是指多个进程在运行过程中因争夺资源而造成的一种僵局，当过程处于这种僵持状态时，若无外力作用，他们
将无法向前推进。在资源动态分配过程中，防止系统进入不安全状态，以避免发生死锁。
### 轮询任务调度和可抢占式调度有什么区别？
>* 轮询任务调度无需记录当前所有连接的状态，所以它是一种无状态调度，但不利于后面的请求及时得到响应。
>* 抢占式调度允许高优先级的任务打断当前执行的任务，抢占CPU的控制权。这有利于后面的高优先级的任务也能及时得到响
应。但实现相对较复杂且可能出现低优先级的任务长期得不到调度。
### 简单描述面向对象的三个特征？
>* 封装：将客观事物抽象成类，每个类对自身的数据和方法实行protection(private,protected,public) 。
>* 继承：它可以使用现有类的所有功能，并在无需重新编写原来的类的情况下对这些功能进行扩展。
>* 多态：是将父对象设置成为和一个或更多的他的子对象相等的技术，赋值之后，父对象就可以根据当前赋值给它的子对象的特性以不同的方式运作。
### 交换和路由的区别是什么？VLAN有什么特点？
>* 交换是不需要 IP 地址的，而路由需要。
>* VLAN 是虚拟局域网的英文缩写，它的特点有三：控制广播，安全，灵活性和可扩张性。
### C语言中的static的作用是什么？
> static在c里面可以用来修饰变量，也可以用来修饰函数。
### C++中引用与指针有什么区别？
> 引用是变量的别名，引用不占用内存空间，而指针占用内存空间。
### C语言编程：实现把一个字符倒序的功能，如abcd倒成dcba。
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main(void)
{
    char    str[120];
    int     i, j;
    char    tmp;
    while (scanf("%s", str) == 1) {    // 连续输入字符串给str变量,遇到EOF结束
        i = strlen(str);
        i--;   // 求结束符'\0'前一个位置
        for (j = 0; j < i; j++, i--) {     //字符串反转
            tmp = str[i];
            str[i] = str[j];
            str[j] = tmp;
        }
        printf("%s\n", str);
    }
 return 0;}
 ```
 ### 请用C语言编写算法求ax2+bx+c=0方程的根。a,b,c由键盘输入，设b2-4ac>0(采用if语句）。
 ```c
 #include <stdio.h>
#include <math.h>
 int main()
{
        float a,b,c,d,x1,x2;
        printf("输入方程的三个系数:");
        scanf("%f %f %f",&a,&b,&c);
        if(a!=0)
        {
                d=sqrt(b*b-4*a*c);
                x1=(-b+d)/(2*a);
                x2=(-b-d)/(2*a);
                if(x1<x2) 
                    printf("%0.2f %0.2f\n",x2,x1); 
                else
                    printf("%0.2f %0.2f\n",x1,x2);
        }
        return 0;}
		
以下程序的运行结果为？
#include<stdio.h>
int main();
{
        int sum,pad;
		sum=pad=5;
		pad=sum++;
		pad++;
		++pad;
		printf("%d\n", pad);
}
```
### js的数据类型？
> 字符串、数字、布尔、数组、对象、Null、Undefined.
### js的事件流模型都有什么？
> 单击事件:onclick，改变事件:onchange，选中事件:onselect，获得焦点事件:onfocus，失去焦点事件:on
blur，载入文件事件:onload，鼠标镇盖事件:onmouseover等。
### 什么是ajax和json？
>* Ajax用来描述一组技术，它使浏览器可以为用户提供更为自然的浏览体验，它是“Asynchronous JavaScript + XML的简写”。
>* JSON来自于javascript，是一种比较流行的标准格式，是数据的载体，更加易读、更便于肉眼检查。
### 想实现一个对页面某个支点的拖曳？如何做？
> 给需要拖拽的节点绑定mousedown, mousemove, mouseup事件。mousedown事件触发后，开始拖拽。mousemove时，需要通过event.clientX和clientY获取
拖拽位置，并实时更新位置。mouseup时，拖拽结束。需要注意浏览器边界的情况。
### 页面布局常用的HTML5语义元素有哪些？
>* header 
>* footer 
>* section
>* article
>* aside
### call 和apply的区别是什么?
>* call：它可以接受多个参数，第一个参数与apply一样，后面则是一串参数列表。
>* apply：最多只能有两个参数――新this对象和一个数组argArray。
### 请说明一下static，relative，absolute和fixed元素的特点？
>* static(静态) 不能通过z-index进行层次分级。 
>* relative(相对定位) 参考自身静态位置通过top,bottom,left,right 定位，并且可以通过z-index进行层次分级。
>* fixed（固定定位）所固定的参照对像是可视窗口而并非是body或是父级元素，其总是固定在浏览器窗口的某个位置，并且不受滚动的影响，是绝对的坐标定位。
### 请解释一下inline和inline-block的区别？
>* inline元素设置width,height属性无效。
>* inline-block展现inline元素的属性，但是可以设置自己的宽和高了。
### 日志文件用于保存？ 
> 日志文件是 对数据库的更新操作.
### String,StringBuffer,StringBuilder的区别?
>* 操作少量的数据使用 String；
>* 单线程操作大量数据使用 StringBuilder；
>* 多线程操作大量数据使用 StringBuffer。
### 在浏览器地址栏键入URL,按下回车之后会经历以下流程:
>* 浏览器向DNS服务器谞求解析该URL中的域名所对应的IP地址；
>* 解析出IP地址后，根据该IP地址和默口 80,和服务器建立TCP连接；
>* 浏览器发出读取文件(URL中域名后面部分对应的文件)的HTP请求,该请求报文作为TCP三次握手的第三个报文的数据发送给服务器
>* 服务器对浏览器请求作出响应,并把对应的htm文本发送给浏览器
>* 释放TCP 连接
>* 浏览器将该html文本并显示内容
### IP地址中的ABCD类网:
>* A类地址范围：1. 0. 0.1—126.155. 255. 254
>* B类地址范围：128. 0. 0.1—191. 255. 255. 254
>* C类地址范围：192. 0. 0.1—223. 255. 255. 254
>* D类地址范围：224. 0. 0.1—239. 255. 255. 254
>* E类地址范围：240. 0. 0.1—255. 255. 255. 254
### OSI七层机构:


| 具体七层 | 数据格式  |  功能和连接方式  | 典型设备 |
| --------   | -----:  | :----:  | :----:  |
| 应用层    | data |   网络服务和使用者应用程序间的一个接口    |  终端设备(pc和手机) |
| 表示层    | data |   数据表示,数据安全,数据压缩    |  终端设备(pc和手机) |
| 会话层    | data |   数据传输,会话连接管理与流量控制,差错控制    |  终端设备(pc和手机) |
| 传输层    | 数据组织成数据段 |   用一个寻址机制来标识一个特定的应用程序(端口号    |  终端设备(pc和手机) |
| 网络层    | 分割和重新组织成数据包pocket |   基于网络层地址(IP地址)进行不同网络系统的地址选择    |  网关,路由器 |
| 数据链路层   | 将比特信息封装成比特帧 |   通过系统提供的物理地址来寻址    |  网桥和交换机 |
| 物理层    | 比特流(bit) |   建立或者取消物理连接   |  光纤,同轴电缆,中继器,集线器 |


