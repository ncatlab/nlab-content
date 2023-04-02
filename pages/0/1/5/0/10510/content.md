
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Parameterized ([[stable homotopy theory|stable]]) [[homotopy theory]] is ([[stable homotopy theory|stable]]) [[homotopy theory]] of [[bundles]] of [[homotopy types]]/[[stable homotopy types]] over a given base space.

For formalizations see also at

* [[ex-space]]

* [[parameterized spectrum]], [[excisive functor]]

* [[(infinity,1)-module bundle]]

* [[tangent (infinity,1)-topos]]

* [[twisted cohomology]]

## Parameterized point-set topology

> The [[point-set topology]] of parametrized spaces is surprisingly subtle. &lbrack;[May & Sigurdsson 2006, p. 15](#MaySigurdsson06)&rbrack;

Write:

* $kTop$ for the [[convenient category of topological spaces|convenient category]] of [[compactly generated topological spaces]] (k-spaces)

* $kwHaus \subset Top_k$ for that of [[compactly generated weak Hausdorff spaces]].

For $B \,\in\, \mathcal{C}$ an [[object]] in any [[category]], write $\mathcal{C}_{/B}$ for the [[slice category]] over it.

In the following all bases spaces are assumed (as in [MaSi06, p. 19](#MaySigurdsson06)) to be [[compactly generated weak Hausdorff spaces]] regarded among k-spaces:

\[
  \label{kwHausBaseSpace}
  B \;\in\; kwHaus \xhookrightarrow{\;} kTop
  \,.
\]

Notice that for $(X,p_X), (Y,p_Y) \,\in\, kTop_{/B}$, their [[Cartesian product]] in the [[slice category]] is given by the [[fiber product]] in [[compactly generated topological space|$kTop$]]:

$$
  (X,p_X) \times (Y, p_Y)
  \;\simeq\;
  \big(
    X \times_B Y
    ,\,
    p_X \circ pr_X
    =
    p_Y \circ pr_Y
  \big)
  \;\;\;
  \in
  \;
  kTop_{/B}
$$

For $f \,\colon\, B_1 \xrightarrow{\;\;} B_2$ a [[continuous map]] between such base spaces,
notice the usal [[base change]] [[adjoint triple]]:

\[\label{BaseChangeAdjointTriple}\]
\begin{tikzcd}
  \mathrm{kTop}_{/B_1}
    \ar[
      rr,
      shift left=20pt,
      "{f_!}"{description}
    ]
    \ar[
      from=rr,
      "{f^\ast}"{description}
    ]
    \ar[
      rr,
      shift right=20pt,
      "{f_\ast}"{description}
    ]
    \ar[rr, phantom, shift left=10pt, "{\scalebox{.6}{$\bot$}}"]
    \ar[rr, phantom, shift right=10pt, "{\scalebox{.6}{$\bot$}}"]
  &&
  \mathrm{kTop}_{/B_2}
  \,,
\end{tikzcd}

where

1. $f^\ast$ is [[pullback]] in $kTop$ along $f$;

1. $f_!$ is post-[[composition]] with $f$;

Notice the "[[Frobenius reciprocity]] law" (in its [[cartesian monoidal category|cartesian]] version [here](Frobenius+reciprocity#InCategoryTheory)) which follows immediately by the [[pasting law]] in $kTop$, namely the following [[natural isomorphism]]:

\[
  \label{CartesianFrobeniusReciprocity}
  f_!
  \big(
    (U,p_U)
    \times
    f^\ast (X,p_X)
  \big)
  \;\simeq\;
  \big(
    f_!(U,p_U)
  \big)
  \times
  (X,p_X)
  \,.
\]

In the special case where $f$ is the [[terminal object|terminal]] map to the [[point space]], which we denote

$$
  p_B \,\colon\, B \xrightarrow{\;} \ast
  \,.
$$

we have $kTop_{/\ast} \,\simeq\, kTop$ and the above [[base change]] [[adjoint triple]] becomes

\[\label{TerminalBaseChange}\;\]
\begin{tikzcd}
  \mathrm{kTop}_{/B}
    \ar[
      rr,
      shift left=20pt,
      "{(p_B)_!}"{description}
    ]
    \ar[
      from=rr,
      "{(p_B)^\ast}"{description}
    ]
    \ar[
      rr,
      shift right=20pt,
      "{(p_B)_\ast}"{description}
    ]
    \ar[rr, phantom, shift left=10pt, "{\scalebox{.6}{$\bot$}}"]
    \ar[rr, phantom, shift right=10pt, "{\scalebox{.6}{$\bot$}}"]
  &&
  \mathrm{kTop}
  \,,
\end{tikzcd}

In this case

1. the functor $(p_B)^\ast$ is the [[Cartesian product]] with $B$, regarded as the trivial fibration:

   \[
     \label{TrivialFibration}
     (p_B^\ast) X_0
     \;=\;
     B \times X_0 \xrightarrow{\; pr_B \;} B
     \,,
   \]

1. $(p_B)_!$ gives the total space of a fibration:

   $$
     (p_B)_! \big( X \to B\big) \;=\; X
   $$

1. $(p_B)_*$ gives the [[space of sections]] of a fibration.


Eventually we consider [[pointed objects]]

$$
  (X, p_X, \sigma_X) \;\in\; \big( kTop_{/B}\big)^{B/} \;=\; kTop_{/B}^{B/}
$$

in the [[slice category]] of such a base space -- hence topological "[[bundles]]" $X \xrightarrow{p_X} B$ (in the most general sense, without any condition on the bundle projection, except [[continuous function|continuity]]) equipped with a fixed [[section]] $\sigma_X$ (sometimes called "ex-spaces", see &lbrack;[May & Sigurdsson 2006, p. 19, footnote 1](#MaySigurdsson06)&rbrack;).


### Fiberwise mapping spaces
 {#FiberwiseMappingSpaces}

> Parametrized mapping spaces are especially delicate &lbrack;[May & Sigurdsson 2006, p. 15](#MaySigurdsson06), see Rem. \ref{FibMapSpaceDoesNotPreserveWeakHausdorffness} below&rbrack;


\begin{definition}\label{PartialMapClassifierSpace}
**(partial map classifier space)**
\linebreak
  For $X \,\in\, kTop$, write $\widetilde X \,\in\, kTop$ for its continuous [[partial map classifier]]: The result of forming the [[disjoint union]] of the [[underlying]] [[set]] of $X$ with a [[singleton set]] $\{\bot\}$  and declaring the [[closed subsets]] on the result to be those of $X$ under the defining [[injection]]
$$
  X \xhookrightarrow{\;\; \iota_X \;\;} \widetilde{X}
$$
together with $\widetilde{X}$ itself.

\end{definition}

([MaSi06, Def. 1.3.6](#MaySigurdsson06))


\begin{definition}\label{FiberwiseMappingSpace}
**(fiberwise mapping space)**
\linebreak
For
$$
  (X, p_X),
  \,
  (A,p_A)
  \;\in\;
  kTop_{B}
$$
a [[pair]] of [[k-spaces]] over $B$ (eq:kwHausBaseSpace)
their *fiberwise mapping space* is the [[pullback]] (in $kTop$):
\[
  \label{FiberwiseMappingSpaceAsPullback}
  \array{
    \phantom{---}
    \mathclap{
    Map
    \big(
       (X,p_X)
       ,\,
       (A,p_A)
    \big)
    }
    \phantom{---}
    &\xrightarrow{\phantom{-------}}&
    Map
    \big(
      X,
      \widetilde{A}
    \big)
    \\
    \big\downarrow
    &{}_{{}^{(pb)}}&
    \big\downarrow{}^{\mathrlap{
      Map
      \big(
        X, \widetilde{p_A}
      \big)
    }}
    \\
    B
    &
    \underset{
     b \mapsto
     \left(
       x
       \mapsto
       \left\{
         \begin{array}{ll}
           b & if\, x \in X_b
           \\
           \bot & otherwise
         \end{array}
       \right.
     \right)
    }{\longrightarrow}
    &
    Map
    \big(
      X,
      \widetilde{B}
    \big)
    \,,
  }
\]
regarded as an object of $kTop_{/B}$.

Here $Map(X,\widetilde{A})$ denotes the ordinary [[compact-open topology|mapping space]] into the continuous partial map classifier from Def. \ref{PartialMapClassifierSpace}.
\end{definition}

(This is  [May & Sigurdsson 2006, Def. 1.3.7](#MaySigurdsson06), following [Booth & Brown 1978a](#BoothBrown78a)).



\begin{remark}
**(on notation)**
\linebreak
Contrary to most references, Def. \ref{FiberwiseMappingSpace} is intentionally not using a subsript "${}_B$" in the notation for the fiberwise mapping space: This is because "$Map(X,A)_B$" is also standard notation for $Map(X,A) \underset{Map(X,B)}{\times} \{p_B\}$ (see e.g. at *[[space of sections]]*), which is crucially different. Instead, with the above notation, $Map(-,-)$ is always of the same [[type]] as its arguments, as befits an [[internal hom]].
\end{remark}

\begin{proposition}\label{FiberwiseMappingSpaceSatisfiesExponentialLaw}
**(fiberwise mapping space satisfies the exponential law)**
\linebreak
  With $B$ as above (eq:kwHausBaseSpace),
  the fiberwise mapping space (Def. \ref{FiberwiseMappingSpace}) is an [[exponential object]] (satisfies the [[exponential law for spaces|exponential law]]) in that there is a [[natural isomorphism]] of [[hom-sets]]
\[
  \label{ExponentialLawForFiberwiseMappingSpace}
  kTop_{/B}
  \Big(
    (X,p_X)
    ,\,
    Map
    \big(
      (Y,p_Y)
      ,\,
      (A,p_A)
    \big)
  \Big)
  \;\;
  \simeq
  \;\;
  kTop_{/B}
  \big(
    (X,p_X) \times (Y,p_Y)
    ,\,
    (A,p_A)
  \big)
\]
(where on the right we have the [[Cartesian product]] in the [[slice category|slice]], given by the [[fiber product]] $X \times_B Y$ in $kTop$).
\end{proposition}
([Booth & Brown 1978a, Thm. 3.5](#BoothBrown78a), see [May & Sigurdsson 2006, (1.3.9)](#MaySigurdsson06))

\begin{example}\label{FiberwiseMappingSpaceBetweenTrivialFibrations}
**(fiberwise mapping space between trivial fibrations)**
\linebreak
  The fiberwise mapping space (Def. \ref{FiberwiseMappingSpace})
between trivial fibrations (eq:TrivialFibration) is the trivial fibration with fiber the ordinary [[compact-open topology|mapping space]] between the fibers:
$$
  Map
  \big(
     p_B^\ast X_0
     ,\,
     p_B^\ast A_0
  \big)
  \;\simeq\;
  p_B^\ast
  Map\big(X_0,\, A_0\big)
  \,.
$$
\end{example}
\begin{proof}
  This may be gleaned concretely from [[point-set topology|point-set]]-analysis of the defining pullback diagram (eq:FiberwiseMappingSpaceAsPullback), but it also follows abstractly by [[adjunction|adjointness]] from the [[exponential law]] (Prop. \ref{FiberwiseMappingSpaceSatisfiesExponentialLaw}):

For any $(U, p_U) \,\in\, kTop_{/B}$ we have the following sequence of [[natural isomorphisms]]:
$$
  \begin{aligned}
    &
    kTop_{/B}
    \Big(
      (U, p_U)
      ,\,
      \Map
      \big(
        p_B^\ast X_0
        ,\,
        p_B^\ast A_0
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \big(
      (U, p_U) \times (B \times X_0, pr_{B})
      ,\,
      p_B^\ast A_0
    \big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \big(
      (U \times X_0, p_U \circ pr_U)
      ,\,
      p_B^\ast A_0
    \big)
    \\
    &
    \;\simeq\;
    kTop
    \Big(
      U \times X_0
      ,\,
      A_0
    \big)
    \\
    &
    \;\simeq\;
    kTop
    \Big(
      U
      ,\,
      Map
      \big(
        X_0
        ,\,
        A_0
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop
    \Big(
      (p_B)_!
      (U,p_U)
      ,\,
      Map
      \big(
        X_0
        ,\,
        A_0
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      (U,p_U)
      ,\,
      p_B^\ast
      Map
      \big(
        X_0
        ,\,
        A_0
      \big)
    \Big)
  \end{aligned}
$$
Here most steps are [Hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the various [[adjoint functors]]: (eq:TerminalBaseChange) and (eq:ExponentialLawForFiberwiseMappingSpace).
Since this holds naturally for all $(U, p_U)$, the claim follows by the [[Yoneda lemma]] (over the [[large category]] $\big(kTop_{/B}\big)^{op}$).
\end{proof}

Similarly:

\begin{proposition}\label{PullbackOfFiberwiseMappingSpace}
**(pullback of fiberwise mapping space)**
\linebreak
For $f \,\colon\, B' \longrightarrow B$ a [[map]] of base spaces (eq:kwHausBaseSpace), the [[pullback]] (eq:BaseChangeAdjointTriple) along $f$ of the fiberwise mapping space (Def. \ref{FiberwiseMappingSpace}) is the fiberwise mapping space of the pullback of the arguments:
$$
  f^\ast
  Map
  \big(
    (X,p_X)
    ,\,
    (A, p_A)
  \big)
  \;\;
  \simeq
  \;\;
  Map
  \big(
    f^\ast
    (X,p_X)
    ,\,
    f^\ast
    (A, p_A)
  \big)
  \,.
$$
In other words: Pullback $f^\ast$ is a [[closed functor]] with respect to fiberwise mapping spaces.
\end{proposition}
\begin{proof}
For any $(U, p_U) \,\in\, kTop_{/B'}$ we have the following sequence of [[natural isomorphisms]]:
$$
  \begin{aligned}
    &
    kTop_{/B'}
    \Big(
      (U,p_U)
      ,\,
      f^\ast
      Map
      \big(
        (X,p_X)
        ,\,
        (A,p_A)
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      f_! (U,p_U)
      ,\,
      Map
      \big(
        (X,p_X)
        ,\,
        (A,p_A)
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      \big(
        f_!(U, p_U)
      \big)
      \times
      (X, p_X)
      ,\,
      (A,p_A)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      f_!
      \big(
        (U, p_U)
        \times
        f^\ast (X, p_X)
      \big)
      ,\,
      (A,p_A)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B'}
    \Big(
        (U, p_U)
        \times
        f^\ast (X, p_X)
      ,\,
      f^\ast
      (A,p_A)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B'}
    \Big(
      (U, p_U)
      ,\,
      Map
      \big(
        f^\ast (X, p_X)
        ,\,
        f^\ast (A,p_A)
      \big)
    \Big)
  \end{aligned}
$$
Here the crucial step, besides various [Hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism), is the use of Cartesian "[[Frobenius reciprocity]]" (eq:CartesianFrobeniusReciprocity).

Since these isomorphism are [[natural isomorphism|natural]] in $(U,p_U)$, the claim follows by the [[Yoneda embedding]] (for the [[large category]] $\big( kTop_{/B'}\big)^{op}$).
\end{proof}
,


\begin{example}\label{FiberOfFiberwiseMappingSpace}
**(fiber of fiberwise mapping space is mapping space of fibers)**
\linebreak
  For $b \in B$, the [[fiber]] of the fiberwise mapping space fibration (Def. \ref{FiberwiseMappingSpace}) is [[homeomorphism|homemorphic]] to the ordinary [[compact-open topology|mapping space]] betwee the [[fibers]]:
$$
  Map
  \big(
    (X,p_x)
    ,\,
    (A,p_A)
  \big)_b
  \;\;
  \simeq
  \;\;
  Map
  \big(
    X_b
    ,\,
    A_b
  \big)
  \,.
$$
\end{example}
(e.g. [May & Sigurdsson 2006, p. 21](#MaySigurdsson06))
\begin{proof}
  This is immediate from concrete analysis of the defining [[pullback]]-diagram (eq:FiberwiseMappingSpaceAsPullback) in Def. \ref{FiberwiseMappingSpace}, but it is also the special case of Prop. \ref{PullbackOfFiberwiseMappingSpace} for $B = \{b\}$.
\end{proof}



### Homotopy theory of the fiberwise mapping space

\begin{proposition}\label{FiberwiseMappingSpacePreservesHFibrations}
**(fiberwise mapping space preserves h-fibrations)**
\linebreak
  If $p_X \colon X \to B$
  and $p_A \colon A \to B$
  are [[Hurewicz fibrations]], then so is the map (eq:FiberwiseMappingSpaceAsPullback) out of their fiberwise mapping space (Def. \ref{FiberwiseMappingSpace}):
$$
  p_X, p_A \,\in\, hFib
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  p_{ Map\big( (X,p_X) , (A,p_A)\big) }
  \;\in\;
  hFib
  \,.
$$
\end{proposition}
(This is due to [Booth 1970, §6.1](#Booth70), see [MaSi06, Prop. 1.3.11](#MaySigurdsson06).)

\begin{remark}\label{FibMapSpaceDoesNotPreserveWeakHausdorffness}
**(fiberwise mapping space does not preserve weak Hausdorffness)**
\linebreak
  Even if $X$ and $A$ are [[weak Hausdorff spaces]] over the weak Hausdorff space $B$ (eq:kwHausBaseSpace), their
  fiberwise mapping space (Def. \ref{FiberwiseMappingSpace}) need  not be weak Hausdorff ([Booth & Brown 1974a](#BoothBrown74a)). Sufficient conditions for this to be the case are given in [Lewis 1985, Prop. 1.5](#Lewis85)

On the other hand, the suitable [[cofibrant resolution]] of the fiberwise mapping space will again be weak Hausdorff (see [MaSi06, p. 19](#MaySigurdsson06)).
\end{remark}




## Related concepts

* [[retractive space]]

* [[parameterized spectrum]]

* [[model structure for parameterized spectra]]

* [[rational parametrized homotopy theory]]

  * [[rational fibration lemma]]

* [[rational parameterized stable homotopy theory]]


## References


[[!include exponential law for parameterized topological spaces -- references]]



### Parameterized ("fiberwise") homotopy theory

On the [[homotopy theory]] of such parameterized topological spaces:

* [[Ioan Mackenzie James]], §IV of: *Fibrewise topology*, Cambridge Tracts in Mathematics, Cambridge University Press (1989) &lbrack;ISBN:9780521360906&rbrack;

* [[Ioan Mackenzie James]], _[[Introduction to fibrewise homotopy theory]]_, in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_ (1995)

* [[Michael C. Crabb]], [[Ioan Mackenzie James]]: *Fiberwise homotopy theory*, Springer Monographs in Mathematics, Springer (1998) &lbrack;[doi:10.1007/978-1-4471-1265-5](https://doi.org/10.1007/978-1-4471-1265-5), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/crabbjames.pdf) ,[pdf](https://www.gbv.de/dms/ilmenau/toc/243540361.PDF)&rbrack;

On [[model structures for parameterized spectra]]:

* {#MaySigurdsson06} [[Peter May]], [[Johann Sigurdsson]], _[[Parametrized Homotopy Theory]]_,  Mathematical Surveys and Monographs, vol. 132, AMS 2006   ([ISBN:978-0-8218-3922-5](https://bookstore.ams.org/surv-132), [arXiv:math/0411656](https://arxiv.org/abs/math/0411656), [pdf](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf))

* {#BraunackMayer19} [[Vincent Braunack-Mayer]], *Combinatorial parametrised spectra*, Algebr. Geom. Topol. **21** (2021) 801-891 &lbrack;[arXiv:1907.08496](https://arxiv.org/abs/1907.08496), [doi:10.2140/agt.2021.21.801](https://doi.org/10.2140/agt.2021.21.801)&rbrack;

  > (based on the [[schreiber:thesis Braunack-Mayer|PhD thesis]])

* [[Fabian Hebestreit]], [[Steffen Sagave]], [[Christian Schlichtkrull]], *Multiplicative parametrized homotopy theory via symmetric spectra in retractive spaces*, Forum of Mathematics, Sigma **8** (2020) e16 &lbrack;[arXiv:1904.01824](https://arxiv.org/abs/1904.01824), [doi:10.1017/fms.2020.11](https://doi.org/10.1017/fms.2020.11)&rbrack;


* [[Cary Malkiewich]], *Parametrized spectra, a low-tech approach* &lbrack;[arXiv:1906.04773](https://arxiv.org/abs/1906.04773), user guide: [pdf](https://people.math.binghamton.edu/malkiewich/users_guide_parametrized.pdf), [[Malkiewich-ParametrizedSpectraUserGuide.pdf:file]]&rbrack;


Discussion in [[(∞,1)-category theory]]:

* {#AndoBlumbergGepner11} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Parametrized spectra, multiplicative Thom spectra, and the twisted Umkehr map_, Geom. Topol. 22 (2018) 3761-3825 ([arXiv:1112.2203](http://arxiv.org/abs/1112.2203))



Discussion as a [[linear homotopy type theory]]:

* {#Schreiber14} [[Urs Schreiber]], _[[schreiber:Quantization via Linear homotopy types]]_ &lbrack;[arXiv:1402.7041](http://arxiv.org/abs/1402.7041)&rbrack;

  > (intended [[categorical semantics]])

* [[Mitchell Riley]], [[Eric Finster]], [[Daniel R. Licata]], *Synthetic Spectra via a Monadic and Comonadic Modality* &lbrack;[arXiv:2102.04099](https://arxiv.org/abs/2102.04099)&rbrack;

  > ([[inference rules]] for the [[classical modality]] $\natural$)

* {#Riley22Thesis} [[Mitchell Riley]], *A Bunched Homotopy Type Theory for Synthetic Stable Homotopy Theory*, PhD Thesis (2022) &lbrack;[doi:10.14418/wes01.3.139](https://doi.org/10.14418/wes01.3.139), [ir:3269](https://digitalcollections.wesleyan.edu/object/ir%3A3269),  [pdf](https://mvr.hosting.nyu.edu/pubs/thesis.pdf)&rbrack;

  > (including [[inference rules]] for the [[multiplicative conjunction]] by bringing in the required [[bunched logic]])




[[!redirects parametrized homotopy theory]]

[[!redirects fiberwise homotopy theory]]
[[!redirects fibrewise homotopy theory]]

[[!redirects parameterized stable homotopy theory]]
[[!redirects parametrised stable homotopy theory]]
[[!redirects parametrized stable homotopy theory]]

[[!redirects parameterized topology]]
[[!redirects fiberwise topology]]
[[!redirects fibrewise topology]]

[[!redirects fiberwise mapping space]]
[[!redirects fiberwise mapping spaces]]



