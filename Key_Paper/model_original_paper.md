Capital invested in any project is expected to depreciate at the rate $\delta$ due to usual wear and tear. In addition, capital invested in project $i$ is subject to a project-specific shock $\tilde{x}_{i}$, which can be thought of as a shock to the depreciation rate or a capital quality shock. Therefore, the total payoff from investing $k_{i}$ in project $i$ is

$$
\begin{equation*}
r k_{i}+(1-\delta) k_{i}-\tilde{x}_{i} k_{i}=\left(R-\tilde{x}_{i}\right) k_{i}, \tag{5}
\end{equation*}
$$

where $R=1+r-\delta$. Project-specific shocks are realized after capital investors make their investment decisions. Their realizations are independent across islands and time. I assume that each $\tilde{x}_{i}$ comes from a normal distribution, $\tilde{x}_{i} \sim$ $\mathcal{N}\left(0, \sigma_{x}^{2}\right)$. The normality assumption is important to keep the portfolio choice of banks tractable. ${ }^{9}$ In what follows, the cumulative distribution function of the standard normal distribution is denoted by $\Phi(\cdot)$ and the probability density function is denoted by $\phi(\cdot)$.

## A.2. Interbank Market and Diversification

Although the storage technology is available to all banks, only investing banks have access to the risky projects. In particular, an investing bank from island $i$ has expertise in project $i$ and can invest in it at no cost. It can also allocate some of its assets to the remaining projects at an upfront proportional cost $f>0$ per unit of investment, which includes any monitoring expenses. Noninvesting banks cannot access the risky technology directly. This heterogeneity gives rise to the intraperiod interbank market in which investing banks borrow from noninvesting banks.

I assume that interbank borrowing happens within islands. This assumption implies that the economy features segmented interbank markets, where the interbank borrowing rate on island $i$ is $\rho_{i}$. This setup captures the idea that establishing new interbank links might be costly with these costs preventing cross-island borrowing. An island in the model includes banks with established relationships that can contact each other at no cost.

Because investing banks invest in the risky technology, interbank debt is subject to defaults that are associated with deadweight losses. In particular, a fraction $\theta>0$ of borrower assets is lost in the case of its default. This is rationally priced in the interbank borrowing rates. Therefore, despite their risk-neutrality and positive monitoring costs, investing banks are willing to invest in projects of other islands to diversify their individual risks and reduce the probability of costly default. As a result of cross-island investments, an investing bank $i$ holds a portfolio $\left\{\omega_{i j}\right\}_{j=1}^{N}, \sum_{j=1}^{N} \omega_{i j}=1$, where $\omega_{i j} \geq 0$ represents the fraction of its assets under management $a_{i}$ invested in project $j$. Here, $a_{i}$ consists of assets raised directly from the household and borrowed in the interbank market. The upfront cost of portfolio formation is $f a_{i} \sum_{j \neq i} \omega_{i j}$.

[^0]Portfolio weights $\left\{\omega_{i j}\right\}_{i, j=1}^{N}$ characterize commonalities in risk exposures across investing banks. In particular, a large $\omega_{i j}$ implies that investing bank $i$ is strongly exposed to project $j$ 's shocks. As long as $\omega_{i j}>0 \forall i$, a shock to project $j$ affects all investing banks and can potentially lead to simultaneous defaults of many institutions. Importantly, defaults do not trigger cascading losses among investing banks because they do not hold assets directly related to the payoffs of other investing banks. I provide further discussion of the structure of the financial system at the end of this section.

## A.3. Problem of an Investing Bank

The problem of investing bank $i$ can now be formulated. Because the model is symmetric, island-specific indices are omitted where possible. Bank $i$ starts a period with assets $a_{o}$ that are raised from the representative household. Additionally, it borrows $a_{b}$ at the rate $\rho$ in the interbank market and chooses an investment portfolio $\left\{\omega_{i j}\right\}_{j=1}^{N}$ to maximize its expected payoff subject to a break-even constraint of its lenders.
Suppose that projects are hit by shocks $x=\left(x_{1}, \ldots, x_{N}\right)$. At the end of the period, investing bank $i$ is insolvent if its portfolio payoff is below the face value of its debt,

$$
\begin{equation*}
a\left[\sum_{j=1}^{N} \omega_{i j}\left(R-x_{j}\right)\right]-\rho a_{b}<0 \Leftrightarrow \sum_{j=1}^{N} x_{j} \omega_{i j}>R-\rho \mu, \tag{6}
\end{equation*}
$$

where $a=a_{o}+a_{b}$ is the total assets under management of each investing bank and $\mu=\frac{a_{b}}{a} \in[0,1]$ is the ratio of borrowed assets to total assets. Inequality (6) implies that investing bank $i$ defaults when its profit margin, captured by the spread $R-\rho \mu$, is below the overall loss of its portfolio due to projectspecific shocks.

Investing bank $i$ maximizes the expected payoff of its portfolio under limited liability net of diversification costs. ${ }^{10}$ It is also subject to several constraints. I first write the objective function in (7). I then show the constraints in (8)-(10). The objective function is

$$
\begin{equation*}
\max _{\rho, \mu,\left\{\omega_{i j} j_{j=1}^{N}\right.} \underbrace{\frac{a_{o}}{1-\mu}}_{=a} \mathbb{E}_{x}\left[\left(R-\rho \mu-\sum_{j=1}^{N} \tilde{x}_{j} \omega_{i j}\right) \mathbb{I}\left\{\sum_{j=1}^{N} \tilde{x}_{j} \omega_{i j} \leq R-\rho \mu\right\}-f \sum_{j \neq i} \omega_{i j}\right], \tag{7}
\end{equation*}
$$

where $\mathbb{E}_{x}[\cdot]$ denotes expectation with respect to project-specific shocks. This expectation can be computed analytically under normality of projectspecific shocks.

[^1]When solving (7), investing bank $i$ is subject to several constraints. First, portfolio weights have to sum to one and cannot be negative (no short-selling),

$$
\begin{equation*}
\sum_{j=1}^{N} \omega_{i j}=1, \quad \omega_{i j} \geq 0 \forall j \in\{1, \ldots, N\} \tag{8}
\end{equation*}
$$

Second, investing bank $i$ is subject to the break-even constraint of its lenders,

$$
\begin{equation*}
\rho_{s} \leq \mathbb{E}_{x}\left[\rho \mathbb{I}\left\{\sum_{j=1}^{N} \tilde{x}_{j} \omega_{i j} \leq R-\rho \mu\right\}+\frac{1}{\mu}\left(R-\sum_{j=1}^{N} \tilde{x}_{j} \omega_{i j}-\theta\right) \mathbb{I}\left\{\sum_{j=1}^{N} \tilde{x}_{j} \omega_{i j}>R-\rho \mu\right\}\right] . \tag{9}
\end{equation*}
$$

In the case of no default, each lender receives a promised return $\rho$. In the case of default, lenders split their borrower's portfolio equally. Recall that $\theta$ denotes the fraction of assets managed by a failed investing bank that is lost in default. Lending to investing banks should be at least as attractive as investing in the outside option available to noninvesting banks, that is, the expected return from lending should be greater than or equal to the storage return $\rho_{s}$.

Finally, each investing bank can operate at most all assets within its island,

$$
\begin{equation*}
\mu \leq \bar{\mu}=\frac{M-1}{M} . \tag{10}
\end{equation*}
$$

In equilibrium, the fraction $\frac{1-\bar{\mu}}{1-\mu}$ of all assets in the economy is invested in the risky projects and the remaining share $1-\frac{1-\bar{\mu}}{1-\mu}$ goes to the riskless storage technology. Throughout the paper, the risky projects are assumed to be sufficiently productive such that investing banks always want to borrow, $\mu>0$. This is indeed the case in the calibrated model.

To summarize the description of the banking sector, Figure 2 shows its structure and gives the timing of the intraperiod events.

## B. Representative Household

The representative household starts a period with assets $\alpha_{h h}$. Renting these assets to the financial sector generates total return $r_{h h}$, defined as the average return generated by all banks, net of diversification costs, depreciation, and default losses if any (see equation (12) below). It also supplies labor $l$ at wage $w$. At the end of a period, the household consumes and decides on the amount of assets in the next period $\alpha_{h h}^{\prime}$. The household solves

$$
\begin{align*}
& V\left(a_{h h}\right)=\max _{a_{h h}^{\prime}, c, l} \frac{1}{1-\psi}\left(c-\frac{1}{1+v} l^{1+v}\right)^{1-\psi}+\beta \mathbb{E}\left[V\left(a_{h h}^{\prime}\right)\right],  \tag{11}\\
& \text { s.t. } a_{h h}^{\prime}=r_{h h} a_{h h}+w l-c+\chi .
\end{align*}
$$

The household has GHH preferences (Greenwood, Hercowitz, and Huffman (1988)) over consumption and labor with the inverse Frisch labor supply
![](https://cdn.mathpix.com/cropped/2025_03_17_6b24cbbaa17d6d4c0aa8g-04.jpg?height=501&width=424&top_left_y=238&top_left_x=198)

Panel B. Ex-post heterogeneity; interbank lending

Panel D. Project-specific shocks are realized
![](https://cdn.mathpix.com/cropped/2025_03_17_6b24cbbaa17d6d4c0aa8g-04.jpg?height=414&width=413&top_left_y=882&top_left_x=194)

Panel E. Interbank debts are repaid; defaults may happen
![](https://cdn.mathpix.com/cropped/2025_03_17_6b24cbbaa17d6d4c0aa8g-04.jpg?height=438&width=438&top_left_y=867&top_left_x=626)

Panel F. Household receives the banking sector's proceeds
![](https://cdn.mathpix.com/cropped/2025_03_17_6b24cbbaa17d6d4c0aa8g-04.jpg?height=435&width=401&top_left_y=869&top_left_x=1064)

| Island | Bank |
| :--- | :--- |
| Investing bank | Shocked investing bank |
| Exposed investing bank |  |

Figure 2. Economy's structure and intraperiod timing. (Color figure can be viewed at wileyonlinelibrary.com)
elasticity $\nu$, the inverse elasticity of intertemporal substitution $\psi$, and the time-discounting factor $\beta .{ }^{11}$ The term $\chi$ in the budget constraint represents the total monitoring costs incurred by investing banks to diversify their portfolios. In the baseline model, I assume that diversification costs are not deadweight losses. Internet Appendix Section VIII compares the baseline

[^2]model to the model in which diversification costs are real and are not rebated to the household. The rebate amount $\chi$, as well as the prices $r_{h h}$ and $w$, are functions of the aggregate state variables (to be specified below) and thus are taken by the household as given.

## C. Equilibrium

The model's state variables are the stock of assets $A$, aggregate productivity $z$, and project-specific shocks $x=\left(x_{1}, \ldots, x_{N}\right), \Omega=(A, z, x)$. Because projectspecific shocks are independent over time and are realized after banks have made their choices, a relevant set of state variables for banks is $\Omega_{-x}=(A, z)$. I focus on symmetric equilibria. In any symmetric equilibrium, portfolio weights are $\omega_{i j}=\omega_{j i}, \omega_{i i}=\omega_{j j}=\alpha, \forall i, j$. Under GHH preferences, there is no wealth effect on the labor supply, so wage does not depend on $x$. A decentralized recursive equilibrium consists of a set of quantities and prices described below.

Investing banks

- $\mu=\mu\left(\Omega_{-x}\right), \rho=\rho\left(\Omega_{-x}\right)$, and $\left\{\omega_{i j}\right\}_{j=1}^{N}=\left\{\omega_{i j}\left(\Omega_{-x}\right)\right\}_{j=1}^{N}$ solve (7) subject to (8)-(10).
- Each project receives $\frac{1-\bar{\mu}}{1-\mu} \frac{A}{N}$ units of capital from investing banks and hires $l^{d}=l^{d}\left(\Omega_{-x}\right)$ units of labor, where $l^{d}$ solves (3).


## Representative household

- $c\left(a_{h h}, \Omega\right), l\left(a_{h h}, \Omega_{-x}\right)$, and $\alpha_{h h}^{\prime}\left(a_{h h}, \Omega\right)$ solve (11). The household takes $r_{h h}=$ $r_{h h}(\Omega), w=w\left(\Omega_{-x}\right)$, and $\chi=\chi\left(\Omega_{-x}\right)$ as given, where $\chi=A \frac{1-\bar{\mu}}{1-\mu} f(1-\alpha)$.


## Market clearing

- Wage $w$ clears the labor market, $L\left(\Omega_{-x}\right)=N \cdot l^{d}\left(\Omega_{-x}\right)=l\left(A, \Omega_{-x}\right)$.
- The return on the household's assets is

$$
\begin{equation*}
r_{h h}=\left(1-\frac{1-\bar{\mu}}{1-\mu}\right) \rho_{s}+\frac{1-\bar{\mu}}{1-\mu}\left[R-\frac{1}{N} \sum_{j=1}^{N} x_{j}-\theta \frac{N^{d}}{N}-f(1-\alpha)\right], \tag{12}
\end{equation*}
$$

where $R=1+r-\delta, r=r\left(\Omega_{-x}\right)$ is given by (4), and $N^{d}=N^{d}(\Omega)$ is the number of investing banks in default, $N^{d}=\sum_{i=1}^{N} \mathbb{I}\left\{\sum_{j=1}^{N} x_{j} \omega_{i j}>R-\rho \mu\right\}$.

- Individual decisions are consistent with the aggregate dynamics, $\alpha_{h h}^{\prime}(A, \Omega)=A^{\prime}(\Omega)$.
- The goods market clears,

$$
A^{\prime}+C=\left(1-\frac{1-\bar{\mu}}{1-\mu}\right) \rho_{s} A+z\left(\frac{1-\bar{\mu}}{1-\mu} A\right)^{\eta} L^{1-\eta}+\frac{1-\bar{\mu}}{1-\mu} A\left[1-\delta-\frac{1}{N} \sum_{j=1}^{N} x_{j}-\theta \frac{N^{d}}{N}\right] .
$$

## D. Discussion of Assumptions

## D.1. Structure of the Financial System

The financial system in the model is two-tiered. Noninvesting banks do not have direct access to the efficient production technology and lend their funds to investing banks. Investing banks then form diversified asset portfolios by investing in multiple projects. This is akin to a core-periphery structure of real-life financial systems (e.g., Boss et al. (2004), Craig and von Peter (2014), Craig and Ma (2022)).
The assumption confining interbank borrowing within islands is not important for the results. Crucially, costly defaults happen when investing banks' payoffs drop below an insolvency threshold. Therefore, it is the structure of investing banks' asset portfolios that affects expected default losses and the interbank borrowing rate. The portfolio structure of noninvesting banks is irrelevant for expected default losses, so I simply assume that each noninvesting bank lends to one borrower.

The main role of noninvesting banks is to provide funds to investing banks in the form of risky debt. Modern financial institutions are known to be financed to a large extent by debt. Moreover, funding through risky debt, especially short-term risky debt, was a crucial source of financial fragility during the crisis of 2007-2008 (Brunnermeier (2009)). The model is agnostic, however, about why debt arises as a source of funding in the first place. One possible reason is costly state verification (Townsend (1979)). When at least part of investing banks' funding comes from risky debt, banks have incentives to diversify to reduce their borrowing costs. Resulting asset commonality makes investing banks subject to similar shocks and gives rise to systemic risk. The source of such funding is of less importance. In particular, it can also come directly from households in the form of unsecured deposits.

## D.2. Common Risk Exposures and Systemic Risk

In the paper, investing banks hold overlapping asset portfolios. Asset commonality might arise both as a result of contractual links (e.g., when several banks initiate syndicated loans or participate in asset swaps) and in the absence of direct contacts (e.g., due to securitization or lending to similar firms). Systemic crises happen when many institutions have similar exposures to one or several badly performing underlying projects. Investing banks do not hold any securities directly related to payoffs of other intermediaries, for example, their debt or equity. As a result, defaults of investing banks do not cause default cascades-the domino effect-among other investing banks. Bankruptcy losses propagate from investing to noninvesting banks only within islands.
As discussed in the review paper of Cabrales, Gale, and Gottardi (2016), the systems in which financial institutions have strong common risk exposures or are directly exposed to one another's defaults are susceptible to simultaneous failures of many institutions. Therefore, incorporating the domino effect into my setting is likely to make the financial system even more vulnerable
to systemic collapse. Evidence on whether the domino effect is an important contributor to systemic risk is mixed (see Upper (2011) for a survey). Comparing relative strengths of the domino and the common exposures mechanisms in the Austrian banking system, Elsinger, Lehar, and Summer (2006) find that the latter is a dominant source of systemic risk. A crucial role of common exposures for systemic crises is also emphasized by Borio (2003).

## II. Characterization

This section outlines how banks' portfolio choices shape systemic risk, and how banks' decisions interact with the household's dynamic choices.

## A. Optimal Portfolio Structure

I start by establishing the following intuitive lemma that describes the structure of investing banks' portfolios.

Lemma 1: Investing bank $i$ allocates share $\omega_{i i}=\alpha \in\left[\frac{1}{N}, 1\right]$ of assets to project $i$ and allocates equal smaller shares of assets to other projects, $\omega_{i j}=\frac{1-\alpha}{1-N} \leq \omega_{i i}$ $\forall j \neq i$.

Proof: See the Appendix.
An investing bank internalizes that its expected default losses are priced in the interbank rate. The individual default probability of investing bank $i$ is

$$
\begin{equation*}
p_{i}^{d}=\mathbb{P}\left\{\sum_{j=1}^{N} \tilde{x}_{j} \omega_{i j}>R-\rho \mu\right\}=1-\Phi\left(\frac{R-\rho \mu}{\sqrt{\sigma_{x}^{2} \sum_{j=1}^{N} \omega_{i j}^{2}}}\right) . \tag{13}
\end{equation*}
$$

Because $\sum_{j=1}^{N} \omega_{i j}^{2}$ is convex, the individual default probability can be reduced through diversification, that is, $p_{i}^{d}$ is minimized when a portfolio is evenly exposed to the underlying shocks. At the same time, for investing bank $i$, allocating resources toward all but project $i$ is subject to equal nonnegative costs. Hence, the fraction of assets invested in project $i$ is larger than the fraction invested in all remaining projects, $\omega_{i i}=\alpha \geq \omega_{i j}=\frac{1-\alpha}{N-1} \forall j \neq i$.

I define the degree of portfolio overlap among investing banks as $P O(\alpha)=$ $\frac{1-\alpha}{1-1 / N} \in[0,1]$. If $\alpha$ is close to one, investing banks invest primarily in projects of their islands and thus portfolio overlap is close to zero. Investing banks fail predominantly in isolation, when projects of their islands are directly hit by adverse shocks. In contrast, when $\alpha$ approaches its minimum value of $\frac{1}{N}$, banks' investments are evenly spread across the risky projects and portfolio overlap is close to one. Shocks to individual projects affect all institutions similarly, and simultaneous defaults of many banks are more likely ceteris paribus. In what follows, I assume that the diversification cost is not prohibitively large and so $\alpha<1$.

## B. Portfolio Overlap and Systemic Risk

While diversification helps individual institutions protect themselves against costly defaults, it also increases the probability of a systemic collapse. In this section, I define a systemic crisis as an event that occurs when all investing banks default simultaneously. This happens when shock realizations are such that $x_{i}^{f u l l}(\alpha)=\alpha x_{i}+\frac{1-\alpha}{N-1} \sum_{j \neq i} x_{j}>R-\rho \mu \forall i$. Define a random variable $\tilde{x}_{\text {min }}^{\text {full }}=\min \left\{\tilde{x}_{1}^{\text {full }}, \ldots, \tilde{x}_{N}^{\text {full }}\right\}$. Then, the probability of a systemic crisis is

$$
p_{\text {syst }}^{d}=\mathbb{P}\left(\tilde{x}_{\text {min }}^{\text {full }}(\alpha)>R-\rho \mu\right) .
$$

Clearly, the probability of a systemic crisis is high when the investing banks' profit margin $R-\rho \mu$ is narrow. Furthermore, it is high when portfolio overlap is strong and banks have similar risk exposures. This is because for any realization of project-specific shocks, $x_{\text {min }}^{\text {full }}$ decreases in $\alpha$ and thus increases in $P O$. Intuitively, when $\alpha$ is low, an investing bank whose project in which it specializes receives the most plausible shock (i.e., a shock with the lowest $x_{i}$ ) is weakly exposed to this shock. Lemma 2 immediately follows.
Lemma 2: Individual default probability $p_{i}^{d}$ declines in portfolio overlap PO and systemic default probability $p_{\text {syst }}^{d}$ increases in PO. Both $p_{i}^{d}$ and $p_{\text {syst }}^{d} d e-$ crease in spread $\xi=R-\rho \mu$.

In equilibrium, the variables affecting default probabilities-portfolio overlap and spread-are set endogenously. Below, I investigate comparative statics of these variables with respect to changes in the aggregate state variables, that is, total asset amount $A$ and aggregate productivity $z$. I start by analyzing the case in which the underlying projects are sufficiently productive and investing banks borrow all funds within their islands, $\mu=\bar{\mu}$.

In what follows, I assume that default risk is sufficiently small.
ASSUMPTION 1: Default risk is sufficiently small, $p_{i}^{d}<1-\Phi(\sqrt{2})$.
Under Assumption 1, $p_{i}^{d}=p_{i}^{d}(\alpha, \xi)$ is convex in $\alpha$. If this assumption does not hold, investing banks' objective function might be nonconcave in $\alpha$. Furthermore, this assumption implies that diversification becomes more attractive when investing banks' balance sheets weaken. In particular, $\frac{\partial^{2} p_{i}^{d}}{\partial \xi \partial \alpha}<0$, where $\xi=R-\rho \mu$; a reduction in the spread makes the individual default probability more sensitive to changes in $\alpha$, that is, diversification. I formally establish these results and provide further discussion in the Appendix. Importantly, Assumption 1 holds in the calibrated model.

Proposition 1 establishes how investing banks' choices are affected by changes in the aggregate state variables. Notably, Assumption 1 is sufficient but not necessary for this proposition.

Proposition 1: Suppose that constraint (10) binds, $\mu=\bar{\mu}$. Then, portfolio overlap $P O(A, z)$ increases in $A$ and decreases in $z$, and spread $\xi(A, z)=$ $R(A, z)-\rho(A, z) \bar{\mu}$ decreases in $A$ and increases in $z$.

Proof: See the Appendix.
The aggregate state variables affects the interbank allocation through the project return $R$. Clearly, the aggregate productivity $z$ is positively related to $R$. Furthermore, as long as $\mu=\bar{\mu}$, an increase in the amount of assets $A$ translates into higher investment in the risky decreasing-returns technology and hence a lower $R$. From the perspective of investing banks, $R$ is a nonrandom part of their total return on assets. Holding everything else equal, a decline in $R$ reduces spread $R-\rho \bar{\mu}$ and increases their individual default probabilities. Noninvesting banks-lenders in the interbank market-require compensation for this additional risk. To prevent their borrowing rate $\rho$ from a sharp increase, investing banks diversify more actively.

A change in $R$, therefore, affects the individual and systemic default probabilities in two ways. First, a decline in $R$ narrows spread $R-\rho \bar{\mu}$ and, by Lemma 2, makes both systemic and individual defaults more likely. Second, an increase in diversification following a decline in $R-\rho \bar{\mu}$ leads to an increase in portfolio overlap and makes risk exposures of investing banks more alike. Diversification prevents the probability of individual defaults from a steep increase. However, systemic crises become more likely. Corollary 1 immediately follows.

Corollary 1: Suppose that constraint (10) binds, $\mu=\bar{\mu}$. Then systemic default probability $p_{\text {syst }}^{d}(A, z)$ increases in $A$ and decreases in $z$. Individual default probability $p_{i}^{d}(A, z)$ is generally nonmonotone in $A$ and $z$.

Proposition 1 and Corollary 1 imply that systemic crises, associated with defaults of all investing banks and large real losses, are more likely when the total amount of assets $A$ is large but assets are unproductive, that is, $z$ is low. In normal times, when $A$ and $z$ are close to their average values, only large negative project-specific shocks can cause defaults of all investing banks. Such large negative shocks are unlikely, meaning that the systemic default probability is low in those states of the world. However, when $A$ is high and $z$ is low, smaller project-specific shocks are sufficient to trigger simultaneous defaults of all investing banks. Corollary 2 formalizes this idea. In particular, it states that there exists a threshold $A^{*}=A^{*}(z, x)$, where $x=\left(x_{1}, \ldots, x_{N}\right)$ is the vector of realized project-specific shocks, such that a systemic crisis happens if and only if the total asset amount exceeds this threshold. Naturally, if the economy is hit by adverse shocks (i.e., $z$ is low and elements of $x$ are high), the threshold is low, meaning that a systemic crisis happens for lower values of $A$.

Corollary 2: Suppose that constraint (10) binds, $\mu=\bar{\mu}$. Then, for given $z$ and vector of realized project-specific shocks $x=\left(x_{1}, \ldots, x_{N}\right)$, there exists a threshold $A^{*}(z, x) \leq \infty$ such that a systemic crisis occurs if and only if $A>A^{*}(z, x) .{ }^{12}$ Furthermore, if $A^{*}(z, x)<\infty$, then $A^{*}(z, x)$ increases in $z$ and decreases in $x_{i} \forall i$.

[^3]![](https://cdn.mathpix.com/cropped/2025_03_17_6b24cbbaa17d6d4c0aa8g-10.jpg?height=604&width=1275&top_left_y=235&top_left_x=200)

Figure 3. Comparative statics with respect to the total amount of assets $A$ and the aggregate productivity $z$ in the calibrated model. The calibration is described in Section III. Solid blue lines are obtained under $\log z=0.0255$ ( 0.80 standard deviations above average). Red dashed lines are obtained under $\log z=-0.0255$ ( 0.80 standard deviations below average). Vertical gray lines mark asset amounts at which the constraint $\mu \leq \bar{\mu}$ becomes slack. (Color figure can be viewed at wileyonlinelibrary.com)

Figure 3 summarizes the comparative statics results. As long as $\mu=\bar{\mu}$, the fraction of assets invested in the risky technology is $\frac{1-\bar{\mu}}{1-\mu}=1$ (Panel A, horizontal parts of the lines), and the variables respond to changes in $A$ and $z$ in line with Proposition 1 and Corollary 1. When $R$ is sufficiently low, the constraint $\mu \leq \bar{\mu}$ becomes slack. In this regime, the risky projects are unproductive and a nonzero amount of the economy's total assets is allocated to the storage technology. A further increase in $A$ barely affects the amount of assets invested in the risky technology and hence the return $R$. Default probabilities, spread, interbank rate, and the degree of portfolio overlap all flatten. ${ }^{13}$ Notably, even in the states with $\mu<\bar{\mu}$ (high $A$, low $z$ ), portfolio overlap and systemic risk remain high.

The analyses above show how changes in the aggregate state variables affect the decisions of investing banks, the degree of portfolio overlap, and the probabilities of costly defaults. To emphasize the role of endogenous changes in the investing banks' portfolio structures for these outcomes, in Internet Appendix Section VII, I consider the model in which investing banks are forced to invest only in projects of their islands. In that model, portfolio overlap is mechanically zero and systemic risk is low. At the same time, being unable to diversify their individual risks, investing banks face much higher individual default risks and much higher borrowing rates. As a result, they choose to borrow less in the interbank market (in particular, the constraint $\mu \leq \bar{\mu}$ is slack

[^4]![](https://cdn.mathpix.com/cropped/2025_03_17_6b24cbbaa17d6d4c0aa8g-11.jpg?height=679&width=1212&top_left_y=239&top_left_x=244)

Figure 4. Equilibrium asset accumulation policy functions $A^{\prime}(A, z, x)$. Policies are obtained from solving the calibrated model. The solution method is discussed in Internet Appendix Section IX. The calibration is described in Section III. Shock values: $\log z_{a v}=0 ; \log z_{\text {boom }}=0.0537$ (1.69 standard deviations above average); $x_{i g}=0$ for five projects and 0.0339 for two projects ( 1.36 standard deviations above average $) ; x_{i b}=0.0339$ for seven projects. $A^{*}\left(z_{a v}, x_{b}\right)$ is the systemiccrisis threshold defined in Corollary 2. (Color figure can be viewed at wileyonlinelibrary.com)
in more states of the world), resulting in lower investment in the productive risky technology.

## C. Systemic Crises in a Dynamic Model

Even though the interbank problem is static, banks' optimal choices are functions of the state variables and thus change over time. This subsection discusses how the household's intertemporal asset accumulation choices and time-varying aggregate productivity interact with the interbank outcomes. In particular, it describes how the economy transits from states of low systemic risk to states of high systemic risk.

Figure 4 shows equilibrium asset accumulation policies $A^{\prime}(A, z, x)$ for two values of aggregate productivity $z$, a long-run average $z_{a v}$ and $z_{b o o m}>z_{a v}$, and two sets of realizations of project-specific shocks, $x_{g}<x_{b}$ (see caption for exact values). These policy functions are obtained from solving the calibrated model described in the next section. The discontinuity in the policy $A^{\prime}\left(A, z_{a v}, x_{b}\right)$ at $A^{*}\left(z_{a v}, x_{b}\right)$ is associated with a systemic crisis. In particular, for $z=z_{a v}$ and $x=x_{b}$, a systemic default happens if $A>A^{*}\left(z_{a v}, x_{b}\right)$ and does not happen otherwise (Corollary 2). The discontinuity at $A^{*}\left(z_{a v}, x_{b}\right)$ reflects the fact that if the economy starts the period with $A>A^{*}\left(z_{a v}, x_{b}\right), z=z_{a v}$, and the risky projects are hit by shocks $x_{b}$, all investing banks default simultaneously and a fraction $\theta$ of all assets in the economy is lost. That is, the project-specific shocks not
only reduce the payoff to capital investors (5) directly but also lead to large real losses due to a systemic financial crisis. These default losses lead to sharp declines in the asset accumulation policy, consumption, and the household's welfare. ${ }^{14}$ If $A<A^{*}\left(z_{a v}, x_{b}\right)$, the same project-specific shocks lead to the same direct capital losses but do not trigger a systemic crisis, and so the economy is able to avoid large real default costs.

Consider the economy starting at point $O$, which is the steady state for $z=z_{a v}$ and $x=x_{g}$. At this point, the total amount of assets is relatively low and the risky projects are productive. Diversification needs are limited, investing banks' portfolio overlap is relatively low, and their risk exposures are not strongly correlated. In states with productive projects and low portfolio overlap, systemic crises are unlikely. Adverse realizations of project-specific shocks, $x=x_{b}$, bring the economy to $B_{O}$. This is not exceptionally painful because the financial system manages to avoid a systemic crisis and a large real loss of assets.

Consider now the economy at point $C$. Here, aggregate productivity is the same as at $O, z=z_{a v}$. However, the amount of assets is significantly larger, $A_{C}>A^{*}\left(z_{a v}, x_{b}\right)>A_{O}$, which translates into a lower return $R$ and higher default probabilities of investing banks. Investing banks respond by more active diversification. Consequently, the degree of portfolio overlap increases and so does the commonality in risk exposures among investing banks. The probability of a systemic crisis is therefore higher than at $O$. The same project-specific shocks $x_{b}$ that have only a modest negative impact on the economy at $O$ are more detrimental at $C$. They cause large default losses due to simultaneous failures of all investing banks, bringing the economy from $C$ to $B_{C}$.

How does the economy move from $O$ to $C$ ? A positive shock to aggregate productivity (in Figure $4, z$ increases from $z_{a v}$ to $z_{\text {boom }}$ ) drives up returns on the risky projects. The representative household starts to accumulate more assets, which leads to a credit expansion. However, due to its mean-reversion, aggregate productivity comes back to $z_{a v}$ after a few periods in the boom state. The economy arrives at $C$ where it is more fragile than at $O$, in the sense that smaller project-specific shocks are able to cause a systemic crisis.
The results of this section suggest that large-scale financial crises in this economy tend to occur after a period of credit expansion that is driven by a temporary productivity boom. In the following section, I calibrate the model and show that this prediction holds in the calibrated model.

## III. Quantitative Analysis

This section calibrates and quantitatively evaluates the model. Specifically, I explore how the model economy behaves around financial crises and how these model-implied behaviors compare to those in the data.

[^5]Table I
Parameterization

| Parameter | Value | Parameter | Value |
| :--- | ---: | :--- | ---: |
| Preferences |  | Project-specific shocks |  |
| Inverse IES | $\psi=4$ | Number of islands | $N=7$ |
| Inverse Frisch elasticity | $\nu=0.5$ | Standard deviation | $\sigma_{x}=0.025$ |
| Time-discounting factor |  |  |  |
| Production technology | $\eta=0.9$ | Banking sector |  |
| Capital share | $\delta=0.1$ | Diversification cost | $f=0.0069$ |
| Depreciation rate |  | Storage return | $\rho_{s}=1.0005$ |
| Aggregate shocks | $\varphi_{z}=0.90$ | Default loss | $\theta=0.12$ |
| Persistence | $\sigma_{z}=0.014$ | Banks per islands | $M=570$ |
| St. dev. of innovations |  |  |  |

## A. Calibration

The model period is one year. Table I lists parameter values. Some of the parameters are standard. Other parameters are calibrated to simultaneously match certain empirical moments. Below, I describe these moments and specify which parameters they are mostly helpful in identifying. ${ }^{15}$

Preferences and production technology. Several parameters are set to the values commonly used in the macroeconomic literature. The time-discounting factor is $\beta=0.98$, the Frisch elasticity of labor supply is $v^{-1}=2$, and the intertemporal elasticity of substitution is $\psi^{-1}=0.25$. I set $\delta=0.1$, which implies an average capital depreciation rate of $10 \%$. For the risky production technology, I use $\eta=0.3$, which implies an average capital share of 0.306 . The small difference between the capital share and $\eta$ arises because final output in the model can be produced via the risky production technology and via the storage technology. However, in the calibrated model, the storage technology is rarely used. The economy spends $68 \%$ of time in the states in which the storage technology is not used at all, $\mu=\bar{\mu}$. On average, only $3 \%$ of the total capital stock is invested in storage. As a result, taking the storage technology into account when computing the capital share has a very small effect on the results.

Aggregate shocks. Using postwar U.S. data on GDP, hours, and investment from the Bureau of Economic Analysis (BEA), I construct a series of Solow residuals and log-linearly detrend it. The same exercise is then repeated in the model. The parameters $\varphi_{z}$ and $\sigma_{z}$ are picked to match the persistence and the standard deviation of innovations in the $\operatorname{AR}(1)$ process (2). I obtain $\varphi_{z}=0.90$ and $\sigma_{z}=0.014$.

Project-specific shocks. Two parameters govern the importance of projectspecific shocks: their volatility $\sigma_{x}$ and the number of independent risk factors

[^6]
[^0]:    ${ }^{9}$ Under normal shocks, the capital payoff (5) or overall depreciation rate $\delta+\tilde{x}_{i}$ can be negative. However, in the calibrated model, both of these possibilities are vanishingly improbable because $\sigma_{x}^{2}$ is sufficiently low.

[^1]:    ${ }^{10}$ Notice that diversification costs are paid by investing banks' shareholders (the representative household) upfront. An alternative assumption would be that diversification costs are paid by investing banks ex post and thus directly affect their default cutoffs.

[^2]:    ${ }^{11}$ Positive $\psi$ implies that the household is risk-averse, whereas banks are risk-neutral. Such a preference misalignment can be justified, for example, by imperfect compensation schemes of bankers (Chevalier and Ellison (1997)). This assumption substantially simplifies both theoretical and numerical analyses. However, the main results hold if there is no preference misalignment, as shown in Internet Appendix Section V.

[^3]:    ${ }^{12}$ Note that $A^{*}(z, x)=\infty$ implies that a systemic crisis never occurs for any finite $A$ for given $z$ and $x$.

[^4]:    ${ }^{13}$ In default states, lenders split the recovered value of their borrower's portfolio and so their return is proportional to $\frac{1}{\mu}$ (see (9)). A reduction in $\mu$ increases this return, and so the borrowing rate $\rho$ and the default probabilities $p_{\text {syst }}^{d}$ and $p_{i}^{d}$ decrease mildly.

[^5]:    ${ }^{14}$ Section IV conducts a formal welfare analysis and discusses policies that can prevent a large fraction of systemic crises and associated real default losses.

[^6]:    ${ }^{15}$ Internet Appendix Section I describes the data sources. Internet Appendix Section II.E conducts sensitivity analysis with respect to several key parameters. Internet Appendix Section III.A verifies that the model matches the targeted moments well, and Section III.B shows that the model performs reasonably well in terms of matching second moments of aggregate macroeconomic series. The numerical algorithm used to solve the model is described in Internet Appendix Section IX.

