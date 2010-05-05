#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The [[Dold-Kan correspondence]] relates [[simplicial group]]s to [[chain complex]]es. The Eilenberg-Zilber theorem says how in this context [[double complex]]es and their [[total complex]]es relate to [[bisimplicial group]]s and their [[diagonal of a bisimplicial set|diagonals]].

Analogously there is also a version of the theorem for bi-cosimplicial abelian groups.

## Statement

### Simplicial version

Let $A : \Delta^{op} \times \Delta^{op} \to Ab$ be a [[bisimplicial object|bisimplicial abelian group]]. Write 

* $C Diag A$ for the [[Moore complex]] of its diagonal simplicial group $Diag A : \Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{A}{\to} Ab$;

* $Tot (C A)$ for the [[total complex]] of the [[double complex]] obtained by applying the [[Moore complex]] functor on both arguments of $A$.

+-- {: .un_theorem }
###### Theorem
**(Dold-Puppe generalization of Eilenberg-Zilber)**

There is a [[quasi-isomorphism]] (even a chain-homotopy equivalence)

$$
  C Diag (A) \stackrel{\simeq}{\to} Tot C (A)
  \,.
$$

=--

+-- {: .un_remark}
###### Remark


Notice (see the discussion at [[bisimplicial set]]) that the diagonal simplicial set is isomorphic to the realization 

$$
  Diag F_{\bullet,\bullet} 
  \simeq 
   \int^{[n] \in \Delta} \Delta^n \cdot F_{n,\bullet}
  \,.
$$

=--


### Cosimplicial version


Let $A : \Delta \times \Delta \to Ab$ be a bi-cosimplicial abelian group. And let $C : Ab^\Delta \to Ch^\bullet$ the Moore cochain complex functor. Write $C(A)$ for the [[double complex]] obtained by applying $C$ to each of the two cosimplicial directions. Then we have natural isomorphisms in cohomology

+-- {: .un_theorem }
###### Theorem

There is a [[natural isomorphism]]

$$
  H^\bullet C Diag(A)
  \simeq
  H^\bullet Tot C(A)
$$ 

=--

## References

A weak version of the simplicial statement is in theorem 8.1.5 in 

* [[Charles Weibel]], _An introduction to homological algebra_

The stronger version as stated above is in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* Goerss-Jardine, _Simplicial homotopy theory_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

The cosimplicial version of the theorem appears as theorem A.3 in

* L. Grunenfelder and M. Mastnak, _Cohomology of abelian matched pairs and the Kac sequence_ ([arXiv:math/0212124](http://arxiv.org/abs/math/0212124))