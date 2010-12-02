[[!redirects (2,1)-algebraic theeory of E-infinity algebras]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The [[(∞,1)-algebraic theory]] whose [[∞-algebra over an (∞,1)-algebraic theory|algebras]] are [[E-∞ algebra]]s is the $(2,1)$-category of [[span]]s of [[finite set]]s.


## Definition


+-- {: .un_defn}
###### Definition

Let $2Comm$ be the [[bicategory]] of [[span]]s of [[finite set]]s:

* [[object]]s are finite sets;

* [[morphism]]s are [[span]]s $X_1 \leftarrow Y \to X_1$ in [[FinSet]];

* [[2-morphism]]s are diagrams

  $$
    \array{
        && Y
        \\
        & \swarrow && \searrow
        \\
       X_0 &&\downarrow^{\simeq}&& X_1
       \\
       & \nwarrow && \nearrow
       \\
       && Y'
    }
  $$

  in $FinSet$ whith the vertical morphism an [[isomorphism]].

=--


This is in fact an [[(n,r)-category|(2,1)-category]]. 

## Properties


+-- {: .un_lemma}
###### Observation

Let $Comm$ be the ordinary [[Lawvere theory]] of commutative monoids. There is a forgetful 2-functor

$$
  2Comm \to Comm
 \,.
$$

This exhibits $2Comm$ as being like $Comm$ but with some additional auto-2-morphisms of the morphism of $Comm$.

=--

This is discussed in ([Cranch, beginning of section 5.2](#Cranch)).


+-- {: .un_prop}
###### Proposition

The $(\infty,1)$-category $2Comm$ has finite [[product]]s. The products of objects $A, B$ in $2Comm$ is their [[coproduct]] $A \coprod B$ in [[FinSet]].

=--

This appears as ([Cranch, prop. 4.7](#Cranch)).


+-- {: .un_prop}
###### Proposition

An [[(∞,1)-category]] with [[(∞,1)-limit|(∞,1)-product]] is naturally an algebra over the $(2,1)$-theory $2Comm$.

=--

This appears as ([Cranch, theorem 4.26](#Cranch)).

+-- {: .un_theorem}
###### Theorem

An algebra over the $(2,1)$-theory $2Comm$ in [[(∞,1)Cat]] is
a [[symmetric monoidal (∞,1)-category]].

=--

This appears as ([Cranch, theorem 5.3](#Cranch)).

+-- {: .un_theorem}
###### Theorem

There is a $(2,1)$-algebraic theory $E_\infty$ whose algebras
are at least in parts like [[E-∞ algebra]]s.

=--

This is ([Cranch](#Cranch)), prop. 6.12, theorem 6.13 and section 8.


## References

* [[James Cranch]], _Algebraic Theories and $(\infty,1)$-Categories_ ([arXiv](http://arxiv.org/abs/1011.3243))
{#Cranch}

[[!redirects (2,1)-algebraic theory of E-∞ algebras]]
[[!redirects (2,1)-algebraic theory of E-∞-algebras]]