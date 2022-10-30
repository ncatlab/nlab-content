
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

The natural [[tensor product]] operation on [[abelian categories]] is known as the _Deligne tensor product_ or _Deligne box product_, introduced in ([Deligne 90](#Deligne)).

For $A$ and $B$ two suitable [[abelian category|abelian categories]], their Deligne tensor product $A \boxtimes B$ is the abelian category such that suitably [[exact functors]] $A \boxtimes B \to C$ are equivalent to functors $A \times B \to C$ that are suitably exact in each argument.

## Properties

### In terms of categories of modules and tensor product of algebras

For $A$ an [[associative algebra]] over a [[field]] $k$, write $A$[[Mod]] for its [[category of modules]] of finite [[dimension]] over $k$.

Within this entry, we will use the following terminology:

A $k$-linear abelian category $C$ is said to be _finite_ if it is equivalent to a category $A$[[Mod]], as above. 


Let $\mathcal{C}, \mathcal{D}$ be two such finite [[abelian categories]] over $k$.

+-- {: .num_remark}
###### Remark

For every finite abelian category over $k$ there is a $k$-[[associative algebra|algebra]] $A$ and an [[equivalence of categories]]

$$
  \mathcal{C} \simeq A Mod
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $A, B \in Alg_R$ two [[associative algebras]], the Deligne tensor product of [[categories of modules]] is given by the [[tensor product of algebras]]

$$
  (A Mod)  
  \boxtimes
  (B Mod)
  \simeq
  (A \otimes_R B) Mod
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

In the set of lecture notes

* [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], _Topics in Lie theory and Tensor categories_, Lecture notes (spring 2009) ([web](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/))
 {#EGNO}

the Deligne tensor product is discussed in [lecture 9](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/MIT18_769S09_lec09.pdf).


[[!redirects tensor product of abelian categories]]

