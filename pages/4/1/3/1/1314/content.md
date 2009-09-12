<div class="rightHandSide toc">
[[!include differential graded objects - contents]]
</div>

##Idea 

This is the first of a series developing the theory of:

###Differential forms on polyhedra and simplicial sets _&#224; l&#224;_ Sullivan-Thom-Whitney, 

(which has been adapted from Halperin, (see references))

Following ideas of Thom and Whitney, Denis Sullivan defined an algebra of differential forms on a polyhedron. The following is the first of three linked entries dealing with that the initial part of his theory.


##Differential forms on $\mathbf{\Delta}^n$##

Recall that $\mathbf{\Delta}^n \subset \mathbb{R}^{n+1}$ is specified by 

$$\mathbf{\Delta}^n = \left\{\sum^n_0 t_i\mathbf{v}_i \Big| 0\leq t_i\leq 1; \sum^n_0 t_1 =1\right\},$$

where the $\mathbf{v}_i$ form the standard basis for $\mathbb{R}^{n+1}$, so $\mathbf{v}_1 = (1, 0, \ldots, 0)$, etc.  We will denote by $F^n$ the affine $n$-plane that contains $\mathbf{\Delta}^n $.  The continuous function $b_i :\mathbf{\Delta}^n\to\mathbb{R}$ given by 

$$b_i(\sum t_j\mathbf{v}_j) = t_i$$

will be called the $i^{th}$ **barycentric coordinate function**.

A *$C^\infty$ $p$-differential form* on $\mathbf{\Delta}^n $, $\Phi$, is a family of $p$-linear skew symmetric maps 

$$\Phi_x : T_x(F^n) \times \ldots\times T_x(F^n) \to \mathbb{R}, \quad x\in \mathbf{\Delta}^n,$$

(where the product is $p$-fold),
which extends to an ordinary $C^\infty$ $p$-form on the manifold $F^n$.

These form a real vector space $A^p_\infty(\mathbf{\Delta}^n)$ and we have the obvious restriction map $A^p_\infty(F^n)\to A^p_\infty(\mathbf{\Delta}^n)$, which is surjective by definition.  It is a straight forward calculation that in the direct sum 

$$A_\infty(\mathbf{\Delta}^n) =\sum_{p=0}^{n}A^p_\infty(\mathbf{\Delta}^n) $$

there is a unique multiplication, $\wedge$, and a unique differential $d$ such that the restriction $A^p_\infty(F^n)\to A^p_\infty(\mathbf{\Delta}^n)$ is a homomorphism of commutative [[differential graded algebra|differential graded algebras]], (c.d.g.a). 

Moreover, the standard proofs of the [[Poincare lemma|Poincaré lemma]] apply to show that $(A_\infty(\mathbf{\Delta}^n),d)$ is acyclic:

$$H(A_\infty(\mathbf{\Delta}^n),d) \cong \mathbf{R}.$$

Next suppose that $f : [n]\to [m]$ be any set map, where $[n] =\{0\lt 1\lt\ldots \lt n\}$, usually considered as an ordered set as shown.  Define a linear map $f : \mathbb{R}^{n+1} \to \mathbb{R}^{m+1}$ by $\mathbf{v}_i\mapsto\mathbf{v}_{f(i)}$. This restricts to a linear map $\mathbf{\Delta}(f) : \mathbf{\Delta}^n \to 
\mathbf{\Delta}^m$, which induces in the standard way a homomorphism of c.d.g.as

$$A_\infty(f) : A_\infty(\mathbf{\Delta}^n)\to A_\infty(\mathbf{\Delta}^m).$$

If $f$ is a face map or a degeneracy map we will simply write $d_i$ or $s_i$ for the corresponding induced maps on the c.d.g.as.  These of course make $A^p_\infty$ into a [[simplicial vector space]] and $A_\infty$ into a [[simplical commutative differential graded algebra]]


Each element of $A^p_\infty(\mathbf{\Delta}^n)$ may be uniquely written


$$\Phi =\sum_{1\leq i_1\lt\ldots\lt i_p\leq n}\Phi_{i_1\ldots i_p}d b_{i_1}\wedge\ldots d b_{i_p},$$


where $b_j$ is as above the $j^{th}$ barycentric coordinate function and each $\Phi_{i_1\ldots i_p}$ is a $C^\infty$-function on $\mathbf{\Delta}^n$.



With this representation the multiplication and differential are given by the usual formulae. The multiplication is defined by $\Phi \wedge \Psi$ and extends linearly the product 

$$(d b_{i_1}\wedge\ldots d b_{i_p})\wedge (d b_{j_1}\wedge\ldots d b_{j_q}) = (d b_{i_1}\wedge\ldots d b_{i_p}\wedge d b_{j_1}\wedge\ldots d b_{j_q})$$

on the generating forms. Now if $f$ is a differentiable function
 
$$d f = \sum_{i=1}^{n} \frac{\partial f}{\partial x^i}d x_i,$$ 

so if 

$$\Phi =\sum_{1\leq i_1\lt \ldots\lt i_p\leq n}\Phi_{i_1\ldots i_p}d b_{i_1}\wedge\ldots d b_{i_p},$$

then 

$$d\Phi =\sum_{1\leq i_1\lt\ldots\lt i_p\leq n} d\Phi_{i_1\ldots i_p} \wedge d b_{i_1} \wedge \ldots d b_{i_p},$$


##References

The source used was:

*  S. Halperin, _Lecture Notes on Minimal Models_, Publications de l'U.E.R. Math&#233;matiques 
Pures et Appliqu&#233;es, Universit&#233; des Sciences et techniques, Lille, Vol 3 (1981) Fasc.3. 

This in turn used ideas from 

* Dennis Sullivan, 
_Infinitesimal computations in topology_, Publications Math&#233;matiques de l'IH&#201;S, 47 (1977), p. 269-331 ([numdam](http://www.numdam.org/numdam-bin/fitem?id=PMIHES_1977__47__269_0))