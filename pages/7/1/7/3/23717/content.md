+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

The concept of [[continuous functions]] familiar from [[epsilontic analysis]].

## Definition ##

+-- {: .num_defn #InRealNumbers}
###### Definition
**(pointwise continuous function in the real numbers)

Let $\mathbb{R}$ be the [[real numbers]] and let 

$$\mathbb{R}_{+} \coloneqq \{a \in \mathbb{R} \vert 0 \lt a\}$$

be the positive elements in $\mathbb{R}$. A function $f:\mathbb{R} \to \mathbb{R}$ is __continuous at a point__ $c \in \mathbb{R}$ if 

$$isContinuousAt(f, c) \coloneqq \forall \epsilon \in \mathbb{R}_{+}. \exists \delta \in \mathbb{R}_{+}. \forall x \in \mathbb{R}. (\vert x - c \vert \lt \delta) \to (\vert f(x) - f(c) \vert \lt \epsilon)$$

$f$ is __pointwise continuous__ in $\mathbb{R}$ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in \mathbb{R}. isContinuousAt(f, c)$$

=--

+-- {: .num_defn #BetweenArchimedeanOrderedFields}
###### Definition
**(pointwise continuous function between Archimedean ordered fields)**

Let $F$ and $K$ be [[Archimedean ordered fields]] and let 

$$F_{+} \coloneqq \{a \in F \vert 0 \lt a\} \quad K_{+} \coloneqq \{a \in K \vert 0 \lt a\}$$

be the positive elements in $F$ and $K$. A function $f:F \to K$ is __continuous at a point__ $c \in F$ if 

$$isContinuousAt(f, c) \coloneqq \forall \epsilon \in K_{+}. \forall x \in F. \exists \delta \in F_{+}. (\max(x - c, c - x) \lt \delta) \to (\max(f(x) - f(c), f(c) - f(x)) \lt \epsilon)$$

$f$ is __pointwise continuous__ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in F. isContinuousAt(f, c)$$

=--

+-- {: .num_defn #BetweenMetricSpaces}
###### Definition
**(pointwise continuous function between metric spaces)**

Let $(X, d_X)$ and $(Y, d_Y)$ be [[metric spaces]], and let 

$$\mathbb{R}_{+} \coloneqq \{a \in \mathbb{R} \vert 0 \lt a\}$$

be the positive real numbers. A function $f:X \to Y$ is __continuous at a point__ $c \in X$ if 

$$isContinuousAt(f, c) \coloneqq \forall \epsilon \in \mathbb{R}_{+}. \forall x \in X. \exists \delta \in \mathbb{R}_{+}. d_X(x, c) \lt \delta \to d_Y(f(x), f(c)) \lt \epsilon)$$

$f$ is __pointwise continuous__ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in X. isContinuousAt(f, c)$$

=--

+-- {: .num_defn #BetweenUniformSpaces}
###### Definition
**(pointwise continuous function between uniform spaces)**

Let $(X, \mathcal{U}(X), \approx)$ and $(Y, \mathcal{U}(Y), \approx)$ be [[uniform spaces]]. A function $f:X \to Y$ is __continuous at a point__ $c \in X$ if 

$$isContinuousAt(f, c) \coloneqq \forall E \in \mathcal{U}(Y). \forall x \in X. \exists D \in \mathcal{U}(X). x \approx_D c \to f(x) \approx_E f(c))$$

$f$ is __pointwise continuous__ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in X. isContinuousAt(f, c)$$

=--

+-- {: .num_defn #BetweenGeneralizedFilterSpaces}
###### Definition
**(pointwise continuous function between generalised filter spaces)**

Let $(X, \mathcal{F}(X), \mathrm{isLimit}_X)$ and $(Y, \mathcal{F}(Y), \mathrm{isLimit}_Y)$ be [[generalised filter spaces]]. A function $f:X \to Y$ is __continuous at a point__ $c \in X$ if 
 
$$isContinuousAt(f, c) \coloneqq \forall F \in \mathcal{F}(X).\mathrm{isLimit}_X(F, c) \to \mathrm{isLimit}_Y(f(F), f(c)))$$

$f$ is __pointwise continuous__ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in X. isContinuousAt(f, c)$$
=--

+-- {: .num_defn #InFunctionLimitSpaces}
###### Definition
**(pointwise continuous function in function limit spaces)**

Let $T$ be a [[Hausdorff function limit space]], and let $S \subseteq T$ be a [[subset]] of $T$. A function $f:S \to T$ is __continuous at a point__ $c \in S$ if the [[limit of a function|limit of $f$ approaching $c$]] is equal to $f(c)$. 

$$\lim_{x \to c} f(x) = f(c)$$

$f$ is __pointwise continuous__ on $S$ if it is continuous at all points $c \in S$: 

$$isPointwiseContinuous(f) \coloneqq \forall c \in S. \lim_{x \to c} f(x) = f(c)$$
=--


### As structure

In [[dependent type theory]], one could change the [[universal quantifiers]] and [[existential quantifiers]] in the definition of uniformly continuous function into [[dependent product types]] and [[dependent sum types]]. 

\begin{definition}
Let $\mathrm{R}_+ \coloneqq \sum_{x:\mathbb{R}} \epsilon \gt 0$ denote the positive real numbers. Given [[metric spaces]] $(X, d_X)$ and $(Y, d_Y)$, a **pointwise continuous function** between $X$ and $Y$ is a function $f:X \to Y$ between their underlying sets with a dependent function which says: 

> For all elements $a:X$ and for all positive real number $\epsilon \gt 0$, there is as structure a positive real number $\delta \gt 0$ such that for all elements $b:X$, $\delta_Y(f(a), f(b))$ is less than $\epsilon$ whenever $\delta_X(a, b)$ is less than $\delta$

$$\prod_{a:X} \prod_{\epsilon:\mathrm{R}_+} \sum_{\delta:\mathbb{R}_+} \prod_{b:X} (\delta_X(a, b) \lt \delta) \to (\delta_Y(f(a), f(b)) \lt \epsilon)$$

By the [[type theoretic axiom of choice]], which is simply the distributivity of [[dependent function types]] over [[dependent sum types]], this is the same as saying that 

> There exists as structure a function $\omega:X \to (\mathrm{R}_+ \to \mathrm{R}_+)$ such that for all elements $a:X$, for all positive real numbers $\epsilon \gt 0$ and for all elements $b:X$, $\delta_Y(f(a), f(b))$ is less than $\epsilon$ whenever $\delta_X(a, b)$ is less than $\omega(\epsilon)$

$$\sum_{\omega:X \to (\mathrm{R}_+ \to \mathrm{R}_+)} \prod_{a:X} \prod_{\epsilon:\mathrm{R}_+} \prod_{b:X} (\delta_X(a, b) \lt \omega(\epsilon)) \to (\delta_Y(f(a), f(b)) \lt \epsilon)$$
\end{definition}

There exists a similar definition for [[uniform spaces]]: 

\begin{definition}
Given uniform spaces $(X, \mathcal{U}(X), \approx)$ and $(Y, \mathcal{U}(Y), \approx)$, a **pointwise continuous function** between $X$ and $Y$ is a function $f:X \to Y$ with a dependent function which says: 

> For all elements $x:A$ and for all [[entourages]] $E:\mathcal{U}(Y)$, there is as structure an entourage $D:\mathcal{U}(X)$ such that for all elements $b:X$, $f(a) \approx_{E} f(b)$ whenever $a \approx_{D} b$

$$\prod_{a:X} \prod_{E:\mathcal{U}(Y)} \sum_{D:\mathcal{U}(X)} \prod_{b:X} (a \approx_{D} b) \to (f(a) \approx_{E} f(b))$$

By the [[type theoretic axiom of choice]], which is simply the distributivity of [[dependent function types]] over [[dependent sum types]], this is the same as saying that 

> There exists as structure a function $\omega:X \to (\mathcal{U}(Y) \to \mathcal{U}(X))$ between the sets of entourages such that for all elements $a:X$ and entourages $E:\mathcal{U}(Y)$ and for all elements $b:X$, $f(a) \approx_{E} f(b)$ whenever $a \approx_{\omega(E)} b$

$$\sum_{\omega:X \to (\mathcal{U}(Y) \to \mathcal{U}(X))} \prod_{a:X} \prod_{E:\mathcal{U}(Y)} \prod_{b:X} (a \approx_{\omega(a, E)} b) \to (f(a) \approx_{E} f(b))$$
\end{definition}

## See also ##

* [[limit of a function]]

* [[differentiable function]]

* [[uniformly continuous function]]


[[!redirects pointwise continuous functions]]

[[!redirects pointwise continuous]]

[[!redirects pointwise continuity]]


