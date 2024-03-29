
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

On the one hand, a map into a [[classifying space]] _classifies_ some kind of [[object]], it is a _[[classifying morphism]]_, meaning that it characterizes the object (only) up to [[equivalence]]. 

On the other hand, the more refined concept of a [[moduli stack]] is such that [[morphisms]] into it characterize the object itself. Hence it makes sense to say that such maps into moduli stacks not just classify, but **modulate** the given object.

Indeed, that is the idea that originally gave rise to the name _[[moduli]]_.  
Because, more specifically, a [[moduli stack]] $\mathbf{F}$ of a certain kind of objects is such that morphisms $X \stackrel{\chi}{\longrightarrow} \mathbf{F}$ into it determine a [[bundle]] 

$$
  \array{
     P
     \\
     \downarrow
     \\
     X 
  }
$$


of $\mathbf{F}$-like objects over $X$. It is this bundle which is "being modulated (by $\chi$) as one moves around in $X$", much as in the language of electronics a waveform is being modulated as one moves around in time. 

## Examples

### Metric structure

To see that the difference really matters, consider the map of [[classifying spaces]] 

$$
  B O(n) \longrightarrow B GL(n)
$$

for the [[orthogonal group]] and the [[general linear group]]. These classify, respectively, $O(n)$-[[principal bundles]] and $GL(n)$-[[principal bundles]]. While as geometric (e.g. topological or smooth) [[bundles]] these are different, their [[equivalence classes]] are the same. Accordingly the above map is in fact a [[homotopy equivalence]] and accordingly for $\Sigma$ any $n$-dimensional [[manifold]] whose [[tangent bundle]] is classified by $\iota \tau_\Sigma \colon \Sigma \longrightarrow B GL(n)$, then the space of lifts $\iota \hat \tau_\Sigma$ in

$$
  \array{
     && B O(n)
     \\
     & {}^{\mathllap{\iota \hat \tau_\Sigma}} \nearrow & \downarrow
     \\
     \Sigma &\stackrel{\iota \tau_\Sigma}{\longrightarrow}& B GL(n)
  }
$$

is [[contractible space|contractible]]. Hence classifying maps see no difference here.

However, there is an important difference which the modulating morphisms do see. Write

$$
  \mathbf{B}O(n) \longrightarrow \mathbf{B}GL(n)
$$

for the corresponding morphism of [[smooth infinity-groupoid|smooth]] [[moduli stacks]] (see at [[looping and delooping]] for more on this). Then a lift $e$ of the modulating map $\tau_\Sigma \colon \Sigma \longrightarrow \mathbf{B}GL(n)$ to one that modulates an actual orthogonal bundle

$$
  \array{
     && \mathbf{B} O(n)
     \\
     & {}^{\mathllap{e}} \nearrow & \downarrow
     \\
     \Sigma &\stackrel{\tau_\Sigma}{\longrightarrow}& \mathbf{B} GL(n)
  }
$$

is genuine data: this is a choice of [[orthogonal structure]]/[[vielbein]] on $\Sigma$ and hence a [[Riemannian metric]] on $\Sigma$. 

### $G$-Structure for maximal compact subgroup inclusions

An analogous situation is obtained for any inclusion of a [[maximal compact subgroup]] into a given [[Lie group]] and the corresponding notion of [[G-structure]]. All $G$-structures arising this way are invisible to classifying maps, but are seen by modulating maps. See at _[[twisted differential c-structure]]_ for a list of further examples

## References

The terminology "modulating" in the context of "moduli stacks" would seem to be inevitable but is not used much in practice. One place where it is used consistently is 

* {#BenZvi} [[David Ben-Zvi]], _Moduli Spaces_ ([pdf](https://www.ma.utexas.edu/users/benzvi/math/pcm0178.pdf))

[[!redirects modulating morphisms]]

[[!redirects modulates]]
[[!redirects modulating]]


