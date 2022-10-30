
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[stack]] $A$ is called a **moduli stack** for certain [[structure]]s, if for any other object $X$ the [[groupoid]] of [[morphism]]s $X \to A$ is [[equivalence of categories|equivalent]] to the groupoid of these kinds of structures on $X$.

This is in contrast to the notion of _[[moduli space]]_, which is only about equivalence classes of structures and loses the information about the [[automorphism]] groups of these structures.

There is an evident generalization of the concept of moduli stacks further up in [[higher topos theory]], to **moduli $\infty$-stacks**.

Notice, however, that every stack is the moduli stack of _something_ . 

## Examples

### Of smooth principal bundles

Let $\mathbf{H} := Sh_\infty(SmthMnfd)$ be collection of [[differentiable stack]]s and generally of [[stacks]] and [[∞-stack]]s over the [[site]] of [[smooth manifold]]s (see [[Smooth∞Grpd]] for details). 

Then every [[Lie group]] $G$ is canonically an [[∞-group|group object]] in $\mathbf{H}$ -- a "group stack" -- and its [[delooping]] in $\mathbf{H}$ produces a stack denoted $\mathbf{B}G$. This is simply the ([[stackification]] of) the [[Lie groupoid]] $*//G$ with a single object and $G$ worth of automorphisms on this object.

Let the $X$ be any [[smooth manifold]], also regarded as a stack, via the [[Yoneda embedding]]. Then one finds that morphisms of stacks

$$
  X \to \mathbf{B}G
$$

are the same as smooth $G$-principal bundles over $X$. More precisely the [[groupoid]] $G Bund(X)$ of smooth $G$-principal bundles and smooth [[gauge transformation]]s between them is canonically equivalent to the [[derived hom-space|hom-groupoid]] of maps from $X$ to $\mathbf{B}G$:

$$
  G Bund(X) \simeq \mathbf{H}(X, \mathbf{B}G)
  \,.
$$

This is discussed in some detail at _[[principal bundle]]_. 

The statement immediately generalizes to higher degrees and to other notions of ([[higher geometry|higher]]) [[geometry]]. This is discussed at _[[principal ∞-bundle]]_.

### Of elliptic curves

A famous moduli stack is that of [[elliptic curves]]. See _[[moduli stack of elliptic curves]]_ for more on this.

## Related concepts

* [[classifying space]], [[moduli space]], [[derived moduli space]], [[geometric invariant theory]]

* [[rigidification of a stack]]

* [[Yoneda lemma]], [[(∞,1)-Yoneda lemma]]

[[!redirects moduli stack]]
[[!redirects classifying stack]]
[[!redirects moduli stacks]]
[[!redirects classifying stacks]]

[[!redirects moduli ∞-stack]]
[[!redirects classifying ∞-stack]]
[[!redirects moduli ∞-stacks]]
[[!redirects classifying ∞-stacks]]

[[!redirects moduli infinity-stack]]
[[!redirects classifying infinity-stack]]
[[!redirects moduli infinity-stacks]]
[[!redirects classifying infinity-stacks]]

[[!redirects moduli 2-stack]]
[[!redirects moduli 2-stacks]]

