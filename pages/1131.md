

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Idea

A _differential graded Lie algebra_, or _dg-Lie algebra_ for short, is equivalently 

* a graded [[Lie algebra]] equipped with a [[differential]] that acts as a graded [[derivation]] with respect to the Lie bracket;

* a [[Lie algebra]] [[internalization|internal to]] the [[category of chain complexes]]; 

* a _strict_ [[L-∞-algebra]], i.e. an $L_\infty$-algebra in which only the unary and the binary brackets may be nontrivial.


## Definition


### Direct explicit definition
 {#DirectExplicitDefinition}


+-- {: .num_defn }
###### Definition

A _dg-Lie algebra_ $(\mathfrak{g},\partial,[-,-])$ is

1. a $\mathbb{Z}$-[[graded vector space]] $\mathfrak{g} = \bigoplus_{i} \mathfrak{g}_i$;

1. a [[linear map]] $\partial \colon \mathfrak{g} \longrightarrow \mathfrak{g}$;

1. a [[bilinear map]] $[-,-] \colon \mathfrak{g}\otimes\mathfrak{g} \longrightarrow \mathfrak{g}$, the _bracket_;

such that (all conditions are expressed for homogeneously graded elements $x_i \in \mathfrak{g}_{\vert x_i \vert}$):

1. $\partial$ is a [[differential]] that makes $(\mathfrak{g},\partial)$ into a [[chain complex]], i.e.

   1. it is of degree -1, $\partial \colon \mathfrak{g}_{i} \to \mathfrak{g}_{i-1}$;

   1. it squares to zero, $\partial \circ \partial = 0$;

1. $\partial$ is a graded [[derivation]] of the bilinear pairing, i.e. 

   $$ 
      \partial [x_1,x_2] = [\partial x_1, x_2] + (-1)^{\vert x_1 \vert} [x_1, \partial x_2]
    \,,

   $$

1. the bilinear pairing is graded skew-symmetric, i.e.

   $$
     [x_1, x_2] = -(-1)^{\vert x_1\vert \vert x_2 \vert} [x_2,x_1]
     \,,
   $$

1. the bilinear pairing satisfies the graded [[Jacobi identity]] (saying that $[x,-]$ is a graded [[derivation]])

   $$
     [x_1,[x_2,x_3]] = [[x_1,x_2], x_3] + (-1)^{\vert x_1 \vert \vert x_2 \vert} [x_2, [x_1, x_3]]
    \,.
   $$

=--

### As graded Lie algebras with nilpotent derivations
 {#AsGradedLieAlgebrasWithDerivations}

+-- {: .num_defn}
###### Definition

A _pre-graded Lie algebra_ (pre-gla) is a [[graded vector space|pre-gvs]], $L$, together with a bilinear map of degree zero

$$[\quad,\quad ] : L\otimes L \to L,$$

such that

$$[x,y] = (-1)^{|x||y|+1}[y,x]$$

and 

$$(-1)^{|x||z|}[x,[y,z]] +(-1)^{|y||x|}[y,[z,x]] +(-1)^{|z||y|}[z,[x,y]] = 0$$

for every triple $(x,y,z)$ of homogeneous elements in $L$.

=--

(The first property is call _antisymmetry_, the second _the Jacobi identity_.)

A _morphism_ $f: L \to L'$ of pre-glas is a linear map of degree zero, that is compatible with the brackets,

$$f[x,y] = [f(x),f(y)].$$

+-- {: .num_example }
###### Example

To any augmented pre-ga $A$, one can associate a pre-gla, denoted $\bar{A}_L$, with underlying gvs $\bar{A}$ and with bracket, the commutator, $[x,y] = xy -(-1)^{|x||y|}yx$ for each pair $(x,y)$ of homogeneous elements.  $\bar{A}_L$ is abelian (i.e. with trivial bracket) if and only if $A$ is graded commutative.

=--



+-- {: .num_example }
###### Example

If $A$ is a pre-cga and $L$ is a pre-gla, the tensor product $A\otimes L$ has a pre-gla structure with bracket

$$[a\otimes l,a'\otimes l'] = (-1)^{|a'||l|}aa' \otimes [l,l']$$

for $a,a', l, l'$ homogeneous.

=--


+-- {: .num_defn }
###### Definition

Let $L$ be a pre-gla.  A _[[derivation]]_ of gla-s, of degree $p\in \mathbb{Z}$, is a linear mapping $\theta \in Hom_p(L,L)$ such that

$$\theta[x,y] = [\theta{x},y] + (-1)^{p|x|}[x,\theta(y)]$$

for any pair $x,y$ of homogeneous elements of $L$.  We denote by $Der_p(L)$, the vector space of degree $p$ derivations of the gla, $L$.

=--

+-- {: .num_defn }
###### Definition


A differential $\partial$ of a pre-gla is a Lie algebra derivation of degree -1 such that $\partial\circ \partial = 0$.  The pair $(L,\partial)$ is then called a _differential pre-graded Lie algebra_ (pre-dgla); its homology $H(L,\partial)$, is a pre-gla.  

A morphism of pre-dglas is a morphism for both the underlying pre-gla and the pre-dgvs. We denote the corresponding category  by $pre DGLA$.

=--

This means that a  differential graded Lie algebra is an internal Lie algebra in the symmetric monoidal category of chain complexes with tensor product given as in [[differential graded vector space|differential graded vector spaces]]. 


+-- {: .num_example }
###### Example

If $(A,\partial)$ is an augmented pre-dga, $(\bar{A}_L,\partial)$ is a pre-dgla.

=--

+-- {: .num_example }
###### Example

If $(A,\partial)$ is a pre-cdga and $(L,\partial')$, a pre-dgla, $A \otimes L$, together with the tensor product differential, is a pre-dgla.

=--

+-- {: .num_example }
###### Example

Let $(V,\partial)$ be a pre-dgvs, then the pre-dgvs, $(Hom(V,V),D)$, constructed earlier is a pre-dga  for the multiplication law given by composition of mappings.  Its associated pre-dgla has

$$[f,g] = f\circ g - (-1)^{|f||g|}g\circ f$$

and 

$$Df = [\partial,f].$$

In particular, if $(V,\partial) = (A,d)$ is a cdga (resp. $(V,\partial) = (L,\partial)$ is dgla), then $Der(A,d) = (\bigoplus_p Der_p(A),D)$, (resp. $Der(L,\partial) = (Der_p(L),D)$) is a sub-pre-dgl of $(Hom(V,V),D)$.

=--

+-- {: .num_defn }
###### Definition

A dgla is a pre-dgla with a lower grading; explicitly:


A **differential graded Lie algebra**, $(L,\partial)$, is a graded vector space $L = \bigoplus_{p\geq 0}L_p$, together with a bilinear map of degree 0
$$[\quad ,\quad] : L\otimes L \to L,$$
and a differential $\partial$ satisfying 
$$\partial L_p \subseteq L_{p-1},  \quad [x,y] = (-1)^{|x||y|+1}[y,x],$$
$$(-1)^{|x||z|}[x,[y,z]] +(-1)^{|y||x|}[y,[z,x]] +(-1)^{|z||y|}[z,[x,y]] = 0$$
and
$$\partial[x,y] = [\partial x,y] + (-1)^{|x|}[x,\partial y]$$
for every triple $(x,y,z)$ of homogeneous elements in $L$.

=--

Let $DGLA$ be the corresponding category.

+-- {: .num_defn }
###### Definition

A dgla is $n$-*reduced* (resp. _homologically $n$-reduced_) if $L_p = 0$ (resp. $H_p(L,\partial) = 0$) for all $p\lt n$.  Denote by $DGLA_n$ (resp.  $DGLA_{hn}$), the corresponding categories.

=--

+-- {: .num_defn }
###### Definition


If $(L,\partial)$ is a pre-dgla, a _gla-filtration_ of $L$ (resp. a _dgla-filtration_ of $( L,\partial)$ ) is a family of subgraded vector spaces $F_p L$, $p\in \mathbb{Z}$, such that $F_p L\subseteq F_{p+1}L$, $[F_p L,F_n L]\subseteq F_{p+n} L$, (resp. and $\partial F_p L\subseteq F_p L$).

=--

+-- {: .num_defn }
###### Definition


Let $L$ be a pre-gla.  Its _bracket length filtration_ is obtained from the descending central series:

$$F^1 L = L; \quad F^p L = [L,F^{p-1} L] \quad  if \quad p\geq 2.$$

It is a gla-filtration.

$Q(L) = L/F^2L$ is called the _space of indecomposables_ of $L$.

If $(L,\partial)$ is a pre-dgla, $F^p L$ is stable by $\partial$.  Letting $Q(\partial)$ be the induced differential on $Q(L)$, $Q$ then defines a functor
$$Q : pre DGLA \to pre DGVS.$$

=--


+-- {: .num_example }
###### Example
**Free Lie algebra, $\mathbb{L}(V)$**

Let $V$ be a pre-gvs, $T(V)$, the tensor algebra on $V$ with augmentation ideal $\overline{T(V)}$ (recall $T(V) = \bigoplus_{n\geq 0} V^{\otimes n}$ and the augmentation sends $V (= V^{\otimes 1}$ to 0). 

 Let $\overline{T(V)}_L$ be $\overline{T(V)}$ with the pre-gla structure given by the commutators.  We denote by $\mathbb{L}(V)$, the Lie subalgebra of $\overline{T(V)}_L$ generated by $V$. 
+--{:query}
[[Tim Porter|Tim]]: A more explicit description may help here, cf. Quillen, Rational Homotopy theory (p.281) or MacLane, Homology.
=--
If $L$ is a pre-gla, any morphism of pre-gvs $f: V\to L$ has a unique extension to a pre-gla morphism $\hat{f} :\mathbb{L}(V)\to L$.  If $(e_\alpha)_{\alpha\in I}$ is a homogeneous basis for $V$, $\mathbb{L}(V)$ may be denoted $\mathbb{L}((e_\alpha)_{\alpha\in I})$.

On the free Lie algebra $\mathbb{L}(V)$, the bracket length filtration comes from a gradation $\mathbb{L}(V) = \bigoplus_j\mathbb{L}^j(V) $, where $\mathbb{L}^j(V) $ is the subspace generated by the brackets of elements of $V$ of length $j$.  The inclusion $\mathbb{L}(V)\hookrightarrow T(V)$ identifies $\mathbb{L}^j(V)$ with $\mathbb{L}(V)\cap T^j(V)$.

If $\mathbb{L}(V), \partial)$ is a dgla, free as a gla, with $V$ fixed, $\partial$ is the sum of derivations $\partial_k$ defined by : $\partial_k \subset \mathbb{L}^k(V)$.  The isomorphism between $V$ and $Q\mathbb{L}(V)$ identifies $\partial_1V$ with $Q(\partial)$.  $\partial_1$ (resp. $\partial_2$) is called the _linear part_ (resp, the _quadratic part_) of $\partial$.

=--


+-- {: .num_defn }
###### Definition

Let $(L,\partial)$ and $(L',\partial')$ be two dglas.  Their _product_ $(L,\partial)\times(L',\partial')$ in $DGLA$ is defined by:

*  the underlying vector space is the direct sum $L\oplus L'$;

*  $(L,\partial)$ and $(L',\partial')$ are two sub differential graded Lie algebras of $(L,\partial)\times(L',\partial')$;

*  if $x\in L$ and $x' \in L'$, then $[x,x'] = 0$.

=--

Their _coproduct_ or _sum_ $(L,\partial)\star(L',\partial')$ is often called their _free product_. 

+-- {: .num_example }
###### Example

$$\mathbb{L}(V)\star \mathbb{L}(V') \cong   \mathbb{L}(V\oplus V').$$

More generally if $L$ and $L'$ are given by generators and relations

$$L = \mathbb{L}(V)/I , \quad L' = \mathbb{L}(V')/I' ,$$

$$L\star L' = \mathbb{L}(V\oplus V')/{I,I'}.$$

The differential on $L\star L'$ is the unique Lie algebra derivation extending $\partial$ and $\partial'$.

=--

## Properties

### Model category structure

* [[model structure on dg-Lie algebras]]


### Relation to $L_\infty$-algebras
 {#RelationToLInfinityAlgebras}

Every dg-Lie algebra is in an evident way an 
[[L-infinity algebra]]. Dg-Lie algebras are precisely those $L_\infty$-algebras for which all $n$-ary brackets for $n \gt 2$ are trivial. These may be thought of as the _strict_ $L_\infty$-algebras: those for which the [[Jacobi identity]] holds on the nose and all its possible higher coherences are trivial.

+-- {: .num_theorem}
###### Theorem

Let $k$ be a [[field]] of [[characteristic]] 0 and write $L_\infty Alg_k$ for the [[category]] of [[L-infinity algebras]] over $k$. 

Then every object of $L_\infty Alg_k$ is [[quasi-isomorphism|quasi-isomorphic]] to a [[dg-Lie algebra]].

Moreover, one can find a functorial replacement: there is a [[functor]]

$$
  W : L_\infty Alg_k \to L_\infty Alg_k
$$

such that for each $\mathfrak{g} \in L_\infty Alg_k$ 

1. $W(\mathfrak{k})$ is a [[dg-Lie algebra]];

1. there is a [[quasi-isomorphism]]

   $$
     \mathfrak{g} \stackrel{\simeq}{\to}
     W(\mathfrak{g})
     \,.
   $$

=--

This appears for instance as ([KrizMay, cor. 1.6](#KrizMay)).

For more see at 

* _[[model structure on dg-Lie algebras]]_ the section _[Relation to L-infinity algebras](model+structure+on+dg-Lie+algebras#RectificationResolution)_.

* [[model structure for L-infinity algebras]], the section _[on dg-Lie algebras](model+structure+for+L-infinity+algebras#OndgLieAlgebras)_.

* [[relation between L-∞ algebras and dg-Lie algebras]]

### Relation to dg-coAlgebras

Via the above relation to $L_\infty$-algebras, dg-Lie algebras are also connected by adjunction to [[dg-coalgebras]]

$$
  dgLieAlg_k
   \underoverset
     {\underset{CE}{\longrightarrow}}
     {\overset{\mathcal{L}}{\longleftarrow}}
     {\bot}
  dgCoAlg_k
$$

Here 

* $CE$ is the [[Chevalley-Eilenberg algebra]] functor. It sends a dg-Lie algebra $(\mathfrak{g}, \partial, [-,-])$ to 

  $$
    CE(\mathfrak{g},\partial,[-,-])
     \;\coloneqq\;
    \left(
      \vee^\bullet \mathfrak{g}[1]  
      ,\;
      D = \partial + [-,-]
    \right)
    \,,
  $$

  where on the right the extension of $\partial$ and $[-,-]$ to graded derivations is understood.

* For $(X,D)$ a dg-coalgebra, then

  $$
    \mathcal{L}(X,D)
     \coloneqq
    \left(
       F(\overline{X}[-1]),\; 
       \partial \coloneqq D + (\Delta - 1 \otimes id - id \otimes 1)
    \right)
  $$

  where
  
  1. $\overline{X} \coloneqq ker(\epsilon)$ is the [[kernel]] of the [[counit]], regarded as a [[chain complex]];

  1. $F$ is the [[free Lie algebra]] functor (as graded Lie algebras);

  1. on the right we are extending $(\Delta - 1 \otimes id - id \otimes 1) \colon \overline{X} \to \overline{X} \otimes \overline{X}$ as a Lie algebra [[derivation]] 

Moreover

$$
  Hom(\mathcal{L}(X), \mathfrak{g})
   \simeq
  Hom(X, CE(\mathfrak{g}))
    \simeq
  MC(Hom(\overline{X},\mathfrak{g}))
$$

is the [[Maurer-Cartan elements]] in the Hom-dgLie algebra from $\overline{X}$ to $\mathfrak{g}$.

For dg-Lie algebras concentrated in degrees $ \geq n \geq 1$ this is due to ([Quillen 69, appendix B, prop 6.1, 6.2](#Quillen)). For unbounded dg-algebras, this is due to ([Hinich 98, 2.2](#Hinich98)).

For more see at _[[model structure on dg-Lie algebras]]_.


### Relation to simplicial Lie algebras

+-- {: .num_theorem}
###### Theorem

There is an [[adjunction]]

$$
  (N^* \dashv N) : LieAlg^\Delta \stackrel{\overset{N^*}{\leftarrow}}{\underset{N}{\to}}
  dgLieAlg
$$

between [[simplicial Lie algebras]] and [[dg-Lie algebra]]s, where $N$ acts on the underlying simplicial vector spaces as the [[Moore complex]] functor.

=--

This is ([Quillen, prop. 4.4](#Quillen)). For more see at _[[simplicial Lie algebra]]_.

+-- {: .num_theorem}
###### Theorem

This adjunction is a [[Quillen adjunction]] with respect to the projective [[model structure on dg-Lie algebras]] and the projective [[model structure on simplicial Lie algebras]] ([this prop.](model+structure+on+simplicial+Lie+algebras#QuillenAdjunctionTodgLieAlgebras)).

The corresponding [[derived functors]] constitute an [[equivalence of categories]] between the corresponding [[homotopy categories]]

$$
  (L N^* \dashv \tilde N) 
   : 
  Ho(LieAlg^\Delta)_1 
   \stackrel{\overset{L N^*}{\leftarrow}}{\underset{\tilde N}{\to}} Ho(dgLieAlg)_1
$$

of [[1-connected]] objects on both sides.

=--

This is in the proof of ([Quillen, theorem. 4.4](#Quillen)).




## Related concepts

* [[crossed complex]] $\Leftarrow$ [[crossed module]] $\Rightarrow$ [[2-crossed module]]

* **dg-Lie algebra** $\Leftarrow$ [[differential crossed module]] $\Rightarrow$ [[differential 2-crossed module]]

* [[L-∞ algebra]]

  * [[model structure for L-∞ algebras]]

  * [[sheaf of L-∞ algebras]]

* [[formal moduli problem]], [[deformation theory]]

## References

A standard reference in the context of [[rational homotopy theory]] is

* {#Quillen} [[Dan Quillen]], _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([JSTOR](http://www.jstor.org/stable/1970725))

For the unbounded case there is general discussion in

* {#Hinich97} [[Vladimir Hinich]], _Homological algebra of homotopy algebras_, Comm. in algebra, 25(10)(1997), 3291&#8211;3323 ([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453))) 

The relation to $L_\infty$-algebras is discussed for instance in 

* {#KrizMay} [[Igor Kriz]], [[Peter May]], _Operads, algebras, modules and motives_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/kmbooklatex.pdf))
 


See also the references at [[model structure on dg-Lie algebras]].

A discussion of how formal neighbourhoods of points in [[infinity-stack]]s are governed by dg-Lie algebras:

* [[Jacob Lurie]], _[[Moduli Problems and DG-Lie Algebras]]_

[[!redirects differential graded Lie algebras]]
[[!redirects dg-Lie algebra]]
[[!redirects Lie dg-algebra]]
[[!redirects dg-Lie algebras]]
[[!redirects Lie dg-algebras]]