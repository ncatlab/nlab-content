
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Nuclear adjunctions
* table of contents
{: toc}


## Definition

A **nuclear adjunction** or **bimonadic adjunction** is an [[adjunction]] that is both [[monadic adjunction|monadic]] and [[comonadic adjunction|comonadic]].

One point in favour of the terminology "nuclear" over "bimonadic" is that the term **bimonadic functor** is sometimes used in the literature for a [[functor]] that is both [[monadic functor|monadic]] and [[comonadic functor|comonadic]], which is a different concept that is related to [[bimonads]].

## Properties

* Consider an adjunction $F \dashv G$, generating a [[monad]] $T$ and a [[comonad]] $D$. Under minimal assumptions on the categories, there is an adjunction between the category of $T$-algebras, and the category of $D$-coalgebras, and this adjunction is nuclear. See [Pavlovic–Hughes](#PavlovicHughes20) and below.

* Consider an adjunction $F \dashv G : B \to A$, generating a [[monad]] $T$ and a [[comonad]] $D$. Assuming that $B$ is [[Cauchy complete]], $F$ is [[comonadic]] if and only if the free–forgetful adjunction associated to the [[Eilenberg–Moore category]] of $T$ is nuclear. See [Mesablishvili](#Mesablishvili06).

## Construction of nuclear adjunction

Let $\ell \dashv r$ be an adjunction, inducing a monad $T_1$. One can form the [[Eilenberg–Moore category]] of $T$, which induces an adjunction $f_{T_1} \dashv u_{T_1}$. This in turn induces a comonad $D_2$ on the Eilenberg–Moore category. One can form the Eilenberg–Moore category of $D_2$, which induces an adjunction $u_{D_2} \dashv c_{D_2}$. This in turn induces a monad $T_3$ on the Eilenberg–Moore of $D_2$. We can then continue to iterate this construction, giving monads and comonads $T_1, D_2, T_3, D_4, T_5, \dots$.

[\begin{tikzcd}
	B && {\mathrm{Alg}(T_1)} & {\mathrm{Coalg}(D_2)} & {\mathrm{Alg}(T_3)} & \cdots \\
	& A
	\arrow[""{name=0, anchor=center, inner sep=0}, "\ell", shift left=2, from=2-2, to=1-1]
	\arrow[""{name=1, anchor=center, inner sep=0}, "r", shift left=2, from=1-1, to=2-2]
	\arrow["{!}", from=1-1, to=1-3]
	\arrow[""{name=2, anchor=center, inner sep=0}, "{f_{T_1}}", shift left=2, from=2-2, to=1-3]
	\arrow[""{name=3, anchor=center, inner sep=0}, "{u_{T_1}}", shift left=2, from=1-3, to=2-2]
	\arrow[""{name=4, anchor=center, inner sep=0}, "{u_{D_2}}"', shift right=2, from=1-4, to=1-3]
	\arrow[""{name=5, anchor=center, inner sep=0}, "{c_{D_2}}"', shift right=2, from=1-3, to=1-4]
	\arrow[""{name=6, anchor=center, inner sep=0}, "{f_{T_3}}", shift left=2, from=1-4, to=1-5]
	\arrow[""{name=7, anchor=center, inner sep=0}, "{u_{T_3}}", shift left=2, from=1-5, to=1-4]
	\arrow["\dashv"{anchor=center, rotate=45}, draw=none, from=0, to=1]
	\arrow["\dashv"{anchor=center, rotate=-49}, draw=none, from=2, to=3]
	\arrow["\dashv"{anchor=center, rotate=-90}, draw=none, from=4, to=5]
	\arrow["\dashv"{anchor=center, rotate=-90}, draw=none, from=6, to=7]
\end{tikzcd}](https://q.uiver.app/?q=WzAsNixbMSwxLCJBIl0sWzAsMCwiQiJdLFsyLDAsIlxcbWF0aHJte0FsZ30oVF8xKSJdLFszLDAsIlxcbWF0aHJte0NvYWxnfShEXzIpIl0sWzQsMCwiXFxtYXRocm17QWxnfShUXzMpIl0sWzUsMCwiXFxjZG90cyJdLFswLDEsIlxcZWxsIiwwLHsib2Zmc2V0IjotMn1dLFsxLDAsInIiLDAseyJvZmZzZXQiOi0yfV0sWzEsMiwiISJdLFswLDIsImZfe1RfMX0iLDAseyJvZmZzZXQiOi0yfV0sWzIsMCwidV97VF8xfSIsMCx7Im9mZnNldCI6LTJ9XSxbMywyLCJ1X3tEXzJ9IiwyLHsib2Zmc2V0IjoyfV0sWzIsMywiY197RF8yfSIsMix7Im9mZnNldCI6Mn1dLFszLDQsImZfe1RfM30iLDAseyJvZmZzZXQiOi0yfV0sWzQsMywidV97VF8zfSIsMCx7Im9mZnNldCI6LTJ9XSxbNiw3LCIiLDAseyJsZXZlbCI6MSwic3R5bGUiOnsibmFtZSI6ImFkanVuY3Rpb24ifX1dLFs5LDEwLCIiLDAseyJsZXZlbCI6MSwic3R5bGUiOnsibmFtZSI6ImFkanVuY3Rpb24ifX1dLFsxMSwxMiwiIiwwLHsibGV2ZWwiOjEsInN0eWxlIjp7Im5hbWUiOiJhZGp1bmN0aW9uIn19XSxbMTMsMTQsIiIsMix7ImxldmVsIjoxLCJzdHlsZSI6eyJuYW1lIjoiYWRqdW5jdGlvbiJ9fV1d)

An obvious question is: does this process ever terminate? In unpublished work of Lack, it is [claimed](#Taylor) that this process terminates at $T_3$. In other words, $f_{T_3} \dashv u_{T_3}$ is a nuclear adjunction. Thus $T_3 \simeq T_5 \simeq \dots$ and $D_4 \simeq D_6 \simeq \dots$. Furthermore, if the domain of $\ell$ is [[Cauchy complete]], then it terminates at $D_2$.

Under the simplifying assumptions of [[Cauchy completeness]], this is proven in [Pavlovic–Hughes](#PavlovicHughes20). They observe that this construction forms a [[pseudo-idempotent 2-monad]] on a 2-category of monads on $Cat$.

Note that this construction is distinct from [[monadic decomposition]], which instead constructs new monads from comparison functors, rather than (co)free–forgetful adjunctions.

## References

* [[Michael Barr]], *Coalgebras in a category of algebras*, in: *Category Theory, Homology Theory and their Applications I*, Lecture Notes in Mathematics **86**, Springer (1969) 1-12 &lbrack;[doi:10.1007/BFb0079381](https://doi.org/10.1007/BFb0079381), [pdf](https://www.math.mcgill.ca/barr/papers/coalgs.pdf), [[Barr-CoalgInAlg.pdf:file]]&rbrack;

* [[Armin Frei]] and [[John L. MacDonald]], _Algebras, coalgebras and cotripleability_, Archiv der Mathematik 22 (1971): 1-6.

* {#Taylor} Paul Taylor's email to the [[categories mailing list]] "monadic completion of adjunctions" ([link](https://github.com/punkdit/categories/blob/26b751bbcbe6765fe447e805629ff6416f4c38b1/www.mta.ca/~cat-dist/catlist/1999/monadic-compl))

* Stefano Kasangian, [[Stephen Lack]], and [[Enrico Vitale]]. _Coalgebras, braidings, and distributive laws_, Theory and Applications of Categories 13.8 (2004): 129-146. ([html](https://www.emis.de/journals/TAC/volumes/13/8/13-08abs.html))

* [[Bart Jacobs]]. _Coalgebras and approximation_. Logical Foundations of Computer Science: Third International Symposium, LFCS'94 St. Petersburg, Russia, July 11–14, 1994 Proceedings. Berlin, Heidelberg: Springer Berlin Heidelberg, 2005.

* {#Mesablishvili06} Bachuki Mesablishvili. _Monads of effective descent type and comonadicity_. Theory and Applications of Categories 16.1 (2006): 1-45. ([pdf](http://www.tac.mta.ca/tac/volumes/16/1/16-01.pdf))

* [[Matias Menni]]. _Bimonadicity and the explicit basis property_. Theory and Applications of Categories 26.22 (2012): 554-581. ([pdf](http://www.tac.mta.ca/tac/volumes/26/22/26-22.pdf))

* [[Bart Jacobs]]. _Bases as coalgebras_. Logical Methods in Computer Science 9 (2013).

* {#PavlovicHughes20} [[Dusko Pavlovic]], Dominic J. D. Hughes, _The nucleus of an adjunction and the Street monad on monads_ ([arXiv:2004.07353](https://arxiv.org/abs/2004.07353))


[[!redirects nuclear adjunctions]]
[[!redirects bimonadic adjunction]]
[[!redirects bimonadic adjunctions]]