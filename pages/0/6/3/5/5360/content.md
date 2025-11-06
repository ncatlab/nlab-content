
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

> For a [[topological space]] satisfying the $R_0$ regularity condition (which states that the [[specialisation preorder]] is [[symmetric relation|symmetric]], hence an [[equivalence relation]]), see [[symmetric topological space]].

***

# Contents
* table of contents
{: toc}

## Idea

A _symmetric space_ is a specially nice [[homogeneous space]], characterized by the property that for each [[point]] there is a symmetry fixing that point and acting as $-1$ on its [[tangent space]].  An example would be the [[sphere]], the [[Euclidean plane]], or the [[hyperbolic plane]].


## Definitions

A **symmetric space** is classically defined to be a [[quotient]] [[manifold]] of the form $G/H$, where $G$ is a [[Lie group]] and the [[subgroup]] $H$ is the set of fixed points of some [[involution]] $\sigma \colon G \longrightarrow G$, that is, a smooth [[homomorphism]] with $\sigma^2 = 1_G$.   Using the involution, every point $a \in G/H$ gives rise to a [[smooth function]]

$$   
  a \triangleright (-)  
  \;\colon\; 
  G/H \longrightarrow G/H
  \mathrlap{\,,} 
$$

fixing the point $a$ and acting as $-1$ on the [[tangent space]] of $a$.  This operations satisfies the laws of an involutory [[quandle]].

More precisely, a **symmetric pair** is a pair $(G,H)$ where $G$ is a [[Lie group]] and the subgroup $H$ is the set of fixed points of some [[involution]] $\sigma : G \to G$.  Different pairs $(G,H)$, $(G',H')$ can give what is normally considered the same symmetric space $G/H \cong G'/H'$.   In other words, not every morphism of symmetric spaces arises from a morphism of symmetric pairs.

To avoid this problem, we can define a symmetric space as a smooth manifold $M$ with a smooth map $\triangleright : M\times M\to M$ such that for all $x,y,z\in M$ 

1. $x \triangleright x = x$ (idempotence)
2. $x \triangleright (x\triangleright y) = y$ 
3. $x \triangleright (y \triangleright z) = (x \triangleright y)\triangleright (x \triangleright z)$ ([[left self-distributivity]])
4. for every $x$ there is a neighborhood $U\subset M$ such that $x \triangleright y = y$ implies $x = y$ for all $z\in U$.

This amounts to an involutory [[quandle]] object $Q$ in the category of smooth manifolds, with the property that each point $a \in Q$ is an _isolated_ fixed point of the map $a \triangleright - : Q \to Q$. 


## Related entries


* [[homogeneous space]]

* [[quandle]]

* [[Lie triple system]]

* [[transvection]]



## References

Original discussion and classification of symmetric spaces:

* {#Cartan1926} [[Élie Cartan]]: *Sur une classe remarquable d'espaces de Riemann*, Bulletin de la Société Mathématique de France **54** (1926) 214-264 &lbrack;[numdam:BSMF_1926__54__214_0](https://www.numdam.org/item/?id=BSMF_1926__54__214_0), [eudml:86508](https://eudml.org/doc/86508)&rbrack;

Further discussion:

* {#Loos69I} Ottmar Loos, _Symmetric Spaces I: General Theory_,  Benjamin (1969) &lbrack;[pdf](https://www2.math.upenn.edu/~wziller/math661/LoosI.pdf)&rbrack;

* {#Loos69II} Ottmar Loos, _Symmetric Spaces II: Compact spaces and classification_,  Benjamin (1969) 

* [[Sigurdur Helgason]], *Group representations and symmetric spaces*, Proc. Internat. Congress Math. Nice 1970, Vol. 2 book no 10, Gauthier-Villars (1971) 313-320 &lbrack;[pdf](https://math.mit.edu/~helgason/group_representations.pdf), [pdf](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0313.0320.ocr.pdf), [djvu](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0313.0320.ocr.djvu)&rbrack;

* [[Sigurdur Helgason]], *Geometric Analysis on Symmetric Spaces*,  Mathematical Surveys and Monographs **39** (1994) &lbrack;[doi:10.1090/surv/039](https://doi.org/10.1090/surv/039)&rbrack;

* [[Sigurdur Helgason]], *Differential geometry, Lie groups and symmetric spaces*, Graduate Studies in Mathematics **34** (2001) &lbrack;[ams:gsm-34](https://bookstore.ams.org/gsm-34)&rbrack;

* S. Araki, _On root systems and an infinitesimal classification of irreducible symmetric spaces_, J. Math. Osaka City Univ. 13 (1962) 1--34


The definition in terms of [[quandles]] coincides with the classical definition in the case of connected symmetric spaces.  For details, including a comparison of other definitions of symmetric space, see:

* Wolgang Bertram, _The geometry of Jordan and Lie structures_, Lecture Notes in Mathematics **1754**, Springer (2000) &lbrack;[doi:10.1007/b76884](https://doi.org/10.1007/b76884)&rbrack;

  > The relation to quandles is given in Theorem I.4.3.  where this result is attributed to chapter II of [Loos 1969 I](#Loos69II).



[[!redirects symmetric spaces]]


