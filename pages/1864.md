+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A concordance between [[cocycle]]s in [[cohomology]] is a relation similar to but different from a plain [[coboundary]], it is a "coboundary after [[geometric realization]]".

A concordance is a left [[homotopy]] in an [[(∞,1)-topos]] with respect to a _topological_ [[interval object]], not with respect to the _[[interval category|categorical interval]]_ .

For instance for $S = Diff$ the [[site]] of smooth manifolds, there is

* the "topological interval" $I \in \mathbf{H}_{diff}$ which is the [[smooth ∞-stack]] on $Diff$ [[representable functor|represented by]] the manifold $I = [0,1]$;

* the "categorical interval" $Ex^\infty \Delta^1 \in \mathbf{H}_{Diff}$ is the [[smooth ∞-stack]] that is constant on the free groupoid on a single morphism.


## Definition

For $\mathbf{H}$ and [[(∞,1)-topos]] with a fixed notion of topological [[interval object]] $I$, for $A \in \mathbf{A}$ any coefficient object and $X \in \mathbf{H}$ any other object, a **concordance** between two objects

$$
  c,d \in \mathbf{H}(X,A)
$$

(two cocycles in $A$-[[cohomology]] on $X$)

is an object $\eta \in A(X \times I)$ such that

$$
\begin{matrix}
X&&\\
\downarrow&\searrow^{c}&\\
X \times I&\stackrel{\eta}{\to}& A\\
\uparrow& \nearrow_{d}&\\
X&&
\end{matrix}
\,.
$$

## Examples 

### For topological principal bundles
 {#ForTopologicalPrincipalBundles}


\begin{proposition}\label{ConcordantTopologicalPrincipalBundlesAreIsomorphic}
**(concordant topological principal bundles are isomorphic)**
\linebreak
  With $kTopSp$ denoting the category of [[compactly generated weakly Hausdorff spaces]],
  for $X \,\in\, kTopSp$ a [[k-topological space]] 
  and $G \,\in\, Grp(kTopSp)$ a $k$-[[topological group]], 
  consider a [[concordance]] between a [[pair]] of 
  $G$-[[principal bundles]] over $X$, 
\begin{tikzcd}
  P_0 
  \ar[r]
  \ar[d, "{p_0}"]
  \ar[dr,phantom,"\mbox{\tiny(pb)}"]
  &
  P
  \ar[d, "{p}"]
  \ar[dr,phantom,"\mbox{\tiny(pb)}"]
  &
  P_1
  \ar[l]
  \ar[d, "{p_1}"]
  \\
  X \times \{0\}
  \ar[r, hook]
  &
  X \times [0,1]
  &
  X \times \{1\}
  \ar[l, hook']
\end{tikzcd}

If 

* {#FirstConditionForConcordanceOfTopologicalPrincipalBundlesToInduceIso} $X$ is a [[CW-complex]], or, more generally, a [[retract]] of a [[cell complex]]

or

* {#SecondConditionForConcordanceOfTopologicalPrincipalBundlesToInduceIso} $P$ is [[numerable bundle|numerable]], e.g. in that $X$ is a [[paracompact topological space]]

(e.g. if $X$ admits the structure of a [[smooth manifold]])

then there exists already an [[isomorphism]] of [[principal bundles]]
\begin{tikzcd}
  P_0
  \ar[dr, "{p_0}"{below, xshift=-2pt}]
  \ar[rr, "{\sim}"]
  &&
  P_1
  \ar[dl, "{p_1}"]
  \\
  & 
  X
\end{tikzcd}
\end{proposition}
(e.g. [Roberts & Stevenson 2016, Cor. 15](#RobertsStevenson16))
\begin{proof}

{#PrincipalBundleIsosAsSections}
Observe that isomorphisms $f \,\colon\, P \xrightarrow{\;} P'$ between principal bundles over $X$ are equivalently [[global sections]] of the fiber bundle $(P \times_X P')/G$:
\begin{tikzcd}[column sep={between origins, 50pt}]
    &[-10pt]
    &[-10pt]
    &&[+30pt]
    P \times G
    \ar[d, shift right=3pt, "\mathrm{pr}_1"{swap}]
    \ar[d, shift left=3pt, "\rho"]
    \ar[rr]
    &&
    \big(
      P \times_X P'
    \big) \times G
    \ar[d, shift right=3pt, "\mathrm{pr}_1"{swap}]
    \ar[d, shift left=3pt, "\rho"]
    \\
    &&&&
    P 
    \ar[d]
    \ar[rr, "{ (\mathrm{id},f) }"{description}]
    &&
    P \times_X P'
    \ar[d]
    \\
    P
      \ar[out=180-66, in=66, looseness=3.5, "\scalebox{.77}{$\,\mathclap{
        G
      }\,$}"{description},shift right=1]
    \ar[rr, "f"]
    \ar[dr]
    &
    &
    P'
      \ar[out=180-66, in=66, looseness=3.5, "\scalebox{.77}{$\,\mathclap{
        G
      }\,$}"{description},shift right=1]
    \ar[dl]
    &\leftrightarrow&
    P/G
    \ar[rr, dashed]
    \ar[dr, -, shift left=1pt]
    \ar[dr, -, shift right=1pt]
    &&
    \big(
      P
        \times_{X}
      P'
    \big) / G
    \ar[dl]
    \\
    &
    X
    &
    &&
    &
    X
\end{tikzcd}

Here, from left to right, the dashed section follows by the [[universal property]] of the [[quotient space]] $X = P/G$. From right to left, the top morphism follows by [[pullback]] along the dashed section, using that 

1. the bundle projections are [[effective epimorphisms]] by [[locally trivial bundle|local triviality]],

1. their [[kernel pairs]] are as shown, by [[principal bundle|principality]],

1. [[compactly generated topological spaces]] form a [[regular category]] (by [this Prop.](compactly+generated+topological+space#kHausIsRegular)), 

1. in a regular category pullback preserves effective epimorphisms ([this Prop.](regular+epimorphism#InRegularCategoryRegularEpisAreStableUnderPullback)) and, of course, their kernel pairs.

In particular, for every $P$ the [[identity morphism]] on it corresponds to the canonical section of $(P \times_X P)/G$.


{#TheLiftingDiagram} In the given situation, this means that we have a canonical local section $\sigma_0$ making the following solid diagram [[commuting square|commute]], exhibiting that the restriction of the bundle $P_0 \times [0,1]$ to $\{0\} \subset [0,1]$ is isomorphic to $P_0$, by construction:

\begin{tikzcd}
  X \times \{0\}
  \ar[rr, "\sigma_0"]
  \ar[dd, "\in \mathrm{Cof} \cap \mathrm{W}"]
  &&
  \big(
    P \underset{X \times [0,1]}{\times} (P_0 \times [0,1])
  \big)/G
  \ar[dd, "\in \mathrm{Fib}"]
  \\
  \\
  X \times [0,1]
  \ar[rr,-, shift right=1pt]
  \ar[rr,-, shift left=1pt]
  \ar[uurr, dashed, "\exists"]
  &&
  X \times [0,1]
\end{tikzcd}

Now

* assuming the [first condition](#FirstConditionForConcordanceOfTopologicalPrincipalBundlesToInduceIso):

  1. the right vertical [[map]] is a [[Serre fibration]], as all [[locally trivial bundle|locally trivial]] [[fiber bundles]] are [[Serre fibrations]] (by [this Prop.](fiber+bundle#RelationToFibrations));

  1. the left vertical [[continuous function|map]] is a [[Serre-Quillen model structure on topological spaces|Serre-Quillen]]-[[acyclic cofibration]] -- since (see [this Prop.](classical+model+structure+on+topological+spaces#HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen)) it is the [[product]]  $id_X \times (D^0 \hookrightarrow D^0 \times [0,1] )$ of the [[cofibrant object]] $X$ with a generating [[acyclic cofibration]] (see [this Def.](classical+model+structure+on+topological+spaces#TopologicalGeneratingAcyclicCofibrations)) --, hence is a [[Serre-Quillen model structure on topological spaces|Serre-Quillen]]-[[acyclic cofibration]] and as such has the [[left lifting property]] against the right map;

or 

* assuming the [second condition](#SecondConditionForConcordanceOfTopologicalPrincipalBundlesToInduceIso):

  1. the right vertical map is a [[Hurewicz fibration]], by [this Prop.](Hurewicz+fibration#NumerableFiberBundlesAreSerreFibrations),

  1. hence it has the [[right lifting property]] against the left map, by definition of [[Hurewicz fibrations]].


In either case, this implies that a [[lift]] exists, as shown by the dashed arrow above. 

The resulting [[commuting diagram|commutativity]] of the bottom right triangle says that this lift is a [[global section]] which hence exhibits an [[isomorphism]] of principal bundles (over $X \times [0,1]$) of this form:

$$
  P
  \;\;
  \simeq_X
  \;\;
  P_0 \times [0,1]
  \,.
$$

The [[restriction]] of this isomorphism to $\{1\} \subset [0,1]$ is hence an isomorphism of the form $P_1 \,\simeq_X\, P_0$, as required.
\end{proof}


### For topological vector bundles
 {#ForTopologicalVectorBundles}

For [[topological vector bundles]] over [[paracompact Hausdorff spaces]], concordance classes coincide with plain [[isomorphism classes]]:

+-- {: .num_prop #ConcondanceOfTopologicalVectorBundles}
###### Proposition
**([[concordance]] of [[topological vector bundles]])**

Let $X$ be a [[paracompact Hausdorff space]]. If $E \to X \times [0,1]$ is a [[topological vector bundle]] over the [[product space]] of $X$ with the [[closed interval]] (hence a _[[concordance]]_ of topological vector bundles on $X$), then the two endpoint-restrictions

$$
  E|_{X \times \{0\}}
  \phantom{AA}
  \text{and}
  \phantom{AA}
  E|_{X \times \{1\}}
$$

are [[isomorphism|isomorphic]] [[topological vector bundles]] over $X$.

=--

For **proof** see at _[[topological vector bundle]]_ [this Prop.](topological+vector+bundle#ConcondanceOfTopologicalVectorBundles).



### More examples

* For $A = VectrBund(-)$ the difference between concordance of [[vectorial bundles]] and isomorphism of vectorial bundles plays a crucial rule in the construction of [[K-theory]] from this model.

* The notions of coboundary and concordance exist in every [[cohesive (∞,1)-topos]].

## References

Discussion of concordance of topological [[principal bundles]] (in fact for [[simplicial principal bundles]] [[parameterized homotopy theory|parameterized]] over some base space):

* {#RobertsStevenson16} [[David Roberts]], [[Danny Stevenson]], Cor. 15 in: _Simplicial principal bundles in parametrized spaces_, New York Journal of Mathematics Volume 22 (2016) 405-440 ([arXiv:1203.2460](https://arxiv.org/abs/1203.2460), [nyjm:22-19](http://nyjm.albany.edu/j/2016/22-19.html))

Discussion of concordance in terms of the [[shape modality]] in the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoids]] (see at *[[shape via cohesive path ∞-groupoid]]* for more):

* {#Pavlov14} [[Dmitri Pavlov]], _Structured Brown representability via concordance_, 2014 ([pdf](https://dmitripavlov.org/concordance.pdf), [[Pavlov_Concordance.pdf:file]])

* {#BEBP} [[Daniel Berwick-Evans]], [[Pedro Boavida de Brito]], [[Dmitri Pavlov]], _Classifying spaces of infinity-sheaves_ ([arXiv:1912.10544](https://arxiv.org/abs/1912.10544))

[[!redirects concordances]]

[[!redirects concordance class]]
[[!redirects concordance classes]]



