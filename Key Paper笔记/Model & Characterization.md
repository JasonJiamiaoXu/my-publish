
# 三、模型分析
本文基于动态一般均衡框架，结合金融网络理论与宏观经济周期分析，围绕＂理论建模——动态传导机制——校准与实证——政策评估＂的脉络展开研究，重点探讨银行资产共同性在商业周期中的内生演化及其对系统性风险的影响。技术路线具体如下：

## 3.1 构建动态随机一般均衡模型

第一步：设定银行部门的双层结构（投资银行与非投资银行），引入银行间债务市场与风险项目投资选择。
（1）生产部门：每个岛屿与一个投资项目相关联。岛屿 $i$ 的项目（简称为项目 $i$ ）的生产需要生产部门投入资本 $k_{i}$ 和劳动力 $l_{i}$ 。采用 Cobb－Douglas 生产函数刻画生产部门的生产行为。
$$
\begin{equation*}
y_{i}=\mathrm{zk}_{\mathrm{i}}^{\eta} \mathrm{l}_{\mathrm{i}}^{1-\eta} \tag{1}
\end{equation*}
$$
其中，$\eta$ 表示资本份额，$z$ 是每期开始时实现的总体生产率。
生产部门在每期开始时的总体生产率对数根据 $\mathrm{AR}(1)$ 过程演变，
$$
\begin{equation*}
\log z^{\prime}=\varphi_{z} \log z+\sigma_{z} \epsilon^{\prime}, \quad \epsilon^{\prime} \sim \mathcal{N}(0,1) \tag{2}
\end{equation*}
$$
参数 $\varphi_{z}$ 和 $\sigma_{z}$ 分别衡量上一期对下一期的影响强度和冲击波动性。并同时会受到服从于正态分布的项目特定冲击 $x_{i}$ 的影响，而工资率和资本利率均由市场上的竞争过程所形成，设定劳动工资率 $w$ 。因此，对于岛屿 $i$ 的项目，厂家的目标函数可以描述如下：
$$
\begin{equation*}
\max _{l_{i}} y_{i}-w l_{i}=r k_{i} \tag{3}
\end{equation*}
$$
由完全竞争市场的均衡条件可以推出：
$$
\begin{equation*}
r=z \eta\left(\frac{(1-\eta) z}{w}\right)^{\frac{1-\eta}{\eta}} \tag{4}
\end{equation*}
$$

进一步，投资于任何项目的资本预计会以 $\delta$ 的速率贬值。此外，投资于项目 $i$ 的资本会受到项目特定的冲击 $\tilde{x}_{i}$ 。因此，投资 $k_{i}$ 于项目 $i$ 的总回报为
$$
\begin{equation*}
r k_{i}+(1-\delta) k_{i}-\widetilde{x}_{l} k_{i}=\left(R-\widetilde{x}_{l}\right) k_{i} \tag{5}
\end{equation*}
$$
$R=1+r-\delta$ ，需要综合考虑资本的边际产出和折旧率。项目特定的冲击在时间和空间上均为独立同分布的，本文假设每个 $\tilde{x}_{i}$ 来自正态分布，$\tilde{x}_{i} \sim \mathcal{N}\left(0, \sigma_{x}^{2}\right)$ 。


（2）银行部门：假设只存在两种银行，即非投资银行（一般商业银行）和投资银行。

其中投资银行可以直接接触风险投资项目，而非投资银行不能直接接触风险投资项目。设定这种差异的原因是为了在银行间引入异质性，形成银行间市场，在该市场中有如下设定：

a．投资银行对于自身岛屿项目 $i$ 有比较优势，因此可以无成本投资；但其同时可以分配资本在其他岛屿的项目上，且每单位投资需要花费 $f>0$ 的前期花费（如项目审核，项目监控费用等）。由于跨岛投资，投资银行 $i$ 持有一个投资组合 $\left\{\omega_{i j}\right\}_{j=1}^{N}, \sum_{j=1}^{N} \omega_{i j}=1$ ，其中 $\omega i j \geqslant 0$ 表示其管理资产 $a_{i}$ 中投资于项目 $j$ 的比例。

b．投资银行从非投资银行借款。同时因为每个岛屿对应一个项目，因此形成了市场的分割。本文规定银行间借贷限于岛屿内部，对应的利率 $\rho_{i}$ ，这样的规定反映了建立新的银行间联系是花费高昂的，会阻碍跨地借贷。

a）投资银行：通过多样化投资降低个体风险。
b）非投资银行：仅提供无风险存储技术，通过银行间市场向投资银行提供融资。
为了更加真实的描述投资市场，本文进一步引入违约机制和破产机制。其中，在违约情况下，资产损失比例为 $\theta$ 。

投资银行目标决策描述如下：银行 $i$ 在期初从代表性家庭筹集资产总量 $a_{0}$ 。此外它以利率 $\rho$ 在银行间市场借入 $a_{b}$ ，并选择投资组合 $\left\{\omega_{i j}\right\}_{j=1}^{N}$ 以最大化其预期收益。

假设项目受到冲击 $x=\left(x_{1}, \ldots, x_{N}\right)$ 。在期末，如果投资银行 $i$ 的投资组合收益低于其债务的面值，它将破产。同时，资金来源方（非投资银行）的盈亏平衡约束要求：放贷回报不低于无风险存储收益。破产的数学描述如下：
$$
\begin{equation*}
a\left[\sum_{j=1}^{N} \omega_{i j}\left(R-x_{j}\right)\right]-\rho a_{b}<0 \Leftrightarrow \sum_{j=1}^{N} x_{j} \omega_{i j}>R-\rho \mu \tag{6}
\end{equation*}
$$
其中 $a$ 是每家投资银行管理的总资产，$\mu=\frac{a_{b}}{a} \in[0,1]$ 是借入资产与总资产的比率。当投资银行 $i$ 的利润率（即利差 $R-\rho \mu$ ）低于其损失时，该银行将违约破产。

因此，投资银行的目标函数就是最大化预期收益，并会受到多个制约条件，分别分析在后：
a．目标函数：预期收益最大化，
$$
\begin{equation*}
\max _{\rho, \mu,\left\{\omega_{i j}\right\}_{j=1}^{N}} \frac{a_{o}}{1-\mu} E_{x}\left[\left(R-\rho \mu-\sum_{j=1}^{N} \widetilde{x}_{J} \omega_{i j}\right) I\left\{\sum_{j=1}^{N} \widetilde{x}_{J} \omega_{i j} \leq R-\rho \mu\right\}-f \sum_{j \neq i} \omega_{i j}\right] \tag{7}
\end{equation*}
$$
其中，$I$ 是示性函数，反映银行是否违约。
b．制约条件 1：投资组合权重必须总和为 1 且不能为负（不允许卖空）
$$
\begin{equation*}
\sum_{j=1}^{N} \omega_{i j}=1, \quad \omega_{i j} \geq 0 \forall j \in\{1, \ldots, N\} \tag{8}
\end{equation*}
$$
c．制约条件 2：投资银行 $i$ 受到其贷款人的盈亏平衡约束
项目的预期收益率需要至少高于无风险项目收益率（如国债），非投资银行（贷款人）才会选择将资金出借给投资银行。具体而言，假设在没有违约的情况下，每个贷款人都会收到承诺的回报 $\rho$ 。而如果违约，进行破产清算，贷款人会按借款比例 $\mu$ 清算剩余利润。因此，对于预期收益率的约束可以描述如下：
$$
\rho_{s} \leq E_{x}\left[\begin{array}{c}
\rho I\left\{\sum_{j=1}^{N} \widetilde{x}_{J} \omega_{i j} \leq R-\rho \mu\right\}  \tag{9}\\
+\frac{1}{\mu}\left(R-\sum_{j=1}^{N} \widetilde{x}_{J} \omega_{i j}-\theta\right) I\left\{\sum_{j=1}^{N} \widetilde{x}_{J} \omega_{i j}>R-\rho \mu\right\}
\end{array}\right]
$$
$\rho_{s}$ 是无风险收益率（如国债收益率）
d．制约条件 3：杠杆约束
上文假定了市场分割，每家投资银行最多只能获得其岛屿内的所有资产，同时对所有银行设定同质性假设（所有银行规模相同，各提供 1 单位资金），以确保模型对称性，避免过度复杂。因此杠杆率存在上限约束 $\bar{\mu}$ ，如下：
$$
\begin{equation*}
\mu \leq \bar{\mu}=\frac{M-1}{M} \tag{10}
\end{equation*}
$$
$M$ 是上文设定的单个岛屿上的银行总量，其中只有一家是投资银行。

可以用杠杆率表示投资银行的资本总量：$a=\frac{a_{0}}{1-\mu}, a_{\max }=\frac{a_{0}}{1-\bar{\mu}}$ ，进一步可以推出在均衡状态下，经济中所有资产的比例 $\frac{1-\bar{\mu}}{1-\mu}$ 投资于风险项目，剩余份额 $1-\frac{1-\bar{\mu}}{1-\mu}$ 则用于无风险的存储技术（如国债等）。

（3）家庭部门：本文通过 GHH 效用函数（Greenwood－Hercowitz－Huffman）其数学形式为：$U=\frac{1}{1-\psi}\left(c-\frac{1}{1+v} l^{1+v}\right)^{1-\psi}$ ，刻画家庭的跨期消费与劳动供给，并不会对劳动力供应产生财富效应，清晰地分离出替代效应。逆弗里斯劳动供给弹性 $v$ ，逆跨期替代弹性 $\psi$ ，时间贴现因子 $\beta$ 。

家庭长期存在，拥有所有资产并通过银行中介参与生产过程；家庭提供劳动力，消费，并决定自身下一期的资产数量。假设：代表性家庭在期初拥有资产 $a_{h h}$ 。总回报 $r_{h h}$定义为所有银行产生的平均回报，扣除多样化投资成本，折旧和可能的违约损失（见下文方程（12））。它还以劳动工资率 $w$ 提供劳动力 $l$ 。在期末，家庭进行消费并决定下一期的资产数量 $a_{h h}$ 。代表性家庭的目标函数如下：
$$
\begin{gather*}
V\left(a_{h h}\right)=\max _{a_{h h^{\prime}, l}^{\prime},} \frac{1}{1-\psi}\left(c-\frac{1}{1+v} l^{1+v}\right)^{1-\psi}+\beta E\left[V\left(a_{h h}^{\prime}\right)\right], \\
\text { s.t. } a_{h h}^{\prime}=r_{h h} a_{h h}+w l-c+\chi . \tag{11}
\end{gather*}
$$
预算约束中的 $\chi$ 代表投资银行为分散其投资组合而产生的总监控成本。

（4）均衡：本文在这个部分给予上述分部门刻画的模型特定的均衡条件。第一，对称均衡，即所有投资银行选择相同投资组合结构。第二，资本和劳动力市场各自出清。

模型的状态变量是资产存量 $A$ ，总生产率 $Z$ 和项目特定冲击 $x=\left(x_{1}, \ldots, x_{N}\right), \Omega=$ $(A, z, x)$ 。由于项目特定冲击在时间上是独立的，并发生在银行决策之后，故银行在决策的时候具体冲击的信息是未知的，而 $A$ 和 $Z$ 是已知的。因此，其相关状态变量集可以排除 $x$ 而描述为 $\Omega_{-x}=(A, z)$ 。本文关注对称均衡，在任何对称均衡中，投资组合权重为 $\omega_{i j}=\omega_{j i}, \omega_{i i}=\omega_{j j}=\alpha, \forall i, j$ ，因此， $1-\alpha$ 就代表了投资非本岛屿的比例，需要支付相应的监管费用 $f$ 。均衡由下面描述的一组数量和价格组成。
a．投资银行
$$
\mu=\mu\left(\Omega_{-x}\right), \rho=\rho\left(\Omega_{-x}\right),\left\{\omega_{i j}\right\}_{j=1}^{N}=\left\{\omega_{i j}\left(\Omega_{-x}\right)\right\}_{j=1}^{N} \text { 是其决策变量,在满足(8)-(10) }
$$
的条件下求解目标函数（7）。同时，投资银行对每个风险项目均匀投资，即每个项目获得
$\frac{1-\bar{\mu}}{1-\mu} \frac{A}{N}$ 单位的资金在劳动力市场上，通过求解方程（3）获得其劳动力需求 $l^{d}=l^{d}\left(\Omega_{-x}\right)$ 。

b．代表性家庭
代表性家庭决策中，消费，利率和下一期资产对冲击是已知的，其他未知。设定参数 $r_{h h}=r_{h h}(\Omega), w=w\left(\Omega_{-x}\right)$ ，以及 $\chi=\chi\left(\Omega_{-x}\right)$ 给定，$c\left(a_{h h}, \Omega\right), l\left(a_{h h}, \Omega_{-x}\right), a_{h h}^{\prime}\left(a_{h h}\right.$ ， $\Omega)$ 是其决策变量，求解目标函数（11）。其中，可以显然得到总监控成本 $\chi=A \frac{1-\bar{\mu}}{1-\mu} f(1-\alpha)$ 。

c．市场出清条件：
资本和劳动力市场各自出清，首先劳动力市场出清，$L\left(\Omega_{-x}\right)=N \cdot l^{d}\left(\Omega_{-x}\right)=$ $l\left(A, \Omega_{-x}\right)$ ，同时可以得到代表性家庭的投资回报率：

$$
\begin{equation*}
r_{h h}=\left(1-\frac{1-\bar{\mu}}{1-\mu}\right) \rho_{s}+\frac{1-\bar{\mu}}{1-\mu}\left[R-\frac{1}{N} \sum_{j=1}^{N} x_{j}-\theta \frac{N^{d}}{N}-f(1-\alpha)\right] \tag{12}
\end{equation*}
$$

其中 $R=1+r-\delta, r=r\left(\Omega_{-x}\right), R$ 由（4）给出，$N^{d}=N^{d}(\Omega)$ 是违约的投资银行数量，$N^{d}=\sum_{i=1}^{N} I\left\{\sum_{j=1}^{N} x_{j} \omega_{i j}>R-\rho \mu\right\}$ 。

代表性家庭假设同时意味着微观个体决策加总和宏观动态一致，因此 $\alpha_{h h}^{\prime}(A$ ， $\Omega)=A^{\prime}(\Omega)$ 。产品市场出清条件如下：
$$
\begin{align*}
A^{\prime}+ & C=\left(1-\frac{1-\bar{\mu}}{1-\mu}\right) \rho_{s} A+z\left(\frac{1-\bar{\mu}}{1-\mu} A\right)^{\eta} L^{1-\eta} \\
& +\frac{1-\bar{\mu}}{1-\mu} A\left[1-\delta-\frac{1}{N} \sum_{j=1}^{N} x_{j}-\theta \frac{N^{d}}{N}\right] \tag{13}
\end{align*}
$$
总需求端包括了 $A^{\prime}$（未来资产积累）和C（当期消费），反映了代表家庭将部分收入储蓄并转化为下一期的资本存量，其余部分作为对最终商品与服务的即期消耗；右端的总供给由三部分构成，分别对应经济中不同来源的价值创造与转移：分别是无风险收益，风险项目的产出和风险资本的净收益价值。

（5）系统性风险来源：投资银行的共同风险敞口导致多个机构同时受项目冲击影响，引发系统性违约。本文的模型强调共同敞口是系统性危机的主要机制。

本项目模型的逻辑架构如图 2 所示。模型包括每个岛屿内部的银行部门，生产部门与投资项目以及不属于单个岛屿的家庭部门与劳动力消费。在岛屿内部。投资银行通过贷款支持投资项目，成为联系不同岛屿投资活动的纽带；非投资银行则负责处理非投资

类资金业务，银行内部通过资金借贷形成协作。生产部门的生产成果经＂出清＂环节完成流通，既对接投资项目的生产需求，也为外部消费提供基础。投资项目通过直接投资获取资金，驱动生产活动，最终服务于岛屿 i 的经济运转。关于岛屿间联系，劳动力价值则通过＂出清＂机制，衔接生产部门的产出与家庭部门的消费需求。家庭部门则作为资金与劳动力的供给端，一方面向银行部门输送资金，参与投资活动；另一方面向生产部门提供劳动力，并通过＂劳动力消费＂环节完成经济循环。其资金与劳动力的流动不局限于单个岛屿，联动其他（N－1）个岛屿，形成跨区域经济网络。
<img src="Pasted image 20250406120412.png" alt="图2 动态一般均衡模型图" style="zoom:0.5; display: block; margin: 0 auto;" />

### D. 假设讨论







## 模型特征分析
接下来分析投资银行资产选择如何和代表性家庭决策动态互动，并最终产生系统性金融风险。
### A. 最优投资组合结构
**引理1：** 投资银行𝑖将资产份额$\omega_{i i}=\alpha \in\left[\frac{1}{N}, 1\right]$分配给项目 $i$，并将相等的较小份额资产分配给其他项目， $\omega_{i j}=\frac{1-\alpha}{1-N} \leq \omega_{i i}$ $\forall j \neq i$. 。
**直观理解：** 投资银行首先对于本岛屿内不需要支付监控费用的项目$i$分配最多份额$\alpha$，剩下$1-\alpha$单位资本，基于分散投资理念，平均投资给剩下$N-1$个项目。详细数学推导见下：

> [!Notes]+  **引理 1: 最优投资组合定理数学推导**
>
> **Proof：**
>
>> **首先标记符号：**
>> - 在（6）中得到受到冲击后银行破产的收益率临界值是 $\xi = R - \rho\mu$。
>> - 总冲击为 $\omega = \sum_{j=1}^N \omega_{ij}^2$。
>>
>> **其次证明概率论预备知识（截断正态分布的期望）：**
>>
>> 1. **截断概率**：  
>>    $E[I\{X \leq \xi\}] = \Phi\left(\frac{\xi}{\sigma_\omega}\right)$.  
>>    - **证明**：根据指示函数定义，  
>>      $$
>>      E[I\{X \leq \xi\}] = P(X \leq \xi) = \Phi\left(\frac{\xi}{\sigma_\omega}\right),
>>      $$
>>      其中 $\Phi(\cdot)$ 是标准正态分布的累积分布函数。
>>
>> 2. **截断期望**：  
>>    $E[X \cdot I\{X \leq \xi\}] = -\sigma_\omega \phi\left(\frac{\xi}{\sigma_\omega}\right).$  
>>    - **证明步骤 1**：变量标准化。令 $z = \frac{x}{\sigma_\omega}$，则 $x = \sigma_\omega z$，且积分区间变为 $z \in (-\infty, \frac{\xi}{\sigma_\omega}]$。代入后：
>>      $$
>>      E[X \cdot I\{X \leq \xi\}] = \sigma_\omega \int_{-\infty}^{\frac{\xi}{\sigma_\omega}} z \cdot \frac{1}{\sqrt{2\pi}} e^{-\frac{z^2}{2}} \, dz.
>>      $$
>>    - **步骤 2**：积分计算。注意到标准正态分布的密度函数为 $\phi(z) = \frac{1}{\sqrt{2\pi}} e^{-\frac{z^2}{2}}$，因此通过对右侧求导可以证明等式：
>>      $$
>>      \int_{-\infty}^a z \phi(z) \, dz = -\phi(a),
>>      $$
>>      其中 $\phi(a)$ 是标准正态密度函数在 $a$ 处的值。因此：
>>      $$
>>      E[X \cdot I\{X \leq \xi\}] = \sigma_\omega \cdot \left( -\phi\left(\frac{\xi}{\sigma_\omega}\right) \right) = -\sigma_\omega \phi\left(\frac{\xi}{\sigma_\omega}\right).
>>      $$
>
> 因为所有项目特定的冲击都是独立的，且 $\tilde{x}_{i} \sim \mathcal{N}\left(0, \sigma_{x}^{2}\right), \sum_{j=1}^{N} \tilde{x}_{j} \omega_{i j} \sim \mathcal{N}\left(0, \sigma_{x}^{2} \sum_{j=1}^{N} \omega_{i j}^{2}\right)$。在（7）和（9）中取期望，得到（A1）和（A2）详细推导见下：
>
> 1. **利润函数的期望（公式 (A1)）**：
>> $$
>> \pi = \frac{a_o}{1 - \mu} \left[ \xi \Phi \left( \frac{\xi}{\sqrt{\sigma_x^2 \sum_{j=1}^N \omega_{ij}^2}} \right) + \sqrt{\sigma_x^2 \sum_{j=1}^N \omega_{ij}^2} \Phi \left( \frac{\xi}{\sqrt{\sigma_x^2 \sum_{j=1}^N \omega_{ij}^2}} \right) - f(1 - \omega_{ii}) \right] \tag{A1}
>> $$
>> **推导过程：**
>> - （7）式中投资银行的利润函数为：
>>   $$
>>   \pi = \frac{a_0}{1 - \mu} E_x \left[ \left( R - \rho \mu - \sum_{j=1}^N \tilde{x}_j \omega_{ij} \right) I \left\{ \sum_{j=1}^N \tilde{x}_j \omega_{ij} \leq R - \rho \mu \right\} - f \sum_{j \neq i} \omega_{ij} \right].
>>   $$
>> - 使用截断正态分布的性质，可以得到：
>>   $$
>>   E \left[ (\xi - X) I\{X \leq \xi\} \right] = \xi \Phi\left(\frac{\xi}{\sigma_\omega}\right) - E[X I\{X \leq \xi\}] = \xi \Phi\left(\frac{\xi}{\sigma_\omega}\right) + \sigma_\omega \phi\left(\frac{\xi}{\sigma_\omega}\right).
>>   $$
>> - 最终得到（A1）。
>
> 2. **非投资银行约束条件的期望（公式 (A2)）**：
>> $$
>> 0 \leq h = \rho + \frac{1}{\mu} (\xi - \theta) \left( 1 - \Phi\left(\frac{\xi}{\sqrt{\sigma_{x}^{2} \sum_{j=1}^{N} \omega_{i j}^{2}}}\right) \right) - \frac{1}{\mu} \sqrt{\sigma_{x}^{2} \sum_{j=1}^{N} \omega_{i j}^{2}} \phi\left(\frac{\xi}{\sqrt{\sigma_{x}^{2} \sum_{j=1}^{N} \omega_{i j}^{2}}}\right) - \rho_s \tag{A2}
>> $$
>> **推导过程：**
>> - 非投资银行在银行间市场借出资金给投资银行，其预期回报必须至少等于无风险收益率 $\rho_s$。（9）式中原始约束为：
>>   $$
>>   \rho_s \leq E_x \left[ 
>>   \rho I \left\{ \sum_{j=1}^N \tilde{x}_j \omega_{ij} \leq R - \rho \mu \right\} 
>>   + \frac{1}{\mu} \left( R - \sum_{j=1}^N \tilde{x}_j \omega_{ij} - \theta \right) I \left\{ \sum_{j=1}^N \tilde{x}_j \omega_{ij} > R - \rho \mu \right\} 
>>   \right].
>>   $$
>> - 使用标记表示为：
>>   $$
>>   \rho_s \leq E[\rho I\{\omega \leq \xi\} + \frac{1}{\mu}(R-\rho-\theta)I\{\omega > \xi\}].
>>   $$
>> - 再使用截断正态分布结论 2 的条件期望形式，得到：
>>   $
>>   E \left[ R - \omega - \theta \mid \omega > \xi \right] = R - \theta - \sigma_\omega \cdot \frac{\phi\left(\frac{\xi}{\sigma_\omega}\right)}{1 - \Phi\left(\frac{\xi}{\sigma_\omega}\right)}.
>>   $
>> - 接下来进行一系列整理，约束变为：
>>   $
>>   \rho_s \leq \rho \Phi + \frac{1}{\mu} \left( (R - \theta)(1 - \Phi) - \sigma_\omega \phi \right).
>>   $
>> - 整理后得到：
>>   $
>>   0 \leq \rho \Phi + \frac{1}{\mu} (R - \theta)(1 - \Phi) - \frac{\sigma_\omega \phi}{\mu} - \rho_s.
>>   $
>> - 即：
>>   $
>>   0 \leq \rho + \frac{1}{\mu} (R - \rho \mu - \theta) (1 - \Phi) - \frac{\sigma_\omega \phi}{\mu} - \rho_s.
>>   $
>> - 由于 $\xi = R - \rho \mu$，最终得到（A2）。
>
>在得到了这两个期望之后，我们可以接下来还需要证明引理A.1来为引理A的最终证明做准备，
>
>引理 A.1：在均衡状态下，$\frac{\partial h}{\partial \rho}>0$ 且盈亏平衡约束（A2）成立。
>>证明：显然可以看出 $\frac{\partial \pi}{\partial \rho}<0$ 。采用反证法思路，假设 $\frac{\partial h}{\partial \rho} \leq 0$ 。那么，一家投资银行可以通过削减 $\rho$ 来增加其预期利润 $\pi$ ，而不违反盈亏平衡约束（A2）。这表明，投资银行还有降低借款利率的套利空间，这个均衡状态明显矛盾。因此，在均衡状态下 $\frac{\partial h}{\partial \rho}>0$。
>
>
> 有了以上引理，我们可以证明引理1：
>
> **证明**：根据引理 A.1，（A2）约束生效。将其代入（A1）。具体而言，先从约束条件反解出 $\rho \Phi$ 的表达式；再将 $\xi \phi$ 展开后代入 $\rho \Phi$，最后代入 A1。得到：
>
> $$
> \pi = \frac{a_{o}}{1-\mu} \left[ R - \rho_{s} \mu - \theta \left( 1 - \Phi\left(\frac{\xi}{\sqrt{\sigma_{x}^{2} \sum_{j=1}^{N} \omega_{i j}^{2}}} \right) \right) - f \left( 1 - \omega_{i i} \right) \right]
> $$
>
> 首先，对本岛屿的项目投资比例最大，$\omega_{i i} \geq \omega_{i j}, \forall j$。
>
> 同样使用反证法，假设不成立。那么，存在 $\exists k$ 使得 $\omega_{i k} > \omega_{i i}$。考虑另一个投资组合，其中 $\widehat{\omega}_{i i} = \omega_{i k}, \widehat{\omega}_{i k} = \omega_{i i}$，并且所有其他项目的权重相同。从分散投资的角度来看，这个投资组合是相同的，但成本更低，不满足唯一最优决策。因此，$\omega_{i i} \geq \omega_{i j}, \forall j$。
>
> 其次，让我们确定 $\omega_{i j} = \omega_{i k}, \forall j, k \neq i$。固定 $\omega_{i i}$ 并记 $\omega_{i} = \sqrt{\sigma_{x}^{2} \sum_{j=1}^{N} \omega_{i j}^{2}}$。通过上面利润函数求导，或者直观理解可以看出：
>
> $$
> \frac{\partial \pi}{\partial \omega_{i}} < 0, \quad \frac{\partial \pi}{\partial \rho} < 0, \quad \text{和} \quad \frac{\partial h}{\partial \omega_{i}} < 0.
> $$
>
> 此外，根据引理 A.1，$\frac{\partial h}{\partial \rho} > 0$。下面求解偏导关系：
>约束$h = 0$隐含了$\rho$与$\omega_{i}$的函数关系，即$\rho=\rho(\omega_{i})$。 
>**目标函数**：$\pi(\omega_{i},\rho(\omega_{i}))$（利润同时直接依赖$\omega_{i}$，并通过$\rho$间接依赖$\omega_{i}$）。
>利润对$\omega_{i}$的总导数： $\frac{d\pi}{d\omega_{i}} = \frac{\partial\pi}{\partial\omega_{i}} + \underbrace{\frac{\partial\pi}{\partial\rho} \cdot \frac{d\rho}{d\omega_{i}}}_{\text{直接效应}\ \ \ \ \text{间接效应}}$
>由$h(\rho,\omega_{i}) = 0$，全微分得： $\frac{\partial h}{\partial\rho}d\rho + \frac{\partial h}{\partial\omega_{i}}d\omega_{i} = 0 \Rightarrow \frac{d\rho}{d\omega_{i}} = -\frac{\partial h / \partial\omega_{i}}{\partial h / \partial\rho}$
>代入得到偏导数公式：
> $$
> \frac{d \pi}{d \omega_{i}} = \frac{\partial \pi}{\partial \omega_{i}} - \frac{\partial \pi}{\partial \rho} \frac{\partial h / \partial \omega_{i}}{\partial h / \partial \rho} < 0.
> $$
>
> 所以一家投资银行希望在任何给定的 $\mu$ 和 $\omega_{i i}$ 下最小化 $\omega_{i}$。显然，对于给定的 $\omega_{i i}, \omega_{i}$，当 $\omega_{i j} = \omega_{i k}, \forall j, k \neq i$ 时最小化。最优投资组合的形式为：
>
> $$
> \omega_{i i} = \alpha \geq \frac{1}{N} \geq \omega_{i j} = \frac{1-\alpha}{N-1}, \quad \forall j \neq i.
> $$

### B．投资组合重叠与系统性风险

从个体和系统的两个角度进行分析。一家投资银行内部化其预期违约损失已计入银行间利率。投资银行 $i$ 的个体违约概率为
$$
\begin{equation*}
p_{i}^{d}=\mathbb{P}\left\{\sum_{j=1}^{N} \tilde{x}_{j} \omega_{i j}>R-\rho \mu\right\}=1-\Phi\left(\frac{R-\rho \mu}{\sqrt{\sigma_{x}^{2} \sum_{j=1}^{N} \omega_{i j}^{2}}}\right) \tag{13}
\end{equation*}
$$
定义$P O(\alpha)=\frac{1-\alpha}{1-1 / N} \in[0,1]$ 为单个投资银行的资产重合度。

系统金融风险定义为所有投资银行同时违约的事件。根据每个项目的资产分配比例，当冲击满足条件：$$x_{i}^{\text {full }}(\alpha)=\alpha x_{i}+\frac{1-\alpha}{N-1} \sum_{j \neq i} x_{j}>R-\rho \mu ,\forall i$$ 这种情况就会发生。定义一个随机变量 $\tilde{x}_{\text {min }}^{\text {full }}=\min \left\{\tilde{x}_{1}^{\text {full }}, \ldots, \tilde{x}_{N}^{\text {full }}\right\}$ 。那么，系统性危机的概率为
$$
p_{\text {syst }}^{d}=\mathbb{P}\left(\tilde{x}_{\min }^{\text {full }}(\alpha)>R-\rho \mu\right)
$$
**引理 2 ：** 个体违约概率 $p_{i}^{d}$ 随投资组合重叠度 PO 的下降而下降，系统性违约概率 $p_{\mathrm{syst}}^{d}$ 随 PO 的上升而上升。两者 $p_{i}^{d}$ 和 $p_{\text {syst }}^{d}$ 都随利差 $\xi=R-\rho \mu$ 的下降而下降。这个引理是直观的。

在均衡状态下，影响违约概率的投资组合重叠度和利差都是内生设定的。下面，我将研究这些变量相对于总体状态变量变化的比较静态分析，即总资产量 $A$ 和总体生产率 $z$变化的影响 。我首先分析项目是有利润可图的并且投资银行在其区域内借入所有资金的情况，$\mu=\bar{\mu}$ 。

假设违约风险足够小。
**假设 1：** 违约风险足够小，$p_{i}^{d}<1-\Phi(\sqrt{2})$ 。

在假设 $1, p_{i}^{d}=p_{i}^{d}(\alpha, \xi)$ 下，$\alpha$ 是凸的。此外，这一假设意味着当投资银行的资产负债表变弱时，多样化变得更具吸引力。特别是，$\frac{\partial^{2} p_{i}^{d}}{\partial {\xi} \partial \alpha}<0$ ，其中 $\xi=R-\rho \mu$ ；利差的降低使得个体违约概率对 $\alpha$ 的变化更加敏感，即多样化。【】【附录】

**命题1：** 假设$\mu=\bar{\mu}$ 。那么比较静态性质为：投资组合重叠度 $P O(A, z)$ 随 $A$ 增加而增加，随 $z$ 增加而减少，而利差 $\xi(A, z)=R(A, z)-\rho(A, z) \bar{\mu}$ 随 $A$ 增加而减少，随 $z$ 增加而增加。

命题1确立了投资银行的选择如何受到总体状态变量变化的影响。值得注意的是，假设 1 对于这一命题是充分的，但不是必要的。












总体状态变量通过作用项目投资回报率 $R$ 影响银行间的资产分配。其中，总体生产率 $z$ 与 $R$ 正相关。此外，当 $\mu=\bar{\mu}$ 不变，由于边际利润递减，资产数量 $A$ 的增加会导致 $R$ 降低。从投资银行的角度来看，$R$ 是其总利润表达式$\pi$中的固定部分，在其他条件不变的情况下，$R$ 的下降会减少利差 $R-\rho \bar{\mu}$ 并增加其个体违约概率。非投资银行作为资金的出借方要求对这种额外风险进行补偿，借款利率 $\rho$ 会上升，为了降低贷款成本，投资银行更加积极地分散投资。

因此，$R$ 的变化通过两种方式影响个体和系统性违约概率。
- 首先，$R$ 的下降会缩小利差 $R-\rho \bar{\mu}$ ，并且根据引理 2 ，使得系统性和个体违约更有可能发生。
- 其次，$R-\rho \bar{\mu}$ 下降后分散投资的增加会导致投资组合重叠度$PO$增加，并使投资银行的共同风险敞口加大。
- 综合而言，分散投资防止了个体违约概率的急剧上升。然而，系统性危机则更有可能发生。推论1立即得出。

**推论1：** 假设$\mu=\bar{\mu}$ 。那么系统性违约概率 $p_{\text {syst }}^{d}(A, z)$ 随 $A$ 增加而增加，随 $z$ 增加而减少。个体违约概率 $p_{i}^{d}(A, z)$ 通常在 $A$ 和 $z$ 上非单调变化。【】

结合命题 1 和推论 1 表明，当资产总量 $A$ 较大但资产生产力 $z$ 较低时，系统性风险更有可能发生。在正常情况下，当 $A$ 和 $z$ 接近其平均水平时，只有较大的特定的项目的负向冲击才能导致所有投资银行违约。这种较大的负向冲击不太可能发生，这意味着在这些状态下系统性违约概率较低。然而，当 $A$ 较高且 $z$ 较低时，较小的项目特定冲击足以触发所有投资银行同时违约。

下面的推论 2 形式化表达了这一观点。特别是，存在一个阈值 $A^{*}=A^{*}(z, x)$ ，其中 $x=$ $\left(x_{1}, \ldots, x_{N}\right)$ 是已实现的项目特定冲击的向量，当且仅当资产总量超过该阈值时，系统性危机才会发生。显然，如果经济受到不利冲击（即 $z$ 较低且 $x$ 的元素的值较高），则阈值较低，这意味着在 $A$ 较低值时就会发生系统性危机。

**推论2：** 假设$\mu=\bar{\mu}$ 。那么，对于给定的 $z$ 和已实现的项目特定冲击向量 $x=$ $\left(x_{1}, \ldots, x_{N}\right)$ ，存在一个阈值 $A^{*}(z, x) \leq \infty$ ，使得系统性危机发生当且仅当 $A>A^{*}(z, x)$。此外，如果 $A^{*}(z, x)<\infty$ ，则 $A^{*}(z, x)$ 随 $z$ 增加而增加，随 $x_{i}, \forall i$ 减少而减少。当$A^{*}(z, x)=\infty$，意味着永远不会发生系统性风险。

![[PixPin_2025-04-10_17-00-19.png]]
<center>图 3</center>
> [!tip]
> 图3是校准模型中关于总资产量 $A$ 和总生产率 $z$ 的比较静态分析。校准过程在第三节中描述。蓝色实线是在 $\log z=0.0255$（高于平均值 0.80 个标准差）下获得的。红色虚线是在 $\log z=-0.0255$（低于平均值 0.80 个标准差）下获得的。灰色垂直线标记了约束条件 $\mu \leq \bar{\mu}$ 变得松弛的资产量。

图 3 总结了比较静态分析的结果。当 $\mu=\bar{\mu}$ ，投资于风险技术的资产比例为 $\frac{1-\bar{\mu}}{1-\mu}=1$（图 A ，线条的水平部分），变量对 $A$ 和 $z$ 变化的响应与命题 1 和推论 1描述的一致。当 $R$ 足够低时（图C右端），约束条件 $\mu \leq \bar{\mu}$ 不再有效，风险项目无生产力，不再投资风险项目，总资产被分配到无风险项目（国债等）中。 $A$ 的增加几乎不影响投资于风险技术的资产量，因此回报 $R$ 也几乎不变。违约概率，利差，银行间利率和投资组合重叠程度都趋于平缓。  值得注意的是，即使在 $\mu<\bar{\mu}$（高 $A$ ，低 $z$ ）状态下，投资组合重叠和系统性风险仍然很高（图B、D）。



### C．动态模型中的系统性风险

尽管银行间问题是静态的，但银行的最优选择是状态变量的函数，因此会随时间变化。本小节讨论了家庭的跨期资产积累决策与变动的总体生产率如何作用投资银行状态。并特别描述了经济如何从低系统性风险状态过渡到高系统性风险状态。

下面我们来详细描述这个过程：
![[PixPin_2025-04-10_17-17-56.png]]<center>图 4</center>
> [!tip]
> 图4：均衡时资产积累政策函数 $A^{\prime}(A, z, x)$ 。这些政策是通过求解校准模型获得的。求解方法在互联网附录第 IX 节中讨论（DSGE求解数值方法）。校准过程在第 III 节中描述。冲击值： $\log z_{a v}=0 ; \log z_{\text {boom }}=0.0537$（高于平均值1．69个标准差 $) ; x_{i g}=0$ 五个项目为 0.0339 ，两个项目为 1.36 个标准差；$x_{i b}=0.0339$ 七个项目。 $A^{*}\left(z_{a v}, x_{b}\right)$ 是推论 2 中定义的系统性危机阈值。

图4显示了两种总体生产率值 $z$ 下的均衡资产积累政策 $A^{\prime}(A, z, x)$ ，分别是长期平均值 $z_{a v}$ 和 $z_{\text {boom }}>z_{a v}$ ，以及两组项目特定冲击的实现值 $x_{g}<x_{b}$。（政策函数是通过求解下一节中描述的校准模型获得的）。

政策函数 $A^{\prime}$ 在 $A^{*}\left(z_{a v}, x_{b}\right)$ 处的不连续性与系统性危机相关。对于 $z=z_{a v}$ 和 $x=x_{b}$ （蓝色细线），如果 $A>A^{*}\left(z_{a v}, x_{b}\right)$ 则发生系统性违约，否则不发生（推论2描述的阈值）。

**信贷繁荣初期：** 如果 $A<A^{*}\left(z_{a v}, x_{b}\right)$ ，相同的项目特定冲击会导致相同的直接资本损失，但不会引发系统性危机，因此经济能够避免巨大的实际违约成本。考虑经济从点 $O$ 开始，这是 $z=z_{a v}$ 和 $x=x_{g}$ 的稳态（蓝色粗线）。在这一点上，资产总量相对较低，风险项目具有生产力。分散投资的激励还较小，投资银行的组合重叠相对较低，共同风险敞口较小，系统性风险不太可能发生。项目特定冲击的负向实现 $x=x_{b}$ 将经济带到 $B_{O}$ 。但这并不十分危险，因为金融系统避免了系统性危机和巨大的资产实际损失。

**危机触发阶段：** 如果 $A>A^{*}\left(z_{a v}, x_{b}\right), z=z_{a v}$ ，并且风险项目受到冲击 $x_{b}$ ，所有投资银行会同时违约，经济中所有资产的一部分 $\theta$ 将损失。如图，现在考虑经济处于点 $C$ 的情况。在这里，总生产率与 $O, z=z_{a v}$ 时相同。然而，资产数量显著增加， $A_{C}>A^{*}\left(z_{a v}, x_{b}\right)>A_{O}$ ，这导致回报率降低 $R$ ，投资银行的违约概率上升。投资银行通过更积极的分散化投资来应对。因此，投资组合的重叠程度增加，投资银行之间的共同风险敞口性也随之增加。因此，系统性危机的概率比 $O$ 时更高。相同的项目特定冲击 $x_{b}$ 在 $O$ 时对经济仅有轻微的负面影响，但在 $C$ 时则更具破坏性，使经济从 $C$ 跌至 $B_{C}$ 。


**风险累积阶段：** 那么经济如何从 $O$ 移动到 $C$ ？总生产率的正向冲击（在图4中，$z$ 从 $z_{a v}$ 增加到橙色线 $z_{\text {boom }}$ ）推高了风险项目的回报率。代表性家庭开始积累更多资产，这导致了信贷扩张。然而，由于$z$ 的均值回归特性，总生产率在繁荣状态几个时期后回到 $z_{a v}$ 。经济到达 $C$ ，

本节的结果表明，在这种经济中，大规模的金融危机往往发生在由暂时性生产率繁荣驱动的信贷扩张期之后。在下一节中，我对模型进行校准，并表明这一预测在校准模型中成立。

