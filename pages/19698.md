+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The concept of an **institution** provides an abstract category-theoretic rendering of the informal concept of a _logical system_. It was introduced by Burstall and [[Joseph Goguen|Goguen]] in the 1970s in order to get a grip on the proliferation of specification logics in programming and constitutes a genuine contribution of theoretical [[computer science]] to general logic and [[abstract model theory]].

## Definition

+-- {: .num_defn #institution}
###### Definition
An _institution_ is a quadruple $\langle\Sigma , S, M, \models\rangle$ with

* $\Sigma$ a category of "signatures", 

* $S:\Sigma\to Set$ a functor assigning to an object $X\in \Sigma$ the set $S(X)$ of "sentences" of signature $X$ ,

* $M:\Sigma^{op} \to Cat$ is a functor assigning to an object $X\in\Sigma^{op}$ the category of "X-structures" and 

* $\models$ is a family of "satisfaction" relations specifying for each signature $X$ and $X$-structure $\mathfrak{A}$ the set of sentences $Th(\mathfrak{A})\subseteq S(X)$ "holding in $\mathfrak{A}$",

subject to the following _satisfaction condition_:

Given a morphism of signatures $\varphi:X\to X'$ and a sentence $e\in S(X)$, the sentence $S(\varphi)(e)$ i.e. the "$\varphi$-translation" of $e$ into an $X'$-sentence, holds in a X'-structure $\mathfrak{A}'$ (in signs: $\mathfrak{A}'\models S(\varphi)(e)$) precisely if $e$ holds in $M(\varphi)(\mathfrak{A}')$:

\[ \mathfrak{A}'\models S(\varphi)(e) \; iff \; M(\varphi)(\mathfrak{A}')\models e\quad .
\]

=--

## Examples

...


## Applications

...

## Related entries

* [[abstract model theory]]

* [[Beth definability theorem]]

* [[Grothendieck fibration]]

* [[signature]]

* [[computer science]]

* [[Joseph Goguen]]

## Links

* The late Joseph Goguen's [page on institutions](http://cseweb.ucsd.edu/~goguen/projs/inst.html).

* A Bremen based community homepage: [Flirts](http://www.informatik.uni-bremen.de/flirts/).

## References

One of the original sources is

* [[Joseph Goguen|J. Goguen]], R. Burstall, _Institutions: Abstract model theory for specification and programming_ , J. ACM **39** no.1 (1992) pp.95–146. ([ps-preprint](http://cseweb.ucsd.edu/~goguen/pps/ins.ps))

A high level introduction

* Răzvan Diaconescu, [Institution Theory](https://www.iep.utm.edu/insti-th/), Internet Encyclopedia of Philosophy

A monograph on the subject is

* Răzvan Diaconescu, _Institution-independent Model Theory_ , Birkh&#228;user Basel 2008.

More specific research papers are

* M. Aiguier, F. Barbier, _An institution-independent Proof of the Beth Definability Theorem_ , Studia Logica **85** no. 3 (2007) pp.333-359. ([pdf](http://perso.ecp.fr/~aiguierm/publications/communications/sl07.pdf))

* Răzvan Diaconescu, _Grothendieck institutions_ , App. Cat. Struc. **10** no.4 (2002) pp.383–402.

* Lucanu, D., Li, Y. F., & Dong, J. S. (2006). 
 Semantic web languages–towards an institutional perspective. 
 In Algebra, Meaning, and Computation (pp. 99-123). Springer, Berlin, Heidelberg. ([pdf](
http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.119.5368&rep=rep1&type=pdf))

* Bao, J., Tao, J., McGuinness, D. L., & Smart, P. (2010). 
 Context representation for the semantic web. ([pdf](https://eprints.soton.ac.uk/270829/))
 

[[!redirects institutions]]
[[!redirects Institution]]
[[!redirects Institutions]]
