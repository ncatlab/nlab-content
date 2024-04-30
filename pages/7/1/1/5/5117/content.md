+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

A _braided monoidal functor_ is a [[functor]] $F : C \to D$ between [[braided monoidal categories]] that is a [[monoidal functor]] which respects the braiding on both sides, i.e. satisfies the law:

\begin{tikzcd}
	{F(x) \otimes F(y)} && {F(y) \otimes F(x)} \\
	{F(x \otimes y)} && {F(y \otimes x)}
	\arrow["{\beta'_{F(x),F(y)}}", from=1-1, to=1-3]
	\arrow["{\mu_{x,y}}"', from=1-1, to=2-1]
	\arrow["{\mu_{y,x}}", from=1-3, to=2-3]
	\arrow["{F(\beta_{x,y})}"', from=2-1, to=2-3]
\end{tikzcd}

where $\beta$ is braiding on $C$, $\beta'$ is braiding on $D$, and $\mu$ is the [[monoidal functor|lax monoidal structure]] on $F$.

## Properties

Between symmetric monoidal categories a braided monoidal functor is the same as a [[symmetric monoidal functor]]. 


## Related concepts

* [[monoidal functor]]

* [[strong monoidal functor]]

* [[lax monoidal functor]]

* [[oplax monoidal functor]]

* [[bilax monoidal functor]]

* [[Frobenius monoidal functor]]

* **braided monoidal functor**

* [[symmetric monoidal functor]]

## References

An exposition is in

* [[John Baez]], [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

[[!redirects braided monoidal functors]]

[[!redirects symmetric monoidal functor]]
[[!redirects symmetric monoidal functors]]
