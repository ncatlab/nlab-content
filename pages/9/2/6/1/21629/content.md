
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The original _May recognition theorem_ ([May 72](#May72)) characterizes the [[homotopy types]] of $n$-fold [[iterated loop spaces]] as "grouplike" [[En-algebras]] in the [[classical model structure on topological spaces|classical homotopy theory of spaces]] ([[∞Grpd]]), hence as [[∞-groups]] with $(n-1)$-fold abelian structure ([[braided ∞-groups]] for $n = 2$, [[sylleptic ∞-group|sylleptic ∞-groups]] for $n=3$, etc.)

The statement generalizes from [[∞Grpd]] to any [[(∞,1)-topos]] ([Lurie 09b, 1.3](#Lurie09b), [Lurie 17, 5.2.6](#Lurie17)).

## Statement


+-- {: .num_prop #RecognitionForGroupsInAnInfinityTopos} 
###### Proposition
**(Recognition of [[group objects in an (∞,1)-category|group objects]] in an [[(∞,1)-topos]])**

Let $\mathbf{H}$ be an [[(∞,1)-topos]]  Then the operation $\Omega$ of forming [[loop space objects]] constitutes an [[equivalence of (∞,1)-categories]]

$$
  Groups(\mathbf{H})
  \underoverset
    {\underset{\;\;\mathbf{B}\;\;}{\longrightarrow}}
    {\overset{\Omega}{\longleftarrow}}
    {\simeq}
  \mathbf{H}^{\ast/}_{\geq 1}
$$

between

1. [[∞-groups]] (i.e. [[groupoid object in an (infinity,1)-category|group objects]]) in $\mathbf{H}$

1. [[pointed object|pointed]] [[n-connected object of an (infinity,1)-topos|connected objects]] in $\mathbf{H}$.

The inverse equivalence is the [[delooping]] $\mathbf{B}$, see at _[[looping and delooping]]_.

=--

This is [Lurie 09a, Theorem 7.2.2.11](#Lurie09a).

More generally:

+-- {: .num_prop #RecognitionForAbelianGroupsInAnInfinityTopos} 
###### Proposition
**(Recognition of abelian [[group objects in an (∞,1)-category|group objects]] in an [[(∞,1)-topos]])**

Let $\mathbf{H}$ be an [[(∞,1)-topos]] and $n \in \mathbb{N}$, $n \geq 1$. Then the operation $\Omega^n$ of forming $n$-fold [[iterated loop space|iterated]] [[loop space objects]] constitutes an [[equivalence of (∞,1)-categories]]

$$
  Groups_{E_n}(\mathbf{H})
  \underoverset
    {\underset{\;\;\mathbf{B}^n\;\;}{\longrightarrow}}
    {\overset{\Omega^n}{\longleftarrow}}
    {\simeq}
  \mathbf{H}^{\ast/}_{\geq n}
$$

1. [[∞-groups]] (i.e. [[groupoid object in an (infinity,1)-category|group objects]]) in $\mathbf{H}$ with [[En-algebra]]-[[mathematical structure|structure]],

1. [[pointed object|pointed]] [[n-connected object of an (infinity,1)-topos|n-connected objects]] in $\mathbf{H}$.


=--

This is [Lurie 09b, Theorem 1.3.6](#Lurie09b), [Lurie 17, Theorem 6.2.6.15](#Lurie17).


## Related concepts

* [[looping and delooping]]

* [[Quillen equivalence between simplicial groups and reduced simplicial sets]]


## References

* {#May72} [[Peter May]], _The geometry of iterated loop spaces_, Lecture Notes in Mathematics, Springer 1972 ([doi:10.1007/BFb0067491](https://link.springer.com/book/10.1007/BFb0067491), [pdf](http://www.math.uchicago.edu/~may/BOOKS/gils.pdf))

* {#Lurie09a} [[Jacob Lurie]], _[[Higher Topos Theory]]_ (2009)

* {#Lurie09b} [[Jacob Lurie]], _Derived Algebraic Geometry VI: $E_k$ Algebras_ ([arXiv:0911.0018](https://arxiv.org/abs/0911.0018))

* {#Lurie17} [[Jacob Lurie]], _[[Higher Algebra]]_ (2017)
