
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
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

The notion of a [[topos]] $X$ that is equipped with a [[local algebra]]-object $\mathcal{O}_X$ is a generalization of the notion of a [[locally ringed topos]]. The algebra object $\mathcal{O}_X$ is then also called the [[structure sheaf]]. 

For that reason in ([Lurie](#Lurie)) such pairs $(X, \mathcal{O}_X)$ are called **structured toposes**. But since the notion of _[[locally ringed topos]]_ is a special case, maybe a more systematic and descriptive term is **locally algebra-ed topos**. Elsewhere this is called a locally _$T$-modelled topos_, where $T$ the given [[algebraic theory]].

## Definition

Let $\mathcal{C}_{\mathbb{T}}$ be the [[syntactic category]] of an [[essentially algebraic theory]] $\mathbb{T}$, hence any category with [[finite limits]]. Let $J$ be a [[subcanonical coverage]] on $\mathcal{C}_{\mathbb{T}}$. Notice that this makes $(\mathcal{C}_{\mathbb{T}}, J)$ be a [[standard site]] and every standard site will do.

Then the [[sheaf topos]] $Sh(\mathcal{C}_{\mathbb{T}}, J)$ is the [[classifying topos]] for the [[geometric theory]] of $\mathbb{T}$-[[local algebra]]s.

For $\mathcal{E}$ any [[topos]], a local $\mathbb{T}$-algebra object in $\mathcal{E}$ is a [[geometric morphism]]

$$
  (\mathcal{O}_X \dashv A_*) : \mathcal{E}
   \stackrel{\overset{\mathcal{O}_X}{\leftarrow}}{\underset{A_*}{\to}}
  Sh(\mathcal{C}_{\mathbb{T}}, J)
  \,.
$$


By the discussion at [[classifying topos]] this is equivalently a functor

$$
  \mathcal{O}_X : \mathcal{C}_{\mathbb{T}} \to \mathcal{E}
$$

such that

1. it preserves [[finite limit]]s (and hence produces a $\mathbb{T}$-[[algebra over an algebraic theory|algebra]] in $\mathcal{E}$);

1. it sends $J$-[[covering]]s to [[epimorphism]]s; which makes it a _local_ $\mathbb{T}$-algebra.

The pair $(\mathcal{E}, \mathcal{O}_X)$ is called a **locally $\mathbb{T}$-algebra-ed topos**.


## Examples

All of the following notions are special cases of locally algebra-ed toposes:

* [[ringed space]], [[locally ringed space]];

* [[ringed site]], [[locally ringed site]]

* [[ringed topos]], [[locally ringed topos]].

The [[(∞,1)-category theory]]-version is that of

* [[locally algebra-ed (∞,1)-topos]].

## Related concepts

* [[Cole's theory of spectrum]]

## References

* [[Julian Cole]], _The Bicategory of Topoi, and Spectra_ , ms. ([pdf](http://www.oliviacaramello.com/Unification/ColeBicategoryTopoiSpectra.pdf))


* {#Lurie} [[Jacob Lurie]], _[[Structured Spaces]]_
 



[[!redirects locally algebra-ed toposes]]

[[!redirects modelled topos]]
[[!redirects T-modelled topos]]
[[!redirects modelled toposes]]
[[!redirects T-modelled toposes]]
[[!redirects modelled topoi]]
[[!redirects T-modelled topoi]]
