
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


# Linear combinations
* table of contents
{: toc}

## Idea

Linear combinations are the most general operations in the [[operads]] for [[modules]] over a [[rig]] (including modules over a [[ring]] and [[vector spaces]] over a [[field]]).


## Definition

Let $R$ be a rig, and let $V$ be a (left) $R$-module.  By 'scalar', we mean an element of $R$; by 'vector', we mean an element of $V$.  Given any [[natural number]] $n$ and any $n$-[[tuple]] $(a_1,\ldots,a_n)$ of scalars (so in short, given a [[finite list]] of scalars), we have an $n$-ary operation on $V$ that maps $(x_1,\ldots,x_n)$ to
$$ a_1 x_1 + \cdots + a_n x_n .$$
The result of this operation is the __linear combination__ of the vectors $x_1$ through $x_n$ with respective __[[coefficients]]__ $a_1$ through $a_n$.

Variations:  If $R$ is a non-unital rig (or more generally if $M$ is a non-unital module), then a linear combination may also have a term $x_0$ with no coefficient.  If $R$ is non-associative (or more generally if $M$ is a non-associative module), then the term with $x_i$ takes the form
$$ a_{i,1} (a_{i,2} \cdots (a_{i,i_m} x_i){\cdots})) .$$
If $R$ is non-commutative and $V$ is a right $R$-module, the term with $x_i$ takes the form $x_i a_i$.  If $V$ is an $R$-$S$-[[bimodule]], then the term with $x_i$ takes the form $a_i x_i b_i$, with $a_i\colon R$ and $b_i\colon S$.  Of course, all of these variations may be combined.

Given a [[subset]] $G$ of (the [[underlying set]] of) $V$, the set of all linear combinations of the vectors in $G$ is a [[submodule]] of $V$, the __$R$-linear span__ of $G$.

More abstractly, by the [[adjunction]] between the underlying-set functor and the [[free functor]], the subset inclusion
$$ i_G\colon G \to {|V|} $$
corresponds to a [[homomorphism]]
$$ \hat{i}_G\colon R[G] \to V .$$
Then the $R$-linear span of $G$ is the image of the homomorphism $\hat{i}_G$. 

This abstract definition works more generally for any set function $f : G \to {|V|}$. The $R$-linear span of the image of $f$ in $V$ is the image of its corresponding homomorphism $\hat{f} \colon R[G] \to V$.   


## Examples

Every operation on the module $V$ is a linear combination:

*  The [[identity operation]] is the linear combination of arity $1$ with coefficient $1$.

*  Addition is the linear combination of arity $2$ with coefficients $(1,1)$, and the zero element is the linear combination of arity $0$ (with no coefficients).

*  Scalar multiplication by the scalar $a$ is the linear combination of arity $1$ with coefficient $a$.

*  If $R$ is a ring (so $-1$ is a scalar), then subtraction is the linear combination of arity $2$ with coefficients $(1,-1)$, and the additive inverse is the linear combination of arity $1$ with coefficient $-1$.

*  If $R$ is [[divisible group|divisible]] (so $1/n$ is a scalar for every [[positive integer]] $n$), then the [[mean]] of $n$ vectors is the linear combination of arity $n$ with every coefficient $1/n$.


## Special cases

An __[[affine linear combination]]__ is a linear combination whose coefficients sum to $1$.  These are the operations in an [[affine space]].

If $R$ is [[ordered ring|ordered]], then a __[[conical linear combination]]__ is a linear combination whose coefficients are all positive, and a __[[convex linear combination]]__ an affine conical linear combination.  These are the operations in (respectively) a [[conical space]] and a [[convex space]].

## References

* {#Lawvere92} [[William Lawvere]], pp. 33 of: *Introduction to Linear Categories and Applications*, course lecture notes (1992) &lbrack;[pdf](https://github.com/mattearnshaw/lawvere/blob/192dac273e8bf352f307f87b9ec4fe8ef7dc85b9/pdfs/1992-introduction-to-linear-categories-and-applications.pdf), [[Lawvere-LinearCategories.pdf:file]]&rbrack;




[[!redirects linear combination]]
[[!redirects linear combinations]]

[[!redirects linear span]]
[[!redirects linear spans]]
