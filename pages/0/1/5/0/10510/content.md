
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

> The [[point-set topology]] of parametrized spaces is surprisingly subtle. $[$[MaSi06, p. 15](#MaySigurdsson06)$]$

### Fiberwise mapping spaces
 {#FiberwiseMappingSpaces}

> Parametrized mapping spaces are especially delicate $[$[MaSi06, p. 15](#MaySigurdsson06), see Rem. \ref{FibMapSpaceDoesNotPreserveWeakHausdorffness} below$]$

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

We consider [[pointed objects]] 

$$
  (X, p_X, \sigma_X) \;\in\; \big( kTop_{/B}\big)^{B/} \;=\; kTop_{/B}^{B/} 
$$

in the [[slice category]] of such a base space -- hence topological "[[bundles]]" $X \xrightarrow{p_X} B$ (in the most general sense, without any condition on the bundle projection, except [[continuous function|continuity]]) equipped with a fixed [[section]] $\sigma_X$ (sometimes called "ex-spaces", see $[$[MaSi06, p. 19, footnote 1](#MaySigurdsson06)$]$).

\begin{definition}{#PartialMapClassifierSpace}
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
      Map(X, \iota_A)
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

(This is  [MaSi06, Def. 1.3.7](#MaySigurdsson06), following [Booth & Brown 1978a](#BoothBrown78a)).



\begin{remark}
**(on notation)**
\linebreak
Contrary to most references, Def. \ref{FiberwiseMappingSpace} is intentionally not using a subsript "${}_B$" in the notation for the fiberwise mapping space: This is because "$Map(X,A)_B$" is also standard notation for $Map(X,A) \underset{Map(X,B)}{\times} \{p_B\}$ (see e.g. at *[[space of sections]]*), which is crucially different. Instead, with the above notation, $Map(-,-)$ is always of the same [[type]] as its arguments, as befits an [[internal hom]].
\end{remark}

\begin{remark}\label{FibMapSpaceDoesNotPreserveWeakHausdorffness}
**(fiberwise mapping space does not preserve weak Hausdorffness)**
\linebreak
  Even if $X$ and $A$ are [[weak Hausdorff spaces]] over the weak Hausdorff space $B$ (eq:kwHausBaseSpace), their
  fiberwise mapping space (Def. \ref{FiberwiseMappingSpace}) need  not be weak Hausdorff ([Booth & Brown 1974a](#BoothBrown74a)). Sufficient conditions for this to be the case are given in [Lewis 1985, Prop. 1.5](#Lewis85) 

On the other hand, the suitable [[cofibrant resolution]] of the fiberwise mapping space will again be weak Hausdorff (see [MaSi06, p. 19](#MaySigurdsson06)).
\end{remark}


\begin{proposition}
**(fiberwise mapping space satisfies the exponential law)**
\linebreak
  With $B$ as above (eq:kwHausBaseSpace),
  the fiberwise mapping space (Def. \ref{FiberwiseMappingSpace}) is an [[exponential object]] (satisfies the [[exponential law for spaces|exponential law]]) in that there is a [[natural isomorphism]] of [[hom-sets]]
$$
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
$$
(where on the right we have the [[Cartesian product]] in the [[slice category|slice]], given by the [[fiber product]] $X \times_B Y$ in $kTop$).
\end{proposition}
([Booth & Brown 1978a, Thm. 3.5](#BoothBrown78a), see [MaSi06, (1.3.9)](#MaySigurdsson06))


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





## Related concepts

* [[rational parametrized homotopy theory]]

  * [[rational fibration lemma]]

* [[rational parameterized stable homotopy theory]]

## References


[[!include exponential law for parameterized topological spaces -- references]]



### Parameterized ("fiberwise") homotopy theory

On the [[homotopy theory]] of such parameterized topological spaces:

* [[Ioan Mackenzie James]], §IV of: *Fibrewise topology*, Cambridge Tracts in Mathematics, Cambridge University Press (1989) $[$ISBN:9780521360906$]$

* [[Ioan Mackenzie James]], _[[Introduction to fibrewise homotopy theory]]_, in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_ (1995)

* [[Michael C. Crabb]], [[Ioan Mackenzie James]]: *Fiberwise homotopy theory*, Springer Monographs in Mathematics, Springer (1998) $[$[doi:10.1007/978-1-4471-1265-5](https://doi.org/10.1007/978-1-4471-1265-5), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/crabbjames.pdf) ,[pdf](https://www.gbv.de/dms/ilmenau/toc/243540361.PDF)$]$

On respective [[model category]]-structures:

* {#MaySigurdsson06} [[Peter May]], [[Johann Sigurdsson]], _[[Parametrized Homotopy Theory]]_,  Mathematical Surveys and Monographs, vol. 132, AMS 2006   ([ISBN:978-0-8218-3922-5](https://bookstore.ams.org/surv-132), [arXiv:math/0411656](https://arxiv.org/abs/math/0411656), [pdf](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf))

  
A formulation of aspects of this in [[(∞,1)-category theory]] is in 

* {#AndoBlumbergGepner11} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Parametrized spectra, multiplicative Thom spectra, and the twisted Umkehr map_, Geom. Topol. 22 (2018) 3761-3825 ([arXiv:1112.2203](http://arxiv.org/abs/1112.2203))
  
Discussion of convenient [[model category]] [[presentable (infinity,1)-category|presentations]]:

* {#BraunackMayer19} [[Vincent Braunack-Mayer]], _Combinatorial parametrised spectra_, based on the [[schreiber:thesis Braunack-Mayer|PhD thesis]] ([arXiv:1907.08496](https://arxiv.org/abs/1907.08496))


[[!redirects parametrized homotopy theory]]

[[!redirects fiberwise homotopy theory]]
[[!redirects fibrewise homotopy theory]]

[[!redirects parameterized stable homotopy theory]]
[[!redirects parametrised stable homotopy theory]]
[[!redirects parametrized stable homotopy theory]]

[[!redirects parameterized topology]]
[[!redirects fiberwise topology]]
[[!redirects fibrewise topology]]


