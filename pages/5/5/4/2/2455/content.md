
> There is also a distinct notion of an [[universal enveloping algebra|enveloping algebra of a Lie algebra]].

***

# Contents
* table of contents
{: toc}

## Definition

Given a [[monoid]] $A$ with multiplication $\mu$ in a [[symmetric monoidal category]] $C$ with symmetry $\tau$ its opposite $A^{op}$ is the same underlying object $A$ with multiplication $\mu\circ\tau$. The __enveloping monoid__ $A^e$ of $A$ is the monoid whose underlying object is $A\otimes A^{op}$ and for which the multiplication is given by

$$
(\mu\otimes (\mu\circ\tau))\circ(id\otimes\tau\otimes id): (A\otimes A^{op})\otimes (A\otimes A^{op})\to A\otimes A^{op}
$$

where $\tau=\tau_{A,A}$ is the symmetry $A\otimes A\to A\otimes A$. 

The enveloping monoid is sometimes called the __enveloping algebra__, especially if the monoidal category is a category of vector spaces. The left $A^e$-modules in $C$ are in 1-1 correspondence with the $A$-$A$-bimodules in $C$.


[[!redirects enveloping algebra]]
[[!redirects enveloping algebras]]
