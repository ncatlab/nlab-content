
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Idea

An important aspect of [[group theory]] is the study of [[normal subgroups]]. A **protomodular** category, even one which is not [[pointed category|pointed]], is defined in such a way that it possesses an intrinsic notion of [[normal subobject]]. The concept is due to [[Dominique Bourn]] and as such sometimes referred to as _Bourn_-protomodularity.

##Definition 

(Taken from [Bourn04](#Bourn04))

Consider any [[finitely complete category]] $\mathcal{C}$ and denote by $Pt\mathcal{C}$ the category whose objects are the [[split epimorphisms]] in $\mathcal{C}$ with a given splitting and morphisms the commutative squares between these data. Denote by $\pi: Pt\mathcal{C} \to \mathcal{C}$ the functor associating its [[codomain]] to any split epimorphism. Since the category $\mathcal{C}$ has [[pullbacks]], the functor $\pi$ is a [[fibration]] which is called the [[fibration of points]].

Any map $f: X \to Y$ induces, by pullbacks, a [[base change]] functor denoted
$f^{\ast}: Pt_Y \mathcal{C} \to Pt_X \mathcal{C}$ between the fibres above $Y$ and $X$.

Then a [[left exact category]] $\mathcal{C}$ is said to be **protomodular** when the fibration $\pi$ has [[conservative functor|conservative]] base change functors, i.e., ones that reflect isomorphisms. A protomodular category is necessarily [[Mal'cev category|Mal'cev]].

## Examples

\begin{example}\label{GroupsFormAProtomodularCategory}
 The category [[Grp]] of all [[groups]] (including [[non-abelian groups]]) is pointed protomodular \end{example}
([Borceux & Bourn 2004, Ex. 3.1.4](#BorceuxBourn04))

\begin{example}
Certain categories of [[varieties of algebras]], such as the category of groups, the category of rings, the category of associative or Lie algebras over a given ring $A$, the category of Heyting algebras, the varieties of $\Omega$-[[Omega-groups|groups]]. (It is shown in [Bourn-Janelidze](#BournJan03) that  a variety $V$ of universal algebras is protomodular if and only if it has $0$-ary terms $e_1, \ldots ,e_n$, binary terms $t_1,\ldots,t_n$, and $(n+1)$-ary term $t$ satisfying
the identities $t(x, t_1(x, y),\ldots,t_n(x, y)) = y$ and $t_i(x, x) = e_i$ for each $i = 1,\ldots,n$.)
\end{example}

\begin{example}
Categories of algebraic varieties as above [[internal category|internal]] to a left exact category, for example, [[TopGrp]].
\end{example}

\begin{example}
Constructions which inherit the property of being protomodular, such as the slice categories $\mathcal{C}/Z$ and the fibres $Pt_Z \mathcal{C}$ of the fibration $\pi$ of pointed objects for instance, or more generally the domain $\mathcal{C}$ of any pullback preserving and conservative functor $U : \mathcal{C} \to \mathcal{D}$; when its codomain $\mathcal{D}$ is protomodular.
\end{example}

\begin{example}
The dual of a [[topos]].
\end{example}

##Consequences of protomodularity

* a map is a [[monomorphism]] if and only if its [[kernel]] is trivial
* a reflective relation is an [[equivalence relation]]
* an [[internal category]] is always an [[internal groupoid]]
* a [[regular epimorphism]] is always the [[cokernel]] of its kernel
* an object is abelian when its diagonal is a normal subobject

A _pointed_ protomodular category is strongly [[unital]], and

* there is a bijection between normal subobjects of an object $X$ and equivalence relations on $X$.

##Strong protomodularity

A category $\mathcal{C}$ is **strongly protomodular** when it is protomodular and is such that any change of base functor $f^{\ast}$ is a _normal_ functor, that is, a left exact conservative functor which reflects the [[normal monomorphisms]].

[[Grp]], [[Ring]] and the dual of any topos are strongly protomodular.

##Related concepts

* [[homological category]]

* [[semi-abelian category]]

* [[regular category]]

## References

* [[Francis Borceux]], [[Dominique Bourn]], *[[Mal'cev, protomodular, homological and semi-abelian categories]]*, Mathematics and Its Applications __566__, Kluwer 2004 ([doi:10.1007/978-1-4020-1962-3](https://link.springer.com/book/10.1007/978-1-4020-1962-3))

* [[Dominique Bourn]], [[Marino Gran]], _Regular, Protomodular, and Abelian Categories_, Chapter IV, pp.165-211 in: Maria Pedicchio, [[Walter Tholen]] (eds.), _Categorical Foundations_, Cambridge University Press 2004 ([doi:10.1017/CBO9781107340985.007](https://doi.org/10.1017/CBO9781107340985.007))

* {#Bourne04} [[Dominique Bourn]], _Protomodular aspect of the dual of a topos_, Advances in Mathematics 187(1), pp. 240-255, 2004.



* [[Dominique Bourn]], _Action groupoid in protomodular categories_, [TAC](http://www.tac.mta.ca/tac/volumes/16/2/16-02abs.html)

* {#BournJan03} [[Dominique Bourn]], [[George Janelidze]], _Characterization of protomodular varieties of universal algebras_, ([TAC](http://www.tac.mta.ca/tac/volumes/11/6/11-06abs.html))

* {#Bourn2017} [[Dominique Bourn]], [_From Groups to Categorial Algebra : Introduction to Protomodular and Mal’tsev Categories_](https://doi.org/10.1007/978-3-319-57219-2), Compact Textbooks in Mathematics, Birkhäuser 2017

[[!redirects protomodular categories]]

[[!redirects Bourn-protomodular]]
[[!redirects Bourn-protomodular category]]
[[!redirects Bourn-protomodular categories]]


