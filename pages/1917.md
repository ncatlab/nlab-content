
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






[[!redirects HQFTs]]