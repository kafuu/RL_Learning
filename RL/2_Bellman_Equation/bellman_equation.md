# 贝尔曼公式Bellman Equation
---
1. Return 是 一个trajectory的reward之和
2. return十分重要，环境一模一样，但是采取不同的策略：
![alt text](image.png)
3. 为了将不同的策略进行对比，需要对不同策略产生的trajectory的return期望进行对比
4. 对于策略1，return为：$0+\gamma1+\gamma^21……=\frac{\gamma}{1-\gamma}$
5. 对于策略2,return为$-1+\gamma1+\gamma^21……=-1+\frac{\gamma}{1-\gamma}$
6. 对于策略3，return为$-0.5+\frac{\gamma}{1-\gamma}$
7. 策略3实际上即是代表S tate value
8. 另一种计算return的方法：用$v_i$表示$s_i$状态开始的return，**递归法**求解return：$v_i=r_i+\gamma v_{i+1}$
![alt text](image-1.png)
例如，$v_1=r_1+\gamma v_2$
这被成为**Bootstrapping**
9. 这种循环关系，看似不可能求解，但是实际上：
$\bold{v}=\bold{r}+\gamma\bold{Pv}$
在此例中$P=\begin{bmatrix}
    0,1,0,0\\
    0,0,1,0\\
    0,0,0,1\\
    1,0,0,0\\
\end{bmatrix}$
即$\bold{(I-\gamma P)v}=\bold{r}$，求解方程组就可以得到$\bold{v}$
$\bold{v}=\bold{r}+\gamma\bold{Pv}$即最简单的确定性的策略下的贝尔曼公式 

## State Value
考虑这样一个单步的过程：$S_t\xrightarrow{A_t}R_{t+1},S_{t+1}$
其中$S_t,A_t,R_{t+1}$都是random variables,也就是可以求exception
![alt text](image-2.png)
对一个trajectory求discounted return,记为$G_t$
1. 那么state value**就是$G_t$的expectation** 
2. 用$v_\pi(s)=E[G_t|S_t=s]$表示state value ,(一个条件期望,state取一个具体的值)
3. $v_\pi(s)$是一个s的函数
4. $v_\pi(s)$是一个$\pi$(策略)的函数
5. value大,则代表state更有价值

- return与state value的关系:return针对单个trajectory,state value是多个trajectory的期望

例子:三个不同策略下的state value
![alt text](image-3.png)

## Bellman Equation


## Action value