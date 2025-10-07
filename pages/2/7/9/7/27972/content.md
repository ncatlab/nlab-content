

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


\tableofcontents


## Idea 


In a [[1-category]], [[compositions]] are by definition unique. However, in a general [[simplicial set]] the notion of composition of [[1-simplices]], such as required for the simplicial set to be a [[quasi-category]], is more subtle. The notion of *composers* &lbrack;[Land 2021, Def. 1.2.1](#Land21)&rbrack; reflects some of this.


## Definition

A *composer* $C$ is a [[simplicial set]] with the right [[lifting property]] against all [[spine]] inclusions $I^n \to \Delta^n$. 

In particular since $I^2=\Lambda^2 _1$ is the [[horn|(2,1)-horn,]] and since a [[pair]] of composable [[1-simplices]] $f,g$ determines an [[image]] of $I^2$, this means that given a composer there is a notion of composition $g \circ f$ as the restriction of the extension of the spine $\sigma|_{\{0,2\}}$. 

\begin{tikzcd}
	& b \\
	a && c
	\arrow["g", from=1-2, to=2-3]
	\arrow["f", from=2-1, to=1-2]
	\arrow[dashed, from=2-1, to=2-3]
\end{tikzcd}

## Examples

\begin{example}
Since spine inclusions are [[anodyne morphism|anodyne]] it follows that every [[quasi-category]] is a composer. This is one way to make precise how there  is a notion of [[composition]] on ([[n-morphism|higher]]) [[morphisms]] in a quasi-category.
\end{example}

## References

* {#Land21} [[Markus Land]], Def. 1.2.1 in: *Introduction to Infinity-Categories*, Birkhäuser (2021) &lbrack;[doi:10.1007/978-3-030-61524-6](https://link.springer.com/book/10.1007/978-3-030-61524-6)&rbrack;



[[!redirects composers]]