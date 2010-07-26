
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


## For Lie algebras

### Standard definition

The _Jacobi identity_ is an identity satisfied by the bracket operation $[-,-] : \mathfrak{g} \wedge \mathfrak{g} \to \mathfrak{g}$ of a [[Lie algebra]] $\mathfrak{g}$.

It asserts that for all $x,y,z \in \mathfrak{g}$ we have

$$
  [x,[y,z]] + [z,[x,y]] + [y,[z,x]] = 0
  \,.
$$


### As a derivation property

One useful way to think of this is that it says that for all $x \in \mathfrak{g}$ the linear map $[x,-] : \mathfrak{g} \to \mathfrak{g}$ is a [[derivation]] with respect to the Lie bracket:

$$
  [x,[a,b]] = [[x,a],b]  + [a,[x,b]]
  \,.
$$

### In terms of Chevalley-Eilenberg algebras

Another useful way to think of it is dually in terms of the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ of the Lie algebra $\mathfrak{g}$ (see there for details). In terms of this [[dg-algebra]] $(\wedge^\bullet \mathfrak{g}^*, d_{\mathfrak{g}})$ the Lie barcket is encoded in the [[differential]]

$$
  d_{\mathfrak{g}}|_{\mathfrak{g}^*} := [-,-]^* : \mathfrak{g}^* \to \mathfrak{g}^* \wedge \mathfrak{g}^* 
$$

and the Jacobi identity is equivalent to the statement that this differential squares to 0

$$
  d \circ d = 0
  \,.
$$

## For $L_\infty$-algebras

When Lie algebras are generalized to [[∞-Lie algebra]]s the Jacobi identity in terms of the binary bracket is relaxed to hold only up to a _jacobiator_ $[-,-,-] : \mathfrak{g}_0 \vee \mathfrak{g}_0 \vee \mathfrak{g}_0 \to \mathfrak{g}_1$

$$
  [x,[y,z]] + [z,[x,y]] + [y,[z,x]] = 
  \delta [x,y,z]
  \,.
$$

On the other hand, in terms of the [[Chevalley-Eilenberg algebra]] this is still encoded in just $d \circ d  = 0$ (see there for details).
