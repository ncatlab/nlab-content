
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **(combinatorial) species** is a [[presheaf]] or [[higher category theory|higher categorical]] presheaf on the [[groupoid]] [[core]]([[FinSet]]).


## Definition


### 1-categorical

The [[category]] of **species**, $Species := PSh(core(FinSet))$, is the [[category of presheaves]] on the [[groupoid]] $\mathbb{P} := core(FinSet)$ of [[finite sets]] and [[bijections]], the [[core]] of [[FinSet]]: 

$$
  \hat \mathbb{P} := PSh(core(FinSet))
  \,.
$$

For more, see [[structure type]].

### 2-categorical

A **2-species** (usually called a [[stuff type]]) is a [[2-presheaf]] on [[core]]([[FinSet]]), i.e. a [[pseudofunctor]]

$$
  core(FinSet) \to Grpd
$$

to the [[2-category]] [[Grpd]].

### $(\infty,1)$-categorical

Generally, an **$\infty$-species** or **homotopical species** is an [[(∞,1)-presheaf]] on $core(FinSet)$, i.e. an [[(∞,1)-functor]]

$$
  core(FinSet)^{op} \to \infty Grpd
$$

to the [[(∞,1)-category]] [[∞Grpd]].

The [[(∞,1)-category]] of $\infty$-species is the [[(∞,1)-category of (∞,1)-presheaves]]

$$
  \infty Species := PSh_{(\infty,1)}(core(FinSet))
  \,,
$$

### Operations on species

There are in fact 5 important monoidal structures on the category of species.  For a discussion of all five, you'll currently have to read about [[Schur functors]], where these operations are discussed in the context of $Fin\Vect$-valued species, i.e. $Fin\Vect$-valued presheaves on the groupoid of finite sets.  But here are two:

#### Sum

The **sum** $A + B$ of two species $A$, $B$ is their [[coproduct]] $A \coprod B$. Since [[colimit]]s of [[presheaves]] are computed objectwise, we have

$$
  (A + B)_n \simeq A_n \coprod B_n
  \,.
$$

#### Product

The category $core(FinSet)$ becomes a [[monoidal category]] under disjoint union of finite sets. This monoidal structure $(core(FinSet), \coprod)$ induces canonically the [[Day convolution]] monoidal structure on $Species := PSh(core(FinSet))$.

For $A$ and $B$ two combinatorial species, their product is given by the [[coend]]

$$
  (A \otimes B)_n
  \simeq
  \int^{n \in FinSet}  A_k \times B_l \times Hom_{core(FinSet)}(n,k+l)
  \simeq
  \coprod_{k+l = n} \prod_{\frac{(k+l)!}{k! + l!}} (A_k \times B_l)
  \,.
$$

## Cardinality

Under [[groupoid cardinality]] 

$$
  {|-|} : \infty Grpd_{tame} \to \mathbb{R}
$$

every (tame) [[∞-groupoid]] is mapped to a [[real number]]

$$
  X \mapsto {|X|} := \sum_{[x] \in \pi_0(X)}\prod_{i = 1}^{\infty} (\pi_i(X,x)^{(-1)^{i}})
  \,.
$$

A species $\mathbf{X}$ assigns an [[∞-groupoid]] $\mathbf{X}_n$ to each [[natural number]] $n \in \mathbb{Z}$. Therefore under [[groupoid cardinality]] we may naturally think of a tame species as mapping to a [[power series]]

$$
  \mathbf{X} \mapsto {|\mathbf{X}|}
  :=
  \sum_{n = 0}^{\infty} \frac{1}{n!} {|\mathbf{X}_n|} z^n
  \in 
  \mathbb{R}[ [ z ] ]
  \,.
$$

This cardinality operation maps the above addition and multiplication of combinatorial species to addition and multiplication of [[power series]].

That [[coproduct]] of species maps to sum of their cardinalities is trivial. That [[Day convolution]] of species maps under cardinality to the product of their cardinality series depends a little bit more subtly on the combinatorial prefactors:

$$
  {| A \otimes B |}
  =
  {|A|} \cdot {|B|}
  =
  \sum_{n=0}^\infty 
   \frac{1}{n!}
   \sum_{k+l = n} \frac{n!}{k! l!} 
   {|A_k|} \cdot {|B_l|}
  \,.
$$

## Variants

If in the definition of combinatorial species the  domain [[core]]([[FinSet]]) is replaced with [[FinVect]] and also the presheaves are take with values in [[FinVect]] then one obtains the notion of  **[[Schur functor]]**.

## References

The notion of species goes back to

* [[André Joyal]], _Une th&#233;orie combinatoire des s&#233;ries formelles_ , Advances in Mathematics 42:1-82 (1981).

An expositional discussion can be found at

* [[Todd Trimble]], _Exponential Generating Function and Introduction to Species_ ([blog](http://topologicalmusings.wordpress.com/2009/03/28/number-of-idempotent-endofunctions/)) (scroll down a bit).

See also wikipedia: [combinatorial species](http://en.wikipedia.org/wiki/Combinatorial_species) and 

* Fran&#231;ois Bergeron, Gilbert Labelle, Pierre Leroux, _Th&#233;orie des esp&#232;ces et combinatoire des structures arborescentes_ , LaCIM, Montr&#233;al (1994). English version: Combinatorial Species and Tree-like Structures, Cambridge University Press (1998).

* Fran&#231;ois Bergeron, Species and variations on the theme of species, invited talk at [Category Theory and Computer Science '04](http://www.itu.dk/research/theory/ctcs2004/), Copenhagen (2004). Slides ([pdf](http://bergeron.math.uqam.ca/Especes_trans.pdf)).

[[!redirects homotopical species]]
[[!redirects (infinity,1) species]]
[[!redirects ∞-species]]
[[!redirects combinatorial species]]
