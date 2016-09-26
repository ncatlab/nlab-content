

#Contents#
* table of contents
{:toc}


## Idea ##
There are several different concepts of [[tensor products]] for [[C-star algebras]], because there are different norms one can put on the algebraic tensor product that turns it into a [[C-star algebra]]. The spatial tensor product uses the smallest norm of all possible norms. There is also a maximal norm and it is a nontrivial theorem that all norms fall in between these two.

If $A$ is a [[C-star-algebra]] it may happen that for every other [[C-star-algebra]] $B$, the maximal and minimal tensor norms on the algebraic tensor product $A\otimes B$ coincide, forcing the $*$-algebra $A\otimes B$ to have a **unique** C-star norm. Such an $A$ is said to be [[nuclear C*-algebra|nuclear]].


## Definition ##
Let $\mathcal{A}_1, ..., \mathcal{A}_k$ be unital $C^*$-algebras faithfully represented on the [[Hilbert spaces]] $H_1, ..., H_k$. Let $H$ be the tensor product of these Hilbert spaces,
$$
H := \otimes_{i=1}^k H_k 
$$
The set of operators of finite sums of $A_1 \otimes ... \otimes_k A_k$ form a $*$-subalgebra of $\mathcal{B}(H)$. The norm closure of this set is the **spatial tensor product** of the given $C^*$-algbras, and is sometimes denoted by $A_1\otimes_{min} \dots \otimes_{min} A_k$.

Remark: The spatial tensor product does not depend on the chosen faithful representations, see references.

## Properties ##
+-- {: .un_theorem}
###### Theorem

**states extend to the spatial tensor product**

Let $\rho_1, ..., \rho_k$ be states on the unitary $C^*$-algebras. Then there is a unique state $\rho$ on the spatial tensor product such that
$$
\rho(A_1 \otimes ... \otimes_k A_k) = \rho_1(A_1) \cdots \rho_k(A_k)
$$
=--


The spatial tensor product is injective, in the sense of Grothendieck's approach to tensor norms, but in general it is not projective.

In the category of operator spaces and completely contractive linear maps (completely short in nLab terminology?), one can introduce the projective tensor product and the injective tensor product in analogy with Grothendieck's definitions for the category of Banach spaces and short linear maps. Then if $A$ and $B$ are $C^*$-algebras, the injective tensor product of their underlying operator spaces is canonically isomorphic to the underlying operator space of $A\otimes_{min} B$.


## References ##

Appendix T in the book

* Niels Erik Wegge-Olsen: _K-theory and $C^*$-algebras: a friendly approach._ ([ZMATH](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0780.46038&format=complete))


[[!redirects Creating spatial tensors]]

[[!redirects tensor product of C*-algebras]]
[[!redirects tensor product of C-star-algebras]]
[[!redirects tensor products of C*-algebras]]
[[!redirects tensor products of C-star-algebras]]
