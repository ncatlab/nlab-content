
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context
###Localization theory
+--{: .hide}
[[!include localization theory - contents]]
=--
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

**Iterated localizations** are, *to a first approximation*, [[functors]] right [[orthogonal]] to [[conservative functors]], i.e. the [[class]] of functors obtained from factoring any functor as some functor followed by a conservative functor.

For the correct statement one needs to regard [[Cat|$\mathbf{Cat}$]] as a [[2-category]], or at least [[canonical model structure on Cat|as a model category]].

## Definition

Given a [[small category]] $C$ and a [[set]] of [[morphisms]] $S \subset Mor(C)$, we can always construct the [[localization of a category|localization category]] $C[S^{-1}]$ which is [[universal property|universal]] in the sense that every functor $F \colon C \to D$ which inverts all the morphisms in $S$ factors through it (see *[[localization]]*):
\begin{tikzcd}[ampersand replacement=\&]
	C \& {C[S^{-1}]} \\
	\& D
	\arrow["L", from=1-1, to=1-2]
	\arrow["F"', from=1-1, to=2-2]
	\arrow["{F'}", dashed, from=1-2, to=2-2]
\end{tikzcd}

On the other hand, it is often interesting to look at which morphisms of $C$ become isomorphisms under the action of a functor $F \colon C \to D$ (e.g. $F$ might be a [[cohomology theory]] and we want to assess which maps in $C$ are [[quasi-isomorphisms]]).

Call $\ker F$ the class of maps in $C$ which are inverted by $F$ (ndr: this isn't standard notation). Then we can localize $C$ at $\ker F$ and thus factor $F$ as a localization $L_1$ followed by a functor $F_1 \,\colon\, C\big[(\ker F)^{-1}\big] \longrightarrow D$:

\begin{tikzcd}
	C & {C\big[(\ker F)^{-1}\big]} \\
	& D
	\arrow["{L_1}", from=1-1, to=1-2]
	\arrow["F"', from=1-1, to=2-2]
	\arrow["{F_1}", from=1-2, to=2-2]
\end{tikzcd}

It turns out that this $F_1$, in general, still inverts further morphisms. Therefore it makes sense to iterate this process to obtain the following [[sequence]] of functors:

\begin{tikzcd}
	C & {C_1} & \cdots & {C_{n+1}} & \cdots & {C_\omega} \\
	\\
	&& D \mathrlap{\,,}
	\arrow["{L_1}", from=1-1, to=1-2]
	\arrow["F"', from=1-1, to=3-3]
	\arrow["{L_2}", from=1-2, to=1-3]
	\arrow["{F_1}", from=1-2, to=3-3]
	\arrow["{L_{n+1}}", from=1-3, to=1-4]
	\arrow["{L_{n+2}}", from=1-4, to=1-5]
	\arrow["{F_{n+1}}"{description}, from=1-4, to=3-3]
	\arrow[from=1-5, to=1-6]
	\arrow["K", from=1-6, to=3-3]
\end{tikzcd}

where $C_{n+1} \coloneqq C\big[(\ker F_n)^{-1}\big]$.

Now consider the [[colimit]] 

$$
  C_\omega 
    \,\coloneqq\, 
  \colim_n C_n
$$ 

of this sequence of localizations. Clearly there is a canonical functor $L \colon C \to C_\omega$ and also a mediating map 
\[
  \label{MediatingMap}
  K 
    \,\colon\, 
  C_\omega 
    \longrightarrow
  D
\] 
such that $K\circ L = F$. In fact, one can prove that $K$ is [[conservative functor|conservative]].

\begin{definition}
A functor $F \colon C \to D$ is an **iterated localization** if $K$ (eq:MediatingMap) is an [[equivalence of categories|equivalence]].
\end{definition}

This makes $\big(\text{iterated localizations}, \text{conservative functors}\big)$ a(n homotopy) [[factorization system]] on $\mathbf{Cat}$ (considered as a 1-category with weak equivalences given by [[equivalence of categories|equivalences of categories]]).

## See also

* [[localization of a category]], [[category of fractions]]

* [[orthogonal factorization systems]]

* [[conservative functor]]


## References

The above is pretty much directly taken from:

* [[Joyal]]'s CatLab, Ex. 6.12 in: *[[joyalscatlab:Factorisation systems|Factorisation systems]]*

* [[André Joyal]], §11.14 and pp. 70 in: *Notes on quasi-categories* (2008) &lbrack;[pdf](http://www.math.uchicago.edu/~may/IMA/Joyal.pdf), [[JoyalNotesOnQuasiCategories.pdf:file]]&rbrack;

[[!redirects iterated localizations]]

