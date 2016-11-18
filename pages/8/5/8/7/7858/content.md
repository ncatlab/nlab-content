#Contents#
* table of contents
{:toc}

## Idea

The classical _M&#246;bius inversion formula_ is a principle originating in [[number theory]], which says that if $f$ and $g$ are two (say, [[complex]]-valued) functions on the positive [[natural numbers]], then
$$f(n) = \sum_{d\mid n} g(d)$$
if and only if
$$g(n) = \sum_{d\mid n} f(d)\mu(n/d)$$
where the sums run over the divisors of $n$, and where $\mu$ is the _M&#246;bius function_:
$$
\mu(n) = \begin{cases}(-1)^r & n\,\text{is the product of}\,r\,\text{distinct primes}\\0 & \text{otherwise}\end{cases}
$$
[[Gian-Carlo Rota]] [(1964)](#Rota64) described a vast generalization of the M&#246;bius inversion formula, which was at the same time a generalization of the classical [[inclusion-exclusion]] principle in [[combinatorics]]. Rota's formulation of M&#246;bius inversion applies to functions defined over [[partially ordered sets]], while further category-theoretic generalizations have also been proposed.

## M&#246;bius inversion for posets

### Incidence algebras and the zeta function

The **incidence algebra** of a poset $P$ (relative to a [[ring]] $R$) is defined as follows.
Its elements are functions $f : P \times P\to R$ such that $x \nleq y$ implies $f(x,y) = 0$.
Pointwise addition $f+g$ and scalar multiplication $r\cdot f$ are defined in the obvious way, while the _convolution product_ $f*g$ is defined as follows:
$$(f*g)(x,y) = \sum_{x \le z \le y} f(x,z) \cdot g(z,y)$$
Note that the unit of the convolution product is the [[Kronecker delta]]:
$$\delta(x,y) = \begin{cases}1 & x = y \\ 0 & \text{otherwise}\end{cases}$$
A special element of the incidence algebra is given by
$$\zeta(x,y) = \begin{cases}1 & x \le y \\ 0 & \text{otherwise}\end{cases}$$
referred to as the **zeta function** of $P$.

### The M&#246;bius function and the M&#246;bius inversion formula

A **M&#246;bius function** of $P$ is defined as an inverse to the zeta function with respect to the convolution product. Such an inverse always exists if the poset is [[locally finite poset|locally finite]], that is, if every [[interval]] $[x,y] = \{z \mid x \le z\le y\}$ is finite.

+-- {: .num_prop }
###### Proposition

[(Rota 1964)](#Rota64):
If $P$ is a locally finite poset, then there exists a function $\mu$ such that $\zeta * \mu = \mu * \zeta = \delta$.

=--

+-- {: .proof} 
###### Proof

$\mu(x,y)$ can be computed by induction on the number of elements in the interval $[x,y]$. In the base case we set $\mu(x,x) = 1$. Otherwise in the case that $x \ne y$, we assume by induction that $\mu(x,z)$ has already been defined for all $z$ in the half-open interval $[x,y)$, and set
$$
\mu(x,y) = -\sum_{x \le z \lt y} \mu(x,z).
$$
From this definition, it is immediate that if
$$x_0 \lt x_1 \lt \cdots \lt x_n$$
is a chain of length $n$ in $P$, where each $x_{i+1}$ [[covering relation|covers]] $x_i$, then for all $i \leq j$,
$$
\mu(x_i,x_j) = \begin{cases}1 & i = j \\ -1 & j - i = 1\\ 0 & j - i \ge 2\end{cases}
$$
It follows that both of the sums
$\sum_{x \le z \le y} \mu(x,z)$ and $\sum_{x \le z \le y} \mu(z,y)$
add to zero unless $x = y$, hence that $\zeta*\mu = \mu*\zeta = \delta$.

=--

We are now ready to state the M&#246;bius inversion formula for posets.

+-- {: .num_prop }
###### Proposition

[(Rota 1964)](#Rota64):
Let $f$ and $g$ be functions defined over a locally finite poset $P$. Then
$$f(y) = \sum_{x \le y} g(x)$$
if and only if
$$g(y) = \sum_{x \le y} f(x)\mu(x,y)$$

=--

+-- {: .proof} 
###### Proof

An easy way of proving the M&#246;bius inversion formula [(Kung et al.)](#KungRotaYan) is to view $\zeta$ and $\mu$ as matrices acting on the column vectors $f$ and $g$ by multiplication. Then the proposition simply says that $f = g * \zeta$ iff $f * \mu = g$. (There is also a dual formulation, corresponding to the statement that $f = \zeta * g$ iff $\mu * f = g$.)

=--

## Properties of the M&#246;bius function

### For product orders

The M&#246;bius function of the [[cartesian product]] $P \times Q$ of two posets $P$ and $Q$ is the product of their M&#246;bius functions:
$$\mu_{P\times Q}((p,q), (p',q')) = \mu_P(p,p') \cdot \mu_Q(q,q')$$
for all $p,p' \in P$ and $q,q' \in Q$.

## Examples of M&#246;bius inversion

### Inclusion-exclusion

Let $\mathcal{P}X$ be the lattice of subsets of a finite set $X$. $\mathcal{P}X$ is isomorphic to the cartesian product of $|X|$ many copies of the 1-chain $[1] = \{ 0 \lt 1 \}$, and so by the product rule for the M&#246;bius function, we have
$$\mu(I,J) = (-1)^{|J|-|I|}$$
for any pair of subsets $I,J \subseteq X$ such that $I \subseteq J$. The M&#246;bius inversion formula then says that for any functions $f$ and $g$ defined on $\mathcal{P}X$, we have
$$f(J) = \sum_{I \subseteq J} g(I)$$
if and only if
$$g(J) = \sum_{I \subseteq J} (-1)^{|J|-|I|} f(I)$$
This is called the _inclusion-exclusion_ principle.


## M&#246;bius inversion for categories

## Related concepts

* [[Euler characteristic]]
* [[incidence algebra]]
* [[inclusion-exclusion]]
* [[zeta polynomial]]

## References

The classical reference on M&#246;bius inversion for posets is:

* [[Gian-Carlo Rota]], _On the foundations of combinatorial theory I: theory of M&#246;bius functions_ , Z. Wahrscheinlichkeitstheorie und Verw. Gebiete 2 (1964), 340&#8211;368.
 {#Rota64}

and a more modern reference is:

* Joseph P. S. Kung, [[Gian-Carlo Rota]], Catherine H. Yan. Combinatorics: The Rota Way. Cambridge, 2009.
 {#KungRotaYan}

M&#246;bius inversion for categories is discussed in:

* Tom Leinster, _Notions of M&#246;bius inversion_, Bulletin of the Belgian Mathematical Society 19 (2012) 911-935, [arXiv:1201.0413v3](http://arxiv.org/abs/1201.0413)

* $n$Cafe: [M&#246;bius inversion for categories](http://golem.ph.utexas.edu/category/2011/05/mbius_inversion_for_categories.html)

Other references include:

* Joachim Kock, _Incidence Hopf algebras_, [pdf](http://mat.uab.es/~kock/seminars/incidence-algebras.pdf)

* Imma G&#225;lvez-Carrillo, Joachim Kock, Andrew Tonks, _Decomposition spaces, incidence algebras and M&#246;bius inversion_, [arxiv/1404.3202](http://arxiv.org/abs/1404.3202)

* Metropolis, N.; Rota, Gian-Carlo, _Witt vectors and the algebra of necklaces_, Advances in Mathematics __50__ (2): 95&#8211;125 (1983) [doi](http://dx.doi.org/10.1016%2F0001-8708%2883%2990035-X)

* wikipedia [M&#246;bius function](http://en.wikipedia.org/wiki/M%C3%B6bius_function), [necklace polynomial](http://en.wikipedia.org/wiki/Moreau%27s_necklace-counting_function)


[[!redirects Mobius inversion]]
[[!redirects Möbius function]]
[[!redirects Moebius function]]
[[!redirects Moebius inversion]]
[[!redirects necklace polynomial]]