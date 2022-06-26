
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The *Brown-Gersten property* is the statement that for certain [[Grothendieck topologies]] the [[homotopy descent]]-property for [[simplicial presheaves]] (i.e. their [[infinity-stack|$\infty$-stack]]-property) follows essentially (up to a simple condition on connected components) already as soon as the given [[simplicial presheaf]] $\mathcal{F}$ satisfies a [Mayer-Vietoris-type property](Whitehead-generalized+cohomology#MayerVietorisSequenceInGeneralizedCohomology) in that for [[covering|covers]] by a [[pair]] of patches $U_1, U_2$ their [[fiber product]]-square is taken by $\mathcal{F}$ to a [[homotopy pullback]]-square.

This has traditionally been discussed over [[schemes]] (see [below](#OverSchemes)) but an analogous statement holds also over [[topological spaces]] and [[smooth manifolds]] (see [further below](#OverSmoothmanifolds)).

## Details

### Over schemes
 {#OverSchemes}

Detailed review in in [Jardine 2015, §5.4](#Jardine15).


### Over smooth manifolds
 {#OverSmoothmanifolds}

Write

* [[SmthMfd]] for the [[category]] of [[smooth manifolds]], regarded as a [[site]] via its [[Grothendieck topology]] of [[open covers]];

* $PSh\big(SmthMfd, sSet)\big)$ for the [[category of simplicial presheaves]] over smooth manifolds.

Recall (e.g. from *[[model structure on simplicial presheaves]]*) that a [[simplicial presheaf]] $\mathcal{F} \,\in\, Psh(SmthMfd, sSet)$ is said to be a [[local object]] or *satisfy [[homotopy descent]]* if for

* all [[smooth manifolds]] $X \in SmthMfd$;

* all its [[open covers]] $\big\{ U_i \hookrightarrow X \big\}_{i \in I}$ 

the canonical morphism of [[simplicial sets]] from the value of $\mathcal{F}$ on $X$ into the [[homotopy limit]] of the [[simplicial diagram]] over values of $\mathcal{F}$ on the [[Čech nerve]] of the cover 
\[
  \label{GeneralDescentProperty}
  \mathcal{F}(X)
  \xrightarrow{\phantom{----}}
  \underset{}{holim}
  \bigg(
    \underset{i \in I}{\prod}
    \mathcal{F}(U_i)
    \rightrightarrows
    \underset{i_1, i_2 \in I}{\prod}
    \mathcal{F}(U_{i_1} \cap U_{i_2})
    \cdots
  \bigg)
\]
is a [[simplicial weak equivalence]].


\begin{theorem}\label{BGPropertyForSmoothManifolds}
**(Brown-Gersten property over smooth manifolds, [Pavlov 2022, Thm. 1.1](#Pavlov22))**
\linebreak
  A simplicial presheaf $\mathcal{F} \,in\, PSh(SmthMfd, sSet)$ satisfies [[homotopy descent]] (eq:GeneralDescentProperty) for all open covers, as soon as it does so 

1. for open covers consisting of a [[pair]] of open subsets;

1. for open covers by pairwise [[disjoint]] patches (hence by [[connected components]]).

\end{theorem}

Notice here that 

1. in the case of an open cover by pair of patches 
   $$
     X \,\simeq\, U_1 \cup U_2
     \,,
   $$
   the [[homotopy descent]]-condition (eq:GeneralDescentProperty) reduces to saying that the   [[commuting square]] 

   $$
     \array{
       \mathcal{F}(X)
       &\longrightarrow&
       \mathcal{F}(U_1)
       \\
       \big\downarrow
       &&
       \big\downarrow
       \\
       \mathcal{F}(U_2)
       &\longrightarrow&
       \mathcal{F}(U_1 \cap U_2)
     }
   $$
   is a [[homotopy cartesian square]] (a [[homotopy pullback]]).

1. in the case of a cover by [[disjoint]] patches, hence $X \,\simeq\, \underset{i \in I}{\coprod} \, U_i$, the [[homotopy descent]]-condition (eq:GeneralDescentProperty) reduces to saying that 

   $$
     \mathcal{F}(X)
     \;\;\simeq\;\;
     \underset{i \in I}{\prod}
     \mathcal{F}(U_i)
   $$

   is a [[homotopy product]]. 

   In particular, if $X = \varnothing$ is the [[empty topological space|empty space]] covered by itself, this means that

   $$
     \mathcal{F}(\varnothing)
     \;\;\simeq\;\;  
     \ast
   $$

   is the [[terminal object]] (i.e. the simplicial presheaf which is constant on the [[singleton set]]).




## References

The original discussion for the [[Zariski topology]]:

* {#BrownGersten73} [[Kenneth S. Brown]], [[Stephen Gersten]], *Algebraic K-theory as generalized sheaf cohomology*, in: *Algebraic K-theory, I: Higher K-theories* (Proc. Conf., Battelle Memorial Inst., Seattle, Wash., 1972), pp. 266-292. Lecture Notes in Math. **341** Springer (1973) &#x5B;[doi:10.1007/BFb0067062](https://doi.org/10.1007/BFb0067062)]

Lecture notes on this case:

* [[J. F. Jardine]],  *Brown-Gersten and Nisnevich descent, motivic descent*, Lecture 13 of: [Lectures on Local Homotopy Theory](https://math.sci.uwo.ca/~jardine/LocalHom/)  &#x5B;[pdf](https://www.uwo.ca/math/faculty/jardine/courses/localhom/localhom-lecture13.pdf)]

The version for the [[Nisnevich topology]]:

* [[Fabien Morel]], [[Vladimir Voevodsky]], *$\mathbb{A}^1$-homotopy theory of schemes*, Publications Mathématiques de l'Institut des Hautes Études Scientifiques **90**  (1999) 45–143 &#x5B;[doi:10.1007/BF02698831](https://doi.org/10.1007/BF02698831)]

Detailed review of these two cases:

* {#Jardine15} [[John F. Jardine]], Section 5.4 of: *Local homotopy theory*, Springer Monographs in Mathematics (2015) &#x5B;[doi:10.1007/978-1-4939-2300-7](https://doi.org/10.1007/978-1-4939-2300-7)]


Generalization of these two cases to [[completely decomposable topology|completely decomposable topologies]]:

* {#Voevodsky10} [[Vladimir Voevodsky]], *Homotopy theory of simplicial presheaves in completely decomposable topologies*, Journal of Pure and Applied Algebra **214** 8 (2010) 1384-1398  &#x5B;[arXiv:0805.4578](https://arxiv.org/abs/0805.4578), [doi:10.1016/j.jpaa.2009.11.004](https://doi.org/10.1016/j.jpaa.2009.11.004)]

Discussion for [[numerable open covers]] of [[topological spaces]] and of [[smooth manifolds]] with application to [[smooth infinity-groupoids|smooth $\infty$-groupoids]] and their [[shape via cohesive path ∞-groupoids]]:

* {#Pavlov22} [[Dmitri Pavlov]], *Numerable open covers and representability of topological stacks* &#x5B;[arXiv:2203.03120](https://arxiv.org/abs/2203.03120)]

[[!redirects Brown-Gersten properties]]

[[!redirects Brown-Gersten condition]]
[[!redirects Brown-Gersten conditions]]

    

