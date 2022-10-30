
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Fr&#233;chet spaces
* table of contents
{: toc}

## Idea

Fr&#233;chet spaces are particularly well-behaved [[topological vector spaces]] (TVSes).  Every [[Cartesian space]] is a Fr&#233;chet space, but Fr&#233;chet spaces may have infinite [[dimension]].  There is [[analysis]] on Fr&#233;chet spaces, yet they are more general than [[Banach spaces]]; as such, they are popular as test spaces for possibly [[infinite-dimensional manifolds]]: _[[Fréchet manifolds]]_.

Note that a 'Fr&#233;chet topology' on a 'Fr&#233;chet topological space' is different; this just means that a [[topological space]] satisfies the $T_1$ [[separation axiom]].  (Like all Hausdorff TVSes, Fr&#233;chet spaces satisfy this axiom, but they have a good deal of additional structure and properties.)


## Definition

A __Fr&#233;chet space__ is a [[complete space|complete]] [[Hausdorff space|Hausdorff]] [[locally convex space]] that is [[metric space|metrisable]].  The metric can be chosen to be translation-invariant.

Equivalently, a __Fr&#233;chet space__ is a complete Hausdorff TVS whose topology may be given (as a [[gauge space]]) by a [[countable set|countable]] family of [[seminormed vector space|seminorms]].

We accept as an [[automorphism]] of Fr&#233;chet spaces any [[llinear map|linear]] [[homeomorphism]]; in particular, the particular translation-invariant metric or countable family of seminorms used to prove that a space is a Fr&#233;chet space is *not* required to be preserved.  More generally, the [[morphisms]] of Fr&#233;chet spaces are the [[continuous map|continuous]] linear maps, so that Fr&#233;chet spaces form a [[full subcategory]] of $TVS$.


## Examples

Every [[Banach space]] is a Fr&#233;chet space.

If $X$ is a [[compact space|compact]] [[smooth manifold]], then the space of [[smooth map|smooth maps]] on $X$ is a Fr&#233;chet space.  This can be extended to some non-compact manifolds, in particular when $X$ is the [[real line]].

The [[Lebesgue space]] $L^p(\mathbb{R})$ for $p \lt 1$ is *not* a Fr&#233;chet space, because it is not locally convex.

The direct product of a countable number of copies of $\mathbb{R}$ is a Fr&#233;chet space.  Let $\pi_n \colon \prod_k \mathbb{R} \to \mathbb{R}^n$ be the projection onto the first $n$ copies and let $\|\cdot\|_n$ be a choice of norm on $\mathbb{R}^n$.  Then a countable family of seminorms on $\prod_k \mathbb{R}$ is given by $v \mapsto {\|\pi_n(v)\|_n}$.

On the other hand, the locally convex direct sum of a countable number of copies of $\mathbb{R}$ is not a Fr&#233;chet space.

## Properties
Fr&#233;chet spaces are [[barrelled]] and [[bornological]]. 

The dual of a Fr&#233;chet space $F$ is a Fr&#233;chet space iff $F$ is a [[Banach space]].

Reference: This follows from the statement paragraph 29.1 (7) in Gottfried Koethe: _Topological Vector Spaces I_, which is: The strong dual of a locally convex metrizable TVS $F$ is metrizable iff $F$ is normable.

## Calculus
It is possible to generalize some aspects of calculus to Fr&#233;chet spaces, for example the definition of the derivative of a curve is simply the same as in finite dimensions:


+-- {: .un_defn}
###### Definition
For a continuous path in a Fr&#233;chet space $f(t)$ we define
$$
f'(t) = \lim_{h \to 0} \frac{1}{h} (f(t + h) - f(t))
$$
If the limit exists and is continous, we say that $f$ is continuously differentiably or $C^1$.
=--

And just as in the finite dimensional case, we can define the partial derivative, or rather: the [[directional derivative|directional]] or G&#226;teaux derivative:

+-- {: .un_defn}
###### Definition
**directional derivative**

Let F and G be Fr&#233;chet spaces, $U \subseteq F$ open and $P: U \to G$ a nonlinear continuous map. The derivative of $P$ at the point $f \in U$ in the direction $h \in F$ is the map
$$
D P: U \times F \to G
$$
$$
D P(f) h = \lim_{t \to 0} \frac{1}{t} ( P(f + t h) - P(f))
$$
If the limit exists and is jointly continuous in both variables we say that $P$ is continuous differentiable or $C^1$.
=--

A simple, but nontrivial example is the operator 
$$
P: C^{\infty}[a, b] \to C^{\infty}[a, b]
$$
$$
P(f) \coloneqq f f'
$$
with the derivative
$$
D P(f) h = f'h + f h'
$$

It is possible to generalize the Riemann integral to Fr&#233;chet spaces, too: For a continuous path $f(t)$ on an interval $[a, b]$ in a Fr&#233;chet space $F$ we look for an element $\int_a^b f(t) d t \in F$. It turns out that such an element exists and is unique, if we impose some properties of the integral known from the finite dimensional case:


+-- {: .un_theorem}
###### Theorem
There exists a unique element $\int_a^b f(t) d t \in F$ such that

(i) for every continuous functional $\phi$ we have  $\phi(\int_a^b f(t) d t) = \int_a^b \phi(f(t)) d t$,

(ii) for every continuous seminorm ${\| \cdot \|}$ we have ${\| \int_a^b f(t) d t \|} \leq \int_a^b {\| f(t) \|} d t$

(iii) integration is linear and 

(iv) additive, i.e. $ \int_a^b f(t) d t + \int_b^c f(t) d t = \int_a^c f(t) d t $

=--

There is a version of the fundamental theorem of calculus:


+-- {: .un_theorem}
###### Theorem
If P is $C^1$ and $f + t h \in Domain(P)$ for $0 \leq t \leq 1$, then 
$$
P(f + h) - P(f) = \int_0^1 D P(f + t h) \;h \; d t
$$

=--

The chain rule is valid:

+-- {: .un_theorem}
###### Theorem
If P and Q are $C^1$ then so is their composition $Q \circ P$ and
$$
D [Q \circ P](f) h = D Q(P(f)) \; D P(f) \; h
$$
=--

The first derivative $D P$ is a function of two variables, the base point $f$ and the direction $h$. Since $D P$ is already linear in $h$, we define the second derivative with respect to $f$ only:

+-- {: .un_defn}
###### Definition
**second derivative**
The second derivative of $P$ in the direction $k$ is defined to be
$$
D^2 P(f) (h, k) = \lim_{t \to 0} \frac{1}{t} (D P(f + t k) h - D P(f) h)
$$
=--
It is a theorem that the second derivative, if it exists and is jointly continuous, is bilinear in $(h ,k)$.

We can iterate this procedure to define derivatives of arbitrary order, and thus the notion of **smooth functions between Fr&#233;chet spaces**.

## References

* [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Fr&#233;chet_space)

Calculus on Fr&#233;chet spaces is nicely explained in this paper:

* Richard S. Hamilton: _The Inverse Function Theorem of Nash and Moser_ (Bulletin (New Series) of the American Mathematical Society Volume 7, Number 1, July 1982)

Refinement to [[noncommutative geometry]] by suitable smoothed [[C-star-algebras]] is discussed in 

* Nikolay Ivankov, _Unbounded bivariant K-theory and an Approach to Noncommutative Fr&#233;chet spaces_ [pdf](http://hss.ulb.uni-bonn.de/2011/2624/2624.pdf)

[[!redirects Frechet space]]
[[!redirects Frechet spaces]]
[[!redirects Fréchet space]]
[[!redirects Fréchet spaces]]