
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The __wedge sum__ $A \vee B$ of two [[pointed sets]] $A$ and $B$ is the [[quotient set]] of the [[disjoint union]] $A \uplus B$ where both copies of the basepoint (the one in $A$ and the one in $B$) are identified.  The wedge sum $A \vee B$ can be identified with a [[subset]] of the [[cartesian product]] $A \times B$; if this subset is collapsed to a point, then the result is the [[smash product]] $A \wedge B$.

The wedge sum can be generalised to [[pointed objects]] in any category $C$ with [[pushouts]], and is the [[coproduct]] in the category of pointed objects in $C$ (which is the [[coslice category]] $*/C$).  A very commonly used case is when $C=$[[Top]] is a category of [[topological spaces]].

In particular, if $C$ itself is a [[pointed category]], then every object is uniquely a pointed object, so that the coproduct in $C$ itself may be called a _wedge sum_.  A commonly used case is when $C=$[[Spectra]] is a category of [[spectra]].

Also, the wedge sum also makes sense for any [[family]] of pointed objects, not just for two of them, as long as $C$ has pushouts of that size.


## Definition

+-- {: .num_defn }
###### Definition

For $\{x_i \colon * \to X_i\}_i$ a set of [[pointed objects]] in a [[category]] $\mathcal{C}$, their _wedge sum_ $\bigvee_i X_i$ is the [[pushout]] in $\mathcal{C}$

$$
  \bigvee_i X_i \coloneqq (\coprod_i X_i) \coprod_{\coprod_{i} *} *
$$

in 

$$
  \array{
     \coprod_{i} * &\stackrel{(x_i)}{\to}& \coprod_i X_i
     \\
     \downarrow && \downarrow
     \\
     * &\to& \bigvee_i X_i
  }
  \,,
$$

if this exists.
=--

Equivalently (see at [overcategory -- limits and colimits](overcategory#LimitsAndColimits)) this is just the [[coproduct]] in the [[undercategory]] $\mathcal{C}\backslash\ast$ of [[pointed objects]].


## Examples

* A wedge sum of pointed [[circles]] is also called a **bouquet** of circles. See for instance at _[[Nielsen-Schreier theorem]]_.

* For $X$ a [[CW complex]] with [[filtered topological space]] structure $X_0 \hookrightarrow \cdots \hookrightarrow \X_k \hookrightarrow X_{k+1} \hookrightarrow \cdots \hookrightarrow X$ the quotient topological spaces $X_{k+1}/X_k$ are wedge sums of $(k+1)$-spheres.

## Related concepts

* [[wedge sum type]]

* [[loop space of a wedge of circles]]

## References

Texbook accounts: 

* {#Munkres75} [[James Munkres]], §71 of: _Topology_, Prentice Hall (1975, 2000) $[$[pdf](http://mathcenter.spb.ru/nikaan/2019/topology/4.pdf)$]$

* {#tomDieck2008} [[Tammo tom Dieck]],  p. 31 of: _Algebraic topology_, European Mathematical Society, Zürich (2008) $[$[doi:10.4171/048](https://www.ems-ph.org/books/book.php?proj_nr=86), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/diecktop.pdf)$]$


See also:

* Wikipedia *[Wedge sum](https://en.wikipedia.org/wiki/Wedge_sum)* 

* [[Neil Strickland]], Section 2 of: *A Bestiary of Topological Objects* \[<a href="https://strickland1.org/courses/bestiary/bestiary.pdf">pdf</a>, [[Strickland-BestiaryTopological.pdf:file]]\]



[[!redirects wedge sum]]
[[!redirects wedge sums]]
