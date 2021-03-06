# 深入理解java虚拟机
## 第一部分走近Java
### 第1章走近Java2
- 1.1概述2
- 1.2Java技术体系3
- 1.3Java发展史5
- 1.4Java虚拟机发展史9
    * 1.4.1SunClassicExactVM9
    * 1.4.2SunHotSpotVM11
    * 1.4.3SunMobile—EmbeddedVMMeta—CircularVM12
    * 1.4.4BEAJRockitIBMJ9VM13
    * 1.4.5AzulVMBEALiquidVM14
    * 1.4.6ApacheHarmonyGoogleAndroidDalvikVM14
    * 1.4.7MicrosoftJVM及其他15
- 1.5展望Java技术的未来16
    * 1.5.1模块化17
    * 1.5.2混合语言17
    * 1.5.3多核并行19
    * 1.5.4进一步丰富语法20
    * 1.5.564位虚拟机21
- 1.6实战：自己编译JDK22
    * 1.6.1获取JDK源码22
    * 1.6.2系统需求24
    * 1.6.3构建编译环境25
    * 1.6.4进行编译26
    * 1.6.5在IDE工具中进行源码调试31
- 1.7本章小结35

## 第二部分自动内存管理机制
### 第2章Java内存区域与内存溢出异常38
- 2.1概述38
- 2.2运行时数据区域38
    * 2.2.1程序计数器39
    * 2.2.2Java虚拟机栈39
    * 2.2.3本地方法栈40
    * 2.2.4Java堆41
    * 2.2.5方法区41
    * 2.2.6运行时常量池42
    * 2.2.7直接内存43
- 2.3HotSpot虚拟机对象探秘43
    * 2.3.1对象的创建44
    * 2.3.2对象的内存布局47
    * 2.3.3对象的访问定位48
- 2.4实战：OutOfMemoryError异常50
    * 2.4.1Java堆溢出51
    * 2.4.2虚拟机栈和本地方法栈溢出53
    * 2.4.3方法区和运行时常量池溢出56
    * 2.4.4本机直接内存溢出59
- 2.5本章小结60

### 第3章垃圾收集器与内存分配策略61
- 3.2对象已死吗62
    * 3.2.1引用计数算法62
    * 3.2.2可达性分析算法64
    * 3.2.3再谈引用65
    * 3.2.4生存还是死亡66
    * 3.2.5回收方法区68
- 3.3垃圾收集算法69
    * 3.3.1标记—清除算法69
    * 3.3.2复制算法70
    * 3.3.3标记—整理算法71
    * 3.3.4分代收集算法72
- 3.4HotSpot的算法实现72
    * 3.4.1枚举根节点72
    * 3.4.2安全点73
    * 3.4.3安全区域74
- 3.5垃圾收集器75
    * 3.5.1Serial收集器76
    * 3.5.2ParNew收集器77
    * 3.5.3ParallelScavenge收集器79
    * 3.5.4SerialOld收集器80
    * 3.5.5ParallelOld收集器80
    * 3.5.6CMS收集器81
    * 3.5.7G1收集器84
    * 3.5.8理解GC日志89
    * 3.5.9垃圾收集器参数总结90
- 3.6内存分配与回收策略91
    * 3.6.1对象优先在Eden分配91
    * 3.6.2大对象直接进入老年代93
    * 3.6.3长期存活的对象将进入老年代95
    * 3.6.4动态对象年龄判定97
    * 3.6.5空间分配担保98
- 3.7本章小结100

### 第4章虚拟机性能监控与故障处理工具101
- 4.1概述101
- 4.2JDK的命令行工具101
    * 4.2.1jps：虚拟机进程状况工具104
    * 4.2.2jstat：虚拟机统计信息监视工具105
    * 4.2.3jinfo：Java配置信息工具106
    * 4.2.4jmap：Java内存映像工具107
    * 4.2.5jhat：虚拟机堆转储快照分析工具108
    * 4.2.6jstack：Java堆栈跟踪工具109
    * 4.2.7HSDIS：JIT生成代码反汇编111
- 4.3JDK的可视化工具114
    * 4.3.1JConsole：Java监视与管理控制台115
    * 4.3.2VisualVM：多合一故障处理工具122
- 4.4本章小结131
### 第5章调优案例分析与实战132
- 5.1概述132
- 5.2案例分析132
    * 5.2.1高性能硬件上的程序部署策略132
    * 5.2.2集群间同步导致的内存溢出135
    * 5.2.3堆外内存导致的溢出错误136
    * 5.2.4外部命令导致系统缓慢137
    * 5.2.5服务器JVM进程崩溃138
    * 5.2.6不恰当数据结构导致内存占用过大139
    * 5.2.7由Windows虚拟内存导致的长时间停顿141
- 5.3实战：Eclipse运行速度调优142
    * 5.3.1调优前的程序运行状态142
    * 5.3.2升级JDK1.6的性能变化及兼容问题145
    * 5.3.3编译时间和类加载时间的优化150
    * 5.3.4调整内存设置控制垃圾收集频率153
    * 5.3.5选择收集器降低延迟157
- 5.4本章小结160

## 第三部分虚拟机执行子系统
### 第6章类文件结构162
- 6.1概述162
- 6.2无关性的基石162
- 6.3Class类文件的结构164
- 6.4字节码指令简介196
    * 6.4.1字节码与数据类型197
    * 6.4.2加载和存储指令199
    * 6.4.3运算指令200
    * 6.4.4类型转换指令202
    * 6.4.5对象创建与访问指令203
    * 6.4.6操作数栈管理指令203
    * 6.4.7控制转移指令204
    * 6.4.8方法调用和返回指令204
    * 6.4.9异常处理指令205
    * 6.4.10同步指令205
- 6.5公有设计和私有实现206
- 6.6Class文件结构的发展207
- 6.7本章小结208
### 第7章虚拟机类加载机制209
- 7.1概述209
- 7.2类加载的时机210
- 7.3类加载的过程214
    * 7.3.1加载214
    * 7.3.2验证216
    * 7.3.3准备219
    * 7.3.4解析220
    * 7.3.5初始化225
- 7.4类加载器227
    * 7.4.1类与类加载器228
    * 7.4.2双亲委派模型229
    * 7.4.3破坏双亲委派模型233
- 7.5本章小结235
### 第8章虚拟机字节码执行引擎236
- 8.1概述236
- 8.2运行时栈帧结构236
    * 8.2.1局部变量表238
    * 8.2.2操作数栈242
    * 8.2.3动态连接243
    * 8.2.4方法返回地址243
    * 8.2.5附加信息244
- 8.3方法调用244
    * 8.3.1解析244
    * 8.3.2分派246
    * 8.3.3动态类型语言支持258
- 8.4基于栈的字节码解释执行引擎269
    * 8.4.1解释执行269
    * 8.4.2基于栈的指令集与基于寄存器的指令集270
    * 8.4.3基于栈的解释器执行过程272
- 8.5本章小结275
### 第9章类加载及执行子系统的案例与实战276
- 9.1概述276
- 9.2案例分析276
    * 9.2.1Tomcat：正统的类加载器架构276
    * 9.2.2OSGi：灵活的类加载器架构279
    * 9.2.3字节码生成技术与动态代理的实现282
    * 9.2.4Retrotranslator：跨越JDK版本286
- 9.3实战：自己动手实现远程执行功能289
    * 9.3.1目标290
    * 9.3.2思路290
    * 9.3.3实现291
    * 9.3.4验证298
- 9.4本章小结299

## 第四部分程序编译与代码优化
### 第10章早期（编译期）优化302
- 10.1概述302
- 10.2Javac编译器303
    * 10.2.1Javac的源码与调试303
    * 10.2.2解析与填充符号表305
    * 10.2.3注解处理器307
    * 10.2.4语义分析与字节码生成307
- 10.3Java语法糖的味道311
    * 10.3.1泛型与类型擦除311
    * 10.3.2自动装箱、拆箱与遍历循环315
    * 10.3.3条件编译317
- 10.4实战：插入式注解处理器318
    * 10.4.1实战目标318
    * 10.4.2代码实现319
    * 10.4.3运行与测试326
    * 10.4.4其他应用案例327
- 10.5本章小结328
### 第11章晚期（运行期）优化329
- 11.1概述329
- 11.2HotSpot虚拟机内的即时编译器329
    * 11.2.1解释器与编译器330
    * 11.2.2编译对象与触发条件332
    * 11.2.3编译过程337
    * 11.2.4查看及分析即时编译结果339
- 11.3编译优化技术345
    * 11.3.1优化技术概览346
    * 11.3.2公共子表达式消除350
    * 11.3.3数组边界检查消除351
    * 11.3.4方法内联352
    * 11.3.5逃逸分析354
- 11.4Java与C/C++的编译器对比356
- 11.5本章小结358

## 第五部分高效并发
### 第12章Java内存模型与线程360
- 12.1概述360
- 12.2硬件的效率与一致性361
- 12.3Java内存模型362
    * 12.3.1主内存与工作内存363
    * 12.3.2内存间交互操作364
    * 12.3.3对于volatile型变量的特殊规则366
    * 12.3.4对于long和double型变量的特殊规则372
    * 12.3.5原子性、可见性与有序性373
    * 12.3.6先行发生原则375
- 12.4Java与线程378
    * 12.4.1线程的实现378
    * 12.4.2Java线程调度381
    * 12.4.3状态转换383
- 12.5本章小结384
### 第13章线程安全与锁优化385
- 13.1概述385
- 13.2线程安全385
    * 13.2.1Java语言中的线程安全386
    * 13.2.2线程安全的实现方法390
- 13.3锁优化397
    * 13.3.1自旋锁与自适应自旋398
    * 13.3.2锁消除398
    * 13.3.3锁粗化400
    * 13.3.4轻量级锁400
    * 13.3.5偏向锁402
- 13.4本章小结403

## 附录
- 附录A编译Windows版的OpenJDK406
- 附录B虚拟机字节码指令表414
- 附录CHotSpot虚拟机主要参数表420
- 附录D对象查询语言（OQL）简介424
- 附录EJDK历史版本轨迹430
