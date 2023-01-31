# 第三章习题

# Exercise 1

> Explain why problem formulation must follow goal formulation.
>
> 解释为什么问题形式化必须在目标形式化之后。



**参考解答** ： 

> 在目标形式化时，我们决定关注世界的哪些方面，而忽略或抽象掉什么方面。在问题形式化中，我们决定如何处理重要方面（并忽略其他方面）。如果我们首先形式化问题，我们将不知道要关注什么或忽视什么。也就是说，在目标形式化、问题形式化和问题解决之间存在一个迭代循环，直到找到一个足够有用和有效的解决方案为止
>


# Exercise 2

> 针对以下每个问题给出一个完整的问题公式。选择一个精确到足以实施的公式。
>
> 1. 六个玻璃盒子排成一排，每个盒子都有锁。前五个盒子中的每一个中都有一把钥匙，用于解开下一个顺序的盒子的锁；最后一个盒子里有一根香蕉。现在你有第一个盒子的钥匙，你想要得到那根香蕉。
> 2. 你从序列 ABABAECCEC 开始，或者任何以 A, B, C 和 E 组成的序列开始。你可以用以下等式转换这个序列：
>
>    - (1) AC = E,
>    - (2) AB = BC,
>    - (3) BB = E,
>    - (4) E$x$ = $x，$对于任何 $x$ 而言。
>
>    你的目标是将序列转换成 E 序列，（即序列中只有 E 一个成员，就是这个序列：E）。举个例子，序列 ABBC 可以通过变换（BB=E）变为 AEC，然后变成 AC（通过变换 EC = C），最后变为目标序列 E（通过变换 AC = E）。
> 3. 有一个 $n \times n$ 的方格网格，每个方格最初要么是未涂漆的地板，要么是无底的坑。你开始站在一个未喷漆的地板方格上，然后可以在你下面的方格上喷漆，或者移动到相邻的未喷漆地板方格上。你要把整个地板都喷上漆。
> 4. 一艘满载集装箱的船在港口。有 13 排集装箱，每排 13 个集装箱宽，5 个集装箱高。你可以控制一台起重机，该起重机可以移动到船上方的任何位置，拾取其下方的集装箱，并将其移动到码头上。你想把船上的集装箱都卸下来。

**参考解答：**

**（待补充）**



# Exercise 3

> Your goal is to navigate a robot out of a maze. The robot starts in the center of the maze facing north. You can turn the robot to face north, east, south, or west. You can direct the robot to move forward a certain distance, although it will stop before hitting a wall.
1. Formulate this problem. How large is the state space?
2. In navigating a maze, the only place we need to turn is at the intersection of two or more corridors. Reformulate this problem using this observation. How large is the state space now?
3. From each point in the maze, we can move in any of the four directions until we reach a turning point, and this is the only action we need to do. Reformulate the problem using these actions. Do we need to keep track of the robot’s orientation now?
4. In our initial description of the problem we already abstracted from the real world, restricting actions and removing details. List three such simplifications we made.
>
> 你的目标是引导机器人走出迷宫。机器人最开始在迷宫的中心，并且面朝北方。你可以将机器人转向北、东、南或西。您可以指示机器人向前移动一定距离，但它会在撞到墙壁之前停下来。
> 
>1. 形式化这个问题。状态空间有多大？
>2. 在走迷宫时，我们唯一需要转弯的地方是两条或多条走廊的交汇处。使用这个观察重新形式化这个问题。现在状态空间有多大？
>3. 从迷宫中的每个点，我们可以向四个方向中的任何一个方向移动，直到到达一个转折点，这是我们唯一需要做的动作。使用这些动作重新形式化问题。我们现在需要跟踪机器人的方向吗？
>4. 在我们对问题的最初描述中，我们已经从现实世界中抽象出来，限制了动作并删除了细节。列出我们所做的三个简化。



**参考解答** ： 

>1. 
> - 状态：机器人位置和朝向的状态描述。  
> - 初始状态：在迷宫中心，面朝北方。  
> - 动作：向前移动一定距离d；改变机器人的方向。  
> - 转移模型：将状态和动作映射为一个结果状态。  
> - 目标状态: 机器人在出口处。  
> - 动作代价：移动的距离。  
> - 状态空间是无限大的，因为机器人可以处在任何位置。 
> 
>2. 
> - 状态：机器人当前所处的交汇处，以及它所面对的方向  
> - 初始状态：在迷宫中心，面朝北方。  
> - 动作：移动到前面的下一个交汇处（如果存在）。转向新的方向。  
> - 转移模型：将状态和动作映射为一个结果状态。  
> - 目标状态：机器人在出口处。  
> - 动作代价：移动的距离。  
> - 状态空间有 4n 个状态，其中 n 是交叉点的数量。  
> 
>3. 
> - 状态：机器人当前所处的交汇处，以及它所面对的方向
> - 初始状态：在迷宫中心，面朝北方。
> - 动作：移动到北、南、东或西的下一个交汇处。
> - 转移模型：将状态和动作映射为一个结果状态。
> - 目标状态: 机器人在出口处。
> - 动作代价：移动的距离。
> - 状态空间有 4n 个状态，其中 n 是交叉点的数量。
> - 不再需要跟踪机器人的方向，因为它与预测我们行动的结果无关，也不是目标的一部分。
> 
>4. 
> - 状态抽象：
> > - 忽略机器人离地面的高度，不管它是否偏离垂直方向。
> > - 机器人只能面向四个方向。
> > - 世界其他地区被忽视：迷宫中其他机器人的可能性，环境对机器人运动影响程度。
> 
> - 行动抽象：
> > - 我们假定了所有位置都可以安全到达：机器人不会被卡住或损坏。
> > - 机器人可以随心所欲地移动，而无需重新进行充电。
> > - 简化的移动系统：向前移动一定距离，而不是控制每个单独的电机并观察传感器以检测碰撞。

# Exercise 4

> 你有一个 $9 \times 9$ 方格网格，每个方格都可以是红色或蓝色的。网格最初都是蓝色的，但你可以多次改变任何正方形的颜色。想象一下，网格被划分为 9 个 $3 \times 3$ 的子方格，你希望每个子方格都是一种颜色，但相邻的子方格是不同的颜色。
>
> 1. 用直截了当的方法表述这个问题。计算状态空间的大小。
> 2. 你只能给一个方格上色一次。重新表述，并计算状态空间的大小。广度优先搜索在这个问题上会比在 (1) 中执行得更快吗？那么迭代加深树搜索呢？
> 3. 给定目标，我们只需要考虑每个子方块都是统一着色的颜色。重新表述问题并计算状态空间的大小。
> 4. 这个问题有多少个解？
> 5. (2) 和 (3) 部分先后抽象了原问题 (1) ，你能否将问题 (3) 的解转化为问题 (2) 的解，并将问题 (2) 的解转化为问题 (1) 的解？

**参考解答：**

**（待补充）**

# Exercise 5

> 假设两个朋友住在地图上的不同城市，例如书中的罗马尼亚地图。在每个回合中，我们可以同时将每个朋友移动到地图上的邻近城市。从城市 $i$ 移动到相邻城市 $j$ 所需的时间等于城市之间的道路距离 $d(i, j)$，但在每个回合中，先到的朋友必须等到另一个人到达（并打电话给第一个人），才能开始下一个转弯。我们希望这两位朋友能尽快见面。
>
> 1. 写出这个搜索问题的详细公式。(你会发现在这里定义一些正式的符号很有帮助。)
> 2. 设 $D(i, j)$ 为城市 $i$ 和 $j$ 之间的直线距离，下列哪个启发式函数是可接受的？
>    - (a) $D(i, j)$；
>    - (b) $2 \cdot D (i, j)$；
>    - (c) $D(i, j) / 2$。
> 3. 是否存在完全连通的地图，但没有解决方案?
> 4. 是否存在所有解决方案都要求一个好友访问同一城市两次的地图?

**参考解答：**

1. **（待补充）**

   - 状态空间：状态是所有可能的的“城市对”$(i, j)$，地图不是状态空间。
   - 动作：$(i, j)$ 的后继节点都是 $(x, y)$ 对，使得有 $F_{临近}(x, i)$ 和 $F_{临近}(y, j)$。
   - 目标状态：找到某个 $i$ ，满足 $(i, i)$。
2. 在最好的情况下，两个朋友各自以相同的步长，直线相对走向对方，每一步可以减少两倍的时间，所以选择 (c)。
3. 存在。举例：一个只有两个节点的图，这两个朋友每次移动都会交换位置。**（还有其他情况，欢迎补充）**
4. **（待补充）**

# Exercise 7

> 使用资料上给出的“有效”增量公式考虑 $n$ 皇后问题。解释为什么状态空间至少有 $\sqrt[3]{n!}$ 个状态，并估计穷举探索可行的最大 $n$ 。
>
> *提示: 通过考虑皇后在任何列中可以攻击的最大方块数来推导分支因子的下界。*

**参考解答：**

**（待补充）**

# Exercise 8

[**原题链接**](https://aimacode.github.io/aima-exercises/search-exercises/ex_8/)

> 为以下每个问题给出一个完整的公式。选择一个精确到可以执行的公式。
>
> 1. 只使用四种颜色，你必须给一个平面地图上色，使相邻的两个区域没有相同的颜色。
> 2. 房间里有一只 3 英尺高的猴子，8 英尺高的天花板上挂着一些香蕉。他想要香蕉。房间里有两个可堆叠、可移动、可攀爬的 3 英尺高的板条箱。
> 3. 你有一个程序，当输入特定输入记录文件时输出消息“非法输入记录”。你知道每个记录的处理是独立于其他记录的。你想知道什么记录是非法的。
> 4. 你有三个罐子，分别是 12 加仑、8 加仑和 3 加仑，还有一个水龙头。你可以把罐子装满，也可以把它们从一个罐子倒到另一个罐子里，或者倒在地上。你需要精确地量出 1 加仑。

**参考解答：**

1. - 初始状态：所有区域都未着色。
   - 动作：给一个未着色区域上色。
   - 转移模型：每块区域的颜色。
   - 目标状态：所有区域都上色，而且没有相邻的两个区域是同一个颜色。
   - 动作代价：任务数。
2. - 初始状态：一个 8 英尺高的天花板；一些香蕉；3 英尺高的猴子；2 个 3英尺高的板条箱。
   - 动作：猴子移动与堆叠板条箱去靠近香蕉。
   - 转移模型：动作执行后板条箱的位置、堆叠状态。
   - 目标状态：猴子得到香蕉。
   - 动作代价：动作数。
3. **（待补充）**
   - 初始状态：所有输入记录文件。
   - 动作：
   - 转移模型：
   - 目标状态：输入特定输入记录文件时，输出“非法消息记录”。
   - 动作代价：程序运行次数。
4. - 初始状态： 罐子都是空的。
   - 动作：装满罐子；倒掉罐子里的水；把水从一个罐子倒到另一个罐子里。
   - 转移模型：每个罐子中的水量变化情况。
   - 目标状态：精确量得 1 加仑水。
   - 动作代价：动作数。

# Exercise 9

> 考虑在具有凸多边形障碍物的平面上寻找两点之间的最短路径的问题，如图所示。这是一个理想化的问题，机器人必须解决在拥挤的环境中导航。
>
> 1. 假设状态空间由平面上的所有位置 $(x,y)$ 组成。一共有多少种状态？通往目标的路径有多少条？
> 2. 简要解释为什么从一个多边形顶点到任何其他多边形顶点的最短路径必须由连接多边形的一些顶点的直线段组成。现在定义一个良好的状态空间。这个状态空间有多大？
> 3. 定义必要的函数来实现搜索问题，包括一个函数，该函数将顶点作为输入并返回一组向量，其中每个向量将当前顶点映射到可以在直线上到达的顶点之一。(不要忘记同一多边形上的邻居。)启发式函数使用直线距离。
> 4. 应用本章中的一个或多个算法来解决该领域的一系列问题，并评论它们的性能。

**参考答案：**
1. 如果考虑所有的点 $(x, y)$，那就会存无数个状态与无数条路径。

2. 我们把起点和终点看做是平面上的两个端点，那么最短路径就是连接它们两个端点的直线。但是现在由于平面上有多边形障碍物，那我们需要让路线尽可能少的偏离之前的直线，所以我们会选择起点到障碍物上的切点。由于障碍物是凸多边形，那切点就会在它的顶点上，以此类推，就会依次连接下一个障碍物的顶点。

3. **（待补充）**

4. **（待补充）**

# Exercise 10 (negative-g-exercise)

> On page, we said that we would not consider problems with negative path costs. In this exercise, we explore this decision in more depth.
> 1. Suppose that actions can have arbitrarily large negative costs; explain why this possibility would force any optimal algorithm to explore the entire state space.
> 2. Does it help if we insist that step costs must be greater than or equal to some negative constant $c$? Consider both trees and graphs.
> 3. Suppose that a set of actions forms a loop in the state space such that executing the set in some order results in no net change to the state. If all of these actions have negative cost, what does this imply about the optimal behavior for an agent in such an environment?
> 4. One can easily imagine actions with high negative cost, even in domains such as route finding. For example, some stretches of road might have such beautiful scenery as to far outweigh the normal costs in terms of time and fuel. Explain, in precise terms, within the context of state-space search, why humans do not drive around scenic loops indefinitely, and explain how to define the state space and actions for route finding so that artificial agents can also avoid looping.
> 5. Can you think of a real domain in which step costs are such as to cause looping?
>
> 在正文中，我们表示不会考虑负路径代价的问题。在本练习中，我们将更深入地探讨这一决定。

>1. 假设动作可能会产生任意大的负代价；解释为什么这种可能性会导致任何最佳算法探索整个状态空间。
>2. 如果我们坚持每步代价必须大于或等于某个负常数 $c$ ，这有帮助吗? 同时考虑树和图。
>3. 假设一组动作在状态空间中形成一个循环，即以某种顺序执行该集合不会导致状态发生实质性变化。如果所有这些动作都具有负成本，那么这意味着智能体在这样的环境中的最佳动作是什么？
>4. 人们可以很容易地想象出具有高负代价的行动，甚至在诸如路线查找之类的领域。例如，一些路段的风景可能非常美丽，以至于在时间和燃料方面远远超过了正常代价。准确地说，在搜索状态空间的背景下，解释为什么人类不会无限期地在风景优美的环路周围行驶，并解释如何定义状态空间和路线搜索的动作，以便人工智能也可以避免环路。
>5. 你能想到一个因为每步代价导致循环的真实情况吗？



**参考解答** ： 

>1. 因为存在负代价，不管怎么走，都可能带来任意小的代价（之前的代价 + 负代价）。因此，需要用尽所有可能的路径，以确保找到最佳路径。
>2. 在树的情况下是有帮助的。如果我们知道状态空间的最大深度，那么任何剩余 $d$ 级的步进代价最多为 $cd$，因此任何比 $cd$ 差的路径都可以被剪枝。  
在图的情况下，这并不起任何作用。因为图中可以存在循环，如果存在一个包含负代价的节点，总是可以利用这个节点不断降低当前最佳路径代价，形成另一个当前最佳路径代价。
>3. 智能体应该永远循环下去，因为它会降低代价函数的值（除非它能找到另一个更好的循环）。
>4. 风景优美的环路的价值在每次重新访问时都会降低；一个新奇的风景是一个很好的体验，但是在一个小时内第十次看到相同的风景是乏味的。为了适应这一点，我们必须扩展状态空间以包含一个记忆状态现在不仅由当前位置表示，而且由当前位置和一系列已经访问过的位置表示。访问新位置的代价是之前访问次数的（递增）函数。
>5. 吃垃圾食品和去上课。

# Exercise 15

> Does a finite state space always lead to a finite search tree? How about a finite state space that is a tree? Can you be more precise about what types of state spaces always lead to finite search trees? (Adapted from , 1996.)
>
> 有限状态空间总是导致有限搜索树吗？有限状态空间是树呢？你能更准确地说明什么类型的状态空间总是导致有限的搜索树吗？（改编自1996年。）


**参考解答** ： 


> 有限状态空间并不总是导致有限搜索树。例如，书中罗马尼亚城市地图示例中的状态空间是有限的：{In(Arad), In(Zerind),...,In(Eforie)}（包含 20 个州），但是使用 Go(City Name) 我们可以无限地通过任何循环路径，从而产生无限的搜索树。
> 在有限状态空间是树的情况下，根据定义不存在循环路径（循环），因此搜索树将是有限的。
> 任何不包含循环路径的合法结构也将具有有限搜索树。有限有向无环图 (DAG) 符合描述，因为根据定义其不包含循环（有向只是意味着从一个状态映射到另一个状态的动作不对称，因此不能在两个相邻状态之间无限循环）。

# Exercise 17

> 下列哪些是正确的，哪些是错误的？解释你的答案。
>
> 1. 深度优先搜索总是与具有可接受启发式的搜索至少扩展相同多的节点。
> 2. $h(n)=0$ 是 8 谜题的一个可接受的启发式。
> 3. $A^*$ 在机器人技术中没有用处，因为感知、状态和动作是连续的。
> 4. 即使允许零步长代价，广度优先搜索也是完备的。
> 5. 假设一只车可以在棋盘上沿直线(垂直或水平)移动任意数量的方块，但不能跳过其他方块。曼哈顿距离是用最小移动次数将车从方格 A 移动到方格 B 的一个可接受的启发式函数。

**参考答案：**

1. 错误。运气好的话， DFS 算法可以刚好扩展 $d$ 个节点就达到目的。$A^*$ 算法在很大程度上限制了保证找到最优解的任何图形搜索算法。

2. 正确。在代价是非负的情况下，$h(n)=0$ 是允许的一个启发式。

3. 错误。$A^*$ 算法也经常用于机器中，因为空间可以被离散化和骨架化。

4. 正确。对 BFS 影响更大的是深度而不是代价。

5. **（待补充）**

# Exercise 23

> 编写一个程序，将两个 Web 页面的 URL 作为输入，并找到从一个到另一个的链接路径。合适的搜索策略是什么？双向搜索会是个好主意吗？搜索引擎可以用来实现前驱函数（predecessor function）吗?

**参考解答：**
浏览网页时，我们只能通过访问网页来生成网页的后继。然后我们可以进行广度优先搜索，或者最佳优先搜索。为了让链接能够到达目标，启发式函数可以是起始页和目标页之间共有的单词数的函数。搜索引擎可以帮助我们得到完整的网页关系图，并可以向我们提供网页之间的链接，这样我们就可以进行双向搜索。


# Exercise 25 (search-special-case-exercise)

> Prove each of the following statements, or give a counterexample:
> 1. Breadth-first search is a special case of uniform-cost search.
> 2. Depth-first search is a special case of best-first tree search.
> 3. Uniform-cost search is a special case of A search.
>
> 证明以下各命题，或给出反例：
> 1.广度优先搜索是一致代价搜索的一个特例。
> 2.深度优先搜索是最佳优先树搜索的一个特例。
> 3.一致代价搜索是A搜索的一个特例。



**参考解答** ： 

>1. 当每步代价相等时，广度优先搜索就是一致代价搜索。
>2. 深度优先搜索是$f(n) = −depth(n)$的最佳优先搜索。
>3. A*搜索是 $g(n)+h(n)$，一致代价搜索$g(n)$。即一致代价搜索是$A^*$搜索在$h(n) = 0$时的情况。

# Exercise 27

>原题目：
>Trace the operation of A search applied to the problem of getting to Bucharest from Lugoj using the straight-line distance heuristic. That is, show the sequence of nodes that the algorithm will consider and the f, g, and h score for each node.

>题目翻译：
>使用直线距离启发式函数，追踪应用于从Lugoj到Bucharest的问题的$A^*$搜索操作。也就是说，显示算法将考虑的节点序列以及每个节点的f、g和h得分（在第三版习题中为A * 搜索）


>答案参考https://www.csie.ntu.edu.tw/~ai2007s/hw/hw02_s.pdf （注意：图片下等号左边为f， 右边第一个为g，第二个为h）


# Exercise 28
> Sometimes there is no good evaluation function for a problem but there is a good comparison method: a way to tell whether one node is better than another without assigning numerical values to either. Show that this is enough to do a best-first search. Is there an analog of A for this setting?\
**翻译:**\
有时，对于一个问题没有好的评价函数，但有一个好的比较方法：告诉一个节点是否比另一个节点好，而不给任何一个节点指定数值的方法。证明这足以做一个最佳优先搜索。在这种情况下是否有A的类似物？

# Exercise 29
> Devise a state space in which A using returns a suboptimal solution with an $h(n)$ function that is admissible but inconsistent.\
**翻译:**\
设计一个状态空间，其中A使用返回一个次优解的$h(n)$函数，是可接受的，但不一致。

# Exercise 30

>原题目：
>Accurate heuristics don’t necessarily reduce search time in the worst  case. Given any depth d, define a search problem with a goal node at depth d, and write a heuristic function such that $|h(n)−h\*(n)|≤O(logh\*(n))$ but A∗ expands all nodes of depth less than d.

>题目翻译：
>在最坏的情况下，精确的启发式并不一定会减少搜索时间。给定任意深度d，定义一个目标节点位于深度d的搜索问题，并编写一个启发函数，使得$|h(n)−h\*(n)|≤O(logh\*(n))$，但A*扩展所有深度小于d的节点。

# Exercise 31

>原题目：
>The **heuristic path algorithm** [Pohl:1977](https://aimacode.github.io/aima-exercises/search-exercises/#) is a best-first search in which the evaluation function is f(n)=(2−w)g(n)+wh(n). For what values of w is this complete? For what values is it optimal, assuming that ℎ is admissible? What kind of search does this perform for w=0, w=1, and w=2?

>题目翻译：
>启发式路径算法是最佳的第一搜索算法，其中评估函数为$f(n) = (2 - w)g(n) + wh(n)$.对于w的什么值，这是完全的？假设ℎ 是可接受的，对于哪些值是最优的？对于w=0、w=1和w=2，这将执行何种搜索？


>答案：
>1. 对于 $ 0 < w < 2 $ 时，是完全的
>2. $w = 0$得到 $f(n) = 2g(n)$ ，行为完全类似于均匀代价搜索
>3. $w = 1$得到 $ A^* $ 搜索
>4. $w = 2$得到 $ f(n) = 2h(n) $ ,是贪心最佳优先搜索

# Exercise 32

>原题目：
>Consider the unbounded version of the regular 2D grid shown in . The start state is at the origin, (0,0), and the goal state is at (x,y).
>1. What is the branching factor b in this state space?
>2. How many distinct states are there at depth k(for k>0)？
>3. What is the maximum number of nodes expanded by breadth-first tree search?
>4. What is the maximum number of nodes expanded by breadth-first graph search?
>5. Is h=|u−x|+|v−y| an admissible heuristic for a state at (u,v)? Explain.
>6. How many nodes are expanded by $A$ graph search using h?
>7. Does ℎ remain admissible if some links are removed?
>8. Does ℎ remain admissible if some links are added between nonadjacent states?



>题目翻译：
>考虑所给的常规二维网格的无界版本。开始状态位于原点（0， 0），目标状态位于（x, y）
>1. 这个状态空间中的分支因子b是什么？
>2. 在深度k处有多少不同的状态（对于k＞0)
>3. 广度优先树搜索扩展的最大节点数是多少？
>4. 广度优先图搜索扩展的最大节点数是多少？
>5. $h=|u−x|+|v−y|$是（u，v）处状态的可接受启发式吗？请做出解释
>6. 使用h的$A^*$图搜索可扩展多少个节点(原题目为A搜索，但找的资料上显示为$A^*$)
>7. ℎ 如果删除了某些链接，是否仍然可以接受
>8. ℎ 如果在非相邻状态之间添加了一些链接，是否仍然保持允许


>答案：
>1. 分支因子为4（每个位置的邻居数）
>2. $2k(2k+1) + 1$
>3. $4^{x + y}$
>4. $2(x + y)(x + y + 1)+1$
>5. 可以，这是曼哈顿距离度量方法，并且只能在网格上移动
>6. $x + y$
>7. 是的;删除链接可能会导致绕路，这需要更多的步骤，所以h是低估的。
>8. 不是的;非相邻状态的链接可以减少一些实际路径长度，从而导致不在处于低估状态。

# Exercise 33

>原题目：
>n vehicles occupy squares (1,1) through (n,1) (i.e., the bottom row) of an n×n grid. The vehicles must be moved to the top row but in reverse order; so the vehicle ithat starts in (i,1) must end up in (n−i+1,n). On each time step, every one of the n vehicles can move one square up, down, left, or right, or stay put; but if a vehicle stays put, one other adjacent vehicle (but not more than one) can hop over it. Two vehicles cannot occupy the same square.
>1. Calculate the size of the state space as a function of n.
>2. Calculate the branching factor as a function of n.
>3. Suppose that vehicle i is at (xi,yi); write a nontrivial admissible heuristic hi for the number of moves it will require to get to its goal location (n−i+1,n), assuming no other vehicles are on the grid.
>4. Which of the following heuristics are admissible for the problem of moving all n vehicles to their destinations? Explain.
> - $\sum^{n}_{i=1}{h_i}$
> - $max(h_1, ... , h_n)$
> - $min(h_1, ... , h_n)$



>题目翻译：
>n辆车占据n×n网格的正方形（1,1）到（n，1）（即，最下面的一行）。车辆必须移到最上面一排，但顺序相反；因此，在（i，1）开始的车辆必须在（n−i+1，n）结束。在每个时间步长上，n辆车中的每一辆都可以向上、向下、向左或向右移动一个正方形，或保持不变；但如果一辆车停在原地，另一辆相邻的车（但不超过一辆）可以跳过它。两辆车不能占用同一个广场。
>1. 根据n计算状态空间的大小
>2. 计算n作为函数的分支因子
>3. 假设车辆i位于（xi，yi)同时网格上没有其他车辆，为到达目标位置（n−i+1，n）所需的移动次数编写一个非平凡的可接受启发式hi（i为下标）
>4. 对于将所有n辆车移至目的地的问题，以下哪种启发式方法是可接受的？解释
> - $\sum^{n}_{i=1}{h_i}$
> - $max(h_1, ... , h_n)$
> - $min(h_1, ... , h_n)$

>答案：
>1. $n^{2n}$
>2. $5^n$
>3. 曼哈顿距离，即$|(n - i + 1) - x_i| + |n - y_i|$,这对一辆车来说是正确的
>4. 只有第三个是可以接受的。这个解释并不简单，因为它需要两个观察结果。首先，设给定解中的W是所有车辆在其关节轨迹上移动的总距离;也就是说，对于每辆车，将所采取的所有步骤的长度相加。我们有$W \geq \sum^{ }_{h_i }{h_i} \geq n * min{h_1, ... h_n}$.其次，我们每一步可以完成的总量≤n。(注意，对于每一辆跳跃2的车，另一辆车必须保持不变(移动0)，因此每一步的总功以n为界。)因此，完成所有工作至少需要n·min{h1，…，hn}/n = min{h1，…, hn}步骤。

# Exercise 34

>原题目：
>Consider the problem of moving k knights from k starting squares s1,…,sk to k goal squares g1,…,gk on an unbounded chessboard, subject to the rule that no two knights can land on the same square at the same time. Each action consists of moving *up to* k knights simultaneously. We would like to complete the maneuver in the smallest number of actions.
>1. What is the maximum branching factor in this state space, expressed as a function of k?
>2. Suppose hi is an admissible heuristic for the problem of moving knight i to goal gi by itself. Which of the following heuristics are admissible for the k-knight problem? Of those, which is the best?
> - $min(h_1, ... ,h_k)$
> - $max(h_1, ... , h_k)$
> - $\sum^{k}_{i=1}{h_i}$
>3. Repeat (b) for the case where you are allowed to move only one knight at a time.

>题目翻译：
>考虑在无界棋盘上将k个骑士从k个起始方块s1，…，sk移动到k个目标方块g1，…，gk的问题，前提是两个骑士不能同时降落在同一个方块上。每个动作包括同时移动最多k个骑士。我们希望以最少的动作达到目标。
>1. 这个状态空间中的最大分支因子是多少，表示为k的函数
>2. 假设hi是将骑士i单独移动到目标gi的问题的可接受启发式。以下哪种启发式方法可用于k骑士问题？其中，哪一个是最好的？
> - $min(h_1, ... ,h_k)$
> - $max(h_1, ... , h_k)$
> - $\sum^{k}_{i=1}{h_i}$
>3. 对于一次只能移动一名骑士的情况，重复（b）

>答案：
>1. 9k。对于k个骑士，除了完全不移动的可能性，我们还有8种移动中的一种;每个动作为每个骑士执行这9个选择中的一个(除非某些选择因落在同一个方格上而发生冲突)，所以有9k个动作。
>2. 1和2是可以的。如果$h_i$是精确的，那么2对于骑士可以落在同一个方格上的松弛问题是精确的。$h_i$是可容许的，因此不大于确切的值，因此2是可容许的。1不大于2，因此1是可接受的。3不可信。例如，如果每个$g_i$距离$s_i$只有一步，那么(iii)返回k，而最优解的代价是1。2决定了1，所以它必须一样好或者更好。所以2最好
>3. 

# Exercise 35
> We saw on page that the straight-line distance heuristic leads greedy best-first search astray on the problem of going from Iasi to Fagaras. However, the heuristic is perfect on the opposite problem: going from Fagaras to Iasi. Are there problems for which the heuristic is misleading in both directions?\
**翻译:**\
我们在页面上看到，从Iasi到Fagaras的问题上，将直线距离作为启发函数，会把贪心最佳优先搜索引入歧途。然而，从Fagaras到Iasi这个相反的问题上，启发式却是完美的。那么，是否存在这样的问题，启发式在两个方向上都有误导？

# Exercise 36
> Invent a heuristic function for the 8-puzzle that sometimes overestimates, and show how it can lead to a suboptimal solution on a particular problem. (You can use a computer to help if you want.) Prove that if $h$ never overestimates by more than $c$, A using $h$ returns a solution whose cost exceeds that of the optimal solution by no more than $c$.\
**翻译:**\
请为8 数码问题发明一个有时会高估的启发式函数，并说明它如何在一个特定问题上导致次优解(你可以使用计算机来帮助你)。证明：如果$h$从未高估过$c$，那么A使用&h&得到的解决方案的成本比最优解决方案的成本多出不超过$c$。

# Exercise 37
> Prove that if a heuristic is consistent, it must be admissible. Construct an admissible heuristic that is not consistent.\
**翻译:**\
证明：如果一个启发式函数是一致的，它一定是可接受的。构建一个不一致的可接受的启发式函数。

# Exercise 38(tsp-mst-exercise)
> The traveling salesperson problem (TSP) can be solved with the minimum-spanning-tree (MST) heuristic, which estimates the cost of completing a tour, given that a partial tour has already been constructed. The MST cost of a set of cities is the smallest sum of the link costs of any tree that connects all the cities.
> 1. Show how this heuristic can be derived from a relaxed version of the TSP.
> 2. Show that the MST heuristic dominates straight-line distance.
> 3. Write a problem generator for instances of the TSP where cities are represented by random points in the unit square.
> 4. Find an efficient algorithm in the literature for constructing the MST, and use it with A graph search to solve instances of the TSP.

> **翻译:**\
> 旅行商问题（TSP）可以用最小生成树（MST）启发式函数来求解，这种启发式函数在已经完成的一部分旅行基础上，预估完成一次旅行的成本。一组城市的MST成本是连接所有城市的树中的那个最小链接成本之和。
> 1. 说明如何从TSP的宽松版本中得到这种启发式函数。
> 2. 证明MST启发式函数在直线距离上占优势。
> 3. 为TSP的实例写一个问题生成器，其中城市由单位面积上的随机点代表。
>4. 在文献中找到一种构建MST的有效算法，并将其与A图搜索一起用于解决TSP的实例。


# Exercise 39(Gaschnig-h-exercise)
>On page 116, we defined the relaxation of the 8-puzzle in which a tile can move from square A to square B if B is blank. The exact solution of this problem defines **Gaschnig's heuristic** [Gaschnig:1979](https://www.semanticscholar.org/paper/Performance-measurement-and-analysis-of-certain-Gaschnig/2ce6e2ce79a59e253cc82efabcc73b1b190e91be). Explain why Gaschnig’s heuristic is at least as accurate as $h1$ (misplaced tiles), and show cases where it is more accurate than both $h1$ and $h2$ (Manhattan distance). Explain how to calculate Gaschnig’s heuristic efficiently.\
**翻译:**\
在第116页 ，我们定义了 8 数码问题的松弛问题：*如果方格 B 是空格，那么滑块可以从方格 A 移动到方格 B*。 这个问题的精确解定义了Gaschnig启发式函数（Gaschnig:1979）。\
请解释为什么Gaschnig的启发式至少和$h1$（错位的瓷砖）一样准确，并说明它比$h1$和$h2$（曼哈顿距离）都要准确的情况。如何有效地计算Gaschnig的启发式函数。
# Exercise 40
> We gave two simple heuristics for the 8-puzzle: Manhattan distance and misplaced tiles. Several heuristics in the literature purport to improve on this—see, for example, [Nilsson:1971](#), [Mostow+Prieditis:1989](https://www.ijcai.org/Proceedings/89-1/Papers/112.pdf), and [Hansson+al:1992](https://journals.lww.com/spinejournal/Abstract/1991/01000/A_Prospective_Study_of_Work_Perceptions_and.1.aspx). Test these claims by implementing the heuristics and comparing the performance of the resulting algorithms.\
> **翻译:**\
我们为 8 数码问题给出了两个简单的启发式函数方案：曼哈顿距离和错位的瓷砖。文献中的一些启发式函数算法声称在此基础上进行了改进，例如，Nilsson:1971, Mostow+Prieditis:1989, 和Hansson+al:1992。请实现这些启发式函数，比较这些算法的性能。
