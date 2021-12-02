
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Saturated classes of limits
* table of contents
{:toc}

## Idea

A class $\mathcal{X}$ of [[limits]] is *saturated* if it is closed under the "construction" of other limits out of limits in $\mathcal{X}$.

## Definition

Let $V$ be a [[Bénabou cosmos]], and let $\mathcal{X}$ be a [[class]] of $V$-functors $\Phi\colon D\to V$ where $D$ is a [[small category|small]] $V$-category.  Note that the domain $D$ may be different for different elements of $\mathcal{X}$.

Any such $\Phi\colon D\to V$ can serve as a *weight* for defining the [[weighted limit]] of a $V$-functor $D\to C$, for any $V$-category $C$.  We say that a $V$-category is **$\mathcal{X}$-complete** if it admits all such limits, for all $\Phi\in\mathcal{X}$, and thath a $V$-functor between $\mathcal{X}$-complete $V$-categories is **$\mathcal{X}$-continuous** if it preserves all such limits.

The **saturation** of $\mathcal{X}$ is the class of all weights $\Phi\colon D\to V$ (with $D$ small) such that

1. Any $\mathcal{X}$-complete $V$-category admits $\Phi$-weighted limits, and
1. Any $\mathcal{X}$-continuous $V$-functor preserves $\Phi$-weighted limits.

It is an open question whether the second condition is implied by the first in general.

Finally, $\mathcal{X}$ is **saturated** if it is its own saturation.

### The conical case

When $V=Set$, we frequently discuss only *conical* limits, i.e. limits whose weight $\Phi\colon D\to Set$ is the constant functor $\Delta_D 1$ at the terminal set.  These give the classical notion of [[limit]] in a [[category]].

In this case, we may consider instead classes $\mathcal{J}$ of small categories; we write $\Delta_{\mathcal{J}}$ for the class of weights $\{ \Delta_C 1 | C \in \mathcal{J}\}$.  We say that a category $D$ lies in the **saturation** of $\mathcal{J}$ if the weight $\Delta_D 1$ lies in the saturation of $\Delta_{\mathcal{J}}$, and that $\mathcal{J}$ is **saturated** if it is its own saturation.

Note that in practically all cases, the saturation of $\Delta_{\mathcal{J}}$ will contain weights that are not of the form $\Delta_D 1$.  Moreover, even when $V=Set$ there are nontrivial saturated classes of *weights* that do not contain any nontrivial *conical* weights, such as the saturation of the weight for "cartesian squares" $A\times A$.

However, for conical weights the answer to the above open question is known to be affirmative.  On the one hand, if $\mathcal{X}$ is a class of $Set$-weights such that every $\mathcal{X}$-complete category is also $\Delta_D 1$-complete, then every $\mathcal{X}$-continuous funtor is also $\Delta_D 1$-continuous.  See [AK](#AK) for a proof of this.

On the other hand, if $\mathcal{J}$ is a class of $Set$-categories and $\Phi$ is a $Set$-weight such that every $\Delta_{\mathcal{J}}$-complete category is also $\Phi$-complete, then every $\Delta_{\mathcal{J}}$-continuous functor is also $\Phi$-continuous.  In fact, this is still true if instead of $\Delta_{\mathcal{J}}$ we consider a class of weights all of which take only nonempty sets as values.  See [KP](#KP) for a proof of this.

## Characterization

The main theorem of [AK](#AK) (which introduced the notion under the name "closure") is the following.

+-- {: .un_theorem}
###### Theorem
$\Phi\colon D\to V$ lies in the saturation of $\mathcal{X}$ if and only if it lies in the closure of the [[representable functor|representables]] under $\mathcal{X}$-weighted colimits in $[D,V]$.
=--

## Examples

The following examples are all for $V=Set$, restricted to the conical case.

* The class of small [[products]] is saturated, as is the class of finite products.  The latter is the saturation of the finite class containing only [[terminal objects]] and binary products.

* The class of [[L-finite limits]] is saturated; it is the saturation of the class of [[finite limits]].  It is also the saturation of the finite class containing only terminal objects and [[pullbacks]], and the saturation of the class containing only finite products and [[equalizers]].

* The class of [[connected limits]] is saturated.  It is the saturation of the class consisting of [[wide pullbacks]] and equalizers.  Similarly, the class of L-finite connected limits is the saturation of the finite class of pullbacks and equalizers.  See also [[pullback]] and [[wide pullback]] for their saturations.

There are also interesting examples for other $V$.

* When $V=Cat$, the classes of [[PIE-limits]] and [[flexible limits]] are saturated.  The former is, essentially by definition, the saturation of the class containing products, [[inserters]], and [[equifiers]].  The latter can be proven to be the saturation of the class containing products, inserters, equifiers, and [[splitting of idempotents]].

* When $V=F$ is the category of [[fully faithful functors]], so that a $V$-category is an [[F-category]], the class of $w$-[[rigged weight|rigged weights]] is saturated (for any of $w=p$, $l$, or $c$ denoting pseudo, lax, or colax).

* For any $V$, the class of [[absolute colimits]] is saturated.  When $V=Set$, this is the saturation of the [[split idempotent|splitting of idempotents]].

It is also worth mentioning some non-examples.

* For $V=Set$, the class of [[finite limits]] is not saturated; its saturation is the class of [[L-finite limits]].

* For $V=Cat$, the class of [[strict pseudo-limits]] is not saturated; it does not even contain the representables.  (The same is true for strict lax limits.)  It is unclear precisely what its saturation looks like.


## References

* Albert and [[Max Kelly|Kelly]], "The closure of a class of colimits", J. Pure. App. Alg. 51 (1988), 1--17
 {#AK}

* [[Max Kelly]] and [[Robert Paré]], "A note on the Albert-Kelly paper 'The closure of a class of colimits'", JPAA 51 (1988), 19--25
 {#KP}


[[!redirects saturated class of limits]]
[[!redirects saturated classes of limits]]
[[!redirects saturated class of colimits]]
[[!redirects saturated classes of colimits]]
[[!redirects saturated class of weights]]
[[!redirects saturated classes of weights]]
[[!redirects saturation of a class of weights]]
[[!redirects saturation of a class of limits]]
[[!redirects saturation of a class of colimits]]
