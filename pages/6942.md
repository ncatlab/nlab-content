
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

A [[stack]] $A$ is called a **moduli stack** for certain [[structures]], if for any other object $X$ the [[groupoid]] of [[morphisms]] $X \to A$ into $A$ is [[equivalence of categories|equivalent]] to the groupoid of these kinds of structures on $X$.

This is in contrast to the notion of _[[moduli space]]_, which is only about [[equivalence classes]] of structures and loses the information about the [[gauge equivalences]]/ [[automorphism]] groups of these structures.

There is an evident generalization of the concept of moduli stacks in the more general context of [[higher topos theory]], to **[[moduli ∞-stacks]]**.

Notice that every stack is the moduli stack of _something_ and in fact in general of different things at the same time (see below). So to some extent saying "moduli stack" is redundant. It is usually used to indicate, roughly, that there are some [[spaces]]/[[stacks]] that one is working on/over, and then there are apart from this stacks, the moduli stacks, that one is mapping _into_. 

This distinction however easily disappears. For instance a historically famous moduli stack is the [[moduli stack of elliptic curves]] which started out as an object used to classify [[bundles]] of elliptic curves over other spaces. Later in the study of [[elliptic cohomology]] and [[tmf]] the "moduli stack" of elliptic curves came to be regarded as a space interesting in itself for the geometry _on_ it, specifically since this is naturally a [[derived algebraic geometry]].

Analogous comments apply to other moduli stacks. For instance for $G$ a [[topological group]], the moduli stack $\mathbf{B}G \simeq \ast //G$ for topological $G$-[[principal bundles]] is itself interesting for its own geometry. Notably it is the base stack of the [[universal principal bundle]] which as such may be equipped with [[differential geometry]] such as a [[connection on a bundle]] etc.

Generally, what one needs for a stack to classify bundles in this way is a _universal bundle_ over it, for then what the stack _modulates_ are precisely the [[pullbacks]] of this universal bundle. A stack with a prescribed universal bundle over it may be regarded as a stack equipped with an [[atlas]].

In conclusion then "moduli stack" pretty much means "stack" or more precisely "stack with specified universal bundle over it or [[atlas]] into it", with the implicit implication that we say "moduli stack" to indicate that we care about pulling back that atlas/bundle along maps into the stack.

(Compare this to how one says "[[presheaf]]" for what is really just a [[functor]] in order to indicate a certain attitude, namely that one will be interested in asking which presheaves are [[sheaves]].)




## Examples

### Of smooth principal bundles

Let $\mathbf{H} := Sh_\infty(SmthMnfd)$ be collection of [[differentiable stack]]s and generally of [[stacks]] and [[∞-stack]]s over the [[site]] of [[smooth manifold]]s (see [[Smooth∞Grpd]] for details). 

Then every [[Lie group]] $G$ is canonically a [[∞-group|group object]] in $\mathbf{H}$ -- a "group stack" -- and its [[delooping]] in $\mathbf{H}$ produces a stack denoted $\mathbf{B}G$. This is simply the ([[stackification]] of) the [[Lie groupoid]] $*//G$ with a single object and $G$ worth of automorphisms on this object.

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

### Of flat connections

* [[moduli stack of flat connections]]

### Of formal groups

* [[moduli stack of formal groups]]

### Of elliptic curves

A famous moduli stack is that of [[elliptic curves]]. See _[[moduli stack of elliptic curves]]_ for more on this.

### Of Line bundles

* [[Picard stack]]

### Of L-parameters

* [[moduli stack of L-parameters]]

## Related concepts

* [[moduli]], [[moduli problem]]

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

[[!redirects higher moduli stack]]
[[!redirects higher moduli stacks]]

[[!redirects modulus]]
