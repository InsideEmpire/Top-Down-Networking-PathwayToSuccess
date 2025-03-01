# CIRCUIT SWITCHING | 电路交换  
Consider the circuit-switched network shown in the figure below, with circuit switches A, B, C, and D. Suppose there are 12 circuits between A and B, 15 circuits between B and C, 12 circuits between C and D, and 15 circuits between D and A.  
请参考下图的电路交换网络，电路交换机为A、B、C和D。假设A和B之间有12条电路，B和C之间有15条电路，C和D之间有12条电路，D和A之间有15条电路。  
![circuit-switched](../src/circuit-switched.png)

---

### 1. What is the maximum number of connections that can be ongoing in the network at any one time? 当网络中有连接时，最多可以有多少个连接同时进行？

> **Hint:** The maximum number of connections is the sum of all links  
> **提示:** 最大连接数等于所有链路电路数量的总和  
> **Answer:** 54  
> **答案:** 54  
> **Explanation:** The maximum number of ongoing connections in the network is the sum of the number of circuits on all links:  
12 (A-B) + 15 (B-C) + 12 (C-D) + 15 (D-A) = 54  
**解释:** 网络中最大连接数等于所有链路的电路数量之和：  
12 (A-B) + 15 (B-C) + 12 (C-D) + 15 (D-A) = 54

---

### 2. Suppose that these maximum number of connections are all ongoing. What happens when another call connection request arrives to the network, will it be accepted? Answer Yes or No 假设这些最大数量的连接都已经进行。如果新的呼叫请求到达网络，它会被接受吗？是或否。

> **Hint:** If all connections are full, the request will be blocked  
> **提示:** 如果所有连接都已满，新的请求将会被阻塞  
> **Answer:** No  
> **答案:** 不  
> **Explanation:** If the network already has the maximum number of connections (i.e., 54), any new call connection request will be blocked because all circuits are occupied.  
**解释:** 如果网络中已有最大数量的连接（即54个），再有新的呼叫请求到来时，网络无法接受新的连接，因为所有的电路都已被占用。

---

### 3. Suppose that every connection requires 2 consecutive hops, and calls are connected clockwise. For example, a connection can go from A to C, from B to D, from C to A, and from D to B. With these constraints, what is the maximum number of connections that can be ongoing in the network at any one time? 假设每个连接需要两个连续的跳数，并且连接是顺时针的。例如，一个连接可以从A到C，从B到D，从C到A，或从D到B。在这些限制下，最多可以有多少个连接同时进行？

> **Hint:** Find the max between the sum of the bottleneck links for cases A->C and B->D, but don't forget about bottleneck links  
> **提示:** 找到A->C和B->D情况下瓶颈链路数量的最大值，但不要忘记考虑瓶颈链路  
> **Answer:** 24  
> **答案:** 24  
> **Explanation:** In this case, each connection requires two consecutive hops. To calculate the bottleneck links for each direction:
> - From A to C, it requires A-B (12) and B-C (15), so the bottleneck link is 12.
> - From B to D, it requires B-C (15) and C-D (12), so the bottleneck link is 12.
> - From C to A, it requires C-D (12) and D-A (15), so the bottleneck link is 12.
> - From D to B, it requires D-A (15) and A-B (12), so the bottleneck link is 12.
> 
> Therefore, the maximum number of ongoing connections is 12 + 12 = 24.  
**解释:** 在这个情况下，连接需要两个连续的跳数。因此，要计算每个方向的瓶颈链路数量：
> - 从A到C，需要A-B (12条) 和 B-C (15条) 的链路，所以瓶颈链路是12。
> - 从B到D，需要B-C (15条) 和 C-D (12条) 的链路，所以瓶颈链路是12。
> - 从C到A，需要C-D (12条) 和 D-A (15条) 的链路，所以瓶颈链路是12。
> - 从D到B，需要D-A (15条) 和 A-B (12条) 的链路，所以瓶颈链路是12。
>
> 最大可用连接数 = 12 + 12 = 24。

---

### 4. Suppose that 20 connections are needed from A to C, and 17 connections are needed from B to D. Can we route these calls through the four links to accommodate all 37 connections? Answer Yes or No 假设需要从A到C的20个连接，以及从B到D的17个连接。我们能通过这四个链路承载所有37个连接吗？是或否

> **Hint:** Taking from the previous question, is the sum of the two connections greater than the value we calculated in question 3?  
> **提示:** 根据第3题，两个连接的数量和是否大于我们在第3题中计算的值？  
> **Answer:** No  
> **答案:** 不  
> **Explanation:** Based on the maximum number of connections we calculated in question 3 (24), and given that 20 connections are required from A to C and 17 from B to D, the sum is 37 connections, which exceeds the maximum of 24. Therefore, not all connections can be accommodated.  
**解释:** 根据第3题计算的最大连接数（24条），而从A到C需要20条连接，从B到D需要17条连接，两者相加为37条连接，超过了24条的最大连接数，因此不能通过现有链路承载所有连接。

---
