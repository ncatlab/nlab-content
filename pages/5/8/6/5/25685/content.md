
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

\begin{definition}
Given a [[polynomial function]] with [[real number|real]] or [[complex number|complex]] [[coefficients]] $x \mapsto f(x)$, a **simple root** is a [[root]] of $x \mapsto f(x)$ such that the [[derivative]] of $x \mapsto f(x)$ evaluated at the root is [[invertible]]. 
\end{definition}

More generally, let $R$ be a [[commutative ring]]. The [[polynomial ring]] $R[x]$ is a [[differential algebra]] and thus has a derivative function $(-)':R[x] \to R[x]$. There is a canonical ring homomorphism $h:R[x] \to (R \to R)$ from the [[polynomial ring]] $R[x]$ to the [[function algebra]] $R \to R$ which assigns constant polynomials to [[constant functions]] in $R$ and the bare indeterminant to the [[identity function]] of $R$, which when [[uncurried]] leads to the evaluation of polynomials $(-)((-)):R[x] \times R \to R$. Since the set of polynomial functions in a commutative ring is a polynomial ring generated by the identity function, the situation for [[polynomial functions]] is simply a special case of the situation for polynomials. Thus, we have the following definition for general polynomials over [[fields]]:

\begin{definition}
Given a [[Heyting field]] $K$ and a [[polynomial]] $f \in K[x]$ with [[coefficients]] in $K$, a **simple root** is a [[root]] $a \in K$ of $f$ such that $f'(a)$, the evaluation of the [[derivative]] of $f$ at $a$, is [[invertible]].
\end{definition}

In [[classical mathematics]] (implying acceptance of the [[law of excluded middle]]), a simple root $a$ is a root that is not a multiple root: it is not the case that $(x-a)^2$ divides $f(x)$, or "not $f'(a) = 0$". But for the purposes of [[constructive mathematics]], it is preferable to state the condition as "$f'(a)$ is [[apartness|apart]] from $0$", or that $f'(a)$ is invertible. Hence the definitions above. 

## Related concepts

* [[root]]
* [[elementary symmetric polynomial]]
* [[unramifiable polynomial]]
* [[fundamental theorem of algebra]]

## References

* {#Ruitenberg91} [[Wim Ruitenberg]], *Constructing Roots of Polynomials over the Complex Numbers*, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract, **84** Centre for Mathematics and Computer Science, Amsterdam (1991) 107–128 &lbrack;[pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf), [[Ruitenberg-Roots.pdf:file]]&rbrack;

[[!redirects simple roots]]
