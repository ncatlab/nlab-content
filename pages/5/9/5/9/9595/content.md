
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

By [[Gelfand duality]], [[commutative C*-algebras]] are  [[equivalence of categories|equivalent]], dually, to suitable [[topological spaces]]. In the spirit of [[noncommutative topology]] one may therefore regard general $C^\ast$-algebras as a [[Isbell duality|formal dual]] to generalized topological spaces and ask if the standard [[homotopy theory]] of topological spaces -- as notably expressed by the standard [[model structure on topological spaces]] -- generalizes to [[noncommutative topology]]. 

By the general discussion at [[simplicial localization]], for a [[category]] to present a [[homotopy theory]] it is sufficient to equip it with the structure of a _[[category with weak equivalences]]_ / _[[homotopical category]]_. Such structures we discuss here. The standard such "noncommutative homotopy" structures reproduce, after [[stabilization]], [[KK-theory]] and [[E-theory]] of $C^\ast$-algebras as their [[triangulated category|triangulated]] [[homotopy categories]].

For practical purposes it is, as usual, useful to enhance the data of the weak equivalences by further ([[cofibration|co]]-)[[fibration]]auxiliary data.
While there cannot be a suitable [[model category]] structure on [[C*Alg]] itself (([Uuye 10]{#Uuye10}); there is however one on [[l.m.c.-C*-algebras]] ([JoachimJohnson 07](#JoachimJohnson07))), there are suitable structures of a [[category of fibrant objects]] ([Uuye 10](#Uuye10)). These we discuss here. For actual [[model category]]-structures see at _[[model structure on operator algebras]]_.

## Definitions

### Category-theoretic preliminaries

Write [[C*Alg]] for the [[category]] of [[C*-algebras]] and [[*-algebra]]-[[homomorphisms]] between them. We regard this as a [[monoidal category]] $(C^\ast Alg, \otimes)$ with the _maximal_ [[tensor product of C*-algebras]].

Write $C^\ast Alg_{sep} \hookrightarrow C^\ast Alg$ for the [[full subcategory]] on the [[separable topological space|separable]] $C^\ast$-algebras.

Write [[Top]] for the category of [[compactly generated topological spaces|compactly generated]] [[weakly Hausdorff topological spaces]]. 

The [[forgetful functor]] which forgets the [[associative algebra]]-structure and the [[*-algebra]]-structure lands in compactly generated weakly Hausdorff spaces and hence is of the form

$$
  U \;\colon\; C^\ast Alg \to Top
  \,.
$$

+-- {: .num_defn}
###### Definition

For $A,B \in $ [[C*Alg]], let 

$$
  C^\ast Alg(A,B) \hookrightarrow Top(U(A), U(B)) \in Top
$$

be the set of $C^\ast$-algebra homomorphisms equipped with the [[subspace topology]] from the [[mapping space]] of the underlying topological spaces.

This makes $C^\ast Alg$ a [[Top]]-[[enriched category]].

=--

+-- {: .num_prop}
###### Proposition

For $A \in $ [[C*Alg]] and $X \in $ [[Top]] be [[compact topological space|compact]], the there is a [[natural isomorphism]]

$$
  Top(X,U(A)) \simeq U(C(X) \otimes A)
  \,.
$$

This defines a [[powering]] of $C^\ast Alg$ over $Top_{cpt}$, by

$$
  A^X \coloneqq C(X) \otimes A
  \,.
$$

=--

([Uuye, lemma 2.2](#Uuye))

+-- {: .num_prop}
###### Proposition

For every $A \in C^\ast Alg$, the [[hom-functor]]

$$
  C^\ast Alg(A,-) \;\colon\; C^\ast Alg \to Top
$$

preserves [[pullbacks]].

=--

([Uuye, corollary 2.6](#Uuye))


### Plain homotopy theory of $C^\ast$-algebras

Write $I \coloneqq [0,1] \in $ [[Top]] for the standard topological [[interval]]. 

+-- {: .num_defn}
###### Definition

For $f,g \colon A \to B$ two morphisms in [[C*Alg]], a [[right homotopy]] $\eta \colon f \Rightarrow g$ is a morphism $\eta \colon A \to B^I$ such that 

$$
  \array{
    && B
    \\
    & {}^{\mathllap{f}}\nearrow& \uparrow^{\mathrlap{B^{i_0}}}
    \\
    A &\stackrel{\eta}{\to}& B^I
    \\
    & {}_{\mathllap{g}}\searrow & \downarrow^{\mathrlap{B^{i_1}}}
    \\
    && B
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Right homotopy is an [[equivalence relation]]. We write $[A,B]$ for the set of right homotopy-[[equivalence classes]] of morphisms $A \to B$. We have a [[natural isomorphism]]

$$
  [A,B] \simeq \pi_0 C^\ast Alg(A,B)
$$

These are the [[hom-sets]] of a [[category]], the [[homotopy category]] $Ho(C^\ast Alg)$

=--


+-- {: .num_defn #HomotopyEquivalence}
###### Definition

Call a morphism $f \colon A \to B$ in [[C*Alg]] a **[[homotopy equivalence]]** of $C^\ast$-algebras if it is an [[isomorphism]] in $Ho(C^\ast Alg)$.

=--

+-- {: .num_defn #SchochetFibration}
###### Definition


Call a morphism $f \colon A \to B$ in [[C*Alg]] a **Schochet fibration** if for all $D \in C^\ast Alg$ the map 

$$
  C^\ast(D,f) \;\colon\; C^\ast(D,A) \to C^\ast(D,B)
$$

is a [[Serre fibration]] in [[Top]].

=--

([Schochet 84](#Schochet84), [Uuye, def. 2.14, prop. 2.18](#Uuye))


+-- {: .num_theorem}
###### Theorem

The category [[C*Alg]] equipped with weak equivalences being the homotopy equivalences of def. \ref{HomotopyEquivalence} and with fibrations being the Schochet fibrations of def. \ref{SchochetFibration} is a [[category of fibrant objects]].

=--

([Schochet 84](#Schochet84), [Uuye, theorem 2.19](#Uuye)).

+-- {: .num_remark}
###### Remark

The canonical functorial [[path space object]] of a $C^\ast$-algebra $A$ in this structure is $A^I$. It follows that the corresponding [[loop space object]] is 

$$
  \Omega A = C_0((0,1), A)
  \,.
$$

Dually, interpreted as a space in [[noncommutative topology]], this corresponds to the [[suspension]] of the space that corresponds to $A$.

=--

### Stabilization at the compact operators

Write $\mathcal{K} \in C^\ast Alg$ for the [[C*-algebra]] of [[bounded operators]] on an infinite-dimensional [[separable Hilbert space]].

+-- {: .num_defn}
###### Definition

Say a morphism $f \colon A \to B$ in [[C*Alg]] is a **stable homotopy equivalence** if $f \otimes id_{\mathcal{K}}$ is a homotopy equivalence, def. \ref{HomotopyEquivalence}. 

Say $f$ is a **stable Schochet fibration** of $f \otimes id_{\mathcal{K}}$ is a Schochet fibration, def. \ref{SchochetFibration}.

=--

+-- {: .num_prop}
###### Proposition

The category [[C*Alg]] becomes a [[category of fibrant objects]] with weak equivalences the stable homotopy equivalences and fibrations the stable Schochet fibrations.

=--

([Uuye, prop. 2.24](#Uuye))

+-- {: .num_remark}
###### Remark

(...) kk-groups (...)

=--

### KK-theory

+-- {: .num_defn #KKEquivalence}
###### Definition

Say a morphism $f \colon A \to B$ in $C^\ast Alg_{sep}$ is a **KK-equivalence** if for all $D \in C^\ast Alg_{sep}$ the morphism

$$
  KK(D,f) \;\colon\; KK(D,A) \to K(D,B)
$$

is an [[isomorphism]], where $KK$ is the [[KK-theory]]-category.

=--

+-- {: .num_theorem}
###### Theorem

The category $C^\ast Alg_{sep}$ carries the structure of a [[category of fibrant objects]] whose weak equivalences are the KK-equivalences of def. \ref{KKEquivalence}, and whose fibrations are the Schochet fibrations, def. \ref{SchochetFibration}.

=--

([Uuye, theore, 2.29](#Uuye))

## References

The various structures of a [[category of fibrant objects]] on [[C*Alg]] are discussed in 

* [[Otgonbayar Uuye]], _Homotopy theory for $C^\ast$-algebras_,  Journal of Noncommutative Geometry,  ([arXiv:1011.2926](http://arxiv.org/abs/1011.2926))
 {#Uuye10}

using notions from

* [[Claude Schochet]], _Topological methods for C&#8727;-algebras. III. Axiomatic homology_, Pacific J. Math. 114 (1984), no. 2, 399&#8211;445. MR 757510 (86g:46102)
 {#Schochet84}

A [[model category|model categorical]] approach is presented in 

* [[Paul Arne Østvær]], _Homotopy theory of $C^*$-algebras_, Frontiers in Mathematics, Springer Basel, 2010, ([arxiv/0812.0154](http://arxiv.org/abs/0812.0154), [pdf](http://folk.uio.no/paularne/file0.pdf))

A [[model category]] structure presenting [[KK-theory]] not on $C^\ast$-algebras itselt but on [[l.m.c.-C*-algebras]] is discussed in

* [[Michael Joachim]], [[Mark Johnson]], _Realizing Kasparov's KK-theory groups as the homotopy classes of maps of a Quillen model category_ ([arXiv:0705.1971](http://arxiv.org/abs/0705.1971))
 {#JoachimJohnson07}

[[!redirects homotopical stricture on C-star algebras]]
