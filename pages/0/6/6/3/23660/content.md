[[!redirects HoTT book real numbers]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A notion of real numbers that is [[sequentially modulated Cauchy complete]], because the [[modulated Cauchy real numbers]] are not sequentially modulated Cauchy complete in [[constructive mathematics]]

## Definition ##

### As a sequentially Cauchy complete Archimedean ordered pointed halving group ###

Note: everything in this particular section was copied from the Sandbox of the HoTT wiki and is likely to be original research. 

The **HoTT book real numbers** is the (homotopy)-initial **sequentially Cauchy complete Archimedean ordered pointed halving group**. There should be a corresponding definition as a higher inductive-inductive type, but that still has to be worked out. 

We define a sequentially Cauchy complete Archimedean ordered pointed halving group below as follows: 

#### Pointed abelian groups ####

A **pointed abelian group** is a set $A$ with an element $1:A$ called **one** and a binary operation $(-)-(-):A \times A \to A$ called **subtraction** such that 

* for all elements $a:A$, $a - a = 1 - 1$

* for all elements $a:A$, $(1 - 1) - ((1 - 1) - a) = a$

* for all elements $a:A$ and $b:A$, $a - ((1 - 1) - b) = b - ((1 - 1) - a)$

* for all elements $a:A$, $b:A$, and $c:A$, $a - (b - c) = (a - ((1 - 1) - c)) - b$

$0$ is defined as $1 - 1$, $-a$ is defined as $0 - a$, and $a + b$ is defined as $a - (-b)$. It is left to the reader as an exercise to prove from the given axioms and definitions that $(A,0,+,-,1)$ is an abelian group with an extra point $1$. 

#### Pointed halving groups ####

A **pointed halving group** is a pointed abelian group *G* with a function $(-)/2:G \to G$ called **halving** or **dividing by two** such that for all elements $g:G$, $g/2 = g - g/2$. 

#### Totally ordered pointed halving groups ####

A pointed halving group $R$ is a totally ordered pointed halving group if it comes with a function $\max:R \times R \to R$ such that 

* for all elements $a:R$, $\max(a, a) = a$

* for all elements $a:R$ and $b:R$, $\max(a, b) = \max(b, a)$

* for all elements $a:R$, $b:R$, and $c:R$, $\max(a, \max(b, c)) = \max(\max(a, b), c)$

* for all elements $a:R$ and $b:R$, $\max(a, b) = a$ or $\max(a, b) = b$

* for all elements $a:R$ and $b:R$, $\max(a, b) = b$ implies that for all elements $c:R$, $\max(a - c, b - c) = b - c$

#### Strictly ordered pointed halving groups ####

A totally ordered pointed halving group $R$ is a strictly ordered pointed abelian group if it comes with a type family $\lt$ such that

* for all elements $a:R$ and $b:R$, $a \lt b$ is a proposition
* for all elements $a:R$, $a \lt a$ is false
* for all elements $a:R$, $b:R$, and $c:R$, if $a \lt c$, then $a \lt b$ or $b \lt c$
* for all elements $a:R$ and $b:R$, if $a \lt b$ is false and $b \lt a$ is false, then $a = b$
* for all elements $a:R$ and $b:R$, if $a \lt b$, then $b \lt a$ is false.
* $1 - 1 \lt 1$
* for all elements $a:R$ and $b:R$, if $1 - 1 \lt a$ and $1 - 1 \lt b$, then $(1 - 1) \lt a - ((1 - 1) - b)$

The homotopy initial strictly ordered pointed halving group is the dyadic rational numbers $\mathbb{D}$. 

#### Archimedean ordered pointed halving groups ####

A strictly ordered pointed halving group $A$ is an Archimedean ordered pointed halving group if for all elements $a:A$ and $b:A$, if $a \lt b$, then there merely exists a dyadic rational number $d:\mathbb{D}$ such that $a \lt h(d)$ and $h(d) \lt b$. 

#### Sequentially Cauchy complete Archimedean ordered pointed halving groups ####

Let 

$$\mathbb{D}_{+} \coloneqq \sum_{a:\mathbb{D}} 0 \lt a$$

be the positive dyadic rational numbers. 

A **sequence** in $A$ is a function $x:\mathbb{N} \to A$. 

A sequence $x:\mathbb{N} \to A$ is a **Cauchy sequence** if for all positive dyadic rational numbers $\epsilon:\mathbb{D}_{+}$, there merely exists a natural number $N:\mathbb{N}$ such that for all natural numbers $i:\mathbb{N}$ and $j:\mathbb{N}$ such that $N \leq i$ and $N \leq j$, $\max(x_i - x_j, x_j - x_i) \lt \epsilon$. 

An element $l:A$ is said to be a **limit** of the sequence $x:\mathbb{N} \to A$ if for all positive dyadic rational numbers $\epsilon:\mathbb{D}_{+}$, there merely exists a natural number $N:\mathbb{N}$ such that for all natural numbers $i:\mathbb{N}$ such that $N \leq i$, $\max(x_i - l, l - x_i) \lt \epsilon$

$A$ is **sequentially Cauchy complete** if every Cauchy sequence in $A$ merely has a limit. 

### As a sequentially modulated Cauchy complete Archimedean field ###

Let $F$ be an [[Archimedean field]]. $F$ is *[[sequentially modulated Cauchy complete]]* if every [[Cauchy sequence]] in $F$ with a [[modulus of convergence]] [[converges]]. The set of __HoTT book real numbers__ $\mathbb{R}_H$ is the [[initial object]] in the [[category]] of sequentially modulated Cauchy complete Archimedean fields. 

### As a Cauchy structure ###

The set of __HoTT book real numbers__ $\mathbb{R}_H$ is the initial object in the category of [[Cauchy structures]] and [[Cauchy structure homomorphisms]]. 

### As a higher inductive-inductive type ###

Let $\mathbb{Q}$ be the [[rational numbers]] and let 

$$\mathbb{Q}_{+} \coloneqq \sum_{x:\mathbb{Q}} 0 \lt x$$

be the positive rational numbers. The __HoTT book real numbers__ $\mathbb{R}_H$ are inductively generated by the following:

* a function $inj: \mathbb{Q} \to \mathbb{R}_H$

* a function $lim: C(\mathbb{R}_H) \to \mathbb{R}_H$, where $C(\mathbb{R}_H)$ is the type of [[Cauchy approximation]]s in $\mathbb{R}_H$.  

* a dependent family of terms

$$a:\mathbb{R}_H, b:\mathbb{R}_H \vdash eq_{\mathbb{R}_H}(a, b): \left( \prod_{\epsilon:\mathbb{Q}_{+}} (a \sim_{\epsilon} b) \right) \to (a =_{\mathbb{R}_H} b)$$

and the [[premetric]] type family $\sim$ is simultaneously inductively generated by the following:

* a dependent family of terms
$$a:\mathbb{Q}, b:\mathbb{Q}, \epsilon:\mathbb{Q}_{+} \vdash \mu_{\mathbb{Q}, \mathbb{Q}}(a, b, \epsilon): (\vert a - b \vert \lt \epsilon) \to (inj(a) \sim_{\epsilon} inj(b))$$

* a dependent family of terms
$$a:\mathbb{Q}, b:C(\mathbb{R}_H), \epsilon:\mathbb{Q}_{+}, \eta:\mathbb{Q}_{+} \vdash \mu_{\mathbb{Q}, C(\mathbb{R}_H)}(a, b, \epsilon, \eta): (inj(a) \sim_{\epsilon} b_{\eta}) \to (inj(a) \sim_{\epsilon + \eta} lim(b))$$

* a dependent family of terms
$$a:C(\mathbb{R}_H), b:\mathbb{Q}, \delta:\mathbb{Q}_{+}, \epsilon:\mathbb{Q}_{+} \vdash \mu_{C(\mathbb{R}_H), \mathbb{Q}}(a, b, \delta, \epsilon): (a_{\delta} \sim_{\epsilon} inj(b) ) \to (lim(a) \sim_{\delta + \epsilon} inj(b))$$

* a dependent family of terms
$$a:C(\mathbb{R}_H), b:C(\mathbb{R}_H), \delta:\mathbb{Q}_{+}, \epsilon:\mathbb{Q}_{+}, \eta:\mathbb{Q}_{+} \vdash \mu_{C(\mathbb{R}_H), C(\mathbb{R}_H)}(a, b, \delta, \epsilon, \eta): (a_{\delta} \sim_{\epsilon} b_{\eta} ) \to (lim(a) \sim_{\delta + \epsilon + \eta} lim(b))$$

* a dependent family of terms
$$a:\mathbb{Q}, b:\mathbb{Q}, \epsilon:\mathbb{Q}_{+} \vdash \pi(a, b, \epsilon): isProp(a \sim_{\epsilon} b)$$

## Properties 

The [[analytic functions]], such as the [[exponential function]], the [[sine function]], and the [[cosine function]] are well defined in the HoTT book real numbers, since all modulated Cauchy sequences converge in the HoTT book real numbers. 

## See also ##

* [[Cauchy real numbers]]
* [[generalized Cauchy real numbers]]
* [[premetric space]]

## References ##

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))
* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)