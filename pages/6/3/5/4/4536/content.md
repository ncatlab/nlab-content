
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


## For nonassociative algebras

### Standard definition

Given a [[nonassociative algebra]] $\mathfrak{g}$ over a field or a ring $k$, whose bilinear product is denoted by bracket $[,]:\mathfrak{g}\otimes\mathfrak{g}\to\mathfrak{g}$, the Jacobi identity for a triple of elements $x,y,z \in \mathfrak{g}$ is 

$$
  [x,[y,z]] + [y,[z,x]] + [z,[x,y]] = 0
  \,.
$$

The principal example is a $k$-Lie algebra: then the Jacobi identity holds for all triples of elements, as well as antisymmetry. 

### Relation to Leibniz identity

In the presence of antisymmetry, the Jacobi identity for all triples is equivalent to the **Leibniz identity** that for all $x,a,b$, 
the linear map $ad_x = [x,-] : \mathfrak{g} \to \mathfrak{g}$ is a [[derivation]] with respect to the Lie bracket:

$$
  [x,[a,b]] = [[x,a],b]  + [a,[x,b]]
  \,.
$$

One can also consider right derivations (right Leibniz identity), what is again equivalent in the presence of antisymmetry:

$$
 [[a,b],x] = [[a,x],b]  + [a,[b,x]]
  \,.
$$

Left and right [[Leibniz algebras]] generalize Lie algebras by having a left or right Leibniz identity, but not necessarily antisymmetry of the bracket. In particular, Jacobi identity, and left and right Leibniz identities do not need to coincide. 

### In terms of Chevalley-Eilenberg algebras

A useful way to think of Jacobi identity for finite-dimensional Lie algebras, is dually in terms of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ of the Lie algebra $\mathfrak{g}$ (see there for details). In terms of this [[dg-algebra]] $(\wedge^\bullet \mathfrak{g}^*, d_{\mathfrak{g}})$ the Lie barcket is encoded in the [[differential]]

$$
  d_{\mathfrak{g}}|_{\mathfrak{g}^*} := [-,-]^* : \mathfrak{g}^* \to \mathfrak{g}^* \wedge \mathfrak{g}^* 
$$

and the Jacobi identity is equivalent to the statement that this differential squares to 0

$$
  d \circ d = 0
  \,.
$$

## For $L_\infty$-algebras

When Lie algebras are generalized to [[∞-Lie algebra]]s the Jacobi identity in terms of the binary bracket is relaxed to hold only up to a natural isomorphism called _jacobiator_ $[-,-,-] : \mathfrak{g}_0 \vee \mathfrak{g}_0 \vee \mathfrak{g}_0 \to \mathfrak{g}_1$

$$
  [x,[y,z]] + [y,[z,x]] + [z,[x,y]]  = 
  \delta [x,y,z]
  \,,
$$

where $\delta$ is the differential. 

On the other hand, in terms of the [[Chevalley-Eilenberg algebra]] this is still encoded in just $d \circ d  = 0$ (see there for details).

[[!redirects Leibniz identities]]