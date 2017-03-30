
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
* table of contents
{:toc}

## Idea 

The **little $k$-disk operad** or **little $k$-cubes operad** (to distinguish from the [[framed little n-disk operad]]) is the [[topological operad]]/[[(∞,1)-operad]] $E_k$ whose $n$-ary operations are parameterized by rectilinear disjoint embeddings of $n$ $k$-dimensional cubes into another $k$-dimensional cube.

When regarded as a [[topological operad]], the topology on the space of all such embedding is such that a continuous path is given by continuously moving the images of these little cubes in the big cube around.

Therefore the [[algebra over an operad|algebras over]] the $E_k$ operad are "$k$-fold monoidal" objects For instance [[k-tuply monoidal (n,r)-category|k-tuply monoidal (n,r)-categories]].

The limiting [[E-∞ operad]] is a [[resolution]] of the ordinary commutative monoid operad [[Comm]]. Its algebras are [[commutative algebra in an (infinity,1)-category|homotopy commutative monoid objects]] such as $E_\infty$-[[E-infinity-ring|rings]].



## Definition

(...)

An [[algebra over an operad]] over $E_k$ is an [[Ek-algebra]].

### Presentation by enriched operads

(...)

**Remark**

Many models for $E_\infty$-operads in the literature are not in fact cofibrant in the [[model structure on operads]], but are $\Sigma$-cofibrant. By the therem at [[model structure on algebras over an operad]], this is sufficient for their categories of algebras to present the correct $\infty$-categories of [[E-∞ algebras]].

(...)


### As $\infty$-operads

+-- {: .num_defn}
###### Definition


Fix an integer $k \ge 0$. We let $\square^k = ( 
-1, 1)^k$ denote an open cube of dimension $k$. We will say that a map $f : \square^k \to \square^k $
is a _rectilinear embedding_ if it is given by the formula $f (x_1 , . . . , x_k ) = (a_1 x_1 + b_1 , . . . , a_k x_k + b_k )$ for some real constants $a_i$ and $b_i$ , with $a_i \gt 0$.

More generally, if $S$ is a finite set, then we will say that a map $\square^k 
\times S \to \square^k$ is a rectilinear embedding if it is an open embedding whose restriction to each connected component of $\square^k\times S$ is rectilinear.

Let $Rect(\square^k \times S, \square^k )$ denote the collection of all rectitlinear embeddings from $\square^k \times S$ into $\square^k$ . We will regard $Rect(\square^2\times S, \square^k )$ as a topological space (it can be identified with an open subset of $(\mathbf{R}^{2k} )^S )$. 

The spaces $Rect(\square^k \times \{1, . . . , n\}, \square^k)$ constitute the $n$-ary operations of a topological operad, which we 
will denote by $tE_k$ and refer to as the _little k-cubes operad_. 

This is [[Higher Algebra]] Definition 5.1.0.1.
=--

+-- {: .num_defn}
###### Definition
 We define a topological category $tE^\otimes_k$ as follows:

* The objects of $t E^\otimes_k$ are the objects $[n] \in Fin_*$.
 
* Given a pair of objects $[m], [n] \in tE^\otimes_k$ , a morphism from $[m]$ to $[n]$ in $t E^\otimes_k$ consists of the following data:

  * A morphism $\alpha : [m] \to [n]$ in $Fin_*$ .

  * For each $j \in [n]^\circ$ a rectilinear embedding $\square^k \times \alpha^{-1} \{j\} \to \square^k$. 
 
* For every pair of objects $[m], [n] \in tE^\otimes_k$ , we regard $Hom_{tE^\otimes_k} ([m], [n])$ as endowed with the topology induced by the presentation 

$$ Hom_{tE^\otimes_k} ([m], [n]) =
 \coprod_{f : [m]\to [n]} \prod_{1\le j\le n}Rect(\times \alpha^{-1} \{j\},\square^k)$$.
 
*  Composition of morphisms in $tE^\otimes_k$ is defined in the obvious way. We let $E^\otimes_k$ denote the nerve of the topological category $tE^\otimes_k$ . Corollary T.1.1.5.12 implies that $E^\otimes_k is an 
$\infty$-category. There is an evident forgetful functor from $tE^\otimes_k$ to the (discrete) category $Fin_*$ , which induces a functor $E^\otimes_k \to N(Fin_* )$. 

This is [[Higher Algebra]] Definition 5.1.0.2.
=--


## Properties {#Propeties}


### Grouplike monoid objects {#GrouplikeMonoid}

Let $\mathcal{X}$ be an [[(∞,1)-sheaf]] [[(∞,1)-topos]] and $X : Assoc \to \mathcal{X}$ be a monoid object in $\mathcal{X}$.  Say that $X$ is _grouplike_ if the composite

$$
  \Delta^{op} \to Ass \to \mathcal{X}
$$

(see 1.1.13 of [[Commutative Algebra]])

is a [[groupoid object in an (infinity,1)-category|groupoid object]] in $\mathcal{X}$.

Say an $\mathbb{E}[1]$-algebra object is grouplike if it is grouplike as an $Ass$-monoid. Say that an $\mathbb{E}[k]$-algebra object in $\mathcal{X}$ is grouplike if the restriction along $\mathbb{E}[1] \hookrightarrow \mathbb{E}[k]$ is.
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

Let $Y$ be a [[topological space]] equipped with an action of the [[little cubes operad]] $\mathcal{C}_k$ and suppose that $Y$ is grouplike. Then $Y$ is homotopy equivalent to a $k$-fold loop space $\Omega^k X$ for some pointed topological space $X$.

=--

+-- {: .proof}
###### Proof

This is [[Ek-Algebras|EkAlg, theorem 1.3.16.]]

=--

Proofs independent of higher order categories can be extracted from the literature. See this [MO answer](http://mathoverflow.net/a/202345/2926) by Tyler Lawson for details. 

### Stabilization hypothesis {#StabilizationHypothesis}

A proof of the [[stabilization hypothesis]] for [[k-tuply monoidal n-category|k-tuply monoidal n-categories]] is a byproduct of corollary 1.1.10 of ([Lurie](#Lurie)), stated as example 1.2.3.


### Additivity theorem {#AdditivityTheorem}

It has been long conjectured that it should be true that when suitably defined, there is a tensor product of $\infty$-operads such that 

$$
  \mathbb{E}_k \otimes \mathbb{E}_{k'} \simeq \mathbb{E}_{k + k'}
  \,.
$$

This is discussed and realized in section 1.2. of ([Lurie](#Lurie)). The tensor product is defined in appendix B.7.


### Homology: Poisson operads

For an $E_k$-operad in a [[category of chain complexes]], its [[homology]] is the [[Poisson operad]] $P_{k}$.

See for instance ([Costello](#Costello)) and see at _[[Poisson n-algebra]]_.

## Examples

Explicit models of $E_\infty$-operads include

* [[Barratt-Eccles operad]]

(...)

## Related concepts


* [[A-∞ operad]]

* [[E-∞ operad]]

* [[L-∞ operad]]

* [[factorization algebra]]


## References

A standard textbook reference is chapter 4 of 

* [[Peter May]], _The geometry of iterated loop spaces_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))
{#May}

[[John Francis]]' work on $E_n$-actions on $(\infty,1)$-categories is in

* [[John Francis]] PhD thesis ([web](http://dspace.mit.edu/handle/1721.1/43792))

This influenced the revised version of

* [[Jacob Lurie]], _[[Commutative Algebra]]_ ([arXiv](http://arxiv.org/abs/math/0703204))

and is extended to include a discussion of traces and centers in

* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral transforms and Drinfeld Centers in Derived Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))

  (see also [[geometric ∞-function theory]])

A detailed discussion of $E_k$ in the context of [[(∞,1)-operads]] is in

* [[Jacob Lurie]], _$\mathbb{E}[k]$-[[Ek-Algebras|Algebras]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-VI.pdf))
{#Lurie}

An elementary computation of the [[homology]] of the little $n$-disk operad in terms of _solar system calculus_ is in

* Dev Sinha, _The homology of the little disks operad_ ([arXiv:math/0610236](http://arxiv.org/abs/math/0610236))

For the relation to Poisson Operads see

* [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in perturbative quantum field theory : $P_0$-operad_ ([wiki](http://math.northwestern.edu/~costello/factorization_public.html#[[P_0%20operad]])) 


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

[[!redirects Ek-operad]]
[[!redirects Ek-operads]]


[[!redirects E-k operad]]
[[!redirects E-n operad]]
[[!redirects E-k-operad]]
[[!redirects E-n-operad]]

[[!redirects E-k operads]]
[[!redirects E-n operads]]
[[!redirects E-k-operads]]
[[!redirects E-n-operads]]


[[!redirects En operad]]


[[!redirects E-k operad]]
[[!redirects E-k operad]]


[[!redirects little disk operad]]
[[!redirects little 2-disk operad]]