
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[duality in string theory]] between [[M-theory]] and [[F-theory]]:

The following line of argument shows why first compactifying M-theory on a torus $S_1^A \times S_1^B$ to get type IIA on a circle and then T-dualizing that circle to get type IIB indeed only depends on the shape $\frac{R_A}{R_B}$ of the torus, but not on its other geometry.

By the [[dualities in string theory]], 10-dimensional [[type II string theory]] is supposed to be obtained from the [[UV-completion]] of [[11-dimensional supergravity]] by first [[Kaluza-Klein mechanism|dimensionally reducing]] over a circle $S^1_A$ -- to obtain [[type IIA supergravity]] -- and then applying [[T-duality]] along another circle $S^1_B$ to obtain [[type IIB supergravity]].

To obtain type IIB sugra in noncompact 10 dimensions this way, also $S^1_B$ is to be compactified (since [[T-duality]] sends the radius $r_A$ of $S^1_A$ to the inverse radius $r_B = \ell_s^2 / R_A$ of $S^1_B$).
Therefore type IIB sugra in $d = 10$ is obtained from 11d sugra compactified on the [[torus]] $S^1_A \times S^1_B$. More generally, this torus may be taken to be an [[elliptic curve]] and this may vary over the 9d base space as an [[elliptic fibration]]. 

Applying T-duality to one of the compact direction yields a 10-dimensional theory which may now be thought of as encoded by a 12-dimensional elliptic fibration. This 12d elliptic fibration encoding a 10d type II supergravity [[vacuum]] is the input data that F-theory is concerned with.

A schematic depiction of this story is the following:

|  |  |  |
|--|--|--|
| [[11d supergravity|M-theory]] in $d = 11$ | | F-theory in $d = 12$ |
| $\downarrow$ [[Kaluza-Klein mechanism|KK-reduction]] along [[elliptic fibration]] | | $\downarrow$ [[axio-dilaton]] is modulus of [[elliptic fibration]] |
| [[type IIA string theory|IIA string theory]] in $d = 9$ | $\leftarrow$[[T-duality]]$\rightarrow$ | [[type IIB string theory|IIB string theory]] in $d = 10$ |

In the simple case where the elliptic fiber is indeed just $S^1_A \times S^1_B$, the [[imaginary part]] of its complex modulus is

$$
  Im(\tau) = \frac{R_A}{R_B}
  \,.
$$

By following through the above diagram, one finds how this determines the [[coupling constant]] in the [[type II string theory]]:

First, the KK-reduction of M-theory on $S^1_A$ yields a type IIA string coupling

$$
  g_{IIA} = \frac{R_A}{\ell_s}
  \,.
$$

Then the T-duality operation along $S^1_B$ divides this by $R_B$:

$$
  \begin{aligned}
    g_{IIB} & = g_{IIA} \frac{\ell_s}{R_B} 
    \\
    & = \frac{R_A}{R_B}
    \\
    & = Im(\tau)
   \end{aligned}
   \,.
$$

## References

See at _[[F-theory]]_ for more
