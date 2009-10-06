
#Idea#

In the axiomatic formulation of [[differential geometry]] given by [[synthetic differential geometry]] the standard [[Kock-Lawvere axiom]] provides a notion of [[differentiation]]. In general this need not come with an inverse operation of [[integration]]. The additional _integration axiom_ on a [[smooth topos]] does ensure this.

# Definition #

+-- {: .un_defn}
###### Definition
**(integration axiom)**

Let $(\mathcal{T}, R)$ be a [[smooth topos]] and let the line object $R$ be equipped with the structure of a [[partial order]] $(R, \leq)$ compatible with its [[ring]] structure $(R, +, \cdot)$ in the obvious way.

Then for any  $a, b\in R$ write

$$
  [a,b] := \{x \in R | a \leq x \leq b\}
$$

We say that $(\mathcal{T},(R,+,\cdot,\leq))$ satisfies the **integration axiom** if for all such intervals, all functions on the interval arise uniquely as derivatives on functions on the interval that vanish at the left boundary:

$$
  \forall f \in R^{[a,b]} : \exists ! \int_a^{-} f \in R^{[a,b]} :
  (\int_a^{-} f)(0) = 0 \wedge (\int_a^{-} f)' = f
  \,.
$$


=--


> ... need to say more ...

# Examples #

The axiom holds for all the [[smooth topos]] presented in [[Models for Smooth Infinitesimal Analysis|MSIA]], listed in appendix 2 there. See appendix 3 for the proof.


#References#

page 49 of 

* [[Anders Kock]], _Synthtic differential geometry_ ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

appendix 3 of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]]