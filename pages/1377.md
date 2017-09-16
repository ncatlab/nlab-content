## Idea ##

A _lax 2-adjunction_ is an [[adjunction]] 'up to adjointness'.  A
1-categorical adjunction is given by a natural isomorphism of hom sets

$$\phi_{A,B} : D(F A,B) \cong C(A,G B)$$

and a strict 2-adjunction is where $C,D$ are 2-categories, $F,G$ are
2-functors, and $\phi$ is an isomorphism of hom categories.  A _lax_
2-adjunction is given by a (suitably natural) pair of functors

$$\hat\phi_{A,B} : D(F A,B) \overset{\to}{\leftarrow} C(A,G B) :
\check\phi_{A,B} $$

such that $\check\phi\dashv\hat\phi$.

## Definition ##

Just as the notion of [[adjunction]] makes sense not just in $Cat$ but
in any 2-category, lax 2-adjunctions can be defined in any 3-category
when the above is suitably internalized.  So, given 0-cells $C,D$ and
1-cells $F:C\to D$, $G:D\to C$ in any 3-category, we say $F$ is lax
left adjoint to $G$ if we have

* 2-cells $\eta:C\Rightarrow G F$ and $\epsilon:F G \Rightarrow D$, and

* instead of strict triangle equalities, 3-cells (called _triangulators_)
  $s,t$

  <center markdown="1">[[lax-adj-mdfs.png:pic]]</center>

  satisfying the _swallowtail identities_:

  <center markdown="1">[[lax-adj-swlwtl-eta.png:pic]]</center>

  and

  <center markdown="1">[[lax-adj-swlwtl-eps.png:pic]]</center>

## Sources ##

This idea was introduced in Gray's [[Gray-adjointness-for-2-categories|book]] under the name of _transcendental quasi-adjunction_.