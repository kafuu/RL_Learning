# 值迭代与策略迭代
---
## 值迭代
值迭代实际就是贝尔曼最优公式的求解过程
1. 值迭代的两个步骤：
   - **policy更新**：求出$v_k$对应最优的$\pi_{k+1}$
   - **value更新**：求出$v_{k+1}$,$v_{k+1}=r_{\pi_{k+1}}+\gamma P_{\pi_{k+1}}v_k$
2. Value iteration:
   1. Policy update: 已知$q_k(s,a)$，求最大的策略$\pi_{k+1}(s)$ 
   2. Value update: 求出$v_{k+1}(s)$
   3. 路径：$$v_k(s)\rightarrow q_k(s,a)\rightarrow greedy\ policy\ \pi_{k+1}(a|s)\rightarrow new\ value\ v_{k+1}=\max_aq_k(s,a)$$
   4. ```如果$v_k$还没有收敛```

<div style="height: 1000px;"></div> 