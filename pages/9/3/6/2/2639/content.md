#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The [[Dold-Kan correspondence]] relates [[simplicial group]]s to [[chain complex]]es. The Eilenberg-Zilber theorem says how in this context [[double complex]]es and their [[total complex]]es relate to [[bisimplicial group]]s and their [[diagonal of a bisimplicial set|diagonals]].

#Statement#

Let $A : \Delta^{op} \times \Delta^{op} \to Ab$ be a [[bisimplicial object|bisimplicial abelian group]]. Write 

* $C diag A$ for the [[Moore complex]] of its diagonal simplicial group $diag A : \Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{A}{\to} Ab$;

* $Tot (C A)$ for the [[total complex]] of the [[double complex]] obtained by applying the [[Moore complex]] functor on both arguments of $A$.

+-- {: .un_theorem }
###### Theorem
**(Dold-Puppe generalization of Eilenberg-Zilber)**

There is a [[quasi-isomorphism]] (even a chain-homotopy equivalence)

$$
  C diag A \stackrel{\simeq}{\to} Tot (C A)
  \,.
$$

=--



#References#

A weak version of the statement is in theorem 8.1.5 in 

* Weibel, _An introduction to homological algebra_

The stronger version as stated above is in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* Goerss-Jardine, _Simplicial homotopy theory_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))