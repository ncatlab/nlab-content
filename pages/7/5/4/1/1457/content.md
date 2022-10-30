
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A **metric space** is a [[set]] which comes equipped with a [[function]] which measures _distance_ between points, called a _metric_. The metric may be used to generate a [[topology]] on the set, the _[[metric topology]]_, and a [[topological space]] whose topology comes from some metric is said to be _[[metrizable]]_. 


## Definitions

Traditionally, a __metric space__ is defined to be a [[set]] $X$ equipped with a __distance__ [[function]] 
$$ d\colon X \times X \to [0, \infty) $$ 
(valued in [[nonnegative number|non-negative]] [[real numbers]]) satisfying the following axioms: 

* [[triangle inequality|Triangle inequality]]: $d(x, y) + d(y, z) \geq d(x, z)$;

* Point inequality: $0 \geq d(x, x)$ (so $0 = d(x,x)$);

* Separation: $x = y$ if $d(x, y) = 0$ (so $x = y$ iff $d(x,y) = 0$);

* Symmetry: $d(x, y) = d(y, x)$.

Given a metric space $(X, d)$ and a point $x \in X$, the __[[open ball]]__ centered at $x$ of radius $r$ is  
$$ 
  B_r(x) \coloneqq \{y \in X : d(x, y) \lt r\}
$$ 
and it may be shown that the open balls form a [[basis for a topology|basis]] for a [[topological structure|topology]] on $X$, the _[[metric topology]]_. In fact, metric spaces are examples of [[uniform spaces]], and much of the general theory of metric spaces, including for example the notion of [[complete space|completion]] of a metric space, can be extrapolated to uniform spaces and even [[Cauchy spaces]].

### As a Richman premetric space

In [[constructive mathematics]], a **metric space** is a [[Richman premetric space]] $(X, \sim)$ such that for all non-negative rational numbers $q \in \mathbb{Q}_{\geq 0}$, and $r \in \mathbb{Q}_{\geq 0}$, if $q \lt r$, than for every $x \in X$ and $y \in X$, either $x \sim_r y$ or $\neg(x \sim_q y)$. Classically, every Richman premetric space is a metric space, but constructively, Richman premetric spaces are only "metric spaces" that are valued in the lower Dedekind real numbers. 

### Metrizable spaces

A **[[metrizable topological space]]** is a [[topological space]] $X$ which admits a metric such that the  [[metric topology]] agrees with the topology on $X$. In general, many different metrics (even ones giving different [[uniform space|uniform structures]]) may give rise to the same topology; nevertheless, metrizability is manifestly a topological notion. 

Metrizable spaces enjoy a number of separation properties: they are [[Hausdorff space|Hausdorff]], [[regular space|regular]], and even [[normal space|normal]]. They are also [[paracompact space|paracompact]]. 

Metrizable spaces are closed under topological [[coproducts]] and of course [[subspaces]] (and therefore [[equalizers]]); they are closed under [[countable family|countable]] [[products]] but not general products (for instance, a product of uncountably many copies of the [[real line]] $\mathbb{R}$ is not a normal space). 

Fundamental early work in point-set topology established a number of metrization theorems, i.e., theorems which give sufficient conditions for a space to be metrizable. One of the more useful theorems is due to [[Urysohn]]: 

+-- {: .num_theorem} 
###### Theorem 
**(Urysohn metrization)** 
A [[separation axiom|regular, Hausdorff]] [[second-countable space]] is metrizable. 
=-- 

So, for instance, a compact Hausdorff space that is second-countable is metrizable. 

+-- {: .num_remark} 
###### Remark 
A compact Hausdorff space that is merely [[separable space|separable]] need not be metrizable; one example is the [[Stone-Cech compactification]] $\beta(\mathbb{N})$, in which $\mathbb{N}$ is dense but no non-principal [[ultrafilter]] $U$ is the limit of a sequence $X = \{x_n\} \subseteq \mathbb{N}$ of principal ultrafilters. (Supposing it were, choose complementary subsets $A, B \subseteq \mathbb{N}$ such that $A \cap X$ and $B \cap X$ are infinite. By the decomposition $\beta(\mathbb{N}) = \beta(A + B) = \beta(A) + \beta(B)$, we have $U$ belonging to exactly one of $\beta(A), \beta(B)$, say $\beta(B)$. But since the subsequence $A \cap X$ converges to $U$, the basic open neighborhood $\beta(B) = \{V \in \beta(\mathbb{N}): B \in V\}$ of $U$ intersects $A \cap X$ non-trivially, i.e., $B$ is contained in some principal ultrafilter $prin(a)$ with $a \in A \cap X$. Then $a$ lies in disjoint sets $B$ and $A \cap X$, contradiction.) 
=-- 


### Variations 

If we allow $d$ to take values in $[0,\infty]$ (the nonnegative [[lower reals]]) instead of just in $[0,\infty)$, then we get __extended metric spaces__.  If we drop separation, then we get __pseudometric spaces__.  If we drop the symmetry condition, then we get __quasimetric spaces__.  Thus the most general notion is that of an extended quasipseudometric space, which are also called __Lawvere metric spaces__ for the reasons below.

{#LawvereMetricSpacesDefinition}On the other hand, if we strengthen the [[triangle inequality]] to
$$ max(d(x,y), d(y,z)) \geq d(x,z) ,$$
then we get __ultrametric spaces__, a more restricted concept.  (This include for example $p$-[[adic completion]]s of [[number fields]].)  Extended quasipseudoultrametric spaces can also be called __Lawvere ultrametric spaces__.

### Metrics valued in another Archimedean integral domain

In some cases, we might want our [[codomain]] of our metric to take values in values other than the real numbers $\mathbb{R}$. This is already important in the definition of the real numbers as [[modulated Cauchy real numbers]], where the metric used is valued in the [[non-negative number|non-negative]] [[rational numbers]] $\mathbb{Q}_{\geq 0}$. 

This becomes even more essential in [[constructive mathematics]]: while in [[classical mathematics]], the [[modulated Cauchy real numbers]] are equivalent to the [[Dedekind real numbers]], in [[constructive mathematics]], those definitions are inequivalent to the [[Dedekind real numbers]], and so there are multiple sets of real numbers in which a metric could be valued in. 

In [[predicative mathematics]], the issue becomes even worse: there is no longer one set of Dedekind real numbers, but a whole hierarchy of Dedekind real numbers, one set for every [[universe]] in the [[foundations of mathematics|foundations]]. As a result, one cannot resort to merely using the [[Dedekind real numbers]] for defining the metric as in impredicative mathematics, one has to define metrics and metric spaces more generally. 

Thus, given an [[Archimedean integral domain]] $R$, an **$R$-metric** on a set $X$ is a function $d:X \times X \to R_{\geq 0}$, where $R_{\geq 0}$ is the set of non-negative elements in $R$, such that 

* [[triangle inequality|Triangle inequality]]: $d(x, y) + d(y, z) \geq d(x, z)$;

* Point inequality: $0 \geq d(x, x)$ (so $0 = d(x,x)$);

* Separation: $x = y$ if $d(x, y) = 0$ (so $x = y$ iff $d(x,y) = 0$);

* Symmetry: $d(x, y) = d(y, x)$.

This is equivalently an $(R_{\geq 0}, \geq, +, 0)$-[[enriched set]]. 

Given any [[Archimedean integral domain]] $R$ and an Archimedean integral subdomain $S \subseteq R$, then $S$ is an $(R_{\geq 0}, \geq, +, 0)$-enriched set. 

### In homotopy type theory

In [[homotopy type theory]], metric and pseudometric spaces could be defined as any [[type]], not just 0-truncated types. Let $\mathbb{R}$ be some suitable notion of real number, and 
$$\mathbb{R}_{\geq 0} \coloneqq \sum_{a:\mathbb{R}} a \geq 0$$ 
be the non-negative real numbers. 

\begin{definition}
A **pseudometric space** is a type $X$ with a function $d:X \times X \to \mathbb{R}_{\geq 0}$, which comes with  witnesses for symmetry, the triangle identity, and the identity-to-zero-distance condition:
$$\mathrm{sym}(x, y):d(x, y) = d(y, x)$$
$$\mathrm{triangle}(x, y, z):d(x, z) \leq d(x, y) + d(y, z)$$
$$\mathrm{idtozerodis}(x, y):(x = y) \to (d(x, y) = 0)$$
\end{definition}

The last axiom is equivalent to the point inequality axiom 
$$\mathrm{ptineq}(x):d(x, x) = 0$$ 
by the induction principle of [[identity types]]. Every pseudometric can be shown to have an [[equivalence relation]]  
$$x \sim y \coloneqq d(x, y) = 0$$ 
through the axioms of a pseudometric space. 

In set theory, the separation axiom is usually defined as the converse of the identity-to-zero-distance axiom. However, in type theory, since not all identity types are propositions, merely postulating a function 
$$\mathrm{sepax}(x, y):(d(x, y) = 0) \to (x = y)$$
does not result in a metric space, since there might be many such functions into the identity type $x = y$. Instead, one must strengthen the condition to a [[Rezk completion|Rezk completeness]] condition for pseudometric spaces, similar to the type-theoretic antisymmetry condition in [[posets]] from [[preorder|preordered types]]: 

\begin{definition}
A pseudometric space is a **metric space** if the axiom 
$$\mathrm{idtozerodis}(x, y):(x = y) \to (d(x, y) = 0)$$
is an [[equivalence in homotopy type theory|equivalence of types]]. 
\end{definition}

Since any type of non-negative real numbers is a set, the Rezk completeness condition automatically implies that every metric space is a set. 

### Category of metric spaces

When working with metric spaces one encounters a broad variety of different maps including non-[[continuous map|continuous]] ones like almost isometries. For a convenient categorical set-up one often restricts to __[[short map|short maps]]__, i.e. maps that do not increase any distance or, equivalently, have are of [[Lipschitz map|Lipschitz norm]] not greater than 1. The category of Lawvere metric spaces and short maps forms the [[category of metric spaces]] $Met$. The restriction to ordinary metric spaces is denoted by $Met_{ord}$.


## Lawvere metric spaces 
  {#LawvereMetricSpace}

In [Lawvere, 73](#Lawvere73), it was pointed out that [Lawvere metric spaces](#LawvereMetricSpacesDefinition) are precisely [[enriched category|categories enriched]] in the [[monoidal category|monoidal]] [[partial order|poset]] $([0, \infty], \geq)$, where the [[tensor product]] is taken to be addition.  The [[composition]] operation in this enriched category identifies with the [[triangle identity]] in the metric space (see at _[triangle inequality -- Interpretation in enriched category theory](triangle+inequality#InterpretationInEnrichedCategoryTheory)_).

Alternatively, taking the monoidal product to be [[supremum]] instead, enriched categories amount to Lawvere ultrametric spaces.

Thus generalized, many constructions and results on metric spaces turn out to be special cases of yet more general constructions and results of [[enriched category theory]].  This includes for example the notion of [[Cauchy complete category|Cauchy completion]], which in general enriched category theory is related to [[Karoubi envelope|Karoubi envelopes]] and [[Morita equivalence]].

Imposing the symmetry axiom then gives us enriched $\dagger$-[[dagger category|categories]].  Note that when enriching over a [[cartesian monoidal category|cartesian monoidal]] poset, there is no difference between a $\dagger$-category and a [[groupoid]], so ultrametric spaces can also be regarded as [[enriched groupoid|enriched groupoids]], which is perhaps a more familiar concept.

(The requisite axioms for an enriched groupoid do not make sense when the enriching category is not cartesian, but one might argue that since in a poset "they would commute automatically anyway", it makes sense to call any poset-enriched $\dagger$-category also an "enriched groupoid".  However, perhaps it makes more sense just to speak about enriched $\dagger$-categories.)

In the presence of the symmetry axiom, the "separation" axiom "$x=y$ if $d(x,y)=0$" is equivalent to [[skeletal category|skeletality]] of an enriched category.  That is, a pseudo-metric space is a metric space precisely when it is skeletal.  But in the non-symmetric case, this separation axiom is stronger than skeletality; the latter would say only "$x=y$ if $d(x,y)=d(y,x)=0$".  That is, a quasi-pseudo-metric space can be skeletal without being a quasi-metric space, at least the way the latter term is usually used.

Note that like any kind of enriched category, Lawvere metric spaces are [[monads]] in a [[bicategory]] of "matrices", whose objects are sets and whose morphisms from $X$ to $Y$ are functions $d:X\times Y \to [0,\infty]$.  This sort of perspective can be generalized to many other kinds of topological structures; an exposition can be found in the book [Monoidal topology](#HST).

The category of metric spaces and categories of random maps as generalised metric spaces were studied in the [thesis](#Meng) of Lawvere's student Xiao-qing Meng. 


## Motivation for the axioms 

The [[triangle inequality|triangle axiom]] is the fundamental idea behind a metric space; it goes back (at least) to [[Euclid]] and captures the idea that we are discussing the *shortest* distance between two points.  Given the triangle inequality, we have the polygon inequality
$$ d(x_0,x_1) + \cdots + d(x_{n-1},x_n) \geq d(x_0,x_n) $$
for all $n \gt 0$; the point inequality extends this to $n = 0$.

Besides extended metric spaces (where distances may be infinite), one might consider spaces where distances may be negative.  But in fact this gives us nothing new, at least if we have symmetry.  First,
$$ d(x,x) + d(x,x) \geq d(x,x) $$
forces $d(x,x) \geq 0$, so $d(x,x) = 0$; then
$$ 2 d(x,y) = d(x,y) + d(y,x) \geq d(x,x) $$
forces $d(x,y) \geq 0$.  A generalisation to negative distances is possible for quasimetric spaces, however; the simplest example has $2$ elements, with $d(x,y) = -d(y,x)$ (but necessarily $d(x,x) = 0$ still).

We can define a [[preorder]] $\leq$ on the points of a Lawvere metric space:
$$ x \leq y \;\Leftrightarrow\; d(x,y) = 0 .$$
Then the symmetry axiom implies that this relation is [[symmetric relation|symmetric]] and hence an [[equivalence relation]].  The [[quotient set]] under this equivalence relation satisfies separation; in this way, every pseudometric space is [[equivalence of categories|equivalent]] (as an enriched category) to a metric space.  Even for quasimetric spaces, we can still define an equivalence relation:
$$ x \equiv y \;\Leftrightarrow\; d(x,y) = 0 \;\wedge\; d(y,x) = 0 .$$
In [[constructive mathematics]], it works better to use $\lneq$:
$$ x \lneq y \;\Leftrightarrow\; d(x,y) \gt 0 ;$$
then the symmetry axiom implies that this is an [[apartness relation]], which (for quasimetric spaces) we can also define directly:
$$ x \# y \;\Leftrightarrow\; d(x,y) \gt 0 \;\vee\; d(y,x) \gt 0 .$$


## Examples 

* Every [[set]] carries the **[[discrete space|discrete metric]]** given by
  $$
    d(x,y) \coloneqq \left\{\array{
      0 & \text{if } x = y
      \\
      1 & \text{otherwise}
    }\right.
  $$

  For certain purposes, it makes more sense to make most the non-zero distance $\infty$ instead of $1$; then one has an extended metric space.

* Every [[normed vector space]] is a metric space by $d(x,y) \coloneqq {\|x - y\|}$; a pseudonormed vector space is a pseudometric space.

* Every [[connected space|connected]] [[Riemannian manifold]] becomes a pseudometric space (or a metric space if, as is often assumed, the manifold is [[Hausdorff space|Hausdorff]]) by taking the distance between two points to be [[infimum]] of the Riemannian lengths of all continuously differentiable [[path|paths]] connecting them:
  $$
    d(x,y) \coloneqq inf_{x \stackrel{\gamma}{\to} y} len(\gamma)
  .$$

  If the manifold might not be connected, then it still becomes an extended metric space.

## Properties

* [[Lebesgue number lemma]]

* [[sequentially compact metric spaces are totally bounded]]

* [[sequentially compact metric spaces are equivalently compact metric spaces]]

* [[countably compact metric spaces are equivalently compact metric spaces]]

* [[metric spaces are fully normal]]

* [[metric spaces are paracompact]]

## Related concepts

* [[induced metric]]

* [[metric jet]] -- a notion of "tangency" for maps of metric spaces

* [[complete metric space]] and [[localic completion]]

* [[separable metric space]]

* [[distance (graph theory)]]

* [[Booij premetric space]]

* [[Richman premetric space]]

* [[enriched poset]]

[[!include generalized uniform structures - table]]


## References

* Wikipedia, _[Metric space](https://en.wikipedia.org/wiki/Metric_space)_

*  {#Lawvere73}  [[Bill Lawvere]] (1973).  _Metric spaces, generalized logic and closed categories_.  Reprinted in [[TAC]], 1986.  [Web](http://www.tac.mta.ca/tac/reprints/articles/1/tr1abs.html).
   

* {#Meng} Xiao-qing Meng, _Categories of convex sets and of metric spaces with applications to stochastic programming and related areas_, PhD thesis ([[Meng.djvu|djvu:file]]) 
 
* {#HST} Dirk Hofmann, Gavin J. Seal, and Walter Tholen (editors), *Monoidal topology: A Categorical Approach to Order, Metric, and Topology*,  Cambridge University Press, 2014

* {#Porton} [[Victor Porton]], _[Algebraic General Topology: Book 3: Algebra](https://mathematics21.org/the-algebra-of-general-topology/)_

* [[Fred Richman]], Real numbers and other completions ([pdf](http://math.fau.edu/richman/docs/RealNums.pdf))

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

[[!redirects metric space]]
[[!redirects metric spaces]]
[[!redirects metric]]
[[!redirects metrics]]
[[!redirects extended metric]]
[[!redirects extended metrics]]
[[!redirects extended metric space]]
[[!redirects extended metric spaces]]
[[!redirects pseudometric]]
[[!redirects pseudometrics]]
[[!redirects pseudometric space]]
[[!redirects pseudometric spaces]]
[[!redirects quasimetric]]
[[!redirects quasimetrics]]
[[!redirects quasimetric space]]
[[!redirects quasimetric spaces]]
[[!redirects quasipseudometric]]
[[!redirects quasipseudometrics]]
[[!redirects quasipseudometric space]]
[[!redirects quasipseudometric spaces]]
[[!redirects ultrametric]]
[[!redirects ultrametrics]]
[[!redirects ultrametric space]]
[[!redirects ultrametric spaces]]
[[!redirects Lawvere metric space]]
[[!redirects Lawvere metric spaces]]


[[!redirects distance]]
[[!redirects distances]]