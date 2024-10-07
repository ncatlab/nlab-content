## Idea

An introspective theory is (very roughly) a category with an [[internal]] version of itself.

More specifically, an introspective theory is an [[essentially algebraic theory]] (a [[category with finite limits]]) such that every [[model]] of the theory itself contains a [[category with finite limits]], with an internal model of the same theory, and with a homomorphism from the same model into (the global aspect of) the internal model.

It is a minimal abstract context in which [[incompleteness theorem|Gödel incompleteness]] (more specifically, [[Loeb's theorem|Löb’s theorem]]) arises. Introspective theories were introduced by [[Sridhar Ramesh]] in his [2023 thesis](#Ramesh23).

## Definition

There are two useful equivalent definitions of introspective theory.

\begin{definition}
An **introspective theory** is

* a [[category with finite limits]] $T$, with

* an [[internal]] [[category with finite limits]] $C$ and

* an [[indexed functor]] $F$ from the [[self-indexing]] $T/-$ to $C$ (viewed as a $T$-[[indexed category|indexed]] [[category with finite limits]]):
\begin{centre}
    \begin{tikzcd}
        T^\mathrm{op} \arrow[r, shift left=7pt, "T/-" name=0] \arrow[r, shift right=7pt, "C"' name=1]
        \arrow["F", shorten <=3pt, shorten >=3pt, Rightarrow, from=0, to=1] & 
        \mathrm{LexCat}
    \end{tikzcd}
\end{centre}
\end{definition}

The following definition is equivalent to the above, but it more directly resembles the concept described in the introduction. For $C$ an internal category in $T$, we below denote by $\mathrm{Hom}_T(1, C)$ the **global aspect** of $C$: the induced category with set of objects $\mathrm{Hom}_T(1, \mathrm{Ob}_C)$ and set of arrows $\mathrm{Hom}_T(1, \mathrm{Arr}_C)$.

\begin{definition}
An **introspective theory** is

* a [[category with finite limits]] $T$, with

* an [[internal]] [[category with finite limits]] $C$,

* a [[finitely continuous functor|finite limit preserving functor]] $\mathcal{S}$ from $T$ to $\mathrm{Hom}_T(1, C)$, and

* a [[natural transformation]] $\mathcal{N}$ from the identity on $T$ to $\mathrm{Hom}_C(1, \mathcal{S}(-))$:
\begin{centre}
    \begin{tikzcd}
        T\arrow[rr, "\mathrm{id}" name=0]\arrow[dr, "\mathcal{S}"']&& 
        T\\
        & \mathrm{Hom}_T(1, C)\arrow[ur, "{\mathrm{Hom}_C(1, -)}"']\arrow["\mathcal{N}", shorten <=3pt, shorten >=3pt, from=0, Rightarrow]
    \end{tikzcd}
\end{centre}

\end{definition}

## Related Concepts

* [[Loeb's theorem|Löb’s theorem]]

* [[incompleteness theorem]]

## References

* {#Ramesh23} [[Sridhar Ramesh]], *Introspective Theories and Geminal Categories*, PhD thesis, Berkeley (2023) &lbrack;[escholarship:3mn0c475](https://escholarship.org/uc/item/3mn0c475), [[Ramesh-IntrospectiveTheories.pdf:file]]&rbrack;