
#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A **covariant derivative** is a way to differentiate a vector field along a curve, and provides a generalization of the usual directional derivative in multivariable calculus.

#Definition#
Now assume $M$ is given a [[Koszul connection]] $\nabla$.  There is a unique operator $D$ sending vector fields along $c$ to vector fields along $c$ such that:


1. If $X$ is a vector field along $c$ and $f: M \to \mathbb{R}$, then $D(fX)(t) = (f \circ c)' X + f D( X)(t)$.

Note that $c'(t) \in (TM)_{c(t)}$, by definition.

2. If $X$ is the restriction of a vector field $\bar{X}$ on $M$, i.e. $X(t) = \bar{X}(c(t))$, then
\[ D(X)(t) = ( \nabla_{c'(t)} \bar{X})(c(t)).\]

This operator is called the **covariant derivative** along $c$.  It is in fact a generalization of the usual directional derivative of vector fields in multivariable calculus, which occurs when you take the connection on $\mathbb{R}^n$ with all Christoffel symbols zero.

#Proof of Existence#

The first condition  means we can, by multiplying $X$ by a cut-off function, assume $X$ is supported in some coordinate neighborhood $U$ with coordinates $x^1, \dots, x^n$.  In particular, we may even assume that the image of $c$ is contained in $U$ by shrinking $J$ and using local uniqueness (which we prove below).  Moreover, we can assume that $c$ is one-to-one by shrinking further.

Now, in the local case, we can write $c(t) = (c^1(t), \dots, c^n(t))$, and $X(t) = \sum_i X^i(t) \partial_i$, where $\partial_i = \frac{\partial}{\partial x_i}$.  We can extend $X$ to $\bar{X} = \sum_i  \bar{X}^i \partial_i $.  Let the Christoffel symbols of the connections be $\Gamma^k_{ij}$.  By linearity
\[ \nabla_{c'(t)} \bar{X} = \sum_{i,k} c'^i(t) \nabla_{\partial_i} \left( \bar{X}^k \partial_k \right).\]
This equals by the derivation-like identity for connections 
\[ \sum_{i,k} c'^i(t)  \frac{\partial \bar{X}^k}{\partial x^i} \partial_k  + \sum_{i,j,k} c'^i(t) \bar{X}^k \Gamma^j_{ik} \partial_j .  \]
Shifting the indices, collecting terms, and using that $X$ is a restriction of $\bar{X}$ gives that if we have such an operator $D$, then
\[ D(X)(t) = \sum_j \left( X'^j(t) + \sum_{i,k} c'^i(t) {X}^k(t) \Gamma^j_{ik}(c(t)) \right) \partial_j.\]
This expression depends only on $X$.  Thus we define $D(X)$ this way in local coordinates; it is easily checked that the conditions are satisfied locally, and one pieces together the local covariant derivatives to get the global ones.  The fact that patching is legal follows from the uniqueness assertion and a partition of unity  argument.
