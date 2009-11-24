
#Contents#
* automatic table of contents goes here
{:toc}

## Definition ##

+-- {: .un_defn}
###### Definition
**(triangulated subcategory)**


A **triangulated subcategory** $A$ of a [[triangulated category]] $B$ is a nonempty [[subcategory]] closed under suspension of objects and such that for all objects $X,Y$ in $A$ if $X\to Y\to Z\to X[1]$ is a distinguished triangle in $B$, then $Z$ is in $A$.  

A triangulated subcategory $A$ is called **thick** if with any object in $A$ it contains all its direct summands in $B$.

=--

+-- {: .un_defn}
###### Definition
**(Verdier quotient)**


For $A \subset B$ a triangulated subcategory, the [[Verdier quotient]] category $B/A$ which is a triangulated category equipped with a canonical functor $Q^*:B\to B/A$ that is also triangulated (additive and preserving distinguished triangles) and universal among all triangulated functors $B\to D$ which send objects of $A$ to objects isomorphic to $0$. 

=--


The Verdier quotient $B/A$  has the property that the only objects whose images in $B/A$ are isomorphic to the [[zero object]] are the objects from $A$. 

+-- {: .un_defn}
###### Definition
**(Bousfield localization)**


Given a thick subcategory $A\subset B$, we say that the **Bousfield localization** exists if the Verdier quotient functor $Q^*$ has a right [[adjoint functor]] $Q_*$ which is then (automatically) triangulated and fully faithful. 

=--

To amplify, writing $B_{loc} := B/A$ a Bousfield localization of a triangulated category $B$ is in particular an [[adjunction]]

$$
  B_{loc} \stackrel{\stackrel{}{\leftarrow}}{\hookrightarrow}
  B
  \,.
$$

Compare this to [[Bousfield localization of model categories]], noticing that most triangulated categories arise as [[homotopy category of an (infinity,1)-category|homtopy categories]] of [[stable (infinity,1)-category|stable (∞,1)-categories]], hence of [[homotopy category|homotopy categories]] of the [[model category|model categories]] presenting these.


## References ##


* Henning Krause, _Localization theory for triangulated categories_ ([arXiv](http://arxiv.org/abs/0806.1324))

chapter 9 of 

* Neeman, _Triangulated categories_

* Neeman, _The connection between the $K$-theory localization theorem of Thomason, Trobaugh and Yao and the smashing subcategories of Bousfield and Ravenel_ ([pdf](http://archive.numdam.org/article/ASENS_1992_4_25_5_547_0.pdf))