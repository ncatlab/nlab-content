
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

\begin{definition}
A **symmetric bicategory** ([May & Sigurdsson 2006, Def. 16.2.1](#MaySigurdsson06)) is a [[bicategory]] $B$ equipped with a bijective-on-objects [[equivalence of 2-categories|biequivalence]] $t \colon B \simeq B^{op}$ to its [[opposite 2-category]].

A **closed symmetric bicategory** is a symmetric bicategory that is [[closed bicategory|closed]] ([May & Sigurdsson 2006, Def. 16.3.1](#MaySigurdsson06)).
\end{definition}


\begin{remark}
The notion of symmetric bicategory is a [[horizontal categorification]] of that of a  [[symmetric monoidal category]]. It is not to be confused with the notion of a  symmetric [[monoidal bicategory]], which is instead a [[vertical categorification]] of the same concept.

Note, however, that single-object symmetric bicategories are more expressive than [[symmetric monoidal categories]]: a symmetric bicategory with a single object, $Obj(B) \simeq \{\ast\}$, is a symmetric monoidal category if and only if the component functor of $t$ is the [[identity functor]] on the single [[hom-category]] $B(\ast,\ast)$.
\end{remark}

## Examples

\begin{example}
[[Prof]] is a closed symmetric bicategory, whose involution is induced by the [[duality involution]] on [[Cat]].
\end{example}

## Related concepts

* [[closed bicategory]]

* [[duality involution]]


## References

The notion of symmetric bicategories was introduced in Definition 16.2.1 (of the published [[MaySigurdsson_ParametrizedHomotopyTheory.pdf:file]]-version, not in the arXiv version, of):

* {#MaySigurdsson06} [[Peter May]], [[Johann Sigurdsson]], _[[Parametrized Homotopy Theory]]_,  Mathematical Surveys and Monographs, vol. 132, AMS 2006   ([ISBN:978-0-8218-3922-5](https://bookstore.ams.org/surv-132), [pdf](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf), [[MaySigurdsson_ParametrizedHomotopyTheory.pdf:file]], [arXiv:math/0411656](https://arxiv.org/abs/math/0411656))



[[!redirects symmetric bicategories]]
[[!redirects closed symmetric bicategory]]
[[!redirects closed symmetric bicategories]]
[[!redirects symmetric closed bicategory]]
[[!redirects symmetric closed bicategories]]
