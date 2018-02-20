
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

For $A$ an [[abelian group|abelian]] [[Lie group]] (often taken to be the [[circle group]] $U(1)$), a [[bundle gerbe]] on $X$ is a representation of a [[cohomology|cocycle]] $c$ in $\mathbf{H}(X,\mathbf{B}^2 A)$.

If a [[central extension]] $A \to \hat G \to G$ is given (often taken to be $U(1) \to U(n) \to P U (n)$) there is a notion of $\hat G$-[[twisted bundle]]s with twist given by $c$.

A _bundle gerbe module_ is the presentation of such a $\hat G$-[[twisted bundle]] corresponding to the presentation of the $\mathbf{B}^2 A$-cocycle by a [[bundle gerbe]].

## Definition 

+-- {: .num_defn #BundleGerbeModule}
###### Definition


If $Y \to X$ is the [[surjective submersion]] relative to which the [[bundle gerbe]] $c$ is defined, and if 

$$
  L \to Y \times_X Y
$$

is the transition [[line bundle]] of the bundle gerbe, then a **bundle gerbe module** for $c$ is a Hermitean [[vector bundle]]

$$
  E \to Y
$$

equipped with an [[action]]

$$
  \rho : \pi_2^* E \otimes L \to \pi_1^* E
$$

(where $\pi_1, \pi_2 : Y \times_X Y \to Y$ are the two projections out of the [[fiber product]])

that respects the bundle gerbe product

$$
  \mu : \pi_{12}^* L \otimes \pi_{2 3}^* L 
  \to \pi_{1 3}^* L
$$

in the obvious way.

=--

When $Y = \coprod_i U_i$ comes form an an open [[cover]] $\{U_i \to X\}$ the above almost manifestly reproduces the explicit description of [[twisted bundle]]s given there. 


## References 

The concept of bundle gerbe modules was introduced in 

* {#CBMMS}  [[Alan Carey]], [[Peter Bouwknegt]], [[Varghese Mathai]], [[Michael Murray]] and [[Danny Stevenson]], _K-theory of bundle gerbes and twisted K-theory_ ,  Commun Math Phys, 228 (2002) 17-49 ([arXiv](http://arxiv.org/abs/hep-th/0106194))
  

for modelling [[twisted K-theory]] by [[twisted bundle]]s.

A [[splitting principle]] for bundle gerbe modules is discussed in

* {#Tomoda07} [[Atsushi Tomoda]], _On the splitting principle of bundle gerbe modules_, Osaka J. Math. Volume 44, Number 1 (2007), 231-246. ([Euclid](https://projecteuclid.org/euclid.ojm/1174324334), talk slides [pdf](http://ton.prosou.nu/official/ryousi2005.pdf))

For more see at _[[twisted vector bundle]]_.

[[!redirects bundle gerbe modules]]
[[!redirects gerbe module]]
[[!redirects gerbe modules]]
