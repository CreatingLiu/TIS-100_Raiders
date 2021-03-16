# TIS-100_Raiders

目前仅基础关部分，解法基本都是自己设计，个别谜题参考了网上其它人的答案，因此数据并不优秀，仅可完成关卡目标

## SELF-TEST DIAGNOSTIC(自检诊断)(00150)

### 目标

![image-20210316185639895](README.assets/image-20210316185639895.png)

- 从IN.X读入值然后写到OUT.X
- 从IN.A读入值然后写到OUT.A

### 剧情

![image-20210316185716224](README.assets/image-20210316185716224.png)

> —计算节点检测—微码转储—
>
> 1C15/SA.64 现在无法找到笔，所以在这里我要记笔记。 看起来像短期存储
>
> 05/10/79 ——今天在交换会上得到了这个。Fella想要450美元但我砍到了200美元。好买卖！！！不知道是谁制造的它。TIS系列和体系结构的新奇闻所未闻。
>
> Randy的手上有个谜题！！

### 解法

![image-20210316191840763](README.assets/image-20210316191840763.png)

| CYCLE | NODE | INSTRUCTION |
| ----- | ---- | ----------- |
| 83    | 8    | 8           |

## SIGNAL AMPLIFIER(信号放大器)(10981)

### 目标

![image-20210316192235900](README.assets/image-20210316192235900.png)

- 从IN.A读入值

- 让值变为两倍

- 将值写到OUT.A

### 剧情

![image-20210316192427387](README.assets/image-20210316192427387.png)

> —计算节点检测—微码转储—
>
> 07/18/1979 ——仍在困惑....... 和Bernie在IBM聊天时他说这听起来像是苏联的O_N.A.. 但那为什么手册是用英语写的？？

### 解法

![image-20210316193203488](README.assets/image-20210316193203488.png)

| CYCLE | NODE | INSTRUCTION |
| ----- | ---- | ----------- |
| 160   | 4    | 6           |

## DIFFERENTIAL CONVERTER(差动转换器)(20176)

### 目标

![image-20210316193406441](README.assets/image-20210316193406441.png)

- 从IN.A和IN.B读入值
- 把IN.A-IN.B写到OUT.P
- 把IN.B-IN.A写到OUT.N

### 剧情

![image-20210316193510817](README.assets/image-20210316193510817.png)

>—计算节点检测—微码转储—
>
>07/19/1979 ——真有意思。它看起来I.V.D$I.@SI 有某种静态内存在这个东西里面。被编码了一些东西或者别的什么。

### 解法

![image-20210316193825244](README.assets/image-20210316193825244.png)

| CYCLE | NODE | INSTRUCTION |
| ----- | ---- | ----------- |
| 201   | 5    | 11          |

## SIGNAL COMPARATOR(信号比较器)(21340)

### 目标

![image-20210316194631190](README.assets/image-20210316194631190.png)

- 从IN读入一个值
- 如果IN>0就向OUT.G写入1
- 如果IN=0就向OUT.E写入1
- 如果IN<0就向OUT.L写入1
- 如果某个输出没有被写入1，则用0代替

### 剧情

![image-20210316194826549](README.assets/image-20210316194826549.png)

>—计算节点检测—微码转储—
>
>09/03/1979 ——在静态内存中发现了一个块。但是，它是我从未见过的专有格式，找不到它的头和尾。哦兄弟....... 现在有太多种类的机器问世了。我喜欢和它们修补就像下一个兄弟，但是当Tom Dick和Mary的实现他们自己的内存地址方案这全都我&...+...#.D..Z>R..1...`FK.V
>
>下面的会被从计算机市场撤下来，记住我说的话。

### 解法

![image-20210316194612709](README.assets/image-20210316194612709.png)

| CYCLE | NODE | INSTRUCTION |
| ----- | ---- | ----------- |
| 283   | 6    | 20          |

## SIGNAL MULTIPLEXER(信号多路复用器)(22280)

### 目标

![image-20210316200804840](README.assets/image-20210316200804840.png)

- 从IN.A和IN.B读入数据
- 从IN.S读入数据
- IN.S=-1时输出IN.A
- IN.S=1时输出IN.B
- IN.S=0时输出IN.A+IN.B

### 剧情

![image-20210316200924696](README.assets/image-20210316200924696.png)

### 解法

![image-20210316201121226](README.assets/image-20210316201121226.png)

| CYCLE | NODE | INSTRUCTION |
| ----- | ---- | ----------- |
| 204   | 7    | 21          |

## SEQUENCE GENERATOR(序列发生器)(30647)

### 目标

![image-20210316201313904](README.assets/image-20210316201313904.png)

- 序列使用0结束
- 从IN.A和IN.B读入值
- 向OUT写入较小的值
- 向OUT写入较大的值
- 向序列末尾写入0

### 剧情

![image-20210316201559994](README.assets/image-20210316201559994.png)

### 解法

![image-20210316201701279](README.assets/image-20210316201701279.png)

| CYCLE | NODE | INSTRUCTION |
| ----- | ---- | ----------- |
| 126   | 5    | 18          |

## SEQUENCE COUNTER(序列计数器)(31904)

### 目标

![image-20210316201854867](README.assets/image-20210316201854867.png)

- 序列使用0结束
- 从IN读入一个序列
- 向OUT.S写入和
- 向OUT.L写入长度

### 剧情

![image-20210316201959916](README.assets/image-20210316201959916.png)

### 解法

![image-20210316202151872](README.assets/image-20210316202151872.png)

| CYCLE | NODE | INSTRUCTION |
| ----- | ---- | ----------- |
| 122   | 5    | 28          |

## SIGNAL EDGE DETECTOR(信号边沿检测器)(32050)

### 目标

![image-20210316202412934](README.assets/image-20210316202412934.png)

- 从IN读入一个值
- 和上一个值进行比较
- 如果变化超过10则写入1
- 如果没有，写入0
- 第一个输出总是0

### 剧情

![image-20210316202516142](README.assets/image-20210316202516142.png)

### 解法

![image-20210316202621404](README.assets/image-20210316202621404.png)

| CYCLE | NODE | INSTRUCTION |
| ----- | ---- | ----------- |
| 385   | 4    | 14          |

