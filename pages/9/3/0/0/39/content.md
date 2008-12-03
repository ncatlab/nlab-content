+-- {: .un_defn}
###### Definition
**(quasi-free differential graded-commutative algebras)**

A _quasi-free differential graded commutative algebra_
(**qDGCA**) is an algebra of smooth functions $A := C^\infty(X)$ on a manifold $X$ together with a degree +1 graded derivation $d$ on the free (over $A$) graded-(anti-)commutative algebra
$
  \wedge^\bullet_A g^* = S^\bullet_A g^*[1]
$
on the dual (over $A$) of a non-positively graded cochain complex $g$ of $A$-modules, such that $d^2 = 0$.
=--

+-- {: .un_defn}
###### Definition
**($L_\infty$-algebroids)**

$L_\infty$-algebroids are by definition the objects dual to qDGCAs. We address the qDGCA corresponding to an $L_\infty$-algebroid $\mathfrak{g}$ as the Chevalley-Eilenberg algebra of $\mathfrak{g}$ and write
$$
  L_\infty Algebroids \stackrel{CE(-)}{\to} qDGCAs 
$$
for the defining contravariant functor.
=--

#Remarks#

* Compare with the discussion of plain [[Lie algebroid|Lie algebroids]].

* Usually one will want to impose the condition that the modules involves are finitely generated and projective. In that case qDGCAs are equivalent to [[NQ-supermanifold]]s.


#Literature# 

This notion originates at or somewhere around

* Pavol &#352;evera, _Some title containing the words "homotopy" and "symplectic", e.g. this one_, ([arXiv](http://arxiv.org/abs/math.SG/0105080)).

The above follows 

* Hisham Sati, Urs Schreiber, Jim Stasheff, _$L_\infty$-algebra connections and applications_ ([arXiv](http://arxiv.org/abs/0801.3480), [blog](http://golem.ph.utexas.edu/category/2007/12/lie_ooconnections_and_their_ap_1.html)).

More discussion along these lines is in Urs Schreiber's private area part of the $n$Lab, at [[Schreiber:Lie theory]].