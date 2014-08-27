
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Idea

Fully generally one might call any [[Picard ∞-groupoid]] equipped with the structure of an [[∞-stack]] a _Picard ∞-stack_. But as with [[Picard groups]] themselves, this fully general concept is typically considered in the special case of [[Picard ∞-groupoids]] of [[∞-line bundles]] over a given [[space]] in [[algebraic geometry]]([[E-∞ geometry]]. That is what we discuss here: [[moduli ∞-stacks]] of [[multiplicative group]]-[[principal ∞-bundles]].

## Definition

### General abstract

For some algebraic [[site]]/[[(∞,1)-site]] such as the [[étale site]] or the [[étale (∞,1)-site]], write $\mathcal{B}$ for the [[(∞,1)-topos of (∞,1)-sheaves]] over that site. For $S\in \mathcal{B}$ any object, write $\mathcal{B}_{/S}$ for its [[slice (∞,1)-topos]].
 
Here $\mathcal{B}$ contains a canonical [[group object in an (∞,1)-category|group object]] $\mathbb{G}_m \in Grp(\mathcal{B})$, the absolute [[multiplicative group]] given as an [[(∞,1)-presheaf]] by the assignment which sends any [[commutative ring]]/[[E-∞ ring]] to its [[group of units]]/[[∞-group of units]]

$$
  \mathbb{G}_m \;\colon\; R \mapsto R^\times
  \,.
$$

The [[inverse image]] of $\mathbb{G}_m$ under [[base change]] along $S \to \ast$ we will still denote by $\mathbb{G}_m \in Grp(\mathcal{B}_{/S})$.

Write $\mathbf{B}\mathbb{G}_m$ for the [[delooping]] of $\mathbb{G}_m$. 

For $X \in \mathcal{B}_{/S}$ any object, then morphisms

$$
  X \longrightarrow \mathbf{B}\mathbb{G}_m  
$$

in $\mathcal{B}_{/S}$ modulate $\mathbb{G}_m$-[[principal ∞-bundles]] on $X$, whose canonically [[associated ∞-bundles]] are algebraic $\mathbb{G}_a$-[[∞-line bundles]]. (...) (Notice that by the [[Koszul-Malgrange theorem]] these are often better thought of as line bundles with flat holomorphic connection...)

The [[internal hom]]/[[mapping stack]]

$$
  \mathbf{Pic}(X) \coloneqq [X,\mathbf{B}\mathbb{G}_m]
  \in 
  \mathcal{B}_{/\mathcal{S}}
$$

is the _Picard $\infty$-stack_ of $X$.

Unwinding the definitions, this is the [[(∞,1)-presheaf]] which sends $S'\to S$ to the [[∞-groupoid]] of [[∞-line bundle]] on the [[(∞,1)-fiber product]] with $X \to S$:

$$
  \mathbf{Pic}(X) \;\colon\; (S' \to S) \mapsto \mathcal{B}(S' \underset{S}{\times}X, \mathbf{B}\mathbb{G}_m)
  \,.
$$

In essentially this form the definition is indicated for instance in  ([Lurie 04, section 8.2](#LurieDAG)).


In good cases its [[truncated object in an (∞,1)-topos|0-truncation]] is a [[scheme]], in which case it is called the _[[Picard scheme]]_.

### More concrete realization

See at _[Picard Scheme -- Picard stack](Picard+scheme#PicardStack)_.

## Properties

### Differentiation / deformation theory

The [[Lie differentiation]] of $\tau_0 \mathbf{Pic}(X)$ is, if it exists as a [[formal scheme|formal]] [[group scheme]], the [[Artin-Mazur formal group]] $\Phi^1_X$.

## Related concepts

* [[Brauer stack]]

## References

* [[The Stacks Project]], _[The Picard stack](http://stacks.math.columbia.edu/tag/0372)_

* {#Lurie04} [[Jacob Lurie]], section 8.2 of _Derived algebraic geometry_, PhD thesis, 2004 ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG.pdf), [web](http://dspace.mit.edu/handle/1721.1/30144))


[[!redirects Picard stack]]
[[!redirects Picard stacks]]

[[!redirects Picard ∞-stack]]
[[!redirects Picard ∞-stacks]]
