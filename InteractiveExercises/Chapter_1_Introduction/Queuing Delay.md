# Queuing Delay | 排队时延

Consider the queuing delay in a router buffer, where the packet experiences a delay as it waits to be transmitted onto the link. The length of the queuing delay of a specific packet will depend on the number of earlier-arriving packets that are queued and waiting for transmission onto the link. If the queue is empty and no other packet is currently being transmitted, then our packet’s queuing delay will be zero. On the other hand, if the traffic is heavy and many other packets are also waiting to be transmitted, the queuing delay will be long.  
考虑路由器缓冲区中的排队时延，在该缓冲区中，数据包在等待传输到链路上时会经历一定的延迟。特定数据包的排队时延取决于之前到达并在队列中等待传输到链路上的数据包数量。如果队列为空，并且当前没有其他数据包正在传输，则该数据包的排队时延为零。另一方面，如果流量很大，许多其他数据包也在等待传输，则排队时延会很长。

![Queuing Delay](../image/Queuing%20Delay.png)

Assume a constant transmission rate of R = 800000 bps, a constant packet-length L = 5100 bits, and a is the average rate of packets/second. Traffic intensity I = La/R, and the queuing delay is calculated as I(L/R)(1 - I) for I < 1.  
假设传输速率为 R = 800000 bps，数据包长度 L = 5100 比特，a 为平均每秒到达的数据包数量。流量强度 I = La/R，当 I < 1 时，排队时延计算公式为 I(L/R)(1 - I)。

---

### 1. In practice, does the queuing delay tend to vary a lot? Answer with Yes or No  在实际情况下，排队时延是否变化很大？请回答 Yes 或 No。

> **Hint:** See section 1.4 in the text for more information on queuing delay  
> **提示:** 参考教材 1.4 节获取更多关于排队时延的信息  
> **Answer:** Yes  
> **答案:** Yes  

---

### 2. Assuming that a = 37, what is the queuing delay? Give your answer in milliseconds (ms)  假设 a = 37，排队时延是多少？请以毫秒 (ms) 为单位给出答案。

> **Hint:** Use the formula given above to calculate the queuing delay  
> **提示:** 使用上述公式计算排队时延  
> **Answer:** 1.1491  
> **答案:** 1.1491  

---

### 3. Assuming that a = 67, what is the queuing delay? Give your answer in milliseconds (ms)  假设 a = 67，排队时延是多少？请以毫秒 (ms) 为单位给出答案。

> **Hint:** Use the formula given above to calculate the queuing delay  
> **提示:** 使用上述公式计算排队时延  
> **Answer:** 1.5599  
> **答案:** 1.5599  

---

### 4. Assuming the router's buffer is infinite, the queuing delay is 1.5599 ms, and 724 packets arrive. How many packets will be in the buffer 1 second later?  假设路由器的缓冲区是无限的，排队时延为 1.5599 ms，并且有 724 个数据包到达。1 秒后缓冲区中还会有多少个数据包？

> **Hint:** The number of packets left in the buffer after 1 second can be calculated with the formula: packets - (60/qdelay) rounded down  
> **提示:** 1 秒后缓冲区中的数据包数量可通过公式计算：数据包总数 - (60/qdelay)，向下取整  
> **Answer:** 83  
> **答案:** 83  

---

### 5. If the buffer has a maximum size of 500 packets, how many of the 724 packets would be dropped upon arrival from the previous question?  如果缓冲区的最大容量为 500 个数据包，那么在前一个问题的情况下，会有多少个数据包在到达时被丢弃？

> **Hint:** The number of packets dropped can be calculated with the formula: a - buffer size (if less than 0, then no packets are lost)  
> **提示:** 丢弃的数据包数量可通过公式计算：a - 缓冲区大小（如果小于 0，则没有数据包丢失）  
> **Answer:** 224  
> **答案:** 224  

---
