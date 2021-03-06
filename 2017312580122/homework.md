# Homework 7

**P4**
考虑下列交换机。假设所有数据报具有相同长度，交换机以一种分时隙、同步的方式运行，在一个时隙中一个数据报能够从某输入端口传送到某输岀端口。其交换结构是纵横式的，因此在一个时隙中至多一个数据报能够传送到一个给定输出端口，但在一个时隙中不同的输出端口能够接收到来自不同输入端口的数据报。
![J05kut.png](https://s1.ax1x.com/2020/04/24/J05kut.png)

a. 从输入端口到它们的输岀端口传送所示的分组，所需的时隙数量最小是多少？此时假定使用你所需要的任何输入排队调度方法(即此时没有HOL阻塞)。
	1. 在顶部输入队列中发送X，在底部输入队列中发送Y。
	2. 在中间输入队列中发送Y，在底部输入队列中发送Z，
	3. 在中间输入队列中发送Z。
b. 假定采用你能够设计的最差情况下的调度方案，且非空输入队列不会空闲，所需的时隙数量最大是多少？  
基于一个非空输入队列永远不空闲的假设，第一个时隙总是由在顶部输入队列中发送X和在中间或底部输入队列中发送Y组成，而在第二个时隙中，我们总是可以多发送两个数据报，最后一个数据报可以在第三时间时隙发送。

**P7**
考虑使用8比特主机地址的数据报网络。假定一台路由器使用最长前缀匹配并具有下列转发表:
![J0Hdns.png](https://s1.ax1x.com/2020/04/24/J0Hdns.png)
对这4个接口中的每个，给出相应的目的主机地址的范围和在该范围中的地址数量。

接口0: 110 00000 ~ 110 11111 (共32个地址)
接口1: 10 000000 ~ 10 111111 (共64个地址)
接口2: 111 00000 ~ 111 11111 (共32个地址)
接口3: 0 0000000 ~ 0 1111111 (共128个地址)

**P14**
考虑向具有700字节MTU的一条链路发送一个2400字节的数据报。假定初始数据报标有标识号422。将会生成多少个分片？在生成相关分片的数据报中各个字段的值是多少?

原始数据报长度$2400$字节中包含20个字节的IP报头，即实际上的数据长度只有$2380$字节。而分片传输数据长度为$700-20=680$字节，故需要分成$\left \lceil \frac{2380}{680} \right \rceil =4$个分片。
除了最后一个分片，每个片段的大小为700字节，最后一个分片的大小为360字节。这4个分片的偏移量基于($\frac{680}{8} = 85$)的倍数，依次为0，85，170，255。