
> This entry is about the identity in [[Lie theory]]. For another identity named after Jacobi, see at _[[Jacobi theta-function]]_ and _[[Jacobi form]]_.

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

## Idea

The Jacobi identity is an important equational identity that holds in [[Lie algebras]] and is also of interest in other [[nonassociative algebra|algebras]].  It can be generalised to [[higher algebra]]s.

There is a non-additive non-abelian form of the Jacobi identity that occurs in considering certain examples in [[identities among relations]] in the presentation of certain groups. There it is also called the Hall-Witt identity.



## For $1$-algebras

### Definition

Given a [[nonassociative algebra]] $\mathfrak{g}$ over a field or a ring $k$, whose bilinear product is denoted by bracket $[,]:\mathfrak{g}\otimes\mathfrak{g}\to\mathfrak{g}$, the __Jacobi identity__ holds for a triple of elements $x,y,z \in \mathfrak{g}$ if

$$
  [x,[y,z]] + [y,[z,x]] + [z,[x,y]] = 0
  \,.
$$

The principal example is that of a [[Lie algebra]]: here the Jacobi identity by definition holds for all triples of elements (and the bracket is skew-symmetric).

### Relation to the Leibniz identity

If the bracket $[-,-]$ is skew-symmetric the Jacobi identity for all triples is equivalent to the **[[Leibniz identity]]** that for all $x,a,b$, 
the linear map $ad_x = [x,-] : \mathfrak{g} \to \mathfrak{g}$ is a [[derivation]] with respect to the Lie bracket:

$$
  \left[x,\left[a,b\right]\right] = \left[\left[x,a\right],b\right]  + \left[a,\left[x,b\right]\right]
  \,.
$$

One can also consider right derivations (right Leibniz identity), what is again equivalent in the presence of antisymmetry:

$$
 \left[\left[a,b\right],x\right] = \left[\left[a,x\right],b\right]  + \left[a,\left[b,x\right]\right]
  \,.
$$

Left and right [[Leibniz algebras]] generalize Lie algebras by having a left or right Leibniz identity, but not necessarily antisymmetry of the bracket. In particular, Jacobi identity, and left and right Leibniz identities do not need to coincide without antisymmetry. 


### In terms of Chevalley--Eilenberg algebras

A useful way to think of Jacobi identity for finite-dimensional Lie algebras, is dually in terms of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ of the Lie algebra $\mathfrak{g}$ (see there for details). In terms of this [[dg-algebra]] $(\wedge^\bullet \mathfrak{g}^*, d_{\mathfrak{g}})$, the Lie bracket is encoded in the [[differential]]

$$
  d_{\mathfrak{g}}|_{\mathfrak{g}^*} := [-,-]^* : \mathfrak{g}^* \to \mathfrak{g}^* \wedge \mathfrak{g}^* 
$$

and the Jacobi identity is equivalent to the statement that this differential squares to $0$

$$
  d \circ d = 0
  \,.
$$


## For $L_\infty$-algebras

When Lie algebras are generalized to [[∞-Lie algebra]]s, the Jacobi identity in terms of the binary bracket is relaxed to hold only up to a [[natural isomorphism]] called the __jacobiator__, $[-,-,-] : \mathfrak{g}_0 \vee \mathfrak{g}_0 \vee \mathfrak{g}_0 \to \mathfrak{g}_1$,

$$
  \left[x,\left[y,z\right]\right] + \left[y,\left[z,x\right]\right] + \left[z,\left[x,y\right]\right]  = 
  \delta \left[x,y,z\right]
  \,,
$$

where $\delta$ is the differential. 

On the other hand, in terms of the [[Chevalley-Eilenberg algebra]] this is still encoded in just $d \circ d  = 0$ (see there for details).


##Related entries

* [[identity among the relations]] 

[[!redirects Jacobi identity]]
[[!redirects Jacobi identities]]
[[!redirects jacobiator]]
[[!redirects jacobiators]]
[[!redirects Jacobiator]]
[[!redirects Jacobiators]]
