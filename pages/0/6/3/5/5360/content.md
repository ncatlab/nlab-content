
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

> For a [[topological space]] satisfying the $R_0$ regularity condition (which states that the [[specialisation preorder]] is [[symmetric relation|symmetric]], hence an [[equivalence relation]]), see [[separation axioms]].

***

# Contents
* table of contents
{: toc}

## Idea

A _symmetric space_ is a specially nice [[homogeneous space]], characterized by the property that for each [[point]] there is a symmetry fixing that point and acting as $-1$ on its [[tangent space]].  An example would be the [[sphere]], the [[Euclidean plane]], or the [[hyperbolic plane]].


## Definitions

A **symmetric space** is classically defined to be a [[quotient]] [[manifold]] of the form $G/H$, where $G$ is a [[Lie group]] and the [[subgroup]] $H$ is the set of fixed points of some [[involution]] $\sigma : G \to G$, that is, a smooth [[homomorphism]] with $\sigma^2 = 1_G$.   Using the involution, every point $a \in G/H$ gives rise to a [[smooth function]]

$$   a \triangleright -  : G/H \to G/H $$

fixing the point $a$ and acting as $-1$ on the tangent space of $a$.  This operations satisfies the laws of an involutory [[quandle]].

More precisely, a **symmetric pair** is a pair $(G,H)$ where $G$ is a [[Lie group]] and the subgroup $H$ is the set of fixed points of some [[involution]] $\sigma : G \to G$.  Different pairs $(G,H)$, $(G',H')$ can give what is normally considered the same symmetric space $G/H \cong G'/H'$.   In other words, not every morphism of symmetric spaces arises from a morphism of symmetric pairs.

To avoid this problem, symmetric space is (equivalent to) a smooth manifold $M$ with multiplication $\cdot : M\times M\to M$ which is a smooth map such that for all $x,y,z\in M$ 

1. $x \cdot x = x$ (idempotence)
2. $x \cdot (x\cdot y) = y$ 
3. $x\cdot (y \cdot z) = (x \cdot y)\cdot (x \cdot z)$ ([[left self-distributivity]])
4. for every $x$ there is a neighborhood $U\subset M$ such that $x\cdot y = y$ implies $x = y$ for all $z\in U$.

This amounts to an involutory [[quandle]] object $Q$ in the category of smooth manifolds, with the property that each point $a \in Q$ is an _isolated_ fixed point of the map $a \triangleright - : Q \to Q$. 



## References

Related items include [[homogeneous space]], [[quandle]], [[Lie triple system]], [[transvection]].

The definition in terms of quandles coincides with the classical definition in the case of connected symmetric spaces.  For details, including a comparison of other definitions of symmetric space, see:

* Wolgang Bertram, _The geometry of Jordan and Lie structures_, Lecture Notes in Mathematics **1754**, Springer, Berlin, 2000.

The relation to quandles is given in Theorem I.4.3.  Bertram attributes this result to part I, chapter II of

* Ottmar Loos, _Symmetric Spaces I, II_, Chapter II, Benjamin, New York, 1969.
* Sigurdur Helgason, _Differential geometry, Lie groups and symmetric spaces_,
* S. Helgason, _Group representations and symmetric spaces_, Proc. ICM. Nice 1970, vol. 2, 313-320, [pdf](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0313.0320.ocr.pdf), [djvu](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0313.0320.ocr.djvu) 
[[!redirects symmetric space]]
[[!redirects symmetric spaces]]
