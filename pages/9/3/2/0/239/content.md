In general, a **tensor product** is the operation in a [[monoidal category]]. But many common tensor products may be derived from other structures.

#Tensor product in a multicategory#

If $M$ is a [[multicategory]] and $A$ and $B$ are objects in $M$, then the _tensor product_ $A \otimes B$ is defined to be an object equipped with a [[universal construction|universal]] multimorphism from $A$ and $B$ to $A \otimes B$. Thus, any multimorphism from $A$ and $B$ to $C$ defines a morphism from $A \otimes B$ to $C$ (and conversely).

For example, if $M$ is the category [[Ab]] of abelian groups, made into a multicategory using multilinear maps as the multimorphisms, then we get the usual tensor product of abelian groups. That is, $A \otimes B$ is equipped with a universal map from $A \times B$ (as a set) to $C$ such that this map is linear (a group homomorphism) in each argument separately.

#Tensor product of modules#

Let $A$ be a [[monoid]] in some monoidal category $(C,\otimes)$ and let $N_1$ be a right [[module]] over $A$ and $N_2$ a left module. Then the _tensor product_

$$
  N_1 \otimes_A N_2
$$

is the [[coequalizer]] of

$$
  N_1 \otimes A \otimes N_2
  \stackrel{\to}{\to}
  N_1 \otimes N_2
$$

where the two maps are given by the right action on $N_1$ and the left action on $N_2$, respectively.