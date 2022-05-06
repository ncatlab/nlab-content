
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


[[!redirects  geometric theory of categories]]
[[!redirects essentially algebraic theory of categories]]
[[!redirects cartesian theory of categories]]

#Contents#
* table of contents
{:toc}

##Idea
The [[geometric theory|geometric]] **theory of categories** $\mathbb{K}$ is a [[first-order logic|first-order]] axiomatisation of the concept of a (strict) [[category]]. $\mathbb{K}$ is in fact an _essentially algebraic_ , or in more recent terminology, a [[cartesian theory]].

Historically, the first formal axiomatisation was given by [[William Lawvere| F. William Lawvere]] in his [[Functorial Semantics of Algebraic Theories|dissertation]] in 1963. (See at [[ETCC]] for further information).

## Definition

The [[signature]] $\Sigma_\mathbb{K}$ has two sorts $O$ and $A$ for objects and arrows, respectively, three function symbols $d_0:A\to O$ , $d_1:A\to O$ and $id:O\to A$, assiging to morphisms their domain, respectively, codomain and to the objects their [[identity|identity morphisms]], as well as a relation symbol $C\righttailarrow A\times A\times A$ expressing composition of morphisms.

The **theory of categories** is the theory $\mathbb{K}$ over the signature $\Sigma_\mathbb{K}$ with the following sequents:

* $\top\vdash_{x:O} d_0(id(x))=x\wedge d_1(id(x))=x\quad$ ,

* $d_1(f_1)=d_0(f_2)\vdash_{f_1:A,f_2:A}\exists f_3 C(f_1,f_2,f_3)\quad$ ,

* $C(f_1,f_2,f_3)\vdash_{f_1:A,f_2:A,f_3:A} d_0(f_1)=d_0(f_3)\wedge d_1(f_1)=d_0(f_2)\wedge d_1(f_2)=d_1(f_3)\quad $ ,

* $C(f_1,f_2,f_3)\wedge C(f_1,f_2,f_4)\vdash_{f_1:A,f_2:A,f_3:A,f_4:A} f_3=f_4\quad $ ,

* $\top \vdash_{f:A} C(f,id(d_1(f)),f)\wedge C(id(d_0(f)),f,f)\quad $ ,

* $C(f_1,f_2,f_4)\wedge C(f_2,f_3,f_5)\wedge C(f_4,f_3,f_6)\wedge C(f_1,f_5,f_7)\vdash_{f_1:A,f_2:A,f_3:A,f_4:A,f_5:A,f_6:A,f_7:A} f_6=f_7\quad $ .


## Properties

Foremost, we have

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a [[Grothendieck topos]]. Then $Mod_{\mathbb{K}}(\mathcal{E})=cat(\mathcal{E})$ with $cat(\mathcal{E}$ the category of (small) [[internal category|internal categories]] in $\mathcal{E}$ with internal functors as morphisms.\qed
=--

## Some related theories

* By adding the following sequents to $\mathbb{K}$

  $\top\vdash _{x:O} \exists x (x=x)\quad $ ,

  $\top\vdash_{x:O,y:O} \exists f_1\exists f_2 (d_0(f_1)=x\wedge d_0(f_2)=y\wedge d_1(f_1)=d_1(f_2))\quad $ , and,

  $d_0(f_1)=d_0(f_2)\wedge d_1(f_1)=d_1(f_2)\vdash_{f_1:A,f_2:A} \exists f_3\exists f_4(C(f_1,f_3,f_4)\wedge C(f_2,f_3,f_4)$

  one obtains the _theory of filtered categories_ $\mathbb{K}_\less$ with models the internal [[filtered category|filtered categories]] cf. Johnstone ([1977](#J77), p.203).

*  The [[theory of model homomorphisms|theory $\mathbb{K}^2$ of $\mathbb{K}$-model homomorphisms]] is the **theory of functors**.

## Related entries

* [[category]]

* [[category theory]]

* [[geometric theory]]

* [[theory of objects]]

* [[theory of model homomorphisms]]

* [[ETCC]]


## References

* [[Peter Freyd|P. J. Freyd]], A. Scedrov, _[[Categories, Allegories]]_ , North-Holland Amsterdam 1990.

* {#J77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York (1977). (Also available as Dover Reprint, Mineola 2014, p.202f)

* {#J02}[[Peter Johnstone]], _Sketches of an Elephant vol.2_ , Oxford UP 2002.

* F. W. Lawvere, _[[Functorial Semantics of Algebraic Theories]]_ , Ph.D. thesis, Columbia University New York 1963. (With an author's comment and a supplement in: Reprints in Theory and Applications of Categories, no.5 (2004) pp.1-121 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/5/tr5.pdf)))

* {#Law66}F. W. Lawvere, _The Category of Categories as a Foundation for Mathematics_ , pp.1-20 in Eilenberg, Harrison, MacLane, R&#246;hrl (eds.), _Proceedings of the Conference on Categorical Algebra - La Jolla 1965_, Springer Heidelberg 1966.




