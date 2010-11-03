
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

## Properties

### Recognition of monoidal Quillen adjunctions {#Recognition}

+-- {: .un_theorem}
###### Theorem

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a [[Quillen adjunction]] between [[monoidal model categories]] and let $R$ be equipped with the strcuture of a [[lax monoidal functor]].

Then the following two conditions are sufficient for $(L \dashv R)$ to be a lax monoidal Quillen adjunction:

1. for some (hence any) cofibrant [[resolution]] $q : \hat I_D \stackrel{\simeq}{\to} D$ of the unit object in $D$, the composite morphism

   $$
     L(\hat I_D) \stackrel{L(q)}{\to} L(I_D) \stackrel{\tilde i}{\to} I_C
   $$

   is a weak equivalence, (wher $\tilde i$ is the [[adjunct]] of $i : I_D \to R(I_C)$);

1. the unit object $I_D$ _detects weak equivalences_ in that for every weak equivalence $f : X \to Y$ between fibrant objects the morphism $D^{\Delta^{op}}(Q I_D, f)$ of [[hom-object]]s in the category of [[simplicial object]]s in $D$ is an equivalence of Kan complexes, for $Q I_D$ a cofibrant resolution in the [[Reedy model structure]] $D^{\Delta^{op}}_{Reedy}$. 

=--

This is proposition 3.16 in ([SchwedeShipley](#SchwedeShipley)).



Let $C$ and $D$ be [[monoidal model categories]] such that on their categories of [[monoid]]s exists the corresponding [[transferred model structure]], transferred along the [[stuff, structure, property|forgetful]]/[[free functor]] adjunction 

$$
  (F_C \dashv U_C) : Mon(C) \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  C
  \,.
$$

### Lift to Quillen adjunctions on monoids {#LiftToMonoids}

+-- {: .un_theorem}
###### Theorem

If $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ is a lax monoidal Quillen adjunction and the forgetful functors induce transferred model structures on monoids, then there is an induced [[Quillen adjunction]]

$$
  (L^{mon} \dashv R) 
  : 
  Mon(C) \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} Mon(D)
  \,,
$$

where the functor underlying the [[right adjoint]] is the original $R$. 


The left adjoint $L^{mon}$ is the functor given by the [[coequalizer]]

$$
  L^{mon} : B 
    \mapsto 
   \lim_{\to}
  (F_D L F_C B \stackrel{\to}{\to} F_D L B)
$$

of the following two morphisms (...)

=--

This is theorem 3.12 in ([SchwedeShipley](#SchwedeShipley)).

## Examples

Examples arise in the [[monoidal Dold-Kan correspondence]]. See there for details.


## Related concepts

* [[Quillen adjunction]]

* [[Quillen equivalence]]

* **monoidal Quillen adjunction**



## References

The notion of strong monoidal Quillen adjunction is def. 4.2.16 in 

* Hovey, _Model categories_

The lax monoidal version is considered as definition 3.6 of 

* [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342))
{#SchwedeShipley}
