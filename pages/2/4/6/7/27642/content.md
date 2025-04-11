
\tableofcontents

## Idea

In [[dependent type theory]], given a [[bounded poset]] $I$, *simplicial types* are those for which $I$ behaves as a [[bounded total order]]. This is important in [[triangulated type theory]] to identify the objects which behave as [[simplicial object in an (infinity,1)-category|simplicial objects]] relative to the [[distributive lattice]] [[interval]] $\mathbb{I}$, in order to define things such as [[(infinity,1)-category|$(\infty,1)$-categories]], which are the *$\mathbb{I}$-simplicial* [[Rezk types]] in triangulated type theory. 

## Definition

In [[dependent type theory]], let $I$ be a [[bounded poset]], such as a [[distributive lattice]]. A type $A$ is **$I$-simplicial** if for all elements $i:I$ and $j:I$ the function

$$\lambda x.\lambda t.x:A \to ((i \leq j \vee j \leq i) \to A)$$

which takes elements $x:A$ to constant functions $\lambda t.x:(i \leq j \vee j \leq i) \to A$ is an [[equivalence of types]]

$$\mathrm{isSimp}_I(A) \coloneqq \mathrm{isEquiv}(\lambda x.\lambda t.x)$$

\begin{theorem}
Suppose that $I$ is a [[total order]]. Then every type $A$ is $I$-simplicial. 
\end{theorem}

\begin{proof}
In a total order, the type $i \leq j \vee j \leq i$ is a [[contractible type]] for all $i:I$ and $j:I$, and given any contractible type $B$, the function $\lambda x.\lambda t.x:A \to (B \to A)$ is an [[equivalence of types]]. Thus, $A$ is $I$-simplicial for all types $A$. 
\end{proof}

In particular, this means that in [[simplicial type theory]] with [[bounded total order]] $\mathbb{I}$, every type is $\mathbb{I}$-simplicial. 

## Related concepts

* [[triangulated type theory]]

* [[simplicial type theory]]

## References

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects simplicial type]]
[[!redirects simplicial types]]