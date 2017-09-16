
####Assumptions and general conventions####

Fix an integer $n \geq 0$ and a field, $K$. All vector spaces will be tacitly assumed to be finite dimensional.  In general $K$ can be replaced by a commutative ring merely by replacing finite dimensional vector spaces by projective $K$-modules of finite type, but we will not do this here.

###A Bit of History###
HQFTs were introduced in 1999 by [[Vladimir Turaev]] for 2-dimensional manifolds.  He extended them to 3-dimensional ones the following year. At about the same time, Brightwell and Turner (1999) looked at what they called the homotopy surface category and its representations. There are two viewpoints which interact and complement each other. Turaev's seems to be to see HQFTs as an extension of the tool kit for studying manifolds given by TQFTs, whilst in Brightwell and Turner's,  it is the 'background space', which is probed by the surfaces.

###Idea###
The idea of Turaev was to extend the basic ideas of [[TQFTs]] from $n$-dimensional manifolds and cobordisms between them, to manifolds with a simple bit of extra structure given by a continuous map to a 'background' space, $B$.

The category of $B$-manifolds and $B$-cobordisms}
The basic objects on which an $(n+1)$-homotopy quantum field theory is built are compact, oriented $n$-manifolds together with  maps to the 'background' space, $B$.  This space $B$ will  be path connected with a fixed base point, $\ast$.  More precisely:



**Definition**

A **$B$-manifold** is a pair $(X, g)$, where $X$ is a closed oriented $n$-manifold (with a choice of base point $m_i$ in each connected component $X_i$ of $X$), and $g$ is a continuous map $g : X \to B$, called the **characteristic map**, such that $g(m_i) = \ast$ for each base point $m_i$.

A **$B$-isomorphism** between $B$-manifolds, $\phi : ( X, g) \to ( Y, h)$ is an isomorphism $\phi : X \to Y$ of the manifolds, preserving the orientation, taking base points into base points and such that $h\phi = g$.


If as  is often the case, the manifolds under consideration will be differentiable and then 'isomorphism' is interpreted as '[[diffeomorphism]]', but equally well we can position the theory in the category of PL-manifolds or triangulable topological manifolds with the obvious changes.  In fact for some of the time it is convenient to  develop constructions for simplicial complexes rather than manifolds, as it is triangulations that provide the basis for the combinatorial descriptions of the structures that we will be using.


Denote by $\mathbf{Man}(n,B)$ the category of $n$-dimensional $B$-manifolds and $B$-isomorphisms.  We define a 'sum' operation on this category using disjoint union.  The disjoint union of $B$-manifolds is defined by
$$( X, g) \amalg ( Y, h) := ( X\amalg Y, g\amalg h),$$
with the obvious characteristic map, $g\amalg h : X \amalg Y \to B$.  With this 'sum' operation, $\mathbf{Man}(n,B)$ becomes a symmetric monoidal category with the unit being given by the empty $B$-manifold, $\emptyset$, with the empty characteristic map.  Of course, this is an $n$-manifold by default.


These $B$-manifolds are the objects of interest, but they have to be related by the analogue of [[cobordisms]] for this setting.

A **$B$-cobordism**, $(W,F)$, from $(X_0,g)$ to $(X_1,h)$ is a [[cobordism]] $W : X_0 \to X_1$ endowed with a homotopy class of maps $F : W \to X$ relative to the boundary such that $F|_{X_0} = 
g$ and $F|_{X_1} = h$. 

Generally unless necessary in this entry, we will not make a notational distinction between the homotopy class $F$ and any of its representatives.  Finally a **$B$-isomorphism of $B$-cobordisms**, $\psi : (W,F) \to (W^\prime, F^\prime)$, is an isomorphism $\psi : W \to W^\prime$ such that 

$$\psi (\partial_+W) = \partial_+W^\prime, \quad \psi (\partial_-W) = \partial_-W^\prime,$$

and $F^\prime \psi = F$, in the obvious sense of homotopy classes relative to the boundary.

We can glue $B$-cobordisms along their boundaries, or more generally, along a $B$-isomorphism between their boundaries, in the usual way.

The detailed structure of $B$-cobordisms and the resulting category $\mathbf{HCobord}(n,B)$ is given in the Appendix to the paper by Rodriques, (see references), at least in the important case of differentiable $B$-manifolds.  This category is a [[monoidal category]] with strict duals.

##Homotopy Quantum Field Theories##

##Definition (Categorical form)##
A **homotopy quantum field theory** is  a [[symmetric monoidal functor]] from $\mathbf{HCobord}(n,B)$  to the category, $Vect$, of finite dimensional vector spaces over the field $K$. 

However let us also give here a more basic definition of a homotopy quantum field theory.

##Less categorical definition of HQFTs##

 A **$(n + 1)$-dimensional homotopy quantum field theory**, $\tau$, with background $B$  assigns 

* to any $n$-dimensional $B$-manifold, $(X,g)$, a vector space, $\tau{(X,g)}$, 

* to any $B$-isomorphism, $\phi : (X, g) \to ( Y, h)$, of $n$-dimensional $B$-manifolds, a $K$-linear isomorphism $\tau(\phi)  : \tau{(X, g)} \to \tau{( Y, h)}$,\\ 

 and

* to any $B$-cobordism, $(W,F) : (X_0,g_0) \to (X_1,g_1)$, a $K$-linear transformation, $\tau(W) : \tau{(X_0,g_0)} \to \tau{(X_1,g_1)}$.

These assignments are to satisfy the following axioms:

1. $\tau$ is functorial in $\mathbf{Man}(n,B)$, i.e., for two $B$-isomorphisms, $\psi: (X, g) \to ( Y, h)$ and $\phi : ( Y, h) \to (P,j)$, we have $\tau(\phi\psi) = \tau(\phi)\tau(\psi),$
and if $1_{(X,g)}$ is the identity $B$-isomorphism on $(X,g)$, then $\tau(1_{(X,g)}) = 1_{\tau{(X,g)}}$

 1.  There are natural isomorphisms
$$c_{(X,g),(Y,h)} : \tau((X,g)\amalg (Y,h)) \cong \tau(X,g)\otimes \tau(Y,h),$$
and an isomorphism, $u : \tau(\emptyset) \cong K$, that satisfy the usual axioms for a [[symmetric monoidal functor]].

1.  For $B$-cobordisms, $(W,F) : (X,g) \to (Y,h)$ and $(V,G): (Y^\prime, h^\prime) \to (P,j)$ glued along a $B$-isomorphism $\psi :(Y,h) \to (Y^\prime,h^\prime)$, we have 
$\tau((W,F)\amalg_\psi (V,G))= \tau(V,G)\tau(\psi)\tau(W,F).$

1.  For the identity $B$-cobordism, $1_{(X,g)} = (I\times X, 1_g)$, we have 
$\tau( 1_{(X,g)}) = 1_{\tau(X,g)}.$

1.  For $B$-cobordisms $(W,F) : (X,g) \to (Y,h)$ and $(V,G) : (X^\prime,g^\prime) \to (Y^\prime,h^\prime)$ and $(P,J): \emptyset \to \emptyset$, some fairly obvious diagrams are commutative.

##Discussion##
*  These axioms are slightly different from those given in the original paper of Turaev in 1999.  The really significant difference is in axiom 4, which is weaker than as originally formulated, where any $B$-cobordism structure on $I \times X$ was considered as trivial.  The effect of this change is important as it is now the case that the HQFT is determined by the $(n+1)$-type of $B$, cf. Rodrigues (2003). 

* With the revised version of the axioms, it becomes possible to attempt to classify HQFTs with a given $n$ and $B$. Turaev did this in the original paper with $n = 2$ and $B$ an [[Eilenberg-MacLane space]], $K(G,1)$.  The results of Brightwell and Turner essentially gave the solution for $B$ a $K(A,2)$.



### References### 

*  V. Turaev, Homotopy field theory in dimension 2 and group-algebras, preprint arXiv: 
[arXiv:math.QA/9910010](http://arxiv.org/abs/math.QA/9910010)

* V. Turaev, Homotopy field theory in dimension 3 and crossed group-categories, preprint 
[arXiv:math.GT/0005291v1](http://arxiv.org/abs/math.GT/0005291v1). 

* M. Brightwell and P. Turner, Representations of the homotopy surface category of a simply 
connected space, J. Knot Theory and its Ramifications, 9 (2000), 855--864. 

* G. Rodrigues. Homotopy Quantum Field Theories and the Homotopy Cobordism Category 
in Dimension 1 + 1, J. Knot Theory and its Ramifications, 12 (2003) 287--317 (previously 
available as [arXiv:math.QA/0105018](http://arxiv.org/abs/math.QA/0105018)). 

* T.Porter and V. Turaev, Formal Homotopy Quantum Field Theories, I: Formal Maps and Crossed $C$-algebras, Journal of Homotopy and Related Structures 3(1), 2008, 113--159. ([arXiv:math.QA/0512032](http://arxiv.org/abs/math.QA/0512032)).






[[!redirects HQFTs]]