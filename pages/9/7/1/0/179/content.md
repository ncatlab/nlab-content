

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An _$\infty$-Lie algebroid_ is the [[infinitesimal space|infinitesimal]] approximation to an [[∞-Lie groupoid]].
 
$\infty$-Lie algebroids are to [[∞-Lie groupoids]] as [[Lie algebras]] are to [[Lie groups]]. 

* [[Lie group]] - [[Lie algebra]]

* [[Lie groupoid]] - [[Lie algebroid]]

* [[∞-group|∞-Lie group]] - [[L-infinity-algebra|∞-Lie algebra]]

* [[∞-Lie groupoid]] - **$\infty$-Lie algebroid** .

One obtains $\infty$-Lie groupoids from $\infty$-Lie algebroids by [[Lie integration]].

In terms of [[synthetic differential geometry]] an $\infty$-Lie algebroid may be thought of as an [[∞-Lie groupoid]] all whose [[k-morphism]]-spaces over a given object are [[infinitesimal space]]s.

Since in typical [[Models for Smooth Infinitesimal Analysis|convenient models for synthetic differential geometry]] these infinitesimal spaces are represented by formal [[duality]] in terms of their [[smooth algebra]]s of functions, it follows that when [[∞-groupoid]]s are incarnated as [[simplicial object|simplicial]] [[smooth space]]s, an $\infty$-Lie algebroid

$$
  \mathfrak{a} = \left(
     \cdots \mathfrak{a}_2
     \stackrel{\to}{\stackrel{\to}{\to}} \mathfrak{a}_1 \stackrel{\to}{\to} \mathfrak{a}_0
  \right)
$$ 

may be modeled by [[cosimplicial algebra|cosimplicial]] [[smooth algebra]]s  

$$
  C^\infty(\mathfrak{a}) = \left(
     \cdots C^\infty(\mathfrak{a}_2)
     \stackrel{\leftarrow}{\stackrel{\leftarrow}{\leftarrow}} 
     C^\infty(\mathfrak{a}_1)
     \stackrel{\leftarrow}{\leftarrow} 
     C^\infty(\mathfrak{a}_0)
  \right)
  \,.
$$ 

Under the [[monoidal Dold-Kan correspondence]], these map by the [[Moore complex|normalized cochain complex functor]] $N$ to cochain [[dg-algebra]]s in non-negative degree:

$$
  CE(\mathfrak{a}) := N C^\infty(\mathfrak{a})
  \,.
$$

This dg-algebra is usefully thought of as the [[Chevalley-Eilenberg algebra]] of the $\infty$-Lie algebroid. If $\mathfrak{a} = \mathfrak{g}$ is an ordinary [[Lie algebra]], then this is indeed the ordinary Chevalley-Eilenberg algebra of that Lie algebra. 

In the literature on [[Lie algebroid]]s, however, $CE(\mathfrak{a})$ often goes by different names, such as "canonical complex" or "the complex that computes Lie algebroid cohomology". In the literature on what we here identify as $\infty$-Lie algebroids, the algebras $CE(\mathfrak{a})$ are often thought of as algebras of functions on [[NQ-supermanifold]]s.

Accordingly, there is a bit of room for different approaches of how to define the [[(∞,1)-category]] of [[∞-Lie algebroid]]s. A very general abstract [[nPOV]] perspective proceeds via the notion of [[function algebras on ∞-stacks]]:

for $T$ an abelian [[Lawvere theory]] (such as that of ordinary commutative and [[associative algebra]]s over a field or that of [[smooth algebra]]s) and for $C \hookrightarrow T Alg^{op}$ a small full subcategory of the spaces formally dual to these algebra, there is an [[(∞,1)-topos]] $\mathbf{H} = Sh_{(\infty,1)}{C}$ of [[∞-Lie groupoid]] modeled on the geometry of $T$-algebras and this is equipped with the canonical $T$-[[line object]] $\mathbb{A}$. 

The [[(∞,1)-category]] $\mathbf{L}$ of [[∞-Lie algebroid]]s is the [[reflective (∞,1)-subcategory]] that [[localization of an (∞,1)-category|localize]] $\mathbf{H}$ at those morphism that induce [[isomorphism]]s in the $\mathbb{A}$-[[cohomology]] internal to $\mathbf{H}$

$$
  \mathbf{L} \stackrel{\leftarrow}{\hookrightarrow}
  \mathbf{H}
  \,.
$$

In the case that $\mathbf{H} = Sh_{(\infty,1)}(C)$ is the [[(∞,1)-category of (∞,1)-sheaves]] on a [[site]] $C$ like the [[opposite category]] $Alg_{\mathbb{R}}^{op}$ of commutative (and suitably "small") [[algebra]]s, or the site $C = \mathbb{L}$ of [[smooth loci]], the opposite $C^\infty Alg^{op}$ of (suitably small) [[smooth algebra]], the line object is the [[real number|real line]] in the corresponding in ternal incarnation, and one finds then that 

$$
  \mathbf{L} \simeq ([\Delta, C^\infty Alg]^op)^\circ
$$

is the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by the the opposite of the [[model structure on cosimplicial rings|model structure on cosimplicial commutative (smooth) algebras]]. 

At least for the underlying plain algebras this is equivalent, by the [[monoidal Dold-Kan correspondence]], to the $(\infty,1)$-category presented by the opposite of the standard [[model structure on dg-algebras]] $(dgAlg^{op})^\circ$, for graded commutative cochain dg-algebras in non-negative degree. This is of course the category in which much of classical [[rational homotopy theory]] takes place, and indeed it has been noticed that much of classical rational homotopy theory may be understood as being about $\infty$-Lie theory. Notably the [[Sullivan construction]] of a [[topological space]] from a [[dg-algebra]] may be thought of as essentially being the [[Lie integration]] of the $\infty$-Lie algebroid corresponding to the dg-algebra to an [[∞-groupoid]]. This can straightforwardly be refined to an integration to an [[∞-Lie groupoid]].

See also [[∞-Lie algebroid cohomology]].

## Special Cases

* a $\infty$-Lie algebroid over the [[point]], $\mathfrak{a} = *$ is an **[[L-∞-algebra]]**;

* an $n$-[[truncated]] $\infty$-Lie algebroid is a **Lie $n$-algebroid**;

* an $\infty$-Lie algebroid the differential of whose [[Chevalley-Eilenberg algebra]] is "co-binary", i.e. $d : \mathfrak{a}^* \to a^* \oplus a^* \wedge g^*$, is **strict**.

So in particular

* a 1-Lie algebroid is a **[[Lie algebroid]]**;

* a 1-Lie algebroid over the point is a **[[Lie algebra]]**;

* a Lie $n$-algebroid over a point is a **[[Lie n-algebra]]**.

* a _[[BRST-complex]]_ is the [[Chevalley-Eilenberg algebra]]
  of an action-$\infty$-Lie algebroid of the 
  [[action]] of an $L_\infty$-algebra, see [[Lie ∞-algebroid representation]];

  more generally, the complexes appearing in [[BV-BRST formalism]] are 
  derived $\infty$-Lie algebroids, whose Chevalley-Eilenberg algebra may have generators in negative degree.

* a [[Courant algebroid]] is a certain Lie 2-algebroid.

* more  generally an [[n-symplectic manifold]] is a Lie $n$-algebroid.

* Standard examples of [[exterior differential system]]s are [[Chevalley?Eilenberg algebras]] of $L_\infty$-algebroids.


## Examples

### Tangent Lie algebroid {#TangentLieAlgebroid}

The following example is in a way the archetypical example on which all others are modeled in a sense.

For $X$ any [[smooth manifold]], there is a standard notion of the [[Lie algebroid]] which is the [[tangent Lie algebroid]] of $X$. As an $\infty$-Lie algebroid, this is the [[simplicial object|simplicial]] [[smooth locus]] given by the [[infinitesimal singular simplicial complex]] 

$$
  T X = 
  \left(
      \cdots 
      X^{(\Delta^2_{inf})} 
        \stackrel{\to}{\stackrel{\to}{\to}} 
        X^{(\Delta^1_{inf})} 
       \stackrel{\to}{\to} X
  \right)
$$

of $X$. By the central observation on combinatorial [[differential forms in synthetic differential geometry]] by [[Anders Kock]], the [[Chevalley-Eilenberg algebra]] of this is indeed isomorphic to the [[de Rham complex]] of $X$:

$$
  CE(T X) := N C^\infty(T X) \simeq (\Omega^\bullet(X), d_{dR})
  \,.
$$

For more details on the computations involved see [Spaces of infinitesimal k-simplices](http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl) at [[infinitesimal object]].

In particular for $X = \mathbb{R}^n$ a [[Cartesian space]], we have

$$
  T \mathbb{R}^n
  =
  \left(
      \cdots 
      \mathbb{R}^n \times \tilde D(2,n)
        \stackrel{\to}{\stackrel{\to}{\to}} 
        \mathbb{R}^n \times \tilde D(1,n)
       \stackrel{\to}{\to} 
       \mathbb{R}^n
  \right)   
  \,,
$$

where $\tilde D(k,n)$ is the [[smooth locus]] of [infinitesimal k-simplices](http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl) based at the origin in $\mathbb{R}^n$.


### Lie algebra {#LieAlgebra}


Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$. We describe how $\mathfrak{g}$ looks when regarded as a special case of an $\infty$-Lie algebroid.

Write 

$$
  \mathbf{B}G =
  \left(
     \cdots G \times G 
     \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} * 
  \right)
$$

for the [[delooping]] [[groupoid]] of $G$, regarded as an an [[∞-Lie groupoid]] modeled by a simplicial [[smooth space]].

We claim that a morphism 

$$
  \omega : T U \to \mathbf{B}G
$$

from the tangent Lie algebroid of some $U \in $ [[CartSp]] is [[groupoid of Lie-algebra valued forms|flat Lie-algebra valued form]] and how that can be used to find the [[Lie algebra]] $\mathfrak{g}$ as the infinitesimal sub-$\infty$-groupoid

$$
  \mathbf{b}\mathfrak{g} \hookrightarrow \mathbf{B}G
$$

inside $\mathbf{B}G$.

Since $\mathbf{B}G$ is [[simplicial skeleton|2-coskeletal]] (being the [[nerve]] of a [[groupoid]]) a morphism $T U \to \mathbf{B}G$ is fixed already under its 2-[[truncated|truncation]]

$$
  \array{
    U \times \tilde D(2,n) 
     &\stackrel{\omega_2}{\to}& 
    G \times G
    \\
    \downarrow \downarrow \downarrow && 
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    \\
    U \times \tilde D(1,n) &\stackrel{\omega_1}{\to}& G
    \\
    \downarrow \downarrow && \downarrow \downarrow
    \\
    U &\to& *
  }
  \,.
$$

It is clear that $\omega_1$ factors through the inclusion $\tilde D(1,dim(G)) \hookrightarrow G$ that sends the unique point of $\tilde D(1, dim(G))$ to the neutral element (by respect for the degeneracy maps).
Then from that one finds that $\omega_2$ factors through the inclusion $\tilde D(2, dim(G)) \hookrightarrow G \times G$ that sends the unique point of $\tilde D(2,dim(G))$ to $(e,e) \in G \times G$. And evidently these two factorizations are universal, in that every other factorization will uniquelyy factor through these

$$
  \array{
    U \times \tilde D(2,n) 
     &\stackrel{\omega_2}{\to}& 
    \tilde D(2,dim(G))
    &\hookrightarrow&
    G \times G
    \\
    \downarrow \downarrow \downarrow 
     && 
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    &&
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    \\
    U \times \tilde D(1,n) 
    &\stackrel{\omega_1}{\to}& 
    \tilde D(1, dim(G))
    &\hookrightarrow&
    G
    \\
    \downarrow \downarrow 
    && \downarrow \downarrow
    && \downarrow \downarrow
    \\
    U &\to& * &\to& *
  }
  \,.
$$

The universal object found this way we claim is the Lie algebra $\mathfrak{g}$ in its incarnation as an infinitesimal $\infty$-Lie groupoid

$$
  \begin{aligned}
    b \mathfrak{g}
    &:=
    InitialObject( T U\downarrow \mathbb{L}^{Delta^{op}}\downarrow \mathbf{B}G)
    \\
    & =
    \left(
       \cdots
       \tilde D(2,dim(G))
       \stackrel{\to}{\stackrel{\to}{\to}}
     \tilde D(1,dim(G))\stackrel{\to}{\to} *
    \right)
  \end{aligned}  
  \,. 
$$

+-- {: .un_prop}
###### Proposition

The normalized cochain complex of the cosimplicial alghebra of functions on thi $b \mathfrak{g}$ is isomorphic to the ordinary [[Chevalley-Eilenberg algebra]] $(\wedge^\bullet \mathfrak{g}^*, [-,-]^*)$ of $\mathfrak{g}$.

=--

+-- {: .proof}
###### Proof

By the discussion at [Spaces of infinitesimal k-simplices](http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl) we have that for $C^\infty(\tilde D(k,dim(G)))_{top} \subset C^\infty(\tilde D(k,n))$ the subspace of those functions that are in the joint kernel of the co-degeneracy maps is naturally isomorpic to $\wedge^k (\mathbb{R}^{dim(G)})^*$, so that we have a natural isomorphism of vector spaces

$$
  N C^\infty(b \mathfrak{g})_k \simeq \wedge^k \mathfrak{g}^*
  \,.
$$

By the fact that everything is [[simplicial skeleton|2-coskeletal]] it suffices to check that the differential in first degree

$$
  N C^\infty(\tilde D(1,dim(G)))
  \stackrel{p_1^* + p_2^* - (\cdot)^*}{\to}
  N C^\infty(\tilde D(2,dim(G)))
$$

is indeed the dual of the Lie bracket. But the product $\cdot_G : G \times G \to G$ restricted along $\tilde D(2,dim(G)) \hookrightarrow G \times G$ to the [[infinitesimal space]] $\tilde D(2, dim(G))$ linearizes in each of its arguments: for $(\vec x,\vec y)$ \in \tilde D(2,dim(G))$ we have

$$
  \vec x \cdot_G \vec y = 
  \vec x \cdot \nabla_x \cdot_G (0,0)
  + 
  \vec y \cdot \nabla_y \cdot_G (0,0)
  +
  \vec x \cdot \nabla_x 
  \vec y \cdot \nabla_y \cdot_G(0,0)
  \,.
$$

Since thr origin here corresponds to the neutral element of $G$ and since with one of its arguments the neutral element the operaton $\cdot_G$ is the identity, and since the double derivative produces the Lie bracket (keeping in mind that $x^i y^j  + x^j y^i = 0$ in $\tilde D(2,dim(G))$), this is

$$
  \cdots = \vec x + \vec y + [\vec x, \vec y]
  \,.
$$

Accordingly the alternating sum of co-face maps is

$$
  \begin{aligned}
     d &= p_1^* + p_2^* - \cdot_G^* 
     \\ & = p_1^* + p_2^* - ( p_1^* + p_2^* + [-,-]^*)
     \\ & = - [-,-]^*
  \end{aligned}
$$

as it should be for the Chevalley-Eilenberg algebra of a Lie algebra.

=--

The infinitesimal reasoning involved in this proof is discussed in section 6.8 of 

* [[Anders Kock]], _Synthetic geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))


### Tangent Lie algebroid of a Lie algebra {#TangentOfLieAlgebra}


We can form the tangent $\infty$-Lie algebroid of any $\infty$-Lie algebroid $\mathfrak{a}$ as

$$
  T \mathfrak{a}
  = 
  \int^{[n] \in \Delta} \Delta[n] \cdot T \mathfrak{a}_n
  =
  \int^{[n] \in \Delta} \Delta[n] \cdot (\mathfrak{a}_n)^{(\Delta^\bullet_{inf})}
  \,.
$$

We want to claim now that for $\mathfrak{g}$ a Lie algebra, we have a canonical isomorphism

$$
  CE(T b \mathfrak{g}) \simeq W(\mathfrak{g})
$$

that identifies the [[Chevalley-Eilenberg algebra]] of the tangent Lie algebra of $b \mathbf{g}$ with the [[Weil algebra]] of $\mathfrak{g}$.


The key observation for this is that in the [[bisimplicial set|bisimplicial object]]

$$
  \array{
    && \vdots && \vdots && \vdots
    \\
    &\cdots&
    \tilde D(3,dim(G))^{(\Delta^2_{inf})} && 
    \tilde D(3,dim(G))^{(\Delta^1_{inf})} && 
    \tilde D(3,dim(G))
    \\
    &&\downarrow \downarrow \downarrow  
    && \downarrow \downarrow \downarrow 
    && \downarrow \downarrow \downarrow
    \\
    &\cdots&
    \tilde D(1,dim(G))^{(\Delta^2_{inf})} && 
    \tilde D(1,dim(G))^{(\Delta^1_{inf})} && 
    \tilde D(1,dim(G))
    \\
    && \downarrow \downarrow  
    && \downarrow \downarrow && \downarrow \downarrow
    \\
     &\cdots& * &\stackrel{\to}{\stackrel{\to}{\to}}&  * 
    &\stackrel{\to}{\to}& *
  }
$$

* the functions on infinitesimal simplices in an infinitesimal space that vanish on degenerate simplices are already isomorphic to covectors at the origin;

* the functions on infinitesimal $r$-simplices in a $\tilde D(k,dim(G))$ for $r \gt k$ which vanish on degenerate simplices already vanish entirely.

Using this the total complex of $N C^\infty(-)$ of this bisimplicial set is manifestly isomorphic to the Weil algebra.


...

## In a cohesive $(\infty,1)$-topos {#InCohesiveContext}

We now give the above considerations a precise context by interpreting them in a [[cohesive (∞,1)-topos]].

### Definition

Let $\mathbf{H} = (\infty,1)Sh(ThCartSp)$ be $(\infty,1)$-[[Cahiers topos]], the [[(∞,1)-sheaf (∞,1)-topos]] on [[ThCartSp]]. 

This is a [[cohesive (∞,1)-topos]].


In the [[model structure on simplicial presheaves|model by simplicial presheaves]] $[ThCartSp^{op}, sSet]_{proj,loc}$ say an $\infty$-Lie algebra is an object of the form

$$
  \mathbf{B} \mathfrak{g}
  =
  \int^{[k]\in \Delta} \mathbf{\Delta}[k] \cdot \mathfrak{g}_k
  \,,
$$

where 

* $\mathbf{\Delta} : \Delta \to sSet$ is the [[fat simplex]];

* $\mathfrak{g} : \Delta^{op} \to ThCartSp \hookrightarrow [ThCartSp^{op}, sSet]$ is degreewise representable by an [[infinitesimal space]] with the point in degree 0.


### Properties


+-- {: .un_lemma }
###### Lemma


The object $\mathbf{B}\mathfrak{g} \in [ThCartSp^{op}, sSet]_{proj,loc}$ is cofibrant.

=--

+-- {: .proof}
###### Proof

The [[coend]] over the [[tensoring]] 

$$
  \int^{[k] \in \Delta}
  (-)\cdot (-)
  : 
  [\Delta, sSet_{Quillen}]_{proj} \times
  [\Delta^{op}, (T Alg^\Delta_{proj})^{op}]_{inj}
  \to 
  (T Alg^\Delta_{proj})^{op}
$$

for the projective and injective [[global model structure on functors]] on the [[simplex category]] and its opposite is a [[Quillen bifunctor]] (as discussed there). We have moreover

1. The [[fat simplex]] is cofibrant in $[\Delta, sSet_{Quillen}]_{proj}$. 

1. Because every representable $ThCartSp \hookrightarrow [ThCartSp^{op}, sSet]_{proj}$ is cofibrant the object $\mathfrak{g}_\bullet \in [\Delta^{op}, [ThCartSp^{op}, sSet]_{proj}]_{inj}$ is cofibrant.

Therefore also $\mathbf{B}\mathfrak{g}$ is cofibrant.

=--


+-- {: .un_lemma }
###### Lemma

The image of $\mathbf{B}\mathfrak{g}$ under the [[(∞,1)-functor]] $\mathcal{O} : \mathbf{H} \to \mathbf{L}$ described at [[function algebras on ∞-stacks]] is weakly equivalent to the object modeled by $\int^{[k] \in \Delta} \Delta[k] \cdot \mathfrak{g}_k$ (meaning: with the ordinary instead of the fat simplex).

=--


+-- {: .proof}
###### Proof

As described at [[function algebras on ∞-stacks]] the $(\infty,1)$-functor $\mathcal{O}$ is modeled by a [[Quillen adjunction]]

$$
  (T Alg^\Delta_{proj})^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\to}
  [ThCartSp^{op}, sSet]_{proj}
  \,,
$$

where $T = $ [[CartSp]] is the [[Lawvere theory]] of [[smooth algebra]]s.

We use now the [[Reedy model structure]]s over the [[simplex category]]: 

In $[\Delta^{op}, (T Alg^{\Delta}_{proj})^{op}]_{Reedy}$ we have that $[k] \mapsto \mathfrak{g}_k$ is cofibrant, because the inclusion of the degenerate $k$-cells into all $k$-cells is dually a surjection of algebras, hence dually a fibration. 

The [[coend]] over the [[tensoring]] 

$$
  \int^{[k] \in \Delta}
  (-)\cdot (-)
  : 
  [\Delta, sSet_{Quillen}]_{Reedy} \times
  [\Delta^{op}, (T Alg^\Delta_{proj})^{op}]_{Reedy}
  \to 
  (T Alg^\Delta_{proj})^{op}
$$

is a [[Quillen bifunctor]] (as discussed there).

Since both the simplex $\Delta$ as well as the [[fat simplex]] $\mathbf{\Delta}$ [[Reedy model structure|are Reedy cofibrant]] and the map $\mathbf{\Delta} \to \Delta$ a weak equivalence, it follows (by the [[factorization lemma]]) that 

$$
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot \mathfrak{g}_k
    \stackrel{\simeq}{\to} 
  \int^{[k] \in \Delta} \Delta[k] \cdot \mathfrak{g}_k
$$

is a weak equivalence in $(T Alg^\Delta_{proj})^{op}$.

=--



+-- {: .un_corollary }
###### Corollary

The image of $\mathbf{B}\mathfrak{g}$ under the [[(∞,1)-functor]] $\Pi : \mathbf{H} \to \infty Grpd$ descrived ar [[locally ∞-connected (∞,1)-topos]] is [[contractible]]

$$
  \Pi \mathbf{B}\mathfrak{g} \simeq *
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since by the above lemma $\mathbf{B}\mathfrak{g}$ is cofibrant, the $(\infty,1)$-functor $\Pi$ acts degreewise by replacinf the representable presheaf by the point (see [[schreiber:path ∞-groupoid]])

$$
  \Pi : 
  \mathbf{B}\mathfrak{g}
  =
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot \mathfrak{g}_{k} 
  \mapsto 
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot *
  \,.
$$ 

That this is equivalent to the point follows from the fact that $\emptyset \to \mathbf{\Delta}$ is an acylic cofibration in $[\Delta, sSet_{Quillen}]_{proj}$, and that

$$
  \int^{[k] \in \Delta}
  (-)\times (-)
  : 
  [\Delta, sSet_{Quillen}]_{proj}
  \times
  [\Delta^{op}, sSet_{Qillen}]_{inj}
  \to 
  sSet_{Quillen}
$$

is a [[Quillen bifunctor]], using that $* \in [\Delta^{op}, sSet_{Quillen}]_{inj}$ is cofibrant.


=--

+-- {: .un_corollary }
###### Corollary

The image of $\mathbf{B}\mathfrak{g}$ under the [[global section]] [[(∞,1)-functor]] $\Gamma : \mathbf{H} \to \infty Grpd$ is [[contractible]]

$$
  \Gamma \mathbf{B}\mathfrak{g} \simeq *
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since [[ThCartSp]] is an [[(∞,1)-cohesive site]] and using the main theorem there, we have that $\Gamma$ is modeled by the functor that evaluates on the point, and that this is a left Quillen functor

$$
  Hom(*,-) : [ThCartSp^{op}, sSet]_{proj,loc} \to sSet_{Quillen}
  \,.
$$

Therefore $\Gamma \mathbf{B}\mathfrak{g}$ is modeled by degreewise evaluating $\mathfrak{g}_k$ on the point. But since this is by assumption an [[infinitesimal space]] it has only a single point, so that

$$
  \Gamma \mathbf{B}\mathfrak{g}_k  = \int^{[k] \in \Delta} \mathbf{\Delta}[k]
  \,.
$$

As in the previous corollary, this is equivalent to the point.

=--

+-- {: .un_corollary }
###### Corollary

The canonical morphism

$$
  \Gamma \mathbf{B}\mathfrak{g} \to \Pi \mathbf{B}\mathfrak{g}
$$


is an [[equivalence in a quasi-category|equivalence]] in [[∞Grpd]].

=--

By the discussion at [[cohesive (∞,1)-topos]] this characterizes $\mathbf{B}\mathfrak{g}$ intrinsically as an infinitesmal object.

## Related concepts


* [[∞-Lie algebroid valued differential forms]]

* [[∞-Chern-Weil theory]]

## References

The term "Lie $\infty$-algebroid" or "$L_\infty$-algebroid" as such is not as yet established in the literature, as most authors working with these objects think of them entirely in terms of [[dg-algebra]]s or [[NQ-supermanifolds]] and either ignore the relation to [[Lie theory]] or take it more or less for granted. 

Possibly the first explicit appearance of the idea of $\infty$-Lie algebroids recognized in their full [[Lie theory|Lie theoretic]] meaning is

* [[Pavol ?evera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080))

which uses "[[NQ-supermanifolds]]". Of course, as this article also points out, in hindsight one finds that much of this is already implicit in the much older theory of [[Sullivan model|Sullivan models]] in [[rational homotopy theory]], which is concerned with modelling _[[topological space]]s_ by [[dg-algebras]]. That these spaces can be regarded as [[∞-groupoids]] and as [[∞-Lie groupoids]] in particular is clear in hindsight, but was possibly first explicitly realized in the above reference. See also [[Lie integration]], [[rational homotopy theory in an (∞,1)-topos]] and [[function algebras on ∞-stacks]].

The explicit term _$\infty$-Lie algebroid_ / _$L_\infty$-algebroid_ as such appears in 

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Twisted differential string- and  fivebrane structures_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">ref</a>)

The term also appears in

* Andrew James Bruce, _From $L_{\infty}$-algebroids to higher Schouten/Poisson structures_ ([arXiv:1007.1389](http://arxiv4.library.cornell.edu/abs/1007.1389))

[[!redirects L-infinity-algebroid]]
[[!redirects L-infinity algebroid]]
[[!redirects L-infinity Lie algebroid]]

[[!redirects L-∞-algebroid]]
[[!redirects L-∞ algebroid]]
[[!redirects L-∞ Lie algebroid]]


[[!redirects Lie-∞-algebroid]]
[[!redirects Lie-∞-algebroids]]
[[!redirects Lie-∞ algebroid]]
[[!redirects Lie-∞ algebroids]]
[[!redirects Lie ∞-algebroid]]
[[!redirects Lie ∞-algebroids]]
[[!redirects L-infinity-algebroids]]
[[!redirects L-infinity algebroids]]
[[!redirects L-infinity Lie algebroids]]

[[!redirects ∞-Lie algebroid]]
[[!redirects ∞-Lie algebroids]]

[[!redirects infinity-Lie algebroid]]
[[!redirects infinity-Lie algebroids]]