

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .un_defn}
###### Definition

For $C$ a [[monoidal category]], the **category of [[monoid]]s** $Mon(C)$  in the $C$ is the [[category]] whose

* [[object]]s are [[monoid]]s in $C$;

* [[morphism]]s are morphisms in $C$ of the underlying objects that respect the monoid structure.

=--


## Properties

### Free monoids {#FreeMonoids}

+-- {: .un_lemma}
###### Observation


Any category of monoids comes with a [[forgetful functor]]

$$
  U : Mon(C) \to C
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

Let $C$ be a [[monoidal category]] with [[coproduct]]s. Then the forgetful functor $U$ has a [[left adjoint]] $F_C : C \to Mon(C)$. On an object $X \in C$ the underlying object of $F_C X$ is

$$
  U_C F_C X 
  = 
  \coprod_{n \in \mathbb{N}} X^{\otimes n}
  = 
  I_C \coprod X \coprod (X \otimes X) \coprod \cdots
$$

in $C$, with the monoidal structure given by tensor product/juxtaposition.


=--


+-- {: .proof}
###### Proof 

A morphism $f : F_C X \to A$ in $Mon(C)$ with components $f_k : X^{\otimes k} \to U_C A$ is entirely fixed by its component $\tilde f = f_1 : X \to U_C A$ on $X$, because by the homomorphism property and the special free nature of the product in $F_C X$

$$
  \array{
    X^{\times k} \otimes X^{\otimes (n-k)} &\stackrel{f_k \otimes f_{n-k}}{\to}&
    A \otimes A
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\mu_A}}
    \\
    X^{\otimes n} &\stackrel{f_{n}}{\to}& A
  }
$$

it follows that 

$$
  f_n :
  X^{\otimes n} \stackrel{f_1^{\otimes n}}{\to} A^{\otimes n} \stackrel{\mu_A}{\to} A
  \,.
$$

Conversely, every choice for $f_1$ extends to a morphism $f$ in $Mon(C)$ this way.

=--


+-- {: .un_remark}
###### Remark/Example

Free algebras of the form $F(A)$ are called **[[tensor algebra]]**s, at lest for $C = $ [[Vect]] and similar.

=--


+-- {: .un_prop #PushOutOfMonoidsAlongFreeMorphisms}
###### Proposition

For $C$ a category with [[colimit]]s the category $Mon(C)$ of monoids has all [[pushout]]s along morphisms $F(f) : F(A) \to F(B)$ for $f : A \to B$ a morphism in $C$ and $F : C \to Mon(C)$ the free monoid functor from above.

=--

The construction is spelled out for instance in the proof of [SchwedeShipley, lemma 6.2](#SchwedeShipley)

+-- {: .proof}
###### Proof 

(...)

=--

### Model structure

If $C$ is a [[monoidal model category]], then $Mon(C)$ may inherit itself the structure of a [[model category]]. See [[model structure on monoids in a monoidal model category]].


## References

* [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf)) 
{#SchwedeShipley}



[[!redirects categories of monoids]]

category: category