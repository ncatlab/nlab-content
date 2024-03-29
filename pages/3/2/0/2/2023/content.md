
> This entry is about the notion in [[order theory]]. For the related concept in [[topology]] see at _[[topological interval]]_, and for  concept in [[homotopy theory]] see at _[[interval object]]_. 

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## In posets

### Idea

In the general context of [[posets]], an _interval_ is an [[under category]], [[over category]], or under-over category. They are closed under betweenness: if two points belong to an interval and a third point is between them, then that third point also belongs to the interval. 


### Definitions

Given a [[poset]] $P$ and an element $x$ of $P$, the __upwards unbounded interval__ $[x,\infty[$ (also $[x,\infty)$, $[x,\infty[_P$, etc) is the [[subset]]
$$ {[x, \infty[} = \{ y : P \;|\; x \leq y \} ;$$
the __downwards unbounded interval__ $]{-\infty}, x]$ (also $(-\infty,x]$, $]{-\infty},x]_P$, etc) is the subset
$$ ]{-\infty}, x] = \{ y : P \;|\; y \leq x \} ;$$
and given an element $y$ of $P$, the __bounded interval__ $[x,y]$ (also $[x,y]_P$) is the subset
$$ [x,y] = \{ z : P \;|\; x \leq z \leq y \} .$$

Thinking of $P$ as a [[category]] and subsets of $P$ as [[full subcategory|subcategories]], $[x,\infty[$ is the [[coslice category]] $(x/P)$, $]{-\infty},x]$ is the [[slice category]] $(P/x)$, and $[x,y]$ is the bislice category $(y/P/x)$.

An interval with distinct [[top]] and [[bottom]] element in a [[total order]] is also called a **linear interval**. (Sometimes this is called a **strict linear interval** and just "linear interval" then refers to the situation where top and bottom may coincide.)

Besides the __closed intervals__ above, we also have the __open intervals__

*  $ {]x, \infty[} = {[x,\infty[} \setminus \{x\} = \{ y : P \;|\; x \lt y \} ,$
*  $ {]{-\infty}, x[} = {]{-\infty}, x]} \setminus \{x\} = \{ y : P \;|\; y \lt x \} ,$
*  $ {]x, y[} = [x, y] \setminus \{x, y\} = \{ z : P \;|\; x \lt z \lt y \} ,$

as well as the __half-open intervals__

*  $ {[x,y[} = [x,y] \setminus \{y\} = \{ z : P \;|\; x \leq z \lt y \} ,$
*  $ ]x,y] = [x,y] \setminus \{x\} = \{ z : P \;|\; x \lt z \leq y \} .$

These are important in analysis, and more generally whenever the [[quasiorder]] $\lt$ is at least as important as the [[partial order]] $\leq$.


The entire poset $P$ is also considered an __unbounded interval__ in itself.


### Examples

#### Intervals in the real line

Intervals of [[real numbers]] are important in [[analysis]] and [[topology]]. They may be succinctly characterized as the [[connected space|connected]] [[subspaces]] of the real line. The bounded closed intervals in the real line are the original [[compact spaces]].

The interval in the reals has a [[universal property|universal]] characterization: it [is the terminal coalgebra](http://ncatlab.org/nlab/show/terminal+coalgebra+of+an+endofunctor#UnitInterval) of the [[endofunctor]] on the category of all intervales that glues an interval end-to-end to itself.

The __unit interval__ $[0,1]$ is primary in [[homotopy theory]]; specifically in [[topological homotopy theory]] a __[[left homotopy]]__ from a [[continuous function]] $f$ to a continuous function $g$ is a continuous function  $h \colon A \times I \to B$ out of the [[product topological space]] with the [[topological interval]] $I = [0,1]$ such that $h(x,0) = f(x)$ and $h(x,1) = g(x)$. More generally this is the concept of left homotopy for an [[interval object]] in a suitable ([[model category|model]]) [[category]].

The usual [[integral]] in ordinary calculus is done over an interval in the real line, a compact interval for a 'proper' integral, or any interval for an 'improper' integral.  The theory of [[Lebesgue measure]] removes this restriction and allows integrals over any [[measurable subset]] of the real line.  Still, the Lebesgue measure on intervals (even compact intervals) generates all of the rest.

To integrate a $1$-[[differential form|form]] on the real line requires orienting an interval; the standard orientation is from $x$ to $y$ in $[x,y]$.  If $x \gt y$, then $[x,y]$ (which by the definition above would be [[empty set|empty]]) may also be interpreted as $[y,x]$ with the reverse orientation.  This also matches the traditional notation for the integral.

### Properties

#### Classifying topos

The [[classifying topos]] for linear intervals is the category [[sSet]] of [[simplicial sets]]. See the section _[For intervals](http://ncatlab.org/nlab/show/classifying+topos#ForIntervals)_ at _[[classifying topos]]_.

#### Relation to simplices
 {#RelationToSimplices}

Let $\mathbb{I}$ be the category of _finite_ linear intervals. 

There is an [[equivalence of categories]]

$$
  \widehat{(-)} : \Delta^{op} \stackrel{\simeq}{\to} \mathbb{I}
$$

from the [[opposite category]] of the [[simplex category]] to $\mathbb{I}$.

Here

$$
  \widehat{[n]} \coloneqq Hom_{\Delta}([n],[1]) \simeq [n+1]
$$

and the inverse is

$$
  [n] \mapsto Hom_{\mathbb{I}}([n],[1])
  \,.
$$

See also at _[Simplex category -- Duality with intervals](simplex+category#DualityWithIntervals)_.

#### Intervals as generators of the incidence algebra

Recall that the [[incidence algebra]] $I(P)$ of a poset $P$ (relative to some commutative ring $R$) is an [[associative unital algebra]] containing all functions $f : P \times P \to R$ such that $x \nleq y$ implies $f(x,y) = 0$. For any pair of elements related by the order $x \leq y$, we can define an element $\epsilon_{x,y}$ of the incidence algebra by:
$$
\epsilon_{x,y}(u,v) = \begin{cases}1 & u = x, w = y \\ 0 & \text{otherwise}\end{cases}
$$
and the collection of such functions $\epsilon_{x,y}$ form a [[basis]] of $I(P)$ as an $R$-[[module]].
So, the [[dimension]] of the incidence algebra $I(P)$ is equal to the total number of (non-empty) intervals in $P$.

Information about the number of intervals in a finite poset is also encoded in its [[zeta polynomial]].

## In homotopy theory

In [[homotopy theory]], "cellular" models for the intervals play a central role. See [[interval object]].

## In geometry

The [[geometry]] (for instance [[differential geometry]]) of intervals, for instance in the [[real line]], are often relevant. 

See for instance [Geometric spaces and their homotopy types](http://ncatlab.org/nlab/show/cohesive+homotopy+type+theory#GeometricSpacesAndTheirHomotopyTypes) at [[cohesive homotopy type theory]].

## Related concepts

* [[interval arithmetic]]

* [[interval type]], [[interval object]]

* [[abstract circle]]

* [[twisted arrow category]]

* [[t-norm]]


[[!redirects interval]]
[[!redirects intervals]]

[[!redirects unit interval]]

[[!redirects under-over category]]

[[!redirects linear interval]]
[[!redirects linear intervals]]

[[!redirects open interval]]
[[!redirects open intervals]]

[[!redirects closed interval]]
[[!redirects closed intervals]]

[[!redirects half-open interval]]
[[!redirects half-open intervals]]
