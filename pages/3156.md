[[!redirects natural weak factorization system]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

##Basic idea##

**Algebraic weak factorization systems** (AWFS) are algebraizations of [[weak factorization system]]s (WFS). The elements in the left and right classes of morphisms are replaced by coalgebras and algebras, respectively, for a certain [[comonad]] and [[monad]] on the [[arrow category]]. This comonad and monad also determine the functorial factorization and give natural coalgebra and algebra structures to the left and right factors.

Algebraic weak factorization systems were originally called **natural weak factorization systems** by Grandis and Tholen.

##Preliminaries##

Recall a **functorial factorization** on a category $K$ is a functor $E : K$<sup>2</sup> &rarr; $K$<sup>3</sup> that is a section to the composition functor $d_1$, induced by the inclusion functor $d^1 : 2 \rightarrow 3$ between the ordinal categories.

Explicitly, $E$ factors a morphism $(u,v) : f \Rightarrow g$ in $K^{2}$ as

$$
  \array{
    \cdot &\stackrel{u}{\to}& \cdot
    \\
    \downarrow^f
    &&
    \downarrow^g
    \\
   \cdot &\stackrel{v}{\to}& \cdot    
  } \array{ & & } \stackrel{E}{\mapsto} \array{ &&}
  \array{
    \cdot &\stackrel{u}{\to}& \cdot
    \\
    \downarrow^{Lf}
    &&
    \downarrow_{Lg}
    \\
    \cdot  & \stackrel{E(u,v)}{\to} & \cdot 
   \\ \downarrow^{Rf} && \downarrow_{Rg} \\
   \cdot &\stackrel{v}{\to}& \cdot    
  }
$$

There are two other injective functors $d^0, d^2 : 2 \rightarrow 3$ whose image misses the object that appears as their superscript. When we compose $E$ with $d_2$ and $d_0$, we obtain endofunctors of $K^{2}$, which we call $L$ and $R$. 

There are obvious natural transformations $1 \Rightarrow R$ and $L \Rightarrow 1$ whose components are given by the data of the functorial factorization $E$. We say $L$ and $R$ are **pointed** endofunctors, with these natural transformations in mind.

##Definition##

A AWFS on a category $K$ consists of a pair $(L,R)$ where $L$ is a comonad and $R$ is a monad, whose underlying pointed endofunctors arise from a functorial factorization $E$. Some authors (Garner) also require that the canonical natural transformation $L R \Rightarrow R L$, whose domain and codomain components are given by the comultiplication and multiplication maps, is a distributive law of the comonad over the monad. This amounts to the requirement that a pentagon involving the comultiplication and multiplication maps commutes.

We refer to the $L$-coalgebras as the **left class** of the AWFS and the $R$-algebras as the **right class**. When we forget the algebra structures, we obtain classes of maps in $K$. The retract closures of these classes form a WFS called the **underlying WFS** of this AWFS.

Given a lifting problem 
$$
  \array{
    \cdot &\stackrel{u}{\to}& \cdot
    \\
    \downarrow^f
    &&
    \downarrow^g
    \\
   \cdot &\stackrel{v}{\to}& \cdot    
  }$$
where $f$ is a $L$-coalgebra and $g$ is an $R$-algebra, the functorial factorization, coalgebra, and algebra structures can be combined to define a solution, which proves that the left class has the left lifting property with respect to the right class. We leave the details as an exercise.

##Interesting features##

* The right class of a AWFS is closed under any limits that exist in $K^{2}$, because the forgetful functor to the underlying category of arrows creates all limits which exist. Note that it does not follow that the right class of the underlying WFS is closed under limits in the arrow category, because first, it is possible that some elements of the right class will not have an $R$-algebra structure, and second, not every map in the arrow category between $R$-algebras is necessarily an $R$-algebra map.

* Algebras for the monad of an AWFS can be composed canonically, as can the coalgebras for the comonad. The composition law for the algebras uses the comultiplication natural transformation, and dually for the coalgebras.

* A AWFS $(L,R)$ on $K$ induces a levelwise AWFS on any diagram category $K^A$. Note that its underlying WFS will not be similarly "levelwise". (Indeed, a WFS does not typically induce a levelwise WFS on a diagram category.)

* An AWFS can be detected as a [[functorial factorization]] that extends to a [[monad]] over $cod$ with a [[composition law for factorizations]].

##Small object argument##

The [[algebraic small object argument]], an enhancement of the [[small object argument]] due to Richard Garner, produces **cofibrantly generated** AWFS by adapting the construction of a [[free monad]] on an endofunctor.  Importantly, Garner's small object argument allows the generators to be a small category over the arrow category $K^{[2]}$, rather than simply a set of arrows. As a result, there are WFS which are not cofibrantly generated in the classical sense, but which can be exhibited as the underlying WFS of a cofibrantly generated AWFS.

Every AWFS on a [[locally presentable category]] generated by such a small category of maps is in particular an [[accessible weak factorization system]], and every accessible WFS admits an algebraic enhancement generated by the algebraic small object argument.  However, not every accessible AWFS is *itself* generated by the algebraic small object argument, unless we enhance it further to take a [[double category]] of generators; see [Bourke and Garner](#BourkeGarnerI).


## Related concepts

* [[algebraic model category]]
* [[accessible model category]]
* [[accessible weak factorization system]]

[[!include algebraic model structures - table]]

## References

* [[Marco Grandis]] and [[Walter Tholen]], _Natural weak factorization systems_, Arch. Math. (Brno) 42(4) (2006) 397&#8211;408. MR2283020 (2008b:18006), Zbl 1164.18300.

* [[Richard Garner]], _Understanding the small object argument_, [arXiv](http://arxiv.org/abs/0712.0724).

* [[Emily Riehl]], _Algebraic model structures_, ([arXiv:0910.2733](http://arxiv.org/abs/0910.2733)).

* [[Thomas Athorne]], _The coalgebraic structure of cell complexes_, [TAC](http://www.tac.mta.ca/tac/volumes/26/11/26-11abs.html)

* [[Tobias Barthel]] and [[Emily Riehl]], *On the construction of functorial factorizations for model categories*, Algebr. Geom. Topol. Volume 13, Number 2 (2013), 1089-1124, , [arxiv](https://arxiv.org/abs/1204.5427)

* {#BourkeGarnerI} [[John Bourke]] and [[Richard Garner]], _Algebraic weak factorisation systems I: accessible AWFS_, [arXiv](http://arxiv.org/abs/1412.6559).

* [[John Bourke]] and [[Richard Garner]], _Algebraic weak factorisation systems II: categories of weak maps_, [arXiv](http://arxiv.org/abs/1412.6560).

* J. Rosicky, _Accessible model categories_, [arxiv](https://arxiv.org/abs/1503.05010)

* [[Emily Riehl]], _Made-to-Order Weak Factorization Systems_, [doi](https://doi.org/10.1007/978-3-319-21284-5_17), [pdf](http://www.math.jhu.edu/~eriehl/made-to-order.pdf)

* [[Ignacio Lopez Franco]], *Cofibrantly generated lax orthogonal factorisation systems*, [arxiv](https://arxiv.org/abs/1510.07131)

A new proof of the [[Strøm model structure]] using algebraic weak factorization systems:

* {#BarthelRiehl13} [[Tobias Barthel]], [[Emily Riehl]], _On the construction of functorial factorizations for model categories_, Algebr. Geom. Topol. 13 (2013) 1089-1124 ([arXiv:1204.5427](http://arxiv.org/abs/1204.5427), [doi:10.2140/agt.2013.13.1089](http://dx.doi.org/10.2140/agt.2013.13.1089), [euclid:agt/1513715550](https://projecteuclid.org/euclid.agt/1513715550))


[[!redirects natural weak factorisation system]]
[[!redirects natural weak factorisation systems]]
[[!redirects natural weak factorization system]]
[[!redirects natural weak factorization systems]]
[[!redirects algebraic weak factorisation system]]
[[!redirects algebraic weak factorisation systems]]
[[!redirects algebraic weak factorization systems]]
[[!redirects NWFS]]
[[!redirects nwfs]]
[[!redirects AWFS]]
[[!redirects awfs]]
[[!redirects algebraic wfs]]
[[!redirects algebraic WFS]]

