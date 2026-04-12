# RL_Learning
---
## 介绍
1. 第一章：概念
    - state，action,reward,return,episode,policy
    - 网格例子
    - MDP马尔可夫决策
2. 第二章：**贝尔曼公式**
   - 状态价值函数
   - 贝尔曼公式：描述所有状态与状态值的关 系
   - 策略评价（policy evaluation）
3. 第三章：**贝尔曼最优公式**
   - 最优策略对应的贝尔曼公式
   - 最优策略
   - 最优状态价值函数
   - 贝尔曼最优公式
4. 第四章：**VI与PI**
   - VI：value iteration
   - PI：policy ～
   - Truncated policy ～
   - 迭代式的方法
5. 第五章：**蒙特卡洛方法**
   - 无模型的寻找最优策略的方法
   - 计算state value
   - 没有模型就要有数据
   - 离散随机变量的期望值
   - MC basic
   - MC exploring starts
   - MC epsilon-greedy
6. 第六章：**随机近似理论** 
   - 从non-incremental到incremental
   - 问题：估计随机变量的EX：什么是non_incremental
   - RM算法：g(w)=0的方程,但是无需gw的公式
   - SGD,随机梯度下降，是一种特殊的RM
   - BGD，BGD,MBGD
7. 第七章：**时序差分方法**TD
   - 计算state value
   - Sarsa方法，计算action value
   - Q-learning，直接计算optimal-action values
   - on-policy, off-policy
   - target policy与behavior policy
   - 两者不同：off policy
8. 第八章：**状态价值函数近似**、
   - VFA（value function approximation）
   - Sarsa with VFA
   - Q-learning with VFA
   - DQN(Deep Q-Learning)
   - 神经网络拟合函数
9. 第九章：**policy-based方法**
   - policy gredient
   - 梯度上升（REINFORCE）
10. 第十章：**actor-critic**：policy-based+value-based方法
    - 更新策略的参数（actor）
    - 更新需要q
    - 最简单的：QAC
    - Advantage：A2C
    - off-policy：重要性采样
    - 确定性策略：DPG