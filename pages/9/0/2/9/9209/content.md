
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

For $A$ and $B$ two finite abelian abelian categories, their Deligne tensor product $A \boxtimes B$ is the abelian category such that their right [[exact functors]] $A \boxtimes B \to C$ are equivalent to functors $A \times B \to C$ that is right exact in each argument.

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

This appears for instance as ([EGNO, prop. 1.46.2](#EGNO)).


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

He points out that while Deligne's tensor product always exists for finite abelian categories, it does not always exist for general [[abelian categories]].  He argues that in this case it is better to use Kelly's tensor product of finitely cocomplete categories, because it always exists, and it agrees with Deligne's tensor product when the latter exists.  

In the set of lecture notes

* [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], _Topics in Lie theory and Tensor categories_, Lecture notes (spring 2009) ([web](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/))
 {#EGNO}

the Deligne tensor product is discussed in [lecture 9](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/MIT18_769S09_lec09.pdf).


[[!redirects tensor product of abelian categories]]

[[!redirects Deligne tensor product]]
[[!redirects Deligne tensor products]]

