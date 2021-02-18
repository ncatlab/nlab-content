
#Contents#
* table of contents
{:toc}

## Idea

The *Nisnevich topology* is a certain [[Grothendieck topology]] on the [[category]] of [[scheme]]s which is finer than the [[Zariski topology]] but coarser than the [[étale topology]]. It retains many desirable properties from both topologies:

* The Nisnevich [[cohomological dimension]] (and even the [[homotopy dimension]]) of a scheme is bounded by its [[Krull dimension]] (like Zariski)
* [[field|Fields]] have [[shape of an (∞,1)-topos|trivial shape]] for the Nisnevich topology (like Zariski)
* [[algebraic K-theory|Algebraic K-theory]] satisfies [[descent]] over the Nisnevich site -- as is true for the [[Zariski site]] but not in full generality for the [[etale site]], see at _[algebraic K-theory -- Descent](algebraic%20K-theory#Descent)_ for more;

* For $Z\subset X$ a [[closed subscheme|closed immersion]] between affine schemes that are smooth over a base $S$, the Nisnevich sheaf $X/(X-Z)$ is isomorphic to $N_{X,Z}/(N_{X,Z}-Z)$, where $N_{X,Z}$ is the normal bundle of $Z$ in $X$ (like &#233;tale)
* Pushforward along a [[finite morphism]] is an [[exact functor]] on Nisnevich sheaves of abelian groups (like &#233;tale)
* Nisnevich cohomology can be computed using [[?ech cohomology]] (like &#233;tale)

The Nisnevich topology plays a central r&#244;le in [[motivic homotopy theory]].


## Definition

An family of morphisms of [[Noetherian scheme]]s $\{p_i:V_i\to U\}$ is a **Nisnevich cover** if each $p_i$ is an [[étale map]] and if every field-valued point $Spec k\to U$ lifts to one of the $V_i$. This is a [[pretopology]] on the category of Noetherian schemes, and the associated topology is the **Nisnevich topology**.

The **Nisnevich site** over a [[Noetherian scheme]] $S$ usually refers to the [[site]] given by the [[category]] of [[smooth scheme]]s of finite type over $S$ equipped with the Nisnevich topology. The **small Nisnevich site** of $S$ is the subsite consisting of [[étale map|étale]] $S$-schemes.

### For non-Noetherian schemes

For a general [[affine scheme]] $X$, one defines a [[sieve]] $S$ on $X$ to be a covering sieve for the Nisnevich topology if there exist a Noetherian affine scheme $Y$, a morphism $f: X\to Y$, and a Nisnevich covering sieve $T$ on $Y$ such that $f^\ast(T)\subset S$. On an arbitrary [[scheme]] $X$, a sieve $S$ is a Nisnevich covering sieve if there exists an open cover $\{U_i\to X\}$ by affine schemes such that $S_{/U_i}$ is a Nisnevich covering sieve on $U_i$ for all $i$.

### As an excision property

Let $Et/S$ be the category of [[étale scheme]]s of [[morphism of finite presentation|finite presentation]] over a [[quasi-compact morphism|quasi-compact]] [[quasi-separated morphism|quasi-separated]] scheme $S$. An [[(∞,1)-presheaf]] $F$ on $Et/S$ is said to satisfy _Nisnevich excision_ if the following conditions hold:

* $F(\emptyset)$ is [[contractible]].
* If $Z$ is a closed subscheme of $X\in Et/S$ and if $X'\to X$ is a morphism in $Et/S$ which is an isomorphism over $Z$, then the square

$$
  \array{
     F(X) &\to& F(X-Z)
     \\
     \downarrow && \downarrow
     \\
     F(X') &\to& F(X'-Z)
  }
$$

is an [[(∞,1)-pullback]] square. Intuitively, this says that the space of sections of $F$ over $X$ with support in $Z$ (i.e., the [[homotopy fiber]] of $F(X) \to F(X-Z)$) does not depend on $X$. This is Definition 2.5 in [DAG XI](#DAGXI).

+-- {: .num_prop}
###### Proposition
An [[(∞,1)-presheaf]] on $Et/S$ is an [[(∞,1)-sheaf]] for the Nisnevich topology if and only if it satisifes Nisnevich excision.

=--

This is [Morel-Voevosky, Prop. 1.16](#MV99) or [DAG XI, Thm. 2.9](#DAGXI).

## Properties

### Homotopy dimension

+-- {: .num_prop}
###### Proposition
If $S$ is a [[Noetherian scheme]] of finite [[Krull dimension]], then the [[(∞,1)-topos]] of [[(∞,1)-sheaves]] on the small Nisnevich site of $S$ has [[homotopy dimension]] $\leq\dim(S)$.

=--

This is [DAG XI, Theorem 2.24](#DAGXI). As a consequence, [[Postnikov tower]]s are convergent in the [[(∞,1)-topos]] of [[(∞,1)-sheaves]] on the Nisnevich site over $S$, and in particular that (∞,1)-topos is [[hypercomplete]].

+-- {: .num_prop}
###### Proposition
More generally, if $S$ is a pro-algebraic space limit of a cofiltered diagram of qcqs algebraic spaces of Krull dimension $\leq d$, then the [[(∞,1)-topos]] of [[(∞,1)-sheaves]] on the small Nisnevich site of $S$ has [[homotopy dimension]] $\leq d$. 

=--

This is Clausen and A. Mathew, Hyperdescent and etale K-theory, 2019, arXiv:1905.06611, Cor.3.11, Thm.3.12, and Thm.3.17.



## Related concepts

* [[fpqc-site]] $\to$ [[fppf-site]] $\to$ [[syntomic site]] $\to$ [[étale site]] $\to$ **Nisnevich site** $\to$ [[Zariski site]]

* [[cd-structure]]

## References

A quick overview is at the beginning of the talk slides

* Jardine, _Motivic spaces and the motivic stable category_ ([pdf](http://www.aimath.org/WWN/motivesdessins/motivic.pdf)) .

A detailed discussion is in [section 3.1.1](http://www.math.uiuc.edu/K-theory/0305/nowmovo.pdf#page=61) of

* [[Fabien Morel]], [[Vladimir Voevodsky]], _$\mathbb{A}^1$-homotopy theory of schemes_ ,  K-theory, 0305 ([web](http://www.math.uiuc.edu/K-theory/0305/) [pdf](http://www.math.uiuc.edu/K-theory/0305/nowmovo.pdf))
{#MV99}

or in the lecture notes

* [[Eric Friedlander]], _[Algebraic Cycles and algebraic K-theory, II](http://www.math.northwestern.edu/~eric/lectures/)_ ([lecture 6 (pdf)](http://www.math.northwestern.edu/~eric/lectures/ihp/ihplec6.pdf))

A self-contained account of the Nisnevich $(\infty,1)$-topos including the non-Noetherian case is in

* [[Jacob Lurie]], _Derived Algebraic Geometry XI: Descent Theorems_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XI.pdf))
{#DAGXI}

[[!redirects Nisnevich topology]]
[[!redirects Nisnevich topos]]
[[!redirects Nisnevich (∞,1)-topos]]

[[!redirects Nisnevich sheaf]]
[[!redirects Nisnevich sheaves]]

[[!redirects Nisnevich descent]]