> under construction

#Contents#
* automatic table of contents goes here
{:toc}


## Idea and definition

An object in an [[(∞,1)-topos]] $\mathbf{H}$ over an [[(∞,1)-site]] $C$ may be regarded as an [[∞-groupoid]] modeled on $C$. A cosimplicial commutative algebra, i.e an object in $\mathbf{L} := (Alg_k^{\Delta})^{op}$, may be regarded as a [[Lie-∞-algebroid]].

If $\mathbf{L}$ is a [[reflective (∞,1)-subcategory]] of $\mathbf{H}$

$$
  \mathbf{L}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\hookrightarrow}}
  \mathbf{H} 
$$

the inclusion identifies $\infty$-Lie algebroids with $\infty$-groupoids whose  [[k-morphism]]s are
[[infinitesimal object|infinitesimal]].

The [[(∞,1)-monad]]

$$
  \mathbf{\flat}_{inf} := Spec \circ \mathcal{O} : 
  \mathbf{H} \stackrel{\mathcal{O}}{\to}
  \mathbf{L} \stackrel{Spec}{\to} 
  \mathbf{H}
$$

acts like $\infty$-[[Lie theory|Lie differentiation]]: it sends an $\infty$-groupoid to its best approximation by an infinitesimal $\infty$-groupoid.

Composed with the terminal [[global section]]s [[geometric morphism]]

$$
  \mathbf{H} 
   \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

the reflective embedding induces a notion of Lie theory on bare $\infty$-groupoids. 

$$
  \mathbf{L}
   \stackrel{
     \overset{\Omega_{SL}}{\leftarrow}}
     {\underset{|-|}{\to}}
  \infty Grpd
  \;\;\;
  :=
  \;\;\;
  \mathbf{L}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\hookrightarrow}}
  \mathbf{H} 
   \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
  \,.
$$


For suitable choices of $\mathbf{H}$, this is ordinary [[rational homotopy theory]]:

* the functor $\Omega_{SL}$ produces a Sullivan model of a topological space;

* the functor $|-|$ sends a Sullivan model to the corresponding [[rational space]].

* the monad $|\Omega_{SL}(-)|$ is [[rationalization]].

+-- {: .query}

[[Urs Schreiber]]: Possibly there should be an intrinsic way to characterize $\mathbf{L}$ given $\mathbf{H}$. Something like like that $\mathbf{L}$ is the [[localization of an (∞,1)-category|localization]] of $\mathbf{H}$ at morphisms that induce isomorphisms "on rational cohomology" or the like.

=--

## Examples

### On formal duals of algebras

Consider the [[site]] $C$ whose underlying category is

$$C = (Alg_k)^{op}$$ 

equipped with the [[fpqc-topology]].

Let 

$$
  \mathbf{H} = Sh_{(\infty,1)}(C) = (sPSh(C)_{loc})^\circ
$$

be the [[(∞,1)-topos]] [[presentable (∞,1)-category|presented]] by the local injective [[model structure on simplicial presheaves]] on $C$. 

The following shows that this gives a model of $\infty$-Lie theory that recovers ordinary rational homotopy theory.

Write $k \in sPSh(C)_{loc}$ for the line object. 


+-- {: .un_def }
###### Definition

Define [[sSet]]-[[enriched functor]]s

$$
  \mathcal{O} := Hom_{sPsh(C)}(-,k) : sPSh(C) \to (Alg_k^{\Delta})^{op}
$$ 

and 

$$
  Spec : A \mapsto (Alg_k^\Delta)^{op}(\mathcal{O}(-),A)
  \,.
$$ 

=--

This is considered in [To06, section 2.2](http://arxiv.org/PS_cache/math/pdf/0012/0012219v6.pdf#page=42).

+-- {: .un_prop }
###### Proposition

These form an [[sSet]]-[[enriched category theory|enriched]] [[Quillen adjunction]]

$$
  (\mathcal{O} \dashv Spec) : sPSh(C)^{inj}_{loc} \stackrel{\leftarrow}{\to}
  (Alg_k^\Delta)^{op}
  \,.
$$

=--

This appears as [To06, prop. 2.2.2](http://arxiv.org/PS_cache/math/pdf/0012/0012219v6.pdf#page=44).

+-- {: .proof}
###### Proof

By the fact that $(Alg_k^\Delta)^{op}$ is a [[sSet]]-[[enriched model category]] so that the enriched hom is a right [[Quillen bifunctor]] it follows that for the _global_ model structure $sSSh(C)_{glob}^{inj}$ $Spec(-)$ is right Quillen.

Since $sPSh(C)_{loc}$ arises by [[Bousfield localization of model categories|left Bousfield localization]] at [[hypercover]]s, it suffices to show that $Spec$ sends fibrant object of $(Alg_k^\Delta)^{op}$ to simplicial presheaves that satisfy [[descent]] at hypercovers. But for this it suffices to observe that for $Y \to U$ a [[hypercover]], the $k$-cohomology of $Y$ is isomorphic to that of $U$, so that $\mathcal{O}(Y) \leftarrow \mathcal{O}(X)$ is a [[quasi-isomorphism]]: we need to check that

$$
  sPSh(Y, Spec A) \to sPSh(X,Spec A) 
$$

is an equivalence, which this is adjunct to

$$
  (Alg^\Delta)^{op}(\mathcal{O}(Y), A) \to (Alg^\Delta)^{op}(\mathcal{O}(X),A)
  \,.
$$

Since every object in $(Alg^{\Delta})^{op}$ is cofibrant and since $A$ is furthermore fibrant, this is the hom of a weak equivalence between cofibrant objects into a fibrant object and [[derived hom space|hence]] a weak equivalence.
 
=--

+-- {: .un_remark }
###### Remark

This proof works very generally whenever hypercovers $Y \to U$ over representables induce isomorphisms in $R$-cohomology as seen by the line object $R$.

=--

+-- {: .un_prop }
###### Proposition

The counit of the adjunction is an isomorphism

$$
  \mathcal{O} Spec A \stackrel{\simeq}{\leftarrow}
  A
  \,.
$$

=--

This appears as [To06, lemma. 2.2.1](http://arxiv.org/PS_cache/math/pdf/0012/0012219v6.pdf#page=43).


+-- {: .proof}
###### Proof

If we think of presheaves over $(Alg^\Delta)^{op}$ then this is just the [[Yoneda lemma]].

=--

+-- {: .un_cor }
###### Corollary

The right [[derived functor]] 

$$
  Spec : \mathbf{L} \stackrel{\leftarrow}{\hookrightarrow} \mathbf{H}
$$

exhibts $\mathbf{L}$ as a [[reflective (∞,1)-subcategory]] of $\mathbf{H}$..

=--

This appears as [To06, cor 2.2.3](http://arxiv.org/PS_cache/math/pdf/0012/0012219v6.pdf#page=44).


+-- {: .un_prop }
###### Proposition

For $k = \mathbb{Q}$,  for $X \in \infty Grpd$, canonical morphism

$$
  X \to |\Omega_{SL}X| :=  \Gamma \circ Spec \circ \mathcal{O} \circ LConst X
$$

(where all functors denote the [[derived functor|derived]] version) is a [[rational topological space|rational equivalence]].

=--

+-- {: .proof}
###### Proof


This appears as [To, theorem. 2.5.1](http://arxiv.org/PS_cache/math/pdf/0012/0012219v6.pdf#page=65).

=--


### On formal duals of simplicial algebra

Let now $C = $ [[simplicial algebra]]s ${}^{op}$. Then...

... essentially as above, see [Ben-Zvi/Nadler](http://arxiv.org/abs/1002.3636)

### On formal duals of smooth algebra

Let now $C = $ [[smooth loci]]. Then...

...(essentially as above, see [[schreiber:Chevalley-Eilenberg algebra]]).

## References


The [[Quillen adjunction]]

$$
  (\mathcal{O} \dashv Spec) : 
  sPSh((Alg_k^{op}))_{loc} \stackrel{\leftarrow}{\to}
  (Alg_k^{\Delta})^{op}
$$

was considered in

* [[Bertrand Toen]], _Affine stacks (Champs affines)_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219)) .

Its generalization to 

$$
  Sh_{(\infty,1)}((dgAlg_k^-)^{op})
  \stackrel{\leftarrow}{\to}
  (dgAlg_k)^{op}
$$

with $(dgAlg_k)^{op}$ the [[(∞,1)-site]] of non-positively graded cochain [[dg-algebra]]s is discussed in 

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv:math/1002.3636](http://arxiv.org/abs/1002.3636))

Comments on the generalization from plain algebras to [[smooth algebra]]s are at

* [[Urs Schreiber]], _[[schreiber:Chevalley-Eilenberg algebra]]_

[[!redirects rational homotopy theory in an (∞,1)-topos]]