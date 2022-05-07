
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
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

What is called _geometric realization of categories_ is a [[functor]] that sends [[categories]] to [[topological spaces]], namely the functor which first forms the [[simplicial set]] $N(\mathcal{C})$ that is the [[nerve]] of the category $\mathcal{C}$, and then forms the [[geometric realization]] ${\vert N(\mathcal{C})\vert}$ of this simplical set. Typically one is interested in this geometric realization up to [[weak homotopy equivalence]].

By the [[homotopy hypothesis]]-theorem the [[geometric realization]] of simplicial sets constitutes a ([[Quillen equivalence|Quillen]])[[equivalence of (infinity,1)-categories|equivalence]] between the [[classical model structure on simplicial sets|classical homotopy theory of simiplicial sets]] and the [[classical model structure on topological spaces|classical homotopy theory of topological spaces]]. 
This means that inasmuch as one is interested in geometric realization of categories up to weak homotopy equivalence, then the key part of the operation is in forming the simplicial nerve $N(\mathcal{C})$ of a category, with the latter regarded as a model for an [[∞-groupoid]]. Indeed, equivalently one could consider the [[Kan fibrant replacement]] of the nerve $N(\mathcal{C})$ (which still has the same geometric realization, up to weak homotopy equivalence).

Therefore an equivalent perspective on geometric realization of categories is that it universally turns a category into an [[infinity-groupoid]] by freely turning all its morphisms into [[equivalence in an (infinity,1)-category|homotopy equivalences]].


Geometric realization of categories has various good properties:

It sends [[equivalences of categories]] to [[weak homotopy equivalences]] (corollary \ref{RealizationOfEquivalenceIsHomotopyEquivalence} below).  A more general sufficient criterion for the geometric realization of a functor is given  by the seminal theorem known as _Quillen's theorem A_ (theorem \ref{QuillenTheoremA} below.)

The existence of the [[Thomason model structure]] ([below](#ThomasonModelStructure)) implies that every [[homotopy type]] arises as the geometric realization of some category. In fact it already arises as the geometric realization of some [[poset]] ([[(0,1)-category]]).
  
## Definition

Write

$$
  N \colon Cat \to sSet
$$

for the [nerve functor](nerve#NerveOfACategory) from [[Cat]] to [[sSet]]. Write

$$
  {\vert - \vert} : sSet \to Top
$$

for the [[geometric realization]] of [[simplicial sets]] from [[sSet]] to [[Top]].

The _geometric realization of categories_ is the [[composition|composite]] of these two operations:

$$
  {\vert - \vert} \coloneqq {\vert N(-)\vert} \;\colon\; Cat \to Top
$$



## Properties

### Thomason model structure
  {#ThomasonModelStructure}

There is a [[model category]] structure on [[Cat]] whose weak equivalences are those [[functors]] $F \colon \mathcal{C} \to \mathcal{D}$ which under [[geometric realization]] become weak equivalences in the [[classical model structure on topological spaces]], hence which become [[weak homotopy equivalences]]. This is called the _[[Thomason model structure]]_.

The existence of the Thomas model structure implies that every [[homotopy type]] arises as the geometric realization of some category, in fact already as the realization of some [[poset]]/[[(0,1)-category]]:


+-- {: .num_defn #PosetOfSimplicesInNerveOfCategory}
###### Definition

For $C$ a [[category]], let $\nabla C$ be the [[poset]] of [[simplices]] in the [[nerve]] $N C$, ordered by inclusion.

=--

+-- {: .num_prop }
###### Proposition

For every category $\mathcal{C}$ the poset $\nabla \mathcal{C}$ from def. \ref{PosetOfSimplicesInNerveOfCategory} has [[weak homotopy equivalence|weakly homotopy equivalent]] geometric realization

$$
  {\vert N(\nabla \mathcal{C}) \vert} \simeq_{wh} {\vert \mathcal{C} \vert}  
  \,.
$$

=--



### Recognizing weak equivalences: Quillen's theorem A and B

Let $\mathcal{C}, \mathcal{D}$ be two [[categories]] and let

$$
  F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
$$

be a [[functor]] between them.


+-- {: .num_theorem #QuillenTheoremA}
###### Theorem
**([Quillen 72](#Quillen72), theorem A)**


If for all [[objects]] $d \in \mathcal{D}$ the [[geometric realization]] ${\vert N(F/d)\vert}$ of the [[comma category]] $F/d$ is [[contractible]] (meaning that $F$ is a "homotopy [[cofinal functor]]", hence a [[cofinal (∞,1)-functor]]), then 

$$
  {\vert N(F) \vert}
   \;\colon\; 
  {\vert N(\mathcal{C}) \vert} 
    \longrightarrow 
  {\vert N(\mathcal{D}) \vert}  
$$ 

is a [[weak homotopy equivalence]].

=--

+-- {: .num_theorem #QuillenTheoremB}
###### Theorem
**([Quillen 72](#Quillen72) theorem B)**

If for all [[objects]] $d \in \mathcal{D}$ we have that ${\vert N(F/d)\vert}$ is [[weak homotopy equivalence|weakly homotopy equivalent]] to a given [[topological space]] $X$ and all morphisms $f \colon d_1 \to d_2$ induce [[weak homotopy equivalences]] between these, then $X$ is the [[homotopy fiber]] of ${\vert N(F) \vert}$, hence we have a [[homotopy fiber sequence]] (in the [[classical model structure on topological spaces]]) of the form

$$
  X   
    \longrightarrow
  {\vert N(\mathcal{C}) \vert} 
    \overset{\vert N(F) \vert }{\longrightarrow} 
  {\vert N(\mathcal{D}) \vert}
  \,.
$$

=--

As a consequence:

+-- {: .num_prop}
###### Proposition
**([McCord 66, theorem 6](#McCord66), [Quillen 78, prop. 1.6](#Quillen78))**

Let $\mathcal{C}, \mathcal{D}$ be [[finite set|finite]] [[posets]] and consider $F \colon  \mathcal{C} \to \mathcal{D}$ be a [[functor]].

If for each element/object $y \in \mathcal{D}$ its [[preimage]] $f^{-1}( \{ y' \in Y \vert  y' \leq y \})$ has [[contractible topological space|contractible]] geometric realization, then ${\vert N(F)\vert}$ is a [[homotopy equivalence]].

=--

An alternative proof is given in ([Barmak 10](#Barmak10)).



### Natural transformations and homotopies

+-- {: .num_prop #NaturalTrafoMapsToHomotopy}
###### Proposition

A [[natural transformation]] $\eta : F \Rightarrow G$ between two [[functors]] $F, G : \mathcal{C} \to \mathcal{D}$ induces under geometric realization a [[homotopy]] 

$$
  {|N(\eta)|} \colon {\vert N(F)\vert} \longrightarrow {\vert N(G) \vert}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The natural transformation is equivalently a functor of the form

$$
  \eta \;\colon\; \mathcal{C} \times \{0 \to 1\} \to \mathcal{D}
$$

out of the [[product category]] of $\mathcal{C}$ with the [[interval category]].

Since [[geometric realization]] of [[simplicial sets]] preserves [[Cartesian products]] (see there) we have that 

$$
  {\vert N( \mathcal{C} \times \{0,1\} ) \vert} 
    \;\simeq_{iso}\; 
  {\vert N(\mathcal{C}) \vert} \times {\vert N(\{0 \to 1\}) \vert}
$$

But this is a [[cylinder object]] in topological spaces, hence ${\vert N(\eta) \vert}$ is a [[left homotopy]].

=--

+-- {: .num_cor #RealizationOfEquivalenceIsHomotopyEquivalence}
###### Corollary

An [[equivalence of categories]] $\mathcal{C} \simeq \mathcal{D}$ induces a [[homotopy equivalence]] between their geometric realizations.

=--

+-- {: .num_remark }
###### Remark

The statement still remains true for a pair of [[adjoint functor]]s $\mathcal{C} \leftrightarrows \mathcal{D}$.

=--

+-- {: .num_remark }
###### Remark

Notice that the converse is far from true: Very different categories can have geometric realizations that are (weakly) homotopy equivalent. This is because geometric realization implicitly involves [[Kan fibrant replacement]]: it freely turns morphisms into [[equivalence in an (infinity,1)-category|equivalences]].

=--

+-- {: .num_cor #RealizationWithTerminalObjectIsContractible}
###### Corollary

If a [[category]] $\mathcal{C}$ has an [[initial object]] or a [[terminal object]], then its geometric realization is [[contractible]].

=--

+-- {: .proof}
###### Proof

Assume the case of a terminal object, the other case works [[formal dual|formally dually]]. Write $*$ for the terminal category.

Then we have an equality of functors

$$
  Id_* = (* \stackrel{\bottom}{\to} C \to *)
  \,,
$$

where the first functor on the right picks the terminal object, and we have a [[natural transformation]]

$$
  Id_C \Rightarrow (C \to * \stackrel{\bottom}{\to} C)
$$

whose components are the unique morphisms into the terminal object. 

By prop. \ref{NaturalTrafoMapsToHomotopy} it follows that we have a [[homotopy equivalence]] $\vert N(\mathcal{C}) \vert \to \vert N(\ast) \vert = \ast$.

=--


### Behaviour under homotopy colimits

+-- {: .num_prop }
###### Proposition


For $F \colon \mathcal{D} \to Cat$ a [[functor]], let 

$$
  {\vert N(F(-))\vert} 
   \;\colon\; 
  \mathcal{D} 
    \overset{F}{\longrightarrow} 
  Cat 
   \stackrel{\vert N(-) \vert}{\to}
  Top
$$ 

be its postcomposition with geometric realization of categories

Then we have a [[weak homotopy equivalence]]

$$
  {\left\vert N\left(\int F \right) \right\vert}
    \simeq
  hocolim {\vert F(N(-)) \vert}
$$

exhibiting the [[homotopy colimit]] in [[Top]] over $\vert N(F (-)) \vert$ as the geometric realization of the [[Grothendieck construction]] $\int F$ of $F$.

=--

This is due to ([Thomason 79](#Thomason79)). 


## Related concepts

* [[geometric realization]]

  * **of categories**, [[geometric realization of simplicial topological spaces|of simplicial topological spaces]], [[geometric realization of cohesive ∞-groupoids|of cohesive ∞-groupoids]]


## References

### General

For general references see also _[[nerve]]_ and _[[geometric realization]]_.

### Quillen's theorems A and B

The original articles are

* {#McCord66} [[Michael C. McCord]], _Singular homology groups and homotopy groups of finite topological spaces_, Duke Math. J. 33 (1966), 465-474

* {#Quillen72} [[Daniel Quillen]], _Higher algebraic K-theory, I: Higher K-theories_ Lect. Notes in Math. 341 (1972), 85-1 ([pdf](http://math.mit.edu/~hrm/kansem/quillen-higher-algebraic-k-theory.pdf))

* {#Quillen78} [[Daniel Quillen]], _Homotopy  properties  of  the  poset  of  nontrivial p-subgroups  of a group_, Adv. Math. 28 (1978), 101-128.

The geometric realization of [[Grothendieck constructions]] has been analyzed in

* {#Thomason79} [[R. W. Thomason]], _Homotopy colimits in the category of small categories_ , Math. Proc. Cambridge Philos. Soc. 85 (1979), no. 1, 91109.


Review is in


* {#Barmak10} [[Jonathan Barmak]], _On Quillen's Theorem A for posets_, Journal of Combinatorial Theory Series A, Volume 118 Issue 8, November, 2011
Pages 2445-2453  ([arXiv:1005.0538](http://arxiv.org/abs/1005.0538))

Further development includes

* [[Clark Barwick]], [[Daniel Kan]], _A Quillen theorem $B_n$ for homotopy pullbacks_ ([arXiv:1101.4879](http://arxiv.org/abs/1101.4879))

* [[David Roberts]], _[[davidroberts:Theorem A for topological categories]]_

 


[[!redirects geometric realization of a category]]

[[!redirects Quillen's theorem A]]
[[!redirects Quillen's theorem B]]
[[!redirects Quillen's Theorem A]]
[[!redirects Quillen's Theorem B]]
[[!redirects Quillen theorem A]]
[[!redirects Quillen theorem B]]
[[!redirects Quillen Theorem A]]
[[!redirects Quillen Theorem B]]
