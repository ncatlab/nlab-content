
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 

Where an ordinary [[category]] has a [[hom-set]], an [[(∞,1)-category]] has an [[∞-groupoid]] of morphisms between any two objects, a _hom-space_.

There are several ways to _present_ an [[(∞,1)-category]] $\mathbf{C}$ by an ordinary [[category]] $C$ equipped with some extra structure: for instance $C$ may be a [[category with weak equivalences]] or a [[model category]] or even a [[simplicial model category]]. In all of these presentations, given two objects $X, Y \in C$, there is a way to construct a [[simplicial sets]] $\mathbb{R}\mathbf{C}(X,Y)$ that presents the hom-[[∞-groupoid]] $\mathbf{C}(X,Y)$. This simplicial set -- or rather its [[homotopy type]] -- is called the 
_derived hom space_ or  _homotopy function complex_ and denoted $\mathbf{R}Hom(X,Y)$ or similarly.

## Presentations

There are many ways to present an [[(∞,1)-category]] by [[category theory|category theoretic data]], and for each of these there are corresponding tools for explicitly computing the derived hom spaces.

The most basic data is that of a [[category with weak equivalences]]. Here the derived hom spaces can be constructed in terms of zig-zags of morphisms by a process called _[[simplicial localization]]_. This we discuss below in _[For a category with weak equivalences](#ForACategoryWithWeakEquivalences)_.

Particularly useful extra structure on a [[category with weak equivalences]] that helps with computing the derived hom spaces is the structure of a _[[model category]]_. Using this one can construct simplicial resolutions of objects -- called _framings_ -- that generalize [[cylinder objects]] and [[path objects]], and then construct the derived hom spaces in terms of direct morphisms between these resolutions. This we discuss below in _[For a model category](#Framings)_.

Still a bit more helpful structure on top of a bare model category is that of a [[simplicial model category]]. Here, after a choice of cofibrant and fibrant resolutions of opjects, the derived hom spaces are given already by the [[sSet]]-[[hom objects]]. This we discuss below in _[For a simplicial model category](#EnrichedHomsCofToFib)_.




### For a category with weak equivalences
 {#ForACategoryWithWeakEquivalences}


Let $(C,W \subset Mor(C))$ be a [[category with weak equivalences]].

+-- {: .num_defn #ZigZagCategories}
###### Definition

Fix $n \in \mathbb{N}$. For $X,Y \in Obj(C)$, define a category $wMor_C^n(X,Y)$ 

* whose objects are [[zig-zag]]s of morphisms in $C$ of length $n$

  $$
    X = X_0 \leftarrow X_1 \to X_2 \leftarrow \cdots \to X_{n-1} \leftarrow X_n = Y
  $$

  such that each morphism going to the left, $X_{2k}\leftarrow X_{2k +1}$, is a [[weak equivalence]], an element in $W$;

* morphisms between such objects $(X,X_i,Y) \to (X',X'_i,Y')$ are collections of weak equivalences $(X_i \to X'_i)$ for all $0 \lt i \lt n $ such that all triangles and squares commute.

=--

+-- {: .num_defn #HammockLocalization}
###### Definition

Write $N(wMor_C^n(X,Y))$ for the [[nerve]] of this category, a [[simplicial set]].

The _[[hammock localization]]_ $L_W^H C$ of $C$ is the [[simplicially enriched category]] with objects those of $C$ and [[hom-objects]] given by the [[colimit]] over the length of these hammock hom-categories

$$
  L^H C(X,Y) := \lim_{\to_n} N(wMor_C^n(X,Y))
  \,.
$$

The [[Kan fibrant replacement]] of this simplicial set is the derived hom-space between $X$ and $Y$ of the $(\infty,1)$-category modeled by $(C,W)$.

=--



### For a model category
 {#Framings}


The derived hom spaces of a model category $C$ may always be computed
in terms of simplicial resolutions with respect to the [[Reedy model structure]]
$[\Delta^{op}, C]_{Reedy}$. These resolutions are often called
_framings_ ([Hovey](#Hovey)). These constructions are originally due to
([Dwyer-Hirschhorn-Kan](#DHK)).


Let $C$ be any [[model category]].

+-- {: .num_prop }
###### Observation

There is an [[adjoint triple]]

$$
  (const \dashv ev_0 \dashv (-)^{\times^\bullet})
  : 
  C
  \stackrel{\overset{const}{\longrightarrow}}{\stackrel{\overset{ev_0}{\longleftarrow}}{\underset{(-)^{\times^\bullet}}{\longrightarrow}}}
  \,,
  [\Delta^{op}, C]
  \,,
$$  

where

1. $const X : [n] \mapsto X$;

1. $ev_0 X_\bullet = X_0$;

1. $X^{\times^\bullet} : [n] \mapsto X^{\times^{n+1}}$.


=--

+-- {: .num_remark #CoDiscreteIsReedyFibrant}
###### Remark

For $X \in C$ fibrant, $X^{\times^\bullet}$ is fibrant in 
the [[Reedy model structure]] $[\Delta^{op}, C]_{Reedy}$.

=--

+-- {: .proof}
###### Proof

The matching morphisms are in fact [[isomorphisms]].

=--


+-- {: .num_defn}
###### Definition

Let $C$ be a model category.

1. For $X \in C$ any object, a _simplicial frame_ on $X$ is a factorization of $const X \to X^{\times^\bullet}$ into a weak equivalence followed by a fibration in the [[Reedy model structure]] $[\Delta^{op}, C]_{Reedy}$.

1. A _right framing_ in $C$ is a functor $(-)_\bullet :  C \to [\Delta^{op}, C]$
   with a [[natural isomorphism]] $(X)_0 \simeq X$ such that $X_\bullet$ is a simplicial
   frame on $X$.

Dually for _cosimplicial frames_.
   
=--

This appears as ([Hovey, def. 5.2.7](#Hovey)).

+-- {: .num_remark}
###### Remark

By remark \ref{CoDiscreteIsReedyFibrant} a simplicial frame $X_\bullet$ in the above is in particular fibrant in $[\Delta^{op}, C]_{Reedy}$.

=--




+-- {: .num_prop #SimplicialFunctionComplexes}
###### Proposition

For $X \in C$ cofibrant and $A \in C$ fibrant, there
are weak equivalences in $sSet_{Quillen}$

$$
  Hom_C(X^\bullet, A)
  \stackrel{\simeq}{\to}
  diag Hom_C(X^\bullet, A_\bullet)
  \stackrel{\simeq}{\leftarrow}
  Hom_C(X, A_\bullet)
  \,,
$$

(where in the middle we have the diagonal of the [[bisimplicial set]] $Hom(X^\bullet, A_\bullet)$).

=--

This appears as ([Hovey, prop. 5.4.7](#Hovey)).

Either of these simplicial sets is a model for the derived hom-space $\mathbb{R}Hom(X,A)$.


+-- {: .num_remark }
###### Remark

By developing these constructions further, one obtains 
a canonical  [[simplicial model category]]-resolution of 
(left proper and combinatorial) model categories $C$, such that 
the simplicial resolutions given by framings are just the 
cofibrant$\to$fibrant $sSet$-hom objects as discussed
[below](#EnrichedHomsCofToFib).

This is discussed at _[Simplicial Quillen equivalent models](http://ncatlab.org/nlab/show/simplicial+model+category#SimpEquivMods)_.

=--

+-- {: .num_prop }
###### Proposition

Let $C$ be a model category, let $\mathrm{c}_\mathrm{w} C$ be the full subcategory of $[\Delta, C]$ spanned by the cosimplicial objects whose coface and codegeneracy operators are weak equivalences, and let $\mathrm{s}_\mathrm{w} C$ be the full subcategory of $[\Delta^{op}, C]$ spanned by the simplicial objects whose face and degeneracy operators are weak equivalences.

1. $const : C \to \mathrm{c}_\mathrm{w} C$ is the right half of an adjoint homotopical equivalence of [[homotopical category|homotopical categories]], and $const : C \to \mathrm{s}_\mathrm{w} C$ is the left half of an adjoint homotopical equivalence of homotopical categories.
2. The functor $\operatorname{diag} Hom_C : (\mathrm{c}_\mathrm{w} C)^{op} \times \mathrm{s}_\mathrm{w} C \to sSet$ admits a right [[derived functor]].
3. The induced functor $(\operatorname{Ho} C)^{op} \times \operatorname{Ho} C \to \operatorname{Ho} sSet$ is the derived hom-space functor.

=--

### For a simplicial model category
 {#EnrichedHomsCofToFib}

We describe here in more detail properties of [[derived hom-functors]] (see there for more) in a [[simplicial model category]].

The crucial axiom used for this is the axiom of an [[enriched model category]] $C$ which says that 

* the [[copower|tensor operation]]

  $$
    \cdot : C \times SSet \to C
  $$

  is a [[Quillen bifunctor]];

* or equivalently that for $X \to Y$ a cofibration 
  and $A \to B$ a fibration the induced morphism

  $$
    C(Y, A) \to C(X,A) \times_{C(X,B)} C(Y,B)
  $$

  is a fibration, which is acyclic if either 
  $X \to Y$ or $A \to B$ is.

First of all the first statement directly implies that for $\emptyset \in C$ the [[initial object]] and $A \in C$ any object, the simplicial set $C(\emptyset,A) = {*}$ is the terminal simplicial set (see also [this Prop.](powered+and+copowered+category#InTensoredCotensoredCategoryInitialObjectIsEnrichedInitial)): because for any simplicial set $S$

$$
  \begin{aligned}
    SSet(S,C(\emptyset, A))
    & =  Hom_C(\emptyset \cdot S, A)
    \\
    & = Hom_C(colim_{\emptyset} \cdot S, A)
    \\
    & = Hom_C(\emptyset, A)
    \\
    &= {*}
  \end{aligned}
  \,,
$$

where we use that the [[copower|tensor]] [[Quillen bifunctor]] is required to respect [[colimit]]s and that the empty colimit is the [[initial object]]. (All equality signs here denote [[isomorphisms]], to distinguish them from weak equivalences.)

Similarly one has for all $X$ that $C(X,{*}) = {*}$.

Using this, the second equivalent form of the enrichment axiom has as a special case the following statement.

+-- {: .num_lemma }
###### Lemma

In a [[simplicial model category]] $C$, for $X \in C$ cofibrant and $A \in C$ fibrant, the [[simplicial set]] $C(X,A)$ is a [[Kan complex]].

=--

+-- {: .proof}
###### Proof

We apply the [[enriched model category]] axiom to the cofibration $\emptyset \to X$ and the fibration $A \to {*}$ to obtain a fibration

$$
  C(X,A) \to C(\emptyset, A) \times_{C(\emptyset,{*})} C(X,{*})  
  \,.
$$

The right hand is the [[pullback]] of the terminal simplicial set ${*} = \Delta^0$ to itself, hence is itself the point. So we have a fibration $ C(X,A) \to {*}$
and $C(X,A)$ is a fibrant object in the standard [[model structure on simplicial sets]], hence a [[Kan complex]].
.
=--


+-- {: .num_lemma }
###### Lemma

In a [[simplicial model category]] $C$, for $X \in C$ cofibrant and $f : A \to B$ a fibration, the morphism of [[simplicial set]]s $C(X,f) : C(X,A) \to C(X,B)$ is a [[Kan fibration]] that is a [[weak homotopy equivalence]] if $f$ is acyclic.

Dually, for $i : X \to Y$ a cofibration and $A$ fibrant, the morphism $C(i,A) : C(X,A) \to C(Y,A)$ is a cofibration of simplicial sets.

=--

+-- {: .proof}
###### Proof

This is as before. Explicity, consider the first case, the second one is the formal dual of that:

We enter the enrichment axiom with the morphisms $\emptyset \to X$ and $A \to B$ and find for the required [[pullback]] that

$$
  C(\emptyset,A) \times_{C(\emptyset, B)} C(X,B)
  =
  {*} \times_{*} C(X,B)
  =
  C(X,B)
$$

and hence that $C(X,A) \to C(X,B)$ is, indeed, a fibration, which is acyclic if $A \to B$ is.

=--


+-- {: .num_proposition }
###### Proposition

Let $C$ be a [[simplicial model category]]. 

Then for $X$ a cofibant object and 

$$
   f : A \stackrel{\simeq}{\to}  B
$$

a weak equivalence between fibrant objects, the [[enriched functor|enriched]] [[hom-object|hom-functor]]

$$
  C(X,f) : C(X,A) \to C(X,B)
$$

is a [[weak homotopy equivalence]] of [[Kan complex]]es.

Similarly, for $A$ a fibrant object and $j : X \stackrel{\simeq}{\to} Y$ a weak equivalence between cofibrant objects, the morphism

$$
  C(j,A) : C(X,A) \to C(Y,A)
$$

is a [[weak homotopy equivalence]] of [[Kan complex]]es.


=--


+-- {: .proof}
###### Proof

The second case is formally dual to the first, so we restrict attention to the first one.

By the above, the axioms of an [[enriched model category]] ensure that the above statement is true when $f$ is in addition a fibration. So we reduce the situation to that case.

This is possible because both $A$ and $B$ are assumed to be fibrant. This allows to apply the _factorization lemma_ that is described in great detail at [[category of fibrant objects]]. By this lemma, for every morphism $f : A \to B$ between fibrant objects there is a commutative diagram

$$
  \array{
    && \mathbf{E}_f B
    \\
    & {}^{\mathllap{\in fib \cap W}}\swarrow && \searrow^{\mathrlap{\in fib}}
    \\
    A &&\stackrel{\simeq}{\to}&& B
  }
$$

Since $f$ is assumed a weak equivalence it follows by [[category with weak equivalences|2-out-of-3]] that $\mathbf{E}_f B$ is also a weak equivalence. 

Therefore by the above properties of simpliciall enriched categories we obtain a [[span]] of acyclic fibrations of [[Kan complex]]es

$$
  C(X,A) \stackrel{\simeq}{\leftarrow}
  C(X, \mathbf{E}_f B)
  \stackrel{\simeq}{\to} 
  C(X,B)
  \,.
$$

By the [[Whitehead theorem]] every weak equivalence of Kan complexes is a [[homotopy equivalence]], hence there is a weak equivalence

$$
  C(X,A) \stackrel{\simeq}{\to} C(X,\mathbf{E}_f B) \stackrel{\simeq}{\to} C(X,B)
$$

that is homotopic to our $C(X,f)$. Therefore this is also a weak equivalence.

=--

### Comparison


Let $C$ be a [[model category]]. We discuss how its 
simplicial function complexes from prop. \ref{SimplicialFunctionComplexes}
are related to the simplicial localization from def. \ref{ZigZagCategories} and def. \ref{HammockLocalization}.

Suppose now that $Q : C \to C$ is a [[cofibrant replacement functor]] and $R : C \to C$ a [[fibrant replacement functor]], $\Gamma^\bullet : C \to (cC)_c$ a [[cosimplicial resolution functor]] and $\Lambda_\bullet : C \to (sC)_f$ a [[simplicial resolution functor]] in the [[model category]] $C$.


+-- {: .num_theorem #DKTheorem}
###### Theorem 
**(Dwyer--Kan)**

There are natural weak equivalences between the following equivalent realizations of this [[SSet]] [[hom-object]]:

$$
  \array{
    Mor_C(\Gamma^\bullet X, R Y)
    &\stackrel{\simeq}{\to}&
    diag Mor_C(\Gamma^\bullet X, \Lambda_\bullet Y)
    &\stackrel{\simeq}{\leftarrow}&
    Mor_C(Q X, \Lambda_\bullet Y)
    \\
    &&
    \uparrow^\simeq
    \\
    &&
    hocolim_{p,q \in \Delta^{op} \times \Delta^{op}}
    Mor_C(\Gamma^p X, \Lambda_q Y)
    \\
    &&\downarrow^\simeq
    \\
    &&N wMor_C^3(X,Y)
    \\
    &&\downarrow^\simeq
    \\
    &&Mor_{L^H C}(X,Y)
  }
  \,.
$$

=--

The top row weak equivalences are those of prop. \ref{SimplicialFunctionComplexes}


### In a category of fibrant objects
 {#InACategoryOfFibrantObjects}

There is also an explicit simplicial construction of the derived hom spaces for a homotopical category that is equipped with the structure of a [[category of fibrant objects]].
This is described in ([Cisinksi 10](#Cisinski10)) and ([Nikolaus-Schreiber-Stevenson 12, section 3.6.2](#NSS12)).


## Properties



### Hom-spaces of equivalences
 {#SpacesOfEquivalences}

+-- {: .num_theorem #DKTheorem}
###### Theorem 

For $C$ a [[simplicial model category]] and $X$ an object, the [[delooping]] of the [[automorphism ∞-group]]

$$
  Aut_W(X) \subset \mathbb{R}Hom(X,X)
$$

has the [[homotopy type]] of the component on $X$ of the [[nerve]] $N(C_W)$ of the [[subcategory]] of weak equivalences:

$$
  \mathbf{B} Aut_W(X) \simeq N(C_W)_X
  \,.
$$

The equivalence is given by a finite sequence of [[zig-zags]] and is natural with respect to [[sSet]]-[[enriched functors]] of simplicial model categories that preserve weak equivalences and send a fibrant cofibrant model for $X$ again to a fibrant cofibrant object.

=--    

This is [Dwyer-Kan 84, 2.3, 2.4](#DK84).

+-- {: .num_cor }
###### Corollary

For $C$ a model category, the simplicial set $N(C_W)$ is a model for the 
[[core]] of the [[(∞,1)-category]] determined by $C$.

=--

+-- {: .proof}
###### Proof

That core, like every [[∞-groupoid]] is equivalent to the disjoint union over its connected components of the deloopings of the automorphism $\infty$-groups of any representatives in each connected component.

=--




## Related concepts

* [[hom-object]]

* [[hom-set]], [[hom-functor]]

* [[hom-category]]

* [[hom-space]], **derived hom-space**, [[cocycle space]]

[[!include homotopy-homology-cohomology]]

## References 


For some original references by [[William Dwyer]] and [[Dan Kan]] see  [[simplicial localization]]. For instance

* {#DK84} [[William Dwyer]], [[Dan Kan]], _A classification theorem for diagrams of simplicial sets_, Topology 23 (1984), 139-155.

Discussion in terms of [[quasi-categories]]:

* [[Jacob Lurie]], Section 1.2.2 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

* [[Dan Dugger]], [[David Spivak]], _Mapping spaces in quasi-categories_, Algebraic & Geometric Topology 11 (2011) 263–325 ([arXiv:0911.0469](http://arxiv.org/abs/0911.0469), [doi:10.2140/agt.2011.11.263](http://dx.doi.org/10.2140/agt.2011.11.263))
 

The theory of _framings_ is due to

* {#DHK} [[William Dwyer]], [[Philip Hirschhorn]], [[Dan Kan]], _Model categories and general abstract homotopy theory_, (1997) ([pdf](http://www.mimuw.edu.pl/~jacho/literatura/ModelCategory/DHK_ModelCateogories1.pdf))
  

and in parallel section 5 of 

* {#Hovey} [[Mark Hovey]], _Model categories_ ([ps](http://math.unice.fr/~brunov/SecretPassage/Hovey-Model%20Categories.ps))
  

and in sections 16, 17 of

* [[Philip Hirschhorn]], _Model categories and their localization_ .


A useful quick review of the interrelation of the various constructions of derived hom spaces is page 14, 15 of

* [[Clark Barwick]], _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

Discussion of derived hom spaces for [[categories of fibrant objects]] is in 

* {#Cisinski10} [[Denis-Charles Cisinski]], _Invariance de la K-th&#233;orie par equivalences d&#233;riv&#233;es_, J. K-theory, 6 (2010), 505&#8211;546.
 

and section 3.6.2 of 

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- Presentations]]_ ([arXiv:1207.0249](http://arxiv.org/abs/1207.0249))
 



[[!redirects (infinity,1)-categorical hom-spaces]]


[[!redirects (∞,1)-categorical hom-space]]
[[!redirects (∞,1)-categorical hom-spaces]]


[[!redirects (infinity,1)-categorical hom space]]
[[!redirects (∞,1)-categorical hom space]]
[[!redirects (infinity,1)-categorial hom-space]]
[[!redirects (∞,1)-categorial hom-space]]
[[!redirects (infinity,1)-categorial hom space]]
[[!redirects (∞,1)-categorial hom space]]

[[!redirects derived hom space]]
[[!redirects derived hom-space]]
[[!redirects derived hom spaces]]
[[!redirects derived hom-spaces]]

[[!redirects hom-space]]
[[!redirects hom-spaces]]


[[!redirects hom-∞-groupoid]]
[[!redirects hom-infinity-groupoid]]
[[!redirects hom-(∞,0)-category]]
[[!redirects hom-(infinity,0)-category]]
[[!redirects hom ∞-groupoid]]
[[!redirects hom infinity-groupoid]]
[[!redirects hom (∞,0)-category]]
[[!redirects hom (infinity,0)-category]]

[[!redirects homotopy function complex]]
[[!redirects homotopy function complexes]]

[[!redirects (∞,1)-hom (∞,1)-functor)]]

[[!redirects (∞,1)-categorical hom]]

[[!redirects (∞,1)-categorical hom-spaces]]