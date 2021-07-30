
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

The concept is due to 

* {#BCMMS02}  [[Peter Bouwknegt]], [[Alan Carey]], [[Varghese Mathai]], [[Michael Murray]], [[Danny Stevenson]], Section 4 of: _K-theory of bundle gerbes and twisted K-theory_ ,  Commun Math Phys, 228 (2002) 17-49 ([arXiv:hep-th/0106194](http://arxiv.org/abs/hep-th/0106194), [doi:10.1007/s002200200646](https://doi.org/10.1007/s002200200646))

recognized as equivalent to earlier discussion of [[twisted bundles]] in

* {#LupercioUribe01} [[Ernesto Lupercio]], [[Bernardo Uribe]], Prop. 7.2.2 (from v2 on) in: *Gerbes over Orbifolds and Twisted K-theory*, Comm. Math. Phys. 245(3): 449-489.  ([arXiv:math/0105039](http://arxiv.org/abs/math/0105039), [doi:10.1007/s00220-003-1035-x](https://doi.org/10.1007/s00220-003-1035-x))

  
both motivated by modelling [[twisted K-theory]] in terms of [[Grothendieck groups]] of [[twisted bundles]].

The [[Cech cohomology|Cech cocycle]]-incarnation of bundle gerbe modules (effectively due to [Lupercio & Uribe 2001, Def. 7.2.1](#LupercioUribe01)) was then also considered in:

* {#Mackaay03} [[Marco Mackaay]], _A note on the holonomy of connections in twisted bundles_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Tome 44 (2003) no. 1, pp. 39-62.  ([arXiv:math/0106019](http://arxiv.org/abs/math/0106019), [numdam:CTGDC_2003__44_1_39_0](http://www.numdam.org/item/?id=CTGDC_2003__44_1_39_0))


A [[splitting principle]] for bundle gerbe modules is discussed in

* {#Tomoda07} [[Atsushi Tomoda]], _On the splitting principle of bundle gerbe modules_, Osaka J. Math. Volume 44, Number 1 (2007), 231-246. ([Euclid](https://projecteuclid.org/euclid.ojm/1174324334), talk slides [pdf](http://ton.prosou.nu/official/ryousi2005.pdf))

For more see at _[[twisted vector bundle]]_.

[[!redirects bundle gerbe modules]]
[[!redirects gerbe module]]
[[!redirects gerbe modules]]
