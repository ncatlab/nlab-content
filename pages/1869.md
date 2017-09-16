

# Idea #

For $A$ an abelian Lie group (often taken to be $U(1)$), a [[bundle gerbe]] on $X$ is a representation of a [[cohomology|cocycle]] $c$ in $\mathbf{H}(X,\mathbf{B}^2 A)$.

If a central extension $A \to \hat G \to G$ is given (often taken to be $U(1) \to U(n) \to P U (n)$) there is a notion of $\hat G$-[[twisted bundle]]s with twist given by $c$.

A bundle gerbe module is the presentation of such a $\hat G$-[[twisted bundle]] corresponding to the presentation of the $\mathbf{B}^2 A$-cocycle by a [[bundle gerbe]].

# Definition #

If $Y \to X$ is the surjective submersion relative to which the [[bundle gerbe]] $c$ is defined, and if 

$$
  L \to Y \times_X Y
$$

is the transition line bundle of the bundle gerbe, then a **gerbe module for $c$ is a vector bundle

$$
  E \to Y
$$

equipped with an action

$$
  \rho : \pi_2^* E \otimes L \to \pi_1^* E
$$

(where $\pi_1, \pi_2 : Y \times_X Y \to Y$ are the two projections out of the fiber product)

that respects the bundle gerbe product

$$
  \mu : \pi_{12}^* L \otimes \pi_{2 3}^* L 
  \to \pi_{1 3}^* L
$$

in the obvious way.

When $Y = \sqcup_i U_i$ comes form an an open [[cover]] $\{U_i \to X\}$ the above almost manifestly reproduces the explicit description of [[twisted bundle]]s given there. 


# References #

Bundle gerbe modules were apparently introduced in 

* P. Bouwknegt, A. L. Carey, V. Mathai, M. K. Murray, D. Stevenson, _Twisted K-theory and K-theory of bundle gerbes_ ([arXiv](http://arxiv.org/abs/hep-th/0106194))

for modelling [[twisted K-theory]] by [[twisted bundle]]s.

[[!redirects gerbe module]]