
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _kernel pair_ of a [[morphism]] in a [[category]] is the [[fiber product]] of the morphism with itself.

The dual notion is that of [[cokernel pair]].
 
## Definition


The **kernel pair** of a morphism $f:X\to Y$ in a category $C$ is a pair of morphisms $R\,\rightrightarrows \, X$ which form a [[limit]] of the diagram

$$\array{
X &            &   &            & X \\
  & \searrow^f &   & \swarrow_f \\
  &            & Y \\
}$$

We can think of this as the [[fiber product]] $X \times_Y X$ of $X$ with itself over $Y$, or as the [[pullback]] of $f$ along itself.

## Properties

The kernel pair is always a [[congruence]] on $X$; informally, $R$ is the [[subobject]] of $X \times X$ consisting of pairs of elements which have the same value under $f$ (sometimes called the 'kernel' of a function in $\Set$).

The [[coequalizer]] of the kernel pair, if it exists, is supposed to be the "object of equivalence classes" of the internal [[equivalence relation]] $R$. In other words, it is the [[quotient object]] of $X$ in which [[generalized element]]s are identified if they are mapped by $f$ to equal values in $Y$. In a [[regular category]] (at least), this can be identified with a [[subobject]] of $Y$ called the [[image]] of $f$.

If a morphism has a kernel pair and is a coequalizer, then it is the coequalizer of its kernel pair.  This is a special case of the correspondence of [[generalized kernels]] in enriched categories.

In any category with binary [[pullbacks]], the kernel pair of the [[identity morphism]] $id$ on an object $X$ is the [[diagonal morphism]] $(id,id)$ of $X$ and has a [[coequalizer]] [[isomorphic]] to $X$ itself. 

## Related concepts

* [[regular epimorphism]]

* [[regular category]]

* [[exact category]]


[[!redirects kernel pairs]]
