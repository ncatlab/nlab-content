[[!redirects Eudoxus real numbers]]

# Contents # 
* table of contents 
{:toc} 

## Idea 

*Eudoxus real number* refers to a construction of the [[ordered field]] of [[real numbers]] discovered by [[Stephen Schanuel]]. The idea is that every real number $r$ can be represented by a [[relation]] on the [[integers]] that is "almost linear", e.g., the function that takes an integer $n$ to the [[floor]] of $r n$. Schanuel named this after [[Eudoxus]], who developed a theory of magnitude and proportion to account for the relations between the discrete and the continuous[^1]. 

[^1]: Quoting Schanuel: "[Eudoxus] noted that to measure
the ratio of a line segment to another with any desired accuracy, it isn't
necessary to cut either of them up -- instead multiply the 'numerator'
segment by a large integer -- thus pointing the way to a direct construction
of the reals as ring from the integers as mere additive group." 

## Definition 

A [[function]] $f: \mathbb{Z} \to \mathbb{Z}$ is *almost linear* if the quantity $f(m+n) - f(m) - f(n)$ taken over all $m, n \in \mathbb{Z}$ is [[bounded set|bounded]]. Almost linear functions are closed under the pointwise [[abelian group]] operations inherited from $\mathbb{Z}$ (i.e., $f + g$, $-f$), and are also closed under composition of functions. 

Define an equivalence relation $\sim$ on the set of almost linear functions $AL(\mathbb{Z})$ by $f \sim g$ if $f - g$ is bounded. This equivalence relation respects the abelian group structure of $AL(\mathbb{Z})$, and if $f \sim f'$, then for any $g \in AL(\mathbb{Z})$ we have $g \circ f \sim g \circ f'$ and $f \circ g \sim f' \circ g$. We write $[f]$ for the equivalence class of $f$. 

+-- {: .num_defn} 
###### Definition 
A **Eudoxus real number** is an equivalence class of $AL(\mathbb{Z})$ under $\sim$. 
=-- 

The set of Eudoxus reals $\mathbb{E} \coloneqq AL(\mathbb{Z})/\sim$ becomes a [[commutative ring]] whose addition and multiplication are descended from $+$ and $\circ$ on $AL(\mathbb{Z})$. Already one distributive law $(f + f') \circ g = f \circ g + f' \circ g$ holds in $AL(\mathbb{Z})$, so as soon as one proves multiplication on $\mathbb{E}$ is commutative, one gets distributivity on the other side. 

A Eudoxus real $[f]$ is deemed *positive* if it is represented by an $f$ such that for any $C$ there are infinitely many $m \in \mathbb{N}$ such that $f(m) \gt C$. It is easy to see this condition would then be satisfied by any representative function. As usual, define $[f] \lt [g]$ to mean $[g-f]$ is positive. 

+-- {: .num_theorem} 
###### Theorem 
The commutative ring $\mathbb{E}$ equipped with $\lt$ is a [[real number|complete ordered field]]. 
=-- 

A careful proof and exposition has been given by [Arthan](#Arthan). The resulting construction is equivalent to the [[Cauchy reals]]; indeed for any almost linear function $f$, the sequence $f(n)/n$ is a [[Cauchy sequence]] of rationals that converges to the corresponding real number.

### As an initial algebra

An endofunction $f:\mathbb{Z}^\mathbb{Z}$ over the [[integers]] is *bounded* if 

$$\exists C \in \mathbb{Z}. \forall m \in \mathbb{Z}. \vert f(m) \vert \lt C$$

and $f$ is *almost linear* if

$$\exists C \in \mathbb{Z}. \forall m \in \mathbb{Z}. \forall n \in \mathbb{Z}. \vert f(m + n) - f(m) - f(n) \vert \lt C$$

Let the set of almost linear endofunctions over the integers be defined as 

$$AL(\mathbb{Z}) \coloneqq \{f\in \mathbb{Z}^\mathbb{Z} \vert \exists C \in \mathbb{Z}. \forall m \in \mathbb{Z}. \forall n \in \mathbb{Z}. \vert f(m + n) - f(m) - f(n) \vert \lt C \}$$

Let us define a *Eudoxus algebra* as a [[set]] $A$ with a function $\iota \in A^{AL(\mathbb{Z})}$ such that 

$$\forall f \in AL(\mathbb{Z}). \forall g \in AL(\mathbb{Z}). (\exists C \in \mathbb{Z}. \forall m \in \mathbb{Z}. \vert f(m) - g(m) \vert \lt C) \implies (\iota(f) = \iota(g))$$

An *Eudoxus algebra homomorphism* between two Eudoxus algebras $A$ and $B$ is a function $f \in B^A$ such that 

$$\forall a \in AL(\mathbb{Z}). f(\iota_A(a)) = \iota_B(a)$$

The *category of Eudoxus algebras* is the category $EudoxusAlg$ whose objects $Ob(EudoxusAlg)$ are Eudoxus algebras and whose morphisms $Mor(EudoxusAlg)$ are Eudoxus algebra homomorphisms. The set of **Eudoxus real numbers**, denoted $\mathbb{R}$, is defined as the initial object in the category of Eudoxus algebras. 

### As a quotient inductive type

Let the proposition that an endofunction $f:\mathbb{Z} \to \mathbb{Z}$ over the [[integers]] is *bounded* be defined as follows:

$$isBounded(f) \coloneqq \left\Vert \sum_{C:\mathbb{Z}} \prod_{m:\mathbb{Z}} \vert f(m) \vert \lt C \ \right\Vert$$

and let the proposition that $f$ is *almost linear* be defined as follows: 

$$isAlmostLinear(f) \coloneqq \left\Vert \sum_{C:\mathbb{Z}} \prod_{m:\mathbb{Z}} \prod_{n:\mathbb{Z}} \vert f(m + n) - f(m) - f(n) \vert \lt C \ \right\Vert$$

Let the type of almost linear endofunctions over the integers be defined as

$$AL(\mathbb{Z}) \coloneqq \sum_{f:\mathbb{Z} \to \mathbb{Z}} isAlmostLinear(f)$$

The type of **Eudoxus real numbers**, denoted as $\mathbb{R}$, is a [[higher inductive type]] generated by:

* a function $\iota: AL(\mathbb{Z}) \to \mathbb{R}$

* a dependent product of functions from propositions to identities:

$$ \eta : \prod_{f:AL(\mathbb{Z})} \prod_{g:AL(\mathbb{Z})} isBounded(f - g) \to (\iota(f) = \iota(g))$$

 * A set-truncator 
$$\tau_0: \prod_{a:\mathbb{R}} \prod_{b:\mathbb{R}} isProp(a=b)$$
 

## Remarks 

In an exchange at the categories list, Steve Schanuel says he got the idea from an old observation by (John) Tate on bilinear maps on $\mathbb{Z}$. The "attribution" to Eudoxus is best understood in the context of the footnote below. Particularly, it should not be thought that Eudoxus was 'constructing' the reals (whether of Dedekind type or Cauchy type) or constructing anything at all necessarily (rationals included), despite modern glosses on the spirit of Eudoxus's theory of magnitude that suggest more of a kinship to Dedekind cuts, and despite the fact that 'Eudoxus reals' as described here are equivalent to Cauchy reals, not Dedekind reals. Mainly, Schanuel is observing that by following a path suggested by Eudoxus, one can get to the reals directly, bypassing the need for the rationals as an intermediate construction.  

There was a discussion on this at the [categories list](#thread). 

## See also

* [[real number]]

* [[modulated Cauchy real number]]

* [[HoTT book real number]]

## References 

Schanuel's discovery was unpublished by him, but was first disseminated by Ross Street: 

* [[Ross Street]], _An efficient construction of the real numbers_, Gazette Australian Math. Soc. 12 (57&#8211;58), 1985. ([web](https://andrescaicedo.files.wordpress.com/2014/09/ross-street-an-efficient-construction-of-real-numbers.pdf)) 

It was subsequently noted several times in the literature that Street's sketch in that note on how to establish completeness isn't quite right. Street of course acknowledged this and gave an updated account here, mentioning for example corrected versions (e.g., by Arthan; see below): 

* Ross Street, _Update on the efficient reals_, September 2003. ([web](http://maths.mq.edu.au/~street/reals.pdf)) 

Scattered remarks by Street, [[Michael Barr]], and Schanuel may be found at the categories list, 

* Schanuel et al., Thread on reals &#224; la Tate, Eudoxus, etc., [categories list](http://facultypages.ecc.edu/alsani/ct99-00%288-12%29/threads.html#00073) (year 2000). 
 {#thread} 

The quote attributed to Schanuel (see the footnote) was drawn from that thread. 

A correct and fairly comprehensive account of the construction is by Arthan, who includes some useful historical material: 

* Rob Arthan, _The Eudoxus Real Numbers_, [http://arxiv.org/abs/math/0405454](http://arxiv.org/abs/math/0405454) (May 24, 2004). 
 {#Arthan} 
