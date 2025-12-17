
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[category]] $\mathcal{C}$, its *free coproduct completion* (or *free sum completion*, or *Fam construction*) is [[generalized the|the]] category $PSh_{\sqcup}(\mathcal{C})$ (often denoted $Fam(\mathcal{C})$, for *[[families]]* in $\mathcal{C}$, but note the usage of this term also for the [[(infinity,n)-category of correspondences|category of correspondences]] in e.g. [Lurie 2009](https://arxiv.org/abs/0905.0465)) obtained by [[free construction|freely]] adjoining [[coproducts]] of all [[objects]] of $\mathcal{C}$. 

## Definitions
 {#Definitions}

Here are a few concrete realizations of free coproduct completions. 


### Via indexed sets of objects
 {#ViaIndexedSetsOfObjects}

An early reference for the following explicit description is [Bénabou (1985), §3](#Bénabou1985), see also [Hu & Tholen (1995), p. 281, 286](#HuTholen95).


An explicit description of the free coproduct completion $PSh_{\sqcup}(\mathcal{C})$ of a category $\mathcal{C}$ is: 

* Its [[objects]] are [[dependent pair|dependent]] [[pairs]] consisting of 

  1. an index [[set]] $I \in $ [[Set]] 

  1. an $I$-[[indexed set]] $\big( X_i  \in \mathcal{C} \big)_{i \in I}$ of [[objects]] of $\mathcal{C}$.

* Its [[morphisms]] $\big( X_i \big)_{i \in I} \xrightarrow{ \; ( \phi_i )_{i \in I} \; } \big( Y_j \big)_{j \in J} $ [[pairs]] consisting of 

  * a [[function]] of index sets $f \,\colon\, I \to J$.

  * an $I$-[[indexed set]] of [[morphisms]] $\phi_i \,\colon\, X_i \xrightarrow{\;} Y_{f(i)}$ for $i \in I$ in $\mathcal{C}$.

* The [[composition]]-law and [[identity morphisms]] are the evident ones.

### As a comma category

The free coproduct completion of a category $\mathcal{C}$ is a sort of [[comma category]] of the following shape:

\begin{tikzcd}
	{\mathbf{Fam}(\mathcal{C})} & 1 \\
	{\mathbf{Set}} & {\mathbf{Cat}}
	\arrow[from=1-1, to=1-2]
	\arrow[from=1-1, to=2-1]
	\arrow["{\mathcal{C}}", from=1-2, to=2-2]
	\arrow[shorten <=7pt, shorten >=7pt, Rightarrow, from=2-1, to=1-2]
	\arrow["{\mathbf{disc}}"', from=2-1, to=2-2]
\end{tikzcd}

However, this requires treating $Cat$ as a 2-category, and allowing the 2-cell to be a [[lax natural transformation]].


### As a Grothendieck construction
 {#AsAGrothendieckConstruction}

The following is also pretty immediate and essentially discussed in [Bénabou (1985), §3](#Bénabou1985) (though without mentioning of the term "[[Grothendieck construction]]").

The free coproduct completion of a category $\mathcal{C}$ is equivalently the [[Grothendieck construction]] 

$$
  PSh_{\sqcup}(\mathcal{C})
  \;\;
    \simeq
  \;\;
  \underset
    { S \,\in\, Set }
    { \textstyle{\int} }
  \;
  \underset{s \in S}{\textstyle{\prod}}
  \mathcal{C}
$$

on the [[contravariant functor|contravariant]] [[pseudofunctor]] on [[Set]] which sends a set $S$ to the $S$-indexed [[product category]] of $\mathcal{C}$ with itself (equivalently: to the [[functor category]] into $\mathcal{C}$ out of the [[discrete category]] on $S$):

$$
  \array{
    Set^{op} &\longrightarrow& Cat
    \\
    S 
      &\mapsto& Func(S,\mathcal{C}) 
      & \simeq \;\underset{s \in S}{\prod} \mathcal{C}
    \\
    \Big\downarrow\mathrlap{{}^{f}}
    &&
    \Big\uparrow\mathrlap{{}^{f^\ast}}
    \\
    T 
      &\mapsto& Func(T,\mathcal{C}) 
      & 
    \simeq \;\underset{t \in T}{\prod} \mathcal{C}
    \mathrlap{\,,}
  }
$$
where the [[base change]]-[[functors]] $f^\ast$ are given (on [[functor categories]] by [[precomposition]] with $f$, hence) by:
\[
  \label{PullbackFunctorBetweenProductCategories}
  f \,\colon\, S \longrightarrow T
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    \underset{t \in T}{\prod} \mathcal{C}
    &\xrightarrow{\;\; f \;\;}&
    \underset{s \in S}{\prod} \mathcal{C}
    \\
    \big(
      X_t
    \big)_{t \in T}
    &\mapsto&
    \big(
      X_{f(s)}
    \big)_{s \in S}
    \,.
  }
\]

Namely, by definition of the [[Grothendieck construction]]

1. its [[objects]] are [[dependent pair|dependent]] [[pairs]] of the form 

   $$
     X_S
     \;\equiv\;
     \big(
       S \in Set
       ,\, 
       (X_s \in \mathcal{C})_{s \in S}   
     \big)
   $$

1. its [[morphisms]] 

   $$
     \phi_f \;\colon\; X_S \longrightarrow Y_T
   $$

   are [[dependent pair|dependent]] [[pairs]] consisting of a [[map]]

   $$
     f \,\colon\, S \longrightarrow T
   $$

   and a morphism in $\underset{s \in S}{\prod} \mathcal{C}$ of the form

   $$
     \phi \,\colon\, X_S \longrightarrow f^\ast Y_T
     \,.
   $$

   where, by definition (eq:PullbackFunctorBetweenProductCategories) of $f^\ast$ and the nature of [[product categories]], the latter is an $S$-[[indexed set]] $(\phi_s)_{s \in S}$ of [[morphisms]] in $\mathcal{C}$ of the form

   $$
     \phi_s \,\colon\, X_s \longrightarrow Y_{f(s)} 
     \,.
   $$

But this is manifestly the same as the explicit description of $PSh_{\sqcup}(\mathcal{C})$ [above](#ViaIndexedSetsOfObjects).




### Via coproducts of presheaves
 {#ViaCoproductOfPresheaves}

The free coproduct completion of $\mathcal{C}$ is [[equivalence of categories|equivalently]] the [[full subcategory]] 

$$
  PSh_{\sqcup}(\mathcal{C})
  \xhookrightarrow{\;}
  PSh(\mathcal{C})
$$

of the [[category of presheaves]] over $\mathcal{C}$ on those which are [[coproducts]] of [[representables]]. The latter is the [[free cocompletion]] of $\mathcal{C}$ under *all* [[small colimit|small]] [[colimits]].

The [[Yoneda embedding]] hence factors through the free coproduct completion

$$
  y
  \;\colon\;
  \mathcal{C}
  \xhookrightarrow{\;}
  PSh_{\sqcup}(\mathcal{C})
  \xhookrightarrow{\;}
  PSh(\mathcal{C})
$$

Notice that the first inclusion here does *not* [[preserved colimit|preserve]] [[coproducts]] (coproducts are freely adjoined irrespective of whether $\mathcal{C}$ already had some coproducts), but the second does. Both inclusions [[preserved limit|preserve]] those [[limits]] that exist.

## Properties

Fairly immediate from the explicit definition [above](#ViaIndexedSetsOfObjects) is:

\begin{proposition}\label{CategoriesOfCoproductsOfConnectedObjects}
  A [[category]] $\mathcal{B}$ with small-indexed [[coproducts]] is [[equivalence of categories|equivalent]] to a [[free coproduct completion]] $PSh_{\sqcup}(\mathcal{C})$ for a [[small category]] $\mathcal{C}$ if 

1. $\mathcal{C} \xhookrightarrow{\;} \mathcal{B}$ is a [[full subcategory]] of [[connected objects]], 

   i.e. $X \,\in\, \mathcal{C} \hookrightarrow \mathcal{B}$ means that the [[hom-functor]] $\mathcal{B}(X,-) \,\colon\, \mathcal{B} \to Set$ [[preserved colimit|preserves]] [[coproducts]]

   (which when $\mathcal{C}$ is [[extensive category|extensive]] means equivalently that if $X$ is a coproduct, then one of the summands is [[initial object|initial]], by [this Prop.](InExtensiveCategoryCOnnectedObjectsArePrimitiveUnderCoproduct));

1. each object of $\mathcal{B}$ is a [[coproduct]] of objects in $\mathcal{C} \hookrightarrow \mathcal{B}$.

\end{proposition}
([Carboni & Vitale 1998, Lem. 42](#CarboniVitale98))
\begin{proof}
  Since, by assumption, the objects of $\mathcal{B}$ are already presented by [[indexed sets]] $\big(X_s\big)_{s \in S}$ of objects in $\mathcal{C}$, it is sufficient to see that under this presentation the morphisms 
$$
  \phi
  \,\colon\,
  \big(\underset{s \in S}{\coprod} X_s\big)
  \longrightarrow
  \big(\underset{t \in T}{\coprod} Y_t\big)
$$
in $\mathcal{B}$ correspond bijectively to indexed sets of morphisms in $\mathcal{C}$ according to the explicit description of the free coproduct completion [above](#ViaIndexedSetsOfObjects). Indeed, using 

1. the [[hom-functors preserve limits|general fact]] that [[hom-functors]] take [[coproducts]] in the first argument to [[products]]  

1. the defining property that the resulting hom-functors out of connected objects take coproducts in the second argument to coproducts, 

we obtain the following sequence of [[natural bijections]]
$$
\begin{array}{ll}
  Hom_{\mathcal{C}}\big(
    \coprod_s X_s
    ,\,
    \coprod_t Y_t
  \big)
  \\
  \;\simeq\;
  \prod_s
  Hom_{\mathcal{C}}\big(
     X_s
    ,\,
    \coprod_t Y_t
  \big)
  \\
  \;\simeq\;
  \underset{s \in S}{\prod}
  \underset{t_s \in T}{\coprod}
  Hom_{\mathcal{C}}\big(
    X_s
    ,\,
    Y_{t_s}
  \big)
  \\
  \;\simeq\;
  \underset{f \colon S \to T}{\coprod}
  \underset{s \in S}{\prod}
  Hom_{\mathcal{C}}\big(
    X_s
    ,\,
    Y_{f(s)}
  \big)
  \,.
\end{array}
$$
\end{proof}

\begin{proposition}
\label{FCCOfAccessibleCatIsAccesible}
  The free coproduct completion of an [[accessible category]] is itself accessible.
\end{proposition}
([Makkai & Paré (1989), Cor. 5.3.6](#MakkaiParé1989))

\begin{prop}
\label{FreeCoproductCompletionIsExtensive}
  Any free coproduct completion is an [[extensive category]].
\end{prop}
(e.g. [Carboni, Lack & Walters 1993](#CarboniLackWalters93))


\begin{proposition}
\label{CoproductCompletionOfCategoryWithProducts}
  For $\mathcal{C}$ a category with all [[Cartesian products]], its free coproduct completion $PSh_{\sqcup}(\mathcal{C})$ also has [[products]] and they [[distributive category|distribute]] over the [[coproducts]].
\end{proposition}
\begin{proof}
  This is readily seen by component inspection, but it may be instructive to see it from more abstract reasoning:

Namely, with the free cocompletion understood as a [[Grothendieck construction]], $PSh_{\sqcup}(\mathcal{C}) \,\simeq\, \int_{S \in Set} \mathcal{C}^S$ discussed [above](#AsAGrothendieckConstruction), its cartesian produducts are computed by the general formula for limits in Grothendieck constructions ([here](Grothendieck+construction#CoLimitsInAGrothendieckConstruction)) as the "[[external tensor product|external]] [[cartesian product]]" ([here](Grothendieck+construction#CartesianProductInGrothendieckConstruction), we now show binary products only, just for ease notation):
$$
  X_S,\, Y_T \,\in\, \textstyle{\int}_{S \in Set} \mathcal{C}
  \;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;
  X_S \times Y_T 
  \;\simeq\;
  \Big(
  \big(
    (pr_S)^\ast X
  \big) 
    \times_{S \times T} 
  \big(
    (pr_T)^\ast Y
  \big)   
  \Big)_{S \times T}
  \,.
$$
Of course this comes down to the expected component formula
$$
  \begin{array}{ll}
  \big(
    X_S \times Y_T
  \big)_{s,t}
  \\
  \;\simeq\;
  \Big(
  \big(
    (pr_S)^\ast X
  \big) 
    \times_{S \times T} 
  \big(
    (pr_T)^\ast Y
  \big)   
  \Big)_{s,t}
  & 
  \text{by the above}
  \\
  \;\simeq\;
  \{(s,t)\}^\ast
  \Big(
  \big(
    (pr_S)^\ast X
  \big) 
    \times_{S \times T} 
  \big(
    (pr_T)^\ast Y
  \big)   
  \Big)
  &
  \text{by definition}
  \\
  \;\simeq\;
  \Big(
  \big(
    \{(s,t)\}^\ast
    (pr_S)^\ast X
  \big) 
    \times_{\{(s,t)\}} 
  \big(
    \{(s,t)\}^\ast
    (pr_T)^\ast Y
  \big)   
  \Big)
  &
  \text{pullback is right adjoint}
  \\
  \;\simeq\;
  \big(
    \{s\}^\ast
    X
  \big) 
    \times_{\{(s,t)\}} 
  \big(
    \{t\}^\ast
    Y
  \big)   
  &
  \text{by commuting diagram below}
  \\
  \;\simeq\;
  X_s \times Y_t
  &
  \text{by definition}
  \end{array}
$$
$$
  \array{
    \{s\} &\simeq& \{(s,t)\} &\simeq& \{t\}
    \\
    \Big\downarrow && \Big\downarrow && \Big\downarrow
    \\
    S &\underset{pr_S}{\longleftarrow}& S \times T &\underset{pr_T}{\longrightarrow}& T
  }
$$
Similarly, the component formula for the free coproduct is
$$
  \big( 
    Y_T \amalg Y'_{T'}
  \big)_{\tau}
  \;\simeq\;
  \left\{
  \begin{array}{lll}
    Y_\tau &\vert& \tau \in T
    \\
    Y'_{\tau} &\vert& \tau \in T'
  \end{array}
  \right.
  \,.
$$
Using all this, distributivity is verified as follows:
$$
  \begin{array}{ll}
    \Big(
    X_S 
      \times 
    \big(
      Y_T \sqcup Y_{T'}
    \big)
    \Big)_{s, \tau}
    \\
    \;\simeq\;
    X_s 
      \times 
    \big(
      Y_T \sqcup Y_{T'}
    \big)_\tau
    \\
    \;\simeq\;
    \left\{
    \begin{array}{lll}
      X_s  \times Y_\tau &\vert& \tau \in T
      \\
      X_s \times Y'_{\tau} &\vert& \tau \in T'
    \end{array}
    \right.
    \\
    \;\simeq\;
    \left\{
    \begin{array}{lll}
      (X_S \times Y_T)_{s, \tau} &\vert& \tau \in T
      \\
      (X_S \times Y'_{T'})_{s, \tau} &\vert& \tau \in T'
    \end{array}
    \right.
    \\
    \;\simeq\;
    \Big(
    \big(
      X_S \times Y_T
    \big)
    \sqcup
    \big(
      X_S \times Y'_{T'}
    \big)
    \Big)_{s,\tau}
    \,.
  \end{array}
$$
\end{proof}

\begin{remark}\label{FreeDistributiveCategoryMonad}
It seems plausible, that, 
more abstractly, Prop. \ref{CoproductCompletionOfCategoryWithProducts} follows 
because the [[2-monad]] for [[free product completion]] would [[distributive law|distribute]] over the 2-monad for free coproduct cocompletion; the composite 2-monad would exhibit the [[free construction|free]] [[distributive category]]-construction. We don't currently have a proof or reference for these statements, though.
\end{remark}

## Examples
 {#Examples}

### Coproduct completion of connected objects

The following examples follow as special cases of Prop. \ref{CategoriesOfCoproductsOfConnectedObjects}:

\begin{example}
The category [[Set]] is the [[free coproduct completion]] of the [[terminal category]].
\end{example}

\begin{example}\label{SkeletalGroupoids}
**([[skeletal groupoids]] form the free coproduct completion of [[groups]])**
\linebreak
  The [[1-category]] of [[skeletal groupoids]] among that of all [[strict groupoids]] is the free coproduct completion of the category of 1-object [[delooping groupoids]] which (*as [[1-categories]]*) is equivalently the category of [[groups]]:
$$  
  PSh_{\sqcup}\big(
    Grp
  \big)
  \;\;
    \simeq
  \;\;
  PSh_{\sqcup}\big(
    Grpd_{(Obj = \ast)}
  \big)
  \;\;
    \simeq
  \;\;
  Grpd_{skl}
  \,.
$$
\end{example}

\begin{example}\label{GActionsAndGOrbits}
**([[G-set|$G$-sets]] are the [[free coproduct completion]] of [[orbit category|$G$-orbits]])**
\linebreak
  Let $G \,\in\, Grp(Set)$ be a [[discrete group]]. Write

* [[G-set|$G Set$]] for its category of [[group actions]] on [[sets]], 

* $G Orbt \xhookrightarrow{\;} G Set$ for its [[orbit category]], the [[full subcategory]] on the [[transitive actions]], hence the [[coset space|sets of cosets]] $G/H$, for [[subgroups]] $H \subset G$.

Since every [[G-set]] $X$ decomposes as a [[disjoint union]] of [[transitive actions]], namely of [[orbits]] of [[elements]] of $X$, this inclusion exhibits $G Set$ as the [[free coproduct completion]] of [[orbit category|G Orbt]].
\end{example}


### Coproduct compeletion of extensive categories

\begin{example}\label{CoproductCompletionOfExtensiveCategories}
**(coproduct completion of extensive categories)**
\linebreak
  While Prop. \ref{FreeCoproductCompletionIsExtensive} says that every free coproduct completion is extensive, if a category $\mathcal{C}$ is already extensive to start with then its free coproduct completion may equivalently be described as the category of $\mathcal{C}$-[[bundles]] over [[sets]], the latter regarded as objects of $\mathcal{C}$ via the unique [[coproduct]]-[[preserved colimit|preserving]] [[functor]] $\iota_{Set} \,\colon\, Set \longrightarrow \mathcal{C}$, hence as the [[comma category]] $\mathcal{C}_{Set} \,\coloneqq\, \big(id_{\mathcal{C}}, \iota_{Set}\big)$:
\[
  \label{AsACategoryOfBundles}
  \mathcal{X}\;\text{extensive}
  \;\;\;\;\;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;\;\;\;\;
  PSh_{\sqcup}(\mathcal{C})
  \;\;
    \simeq
  \;\;
  \mathcal{C}_{Set}
  \;\;
    =
  \;\;
  \left\{
  \array{
    \underset{s \in S}{\coprod} X_s
    &\overset{\phi}{\longrightarrow}&
    \underset{t \in T}{\coprod} Y_t
    \\
    \Big\downarrow
    &&
    \Big\downarrow
    \\
    S &\underset{f}{\longrightarrow}& T
    \,,
  }
  \right\}
\]
where on the right we are indicating a generic [[morphism]] of such [[bundles]].

Namely, since every [[set]] is the [[coproduct]] of [[singleton sets]] indexed by its [[elements]], and due to the defining property of an [[extensive category]] that the coproduct functors are [[equivalence of categories|equivalences]] between ([[product category|products]] of) [[slice categories]]
$$
  \mathcal{C}_{/ \iota(S)}
  \;\;
  \simeq
  \;\;
  \underset{s \in S}{\prod} 
    \mathcal{C}_{/\iota(s)}
$$
it follows that:

1. every object $X_S$ of $\mathcal{C}_{\iota(S)}$ is of the form shown in (eq:AsACategoryOfBundles) hence determined by a family $(X_s)_{s \in S}$,

1. morphisms as shown in (eq:AsACategoryOfBundles) are equivalently (by the [[universal property]] of the [[pullback]]) morphisms of the form

   $$
   \array{
     \underset{s \in S}{\coprod}
     X_s
     &\overset{\phi}{\longrightarrow}&
     \underset{s \in S}{\coprod} Y_{f(s)}
     \\
     \Big\downarrow
     &&
     \Big\downarrow
     \\
     S &\underset{\;\;\; id_S \;\;\;}{\longrightarrow}& S
     \,,
   }
   $$

   (where we used [[universal colimit|pullback stability of coproducts]] in an extensive category, see [there](extensive+category#DisjointAndPullbackStableCoproducts), to deduce that $f^\ast Y_S \,\simeq\, \underset{s \in S}{\coprod} f^\ast(Y_S)_s \,\simeq\, \underset{s \in S}{\coprod} Y_{f(s)}$)

   which by extensitivity are equivalently $S$-indexed families $\phi_s\,\colon\, X_s \longrightarrow Y_{f(s)}$.

This is again manifestly the explicit description of the free coproduct completion from [above](#ViaIndexedSetsOfObjects).

Conversely this gives a sense that if a category $\mathcal{C}$ is *not* extensive, so that the notion of [[bundles]] with total spaces and fibers in $\mathcal{C}$ does not make sense,  its free coproduct completion may be understood as the closest stand-in for that category of $\mathcal{C}$-bundles over sets.
\end{example}



## Related concepts

* [[free cocompletion]], [[idempotent completion]], [[Cauchy completion]]

* [[free cartesian category]]

## References

Early discussion of the concept: 

* {#Bénabou1985} [[Jean Bénabou]], §3.3 in: *Fibered Categories and the Foundations of Naive Category Theory*,  The Journal of Symbolic Logic, Vol. **50** 1 (1985) 10-37 &lbrack;[doi:10.2307/2273784](http://dx.doi.org/10.2307/2273784)&rbrack;

On [[accessible category|accessibility]] of free coproduct completions:

* {#MakkaiParé1989} [[Michael Makkai]], [[Robert Paré]],  §5.2.2 (pp. 116) in: _Accessible categories: The foundations of categorical model theory_,  Contemporary Mathematics **104**, American Mathematical Society (1989) &lbrack;[ISBN:978-0-8218-7692-3](https://bookstore.ams.org/conm-104)&rbrack;

On [[limits]] in free coproduct completions:

* {#HuTholen95} [[Hongde Hu]], [[Walter Tholen]], *Limits in  free  coproduct completions*, Journal of  Pure  and  Applied  Algebra 105 (1995) 277-291 (<a href="https://doi.org/10.1016/0022-4049(94)00153-7">doi:10.1016/0022-4049(94)00153-7</a>, [pdf](https://core.ac.uk/download/pdf/82604415.pdf))

In the context of [[regular and exact completions]]:

* {#CarboniVitale98} [[Aurelio Carboni]], [[Enrico Vitale]], *Regular and exact completions*, Journal of Pure and Applied Algebra **125** 1–3  (1998) 79-116 (<a href="https://doi.org/10.1016/S0022-4049(96)00115-6">doi:10.1016/S0022-4049(96)00115-6</a>)

In the general context of [[extensive categories]]:

* {#CarboniLackWalters93} [[Aurelio Carboni]], [[Stephen Lack]], [[Bob Walters|R. F. C. Walters]], _Introduction to extensive and distributive categories_, JPAA **84** (1993) pp. 145-158 &lbrack;<a href="https://doi.org/10.1016/0022-4049(93)90035-R">doi:10.1016/0022-4049(93)90035-R</a>&rbrack;

As [[categorical semantics]] for [[dependent linear type theories]] (in the context of [[quantum programming languages]] with "[[dynamic lifting]]", such as proto-[[Quipper]]), the free coproduct completion of [[symmetric monoidal category|symmetric]] [[closed monoidal categories]] is considered in

* [[Francisco Rios]], [[Peter Selinger]], §3.2 in: *A Categorical Model for a Quantum Circuit Description Language*, EPTCS **266** (2018) 164-178 &lbrack;[arXiv:1706.02630](https://arxiv.org/abs/1706.02630), [doi:10.4204/EPTCS.266.11](https://doi.org/10.4204/EPTCS.266.11)&rbrack;

* {#FuKishidaSelinger20} [[Peng Fu]], [[Kohei Kishida]], [[Peter Selinger]], _Linear Dependent Type Theory for Quantum Programming Languages_, LICS '20: Proceedings of the 35th Annual ACM/IEEE Symposium on Logic in Computer ScienceJuly 2020 Pages 440–453 ([arXiv:2004.13472](https://arxiv.org/abs/2004.13472), [doi:10.1145/3373718.3394765](https://dl.acm.org/doi/10.1145/3373718.3394765), [pdf](https://depend.cs.uni-saarland.de/lics-icalp/papers/B5.F), [video](https://www.youtube.com/watch?v=GUT8j4V6Nzg))

and its [followups](Quipper#ReferencesDependentLinearTypesAndCategoricalSemantics).

Algebras in the free coproduct completion are considered in: 

* [[Michael Johnson]], [[R. F. C. Walters]], _Algebra objects and algebra families for finite limit theories_, Journal of Pure and Applied Algebra **83** 3 (1992) 283-293 &lbrack;<a href="https://doi.org/10.1016/0022-4049(92)90047-J">doi:10.1016/0022-4049(92)90047-J</a>&rbrack;


[[!redirects free coproduct completions]]

[[!redirects free coproduct cocompletion]]
[[!redirects free coproduct cocompletions]]

[[!redirects free coproduct-cocompletion]]
[[!redirects free coproduct-cocompletions]]

[[!redirects free sum completion]]
[[!redirects free sum completions]]

