
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

## Idea ##

_$L_\infty$-algebras_ (or _strong homotopy Lie algebras_) are a higher generalization (a "[[vertical categorification]]") of [[Lie algebras]]: in an $L_\infty$-algebra the [[Jacobi identity]] is allowed to hold (only) up to higher [[coherence law|coherent]] [[homotopy]]. 

An $L_\infty$-algebra that is concentrated in lowest degree is an ordinary [[Lie algebra]]. If it is concentrated in the lowest two degrees is is a [[Lie 2-algebra]], etc.

From another perspective: an $L_\infty$-algebra is a [[Lie ∞-algebroid]] with a single object.

$L_\infty$-algebras are [[infinitesimal space|infinitesimal]] approximations of [[smooth ∞-group]]s in analogy to how an ordinary Lie algebra is an infinitesimal approximation of a [[Lie group]]. Under [[Lie integration]] every $L_\infty$-algebra $\mathfrak{g}$ "exponentiates" to a [[smooth ∞-group]] $\Omega \exp(\mathfrak{g})$.

## History
 {#History}

+-- {: .num_remark #SuperLInfintiyAsFDA}
###### Remark
**(history of the concept of (super-)$L_\infty$ algebras)**

The identification of the concept of (super-)$L_\infty$-algebras has a non-linear history:

[[L-∞ algebras]] in the incarnation of higher brackets satisfying a higher Jacobi identity (def. \ref{LInfinityDefinitionViaGeneralizedJacobiIdentity}) were introduced in [Stasheff 92](#Stasheff92), [Lada-Stasheff 92](#LadaStasheff92), based on the 
example of such a structure on the [[BRST complex]] of the [[bosonic string]] that  was reported in the construction of [[closed string field theory]] in [Zwiebach 92](#Zwiebach92). 

[Lada-Stasheff 92](#LadaStasheff92) credit [Schlessinger-Stasheff 85](deformation+theory#SchlessingerStasheff85) with the introduction of the concept, but while that article considers many closely related structures, it does not consider $L_\infty$-algebras as such. [Lada-Markl 94](#LadaMarkl94) credit other work by Schlessinger-Stasheff as the origin, but that work appeared much later as [Schlessinger-Stasheff 12](deformation+theory#SchlessingerStasheff12).

According to [Stasheff 16, slide 25](#Stasheff16), Zwiebach had this structure already in 1989, when Stasheff recognized it in a talk by Zwiebach at a [[GUT]] conference in Chapel-Hill.   Zwiebach in turn had been following the [[BV-formalism]] of [Batalin-Vilkovisky 83](#BatalinVilkovisky83), [Batakin-Fradkin 83](#BatakinFradkin83), whose relation to $L_\infty$-algebras was later amplified in [Stasheff 96](#Stasheff96), [Stasheff 97](#Stasheff97).

The observation that these systems of higher brackets are fully characterized by their Chevalley-Eilenberg dg-(co-)algebras
is due to [Lada-Markl 94](#LadaMarkl94).
See [Sati-Schreiber-Stasheff 08, around def. 13](#SatiSchreiberStasheff08).

But in this dual incarnation, [[L-∞ algebras]] and more generally [[super L-∞ algebras]] (of [[finite type]]) 
had secretly been introduced, independently of the [[BV-formalism]] of [Batalin-Vilkovisky 83](#BatalinVilkovisky83), [Batakin-Fradkin 83](#BatakinFradkin83),  within the [[supergravity]] literature already in [D'Auria-Fr&#233;-Regge 80](#DAuriaFreRegge80) and explicitly in [van Nieuwenhuizen 82](#Nieuwenhuizen82).
The concept was picked up in the [[D'Auria-Fré formulation of supergravity]] ([D'Auria-Fr&#233; 82](#DAuriaFre82)) and eventually came to be referred to as "FDA"s (short for "free differential algebra") in the [[supergravity]] literature (but beware that these dg-algebras 
are in general [[free construction|free]] only as graded-[[supercommutative superalgebras]], not as differential algebras)
The relation between super $L_\infty$-algebras and the "FDA"s of the [[supergravity]] literature is made explicit in ([FSS 13](#FSS13)).

| [[nLab:higher Lie theory]] | [[nLab:supergravity]] |
|----------------------------|-----------------------|
| $\,$ [[nLab:super Lie n-algebra]] $\mathfrak{g}$ $\,$ | $\,$ "FDA" $CE(\mathfrak{g})$ $\,$ |

The construction in [van Nieuwenhuizen 82](#Nieuwenhuizen82) in turn was motivated by the [[Sullivan algebras]]
in [[rational homotopy theory]] ([Sullivan 77](#rational+homotopy+theory#Sullivan77)). Indeed, their
dual incarnations in rational homotopy theory are [[dg-Lie algebras]] ([Quillen 69](#rational+homotopy+theory#Quillen69)),
hence a special case of $L_\infty$-algebras.

This close relation between [[rational homotopy theory]] and [[higher Lie theory]] might have remained less of a
secret had it not been for the focus of [[Sullivan minimal models]] on the non-[[simply connected topological space|simply connected]]
case, which excludes the ordinary [[Lie algebras]] from the picture. But the Quillen model of
[[rational homotopy theory]] effectively says that for $X$ a [[rational topological space]] then its [[loop space]]
[[∞-group]] $\Omega X$ is reflected, infinitesimally, by an [[L-∞ algebra]]. This perspective began to 
receive more attention when the [[Sullivan construction]] in [[rational homotopy theory]] was
concretely identified as higher [[Lie integration]] in [Henriques 08](#Lie+integration#Henriques).
A modern review that makes this [[L-∞ algebra]]-theoretic nature of [[rational homotopy theory]] manifest is in 
[Buijs-F&#233;lix-Murillo 12, section 2](BuijsFelixMurillo12).

=--


## Definition ##

### In terms of algebras over an operad

An **$L_\infty$-algebra** is an [[algebra over an operad]] in the [[category of chain complexes]] over the [[L-∞ operad]].

In the following we spell out in detail what this means in components.

### In terms of higher brackets 
 {#DefinitionViaHigherBrackets}

We now state the definition of $L_\infty$-algebras that is most directly related to the traditional definition of ordinary [[Lie algebras]], namely as $\mathbb{Z}$-[[graded vector space]] $\mathfrak{g}$ equipped with $n$-ary [[multilinear maps|multilinear]] and graded-skew symmetric maps $[-,\cdots,-]$ -- the "brackets" -- that satisfy a generalization of the [[Jacobi identity]].

To that end, we here choose grading conventions such that the following definition of $L_\infty$-algebras reduces to that of ordinary [[Lie algebras]] when $\mathfrak{g}$ is concentrated in _degree zero_. Moreover we take the [[differential]] of the underlying [[chain complex]] of the $L_\infty$-algebra to have degree $-1$ ("homological grading"). Together this means in particular that $\mathfrak{g}$ is a  [[Lie n-algebra]] for $n \in \mathbb{N}$, $n \geq 1$, if it is concentrated in degrees 0 to $n-1$.

Beware that there are also other conventions possible, and there are other conventions in use, for both these choices, leading to different signs in the following formulas. 

+-- {: .num_defn #GradedSignatureOfPermutation}
###### Definition
**(graded signature of a permuation)**

Let $V$ be a $\mathbb{Z}$-[[graded vector space]], and for $n \in \mathbb{N}$ let 

$$
  \mathbf{v} = (v_1, v_2, \cdots, v_n)
$$ 

be an [[n-tuple]] of elements of $V$ of homogeneous degree $\vert v_i \vert  \in \mathbb{Z}$, i.e. such that $v_i \in V_{\vert v_i\vert}$. 

For $\sigma$ a [[permutation]] of $n$ elements, write $(-1)^{\vert \sigma \vert}$ for the [[signature of a permutation|signature of the permutation]], which is by definition equal to $(-1)^k$ if $\sigma$ is the composite of $k \in \mathbb{N}$ permutations that each exchange precisely one pair of neighboring elements.

We say that the _$\mathbf{v}$-graded signature of $\sigma$_

$$
  \chi(\sigma, v_1, \cdots, v_n) \;\in\; \{-1,+1\}
$$ 

is the product of the [[signature of a permutation|signature of the permutation]] $(-1)^{\vert \sigma \vert}$ with a factor of $(-1)^{\vert v_i \vert \vert v_j \vert}$ for each interchange of neighbours $(\cdots v_i,v_j, \cdots )$ to $(\cdots v_j,v_i, \cdots )$ involved in the decomposition of the permuation as a sequence of swapping neighbour pairs.

=--


+-- {: .num_defn #LInfinityDefinitionViaGeneralizedJacobiIdentity}
###### Definition

An $L_\infty$-algebra is 

1. a $\mathbb{Z}$-[[graded vector space]] $\mathfrak{g}$;

1. for each $n \in \mathbb{N}$, $n \geq 1$ a [[multilinear map]], called the _$n$-ary bracket_, of the form

   $$
     l_n(\cdots) 
       \;\coloneqq\; 
     [-,-, \cdots, -]_n 
     \;\colon\; 
       \underset{n \; \text{copies}}{\underbrace{\mathfrak{g} \otimes \cdots \otimes \mathfrak{g}}}
       \longrightarrow
       \mathfrak{g}
   $$
  
   and of degree $n-2$

   (if one includes here $n = 0$ then one speaks of a _[[curved L-infinity algebra]]_)
  
such that the following conditions hold:

1. (**graded skew symmetry**) each $l_n$ is graded antisymmetric, in that for every [[permutation]] $\sigma$ of $n$ elements and for every [[n-tuple]] $(v_1, \cdots, v_n)$ of  homogeneously graded elements $v_i \in \mathfrak{g}_{\vert v_i \vert}$ then

   $$
     l_n(v_{\sigma(1)}, v_{\sigma(2)},\cdots ,v_{\sigma(n)}) 
     = 
     \chi(\sigma,v_1,\cdots, v_n) \cdot l_n(v_1, v_2, \cdots v_n)
   $$

   where $\chi(\sigma,v_1,\cdots, v_n)$ is the $(v_1,\cdots,v_n)$-graded signature of the permuation $\sigma$, according to def. \ref{GradedSignatureOfPermutation};

1. (**strong homotopy [[Jacobi identity]]**) for all $n \in \mathbb{N}$, and for all [[n-tuple|$n$-tuples]] $(v_1, \cdots, v_n)$ of homogeneously graded elements $v_i \in \mathfrak{g}_{\vert v_i \vert}$ the followig [[equation]] holds

   \[
     \label{LInfinityJacobiIdentity}
     \sum_{{i,j \in \mathbb{N}} \atop {i+j = n+1}} 
     \sum_{\sigma \in UnShuff(i,j-1)}
     \chi(\sigma,v_1, \cdots, v_{n})
     (-1)^{i(j-1)}
      l_{j} \left(
        l_i \left( v_{\sigma(1)}, \cdots, v_{\sigma(i)} \right),
        v_{\sigma(i+1)} , \cdots , v_{\sigma(n)}
      \right)
     = 0
     \,,
   \]

   where the inner sum runs over all $(i,j-1)$-[[unshuffles]] $\sigma$ and where $\chi$ is the graded signature sign from def. \ref{GradedSignatureOfPermutation}.

=--



+-- {: .num_example }
###### Example

In lowest degrees the generalized Jacobi identity says that

1. for $n = 1$: the unary map $\partial \coloneqq l_1$ squares to 0:

   $$
     \partial (\partial(v_1)) = 0
   $$

1. for $n = 2$: the unary map $\partial$ is a graded [[derivation]] of the binary map

   $$
     - [\partial v_1, v_2] 
     - (-1)^{\vert v_1 \vert \vert v_2 \vert}
     [\partial v_2, v_1]
     +
     \partial [v_1, v_2]
     =
     0
   $$

   hence
 
   $$
     \partial [v_1, v_2] =  [\partial v_1, v_2] + (-1)^{\vert v_1 \vert} [v_1, \partial v_2]
     \,.
   $$

=--

+-- {: .num_example }
###### Example

When all higher brackets vanish, $l_{k \gt 2}= 0$ then for $n = 3$: 

$$
  [[v_1,v_2],v_3] 
  +
  (-1)^{\vert v_1 \vert (\vert v_2 \vert + \vert v_3 \vert)}
  [[v_2,v_3],v_1]
  +
  (-1)^{\vert v_2 \vert (\vert v_1 \vert + \vert v_3 \vert)}
  [[v_1,v_3],v_2]
  =
  0
$$

this is the graded [[Jacobi identity]]. So in this case the $L_\infty$-algebra
is equivalently a [[dg-Lie algebra]].

=--

+-- {: .num_example }
###### Example

When $l_3$ is possibly non-vanishing, then on elements $x_i$ on which $\partial = l_1$ vanishes then the generalized Jacobi identity for $n = 3$ gives

$$
  [[v_1,v_2],v_3] 
  +
  (-1)^{\vert v_1 \vert (\vert v_2 \vert + \vert v_3 \vert)}
  [[v_2,v_3],v_1]
  +
  (-1)^{\vert v_2 \vert (\vert v_1 \vert + \vert v_3 \vert)}
  [[v_1,v_3],v_2]
  =
  - \partial [v_1, v_2, v_3]
  \,.
$$

This shows that the Jacobi identity holds up to an "exact" term, hence up to homotopy.

=--




### In terms of semifree differential coalgebra
 {#ReformulationInSemifreeDgCoalgebra}

In ([Lada-Stasheff 92](#LadaStasheff92)) it was pointed out that the higher brackets of an $L_\infty$-algebra (def. \ref{LInfinityDefinitionViaGeneralizedJacobiIdentity}) induce on the graded-co-commutative [[cofree coalgebra]] $\vee^\bullet \mathfrak{g}$ over the underlying graded vector space $\mathfrak{g}$ the structure of a [[differential graded coalgebra]], with differential $D = [-] + [-,-] + [-,-,-] + \cdots$ the sum of the higher brackets, extended as graded [[coderivations]]. The higher Jacobi identity is equivalently the condition that $D^2 = 0$. In ([Lada-Markl 94](#LadaMarkl94)) it was observed that conversely, such "semifree" [[differential graded coalgebras]] are an equivalent incarnation of $L_\infty$-algebras. 

(If one uses unital dg-co-algebras then the $L_\infty$-algbras encoded with way are generally [[curved L-infinity algebras]]. To restrict to the non-curved one one either considers co-augmented unital dg-co-algebras or non-unital coalgebras.)

Notice that this immediately imples that if $\mathfrak{g}$ is degreewise finite dimensional, then passing to [[dual vector spaces]] turns semifree [[differential graded coalgebra]]
into [[semifree dga|semifree]] [[differential graded algebras]], which hence are [[opposite category|opposite]]-equivalent to $L_\infty$-algebras of [[finite type]]. For $\mathfrak{g}$ an ordinary finite dimensional [[Lie algebra]], then this dg-algebras is its [[Chevalley-Eilenberg algebra]], hence we may generally speak of [[Chevalley-Eilenberg algebras]] of $L_\infty$-algebras of [[finite type]] (and also more generally, if one invokes [[pro-objects]], see at [model structure for L-infinity algebras -- Use of pro-dg-algebras](model+structure+for+L-infinity+algebras#OnProAlg) ).

In term of the [[operad|operadic]] definition of $L_\infty$-algebras [above](#InTermsOfAlgebrasOverAnOperad) this equivalence is an incarnation of the [[Koszul duality]] between the [[Lie operad]] and the [[commutative operad]].

We now spell out this dg-coalgebraic incarnation of $L_\infty$-algebras.

A (connected) **$L_\infty$-algebra** is 

* an $\mathbb{N}_+$-graded vector space $\mathfrak{g}$;

* equipped with a differential $D : \vee^\bullet \mathfrak{g} \to \vee^\bullet \mathfrak{g}$ of degree $-1$ on the [[free graded co-commutative coalgebra]] over $\mathfrak{g}$ that squares to 0

$$
  D^2 = 0
  \,.
$$

Here the free graded co-commutative co-algebra $\vee^\bullet \mathfrak{g}$ is, as a vector space, the same as the graded [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}$ whose elements we write as 

$$
  3 t_1 \vee t_2 + t_3 + t_3 \vee t_4 \vee t_5
$$

etc (where the $\vee$ is just a funny way to write the wedge $\wedge$, in order to remind us that:...)

but thought of as equipped with the standard coproduct

$$
  \Delta (v_1 \vee v_2 \cdots \vee v_n)
  \propto \sum_i \pm (v_1 \vee \cdots \vee v_i) \otimes (v_{i+1} \vee \cdots \vee v_n)
$$

> (work out or see the references for the signs and prefacors).

Since this is a _free_ graded co-commutative coalgebra, one can see that any differential 

$$
  D : \vee^\bullet \mathfrak{g} \to \vee^\bullet \mathfrak{g}
$$

on it is fixed by its value "on cogenerators" (a statement that is maybe unfamiliar, but simply the straightforward dual of the more familar statement to which we come below, that differentials on free graded algebras are fixed by their action on generators) which means that we can decompose $D$ as

$$
  D = D_1 +  D_2 + D_3 + \cdots
  \,,
$$

where each $D_i$ acts as $l_i$ when evaluated on a homogeneous element of the form $t_1 \vee \cdots \vee t_n$ and is then uniquely extended to all of $\vee^\bullet \mathfrak{g}$ by extending it as a _coderivation_ on a coalgebra.

For instance $D_2$ acts on homogeneous elements of word lenght 3 as

$$
  D_2(t_1 \vee t_2 \vee t_3) = 
  D_2(t_1, t_2)\vee t_3 \pm permutations
  \,.
$$

> exercise for the reader: spell this all out more in detail with all the signs and everyrthing. Possibly by looking it up in the references given below.

Using this, one checks that the simple condition that $D$ squares to 0 is precisely equivalent to the infinite tower of generalized Jacobi identities:


$$
  (D^2 = 0)
  \Leftrightarrow
  \left(
    \forall n : 
  \sum_{i+j = n} \sum_{shuffles \sigma}
  \pm l_i (l_j (v_{\sigma(1)}, \cdots, v_{\sigma(j)} )
   , v_{\sigma(j+1)} , \cdots , v_{\sigma(n)} ) = 0
  \right)
  \,.
$$

So in conclusion we have:

+-- {: .standout}

An $L_\infty$-algebra is a [[dg-coalgebra]] whose underlying [[coalgebra]] is cofree and concentrated in negative degree.

=--


### In terms of semifree differential algebra 
 {#ReformulationInTermsOfSemifreeDGAlgebra}

The reformulation of an $L_\infty$-algebra as simply a semi-co-free graded-co-commutative coalgebra $(\vee^\bullet \mathfrak{g}, D)$ is a useful repackaging of the original definition, but the coalgebraic aspect tends to be not only unfamiliar, but also a bit inconvenient. At least when the graded vector space $\mathfrak{g}$ is degreewise [[finite number|finite]] [[dimension|dimensional]], we may simply pass to its degreewise dual graded vector space $\mathfrak{g}^*$. 

(Fully generally the following works when using not just dg-algebras but [[pro-objects]] in [[dg-algebras]], see at _[model structure for L-infinity algebras -- Use of pro-dg-algebras](model+structure+for+L-infinity+algebras#OnProAlg)_).

Its [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}^*$ is then naturally equipped with an ordinary differential $d = D^*$ which acts on $\omega \in \wedge^\bullet \mathfrak{g}^*$ as

$$
  (d \omega) (t_1 \vee \cdots \vee t_n) =
  \pm \omega(D(t_1 \vee \cdots \vee t_n))
  \,.
$$

When the grading-dust has settled one finds that with 

$$
  \wedge^\bullet \mathfrak{g}^* =
  k \oplus \mathfrak{g}^*_1 \oplus (\mathfrak{g}^*_1 \wedge \mathfrak{g}^*_1 \oplus \mathfrak{g}^*_2) \oplus \cdots
$$

with the ground field in degree 0, the degree 1-elements of $\mathfrak{g}^*$ in degree 1, etc, that $d$ is of degree +1 and of course squares to 0

$$
  d^2 = 0
  \,.
$$

This means that we have a [[semifree dga]]

$$
  CE(\mathfrak{g}) := (\wedge^\bullet \mathfrak{g}^*, d)
  \,.
$$

In the case that $\mathfrak{g}$ happens to be an ordinary [[Lie algebra]], this is the ordinary [[Chevalley-Eilenberg algebra]] of this Lie algebra. Hence we should generally call $CE(\mathfrak{g})$ the [[Chevalley-Eilenberg algebra]]
of the $L_\infty$-algebra $\mathfrak{g}$.

One observes that this construction is bijective: every (degreewise finite dimensional) cochain [[semifree dga]] generated in positive degree comes from a (degreewise finite dimensional) $L_\infty$-algebra this way.

This means that we may just as well _define_ a (degreewise finite dimensional) $L_\infty$-algebra as an object in the [[opposite category]] of (degreewise finite dimensional) commutative [[dg-algebra]]s that are [[semifree dga]]s and generated in positive degree.

(In general this corresponds to [[curved L-infinity algebra]]. The flat $L_\infty$-algebras $\mathfrak{g}$ dually correspond to the dg-algebras which are [[augmented algebra|augmented]] over $\mathbb{R}$, i.e for which the canonical projection $CE(\mathfrak{g}) \longrightarrow \mathbb{R}$ is a homomorphism of dg-algebras.)

And this turns out to be one of the most useful perspectives on $L_\infty$-algebras.

In particular, if we simply drop the condition that the dg-algebra be generated in positive degree and allow it to be generated in non-negative degree over the algebra in degree 0, then we have the notion of the (Chevalley-Eilenberg algebra of) an [[L-infinity-algebroid]]. 

#### Details
  {#DGAlgebraDetails}

We discuss in explit detail the computation that shows that an $L_\infty$-algebra structure on $\mathfrak{g}$ is equivalently a [[dg-algebra]]-structure on $\wedge^\bullet \mathfrak{g}^*$.

Let $\mathfrak{g}$ be a degreewise finite-dimensional $\mathbb{N}_+$[[graded vector space]] equipped with multilinear graded-symmetric maps

$$
  [-,\cdots,-]_k : Sym^k \mathfrak{g} \to \mathfrak{g}
$$

of degree -1, for each $k \in \mathbb{N}_+$. 

Let $\{t_a\}$ be a [[basis]] of $\mathfrak{g}$ and $\{t^a\}$ a dual basis of the degreewise dual $\mathfrak{g}^*$. Equip the [[Grassmann algebra]] $Sym^\bullet \mathfrak{g}^*$ with a [[derivation]]

$$
  d : Sym^\bullet \mathfrak{g}^* \to Sym^\bullet \mathfrak{g}^*
$$

defined on generators by

$$
  d : t^a 
    \mapsto 
    -
   \sum_{k = 1}^\infty 
    \frac{1}{k!}
   [t_{a_1}, \cdots, t_{a_k}]^a_k
   \,
   t^{a_1} \wedge \cdots \wedge t^{a_k}
  \,.
$$

Here we take $t^a$ to be of the same degree as $t_a$. Therefore this derivation has degree +1.

We compute the square $d^2 = d \circ d$:

$$
  \begin{aligned}
    d d t^a 
      &= 
    d (-1)\sum_{k = 1}^\infty 
    \frac{1}{k!}
    [t_{a_1}, \cdots, t_{a_k}]^a_k
   \,
   t^{a_1} \wedge \cdots \wedge t^{a_k}
    \\
    & = 
    \sum_{k,l = 1}^\infty
    \frac{1}{(k-1)! l!}
    [[t_{b_1}, \cdots, t_{b_l}], t_{a_2}, \cdots, t_{a_k}]^a
    \,
    t^{b_1} \wedge \cdots \wedge t^{b_l}  
    \wedge  
    t^{a_2} \wedge \cdots \wedge t^{a_{k}}
  \end{aligned}
  \,.
$$

Here the wedge product on the right projects the nested bracket onto its graded-symmetric components. This is produced by summing over all [[permutation]]s $\sigma \in \Sigma_{k+l-1}$ weighted by the Koszul-[[signature]] of the permutation:

$$
  \cdots = 
    \sum_{k,l = 1}^\infty
    \frac{1}{(k+l-1)!}
    \sum_{\sigma \in \Sigma_{k+l-1}}
    (-1)^{sgn(\sigma)}
    \frac{1}{(k-1)! l!}
    [[t_{b_1}, \cdots, t_{b_l}], t_{a_2}, \cdots, t_{a_k}]^a
    \,
    t^{b_1} \wedge \cdots \wedge t^{b_l}  
    \wedge  
    t^{a_2} \wedge \cdots \wedge t^{a_{k}}
  \,.
$$

The sum over all permutations decomposes into a sum over the $(l,k-1)$-[[unshuffle]]s and a sum over permutations that act inside the first $l$ and the last $(k-1)$ indices.
By the graded-symmetry of the bracket, the latter  do not change the value of the nested bracket. Since there are $(k-1)! l!$ many of them, we get

$$
  \cdots 
    =
    \sum_{k,l = 1}^\infty
    \frac{1}{(k+l-1)!}
    \sum_{\sigma \in Unsh(l,k-1)}
    (-1)^{sgn(\sigma)}
    \left[\left[t_{a_1}, \cdots, t_{a_l}\right], t_{a_{l+1}}, \cdots, t_{a_{k+l-1}}\right]
    \,
    t^{a_1} \wedge \cdots \wedge t^{a_{k+l-1}}
  \,.
$$

Therefore the condition $d^2 = 0$ is equivalent to the condition 

$$
    \sum_{k+l = n-1}
    \sum_{\sigma \in Unsh(l,k-1)}
    (-1)^{sgn(\sigma)}
    \left[\left[t_{a_1}, \cdots, t_{a_l}\right], t_{a_{l+1}}, \cdots, t_{a_{k+l-1}}\right]
  = 0
$$

for all $n \in \mathbb{N}$ and all $\{t_{a_i} \in \mathfrak{g}\}$. This is equation (eq:LInfinityJacobiIdentity) which says that $\{\mathfrak{g}, \{[-,\dots,-]_k\}\}$ is an $L_\infty$-algebra.


### In terms of algebras over an operad
 {#InTermsOfAlgebrasOverAnOperad}

$L_\infty$-algebras are precisely the  [[algebras over an operad]] of the cofibrant resolution of the [[Lie operad]]. 


## Examples

### Special cases

* An $L_\infty$-algebra for which $V$ is concentrated in the first $n$ degree is a **Lie $n$-algebra** (sometimes also: "$L_n$-algebra").

* An $L_\infty$-algebra for which only the unary operation and the binary bracket are non-trivial is a **[[dg-Lie algebra]]**: a [[Lie algebra]] [[internalization|internal to]] the [[category]] of [[dg-algebras]]. From the point of view of higher Lie theory this is a **strict $L_\infty$-algebra**: one for which the Jacobi identity does happen to hold "on the nose", not just up to nontrivial coherent isomorphisms.

* So in particular 

  * an $L_\infty$-algebra generated just in degree 1 is an ordinary **[[Lie algebra]]** ;

  * an $L_\infty$-algebra generated just in degree 1 and 2 is a **[[Lie 2-algebra]]** ;

    * an $L_\infty$-algebra generated just in degree 1 and 2 and with at most binary brackets is a **[[strict Lie 2-algebra]]** , equivalently encoded in a [[differential crossed module]].

  * an $L_\infty$-algebra generated just in degree 1, 2 and 3 is a **[[Lie 3-algebra]]** ;

* if $\mathfrak{g}$ is a Lie algebra over $\mathbf{K}$, and $b^{k-1}\mathbb{K}$ is the complex consisting of the field $\mathbb{K}$ in degree $1-k$, then an $L_\infty$-algebra morphism from $\mathfrak{g}$ to $b^{k-1}\mathbb{K}$ is precisely a degree $k$ [[Lie algebra cohomology|Lie algebra cocycle]].

* The skew-symmetry of the Lie bracket is retained strictly in $L_\infty$-algebras. It is expected that weakening this, too, yields a more general [[vertical categorification]] of Lie algebras. For $n=2$ this has been worked out by Dmitry Roytenberg: [On weak Lie 2-algebras](http://arxiv.org/abs/0712.3461).

* The [[horizontal categorification]] of $L_\infty$-algebras are $L_\infty$-[[Lie infinity-algebroid|algebroid]]s.

* An $L_\infty$-algebra with only $D_n$ non-vanishing is called an **[[n-Lie algebra]]** -- to be distinguished from a _Lie $n$-algebra_ ! However, in large parts of the literature $n$-Lie algebras are considered for which $D_n$ is _not_ of the required homogeneous degree in the grading, or in which no grading is considered in the first place. Such $n$-Lie algebras are not special examples of $L_\infty$-algebras, then. For more see [[n-Lie algebra]].

* An $L_\infty$-algebra internal to [[super vector space]]s is a [[super L-∞ algebra]].

### Classes of examples

* [[automorphism Lie 2-algebra]]

* [[inner derivation Lie 2-algebra]]

* [[automorphism ∞-Lie algebra]]

* For every $\infty$-Lie algebra $\mathfrak{g}$ there is its [[automorphism ∞-Lie algebra]]. In terms of [[rational homotopy theory]] this models the rational automorphism group of the [[rational space]] corresponding to $\mathfrak{g}$.

* [[Poisson-bracket Lie n-algebra]]

* [[Heisenberg Lie n-algebra]] of an [[n-plectic manifold]] or more generally of an [[n-plectic smooth infinity-groupoid]]

* some classes of [[W-algebras]] are claimed to induce $L_\infty$-algebras in [Blumenhagen-Fuchs-Traube 17](W+algebra#BlumenhagenFuchsTraube17)

### Specific examples

* [[line Lie n-algebra]]

* [[string Lie 2-algebra]]

* [[fivebrane Lie 6-algebra]]

* [[supergravity Lie 3-algebra]]

* [[supergravity Lie 6-algebra]]

## Properties

### Ind-Conilpotency
 {#IndConilpotency}

+-- {: .num_remark #IndConilpotency}
###### Remark
**([Pridham 10, remark 3.15, remark 3.13](#Pridham))**

For $\mathfrak{g}$ an $L_\infty$-algebra, then its CE chain [[dgc-coalgebra]] $CE_\bullet(\mathfrak{g})$ ([above](#ReformulationInSemifreeDgCoalgebra)) is _ind-conilpotent_.

This means that $CE_\bullet(\mathfrak{g})$ is a [[filtered colimit]] of sub-dg-coalgebras which are conilpotent, in that for each of them there is $n \in \mathbb{N}$ such that their $n$-fold coproduct vanishes. As such these are like "co-[[local Artin algebras]]".

Moreover, since every dg-coalgebra is the [[union]] of its finite-dimensonal subalgebras (see at _[[dg-coalgebra]]_ the section _[As filtered colimits of finite-dimensional pieces](differential+graded+coalgebra#AsFilteredColimits)_), this means that $CE_\bullet(\mathfrak{g})$ is a [[filtered colimit]] of finite dimensional conilpotent coalgebras.

This implies that the dual Chevalley-Eilenberg cochain algebra $CE^\bullet(\mathfrak{g})$ is a [[filtered limit]] of finite-dimensional nilpotent [[dgc-algebras]] (actual [[local Artin algebras]]).

=--





### Model category structure 

See [[model structure for L-∞ algebras]].

### Relation to dg-Lie algebras

Every [[dg-Lie algebra]] is in an evident way an $L_\infty$-algebra. Dg-Lie algebras are precisely those $L_\infty$-algebras for which all $n$-ary brackets for $n \gt 2$ are trivial. These may be thought of as the _strict_ $L_\infty$-algebras: those for which the [[Jacobi identity]] holds on the nose and all its possible higher coherences are trivial.

+-- {: .num_theorem}
###### Theorem

Let $k$ be a [[field]] of [[characteristic]] 0 and write $L_\infty Alg_k$ for the [[category]] of $L\infty$-algebras over $k$. 

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

### Relation to $\infty$-Lie groupoids

In generalization to how a [[Lie algebra]] integrates to a [[Lie group]], $L_\infty$-algebras integrate to [[∞-Lie group]]s.

See 

[[Lie integration]]

and

<a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieIntegrated">Lie integrated ∞-Lie groupoids</a>.

## Related concepts

* [[A-∞ algebra]]

* [[E-∞ algebra]]

* **$L_\infty$-algebra**

  * [[infinity-Lie algebra cohomology]]

  * [[universal enveloping E-n algebra]]

  * [[nilpotent L-∞ algebra]]

  * [[L-∞ algebroid]]

  * [[derived L-∞ algebroid]]

  * [[sheaf of L-∞ algebras]]


## References 
 {#References}

[[!include L-infinity algebras in physics]]

\linebreak

\linebreak

\linebreak




[[!redirects L-infinity-algebras]]
[[!redirects Lie infinity-algebra]]
[[!redirects L-infinity algebra]]
[[!redirects Lie infinity-algebras]]
[[!redirects L-infinity algebras]]
[[!redirects L-∞ algebra]]
[[!redirects L-∞ algebras]]
[[!redirects L-∞-algebra]]
[[!redirects L-∞-algebras]]

[[!redirects ∞-Lie algebra]]
[[!redirects ∞-Lie-algebra]]
[[!redirects ∞-Lie algebras]]
[[!redirects ∞-Lie-algebras]]

[[!redirects infinity-Lie algebra]]
[[!redirects infinity-Lie-algebra]]
[[!redirects infinity-Lie algebras]]
[[!redirects infinity-Lie-algebras]]



[[!redirects Lie n-algebra]]
[[!redirects L-n-algebra]]
[[!redirects L-n algebra]]
[[!redirects Lie n-algebras]]
[[!redirects L-n-algebras]]
[[!redirects L-n algebras]]

[[!redirects strong homotopy Lie algebra]]
[[!redirects strong homotopy Lie algebras]]

[[!redirects higher Lie algebra]]
[[!redirects higher Lie algebras]]
