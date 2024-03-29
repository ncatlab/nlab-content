
# Contents
* table of contents
{: toc}

## Definition

There are two different meanings of the term _coefficient_ in mathematics, one

* [In algebra and analysis](#InAlgebraAndAnalysis)

and one 

* [In cohomology and homology](#InCohomologyAndHomology).

The two notion do however coincide for [[ordinary homology]]/[[ordinary cohomology]] expressed as [[singular homology]]/[[singular cohomology]]. See remark \ref{RelationInSingularCoHomology} below.




### In algebra and analysis
 {#InAlgebraAndAnalysis}

In [[algebra]] and [[analysis]], a _coefficient_ is an element of a [[ring]] (or [[rig]]) $R$ that appears in scalar multiplication; more generally, _coefficients_ are elements of $R$ that appear in a [[linear combinations]].  Thus, we multiply a coefficient by an element of an $R$-[[module]] $M$ (which may even be an algebra, [[associative algebra|associative]] or [[nonassociative algebra|not]]) to get another element of $M$.

For example, given a [[polynomial]] $P = \sum_n a_n x^n$ over $R$ in the [[variable]] $x$, each $a_n \in R$ is the coefficient on $x^n$ in $P$.  The module $M$ here is the [[symmetric algebra]] over $R$.


### In cohomology and homology
 {#InCohomologyAndHomology}

In [[cohomology]] _coefficients_ are what the cohomology takes values in. For [[ordinary cohomology]] $H^\bullet(-,A)$ the [[abelian group]] $A$ is the _coefficient group_. For [[generalized (Eilenberg-Steenrod) cohomology]] $H^\bullet(-,E)$ the given [[spectrum]] $E$  that [[Brown representability|represents]] it is the _coefficient spectrum_. Dually for [[homology]]. 

It is this notion of "coefficient" that appears in terms like

* _[[universal coefficient theorem]]_

* _[[local system of coefficients]]_

* _[[local coefficient bundle]]_.

+-- {: .num_remark #RelationInSingularCoHomology}
###### Remark

This cohomology-theoretic usage of "coefficient" is almost certainly originally derived from the [former](#InAlgebraAndAnalysis) one.  When [[ordinary homology]] with coefficients in $A$ (in the homological sense) is defined using [[singular homology|singular]] or [[cellular homology|cellular]] [[chains]], the chains themselves are [[formal linear combinations]] of [[singular simplices]] or cells whose coefficients (in the algebraic sense) are elements of $A$.  For more general homology and cohomology theories, however, the "coefficient object" is no longer directly interpretable using coefficients in the algebraic sense.

=--

category: disambiguation

[[!redirects coefficient]]
[[!redirects coefficients]]
