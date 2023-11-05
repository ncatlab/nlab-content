
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Rational numbers
* table of contents
{: toc}

## Definition

A _rational number_ is a [[fraction]] of two [[integer]] [[numbers]].

### As a field

The [[field]] of **rational numbers**, $\mathbb{Q}$, is the [[field of fractions]] of the [[commutative ring]] of [[integers]], $\mathbb{Z}$, hence the field consisting of formal [[fractions]] ("[[ratios]]") of [[integers]].

### As a commutative ring

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers. The positive integers are embedded into every [[commutative ring]] $R$: there is an injection $inj:\mathbb{N}^+\to\R$ such that $inj(1) = 1$ and $inj(s(n)) = inj(n) + 1$ for all $n:\mathbb{N}^+$. 

Suppose $R$ has an injection $inv:\mathbb{N}^+\to\R$ such that $inj(n) \cdot inv(n) = 1$ and $\inv(n) \cdot \inj(n) = 1$ for all $n:\mathbb{N}^+$. Then $R$ is called a __[[commutative algebra|$\mathbb{Q}$-algebra]]__, and the commutative ring of __rational numbers__ $\mathbb{Q}$ is the [[initial object|initial]] commutative $\mathbb{Q}$-algebra. 

It can then be proven from the ring axioms and the properties of the integers that every rational number apart from zero and has a multiplicative inverse, making $\mathbb{Q}$ a field.

### As an sequential colimit in CRing

Let $\mathbb{Z}[1/n!]$ be the [[localization of a commutative ring|localization]] of the [[integers]] $\mathbb{Z}$ [[localisation of a commutative ring away from an element|away from]] the [[factorial]] $n!$, and for each $i \in \mathbb{N}$, there is a unique commutative [[ring homomorphism]] $h_{i}:\mathbb{Z}[1/i!]\to\mathbb{Z}[1/(i + 1)!]$ defined by the [[universal property]] of localisation of $\mathbb{Z}[1/i!]$ away from $i + 1$. Then the commutative ring of __rational numbers__ $\mathbb{Q}$ is the [[sequential colimit]] of the [[diagram]]

$$\mathbb{Z}[1/0!] \overset{h_0}\to \mathbb{Z}[1/1!] \overset{h_1}\to \mathbb{Z}[1/2!] \overset{h_2}\to \ldots$$

### As an abelian group

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers and let $(\mathbb{Z},0,+,-,1)$ be the [[free abelian group]] on the set ${1}$.  

Let $A$ be an [[abelian group]] containing $\mathbb{Z}$ as an abelian subgroup. The positive integers are embedded into the [[function algebra|function abelian group]] $A \to A$, with $id_A:A \to A$ being the [[identity function]] on $A$; i.e. there is an injection $inj:\mathbb{N}^+\to (A \to A)$ such that $inj(1) = id_A$ and $inj(s(n)) = inj(n) + id_A$ for all $n:\mathbb{N}^+$.

Suppose $A$ has an injection $inv:\mathbb{N}^+\to (A \to A)$ such that for all $n:\mathbb{N}^+$, $inj(n) \circ inv(n) = id_A$ and $inv(n) \circ inj(n) = id_A$. Then the abelian group of __rational numbers__ $\mathbb{Q}$ is the [[initial object|initial]] such abelian group. 

### As an initial object in a category

Let $\mathbb{Z}$ be the [[integers]] and let 
$$\mathbb{Z}_{#0} \coloneqq \{a \in \mathbb{Z} \vert a \lt 0 \vee 0 \lt a \}$$
be the set of integers apart from zero. 

For lack of a better name, let us define a *set with rational numbers* to be a set $A$ with a function $\iota \in \mathbb{Z} \times \mathbb{Z}_{#0} \to A$ with domain the Cartesian product $\mathbb{Z} \times \mathbb{Z}_{#0}$ and codomain $A$, such that 

$$\forall a \in \mathbb{Z}. \forall b \in \mathbb{Z}_{#0}. \forall c \in \mathbb{Z}. \forall d \in \mathbb{Z}_{#0}. (a \cdot d = c \cdot b) \implies (\iota(a, b) = \iota(c, d))$$

A *homomorphism of sets with rational numbers* between two sets with rational numbers $A$ and $B$ is a function $f \in B^A$ such that 

$$\forall a \in \mathbb{Z}. \forall b \in \mathbb{Z}_{#0}. f(\iota_A(a, b)) = \iota_B(a, b)$$

The *category of sets with rational numbers* is the category $SwRN$ whose objects $Ob(SwRN)$ are sets with rational numbers and whose morphisms $Mor(A,B)$ for sets with rational numbers $A \in Ob(SwDF)$, $B \in Ob(SwRN)$ are homomorphisms of sets with rational numbers. The set of **rational numbers**, denoted $\mathbb{Q}$, is defined as the initial object in the category of sets with rational numbers. 

### In dependent type theory

In [[dependent type theory]], there are multiple different definitions of the type of rational numbers. 

#### As a dependent sum type

Let $\mathbb{Z}$ be the [[integers]], let 

  $$\mathbb{Z}_{\neq 0} \coloneqq \sum_{a:\mathbb{Z}} \max(a,-a) \gt 0$$ 

be the non-zero integers, and let $\gcd:\mathbb{Z} \times \mathbb{Z} \to \mathbb{Z}$ be the [[greatest common divisor]] on the integers. Then the rational numbers is defined as the type of pairs of integers and non-zero integers such that the greatest common divisor is equal to one:

  $$\mathbb{Q} \coloneqq \sum_{x:\mathbb{Z}} \sum_{y:\mathbb{Z}_{\neq 0}} \gcd(x, \pi_1(y)) =_\mathbb{Z} 1$$

We define the function $(-)/(-) : \mathbb{Z} \times \mathbb{Z}_{\neq 0} \rightarrow \mathbb{Q}$ for all integers $a:\mathbb{Z}$ and non-zero integers $b:\mathbb{Z}_{\neq 0}$ by

$$a/b \coloneqq (a \div \gcd(a, \pi_1(b)), \pi_1(b) \div \gcd(a, \pi_1(b)), p(a, b))$$

where $p(a, b)$ is the witness that the greatest common divisor of $a \div \gcd(a, \pi_1(b))$ and $\pi_1(b) \div \gcd(a, \pi_1(b))$ is equal to 1, and $a \div b$ is [[integer]] [[division]], since integers are an [[Euclidean domain]] and thus have a division and remainder operation. 

#### As a higher inductive type

In [[homotopy type theory]], the type of **rational numbers**, denoted $\mathbb{Q}$, is defined ([UBP13, §11.1](#UBP13)) as the [[higher inductive type]] generated by:

* A function $(-)/(-) : \mathbb{Z} \times \mathbb{Z}_{\neq 0} \rightarrow \mathbb{Q}$, where 


  $$\mathbb{Z}_{\neq 0} \coloneqq \sum_{a:\mathbb{Z}} \max(a,-a) \gt 0$$ 

* A dependent product of functions between identities representing that equivalent fractions are equal: 

  $$equivfrac : \prod_{a:\mathbb{Z}} \prod_{b:\mathbb{Z}_{\neq 0}} \prod_{c:\mathbb{Z}} \prod_{d:\mathbb{Z}_{\neq 0}} (a \cdot \pi_1(d) = c \cdot \pi_1(b)) \to (a/b = c/d)\,,$$

* A set-truncator 
  
  $$\tau_0: \prod_{a:\mathbb{Q}} \prod_{b:\mathbb{Q}} isProp(a=b)$$ 

## Properties

Let $i$ be the inclusion of the non-zero integers into the integers. 

### Commutative ring structure on the rational numbers ###

+--{: .num_defn}
###### Definition
The rational number **zero** $0 \in \mathbb{Q}$ is defined as

$$0 \coloneqq 0/1$$
=--

+--{: .num_defn}
###### Definition
The binary operation **addition** $(-)+(-):\mathbb{Q} \times \mathbb{Q} \to \mathbb{Q}$ is defined as

$$a/b + c/d \coloneqq (a \cdot i(d) + c \cdot i(b))/(b \cdot d)$$

for $a \ in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$, $c \in \mathbb{Z}$, $d \in \mathbb{Z}_{#0}$. 
=--

+--{: .num_prop}
###### Proposition
For any $q \in \mathbb{Q}$ and $r \in \mathbb{Q}$, $q + r = r + q$. 
=--

+--{: .proof}
###### Proof
TODO
=--

+--{: .num_defn}
###### Definition
The unary operation **negation** $-(-):\mathbb{Q} \to \mathbb{Q}$ is defined as

$$-(a/b) \coloneqq (-a)/b$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$ 
=--

+--{: .num_defn}
###### Definition
The binary operation **subtraction** $(-)-(-):\mathbb{Q} \times \mathbb{Q} \to \mathbb{Q}$ is defined as

$$a/b - c/d \coloneqq (a \cdot i(d) - c \cdot i(b))/(b \cdot d)$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$, $c \in \mathbb{Z}$, $d \in \mathbb{Z}_{#0}$
=--

+--{: .num_defn}
###### Definition
The rational number **one** $1 \in \mathbb{Q}$ is defined as 

$$1 \coloneqq 1/1$$
=--

+--{: .num_defn}
###### Definition
The binary operation **multiplication** $(-)\cdot(-):\mathbb{Q} \times \mathbb{Q} \to \mathbb{Q}$ is defined as

$$a/b \cdot c/d \coloneqq (a \cdot c)/(b \cdot d)$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$, $c \in \mathbb{Z}$, $d \in \mathbb{Z}_{#0}$
=--

+--{: .num_defn}
###### Definition
The right $\mathbb{N}$-action **exponentiation** $(-)^{(-)}:\mathbb{Q} \times \mathbb{N} \to \mathbb{Q}$ is defined as

$$(a/b)^n \coloneqq (a^n)/(b^n)$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$, $n \in \mathbb{N}$.
=--

This makes the rational numbers into a commutative ring. 

### Order structure on the rational numbers ###

+--{: .num_defn}
###### Definition
The [[predicate]] *is positive*, denoted as $isPositive(a/b)$, is defined as

$$isPositive(a/b) \coloneqq (a \gt 0) \wedge (i(b) \gt 0) \vee (a \lt 0) \wedge (i(b) \lt 0)$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$. 
=--

+--{: .num_defn}
###### Definition
The [[predicate]] *is negative*, denoted as $isNegative(a/b)$, is defined as

$$isNegative(a/b) \coloneqq (a \gt 0) \wedge (i(b) \lt 0) \vee (a \lt 0) \wedge (i(b) \gt 0)$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$. 
=--

+--{: .num_defn}
###### Definition
The [[predicate]] *is zero*, denoted as $isZero(a/b)$, is defined as

$$isZero(a/b) \coloneqq a = 0$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$. 
=--

+--{: .num_defn}
###### Definition
The [[predicate]] *is non-positive*, denoted as $isNonPositive(a/b)$ is defined as

$$isNonPositive(a/b) \coloneqq \neg isPositive(a/b)$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$. 
=--

+--{: .num_defn}
###### Definition
The [[predicate]] *is non-negative*, denoted as $isNonNegative(a/b)$, is defined as

$$isNonNegative(a/b) \coloneqq \neg isNegative(a/b) $$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$. 
=--

+--{: .num_defn}
###### Definition
The [[predicate]] *is non-zero*, denoted as $isNonZero(a/b)$, is defined as

$$isNonZero(a/b) \coloneqq isPositive(a/b) \vee isNegative(a/b)$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$. 
=--


+--{: .num_defn}
###### Definition
The [[relation]] *is less than*, denoted as $p \lt q$, is defined as

$p \lt q \coloneqq isPositive(q - p)$

for $p:\mathbb{Q}$, $q:\mathbb{Q}$.
=--

+--{: .num_defn}
###### Definition
The dependent type *is greater than*, denoted as $p \gt q$, is defined as

$p \lt q \coloneqq isNegative(q - p)$

for $p:\mathbb{Q}$, $q:\mathbb{Q}$.
=-- 

+--{: .num_defn}
###### Definition
The dependent type *is apart from*, denoted as $p \# q$, is defined as

$p \lt q \coloneqq isNonZero(q - p)$

for $p:\mathbb{Q}$, $q:\mathbb{Q}$.

=--  

+--{: .num_defn}
###### Definition
The dependent type *is less than or equal to*, denoted as $p \leq q$, is defined as

$p \lt q \coloneqq isNonNegative(q - p)$

for $p:\mathbb{Q}$, $q:\mathbb{Q}$.

=--  

+--{: .num_defn}
###### Definition
The dependent type *is greater than or equal to*, denoted as $p \leq q$, is defined as

$p \lt q \coloneqq isNonPositive(q - p)$

for $p:\mathbb{Q}$, $q:\mathbb{Q}$.
=--  

### Pseudolattice structure on the rational numbers ###

+--{: .num_defn}
###### Definition
The **ramp function** $ramp:\mathbb{Q} \to \mathbb{Q}$ is defined as

$$ramp(a/b) \coloneqq (ramp(a) \cdot ramp(i(b)) + ramp(-a) \cdot ramp(i(-b)))/(b \cdot b)$$

for $a \in \mathbb{Z}$, $b \in \mathbb{Z}_{#0}$, $ramp:\mathbb{Z} \to \mathbb{Z}$.
=--

+--{: .num_defn}
###### Definition
The **minimum** $min:\mathbb{Q} \times \mathbb{Q} \to \mathbb{Q}$ is defined as

$$\min(p,q) \coloneqq p - ramp(p - q)$$

for $p:\mathbb{Q}$, $q:\mathbb{Q}$.
=--

+--{: .num_defn}
###### Definition
The **maximum** $max:\mathbb{Q} \times \mathbb{Q} \to \mathbb{Q}$ is defined as

$$\max(p, q) \coloneqq p + ramp(q - p)$$

for $p:\mathbb{Q}$, $q:\mathbb{Q}$.
=--

+--{: .num_defn}
###### Definition
The **absolute value** $\vert(-)\vert:\mathbb{Q} \to \mathbb{Q}$ is defined as

$$\vert p \vert \coloneqq \max(p, -p)$$

for $p:\mathbb{Q}$. 
=--

+--{: .num_defn}
###### Definition
The **metric** $\rho:\mathbb{Q} \times \mathbb{Q} \to \mathbb{Q}$ is defined as

$$\rho(p, q) \coloneqq \max(p, q) - \min(p, q)$$

for $p:\mathbb{Q}$, $q:\mathbb{Q}$. 
=--

### Uniform structure on the rational numbers ###

We define the ternary relation $x \sim_\epsilon y \coloneqq \rho(x, y) \lt \epsilon$ for $x \in \mathbb{Q}$, $y \in \mathbb{Q}$, and $\epsilon \in \mathbb{Q}_+$, called "$x$ and $y$ are within a distance of $\epsilon$". One could show that the rational numbers are a [[uniform space]] with respect to the [[uniformity]] [[ternary relation]] $x \sim_\epsilon y$. 

1. For every $x \in \mathbb{Q}$ and $\epsilon \in \mathbb{Q}_+$, $x \sim_\epsilon x$

2. For every $x \in \mathbb{Q}$, $y \in \mathbb{Q}$, $z \in \mathbb{Q}$ and $\delta \in \mathbb{Q}_+$, $\epsilon \in \mathbb{Q}_+$, $x \sim_\delta y$ and $y \sim_\epsilon z$ implies that $x \sim_{\delta + \epsilon} z$. 

3. For every $x \in \mathbb{Q}$, $y \in \mathbb{Q}$ and $\epsilon \in \mathbb{Q}_+$, $x \sim_\epsilon y$ implies that $y \sim_\epsilon x$. 

4. For every $x \in \mathbb{Q}$, $y \in \mathbb{Q}$, $x \sim_1 y$ if and only if $\rho(x, y) \lt 1$. 

5. For every $x \in \mathbb{Q}$, $y \in \mathbb{Q}$ and $\delta \in \mathbb{Q}_+$, $\epsilon \in \mathbb{Q}_+$, $x \sim_{\min(\delta, \epsilon)} y$ implies that $x \sim_{\delta} y$ and $x \sim_{\epsilon} y$. 

6. For every $x \in \mathbb{Q}$, $y \in \mathbb{Q}$ and $\delta \in \mathbb{Q}_+$, $\epsilon \in \mathbb{Q}_+$, $\delta \leq \epsilon$ and $x \sim_{\delta} y$ implies that $x \sim_{\epsilon} y$. 

### Algebraic closure

The [[algebraic closure]] $\overline{\mathbb{Q}}$ of the rational numbers is called the [[field]] of _[[algebraic numbers]]_. The [[absolute Galois group]] $Gal(\overline{\mathbb{Q}}\vert \mathbb{Q})$ has some curious properties, see [there](absolute+Galois+group#OfTheRationalNumbers).

### Topologies

There are several interesting [[topological space|topologies]] on $\mathbb{Q}$ that make $\mathbb{Q}$ into a [[topological group]] under addition, allowing us to define interesting fields by taking the [[complete space|completion]] with respect to this topology:

1.  The _[[discrete topology]]_ is the most obvious, which is already complete.

2.  The _absolute-value topology_ is defined by the [[metric space|metric]] $d(x,y) \coloneqq {|x - y|}$; the completion is the field of [[real numbers]]. The rational numbers are thus a [[Hausdorff space]].

    (This topology is [[totally disconnected space|totally disconnected]] ([this exmpl.](totally+disconnected+space#RationalNumbersAreTotallyDisconnected)))

3.  Fixing a [[prime number]] $p$, the _$p$-adic topology_ is defined by the [[ultrametric]] $d(x,y) \coloneqq 1/n$ where $n$ is the highest exponent on $p$ in the [[prime factorization]] of ${|x - y|}$; the completion is the field of $p$-[[adic number|adic numbers]].

According to [[Ostrowski's theorem]] this are the only possibilities.

Interestingly, (2) cannot be interpreted as a [[locale|localic]] group, although the completion $\mathbb{R}$ can.  (Probably the same holds for (3); I need to check.)

### Analysis 

One could analytically define the concepts of [[limit of a function]] and [[continuous function]] with respect to the absolute-value topology, and prove that the limit of a function satisfy the [[algebraic limit theorem]]. Since the [[reciprocal function]] on the rational numbers is well defined for non-zero rational numbers $\mathbb{Q}_{\neq 0}$, given a continuous function $f:I \to \mathbb{Q}$ for open interval $I \subseteq \mathbb{Q}$ the [[difference quotient]] function exists and thus the [[derivative]] is well-defined for continuous functions. One could thus define [[smooth functions]] on the rational numbers, and because the rational numbers are a Hausdorff space, [[analytic functions]] on the rational numbers, despite the fact that the rational numbers are a totally disconnected space. 

For example, 

* A rational metric space is a type $X$ with a function $d_X:X \times X \to \mathbb{Q}_{\geq 0}$ such that 

  * for all $x \in X$ and $y \in X$, $d_X(x, y) = d_X(y, x)$
  * for all $x \in X$, $y \in X$, and $z \in X$, $d_X(x, z) \leq d_X(x, y) + d_X(y, z)$
  * for all $x \in X$, $x = y \iff d_X(x, y) = 0$

One could show that any [[open interval]], [[half-open interval]], and [[closed interval]] in the rational numbers is a rational metric space, with its metric inherited from the Euclidean metric on the rational numbers $d_\mathbb{Q}(x, y) = {|a - b|}$. Thus one could do analysis with [[partial functions]] in the [[rational numbers]], such as the [[reciprocal function]] $x \mapsto \frac{1}{x}$ and the [[rational functions]] on the rational numbers. 

Then, given a rational metric space $(X, d_X)$:

* if it exists, the (Weierstrass) [[limit of a function]] $f:X \to \mathbb{Q}$ from $X$ to the rational numbers approaching an element $a \in X$ is a rational number $L \in \mathbb{Q}$ with a function on the positive rational numbers $M:\mathbb{Q}_+ \to \mathbb{Q}_+$ such that for all positive rational numbers $\epsilon \in \mathbb{Q}_+$ and for all elements $b \in X$, $0 \lt d_X(a, b) \lt M(\epsilon)$ implies ${|f(b) - L|} \lt \epsilon$

* similarly, if it exists, the (Bourbaki) [[limit of a function]] $f:X \to \mathbb{Q}$ from $X$ to the rational numbers approaching an element $a \in X$ is a rational number $L \in \mathbb{Q}$ with a function on the positive rational numbers $M:\mathbb{Q}_+ \to \mathbb{Q}_+$ such that for all positive rational numbers $\epsilon \in \mathbb{Q}_+$ and for all elements $b \in X$, $d_X(a, b) \lt M(\epsilon)$ implies ${|f(b) - L|} \lt \epsilon$

* a [[pointwise continuous function]] from $X$ to the rational numbers is a function $f:X \to \mathbb{Q}$ with a function from $X$ to the set of endofunctions on the positive rational numbers $M:X \to \mathbb{Q}_+ \to \mathbb{Q}_+$ such that for all positive rational numbers $\epsilon \in \mathbb{Q}_+$ and for all rational numbers $a \in X$ and $b \in X$, $\delta_X(a, b) \lt M(a, \epsilon)$ implies that ${|f(a) - f(b)|} \lt \epsilon$. 

* a [[uniformly continuous function]] from $X$ to the rational numbers is a function $f:X \to \mathbb{Q}$ with a function on the positive rational numbers $M:\mathbb{Q}_+ \to \mathbb{Q}_+$ such that for all positive rational numbers $\epsilon \in \mathbb{Q}_+$ and for all elements numbers $a \in X$ and $b \in X$, $\delta_X(a, b) \lt M(\epsilon)$ implies that ${|f(a) - f(b)|} \lt \epsilon$. 

Now, given an [[injection]] $i:X \hookrightarrow \mathbb{Q}$, so that $X$ is a [[subset]] of the rational numbers,

* a [[pointwise differentiable function]] from $X$ to the rational numbers is a function $f:X \to \mathbb{Q}$ with a [[derivative]] function $f':X \to \mathbb{Q}$ on the rational numbers and a function from $X$ to the set of endofunctions on the positive rational numbers $M:X \to \mathbb{Q}_+ \to \mathbb{Q}_+$ such that for all positive rational numbers $\epsilon \in \mathrm{Q}_+$ and for all elements $a \in X$ and $b \in X$, ${|f(a) - f(b)|} \lt M(a, \epsilon)$ implies that 
$${|f(b) - f(a) - f'(a)(i(b) - i(a)))|} \lt \epsilon {|f(a) - f(b)|}$$

* a [[uniformly differentiable function]] from $X$ to the rational numbers is a function $f:X \to \mathbb{Q}$ with a [[derivative]] function $f':X \to \mathbb{Q}$ on the rational numbers and a function on the positive rational numbers $M:\mathbb{Q}_+ \to \mathbb{Q}_+$ such that for all positive rational numbers $\epsilon \in \mathrm{Q}_+$ and for all elements $a \in X$ and $b \in X$, ${|f(a) - f(b)|} \lt M(\epsilon)$ implies that 
$${|f(b) - f(a) - f'(a)(i(b) - i(a)))|} \lt \epsilon {|f(a) - f(b)|}$$

* a [[smooth function]] in rational numbers is a function $f:\mathbb{Q} \to \mathbb{Q}$ with a [[sequence]] of functions $D^{(-)}f:\mathbb{N} \to (\mathbb{Q} \to \mathbb{Q})$ and a sequence of functions $M^{(-)}f:\mathbb{N} \to (\mathbb{Q}_+ \to \mathbb{Q}_+)$ in the positive rational numbers, such that 

  * for every element $x \in X$, $(D^{0}f)(x) = f(x)$

  * for every natural number $n \in \mathbb{N}$, for every positive rational number $\epsilon \in \mathbb{Q}_+$, for every rational number $h \in \mathbb{Q}$ such that $0 \lt | h | \lt M^{n}f(\epsilon)$, and for every rational number $x \in \mathbb{Q}$, 
$$\left|f(x + h) - \sum_{i=0}^n \frac{h^i (D^{i}f)(x)}{i!}\right| \lt \epsilon |h^n|$$

Alternatively, we could use [[infinitesimals]]. Let $\mathbb{Q}[\epsilon]/(\epsilon^2 = 0)$ be the dual rational numbers, and let $\mathbb{Q}[[\epsilon]]$ be the commutative ring of [[formal power series]] on the rational numbers. The former is equivalent to the product $\mathbb{Q} \times \mathbb{Q}$ and the latter is equivalent to the [[function set]] $\mathbb{Q}^\mathbb{N}$. 

Both of these are commutative [[rational algebras]] with ring homomorphism $h:\mathbb{Q} \to \mathbb{Q}[\epsilon]/(\epsilon^2 = 0)$ and $k:\mathbb{Q} \to \mathbb{Q}[[\epsilon]]$. 

* A function $f:X \to \mathbb{Q}$ is **differentiable** if it has a function $\mathrm{lift}_f:\mathbb{Q}[\epsilon]/(\epsilon^2 = 0) \to \mathbb{Q}[\epsilon]/(\epsilon^2 = 0)$ such that $\mathrm{lift}_f(h(i(a))) = h(i(a))$ and a function $f':X \to \mathbb{Q}$ such that for all elements $a \in X$,

$$\mathrm{lift}_f(h(i(a)) + \epsilon) = h(i(a)) + h(f'(a)) \epsilon$$ 

* A function $f:X \to \mathbb{Q}$ is **smooth** if it has a function $\mathrm{lift}_f:\mathbb{Q}[[\epsilon]] \to \mathbb{Q}[[\epsilon]]$ such that $\mathrm{lift}_f(h(i(a))) = h(i(a))$ and a sequence of functions $\frac{d^{-} f}{d x^{-}}:\mathbb{N} \times X \to \mathbb{Q}$ with $\frac{d^0 f}{d x^0}\left(a\right) = a$ for all $a \in X$, such that for all natural numbers $n \in \mathbb{N}$
$$\mathrm{lift}_f(h(j(a)) + \epsilon) = \sum_{i = 0}^{\infty} \frac{1}{i!} h\left(\frac{d^i f}{d x^i}\left(a\right)\right) \epsilon^i$$ 

## Related concepts

* [[natural number]]

* [[integer]]

* **rational number**

  * a finite [[field extension]] of $\mathbb{Q}$ is called a _[[number field]]_

  * [[dyadic rational number]]

  * [[decimal rational number]]

* [[Q/Z]]
   
* [[algebraic number]]

* [[Gaussian number]]

* [[irrational number]]

* [[quadratic irrational number]]

* [[real number]]

* [[p-adic number]]

* [[rational numbers object]]

* [[rational interval coalgebra]]

* [[rational root theorem]]

## References

* [[Leo Corry]], *A Brief History of Numbers*, Oxford University Press (2015) &lbrack;[ISBN:9780198702597](https://global.oup.com/academic/product/a-brief-history-of-numbers-9780198702597)&rbrack;

See also:

* Wikipedia, *[Rational number](https://en.wikipedia.org/wiki/Rational_number)*

Discussion in [[univalent foundations of mathematics]] ([[homotopy type theory]] with the [[univalence axiom]]):

* {#UBP13} [[Univalent Foundations Project]], §11.1 of: *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

and specifically in [[Agda]]:

* [[UniMath project]], *[agda-unimath/elementary-number-theory.rational-numbers](https://unimath.github.io/agda-unimath/elementary-number-theory.rational-numbers.html)*



[[!redirects rational number]]
[[!redirects rational numbers]]
[[!redirects field of rational numbers]]
[[!redirects rationals]]