
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The _homotopy cardinality_ or _$\infty$-groupoid cardinality_ of a (sufficiently "finite") [[space]] or [[∞-groupoid]] $X$ is an invariant of $X$ (a value assigned to its [[equivalence class]]) that generalizes the [[cardinality]] of a [[set]] (a [[0-truncated]] $\infty$-groupoid).

Specifically, whereas cardinality counts elements in a set, the homotopy cardinality counts [[object]]s up to [[equivalence]]s, up to [[2-morphism|2-equivalence]]s, up to [[3-morphism|3-equivalence]], and so on.  

This is closely related to the notion of [[Euler characteristic]] of a space or $\infty$-groupoid. See there for more details.

## Definition

### Groupoid cardinality

The **cardinality** of a [[groupoid]] $X$ is the [[real number]]

$$
  |X| = \sum_{[x] \in \pi_0(X)} \frac{1}{|Aut(x)|}
  \,,
$$

where the sum is over [[isomorphism]] classes of [[object]]s of $X$ and $|Aut(x)|$ is the cardinality of the [[automorphism group]] of an object $x$ in $X$. 

If this sum diverges, we say $|X| = \infty$. If the sum converges, we say $X$ is **tame**. (See at _[[homotopy type with finite homotopy groups]]_).

### $\infty$-Groupoid cardinality {#InfingroupoidCardinality}

This is the special case of a more general definition:

The groupoid cardinality of an [[∞-groupoid]] $X$ -- equivalently the **Euler characteristic** of a [[topological space]] $X$ (that's the same, due to the [[homotopy hypothesis]]) -- is, if it converges, the alternating product of cardinalities of the ([[simplicial homotopy group|simplicial]]) [[homotopy group]]s

$$
  |X| := \sum_{[x] \in \pi_0(X)}\prod_{k = 1}^\infty |\pi_k(X,x)|^{(-1)^k}
  =
  \sum_{[x]}
  \frac{1}{|\pi_1(X,x)|}
  |\pi_2(X,x)|
  \frac{1}{|\pi_3(X,x)|}
  |\pi_4(X,x)|
  \cdots
  \,.
$$

This corresponds to what is referred to as the *total homotopy order of a space*, introduced by Quinn in notes in 1995 on TQFTs (see reference list).



## Examples 

* Let $X$ be a [[discrete category|discrete groupoid]] on a finite [[set]] $S$ with $n$ elements. Then the groupoid cardinality of $X$ is just the ordinary [[cardinality]] of the [[set]]  $S$

  $$
    |X| = n
    \,. 
  $$

* Let $\mathbf{B}G$ be the [[delooping]] of a finite [[group]] $G$ with $k$ elements. Then

  $$
    |\mathbf{B}G| = \frac{1}{k}
  $$

* More generally, for an [[action]] of $G$ on a [[set]] $X$, then the cardinality of the [[action groupoid]] $X//G$ is $\frac{\vert X\vert} {\vert G \vert}$. This is traditionally sometimes called the _[[class formula]]_.

* Let $A$ be an [[abelian group]] with $k$ elements. Then we can [[delooping|deloop]] arbitrarily often and obtain the [[Eilenberg?Mac Lane objects]] $\mathbf{B}^n A$ for all $n \in \mathbb{N}$. (Under the [[Dold?Kan correspondence]] $\mathbf{B}^n A$ is the [[chain complex]] $A[n]$ (or $A[-n]$ depending on notational convention) that is concentrated in degree $n$, where it is the group $A$). Then

  $$
    |\mathbf{B}^n A| = 
    \begin{cases}
       k           & \text{if }\; n \;\text{ is even} \\
       \frac{1}{k} & \text{if }\; n \;\text{ is odd}
    \end{cases}
  $$

* Let $E = core(FinSet)$ be the groupoid of finite sets and bijections -- the [[core]] of [[FinSet]]. Its groupoid cardinality is the [[Euler number]]

  $$
    |E| = \sum_{n\in \mathbb{N}} \frac{1}{|S_n|} = \sum_{n\in \mathbb{N}} \frac{1}{n!} = e
   \,.
  $$

* Let $E=(E_i)$ be a finite [[crossed complex]], (i.e., an [[omega-groupoid]]; see the work of Brown and Higgins) such that for any object $v \in E_0$ of $E$ the cardinality of the set of $i$-cells with source $v$ is independent of the vertex $v$. Then the groupoid cardinality of $E$ can be calculated as $|E|=\displaystyle{\prod_{i} \#(E_i)^{(-1)^i}}$, much like a usual Euler characteristic. For the case when $F$ is a totally free crossed complex, this gives a very neat formula for the groupoid cardinality of the internal hom $HOM(F,E)$, in the category of [[omega-groupoids]]. Therefore the groupoid cardinality of the  function spaces (represented themselves by internal homs) can easily be dealt with if the underlying target space is represented by a [[omega-groupoid]], i.e.,  has trivial [[Whitehead products]]. (This is explored in the papers by Faria Martins and Porter mentioned in the reference list, below.)

* for $G$ a suitable [[algebraic group]], for $\Sigma$ a suitable [[algebraic curve]], and for $q$ a [[prime number]], then the groupoid cardinality of the $\mathbb{F}_q$-points of the [[moduli stack of G-principal bundles]] over $X$, $Bun_G(X)$ is the subject of the [[Weil conjectures on Tamagawa numbers]].

## Related concepts

* [[class formula]]

## References

* [[John Baez]], [[Alexander Hoffnung]], Christopher Walker, _Groupoidification Made Easy_ (web [pdf](http://math.ucr.edu/home/baez/groupoidification.pdf), [blog](http://golem.ph.utexas.edu/category/2008/12/groupoidification_made_easy.html)); _Higher-dimensional algebra VII: Groupoidification_, [arxiv/0908.4305](http://arxiv.org/abs/0908.4305)

* [[John Baez]], [[James Dolan]], _From Finite Sets to Feynman Diagrams_ ([arXiv](http://arxiv.org/abs/math.QA/0004133))

* [[João Faria Martins]],  On the homotopy type and the fundamental crossed complex of the skeletal filtration of a CW-complex (web [pdf](http://www.intlpress.com/HHA/v9/n1/a13/) ) 

* [[João Faria Martins]], [[Tim Porter]], On Yetter's Invariant and an Extension of the Dijkgraaf-Witten Invariant to Categorical Groups, (web [pdf] (http://www.tac.mta.ca/tac/volumes/18/4/18-04abs.html )) 

* [[Tom Leinster]], _The Euler characteristic of a category_ ([arXiv](http://arxiv.org/abs/math.CT/0610260), [TWF](http://math.ucr.edu/home/baez/week244.html), [blog](http://golem.ph.utexas.edu/category/2007/02/this_weeks_finds_in_mathematic_5.html), [blog](http://golem.ph.utexas.edu/category/2006/10/euler_characteristic_of_a_cate.html))

* Kazunori Noguchi, _The Euler characteristic of infinite acyclic categories with filtrations_, [arxiv/1004.2547](http://arxiv.org/abs/1004.2547)


* [[Frank Quinn]], 1995, Lectures on axiomatic topological quantum field theory , in D. Freed and 
K. Uhlenbeck, eds., Geometry and Quantum Field Theory , volume 1 of IAS/Park City Mathematics Series , AMS/IAS.

[[!redirects ∞-groupoid cardinality]]
[[!redirects homotopy cardinality]]

[[!redirects infinity-groupoid cardinality]]