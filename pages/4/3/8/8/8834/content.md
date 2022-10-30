
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[abelian categories]] one talks of [[chain complexes]]; and in that context a composable pair $ A \to B \to C $ is null iff $ B \to C $ factors through the [[cokernel]] $ B/(A) $:
$$ \begin{array}{ccccc}
A & \to & B \\
\downarrow &  & \downarrow & \searrow \\
0 & \to & B/(A) & \to & C
\end{array}
$$
and so forth.  In a strict context, the factorization is unique.

In a pointed [[(∞,1)-category]] with [[(∞,1)-colimits]] of small [[1-truncated]] [[diagrams]], one may still consider factorizations through [[cofibers]]:
$ A \to B \to C \sim * : A \to C $
but now there is a choice to make, roughly parametrized by an [[action]] of $Map_* (\Sigma A, C)$.  This leads to interesting structure, describing (with upper bounds!) how trivially a particular sequence of arrows may compose.

To begin, consider a sequence of maps $ A_0 \to A_1 \to A_2 \to A_3 $.  If the composites $A_0 \to A_2 $ and $ A_1\to A_3$ are nulhomotopic, then one has a diagram
$$\begin{array}{ccccc}
A_0 & \to & A_1 & \to & * \\
\downarrow & & \downarrow & & \downarrow \\
* & \to & A_2 & \to & A_3
\end{array} $$
any choice of homotopies in the two squares gives a map $ \Sigma A_0 \to A_3 $.


## Preliminaries


Define $C$ and $D$ to be the cofibers of $A_0 \to A_1$ and $A_1\to A_2$, respectively. A choice of homotopy $ A_0 \to A_2 \sim 0 $ corresponds to a choice of factorization $ A_1 \to C \to A_2 $, which gives a diagram of pushout squares

$$\begin{array}{ccccccc}
A_0 & \to & A_1 & \to & * \\
\downarrow & & \downarrow & & \downarrow \\
* & \to & C &\to & \Sigma A_0  & \to & *\\
 & & \downarrow & & \downarrow & & \downarrow \\
 & & A_2 & \to & D & \to & C'
\end{array}$$

It is to be noted that the map $ \Sigma A_0 \to D $ and possibly the object $C'$ depend on the choice of factor $ C \to A_2 $, but that $A_2 \to D$ does not, in any meaningful sense, so depend: this is just the structure map of the cofiber of $A_1\to A_2$.  Note that the cofiber $C'$ of $C\to A_2$ is thus equivalent to that of $\Sigma A_0 \to D$; but again the role of choices must be studied.

## Definitions

A sequence of maps $A_0 \to A_1 \to \cdots \to A_n$ will be called *a bracket sequence* (a novel phrase for the purposes of this entry) in either of two cases:

* $n = 3$ and the composites $A_0 \to A_2$ and $A_1 \to A_3$ are nulhomotopic; OR
* $n \gt 3$, and (using the preceding notations), there are choices of factor $C\to A_2$ and $ D \to A_3 $ such that the induced sequence $ \Sigma A_0 \to D \to A_3 \to \cdots \to A_n$ is a bracket sequence.

In all cases, a bracket sequence leads to a three-map sequence
$$ \Sigma^m A_0 \to D_m \to A_{m+2} \to A_{m+3} $$
in which consecutive maps compose trivially, and so there are induced choices of maps
$$ \Sigma^{m+1} A_0 \to A_{m+3} .$$

The collection of all such maps, taking all compatible variations, is the **Toda Bracket** of the bracket sequence.

Among the bracket sequences, a particular family arises which here will be called _null-bracket_ (again, a novel phrase).  A sequence will be called null-bracket if

* $n=2$ and $A_0 \to A_2$ is trivial, OR
* $n \gt 2$, and there is a choice of factorization $ A_1 \to C \to A_2 $ such that the sequence $ C \to A_2 \to \cdots \to A_n $ is null-bracket.

If the Toda bracket for a bracket sequence includes the trivial map $\Sigma^{m+1} A_0 \to A_{m+3}$ then the sequence is null-bracket.

## Applications

By definition, if a sequence is a bracket sequence AND NOT a null-bracket sequence, it follows that all the relevant maps $\Sigma^{k} A_0 \to A_n$ are nontrivial.  Things like these Toda brackets have been studied by many _(FIXME: referrences later)_ and especially the length-three brackets used by H. Toda to describe most of $\pi_k \mathbb{S}^n$ for $k \lt 31$ or so.

In ([Cohen, 1968](#Cohen)) is given a criterion for stable maps of spheres to inhabit non-null Toda brackets; this turns out to be most of $\pi_* \mathbb{S}$, and furthermore the maps in the bracket sequences can be chosen from a very small set (_FIXME_: be more precise! degree maps $n \iota$, [[Hopf map]]s $\eta, \theta,\sigma$, and $\alpha_p$... )

## Related concepts

* [[Massey product]]

## References

* Joel Cohen, _The decomposition of stable homotopy_, Annals of Mathematics (2) 87 (2): 305&#8211;320 (1968)
 {#Cohen}

* [[Hans-Joachim Baues]], _On the cohomology of categories, universal Toda brackets and homotopy pairs_, K-Theory __11__:3, April 1997, pp. 259-285 (27) [springer](http://link.springer.com/article/10.1023/A%3A1007796409912)
* Boryana Dimitrova, _Universal Toda brackets of commutative ring spectra_, poster, Bonn 2010, [pdf](http://www.math.uni-bonn.de/people/grk1150/YWT2010/YWT_Dimitrova.pdf) 
* [[C. Roitzheim]], [[S. Whitehouse]], _Uniqueness of $A_\infty$-structures and Hochschild cohomology_, [arxiv/0909.3222](http://arxiv.org/abs/0909.3222)
* Steffen Sagave, _Universal Toda brackets of ring spectra_, Trans. Amer. Math. Soc., 360(5):2767-2808, 2008, [math.KT/0611808](http://arxiv.org/abs/math/0611808)

[[!redirects Toda Brackets]]

[[!redirects Toda brackets]]
