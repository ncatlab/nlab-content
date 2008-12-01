+-- {: .un_defn}
###### Definition
**(quasi-free differential graded-commutative algebras)**

A _quasi-free differential graded commutative algebra_
(**qDGCA**) is an algebra of smooth functions $A := C^\infty(X)$ on a manifold $X$ together with a degree +1 graded derivation $d$ on the free (over $A$) graded-(anti-)commutative algebra
$
  \wedge^\bullet g^* = S^\bullet g^*[1]
$
on the dual (over $A$) of a non-positively graded cochain complex $g$ of $A$-modules, such that $d^2 = 0$.

A morphism of qDGCAs is a linear map of the underlying graded-(anti-)commuting algebras respecting the differential.
=--

Notice that the first few terms of $\wedge^\bullet g^*$ in degree 0, 1 and 2, respectively, are
$$
  \wedge^\bullet g^*
  =
  A \oplus g_0^*[1] \oplus  (g_0^*[1]\wedge g_0^*[1])
  \oplus g_{-1}^*[1] \oplus \cdots
  \,.
$$

**Remark:** There is plenty of room to fuss about the grading conventions. 

**Remark:** Usually one requires the module $g$ to be projective and of finite rank. In this case $g$ is the module of sections of a $\mathbb{N}$-graded vector bundle on $X$ and the above definition becomes equivalent to that of an [[NQ-supermanifold]].

+-- {: .un_defn}
###### Definition
**($L_\infty$-algebroids)**

$L_\infty$-algebroids are the objects dual to 
qDGCAs.
=--

We write 
$$
  L_\infty Algebroids \stackrel{CE(-)}{\to} qDGCAs
$$
for the corresponding contravariant functor and address the qDGCA $CE(g) := (\wedge^\bullet g^*, d)$ as the (generalized) [[Chevalley-Eilenberg algebra]] of $g$.
