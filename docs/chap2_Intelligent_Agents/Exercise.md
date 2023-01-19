# 第二章习题

# Exercise 1
> Suppose that the performance measure is concerned with just the first $T$ time steps of the environment and ignores everything thereafter. Show that a rational agent’s action may depend not just on the state of the environment but also on the time step it has reached.

# Exercise 2

> Let us examine the rationality of various vacuum-cleaner agent functions.
> 1. Show that the simple vacuum-cleaner agent function described in Figure [vacuum-agent-function-table](https://aimacode.github.io/aima-exercises/figures/vacuum-agent-function-table.png) is indeed rational under the assumptions listed on page vacuum-rationality-page
> 2. Describe a rational agent function for the case in which each movement costs one point. Does the corresponding agent program require internal state?
> 3. Discuss possible agent designs for the cases in which clean squares can become dirty and the geography of the environment is unknown. Does it make sense for the agent to learn from its experience in these cases? If so, what should it learn? If not, why not?











# Exercise 5

> For each of the following activities, give a PEAS description of the task environment and characterize it in terms of the properties listed in Section 
> \- Playing soccer.
> \- Exploring the subsurface oceans of Titan.
> \- Shopping for used AI books on the Internet.
> \- Playing a tennis match.
> \- Practicing tennis against a wall.
> \- Performing a high jump.
> \- Knitting a sweater.
> \- Bidding on an item at an auction. 



>  对于以下每个活动，给出任务环境的 PEAS 描述，并根据部分中列出的属性对其进行表征 
> \- 踢足球。
> \- 探索土卫六的地下海洋。
> \- 在互联网上购买二手 AI 书籍。
> \- 打网球比赛。
> \- 靠墙练习网球。
> \- 表演跳高。
> \- 织毛衣。
> \- 在拍卖会上竞标一件物品。 

## 2.5.1 PEAS：

|                            | 性能度量               | 环境                   | 执行器                     | 传感器                               |
| -------------------------- | ---------------------- | ---------------------- | -------------------------- | ------------------------------------ |
| 踢足球                     | 进球数、抢断数、犯规数 | 足球场、参赛选手、裁判 | 腿、头、胸                 | 高速摄像机、红外传感器、超声传感器   |
| 探索土卫六的地下海洋       | 正确感知地理环境       | 地下海洋、礁石、暗流   | 发动机、探测器             | 温度传感器、红外传感器、超声波传感器 |
| 在互联网上购买二手 AI 书籍 | 花费最小、质量最佳     | 店铺商品信息           | 计算机                     | 计算机                               |
| 打网球比赛                 | 个人得分、胜负         | 网球场、竞争对手       | 带关节的手臂、腿           | 超声波传感器，摄像头                 |
| 靠墙练习网球               | 成功击球数             | 墙                     | 带关节的手臂               | 超声波传感器                         |
| 表演跳高                   | 跳跃高度、动作美观度   | 跳高架、杆             | 腿、腰                     | 高度输入                             |
| 织毛衣                     | 毛线整齐度、花纹美观度 | 针、线                 | 手                         | 关节角度传感器、触觉传感器           |
| 在拍卖会上竞标一件物品     | 成交价最小化           | 拍卖对手               | CPU、GPU、策略反馈的显示器 | 价格输入                             |

## 2.5.2 属性：

|                            | 可观测     | 智能体 | 确定性 | 回合式 | 静态   | 离散 |
| :------------------------: | ---------- | :----: | :----: | :----: | ------ | ---- |
|           踢足球           | 部分可观测 |   多   | 不确定 |  回合  | 动态   | 连续 |
|    探索土卫六的地下海洋    | 部分可观测 |   单   | 不确定 |  序贯  | 半动态 | 连续 |
| 在互联网上购买二手 AI 书籍 | 完全可观测 |   单   |  确定  |  序贯  | 静态   | 离散 |
|         打网球比赛         | 部分可观测 |   多   | 不确定 |  序贯  | 动态   | 连续 |
|        靠墙练习网球        | 完全可观测 |   单   |  确定  |  回合  | 动态   | 连续 |
|          表演跳高          | 完全可观测 |   单   |  确定  |  回合  | 静态   | 离散 |
|           织毛衣           | 完全可观测 |   单   |  确定  |  序贯  | 动态   | 连续 |
|   在拍卖会上竞标一件物品   | 部分可观测 |   多   | 不确定 |  序贯  | 动态   | 连续 |



# Exercise 6

题目和Exercise 5 相同




# Exercise 7

> For each of the following act
>
> Define in your own words the following terms: agent, agent function, agent program, rationality, autonomy, reflex agent, model-based agent, goal-based agent, utility-based agent, learning agent. 



> 用你自己的话定义以下术语：智能体、智能体函数、智能体程序、理性、自主、反射智能体、基于模型的智能体、基于目标的智能体、基于效用的智能体、学习智能体。 



**智能体**：任何通过传感器、感知环境并通过执行器作用于该环境的事物都可以被视为智能体（agent）。

**智能体函数**：将任意一个给定的感知序列映射到一个动作，即，接收消息产生动作。

**智能体程序**：将当前的感知作为传感器的输入，并将动作返回给执行器。

**理性**：对于每个可能接收到的感知序列，给定感知序列的性能度量、先验知识，选择一个期望最大化的动作。

**自主**：不依赖于设计者的先验知识，能通过自身的感知进行学习和弥补不正确的先验知识。

**反射智能体**：根据当前感知选择动作。

**基于模型的智能体**： 转移模型和传感器模型结合在一起让智能体能够在传感器受限的情况下尽可能地跟踪世界的状态。

**基于目标的智能体**： 根据当前的感知序列和理想目标的信息，选择实现目标的动作。

**基于效用的智能体**： 根据性能度量函数，最大化其动作结果的期望效用，即效用函数最大化。

**学习型智能体**：根据感知序列，对智能体的各个组件进行改进，使得各组件与可用的反馈信息更接近，达到提高整体性能的目的。





# Exercise 8

> This exercise explores the differences between agent functions and agent programs.
>
> 1. Can there be more than one agent program that implements a given agent function? Give an example, or show why one is not possible.
> 2. Are there agent functions that cannot be implemented by any agent program?
> 3. Given a fixed machine architecture, does each agent program implement exactly one agent function?
> 4. Given an architecture with nn bits of storage, how many different possible agent programs are there?
> 5. Suppose we keep the agent program fixed but speed up the machine by a factor of two. Does that change the agent function? 



> 本练习探讨了智能体功能和智能体程序之间的差异。
>
> 1. 是否可以有多个智能体程序实现给定的智能体函数？举个例子，或者说明为什么不可能。
> 2. 是否有任何智能体程序无法实现的智能体功能？
> 3. 给定一个固定的机器架构，每个智能体程序是否只实现一个智能体功能？
> 4. 给定一个架构nn存储位，有多少种不同的可能智能体程序？
> 5. 假设我们保持智能体程序不变，但将机器速度提高两倍。这会改变智能体功能吗？ 



1. 可以。例如，智能体在较大的区域搜寻目标时，智能体函数是用最少的时间找到目标。多个智能体协同搜寻目标，同时扫描不同的区域，协同反馈给智能体函数，最终搜寻到目标。

2. 有。当智能体程序无法通过感知序列或先验知识对当前动作或状态进行判断，从而不能产生动作时。例如，让机器人说出我在想什么？

3. 看具体功能，如果智能体程序不需要交互，是独立运行的，就只实现一个智能体功能；如果需要交互，就不是。

4. $$
   2^{n}种
   $$

5. 当任务是序贯且连续发生的，结果可能会发生改变；当任务是静态且离散时，结果不会发生改变


# Exercise 13


> Consider a modified version of the vacuum environment in Exercise [2.10](https://aimacode.github.io/aima-exercises/agents-exercises/ex_10), in which the agent is penalized one point for each movement.
> 
> 1. Can a simple reflex agent be perfectly rational for this environment? Explain
> 2. What about a reflex agent with state? Design such an agent
> 3. How do your answers to 1 and 2 change if the agent’s percepts give it the clean/dirty status of every square in the environment?


> 考虑练习2.10中真空环境的一个修改版本，在该版本中，每行动一次，智能体将被罚一分。
> 
> 1. 对于这种环境，一个简单反射型智能体是否完全合理？请做出解释
> 2. 那么带有状态的反射型智能体呢？请设计一个这样的智能体
> 3. 如果智能体的感知为环境中每个广场的清洁/肮脏状态，您对1和2的回答会如何变化



# Exercise 15

> Repeat Exercise [2.13](https://aimacode.github.io/aima-exercises/agents-exercises/ex_13) for the case in which the location sensor is replaced with a “bump” sensor that detects the agent’s attempts to move into an obstacle or to cross the boundaries of the environment. Suppose the bump sensor stops working; how should the agent behave?


> 对于位置传感器被替换为”碰撞“传感器的情况，该传感器可以检测到智能体进入障碍物或者越过环境边界的尝试。重复练习2.13。假设碰撞传感器停止工作，智能体该如何表现？


# Exercise 16

>The vacuum environments in the preceding exercises have all been deterministic. Discuss possible agent programs for each of the following stochastic versions:
> 1. Murphy’s law: twenty-five percent of the time, the $Suck$ action fails to clean the floor if it is dirty and deposits dirt onto the floor if the floor is clean. How is your agent program affected if the dirt sensor gives the wrong answer 10% of the time?
> 2. Small children: At each time step, each clean square has a 10% chance of becoming dirty. Can you come up with a rational agent design for this case?

### 翻译
> 前面练习中的真空环境都是确定性的。下面讨论一下以下每个随机版本的可能代理程序。
> 1. 墨菲定律：25%的时间里，如果地板是脏的，$吸吮$动作就不能清洁; 如果地板是干净的，就会在地板上沉积灰尘。如果污垢传感器在10%的时间内给出错误的答案，你的代理程序会受到什么影响？
> 2. Small children：在每个时间步骤中，每个干净的方块有10%的机会变脏。你能为这种情况想出一个合理的代理设计吗？

### 参考答案
>1. The failure of $Suck$ action doesn’t cause any problem at all as long as we replace
the reflex agent’s $‘Suck’$ action by $‘Suck\ until\ clean’$\
If the dirt sensor can be wrong on each step, then the agent
might want to wait for a few steps to get a more reliable measurement before deciding whether to $Suck$ or
move on to a new square. Obviously, there is a trade-off because waiting too long means that dirt remains
on the floor (incurring a penalty), but acting immediately risks either dirtying a clean square or ignoring a
dirty square (if the sensor is wrong). A rational agent must also continue touring and checking the squares
in case it missed one on a previous tour (because of bad sensor readings). It is not immediately obvious
how the waiting time at each square should change with each new tour. These issues can be clarified by
experimentation, which may suggest a general trend that can be verified mathematically. This problem is a
partially observable Markov decision process, which we’ll talk about in Chapter 17. Such problems are
hard in general, but some special cases may be amenable to careful analysis. \
> 只要我们把智能体反应的'吸食'动作换成'吸食到干净为止'，吸食动作的失败就完全不会造成任何问题。\
如果污垢传感器在每一步上都可能出错，那么智能体可以选择等待几步以获得更可靠的测量结果，然后再决定是吸食还是继续前进到一个新的位置。显然，这是一个权衡，因为等待的时间太长意味着污物仍在地板上（招致惩罚），但立即行动有可能弄脏一个干净的方块或忽略一个肮脏的方块（如果传感器是错误的）。一个理性的智能体还必须继续巡视和检查每个位置，以防它在以前的巡视中错过了一个位置（因为传感器的读数不好）。每一个方块的等待时间应该如何随着每一次新的巡查而变化，这一点很困难，不过这些问题可以通过实验来明晰，需要用数学方法验证来一般趋势。这个问题是一个部分可观察的马尔可夫决策过程，我们将在第17章中谈论这个问题。这样的问题一般来说是很难的，但一些特殊情况可能是可以仔细分析的。
> 2. In this case, the agent must keep touring the squares indefinitely. The probability that a square is dirty
increases monotonically with the time since it was last cleaned, so the rational strategy is, roughly
speaking, to repeatedly execute the shortest possible tour of all squares. (We say “roughly speaking”
because there are complications caused by the fact that the shortest tour may visit some squares twice,
depending on the geography.) This problem is also a partially observable Markov decision process.\
在这种情况下，智能体必须无限期地巡视这些方格。一个广场被弄脏的概率随着它上次被清理的时间而单调增加，因此，大致上说，合理的策略是重复执行对所有广场的最短巡回。(我们说 "大致上 "是因为最短的巡视可能会访问某些方格两次，这是一个复杂的事实，取决于地理环境）。这个问题也是一个部分可观察的马尔可夫决策过程。

