
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The **little $k$-cubes operad** is the [[operad]] or [[(∞,1)-operad]] whose $n$-ary operations are parameterized by rectilinear disjoint embeddings of $n$ $k$-dimensional cubes into another $k$-dimensional cube.

When regarded as a [[topological operad]], the topology on the space of all such embedding is such that a continuous path is given by continuously moving the images of these little cubes in the big cube around.

Therefore the [[algebra over an operad|algebras over]] the $E_k$ operad are "$k$-fold monoidal" objects For instance [[k-tuply monoidal (n,r)-category|k-tuply monoidal (n,r)-categories]].

The limiting $E_\infty$ operad is the resolution of the ordinary commutative monoid operad $Comm$. Its algebras are [[commutative algebra in an (infinity,1)-category|homotopy commutative monoid objects]] such as $E_\infty$-[[E-infinity-ring|rings]].



## Definition

### Presentation by enriched operads

(...)

**Remark**

Many models for $E_\infty$-operads in the literature are not in fact cofibrant in the [[model structure on operads]], but are $\Sigma$-cofibrant. By the therem at [[model structure on algebras over an operad]], this is sufficient for their categories of algebras to present the correct $\infty$-categories of [[E-∞ algebras]].

(...)


### As $\infty$-operads

(...)

## Properties


### Grouplike monoid objects {#GrouplikeMonoid}

Let $\mathcal{X}$ be an [[(∞,1)-sheaf]] [[(∞,1)-topos]] and $X : Assoc \to \mathcal{X}$ be a monoid object in $\mathcal{X}$.  Say that $X$ is _grouplike_ if the composite

$$
  \Delta^{op} \to Ass \to \mathcal{X}
$$

(see 1.1.13 of [[Commutative Algebra]])

is a [[groupoid object in an (infinity,1)-category|groupoid object]] in $\mathcal{X}$.

Say an $\mathbb{E}[1]$-algebra object is grouplike if it is grouplike as an $Ass$-monoid. Say that an $\mathbb{E}[k]$-algebra object in $\mathcal{X}$ is grouplike is the restriction along $\mathbb{E}[1] \hookrightarrow \mathbb{E}[k]$ is.
Write 

$$
  Mon^{gp}_{\mathbb{E}[k]}(\mathcal{X})
  \subset
  Mon_{\mathbb{E}[k]}(\mathcal{X})
$$

for the [[(∞,1)-category]] of grouplike $\mathbb{E}[k]$-monoid objects.


### $k$-fold delooping, monoidalness and $\mathbb{E}[k]$-action###
{: #MainResult}

The following result of ([Lurie](#Lurie)) makes precise for _parameterized [[∞-groupoid]]s_  -- for [[∞-stack]]s -- the general statement that $k$-fold [[delooping]] provides a correspondence betwen [[n-category|n-categories]] that have trivial [[k-morphism|r-morphism]]s for $r \lt k$ and  [[k-tuply monoidal n-category|k-tuply monoidal n-categories]].

+-- {: .un_theorem}
###### Theorem (k-tuply monoidal $\infty$-stacks)

Let $k \gt 0$, let $\mathcal{X}$ be an [[∞-stack]] [[(∞,1)-topos]] and let $\mathcal{X}_*^{\geq k}$ denote the [[full subcategory]] of the category $\mathcal{X}_{*}$ of pointed objects, spanned by those pointed objects thar are $k-1$-[[connected]] (i.e. their first $k$ [[homotopy groups in an (∞,1)-topos|∞-stack homotopy groups]]) vanish. Then there is a canonical equivalence of [[(∞,1)-category|(∞,1)-categories]]

$$
  \mathcal{X}_*^{\geq k} \simeq Mon^{gp}_{\mathbb{E}[k]}(\mathcal{X}) \,.
$$

=--

+-- {: .proof}
###### Proof

This is [[Ek-Algebras|EKAlg, theorem 1.3.6.]].

=--

Specifically for $\mathcal{X} = Top$, this refines to the classical theorem by ([May](#May)).

+-- {: .un_theorem}
###### Theorem (May recognition theorem)

Let $Y$ be a [[topological space]] equipped with an action of the [[little cubes operad]] $\mathcal{C}_k$ and suppose that $X$ is grouplike. Then $Y$ is homotopy equivalent to a $k$-fold loop space $\Omega^k X$ for some pointed topological space $X$.

=--

+-- {: .proof}
###### Proof

This is [[Ek-Algebras|EkAlg, theorem 1.3.16.]]

=--



### Stabilization hypothesis {#StabilizationHypothesis}

A proof of the [[stabilization hypothesis]] for [[k-tuply monoidal n-category|k-tuply monoidal n-categories]] is a byproduct of corollary 1.1.10 of ([Lurie](#Lurie)), stated as example 1.2.3.


### Additivity theorem {#AdditivityTheorem}

It has been long conjectured that it should be true that when suitably defined, there is a tensor product of $\infty$-operads such that 

$$
  \mathbb{E}_k \otimes \mathbb{E}_{k'} \simeq \mathbb{E}_{k + k'}
  \,.
$$

This is discussed and realized in section 1.2. of ([Lurie](#Lurie)). The tensor product is defined in appendix B.7.





## References

A standard textbook reference is chapter 4 of 

* [[Peter May]], _The geometry of iterated loop spaces_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))
{#May}

[[John Francis]]' work on $E_n$-actions on $(\infty,1)$-categories is in

* [[John Francis]] PhD thesis ([web](http://dspace.mit.edu/handle/1721.1/43792))

This influenced the revised version of

* [[Jacob Lurie]], _[[Commutative Algebra]]_ ([arXiv](http://arxiv.org/abs/math/0703204))

and is extended to include a discussion ot traces and centers in

* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral transforms and Drinfeld Centers in Derived Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))

  (see also [[geometric ∞-function theory]])

A detailed discussion of $E_k$ in the context of [[(∞,1)-operads]] is in

* [[Jacob Lurie]], _$\mathbb{E}[k]$-[[Ek-Algebras|Algebras]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-VI.pdf))
{#Lurie}

[[!redirects little k-cubes operad]]
[[!redirects little n-cubes operad]]
[[!redirects little cube operad]]
[[!redirects little k-cube operad]]
[[!redirects little n-cube operad]]

[[!redirects little discs operad]]
[[!redirects little disc operad]]
[[!redirects little k-discs operad]]
[[!redirects little n-discs operad]]
[[!redirects little k-disc operad]]
[[!redirects little n-disc operad]]
[[!redirects little disks operad]]
[[!redirects little disk operad]]
[[!redirects little k-disks operad]]
[[!redirects little n-disks operad]]
[[!redirects little k-disk operad]]
[[!redirects little n-disk operad]]

[[!redirects E-k operad]]
[[!redirects E-n operad]]
[[!redirects E-k-operad]]
[[!redirects E-n-operad]]

[[!redirects E-infinity operad]]
[[!redirects E-∞ operad]]
[[!redirects E-infinity-operad]]
[[!redirects E-∞-operad]]

[[!redirects E-k operad]]
[[!redirects E-k operad]]
