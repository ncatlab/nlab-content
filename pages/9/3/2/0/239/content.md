#Idea#

* In its original sense the _tensor_ product of two objects on which a third object acts is the quotient of their product by this [[action]].

* This notion has various _generalizations_, which often go by the same name:

  * there is a notion of tensor product in any [[multicategory]];

  * the functor $\otimes : C \times C \to C$ which is part of the data of a [[monoidal category]] $C$ is called a _tensor product_. In parts of the literature (certain) abelian categories are even addressed as _tensor categories_. 

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

##Examples##

**Tensor product of abelian groups.** Let $C$ be the monoidal category [[Set]] of sets, with monoidal structure given by the cartesian product of sets. The additive group of integers $\mathbb{Z}$ is a monoid, hence a monoid in $Sets$. An abelian group $A$ is a module over this monoid. The tensor product

$$
  A \otimes B
  \subset A \times B
$$

of two abelian groups (over $\mathbb{Z}$) is, as a set, the set of pairs $(a,b) \in A \times B$ modulo the equivalence relation $(n \cdot a, b) \sim (a, n \cdot b)$ for all $n \in \mathbb{Z}$.

The category [[Ab]] of abelian groups becomes a monoidal category with this tensor product giving the monoidal structure. 

**Tensor product of ring modules** Let the ambient category be the category [[Ab]] of abelian groups with the monoidal structure described above. Any [[ring]] $R$ is a monoid in [[Ab]] and any two (right, left) modules $N_R$, ${}_R M$ over this ring are (right, left) modules in [[Ab]] over this monoid. The tensor product

$$
  N \otimes_R M
$$

of $N$ with $M$ over $R$ is the abelian group whose underlying set is the quotient of the tensor product of abelian groups by the equivalence relation $(n \cdot r, m) \sim (n, r \cdot m)$ for all $n\in N$, $m \in M$, $r \in R$.

**Tensor product of vector spaces**
The probably most familiar case of a tensor product is that of vector spaces, which is also probably the situation where the concept was first conceived. Noticing that a vector space is an abelian group which is a [[module]] over a [[ring]] that happens to be a [[field]], the tensor product of vector spaces is a special case of the tensor product of ring modules described above.



#Tensor product in a multicategory#

If $M$ is a [[multicategory]] and $A$ and $B$ are objects in $M$, then the _tensor product_ $A \otimes B$ is defined to be an object equipped with a [[universal construction|universal]] multimorphism from $A$ and $B$ to $A \otimes B$. Thus, any multimorphism from $A$ and $B$ to $C$ defines a morphism from $A \otimes B$ to $C$ (and conversely).

For example, if $M$ is the category [[Ab]] of abelian groups, made into a multicategory using multilinear maps as the multimorphisms, then we get the usual tensor product of abelian groups. That is, $A \otimes B$ is equipped with a universal map from $A \times B$ (as a set) to $C$ such that this map is linear (a group homomorphism) in each argument separately.

