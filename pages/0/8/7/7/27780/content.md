

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--


\tableofcontents


## Idea 

The *Atiyah-Jänich theorem* ([Jänich 1965](#Jänich65), [Atiyah 1967 Thm A1](#Atiyah67)) states that the space of [[Fredholm operators]] $Fred(\mathscr{H})$ on a (countably infinite-dimensional [[separable Hilbert space|separable]], [[complex vector space|complex]]) [[Hilbert space]] $\mathscr{H}$ is a [[classifying space]] for [[topological K-theory]] $K(-)$:

For $X$ a [[compact Hausdorff space]], the [[homotopy classes]] of [[continuous maps]] from $X$ (hence the [[connected components]] of the [[mapping space]]) to $Fred(\mathscr{H})$ are in [[natural bijection]] with $K(X)$

\[
  \label{IndexMap}
  \pi_0 \, 
  Map\big(
    X,
    \,
    Fred(\mathscr{H})
  \big)
  \xrightarrow[\sim]{\phantom{-}ind_X\phantom{-}}
  K(X)
  \,,
\]

where $ind_X$ forms the *index bundle*, an $X$-parameterized enhancement of the [[Fredholm index]] (see Prop. \ref{IndexViaVirtualKernelBundlesOfConstantDimPerturbation} below).

This statement generalizes:

1. to any degrees and to [[KO-theory]] ([Atiyah & Singer 1969 Thm. B](#AtiyahSinger1969), [Karoubi 1970 Lem 1.4 & Prop. 1.5](#Karoubi1970)), given by maps to Fredholm operators satisfying further (anticommutation) conditions,

1. to a definition of [[twisted K-theory]] and of [[equivariant K-theory]] (hence of [[twisted equivariant K-theory]]), given by homotopy classes of [[sections]] of $Fred(\mathscr{H})$-[[fiber bundles]] ([Atiyah & Segal 2004](#AtiyahSegal04)).


## Statement
 {#Statement}

The original Atiyah-Jänich theorem theorem concerns complex [[topological K-theory]], $K(-) = KU^0(-)$ in degree 0 (and hence in any [[even number|even]] degree), see:

* [Statement for $KU^0$](#StatementForKU0).

Generalization to any degree and to [[KO-theory]] is due to [Atiyah & Singer 1969](#AtiyahSinger1969), [Karoubi 1970](#Karoubi1970), see:

* [Statement for $KU^1$](#StatementForKU1).


### For $KU^0$
 {#StatementForKU0}


\begin{proposition}
\label{KernelBundles}
  If $f \colon X \longrightarrow Fred(\mathscr{H})$ is such that the [[dimension of a vector space|dimension]] of the [[kernels]] of $f(x)$ is [[locally constant function|locally constant]], hence that they form a [[continuous map]] to the [[integers]]
$$
  dim\Big(
    ker\big(
     f(-)
    \big)
  \Big)
  \,\colon\, 
  X \longrightarrow \mathbb{Z}
$$
then the collection of [[kernels]] and [[cokernels]] themselves, as [[subspaces]] of $X \times \mathscr{H}$, form [[topological vector bundles]]
$$
  ker\big(
    f(-)
  \big),
  \;
  coker\big(
    f(-)
  \big)
  \in
  \mathbb{C}Vec_{X}
  \,.
$$

\end{proposition}

([Jänich 1965 Lemma 4](#Jänich65)).

\begin{proposition}
\label{ConstantKernelDeformationsExist}
Every [[continuous map]] $f \colon X \longrightarrow Fred(\mathscr{H})$ is [[homotopy|homotopic]] to a map $f'$ for which $dim\big(ker(f')\big)$ is continuous.
\end{proposition}
([Jänich 1965 below Lemma 4 using Lemma 3](#Jänich65)).


\begin{proposition}
\label{IndexViaVirtualKernelBundlesOfConstantDimPerturbation}
The index (eq:IndexMap) is given by

$$
  \begin{array}{ccc}
    \pi_0 Map\big(X,Fred(\mathscr{H})\big)
      &\xrightarrow{ ind_X }&
    K(X)
    \\
    [f]  
      &\mapsto&
    \big[ker(f') \ominus coker(f')\big]
    \mathrlap{\,,}
  \end{array}
$$

where $f'$ is any representative of the class $[f]$ according to Prop. \ref{ConstantKernelDeformationsExist}, $ker(f')$ and  $coker(f')$ are its (co)kernel bundles according to Prop. \ref{KernelBundles}, and $(-) \ominus (-)$ is their their [[virtual vector bundle|virtual difference bundle]].
\end{proposition}
([Jänich 1965 Lemma 5](#Jänich65))

\begin{remark}
  The construction of the index map (eq:IndexMap) by [Atiyah 1967 Lem A3, Cor A4](#Atiyah67) is a little different (though the result, of course, is the same). Exposition is in [Sheth §2](#Sheth).
\end{remark}

### For $KU^1$
 {#StatementForKU1}

\begin{proposition}
  The space of [[self-adjoint operator|self-adjoint]] [[Fredholm operators]] 
  $$
    Fred^{sa}
    \subset
    \Big\{
      F \in Fred 
      \;\Big\vert\;
      F^\dagger = F
    \Big\}
  $$
  has three [[connected components]]
  $$
    Fred^{sa}
    \;\simeq\;
    Fred_+^{sa}
    \,\sqcup\,
    Fred_-^{sa}
    \,\sqcup\,
    Fred_\ast^{sa}
    \mathrlap{\,,}
  $$
  corresponding to those Fredholm operators whose [[essential spectrum]] (which is [[real number|real]], by [[self-adjoint operator|self-adjointness]]) is, respectively:

  1. $Fred_+^{sa}$: purely [[positive number|positive]],

  1. $Fred_-^{sa}$: purely [[negative number|negative]],

  1. $Fred_{\ast}^{sa}$: both, hence [[inhabited set|nonempty]] both above and below [[zero]].

Moreover, 

1. the first two components are [[contractible topological space|contractible]]

   $$
     Fred^{sa}_{\pm} \simeq \ast
     \,,
   $$

1. the last component is [[homotopy equivalence|homotoppy equivalent]] to the [[stable unitary group]], hence the [[classifying space]] for [[topological K-theory]] in odd degree:

   $$
     Fred^{sa}_{\ast} \simeq U \simeq KU_1
     \,.
   $$

\end{proposition}
Up to some straightforward reidentifications (for instance one may equivalently use *skew* self-adjoint operators whose spectrum is then purely [[imaginary number|imaginary]]), this is the statement of [Atiyah & Singer 1969 Thm. B](#AtiyahSinger1969) and [Karoubi 1970 Lem 1.4 & Prop. 1.5](#Karoubi1970).



## Examples

\begin{example}
  For discussion of the [[basic complex line bundle on the 2-sphere]] realized as a Fredholm index bundle see [there](basic+complex+line+bundle+on+the+2-sphere#AsAFredholmIndexBundle). 
\end{example}


## References

The original articles:

* {#Jänich65} [[Klaus Jänich]]: *Vektorraumbündel und der Raum der Fredholm-Operatoren*, Mathematische Annalen **161** (1965) 129–142 &lbrack;[doi:10.1007/BF01360851](https://doi.org/10.1007/BF01360851)&rbrack;

* {#Atiyah67}  [[Michael Atiyah]], Thm. A.1 in: *K-theory*, Harvard Lecture 1964 (notes by D. W. Anderson), Benjamin (1967) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahk.pdf), [[AtiyahKTheory.pdf:file]]&rbrack;

* {#Atiyah69} [[Michael Atiyah]], §2 in: *Algebraic Topology and Operators in Hilbert Space*, in: *Lectures in Modern Analysis and Applications I*, Lecture Notes in Mathematics **103**, Springer (1969) 101-121 &lbrack;[doi:10.1007/BFb0099987](https://doi.org/10.1007/BFb0099987), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/atiyah002.pdf), [[Atiyah-AlgTopAndOperators.pdf:file]]&rbrack;


Generalization to general degree and to [[KO-theory]]:

* {#AtiyahSinger1969} [[Michael F. Atiyah]], [[Isadore M. Singer]]: *Index theory for skew-adjoint Fredholm operators*, Publications Mathématiques de l'IHÉS **37** (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [numdam:PMIHES_1969__37__5_0](https://www.numdam.org/item/PMIHES_1969__37__5_0), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/askew.pdf)&rbrack;

* {#Karoubi1970} [[Max Karoubi]]: *Espaces Classifiants en K-Théorie*, Trans. Amer. Math. Soc. **147** (1970) 75-115 &lbrack;[doi:10.2307/1995218](https://doi.org/10.2307/1995218), [jstor:1995218](https://www.jstor.org/stable/1995218)&rbrack;


In monographs:

* {#Karoubi78} [[Max Karoubi]], §I.7.10 in: _K-Theory -- An Introduction_, Grundlehren der mathematischen Wissenschaften **226**, Springer (1978) &lbrack;[pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3)&rbrack;
  > (related discussion)

Lecture notes:

* {#Sheth} Arshay Sheth: *The Atiyah-Jänich Theorem* &lbrack;[pdf](https://warwick.ac.uk/fac/sci/maths/people/staff/sheth/report_talk12_arshaysheth.pdf), [[Sheth-AtiyahJanich.pdf:file]]&rbrack;


As the basis of a definition of [[twisted K-theory]] and [[equivariant K-theory]] and [[twisted equivariant K-theory]]:

* {#AtiyahSegal04} [[Michael Atiyah]], [[Graeme Segal]], _Twisted K-theory_, Ukrainian Math. Bull. **1** 3 (2004) &lbrack;[arXiv:math/0407054](http://arxiv.org/abs/math/0407054), [journal page](http://iamm.su/en/journals/j879/?VID=10), [published pdf](http://iamm.su/upload/iblock/45e/t1-n3-287-330.pdf)&rbrack;

See also:

* [[Byungdo Park]]: *The Atiyah-Jänich theorem and its twisted refinement -- An introduction to category theory for freshmen*, talk notes (2018) &lbrack;[pdf](https://byungdo.github.io/slides/2018-03-13_incheonU_printerfriendly.pdf), [[Park-AJTheorem.pdf:file]]&rbrack;

Further development:

* Kamran Sharifi: *Atiyah-Jänich theorem for  $\sigma$-$C^\ast$-algebras* &lbrack;[arXiv:1612.03287](https://arxiv.org/abs/1612.03287)&rbrack;



[[!redirects Atiyah-Janich theorem]]
[[!redirects Atiyah-Jaenich theorem]]
