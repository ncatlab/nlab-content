+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--

[[higher geometry]] $\leftarrow$ **Isbell duality**  $\rightarrow$ [[higher algebra]]

***


#Contents#
* tabel of contents
{:toc}

## Idea

A general abstract [[adjunction]] 

$$
  (\mathcal{O} \dashv Spec)
  : 
  CoPresheaves
  \underoverset{Spec}{O}{\leftrightarrows}
  Presheaves
$$ 

relates (higher) [[presheaves]] with (higher) [[copresheaves]] on a given ([[higher category theory|higher]]) [[category]] $C$: this is called **Isbell conjugation** or **Isbell duality** (after [[John Isbell]]).

To the extent that this adjunction descends to presheaves that are ([[higher topos theory|higher]]) [[sheaves]] and copresheaves that are ([[(infinity,1)-algebraic theory|higher]]) [[algebra over an algebraic theory|algebras]] this duality relates [[higher geometry]] with [[higher algebra]].

Objects preserved by the [[monad]] of this adjunction are called **Isbell self-dual**.

Under the interpretation of [[presheaves]] as generalized [[spaces]] and [[copresheaves]] as generalized [[quantities]] modeled on $C$ ([Lawvere 86](#Lawvere86), see at _[[space and quantity]]_), Isbell duality is the archetype of the [[duality]] between [[geometry]] and [[algebra]] that permeates mathematics (such as [[Gelfand duality]], [[Stone duality]], or the [[embedding of smooth manifolds into formal duals of R-algebras]]).


## Definition

Let $\mathcal{V}$ be a good enriching category (a [[cosmos]], i.e. a [[complete category|complete]] and [[cocomplete category|cocomplete]] [[closed monoidal category|closed]] [[symmetric monoidal category]]).

Let $\mathcal{C}$ be a [[small category|small]] $\mathcal{V}$-[[enriched category]].

Write $[\mathcal{C}^{op}, \mathcal{V}]$ and $[\mathcal{C}, \mathcal{V}]$ for the [[enriched functor categories]].

+-- {: .num_prop}
###### Proposition

There is a $V$-[[adjunction]]

$$
  (\mathcal{O} \dashv Spec)
  \colon
  [C, \mathcal{V}]^{op}
  \underoverset{Spec}{O}{\leftrightarrows}
  [C^{op}, \mathcal{V}]
$$

where 

$$
  \mathcal{O}(X) \colon c \mapsto [C^{op}, \mathcal{V}](X, \mathcal{V}(-,c))
  \,,
$$

and

$$
  Spec(A) \colon c \mapsto [C, \mathcal{V}]^{op}(\mathcal{V}(c,-),A)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is also called [[Isbell duality]]. Objects which are preserved by $\mathcal{O} \circ Spec$ or $Spec \mathcal{O}$ are called __Isbell self-dual__.

=--


The proof is mostly a tautology after the notation is unwound. The mechanism of the proof may still be of interest and be relevant for generalizations and for less tautological variations of the setup. We therefore spell out several proofs.

+-- {: .proof}
###### Proof A

Use the [[end]]-expression for the [[hom-object]]s of the [[enriched functor categories]] to compute

$$
  \begin{aligned}
     [C,\mathcal{V}]^{op}(\mathcal{O}(X), A)
     & :=
     \int_{c \in C} \mathcal{V}(A(c), \mathcal{O}(X)(c))
     \\
     & := 
     \int_{c \in C} \mathcal{V}(A(c), [C^{op}, \mathcal{V}](X, \mathcal{V}(-,c)))
     \\
     & :=
     \int_{c \in C} \int_{d \in C} \mathcal{V}(A(c), \mathcal{V}(X(d), \mathcal{V}(d,c)))
     \\
     & \simeq 
     \int_{d \in C} \int_{c \in C} \mathcal{V}(X(d), \mathcal{V}(A(c), \mathcal{V}(d,c)))
    \\
     & =:
     \int_{d \in C}  \mathcal{V}(X(d), [C,\mathcal{V}]^{op}(\mathcal{V}(d,-),A))
    \\
     & =:
     \int_{d \in C}  \mathcal{V}(X(d), Spec(A)(d))
    \\
     & =:
     [C^{op}, \mathcal{V}](X, Spec(A))
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Here apart from writing out or hiding the ends, the only step that is not a definition is precisely the middle one, where we used that $\mathcal{V}$ is a [[symmetric monoidal category|symmetric]] [[closed monoidal category]].

=--

The following proof does not use ends and needs instead slightly more preparation, but has then the advantage that its structure goes through also in great generality in [[higher category theory]].
{#ProofB}

+-- {: .proof}
###### Proof B

Notice that 

**Lemma 1:** $Spec(\mathcal{V}(c,-)) \simeq \mathcal{V}(-,c)$

because we have a natural isomorphism

$$
  \begin{aligned}
    Spec(\mathcal{V}(c,-))(d) 
    & :=
    [C,\mathcal{V}](\mathcal{V}(c,-), \mathcal{V}(d,-))
    \\
    & \simeq
    \mathcal{V}(d,c)
  \end{aligned}
$$ 

by the [[Yoneda lemma]].

From this we get

**Lemma 2:** $[C^{op}, \mathcal{V}](Spec \mathcal{V}(c,-), Spec A) \simeq 
    [C,\mathcal{V}](A, \mathcal{V}(c,-))$

by the sequence of natural isomorphisms

$$
  \begin{aligned}
     [C^{op}, \mathcal{V}](Spec \mathcal{V}(c,-), Spec A)
     & \simeq
     [C^{op}, \mathcal{V}](\mathcal{V}(-,c), Spec A)
     \\
     & \simeq (Spec A)(c)
     \\
     & := [C, \mathcal{V}](A, \mathcal{V}(c,-))
  \end{aligned}
  \,,
$$

where the first is Lemma 1 and the second the [[Yoneda lemma]].

Since (by what is sometimes called the [[co-Yoneda lemma]]) every object $X \in [C^{op}, \mathcal{V}]$ may be written as a [[colimit]]

$$
  X \simeq {\lim_\to}_i \mathcal{V}(-,c_i) 
$$

over [[representable functor|representables]] $\mathcal{V}(-,c_i)$ we have

$$
  X \simeq {\lim_\to}_i Spec(\mathcal{V}(c_i,-))
  \,.
$$

In terms of the same diagram of representables it then follows that

**Lemma 3:** 

$$
  \mathcal{O}(X) \simeq {\lim_{\leftarrow}}_i \mathcal{V}(c_i,-)
$$

because using the above colimit representation and the Yoneda lemma we have natural isomorphisms

$$
  \begin{aligned}
     \mathcal{O}(X)(d) 
     &=
     [C^{op}, \mathcal{V}](X, \mathcal{V}(-,c))
     \\
     & \simeq
     [C^{op}, \mathcal{V}]({\lim_\to}_i \mathcal{V}(-,c_i), \mathcal{V}(-,c))
     \\
     & \simeq
     {\lim_\leftarrow}_i [C^{op}, \mathcal{V}](\mathcal{V}(-,c_i), \mathcal{V}(-,c))
     \\
     & \simeq 
     {\lim_\leftarrow}_i \mathcal{V}(c_i,c)
  \end{aligned}
  \,.
$$


Using all this we can finally obtain the adjunction in 
question by the following sequence of natural isomorphisms

$$
  \begin{aligned}
     [C,\mathcal{V}]^{op}(\mathcal{O}(X), A)
     & 
     \simeq
     [C,\mathcal{V}](A, {\lim_\leftarrow}_i \mathcal{V}(c_i,-), )
     \\
     & \simeq 
     {\lim_{\leftarrow}}_i [C, \mathcal{V}](A, \mathcal{V}(c_i,-))
     \\
     & \simeq 
     {\lim_{\leftarrow}}_i [C^{op}, \mathcal{V}](Spec \mathcal{V}(c_i,-), Spec A)
     \\
     & \simeq
     [C^{op}, \mathcal{V}]({\lim_{\to}}_i  Spec \mathcal{V}(c_i,-), Spec A)
     \\
     & \simeq
     [C^{op}, \mathcal{V}](X, Spec A)     
  \end{aligned}
  \,.
$$

=--

The pattern of this proof has the advantage that it goes through in great generality also on [[higher category theory]] without reference to a higher notion of enriched category theory.



+-- {: .num_defn}
###### Definition

An object $X$ or $A$ is **Isbell-self-dual** if 

* $A \stackrel{}{\to} \mathcal{O} Spec(A)$ is an [[isomorphism]] in $[C,\mathcal{V}]$;

* $X \to Spec \mathcal{O} X$ is an [[isomorphism]] in $[C^{op}, \mathcal{V}]$, respectively.


=--

+-- {: .num_remark}
###### Remark

Under certain circumstances, Isbell duality can be extended to large $\mathcal{V}$-enriched categories $C$. For example, if $C$ has a small generating subcategory $S$ and a small cogenerating subcategory $T$, then for each $F: C^{op} \to \mathcal{V}$ and $G: C \to \mathcal{V}$, one may construct $\mathcal{O}(F)$ and $Spec(G)$ objectwise as appropriate subobjects in $\mathcal{V}$: 

$$\mathcal{O}(F)(c) = [C^{op}, \mathcal{V}](F, C(-, c)) \hookrightarrow \int_{s: S} \mathcal{V}(F s, \hom(s, c))$$ 

$$Spec(G)(c) = [C, \mathcal{V}](G, C(c, -)) \hookrightarrow \int_{t: T} \mathcal{V}(G t, \hom(c, t))$$

=--

## Example

In the simplest case, namely for an ordinary category $\mathcal{C}$, the adjunction between presheaves and copresheaves arises as follows.  

The category of [[presheaves]] $[\mathcal{C}^{op}, \mathrm{Set}]$ is the [[free cocompletion]] of $\mathcal{C}$.  This means that any functor 

$$f \colon \mathcal{C} \to \mathcal{D}$$ 

to a [[cocomplete category]] $\mathcal{D}$ extends along the [[Yoneda embedding]] $y \colon \mathcal{C} \to [\mathcal{C}^{op}, \mathrm{Set}]$ to a [[cocontinuous functor]]  

$$F \colon [\mathcal{C}^{op}, \mathrm{Set}] \to \mathcal{D}$$

in a manner unique up to natural isomorphism.

Dually, the category of [[copresheaves]]  $[\mathcal{C}, \mathrm{Set}]^{op}$ is the [[free completion]] of $\mathcal{C}$.  This means that any functor 

$$g \colon \mathcal{C} \to \mathcal{D}$$ 

to a [[complete category]] $\mathcal{D}$ extends along the [[co-Yoneda lemma|co-Yoneda embedding]] $z \colon \mathcal{C} \to [\mathcal{C}, \mathrm{Set}]^{op}$ to a [[continuous functor]].

$$G \colon [\mathcal{C}, \mathrm{Set}]^{op} \to \mathcal{D}$$

in a manner unique up to natural isomorphism.

We can apply these ideas to get the functors involved in Isbell duality.   The presheaf category $[\mathcal{C}^{op}, \mathrm{Set}]$ has all limits, so we can extend the Yoneda embedding to a continuous functor

$$ Y \colon [\mathcal{C}, \mathrm{Set}]^{op} \to [\mathcal{C}^{op}, \mathrm{Set}] $$

from copresheaves to presheaves.   Dually, the copresheaf category $[\mathcal{C}, \mathrm{Set}]^{op}$ has all colimits, so we can extend the co-Yoneda embedding to a cocontinuous functor 

$$ Z \colon [\mathcal{C}^{op}, \mathrm{Set}] \to [\mathcal{C}, \mathrm{Set}]^{op} $$

from presheaves to copresheaves.   

Isbell duality says that these are adjoint functors: $Y$ is right adjoint to $Z$.


## Properties

###Relation to Yoneda embedding

$Spec$ is the [[left Kan extension]] of the [[Yoneda embedding]] along the contravariant Yoneda embedding, while $\mathcal{O}$ is the left Kan extension of the contravariant Yoneda embedding along the Yoneda embedding. 

The [[codensity monad]] of the [[Yoneda embedding]] is isomorphic to the monad induced by the Isbell adjunction, $Spec \mathcal{O}$ ([Di Liberti 19, Thrm 2.7](#DiLiberti)).

### Respect for limits

Choose any [[class]] $L$ of [[limit]]s in $C$ and write $[C,\mathcal{V}]_\times \subset [C,\mathcal{V}]$ for the [[full subcategory]] consisting of those functors preserving these limits. 

+-- {: .num_prop}
###### Proposition

The $(\mathcal{O} \dashv Spec)$-adjunction does descend to this inclusion, in that we have an adjunction

$$
  (\mathcal{O} \dashv Spec)
  :
  [C, \mathcal{V}]_{\times}^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  [C^{op}, \mathcal{V}]
$$

=--

+-- {: .proof}
###### Proof

Because the [[hom-functor]]s preserves all [[limit]]s:

$$
  \begin{aligned}
    \mathcal{O}(X)({\lim_{\leftarrow}}_j c_j)
    & := [C^{op}, \mathcal{V}](X,\mathcal{V}(-,{\lim_{\leftarrow}}_j c_j))
    \\
    & \simeq [C^{op}, \mathcal{V}](X,{\lim_{\leftarrow}}_j  \mathcal{V}(-,c_j))
    \\
    & \simeq {\lim_{\leftarrow}}_j  [C^{op}, \mathcal{V}](X,\mathcal{V}(-,c_j))
    \\
    & =: {\lim_{\leftarrow}}_j \mathcal{O}(X)(c_j)
  \end{aligned}
  \,.
$$ 

=--



### Isbell self-dual objects

+-- {: .num_prop}
###### Proposition

All [[representable functor|representables]] are Isbell self-dual.

=--

+-- {: .proof}
###### Proof

By [Proof B , lemma 1](#ProofB) we have a [[natural isomorphism]]s in $c \in C$

$$
  Spec(\mathcal{V}(c,-)) \simeq \mathcal{V}(-,c)
  \,.
$$

Therefore we have also the natural isomorphism

$$
  \begin{aligned}
     \mathcal{O} Spec \mathcal{V}(c,-)(d)
     & \simeq
     \mathcal{O} \mathcal{V}(-,c) (d)
     \\
     & :=
      [C^{op}, \mathcal{V}](\mathcal{V}(-,c), \mathcal{V}(-,d))
     \\
     & \simeq
     \mathcal{V}(c,d)
  \end{aligned}
  \,,
$$

where the second step is the [[Yoneda lemma]]. Similarly the other way round.

=--

### Isbell envelope

See [[Isbell envelope]].




## Examples and similar dualities

Isbell duality is a template for many other [[space]]/[[algebra]]-[[dualities]] in [[mathematics]]. 


### Function $T$-Algebras on presheaves {#FunctionAlgebrasOnPresheaves}

Let $\mathcal{V}$ be any [[cartesian closed category]]. 

Let $C := T$ be the [[syntactic category]] of a $\mathcal{V}$-enriched [[Lawvere theory]], that is a $\mathcal{V}$-category with finite [[product]]s such that all objects are generated under products from a single object $1$.

Then write $T Alg := [C,\mathcal{V}]_\times$ for category of product-preserving functors: the category of $T$-algebras. This comes with the canonical forgetful functor

$$
  U_T : T Alg \to \mathcal{V} :   A \mapsto A(1)
$$

Write 

$$
  F_T : T^{op} \hookrightarrow T Alg
$$ 

for the [[Yoneda embedding]]. 

+-- {: .num_defn}
###### Definition

Call 

$$
  \mathbb{A}_T := Spec(F_T(1))  \in [C^{op}, \mathcal{V}]
$$

the **$T$-line object**.

=--

+-- {: .num_lemma}
###### Observation

For all $X \in [C^{op}, \mathcal{V}]$ we have

$$
  \mathcal{O}(X) \simeq
  [C^{op}, \mathcal{V}](X, Spec(F_T(-)))
  \,.
$$

In particular 

$$
  U_T(\mathcal{O}(X)) \simeq [C^{op}, \mathcal{V}](X,\mathbb{A}_T)
  \,.
$$

=--


+-- {: .proof}
###### Proof

We have isomorphisms natural in $k \in T$

$$
\begin{aligned}
  [C^{op}, \mathcal{V}](X, Spec(F_T(k)))
  & \simeq
  T Alg(F_T(k), \mathcal{O}(X))
  \\
  & \simeq
  \mathcal{O}(X)(k)
\end{aligned}
$$

by the above adjunction and then by the [[Yoneda lemma]].

=-- 


All this generalizes to the following case:

instead of setting $C := T$ let more generally

$$
  T \subset C \subset T Alg^{op}
$$

be a [[small category|small]] [[full subcategory]] of $T$-algebras, containing all the free $T$-algebras.

Then the original construction of $\mathcal{O} \dashv Spec$ no longer makes sense, but that in terms of the line object still does

+-- {: .num_prop}
###### Proposition

Set

$$
 Spec A : B \mapsto T Alg(A,B)
$$

and

$$
  \mathcal{O}(X) : k \mapsto 
  [C^{op}, \mathcal{V}](X, Spec(F_T(k)))
  \,.
$$

Then we still have an adjunction

$$
  (\mathcal{O} \dashv Spec)
  :
  T Alg^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  [C^{op}, \mathcal{V}]
  \,.
$$


=--


+-- {: .proof}
###### Proof


$$
  \begin{aligned}
    T Alg^{op}(\mathcal{O}(X), A)
    & :=
    \int_{k \in T} \mathcal{V}( A(k), \mathcal{O}(X)(k) )
    \\
    & := 
    \int_{k \in T} \mathcal{V}( A(k), [C^{op}, \mathcal{V}](X, Spec(F_T(k))) )
    \\
    & := \int_{k \in T} \int_{B \in C}
    \mathcal{V}(A(k), \mathcal{V}(X(B), T Alg(F_T(k), B) ))
    \\
    & \simeq \int_{k \in T} \int_{B \in C}
    \mathcal{V}(A(k), \mathcal{V}(X(B), B(k) ))
    \\
    & \simeq \int_{k \in T} \int_{B \in C}
    \mathcal{V}(X(B), \mathcal{V}(A(k), B(k) ))
    \\
    & =: \int_{B \in C} \mathcal{V}(X(B), T Alg(A,B))
    \\
    & =:
    \int_{B \in C} \mathcal{V}(X(B), Spec(A)(B))
    \\
    & =:
    [C^{op}, Set](X,Spec(A))
  \end{aligned}
  \,.
$$

The first step that is not a definition is the [[Yoneda lemma]]. The step after that is the symmetric-closed-monoidal structure of $\mathcal{V}$.

=--

### Function $k$-algebras on derived $\infty$-stacks {#FuncCompDerStacks}

The structure of our [Proof B](#ProofB) above goes through in higher category theory. 

Formulated in terms of [[derived stack]]s over the [[(∞,1)-category]] of [[dg-algebra]]s, this is essentially the argument appearing on [page 23](http://arxiv.org/PS_cache/arxiv/pdf/1002/1002.3636v1.pdf#page=23) of ([Ben-ZviNadler](#Ben-ZviNadler)).

### Function $T$-algebras on $\infty$-stacks

for the moment see at _[[function algebras on ∞-stacks]]_.

### Function 2-algebras on algebraic stacks

see [[Tannaka duality for geometric stacks]]

### Gelfand duality
 {#GelfandDuality}

[[Gelfand duality]] is the [[equivalence of categories]] between (nonunital) commutative [[C-star algebra|C*-algebras]] and ([[locally compact space|locally]]) [[compact topological spaces]]. See there for more details.

### Serre-Swan theorem

The [[Serre-Swan theorem]] says that suitable [[modules]] over an commutative [[C-star algebra|C*-algebra]] are equivalently modules of [[sections]] of [[vector bundles]] over the [Gelfand-dual](#GelfandDuality) topological space.


## Related concepts

* [[duality between algebra and geometry]]

* [[function algebra]]

* [[function algebras on ∞-stacks]]

* [[nucleus of a profunctor]]

[[!include Isbell duality - table]]


## References

The original articles on Isbell duality and the [[Isbell envelope]] are

* {#Isbell66} [[John Isbell]], _Structure of categories_, Bulletin of the American Mathematical Society 72 (1966), 619&#8211; 655. ([project euclid](http://projecteuclid.org/euclid.bams/1183528163))

* {#Isbell67} [[John Isbell]], _Normal completions of categories_, Reports of the Midwest Category Seminar, vol. 47, Springer, 1967, 110&#8211;155.

More recent discussion is in

* {#Lawvere86} [[William Lawvere]], p. 17 of _Taking categories seriously_, Revista Colombiana de Matematicas, XX (1986) 147-178, reprinted as: Reprints in Theory and Applications of Categories, No. 8 (2005) pp. 1-24 ([web](http://tac.mta.ca/tac/reprints/articles/8/tr8abs.html))

* [[Michael Barr]], John Kennison, R. Raphael, Isbell Duality, Theory and Applications of Categories, Vol. 20, 2008, No. 15, pp 504-542. ([web](http://www.tac.mta.ca/tac/volumes/20/15/20-15abs.html))

* [[Richard Garner]], _The Isbell monad_, Advances in Mathematics **274** (2015) pp.516-537. ([draft](http://comp.mq.edu.au/~rgarner/Papers/Isbell.pdf))

* [[Vaughan Pratt]], _Communes via Yoneda, from an elementary perspective_, Fundamenta Informaticae 103 (2010), 203&#8211;218.

* {#DL19} [[Ivan Di Liberti]], [[Fosco Loregian]], _On the Unicity of Formal Category Theories_, arXiv:1901.01594 (2019). ([abstract](https://arxiv.org/abs/1901.01594))

* {#DiLiberti} [[Ivan Di Liberti]], _Codensity: Isbell duality, pro-objects, compactness and accessibility_, ([arXiv:1910.01014](https://arxiv.org/abs/1910.01014))

* [[Tom Avery]], [[Tom Leinster]], _Isbell conjugacy and the reflexive completion_, arXiv:2102.08290 (2021). ([abstract](https://arxiv.org/abs/2102.08290))

Isbell conjugacy for [[(∞,1)-presheaves]] over the [[(∞,1)-category]] of duals of [[dg-algebra]]s is discussed around page 32 of

* [[David Ben-Zvi]], [[David Nadler]], _Loop spaces and connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))
{#Ben-ZviNadler}

in 

* {#Toen} [[nLab:Bertrand Toën]], _Champs affines_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))


Isbell self-dual [[∞-stack]]s over duals of commutative [[associative algebra]]s are called _affine stacks_. They are characterized as those objects that are _small_ in a sense and local with respect to the [[cohomology]] with coefficients in the canonical [[line object]].

A generalization of this latter to $\infty$-stacks over duals of [[algebra over a Lawvere theory|algebras over arbitrary abelian Lawvere theories]] is the content of 

* {#Stel} [[Herman Stel]], _$\infty$-Stacks and their function algebras -- with applications to $\infty$-Lie theory_, master thesis (2010) ([[schreiber:master thesis Stel|web]])


See also

* MathOverflow: [theme-of-isbell-duality](http://mathoverflow.net/questions/84641/theme-of-isbell-duality)

* R.J. Wood, _Some remarks on total categories_, J. Algebra __75_:2, 1982, 538&#8211;545 <a href="http://dx.doi.org/10.1016/0021-8693(82)90055-2">doi</a>

[[!redirects Isbell dualities]]

[[!redirects Isbell conjugation]]
[[!redirects Isbell conjugations]]

[[!redirects Isbell adjunction]]
[[!redirects Isbell adjunctions]]

