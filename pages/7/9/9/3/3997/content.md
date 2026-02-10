

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


* table of contents
{: toc}

## Definition

\begin{definition}
  \label{CreatedLimit}
  Let $F\colon C \to D$ be a [[functor]] and $J\colon I \to C$ a [[diagram]]. We say that $F$ __creates__ limits of $J$ if it both [[lifted limit|lifts]] and [[reflected limit|reflects]] limits of $J$.
\end{definition}

Explicitly, this says that any [[limit|limiting]] [[cone]] $(d, \eta)$ for $F \circ J$ has, up to isomorphism, a unique cone $(c, \alpha)$ over $J$ with $(F c, F \cdot \alpha) \cong (d, \eta)$ in the category of cones over $F \circ J$, and moreover $(c, \alpha)$ is limiting. This implies that a cone over $J$ in $C$ is limiting if and only if its image in $D$ is limiting.

Of course, a functor $F$ creates a [[colimit]] if $F^{op}$ creates the corresponding limit.

If $F$ creates all limits or colimits of a given type (i.e. over a given category $I$), we simply say that $F$ creates that sort of limit (e.g. $F$ creates products, $F$ creates equalizers, etc.).

\begin{remark}
  Suppose $F$ creates limits of $J$, and $F \circ J$ has at least one limiting cone. Then $F$ additionally __[[preserved limit|preserves]]__ limits of $J$.
\label{vacuous}
\end{remark}

This follows from [[lifted limit#vacuousPreserve|this remark]] on the page for [[lifted limit|lifting of limits]]. Thus, creation of limits either holds vacuously, or holds together with preservation.

\begin{remark}
  Sometimes, we additionally require $F \circ J$ to have a limit for $F$ to creates limits of $J$. In that case, creation is equivalent to preservation, reflection and lifting.
\end{remark}

### Strictness

The definitions given above are all "up to isomorphism", i.e. they satisfy the [[principle of equivalence]].  The definition in [[Categories Work]] is additionally *strict*: it requires that for every limiting cone $L$ over $F J$ in $D$ there exists a *unique* cone $L'$ over $J$ which is mapped *exactly* to $L$, and this $L'$ is a limit of $J$.  This is used in stating the version of the [[monadicity theorem]] that characterizes the [[category of algebras for a monad]] up to [[isomorphism]] rather than [[equivalence of categories]]. For [[amnestic functor|amnestic]] [[isofibrations]] the strict and the non-strict notion are equivalent.

\begin{proposition}
  \label{strictCreationImpliesCreation}
  Suppose a functor $F \colon C \to D$ strictly creates limits of $J$. Then it creates limits of $J$.
\end{proposition}

\begin{proof}
  Strictly lifting limits for $J$ already implies lifting limits for $J$, so it suffices to show that $F$ reflects limits of $J$. Take a cone $(x, \eta)$ for $J$ such that $(F(x), F \cdot \eta)$ is a limit cone for $F \circ J$. Since $F$ strictly lifts limits for $J$, there exists a unique cone $(x', \eta')$ over $J$ satisfying $(F(x'), F \cdot \eta') = (F(x), F \cdot \eta)$, and moreover $(x', \eta')$ is a limit of $J$. But clearly $(x, \eta)$ is such a lift, implying $(x, \eta) = (x', \eta')$ and thus is a limit for $J$. Hence, $F$ reflects limits of $J$, as required.
\end{proof}

In practice, many functors that create limits do so strictly, and it can be more straightforward to verify strict creation than to separately verify reflection and lifting.

## Examples

\begin{proposition}\label{MonadicFunctorsCreateLimits}
**([[monadic functors]] [[created limit|create limits]])**
A [[monadic functor]] 

1. creates all limits that exist in its [[codomain]];

1. creates all colimits that exist in its codomain and are preserved by the corresponding monad (or, equivalently, by the monadic functor itself).  

\end{proposition}
(e.g. [MacLane 71, Exercise IV.2.2 (p. 138)](#MacLane71))



Creation of a particular sort of [[split coequalizer]] figures prominently in Beck's [[monadicity theorem]].

\begin{proposition}
  \label{evaluationFunctorsCollectivelyStrictlyCreateLimits}
  The forgetful functor $U \colon [A, C] \to C^{ob(A)}$ strictly creates all limits - so, when the limit exists in the latter category, it exists in the functor category and is computed pointwise.
\end{proposition}

\begin{proof}
  Using [[limit#limitProductCategoryComponentwise|limits in product categories are computed componentwise]], if a limit for $U \circ D \colon J \to C^{ob(A)}$ exists, then it is a limit cone in each factor.

We can then apply [[representability determines functoriality]] - define a bifunctor $P \colon C^{op} \times A \to \mathbf{Set}$ on objects by $P(c, a) = Nat(\Delta_c, D(-)(a))$, where $\Delta_c \colon J \to C$ is a constant functor. Having a limit cone in each factor says that $P$ is representable in the $C^{op}$ argument by some $La$ for each $a$; parametrised representability then guarantees that this lifts uniquely to a functor $L \colon A \to C$ that has a cone over $D$, and moreover this cone is a limit. Thus, $U$ strictly creates limits.
\end{proof}


## Creation of non-existing limits

It seems that the notion of "creating a limit" is used most frequently when the limits exist in the codomain.  One may want to extend the terminology to cases when such limits don't exist, which would require making a choice about whether a non-existing limit should be regarded as "created".

In [[Categories Work]], and in the definition above, the convention is that a functor creates *all* limits that do not exist in its codomain.  In this case, the more generally applicable definition could be stated as "$F$ creates limits for $J$ if $J$ has a limit whenever $F\circ J$ has a limit, and *in that case* limits of $J$ are preserved and reflected by $F$."

On the other hand, one might argue that it doesn't make sense to regard a limit that exists in the domain as being "created by the functor" if the limit in the codomain doesn't even exist.  In this case the more generally applicable definition could be stated as "$F$ creates limits for $J$ if $J$ has a limit whenever $F\circ J$ has a limit, and *furthermore in all cases* limits of $J$ are preserved and reflected by $F$."

Finally, one might even argue that based on the meaning of the English word "created", only something that exists can be created at all.  In this case the more generally applicable definition could be stated as "$F$ creates limits for $J$ if $J$ and $F\circ J$ both have limits, and furthermore limits of $J$ are preserved and reflected by $F$."


## Remarks

[Kissinger](https://raw.githubusercontent.com/punkdit/categories/26b751bbcbe6765fe447e805629ff6416f4c38b1/gmane/science/mathematics/categories/6644) suggested a concise way to state creation/preservation/etc. of limits.  However, there is [some dispute](https://nforum.ncatlab.org/discussion/7024/lifted-limit/?Focus=56765#Comment_56765) about its correctness.


## Related pages

* [[preserved limit]]

* [[reflected limit]]

* **created limit**

* [[lifted limit]]


## References

* {#MacLane71} [[Saunders Mac Lane]], Definition V.1 in: _[[Categories for the Working Mathematician]]_ (1971)


* [[Jiří Adámek]], [[Horst Herrlich]], [[George E. Strecker]], Definition 13.17(2) in: _[[Abstract and Concrete Categories]]_.


* [[Emily Riehl]], §3.3 in: *[[Category Theory in Context]]*, Dover Publications (2017) &lbrack;[pdf](https://emilyriehl.github.io/files/context.pdf), [book website](https://math.jhu.edu/~eriehl/context/)&rbrack;
  


[[!redirects created limits]]
[[!redirects creation of limits]]
[[!redirects created colimit]]
[[!redirects created colimits]]
[[!redirects creation of colimits]]

[[!redirects creates limits]]
[[!redirects creates colimits]]

[[!redirects closure under limits]]
[[!redirects closure under colimits]]