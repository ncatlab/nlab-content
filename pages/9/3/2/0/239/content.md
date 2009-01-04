#Idea#

* In its original sense the _tensor_ product of two objects on which a third object acts is the quotient of their product by this [[action]].

+--{.query}
Urs, why do you say that this is the *original* sense? (By the way, I see now how what you first wrote here *does* cover the case of $\Ab$ without circularity.) &#8212;Toby

I would argue that the multicategorical version (a tensor product is a representing object for multilinear maps) is more "original," since as I noted below the case of $Ab$ cannot actually be viewed as a quotient of some pre-existing product.  Actually, historically speaking my guess would be that the most "original" notion of tensor product is as a left adjoint to an internal hom, but don't quote me on that.  --[[Mike Shulman|Mike]]
=--

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

In general, $N_1\otimes_A N_2$ will no longer be an $A$-module of any sort, unless $A$ is a _commutative_ monoid (in which case left and right modules are the same).  This makes the category of modules over a commutative monoid in a symmetric monoidal category into a symmetric monoidal category itself.

##Examples##

**Tensor product of ring modules** Let the ambient category be the category [[Ab]] of abelian groups with the monoidal structure described above. Any [[ring]] $R$ is a monoid in [[Ab]] and any two (right, left) modules $N_R$, ${}_R M$ over this ring are (right, left) modules in [[Ab]] over this monoid. The tensor product

$$
  N \otimes_R M
$$

of $N$ with $M$ over $R$ is the abelian group whose underlying set is the quotient of the tensor product of abelian groups by the equivalence relation $(n \cdot r, m) \sim (n, r \cdot m)$ for all $n\in N$, $m \in M$, $r \in R$.

**Tensor product of vector spaces**
The probably most familiar case of a tensor product is that of vector spaces, which is also probably the situation where the concept was first conceived. Noticing that a vector space is an abelian group which is a [[module]] over a [[ring]] that happens to be a [[field]], the tensor product of vector spaces is a special case of the tensor product of ring modules described above.


##Non-example##

**Tensor product of abelian groups.** If $A$ and $B$ are abelian groups, their tensor product $A\otimes B$ is obtained by

1. starting with their cartesian product $A\times B$ as sets,
1. generating a _free_ abelian group from it, and then
1. quotienting by relations $(a_1,b)+(a_2,b)\sim (a_1+a_2,b)$ and $(a,b_1)+(a,b_2)\sim (a,b_1+b_2)$.  (The 0-ary relations $(0,b)\sim 0$ and $(a,0)\sim 0$ follow automatically.)

Note that $A\otimes B$ is not a subobject _or_ a quotient of the cartesian product $A\times B$.  Therefore, this is not the tensor product of modules over any monoid in the cartesian monoidal category [[Set]].  Abelian groups _can_ be considered as "sets with an action by something," but that something is more complicated than a monoid: it is a special sort of [[monad]] called a [[commutative theory]].


#Tensor product in a multicategory#

If $M$ is a [[multicategory]] and $A$ and $B$ are objects in $M$, then the _tensor product_ $A \otimes B$ is defined to be an object equipped with a [[universal construction|universal]] multimorphism from $A$ and $B$ to $A \otimes B$. Thus, any multimorphism from $A$ and $B$ to $C$ defines a morphism from $A \otimes B$ to $C$ (and conversely).

For example, if $M$ is the category [[Ab]] of abelian groups, made into a multicategory using multilinear maps as the multimorphisms, then we get the usual tensor product of abelian groups. That is, $A \otimes B$ is equipped with a universal map from $A \times B$ (as a set) to $C$ such that this map is linear (a group homomorphism) in each argument separately.  The same idea works for modules over rings and for vector spaces.

Many other tensor products arise in this way as well.  For example, the [[Gray tensor product]] of [[strict 2-categories]] can also be described as an object equipped with a universal multimorphism in some multicategory.


#Tensor product in a bicategory#

The tensor product of modules for a monoid in a monoidal category is easily extended to a tensor product of modules for a [[monad]] in a [[bicategory]].

For example, consider the bicategory $V-Mat$ of $V$-valued matrices for some monoidal category $V$.  A monad in $V-Mat$ is a $V$-[[enriched category]] $A$, an $(A,I)$-bimodule is a functor $A\to V$, an $(I,A)$-bimodule is a functor $A^{op}\to V$, and their tensor product in $V-Mat$ is a classical construction called the **tensor product of functors**.  It can also be computed as a [[end|coend]].
