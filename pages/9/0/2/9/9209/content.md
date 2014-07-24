
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The natural [[tensor product]] operation on [[finite abelian category|finite abelian categories]] is known as the _Deligne tensor product_ or _Deligne box product_, introduced in ([Deligne 90](#Deligne)).

For $A$ and $B$ two [[abelian categories]], their Deligne tensor product $A \boxtimes B$ is the abelian category such that for any other abelian category $C$ right [[exact functors]] of the form $A \boxtimes B \to C$ are equivalent to functors $A \times B \to C$ that are right exact in each argument separately.

This tensor product exists for [[finite abelian categories]] but not generally on all [[abelian categories]]. However a slight variant does: instead of abelian categories one can consider categories with [[finite colimits]], see [Franco 12](#Franco12) and ([Chirvasitu&Johnson-Freyd 11, remark 2.2.8](#ChirvasituJohnson-Freyd11)).

## Properties

### In terms of categories of modules and tensor product of algebras

Recall that for every [[finite abelian category]] over $k$, there is a finite-dimensional [[associative algebra|algebra]] $A$ over $k$ and a $k$-linear [[equivalence of categories]]

$$
  \mathcal{C} \simeq A Mod_{fd}
  \,
$$

where the right side consists of $A$-modules which are finite-dimensional as vector spaces over $k$.   $A$ is uniquely determined up to [[Morita equivalence]]. 

+-- {: .num_prop}
###### Proposition

For $A, B \in Alg_k$ two finite-dimensional [[associative algebras]] over a field $k$, the Deligne tensor product of their categories of finite-dimensional modules is the category of finite-dimensional modules of the [[tensor product of algebras]] $A \otimes_k B$:

$$
  A Mod_{fd} 
  \boxtimes
  B Mod_{fd}
  \simeq
  (A \otimes_k B) Mod_{fd}
  \,.
$$

=--

This appears for instance as ([EGNO, prop. 1.46.2](#EGNO)). Without the finiteness constraints and using the tensor product of categories with finite colimits, this appears as ([Chirvasitu&Johnson-Freyd 11, remark 2.2.8](#ChirvasituJohnson-Freyd11)).


## Related concepts

* [[tensor product of presentable (infinity,1)-categories]]

## References

The construction was introduced in 

* [[Pierre Deligne]], _Cat&#233;gories tannakiennes_, The Grothendieck
Festschrift, Vol. II. Progr. Math. 87, 111&#8211;195. Birkh&#228;user
Boston. 1990 (1990)
 {#Deligne}

A survey is in 

* Ignacio L&#243;pez Franco, _Tensor products of finitely cococomplete and
abelian categories_ (2012) ([pdf](http://www.mat.uc.pt/~workCT/slides/Ignacio.pdf))
 {#Franco12}

Here the author points out that while Deligne's tensor product always exists for finite abelian categories, it does not always exist for general [[abelian categories]].  He argues that in this case it is better to use Kelly's tensor product of finitely cocomplete categories, because it always exists, and it agrees with Deligne's tensor product when the latter exists.  

Similar remarks (in the context of [[2-rings]]/[[2-modules]]) are from corollary 2.2.5 on in 

* Alexandru Chirvasitu, [[Theo Johnson-Freyd]], _The fundamental pro-groupoid of an affine 2-scheme_ ([arXiv:1105.3104](http://arxiv.org/abs/1105.3104))
 {#ChirvasituJohnson-Freyd11}

In the set of lecture notes

* [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], _Topics in Lie theory and Tensor categories_, Lecture notes (spring 2009) ([web](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/))
 {#EGNO}

the Deligne tensor product is discussed in [lecture 9](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/MIT18_769S09_lec09.pdf).


[[!redirects tensor product of abelian categories]]

[[!redirects Deligne tensor product]]
[[!redirects Deligne tensor products]]

