An $A_\infty$-algebra is an algebra for the cofibrant resolution of the [[operad]] $Ass$ of associative algebras: it is an algebra which is associative only up to higher coherent homotopy.

Concretely, an $A_\infty$-algebra is the structure of a degree 1 coderivation 

$$
  D : T V \to T V
$$

on the free tensor coalgebra $T V$ over a graded vector space $V$ (the coproduct is the _unshuffle_ product) such that 
$$
  D^2 = 0
  \,.
$$

Coderivations on free coalgebras are entirely determined by their "value on cogenerators", which allows to decompose

$$
  D = D_0 + D_1 + D_2 + D_3 + \cdots
$$

with each $D_k$ specified entirely by its action

$$
  D_k : V^{\otimes k} \to V
  \,.
$$

Then:

* $D_2 : V^{\otimes 2} \to V$ is the _product_ in the algebra;

* $D_3 : V^{\otimes 3}$ is the _associator_ which measures the failure of $D_2$ to be associative;

* $D_4 : V^{\otimes 4} \to V$ is the _pentagonator_ (or so) which measures the failure of $D_3$ to satisfy the pentagon identity;

* and so on.


#Remarks#

* See also [[L-infinity algebra]].

#References#

* B. Keller, _A brief introduction to $A_\infty$-algebras_ ([pdf](http://people.math.jussieu.fr/~keller/publ/IntroAinfEdinb.pdf))