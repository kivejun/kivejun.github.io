---
title: NOTE：强化学习学习笔记
tags: 强化学习
categories: 强化学习
---
## NOTE：强化学习学习笔记

### 事例：火星探测车



强化学习算法在决定如何采取下一步行动的关键要素：

* state（状态）、action（动作）、R(s) （奖励函数）、state' （下一个状态）

## 1.1、The return in the reinforcement learning



存在折扣因子 $\gamma$ ，使得越早获得奖励使得总回报的价值更高

The return depends on the **actions** you take 

回报是系统获得奖励的总和，经过折扣因子的加权，其中远期奖励的权重是折扣因子提高到更高次幂的结果



## 1.2、Policies in reinforcement learning



1、马尔科夫决策过程（MDP）

* 未来仅取决于当前状态，而不依赖于达到当前状态之前可能发生的任何情况

  where you are now，not how you get here





## 2.1 状态动作价值函数



$ Q_{(s,a)}=$ return if you [考虑自己当前的状态]

* start in state s
* take action a(once)
* then behave optimally after that.



当我处在state s 时，我需要计算在state s下各个动作$a_i$的状态动作价值函数，即$Q_{(s,a)}$，然后比较各个动作的Q函数的大小，取到最大值，即$max Q_{(s,a)}$ ，这样就找到了在state s下的最佳动作 a，得到最佳策略

## 2.2 贝尔曼方程

[参量定义]



贝尔曼方程：

## $ Q_{(s,a)}=R_{(s)}+\gamma \max_{a'}{Q_{(s',a')}}$



相关解释：



### **当前状态的总回报=及时回报+$\gamma \cdot$下一状态最优策略的回报**

## 2.3 随机环境强化学习

* 在执行action a 的时候，有概率执行action b，比如要求向左走，结果最后向右走，即向左走的概率为$p_1$，向右走的概率为$p_2$



### goal of reinforcement learning

注意到在得到预期未来回报时要考虑**期望值** （由s到s'是随机的）