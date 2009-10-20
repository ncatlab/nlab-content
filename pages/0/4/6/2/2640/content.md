#Contents#
* automatic table of contents
{:toc}

#Definition#

A _bisimplicial object_ in a [[category]] $C$ is a [[functor]]

$$
  F : \Delta^{op} \times \Delta^{op} \to C
$$

where $\Delta$ is the [[simplex category]].

This is the same as a [[simplicial object]] in the [[category]] of [[simplicial object]]s in $C$.

#Special cases#

## bisimplicial sets ##

+-- {: .un_prop }
###### Proposition

Let $X,Y : \Delta^{op} \times \Delta^{op} \to Set$ be bisimplicial sets.
A morphism $f : X \to Y$ which is degreewise in one argument a weak equivalence
$f_{n,\bullet} : X(n,\bullet) \to Y(n,\bullet)$ induces a weak equivalence 
$d(f) : d(X) \to d(Y)$ of the associated diagonal simplicial sets
(with respect to the standard [[model structure on simplicial sets]]s).

=--


+-- {: .proof}
###### Proof

This is prop 1.9 in [chaper 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* Goerss-Jardine, _Simplicial Homotopy Theory_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html)) 

=--

## bisimplicial abelian groups ##


+-- {: .un_prop }
###### Proposition

Let $A,B : \Delta^{op} \times \Delta^{op} \to Ab$ be bisimplicial abelian groups.
A morphism $f : A \to B$ which is degreewise in one argument a weak equivalence
$f_{n,\bullet} : A(n,\bullet) \to B(n,\bullet)$ induces a weak equivalence 
$d(f) : d(A) \to d(B)$ of the associated diagonal complexes.

=--


+-- {: .proof}
###### Proof

This is Lemma 2.7 in [chaper 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* Goerss-Jardine, _Simplicial Homotopy Theory_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html)) 

=--

[[!redirects bisimplicial group]]