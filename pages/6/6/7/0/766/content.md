[[!redirects higher homotopy van Kampen theorem]]
[[!redirects higher homotopy van Kampen theorem]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _higher homotopy van Kampen theorem_ is a theorem that asserts that the [[homotopy type]] of a [[topological space]] can be computed by a suitable [[colimit]] or [[homotopy colimit]] over homotopy types of its pieces.

This generalizes the [[van Kampen theorem]], which only deals with the underlying 1-type (the fundamental groupoid).

## For topological spaces {#ForTopSpaces}

### General statement

+-- {: .un_theorem}
###### Theorem

Let $X$ be a [[topological space]], write $Op(X)$ for its [[category of open subsets]] and let

$$
  \chi : C \to Op(C)
$$

be a [[functor]] out of a [[small category]] $C$ such that

* for each point $x\in X$ the [[full subcategory]] $C_x$ of objects $c$ such that $\chi(x)$ contains $x$ has a [[weak homotopy equivalence|weakly]] [[contractible]] [[nerve]].

Then:

the canonical morphism in [[sSet]] out of the [[colimit]]

$$
   {\lim_\to} Sing \circ \chi \to Sing(X)
$$ 

into the [[singular simplicial complex]] of $X$ exhibits $Sing(X)$ as the [[homotopy colimit]]  $hocolim Sing \circ \chi$.


=--

This is theorem A.1.1 in ([Lurie](#Lurie)).


### Strict version

The following is a version of the above general statement restricted to a [[strict ∞-groupoid]]-version of the [[fundamental ∞-groupoid]] and applicable for [[topological spaces]] that are equipped with the extra structure  of a [[filtered topological space]].

Notice that these strict $\infty$-groupoids are equivalent to [[crossed complex]]es.


Suppose $X_*$ is a [[filtered space]] and $X$ is the union of the interiors of sets $U^i$, $i \in I$. Let $U^i_*$ be the filtered space given by the intersections $U^i \cap X_n$ for $n \geq 0$. If $d=(i,j) \in I^2$ we write $U^d$ for $U^i \cap U^j$. We then have a coequaliser diagram of filtered spaces 

$$\bigsqcup_{d \in I^2} U^d_* \rightrightarrows ^a_b \bigsqcup _{i \in I} U^i_* \to ^c X_*.$$

+-- {: .un_theorem}
###### Strict Higher van Kampen Theorem

If the filtered spaces $U^f_*$ are [[connected filtered space]]s for all finite intersections $U^f_*$ of the filtered spaces $U^i_*$, then

1. (Conn) The filtered space $X_*$ is connected; and

1. (Iso) The fundamental [[crossed complex]] functor $\Pi$ takes the above coequaliser diagram of filtered spaces to a coequaliser diagram of crossed complexes.

=--

**Remarks**

* Note that because $\Pi$ uses groupoids, it obviously takes disjoint unions $\bigsqcup$ of filtered spaces into disjoint unions (= coproducts) $\bigsqcup$ of crossed complexes. 

* The proof of the theorem is not direct but goes via the fundamental cubical $\omega$-groupoid with connections of the filtered spaces, as that context allows the notions of _algebraic inverse to subdivision_ and of _commutative cube_. However the proof is a direct generalisation of a proof for the [[van Kampen theorem]] for the [[fundamental groupoid]].  

* Applications of this theorem include many basic facts in algebraic topology, such as the Relative Hurewicz Theorem, the Brouwer degree theorem, and new nonabelian results on 2nd relative homotopy groups, not of course obtainable by the traditional wholly abelian methods. No use is made of _singular homology theory_ or of _simplicial approximation_.



## For objects in a cohesive $(\infty,1)$-topos

In a [[cohesive (∞,1)-topos]] higher van Kampen theorems hold in great generality. 

See the section <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#vanKampenTheorem">cohesive (∞,1)-topos -- van Kampen theorem</a>.

In particular for the cohesive $(\infty,1)$-topos [[?TopGrpd]] of [[topological ∞-groupoid]]s this reproduces the [topological higher van Kampen theorem](#ForTopSpaces) discussed above.


## Examples

Here is one application in dimension 2 not easily obtainable by traditional [[algebraic topology]]. 

Let $0 \to P \to Q \to R \to 0$ be an [[exact sequence]] of [[abelian groups]]. Let $X$  be the [[mapping cone]] of the induced map $K(P,1) \to K(Q,1)$ of [[Eilenberg-Mac Lane space]]s. Then a [[crossed module]] representing the [[homotopy 2-type]] of $X$ is $\mu: C \to Q$ where $C$ is abelian and is the direct sum $\oplus_{r \in R} P^r$  of copies of $P$ one for each $r \in R$ and the action of $Q$ is via $R$ and permutes the copies by $(p,r)^s=(p,r+s)$. Similar examples for $P,Q,R$ nonabelian are do-able,   more complicated, and certainly **not** obtainable by traditional methods.





## References

The version for topological spaces and the [[fundamental infinity-groupoid]] functor is discussed in  Appendix A of

* [[Jacob Lurie]], _[[Ek-Algebras]]_

The version for filtered topological spaces and the strict homotopy $\infty$-groupoid functor is discussed in

* [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]], _[[Nonabelian Algebraic Topology]]_

[[!redirects Higher Homotopy van Kampen Theorem]]
[[!redirects higher homotopy van Kampen Theorem]]

[[!redirects higher van Kampen theorem]]