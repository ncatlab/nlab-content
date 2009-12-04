
notes on

* [[Jacob Lurie]], _$\mathbb{E}[k]$-Algebras_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-VI.pdf))


#Contents#
* automatic table of contents goes here
{:toc}


## Grouplike monoid objects {#GrouplikeMonoid}

Let $\mathcal{X}$ be an [[∞-stack]] [[(∞,1)-topos]] and $X : Ass \to \mathcal{X}$ be a monoid object in $\mathcal{X}$.  Say that $X$ is _grouplike_ if the composite

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

## Main result {#MainResult}


The following result makes precise for _parameterized [[∞-groupoid]]s_  -- for [[∞-stack]]s -- the general statement that $k$-fold [[delooping]] provides a correspondence betwen [[n-category|n-categories]] that have trivial [[k-morphism|r-morphism]]s for $r \lt k$ and  [[k-tuply monoidal n-category|k-tuply monoidal n-categories]].

+-- {: .un_theorem}
###### Theorem (k-tuply monoidal $\infty$-stacks)

Let $k \gt 0$, let $\mathcal{X}$ be an [[∞-stack]] [[(∞,1)-topos]] and let $\mathcal{X}_*^{\geq k}$ denote the [[full subcategory]] of the category $\mathcal{X}_{*}$ of pointed objects, spanned by those pointed objects thar are $k$-connective (i.e. its first $k$ [[homotopy group (of an ∞-stack)|∞-stack homotopy groups]]) vanish. Then there is a canonical equivalence of [[(∞,1)-category|(∞,1)-categories]]

$$
  \mathcal{X}_*^{\geq k} \simeq Mon^{gp}_{\mathbb{E}[k]}(\mathcal{X}) \,.
$$

=--

+-- {: .proof}
###### Proof

Theorem 1.3.6.

=--

Specifically for $\mathcal{X} = Top$, this reefines to the classical theorem by [[Peter May]]

+-- {: .un_theorem}
###### Theorem (May)

Let $Y$ be a [[topological space]] equipped with an action of the [[little cubes operad]] $\mathcal{C}_k$ and suppose that $X$ is grouplike. Then $Y$ is homotopy equivalent to a $k$-fold loop space $\Omega^k X$ for some pointed topological space $X$.

=--

+-- {: .proof}
###### Proof

Theorem 1.3.16.

=--

### Related literature

Lurie's proof of the equivalence of $n$-connected objects with grouplike $E[k]$-objects is entirely at the level of [[(∞,1)-category|(∞,1)-categories]]. One would hope that in addition there is a model for this equivalence at the level of [[model category|model categories]].

There is a model category structure on the category $Top_*$ of pointed topological spaces, such that the cofibrant objects are $n$-connected [[CW-complex]]es, described in

* J. Aldana, J. Paricio, M. Rodriguez, _A closed model category for $(n-1)$-connected spaces_ ([pdf](http://www.ams.org/proc/1996-124-11/S0002-9939-96-03606-4/S0002-9939-96-03606-4.pdf))


## Stabilization hypothesis {#StabilizationHypothesis}

A proof of the [[stabilization hypothesis]] for [[k-tuply monoidal n-category|k-tuply monoidal n-categories]] is a byproduct of corollary 1.1.10, stated as example 1.2.3

## contents  

* [[(infinity,1)-operad]]

* [[little cubes operad]]

* [[topological chiral homology]]


[[!redirects E-k-Algebras]]

category: reference