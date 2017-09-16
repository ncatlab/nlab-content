Given a [[function]] $f: X \to Y$ and a [[subset]] $S$ of $Y$, the __preimage__ (or __inverse image__) of $T$ under $f$ is a subset of $S$, consisting of those arguments whose values belong to $S$.  That is,
$$ f^*(S) = \{ a: X \;|\; f(a) \in S \} .$$
The traditional notation for $f^*$ is $f^{-1}$, but this can conflict the notation for an [[inverse function]] of $f$ (which indeed might not even exist).  This then suggests $f_*$ for the [[image]] of $f$.

We borrow $f^*$ from a notation for [[pullback]]s, and indeed a preimage is an example of a pullback:
$$ \array {
f^*(S)     & \hookrightarrow & X \\
\downarrow &                 & \downarrow f \\
S          & \hookrightarrow & Y
} $$

For a generalisation to [[sheaf|sheaves]], see [[inverse image]].