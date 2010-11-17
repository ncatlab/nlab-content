
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

For $C$ and $D$ [[monoidal model categories]], a **lax monoidal Quillen adjunction**

$$
  (L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
  D
$$

is

* a [[Quillen adjunction]] $(L \dashv R)$ between the underlying [[model categories]];

* equipped with the structure of a [[lax monoidal functor]] on $R$ with respect to the underlying [[monoidal categories]]

* such that the induced structure of an [[oplax monoidal functor]] on $L$ satisfies:

  1. for all cofibrant objects $x,y \in D$ the oplax monoidal transformation

     $$
       L(x \otimes y) \to L(x) \otimes L(y)
     $$

     is a weak equivalence in $C$    

  1. for some (hence any) cofibrant [[resolution]] $q : \hat I_D \stackrel{\simeq}{\to} I_D$ of the monoidal unit object in $D$, the composite

     $$
       L(\hat I_D) \stackrel{L(q)}{\to} L(I_D) \to I_C
     $$

     is a weak equivalence in $C$.

This is called a **strong monoidal Quillen adjunction** if $L$ is a [[strong monoidal functor]]. 

If a monoidal Quillen adjunction is also a [[Quillen equivalence]] it is called a **monoidal Quillen equivalence**.

## Properties

### Recognition of monoidal Quillen adjunctions {#Recognition}

+-- {: .un_theorem}
###### Theorem

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a [[Quillen adjunction]] between [[monoidal model categories]] and let $R$ be equipped with the strcuture of a [[lax monoidal functor]].

Then the following two conditions are sufficient for $(L \dashv R)$ to be a lax monoidal Quillen adjunction:

1. for some (hence any) cofibrant [[resolution]] $q : \hat I_D \stackrel{\simeq}{\to} I_D$ of the unit object in $D$, the composite morphism

   $$
     L(\hat I_D) \stackrel{L(q)}{\to} L(I_D) \stackrel{\tilde i}{\to} I_C
   $$

   is a weak equivalence, (wher $\tilde i$ is the [[adjunct]] of $i : I_D \to R(I_C)$);

1. the unit object $I_D$ _detects weak equivalences_ in that for every weak equivalence $f : X \to Y$ between fibrant objects the morphism $D^{\Delta^{op}}(Q I_D, f)$ of [[hom-object]]s in the category of [[simplicial object]]s in $D$ is an equivalence of Kan complexes, for $Q I_D$ a cofibrant resolution in the [[Reedy model structure]] $D^{\Delta^{op}}_{Reedy}$. 

=--

This is proposition 3.16 in ([SchwedeShipley](#SchwedeShipley)).




### Lift to Quillen adjunctions on monoids {#LiftToMonoids}

We discuss how a monoidal Quillen adjunction $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ induces, under mild conditions, a Quillen adjunction $(L^{mon} \dashv R) : Mon(C) \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} Mon(D)$ on the corresponding categories of [[monoid]]s.


The [[lax monoidal functor]] $R : C \to D$ induces (as described there) a functor $R : Mon(C) \to Mon(D)$ on monoids (which by slight abuse of notation we denote by the same symbol). While the left adjoint $L$ will not extend to monoids unless $R$ is a [[strong monoidal functor]] there is nevertheless an adjoint $L^{mon}$ to $R : Mon(C) \to Mon(D)$:

+-- {: .un_prop}
###### Proposition

Let $C$ be a [[monoidal category]] with colimits, write $Mon(C)$ for its category of [[monoid]]s and $U_C : Mon(C) \to C$ for the evident [[forgetful functor]]. This has a [[left adjoint]] $F_C : C \to Mon(C)$ where on an object $X \in C$ the underlying object of $F_C X$ is

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

+-- {: .un_prop #AdjunctionOnMonoids}
###### Proposition

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a pair of adjoint functors between monoidal categories where $R$ is a lax monoidal functor and $D$ has all small colimits.

Then the functor $R : Mon(C) \to Mon(D)$ has a left adjoint

$$
  L^{mon} : Mon(D) \to Mon(C)
$$

given by forming the [[coequalizer]]s

$$
  L^{mon} : B 
    \mapsto 
   \lim_{\to}
  (F_D L F_C B \stackrel{\to}{\to} F_D L B)
$$

of the following two morphisms

* the first one is the image under $F_C \circ L$ of the adjunction counit $ F_D U_D B  \to B$;

* the second is the unique $C$-monoid morphism that restricts to the $C$-morphism

  $$
    L F_D B
    \simeq
   \coprod_{n \in \mathbb{N}} L( B^{otimes n})
    \stackrel{\coprod \tilde e}{\to}
   \coprod_{n \in \mathbb{N}}
   (L B)^{\otimes n}
   \simeq
   F_C L B
   \,.
  $$


This monoid left adjoint is related to the original left adjoint by a [[natural isomorphism]]

$$
  L^{mon} \circ F_D
  \simeq
  F_C \circ L
$$

=--

This is considered on p. 305 of ([SchwedeShipley](#SchwedeShipley))

+-- {: .proof}
###### Proof 

(...)

=--

For $C$ and $D$ [[monoidal model categories]] we may ask if on their categories of [[monoid]]s exist the corresponding [[transferred model structure]]s, transferred along the [[stuff, structure, property|forgetful]]/[[free functor]] adjunction 

$$
  (F_C \dashv U_C) : Mon(C) \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  C
  \,.
$$

For the purposes of the following statement, we define

+-- {: .un_def #CreatedModelStructure}
###### Definition

We say a model category structure on $Mon(C)$ is _created_ by $U_C$ is

* it is the [[transferred model structure]];

* every cofibrant object in $Mon(C)$ is a [[retract]] of a [[cell object]].

=--

+-- {: .un_theorem}
###### Theorem

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a lax monoidal Quillen adjunction between [[monoidal model categories]] with cofibrant unit obects.

If the forgetful functors $U_C$ and $U_D$ [create](#CreatedModelStructure) model structures on monoids, then the adjunction $(L^{mon} \dashv R)$ from [above](#AdjunctionOnMonoids) is a [[Quillen adjunction]]

$$
  (L^{mon} \dashv R) 
  : 
  Mon(C) \stackrel{\overset{L^{mon}}{\leftarrow}}{\underset{R}{\to}} Mon(D)
  \,,
$$

between the transferred model structures on monoids.

=--

This is theorem 3.12 in ([SchwedeShipley](#SchwedeShipley)). Its proof uses the following technical lemmas

+-- {: .un_lemma #OneTechnicalLemma}
###### Lemma

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a monoidal Quillen adjunction between monoidal model categories with cofibrant unit objects.

Suppose the adjunction

$$
  (L^{mon} \dashv R) 
  : 
  Mon(C) \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} Mon(D)
$$

described above exists (just as an adjunction, not yet assumed to be a Quillen adjunction). Then for every monoid $B \in Mon(D)$ which is an $(L^\mon \dashv R)$-[[cell object]], the [[adjunct]]

$$
 \chi_B :  L B \to L^{mon} B
$$

to the morphism underlying the unit $B \to R L^{mon} B$ is a weak equivalence.

=--

This is proposition 5.1 in ([SchwedeShipley](#SchwedeShipley)).

+-- {: .proof}
###### Proof 

We first show this for $B = I_D$ the tensor unit in $D$, which in $Mon(D)$ is the [[initial object]]s. Since $L^{mon}$ is a [[left adjoint]] it sends this initial object to he initial object in $Mon(D)$, $L^{mon} : I_D \mapsto I_C$. One checks 
  
(...) 

that the adjunction unit $I_C \to R L^{mon} I_D \stackrel{\simeq}{\to} R(I_C)$ is the lax monoidal unit. Therefore by the axioms on monoidal Quillen adjunctions its adjunct $\chi_I$ is a weak equivalence.

Now the strategy is to proceed from here by induction over the cells of the [[cell object]] of which every cofibrant monoid is, by assumption, a retract.

(...)

=--


+-- {: .un_lemma #AnotherTechnicalLemma}
###### Lemma

If $U_C$ [creates](#CreatedModelStructure) the model structure on $Mon(C)$ and the unit in $C$ is cofibrant,  then a cofibrant $C$-monoid is also cofibrant as an object in $C$.

=--

This is a special case of lemma 6.2 in ([SchwedeShipleyAlgebras](#SchwedeShipleyAlgebras))

+-- {: .proof}
###### Proof 

(...)

=--


+-- {: .proof}
###### Proof of the theorem

First notice that since by assumption the model structure on $Mon(D)$ is [created](#CreatedModelStructure) by $U_D$ it follows by definition that the cofibrant $B$ is a [[retract]] of a [[cell object]] in $Mon(D)$. Then the [above lemma](#OneTechnicalLemma) asserts that

$$
  \chi_B : L B \to L^{mon} B
$$

is a weak equivalence. 


To prove the theorem, we have to show for every cofibrant $B \in Mon(D)$  and fibrant $Y \in Mon(C)$ that a morphism $B \to R Y$ is a weak equivalence in $Mon(D)$ (hence its underlying morphism in $D$) precisely if its adjunct $L^{mon} B \to Y$ is a weak equivalence in $Mon(C)$ (hence its underlying morphism in $C$).

By definition of adjunct we have that 

$$
 (B \to R Y) = ( B \to R L^{mon} B  \to R Y)
 \,.
$$

By the [second lemma above](#AnotherTechnicalLemma) we have that $B$ is cofibrant also in $C$. Therefore, since $(L \dashv R)$ is a Quillen equivalence between $C$ and $D$, the right hand is a weak equivalence precisely if its $(L \dashv R)$-adjunct

$$
  L B \stackrel{\chi_B}{\to} L^{mon} B \to Y
$$ 
 
is a weak equivalence in $D$. But since $\chi_B$ is a weak equivalence, this is the case precisely if $L^{mon}B \to Y$ is a weak equivalence.

=--


## Examples

Examples arise in the [[monoidal Dold-Kan correspondence]]. See there for details.


## Related concepts

* [[Quillen adjunction]]

* [[simplicial Quillen adjunction]]

* [[Quillen equivalence]]

* **monoidal Quillen adjunction**



## References

The notion of strong monoidal Quillen adjunction is def. 4.2.16 in 

* [[Mark Hovey]], _Model categories_

The lax monoidal version is considered as definition 3.6 of 

* [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342))
{#SchwedeShipley}

Some of the facts mentioned above are from

* [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf)) 
{#SchwedeShipleyAlgebras}

[[!redirects monoidal Quillen adjunctions]]

[[!redirects monoidal Quillen equivalence]]
[[!redirects monoidal Quillen equivalences]]
