
<div class="rightHandSide toc" markdown="1">
[[!include (infinity,1)-topos - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea 

An object in an [[(∞,1)-topos]] $\mathbf{H}$ may be regarded as an [[∞-groupoid]] with extra structure.

An object in the [[(∞,1)-category]] $\mathbf{L}$ of [[Lie-∞-algebroid|∞-Lie algebroid]]s is an [[infinitesimal object|infinitesimal]] version of an $\infty$-groupoid.

A [[reflective (∞,1)-subcategory|reflective embedding]] $\mathbf{L} \hookrightarrow \mathbf{H}$ equips $\mathbf{H}$ with a _rational structure_ and a notion of [[Lie theory]]. 

This is _well adapted_ if composed with the [[global section]]s morphism $\Gamma$ 

$$
  \mathbf{L} \hookrightarrow \mathbf{H} \stackrel{\Gamma}{\to} \infty Grpd
$$

this identifies $\mathbf{L}$ inside [[? Grpd]] as the [[rational space]]s of [[rational homotopy theory]].

## Definition

### $\infty$-Lie algebroids

For the context of ordinary geometry, write $\mathbf{L} := ((Alg_k^{\Delta})^{op})^\circ$ for the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by the [[opposite category|opposite]] of the [[model structure on cosimplicial algebras]] over $k$. By the [[monoidal Dold-Kan correspondence]] this is [[Quillen equivalence|equivalently]] the [[model structure on dg-algebra|model structure on commutative non-negative cochain dg-algebra]]s $dgAlg_k^+$. A cofibrant object in $dgAlg_k^+$ may be thought of as the [[Chevalley-Eilenberg algebra]] of an [[Lie-∞-algebroid|∞-Lie algebroid]]. 

Accodingly, the opposite $\mathbf{L}$ may be thought of as the **$(\infty,1)$-category of (∞,1)-Lie algebroids**.

For the context of [[derived geometry]] take $\mathbf{L}$ to be given by the model structure on _all_ (unbounded) dg-algebras, corresponding to that on cosimplicial simplicial algebras.


+-- {: .query}

[[Urs Schreiber|Urs]]: Possibly there should be an intrinsic way to characterize $\mathbf{L}$ given $\mathbf{H}$. Something like like that $\mathbf{L}$ is the [[localization of an (∞,1)-category|localization]] of $\mathbf{H}$ at morphisms that induce isomorphisms on "rational cohomology" or the like.

=--

### Rational structure and Lie theory

For $\mathbf{H}$ an [[(∞,1)-topos]], we shall say that a **rational structure** on $\mathbf{H}$ or a **Lie theory structure** on $\mathbf{H}$ is an [[adjoint (∞,1)-functor|(∞,1)-adjunction]] 

$$
  \mathbf{L}
  \stackrel{\overset{Lie}{\leftarrow}}{\underset{}{\hookrightarrow}}
  \mathbf{H} 
$$


that exhibits $\mathbf{L}$ as a [[reflective (∞,1)-subcategory]] of $\mathbf{H}$.

We think of the image of $\mathbf{L}$ in $\mathbf{H}$ as consisting of those structured [[∞-groupoid]]s whose [[k-morphism]]s for all $k$ have [[infinitesimal object|infinitesimal]] extension. 

The [[localization of an (∞,1)-category|localization]] [[(∞,1)-monad]]

$$
  (-)\otimes R : 
  \mathbf{H} \stackrel{Lie}{\to}
  \mathbf{L} \stackrel{}{\hookrightarrow} 
  \mathbf{H}
$$

acts like $\infty$-[[Lie theory|Lie differentiation]]: it sends an $\infty$-groupoid to its best approximation by an infinitesimal $\infty$-groupoid.

### Ordinary rational homotopy

There is canonically a Lie theory-like structure on the terminal $(\infty,1)$-topos [[∞Grpd]] 

$$
   ( \Omega^\bullet_{Sl} \dashv |-|) : 
   \mathbf{L} \stackrel{\overset{\Omega^\bullet_{Sl}}{\leftarrow}}{\underset{|-|}{\to}}
   \infty Grpd
$$

given by ordinary [[rational homotopy theory]]: 

* the [[(∞,1)-functor]] $\Omega_{Sl}$ produces a Sullivan model of a topological space;

* the functor $|-|$ sends a Sullivan model to the corresponding [[rational space]].

* the monad $|\Omega_{Sl}(-)|$ is [[rationalization]].


### Internal rational homotopy

For $\mathbf{L} \hookrightarrow \mathbf{H}$ an $(\infty,1)$-topos with Lie structure, we say that the Lie structure is **well adapted** if composed with the terminal [[global section]]s [[geometric morphism]]

$$
  \mathbf{H} 
   \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

the reflective embedding induces the Lie theory structure on [[∞Grpd]]

$$
  \mathbf{L}
   \stackrel{
     \overset{\Omega_{Sl}}{\leftarrow}}
     {\underset{|-|}{\to}}
  \infty Grpd
  \;\;\;
  \simeq
  \;\;\;
  \mathbf{L}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\hookrightarrow}}
  \mathbf{H} 
   \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
  \,.
$$




## Examples

### $\infty$-Stacks on formal duals of algebras

Consider the [[site]] $C$ whose underlying category is

$$C = (Alg_k)^{op}$$ 

equipped with the [[fpqc-topology]].

Let 

$$
  \mathbf{H} = Sh_{(\infty,1)}(C) = (sPSh(C)_{loc})^\circ
$$

be the [[hypercomplete (∞,1)-topos]] of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]] on $C$, [[presentable (∞,1)-category|presented]] by the local injective [[model structure on simplicial presheaves]] on $C$. 

In the language used here, the article

* [[Bertrand Toen]], _Affine stacks (Champs affines)_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219)) .

shows that this $\mathbf{H}$ has a well-adapted rational structure.

#### The rational structure {#ToenRationalStructure}

Write $\mathbb{A}^1 \in sPSh(C)$ for the [[lined topos|line object]], the formal dual of the free $k$-algebra $F_k[X]$ on one generator. This means that 

$$
  \mathbb{A}^1 : Spec A \mapsto Alg_k(F_k[X], A) \simeq A
$$

is the tautological algebra valued presheaf that sends $Spec A$ to $A$.

+-- {: .un_def }
###### Definition

Define [[sSet]]-[[enriched functor]]s

$$
  \mathcal{O} : (Alg_k^\Delta)^{op}
   \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
   sPSh((Alg_k)^{op})
   :
   Spec
$$

by

$$
  \mathcal{O} := Hom_{sPsh(C)}(-,\mathbb{A}^1) 
$$ 

and 

$$
  Spec : A \mapsto (Alg_k^\Delta)^{op}(\mathcal{O}(-),A)
  \,.
$$ 

=--

This is considered in [To06, section 2.2](http://arxiv.org/PS_cache/math/pdf/0012/0012219v6.pdf#page=42).

In particular for $*$ the terminal presheaf we have 

$$
  \mathcal{O}(*) = sPSh(*, \mathbb{A}^1) = \int_{Spec A \in Alg_k} Hom_{Set}(*,A)
  = \lim_{A \in Alg_k} A
  = k     
$$

because $k$ is initial in $Alg_k$.



+-- {: .un_prop }
###### Proposition

The functors $\mathcal{O}$ and $Spec$ form an [[sSet]]-[[enriched category theory|enriched]] [[Quillen adjunction]]

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

This proof works very generally whenever hypercovers $Y \to U$ over representables induce isomorphisms in $\mathbb{A}^1$-cohomology as seen by the line object $\mathbb{A}^1$.

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

exhibts $\mathbf{L}$ as a [[reflective (∞,1)-subcategory]] of $\mathbf{H}$.

=--

This appears as [To06, cor 2.2.3](http://arxiv.org/PS_cache/math/pdf/0012/0012219v6.pdf#page=44).


#### The well-adapted rational structure {#ToenWellAdapt}

+-- {: .un_prop }
###### Proposition

For $k = \mathbb{Q}$,  for $X \in \infty Grpd$, the canonical morphism

$$
  X \to |\Omega_{SL}X| :=  \Gamma \circ Spec \circ \mathcal{O} \circ LConst X
$$

(where all functors denote the [[derived functor|derived]] version) is a [[rational topological space|rational equivalence]].

=--

+-- {: .proof}
###### Proof


This appears as [To, theorem. 2.5.1](http://arxiv.org/PS_cache/math/pdf/0012/0012219v6.pdf#page=65).

=--


### Derived $\infty$-stacks on formal duals of simplicial algebra

Let now $C = $ [[simplicial algebra]]s ${}^{op}$. Then...

... essentially as above, see [Ben-Zvi/Nadler](http://arxiv.org/abs/1002.3636)

### $\infty$-Stacks on formal duals of smooth algebras

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

The localization denoted $\mathbf{H} \to \mathbf{L} \hookrightarrow \mathbf{H}$ above is called **affinization** in these articles.

Comments on the generalization from plain algebras to [[smooth algebra]]s are at

* [[Urs Schreiber]], _[[schreiber:Chevalley-Eilenberg algebra]]_

[[!redirects rational homotopy theory in an (∞,1)-topos]]