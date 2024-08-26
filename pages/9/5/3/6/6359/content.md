
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

**Iterated localizations** are, *to a first approximation*, functors right [[orthogonal]] to conservative functors, i.e. the class of functors we get if we want to factor every functor as something followed by a conservative functor.

The correct statement needs to take into account that $\mathbf{Cat}$ is a 2-category, or at least a [[canonical model structure on Cat|model category]].

## Definition
Given a small category $C$ and a set of morphisms $S$ in it, we can always construct a category $C[S^{-1}]$ which is universal in the sense that every functor $F:C \to D$ which inverts all the morphisms in $S$ factors through it (see [[localization]]):
\begin{tikzcd}[ampersand replacement=\&]
	C \& {C[S^{-1}]} \\
	\& D
	\arrow["L", from=1-1, to=1-2]
	\arrow["F"', from=1-1, to=2-2]
	\arrow["{F'}", dashed, from=1-2, to=2-2]
\end{tikzcd}

On the other hand, it is often interesting to look at which morphisms of $C$ become isomorphisms under the action of a functor $F:C \to D$ (e.g. $F$ might be a [[cohomology theory]] and we want to assess which maps in $C$ are [[quasi-isomorphisms]]).

Call $\ker F$ the class of maps in $C$ which are inverted by $F$ (ndr: this isn't standard notation). Then we can localize $C$ at $\ker F$ and thus factor $F$ as a localization $L_1$ followed by a functor $F_1:C[\ker F^{-1}] \to D$:

\begin{tikzcd}
	C & {C[\ker F^{-1}]} \\
	& D
	\arrow["{L_1}", from=1-1, to=1-2]
	\arrow["F"', from=1-1, to=2-2]
	\arrow["{F_1}", from=1-2, to=2-2]
\end{tikzcd}

It turns out $F_1$, in general, still inverts arrows, thus we can iterate this process and get a sequence:

\begin{tikzcd}
	C & {C_1} & \cdots & {C_{n+1}} & \cdots & {C_\omega} \\
	\\
	&& D
	\arrow["{L_1}", from=1-1, to=1-2]
	\arrow["F"', from=1-1, to=3-3]
	\arrow["{L_2}", from=1-2, to=1-3]
	\arrow["{F_1}", from=1-2, to=3-3]
	\arrow["{L_n}", from=1-3, to=1-4]
	\arrow["{L_{n+1}}", from=1-4, to=1-5]
	\arrow["{F_{n+1}}"{description}, from=1-4, to=3-3]
	\arrow[from=1-5, to=1-6]
	\arrow["K", from=1-6, to=3-3]
\end{tikzcd}

where $C_{n+1} = C[\ker F_n^{-1}]$. Now take the colimit of the sequence of localizations, and get $C_\omega = \colim_n C_n$. Clearly there is a functor $L:C \to C_\omega$ and also a mediating map $K:C_\omega \to D$ such that $KL = F$. In fact, one can prove $K$ is [[conservative]].

\begin{definition}
A functor $F:C \to D$ is an **iterated localization** when $K$ is an equivalence.
\end{definition}

This makes $(\text{iterated localizations}, \text{conservative functors})$ a(n homotopy) [[factorization system]] on $\mathbf{Cat}$ (considered as a 1-category with weak equivalences given by [[equivalence of categories|equivalences of categories]]).

## See also

* [[localization of a category]], [[category of fractions]]
* [[orthogonal factorization systems]]
* [[conservative functor]]

## References

The above is pretty much directly taken from Joyal's definition of such functors:

* [[Joyal]]'s CatLab, [[joyalscatlab:Factorisation systems|Factorisation systems]].
* [[André Joyal]], _Notes on quasi-categories_, [pdf](https://www.math.uchicago.edu/~may/IMA/Joyal.pdf)