# Iteration theory

* table of contents
{: toc}

## Idea

An __iteration theory__ is an [[algebraic theory]] that supports iteration on its operators.

In particular, in an iteration theory, any equation 

$$ x = t $$

has a well behaved solution, $t^\dagger$, such that $t[t^\dagger/x]=t^\dagger$. 
More generally, any finite sequence of equations has a solution,

$$ x_1 = t_1, x_2 = t_2, \dots x_n = t_n$$

In general, $t_i$'s may have other free variables too. 

Keeping it simple for a moment, suppose for a second that $n=1$ and $t$ has just one free variable, $x$. For any algebra $A$, the  term is interpreted as a function $\llbracket t\rrbracket:A\to A$, and the solution $t^\dagger$ is interpreted as a constant in $\llbracket t^\dagger\rrbracket\in A$, which is a fixed point for the function $\llbracket t\rrbracket$. Thus an iteration theory provides canonical fixed points for equations, in every algebra.

## Definition

Let $T$ be an abstract [[clone]]. It is a _Conway theory_ when it is equipped with a family of operations

$$ \dagger_{m,n} : T(m+n)^m \to T(n)^m $$

such that, for $f\in T(m+n)^m$, (omitting subscripts):

$$ f^\dagger(i) \quad = \quad f(i) \rhd j. \begin{cases} f^\dagger(j) & j\in m \\ \eta(j) & j\in n\end{cases}$$

and satisfying axioms:

* parameter identity: $((1_n \oplus g) \circ f)^\dagger = g \circ f ^\dagger$ where $f:n \to n+p, \ g:p \to q$

* composition identity: $\langle (\langle f , \ 0_m \oplus 1_p \rangle \circ g)^\dagger , 1_p \rangle \circ f = (\langle g , \ 0_n \oplus 1_p \rangle \circ f)^\dagger$ where $f:n \to m+p, \ g:m \to n+p$

* double dagger identity: $(\langle 1_n , \ 1_n \rangle \oplus 1_p) \circ f)^\dagger = (f^\dagger)^\dagger$ where $f: n \to n+n+p$

in the corresponding [[Lawvere theory]].

It is an _iteration theory_ if the operations also satisfy:

* commutative identity: $\langle (\rho_1 \oplus 1_p) \circ (f \circ \rho)_1 , \ ... \ , \ (\rho_m \oplus 1_p) \circ (f \circ \rho)_m) \rangle ^\dagger = ((\rho \oplus 1_p) \circ f)^\dagger \circ \rho$ 

where $f: n \to m+p, \ \rho: m \to n$ is a surjective base morphism and $\rho_i: m \to m$ are base with $\rho \circ \rho_i = \rho$ for every i.


This connects with the basic idea, because $f\in T(m+n)^m$ can be thought of as a sequence of $m$ terms with $m+n$ variables, and the solution $f^\dagger$ comprises $m$ terms just having the $n$ free variables. 

## Properties

To equip an abstract clone $T$ with the structure of a Conway theory is to equip the corresponding [[Lawvere theory]] with the structure of a [[traced monoidal category]] for the categorical product structure. 

## Continuous theories

An abstract clone $T$ is _continuous_ if each set $T(n)$ is equipped with the structure of a [[cpo]], and the clone operations are continuous. 

If $T$ is also pointed, i.e. each $T(n)$ has a least element $\bot$, then $T$ has a canonical structure of a Conway theory.

For any $f\in T(m+n)^m$, we define an endofunction 
$F_f : T(n)^m \to T(n)^m$ by

$$ F_f (g) \quad = \quad f(i) \rhd j. \begin{cases} g(j) & j\in m \\ \eta(j) & j\in n\end{cases}$$

and then use [[Tarski]]'s [[fixed point]] theorem to define

$$ f^\dagger \quad = \quad \bigvee_{i=1}^\infty (F_f)^n(\bot) .$$



## References 

The ideas originated in the work by Calvin C. Elgot in the 1970s. A textbook reference is:

* Stephen L. Bloom & Zoltán Ésik , _Iteration theories_, Springer 1993. ([citeseer](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.363.3634))

The connection with traced monoidal categories is due to [[Masahito Hasegawa]] and [[Martin Hyland]], see Theorem 3.1 of:

* {#Hasegawa97} [[Masahito Hasegawa]], _Recursion from Cyclic Sharing: Traced Monoidal Categories and Models of Cyclic Lambda Calculi_, Proc. 3rd International Conference on Typed Lambda Calculi and Applications (TLCA 1997). Springer LNCS1210, 1997 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.31))

This setting is further studied by [[Alex Simpson]] and [[Gordon Plotkin]] in 

* [[Alex Simpson]] and [[Gordon Plotkin]]. _Complete Axioms for Categorical Fixed-point Operators_. Proc. LICS 2000. [pdf](https://homepages.inf.ed.ac.uk/gdp/publications/fixpoints.pdf)

[[!redirects Conway theory]]
