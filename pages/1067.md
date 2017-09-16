#Idea#

#Definition#

A ($\mathbb{Z}$-graded) **chain complex** in a [[pre-additive category]] $C$ is a sequence of objects $V_n$, $n\in\mathbb{Z}$, and morphisms $d_n:V_n \to V_{n-1}$ called [[differential|differentials]]:
$$ \cdots \overset{d_3}{\to} V_2 \overset{d_2}{\to} V_1 \overset{d_1}{\to} V_0 \overset{d_0}{\to} V_{-1} \overset{d_{-1}}{\to} \cdots$$
such that $d_n d_{n+1} = 0$ (the [[zero morphism]]) for each $n$.  More precisely, this is a _homologically graded_ chain complex, in which the differentials lower degree; if we rename $V_n$ to $V_{-n}$ so that the differentials raise degree, it becomes a _cohomologically graded_ chain complex or a **cochain complex**.  Common choices for $C$ include [[Ab]], [[Vect]], or $R-Mod$, in which case we obtain the familiar definition of an (unbounded) chain complex of abelian groups, vector spaces, or modules.

Frequently one also considers $\mathbb{N}$-graded (or _nonnegatively graded_) chain complexes, which can be identified with $\mathbb{Z}$-graded ones for which $V_n=0$ when $n\lt 0$.  Similarly, an $\mathbb{N}$-graded _cochain_ complex is a cochain complex for which $V_n=0$ when $n\lt 0$, or equivalently a chain complex for which $V_n=0$ when $n\gt 0$.

## Using a translation

Note that in particular, a chain complex is a [[graded object]] with extra structure.  This extra structure can be codified as a map of graded objects $d:V\to T V$, where $T$ is the 'shift' endofunctor of the category $Gr(V)$ of graded objects in $C$, such that $T(d) \circ d = 0$.  More generally, in any pre-additive category $G$ [[category with translation|with translation]] $T : G \to G$, we can define a **chain complex** to be a [[differential object]] $d_V : V \to T V$ such that $V \stackrel{d_V}{\to} T V \stackrel{T(d_V)}{\to} T T V$ is the [[zero morphism]].  When $G= Gr(C)$ this recovers the original definition.

