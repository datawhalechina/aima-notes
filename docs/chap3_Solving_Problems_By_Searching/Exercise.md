# 第三章习题

# Exercise 1

> Explain why problem formulation must follow goal formulation.

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

# Exercise 28
> Sometimes there is no good evaluation function for a problem but there is a good comparison method: a way to tell whether one node is better than another without assigning numerical values to either. Show that this is enough to do a best-first search. Is there an analog of A for this setting?\
**翻译:**\
有时，对于一个问题没有好的评价函数，但有一个好的比较方法：告诉一个节点是否比另一个节点好，而不给任何一个节点指定数值的方法。证明这足以做一个最佳优先搜索。在这种情况下是否有A的类似物？

# Exercise 29
> Devise a state space in which A using returns a suboptimal solution with an $h(n)$ function that is admissible but inconsistent.\
**翻译:**\
设计一个状态空间，其中A使用返回一个次优解的$h(n)$函数，是可接受的，但不一致。

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
