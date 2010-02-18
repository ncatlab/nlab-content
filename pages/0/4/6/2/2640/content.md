#Contents#
* automatic table of contents
{:toc}

## Definition

A _bisimplicial object_ in a [[category]] $C$ is a [[functor]]

$$
  F : \Delta^{op} \times \Delta^{op} \to C
$$

where $\Delta$ is the [[simplex category]].

This is the same as a [[simplicial object]] in the [[category]] of [[simplicial object]]s in $C$.

#Special cases#

## Bisimplicial sets 

### Definition

A bisimplicial set is a bisimplicial object in [[Set]].

### Properties

+-- {: .un_prop }
###### Proposition
**(degreewise weak equivalences)**

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

+-- {: .un_def }
###### Definition
**(diagonal)**

For $X_{\bulet,\bullet}$ a bisimplicial set, its **diagonal** is the simplicial set that this the precomposition with $(Id, Id) : \Delta^{op} \to \Delta^{op} \times \Delta^{op}$, i.e. the simplicial set with components.

$$
  d(X)_n = X_{n,n}
  \,.
$$

=--


+-- {: .un_def }
###### Definition
**(realization)**

The **realization** $|X|$ of a bisimplicial set $X_{\bullet,\bullet}$ is the [[simplicial set]] that is given by the [[coend]]

$$
  |X| =  \int^{[n] \in \Delta} X_{n,\bullet} \times \Delta[n]_\bullet
$$

in [[sSet]].

=--

+-- {: .un_def }
###### Definition
**(diagonal is realization)**

For $X$ a bisimplicial set, its diagonal $d(X)$ is (isomorphic to) its realization $|X|$:

$$
  |X| \simeq d(X)
  \,.
$$


=--

+-- {: .proof}
###### Proof

This is exercise 1.6 in  in [chaper 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* Goerss-Jardine, _Simplicial Homotopy Theory_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html)) 


=--



## Bisimplicial abelian groups 


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
[[!redirects bisimplicial set]]
