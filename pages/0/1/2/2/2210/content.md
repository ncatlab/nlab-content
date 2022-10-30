
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#

* table of contents
{:toc}

## Idea 

The _infinitesimal singular simplicial complex_ of a [[space]] $X$ in a [[smooth topos]] $(\mathcal{T},R)$ is the infinitesimal analogue of the singular simplicial complex $X^{\Delta_R^\bullet}$ (see [[interval object]]) that in degree $k$ is the space of $k$-simplices $\Delta^k_R \to X$ in $X$: the infinitesimal singular simplicial complex has in degree $k$ the [[infinitesimal space|infinitesimal]] $k$-simplices in $X$.

There are several ways to make the notion of "infinitesimal $k$-simplex in $X$" precise. Here we describe a notion promoted by [[Anders Kock]], where an "infinitesimal $k$-simplex" in $X$ for $X$ a suitably _locally linear space_ , is a $(k+1)$-tuple $(x_0,\cdots, x_k) \in X^{\times^{k+1}}$ of points in $X$ that are pairwise _infinitesimal neighbours_ in $X$. 

One central application of the singular simplicial complex is in the definition of [[differential forms in synthetic differential geometry]].


## Definition 

The basic definition applies to spaces of the form $R^n$ and is generalized from there to spaces that "locally look like" $R^n$ in one way or other.

Let here and in the following $(\mathcal{T},R)$ be a [[smooth topos]].

## in $R^n$ ##

Write, as usual

$$
  D(n) := \{(\epsilon_i) \in n | \epsilon_i \epsilon_j = 0\} \hookrightarrow R^n
$$ 

for the [[infinitesimal space]] of first order infinitesimal neighbours of the origin of $R^n$, with its canonical inclusion into $R^n$. 

Two elements $x , y \in R^n$ are called **first order infinitesimal neighbours**, denoted $x \sim_1 y$, if their difference is in the image of this inclusion.

$$
  (x \sim_1 y) \Leftrightarrow
  (\exists \epsilon \in D(n) :
  (x-y) = \epsilon) \,.
$$

Write 

$$
  (R^n)^{\Delta^k_{inf}}
  :=
  \{
    (x_0 \in R^n, \cdots, x_k \in R^n) |
    x_i \sim_1 x_j
  \}
  \,.
$$

This naturally forms a [[simplicial object]] $X^{\Delta_{inf}^{bullet}} : \Delta^{op} \to \mathcal{T}$. 
This is the infinitesimal simplicial singular complex of $R^n$.

A more detailed discussion of this is in the entry [[infinitesimal object]] in the section [Spaces of infinitesimal simplices](http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl).

### In smooth loci 

>**warning** this section is as such not drawn from the literature, it seems

Recall that a [[smooth locus]] in $\mathcal{T}$ is an object $\ell A$ that is the joint [[limit]] over some

$$
  R^n \stackrel{\stackrel{f \in J}{\to}}{\stackrel{0}{\to}}
  R
$$

here $J \subset Hom_{\mathcal{T}}(R^n,R)$ is an ideal. 

Declare that two [[generalized element]]s $x,y \in \ell A$ are infinitesimal neighbours if their image under the injection

$$
  \ell A \hookrightarrow R^n
$$

is a pair of infinitesimal neighbour in $R^n$. Then let 

$$
  (\ell A)^{\Delta^\bullet_{inf}}
  \hookrightarrow
  (R^n)^{\Delta_R^\bullet}
$$ 

be the sub-simplicial object of infinitesimal neighbours in $R^n$ that are points in $\ell A$.

+-- {: .un_lemma}
###### Observation
**(linearity of space of infinitesimal neighbours)**

If $p, q \in \ell A$ are infinitesimal neighbours in the [[smooth locus]] $\ell A \subset R^n$, then for all $t \in R$ also the element $p + t(q-p)$ formed by linear combination in $R^n$ is in $\ell A$ and hence is an infinitesimal neighbour of $p$ there.

=--

+-- {: .proof}
###### Proof

Because by the [[Kock-Lawvere axiom]] valid in the [[smooth topos]] $(\mathcal{T},R)$ we have for all $f : R^n \to R$

$$
  0 = f(q) = f(p + (q-p)) = 
  f(p) + \sum_i (q-p)_i (\partial_i f)(q)
  = \sum_i (q-p)_i (\partial_i f)(q)
  \,.
$$

Therefore also 

$$
  f(p + t(q-q)) = t \sum_i (q-p)_i (\partial_i f)(q) = 0
  \,.
$$

=--


#### Examples 

Consider the circle $S^1$ regarded as the [[smooth locus]] $S^1 = \{(x, y) \in R^2 | x^2 + y^2 = 1\}$.

For $a \in S^1 \subset R^2$ an infinitesimal neighbour $(a + \epsilon)$ in $R^2$ is again a point on the circle, and hence an infinitesimal neighbour of $a$ in $S^1$, if 

$$
  a_x^2 + 2 a_x \epsilon_x  + a_y^2 + 2 a_y \epsilon_y = 1
$$

which, due to $a_x^2 + a_y^2 = 1$ is equivalent to

$$
  2 a_x \epsilon_x + 2 a_y \epsilon_y = 0
  \,.
$$

This is solved by $\epsilon$ of the form 

$$
  \epsilon = \delta \left(
    \array{
       a_y
       \\
       - a_x
    }
  \right)
$$

for some fixed $\delta \in D$.

### In formal manifolds

>use that each manifold is locally isomorphic to an $R^n$ and that the neighbourhood relation only needs an infinitesimal neighbourhood. Proceed locally as above and then patch. See references below.

## Inclusion into the finite singular simplicial complex {#InclusionIntoFinPaths}

The [[lined topos]] $(\mathcal{T}, R)$ also comes canonically for every object $X \in \mathcal{T}$ with the finite singular simplicial complex $\Pi(X) : [n] \mapsto X^{R^n}$ induced from regarding

$$
  (0_*, 1_*) : {*} \coprod {*} \to R
$$

as an [[interval object]] (see there for details).

+-- {: .un_def}
###### Definition
**(inclusion of infinitesimal into finite simplices)**

For $\ell A =: X \hookrightarrow R^n$ a [[smooth locus]]
define for all $n \in \mathbb{N}$ a morphism

$$
  \iota_n
  :
  X^{\Delta^k_{inf}}
  \to 
  X^{\Delta_R^k} = X^{R^k}
$$

by defining it on [[generalized element]]s as

$$
  (x^0, \cdots, x^{k})
  \mapsto
  (\vec t \mapsto x^0 + \sum_{i=1}^{k} t_i (x^i - x^{i-1}) )
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

The morphisms $\iota_n$ constitute a morphism of [[simplicial object]]s 

$$
  \iota : X^{\Delta^\bullet_{inf}}
  \hookrightarrow
  X^{\Delta_R^k}
$$

in that they respects the face and degenracy maps on each side.

=--

+-- {: .proof}
###### Proof

Straightforward checking:

For instance

* The inner face maps $d_i$ on $X^{\Delta_{inf}^{k}}$ omit the $i$th point in the $(k+1)$-tuple of points, while on $X^{\Delta^{k}}$ they act by pullback along $(t_1, \cdots, t_k) \mapsto (t_1, \cdots, t_{i-1}, t_{i}, t_i, t_{i+1}, cdots, t_k)$. That means that in the sum above $t_i$ appears twice to yield

  $$
    \cdots + t_i(x^i - x^{i-1}) + t_i(x^{i+1} - x^i) + \cdots
    =
    \cdots + t_i(x^{i+1} - x^{i-1} ) + \cdots    
  $$

  which indeed corresponds to omission of the $i$th point $x^i$.

=--


## Related concepts

The collection of first order infinitesimal neighbours of a space $X$ arranges itself into the [[schreiber:infinitesimal path ∞-groupoid]] $\Pi^{inf}(X)$. Various concepts derive from this one:

of [[differential form]]s may be understood in terms of functions on $\Pi(x)^{inf}$. This is described at

* [[differential forms in synthetic differential geometry]].

A [[deRham space]] is the colimit over a $\Pi^{inf}(X)$. 



## References 

In the language of [[synthetic differential geometry]] the infinitesimal singular complex for "formal manifolds" (internally defined manifolds with an infinitesimal thickening to all orderes) is described (with the simplicial structure not made explicit) in

section I.18 of 

* [[Anders Kock]], _Synthetic Differential Geometry_ ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

and in [section 2.8](http://home.imf.au.dk/kock/SGM-final.pdf#page=89) of

* Anders Kock, _Synthetic geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

Discussion of this that does make the simplicial structure explicit and relates it to the [[Dold-Kan correspondence]] is in 

* Herman Stel, _[[schreiber:master thesis Stel|∞-Stacks and their Function Algebras ? with applications to ∞-Lie theory]]_.

The details of what $X^{\Delta^k_{inf}}$ is like concretely on representables in the [[smooth topos]] $PSh(k-Alg^{op})$ of [[algebraic geometry]], i.e. on [[affine schemes]] is worked out in detail in 

* [[Larry Breen]], [[William Messing]], _Combinatorial differential forms_ ([pdf](http://arxiv.org/abs/math/0005087))

The formulas given there should more or less directly carry over to [[smooth topos]]es with [[smooth locus|smooth loci]] by replacing ordinary rings with [[smooth algebra]]s.

> to be discussed

As the title suggests, the infinitesimal singular simplicial complex is tightly related to [[differential forms in synthetic differential geometry]]: the deRham complex is the normalized [[Moore complex|Moore cochain complex]] of the [[cosimplicial algebra]] $C^\infty(X^{\Delta^\bullet_{inf}})$ of functions on the spaces of infinitesimal simplices.

There is also

* Dubuc, [[Anders Kock|Kock]], _On 1-form classifiers_ , Communications in Algebra 12
(1984)

* Dubuc, $C^\infty$-schemes, Amer. J. of Math. 103 (1981)

* Kumpera, Spencer, _Lie Equations_ , Annals of Math. Studies 73 (1973)


There is also a version of the infinitesimal singular simplicial context in the context of [[nonstandard analysis]]. See

* Zivaljevic, _On a cohomology theory based on hyperfinite sums of microcomplexes_ .

[[!redirects infinitesimal path ∞-groupoid in a lined topos]]
[[!redirects infinitesimal path ∞-groupoid in a smooth topos]]
[[!redirects infinitesimal path infinity-groupoid in a smooth topos]]
[[!redirects infinitesimal path infinity-groupoid in a lined topos]]
[[!redirects infinitesimal neighbour]]