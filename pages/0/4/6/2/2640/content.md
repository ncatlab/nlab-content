#Definition#

A _bisimplicial object_ in a [[category]] $C$ is a [[functor]]

$$
  F : \Delta^{op} \times \Delta^{op} \to C
$$

See [[simplicial object]].

#Properties#


**proposition**

Let $X,Y : \Delta^{op} \times \Delta^{op} \to Set$ be bisimplicial sets.
A morphism $f : X \to Y$ which is degreewise in one argument a weak equivalence
$f_{n,\bullet} : X(n,\bullet) \to Y(n,\bullet)$ induces a weak equivalence 
$d(f) : d(X) \to d(Y)$ of the associated diagonal simplicial sets
(with respect to the standard [[model structure on simplicial sets]]s).

**proof** 

Prop 1.9 in section 4 of 

+ Goerss-Jardine, _Simplicial Homotopy Theory_ ([dvi](...)) 



**proposition**

Let $A,B : \Delta^{op} \times \Delta^{op} \to Ab$ be bisimplicial abelian groups.
A morphism $f : A \to B$ which is degreewise in one argument a weak equivalence
$f_{n,\bullet} : A(n,\bullet) \to B(n,\bullet)$ induces a weak equivalence 
$d(f) : d(A) \to d(B)$ of the associated diagonal complexes.

**proof** 

Lemma 2.7 in section 4 of 

+ Goerss-Jardine, _Simplicial Homotopy Theory_ ([dvi](...)) 

[[!redirects bisimplicial group]]