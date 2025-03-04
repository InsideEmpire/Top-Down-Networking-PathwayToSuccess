# Car - Caravan Analogy | 汽车 - 车队类比

Consider the figure below, adapted from Figure 1.17 in the text, which draws the analogy between store-and-forward link transmission and propagation of bits in packet along a link, and cars in a caravan being serviced at a toll booth and then driving along a road to the next tollbooth.  
考虑下图，该图改编自教材中的图 1.17，它将存储转发链路传输与分组沿链路传播的比特进行类比，以及收费站服务车辆并驶向下一个收费站的车队进行类比。

![Caravan-Analogy](../image/Caravan-Analogy.png)

Suppose the caravan has 5 cars, and that the tollbooth services (that is, transmits) a car at a rate of one car per 1 second. Once receiving service, a car proceeds to the next tollbooth, which is 400 kilometers away at a rate of 20 kilometers per second. Also assume that whenever the first car of the caravan arrives at a tollbooth, it must wait at the entrance to the tollbooth until all of the other cars in its caravan have arrived and lined up behind it before being serviced at the toll booth. (That is, the entire caravan must be stored at the tollbooth before the first car in the caravan can pay its toll and begin driving towards the next tollbooth).  
假设车队有 5 辆车，收费站的服务速率（即传输速率）为每秒 1 辆车。当一辆车接受完服务后，它会以 20 公里/秒的速度行驶 400 公里到下一个收费站。此外，假设当车队的第一辆车到达收费站时，它必须等到车队中的所有其他车辆都到达并排在其后，才能开始接受服务（也就是说，整个车队必须先存储在收费站，第一辆车才能支付通行费并驶向下一个收费站）。

---

### 1. Once a car enters service at the tollbooth, how long does it take until it leaves service? 一辆车进入收费站接受服务后，需要多长时间才能完成服务？

> **Hint:** This value is given in the prompt  
> **提示:** 该值在题目中已给出  
> **Answer:** 1  
> **答案:** 1  

---

### 2. How long does it take for the entire caravan to receive service at the tollbooth (that is, the time from when the first car enters service until the last car leaves the tollbooth)? 整个车队在收费站接受服务需要多长时间（即从第一辆车进入服务到最后一辆车离开收费站的时间）？

> **Hint:** Try taking the time to service multiplied by number of cars  
> **提示:** 尝试将服务时间乘以车辆数  
> **Answer:** 5  
> **答案:** 5  

---

### 3. Once the first car leaves the tollbooth, how long does it take until it arrives at the next tollbooth? 第一辆车离开收费站后，需要多长时间才能到达下一个收费站？

> **Hint:** The time taken can be calculated by dividing the distance by the car's speed  
> **提示:** 可通过距离除以车辆速度计算时间  
> **Answer:** 20  
> **答案:** 20  

---

### 4. Once the last car leaves the tollbooth, how long does it take until it arrives at the next tollbooth? 最后一辆车离开收费站后，需要多长时间才能到达下一个收费站？

> **Hint:** The time taken can be calculated by dividing the distance by the car's speed  
> **提示:** 可通过距离除以车辆速度计算时间  
> **Answer:** 20  
> **答案:** 20  

---

### 5. Once the first car leaves the tollbooth, how long does it take until it enters service at the next tollbooth? 第一辆车离开收费站后，需要多长时间才能在下一个收费站接受服务？

> **Hint:** Take the time to service all cars but one, summed with the time it takes every car to reach the next toll booth  
> **提示:** 计算所有车辆（除第一辆外）的服务时间，并加上每辆车到达下一个收费站的时间  
> **Answer:** 24  
> **答案:** 24  

---

### 6. Are there ever two cars in service at the same time, one at the first toll booth and one at the second toll booth? Answer Yes or No 是否曾经有两辆车同时在接受服务，一辆在第一个收费站，另一辆在第二个收费站？请回答“是”或“否”

> **Hint:** Cars can't get service at the next tollbooth until all cars have arrived  
> **提示:** 只有当所有车辆到达后，才能在下一个收费站接受服务  
> **Answer:** No  
> **答案:** 否  

---

### 7. Are there ever zero cars in service at the same time, i.e., the caravan of cars has finished at the first toll booth but not yet arrived at the second tollbooth? Answer Yes or No 是否曾经有一段时间，所有车辆都不在接受服务，即整个车队已经完成第一个收费站的服务但尚未到达第二个收费站？请回答“是”或“否”

> **Hint:** There is a situation where the last car in the caravan, after being serviced but still traveling, will result in no cars being serviced until it arrives  
> **提示:** 当车队的最后一辆车接受完服务但仍在行驶时，会出现这种情况  
> **Answer:** Yes  
> **答案:** 是  

---
