<div class="rightHandSide toc">
[[!include homotopy - contents]]
</div>

#Conetnts#

* automatic table of contents goes here
{:toc}

#Idea#

Given a [[site]] $C$ equipped with an [[interval object]] ${*}\amalg {*} \stackrel{[i_0, i_1]}{\to}I$ the **homotopy localization** of an [[(∞,1)-category of (∞,1)-sheaves]] $Sh_\infty(C)$ on $C$ is the [[localization of an (∞,1)-category|(∞,1)-categorical localization]] of $Sh_\infty(C)$ at the morphisms of the form

$$
  X \stackrel{Id \times i_0}{\to} X \times I
  \,.
$$

+--{: .query}
[[David Roberts]]: From what I understand of the work on $A^1$ homotopy, the localisation is of morphisms of the form $X \times I \to X$.

[[Urs Schreiber]]: but should that make a difference?

=--


#Examples#

* Taking $C =$ [[Top]] and the [[interval object]] $I$ to be the standard topological interval $I = [0,1]$, the homotopy localization of $\infty$-stacks on $Top$ is equivalent to the [[(∞,1)-category]] [[Top]] itself again. This is discussed in 
  
  * Dan Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://math.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))
 
* Taking $C = $ $Sch/S$ the category of [[scheme]]s over a [[Noetherian scheme]] $S$ and taking $I = \mathbb{A}^1$ the [[affine line]], the study of the corresponding homotopy localization is called [[A1 homotopy theory]].