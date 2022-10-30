+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

In earlier work \cite{chacaltana:2010ks, fubar, MR3046557}, we actually did stuff.

# Sandbox
* table of contents
{: toc}

# Section

# Another section

***

First of all, since $M_S$ belongs to a prefactorization system, it is closed under composites, pullbacks, and any intersections which exist.  Therefore, if we define $M' \coloneqq M \cap M_S$, then $M'$ satisfies the hypotheses of Theorem \ref{ConstructingOFS}, and so we have an OFS $(E',M')$.

Moreover, it is useful to notice that $E_S=$: this is an easy consequence of the fact that if $S\dashv T$, then $Sa\perp b\iff a\perp Tb$, since $f\perp Tu\iff Sf\perp u$ for each $u\in\hom(C)$, so that $S f $ is an isomorphism.

Now suppose given $f\colon A\to B$; we want to construct an $(E_S,M_S)$-factorization.  Let $v$ be the pullback of $T S f$ along the [[unit of an adjunction|unit]] $\eta_B \colon B \to T S B$.  The naturality square for $\eta$ at $f$ shows that $f$ factors through $v$, say $f = v w$.
$$\begin{array}{ccccc}
A & \\
 &\overset{w}\searrow\\
 && P &\overset{u}\to& T S A \\
 && {}^v\downarrow  && \downarrow^{T S f}\\
 && B &\underset{\eta_B}\to& T S B
\end{array}
$$ 
Since $T S f$ is evidently in $M_S=({}^\perp T(\hom(C)))^\perp\supseteq T(\hom (C))$, so is $v$; thus it suffices to find an $(E_S,M_S)$-factorization of $w$.

Let $w = n g$ be the $(E',M')$-factorization of $w$.  Since $M' \subseteq M_S$, it suffices to show that $g\in E_S$.  Note also that since $w$ is a first factor of the unit $\eta_A$, by passing to adjuncts we find that $S w$ is [[split monic]]: in the former diagram we have $u w=\eta_A$, so that the adjunct $\epsilon_{S A} \cdot S u\cdot  S n\cdot  S g=1$, hence also $S g$ is a split monic.  But $T S g$ is then also split monic, hence belongs to $M$ and thus also to $M'$ (since it obviously belong to $M_S=({}^\perp T(\hom(C)))^\perp\supseteq T(\hom (C))$).  Therefore, since $g\in E'$, the naturality square for $\eta$ at $g$ contains a lift: there is an $\alpha\colon X\to T S A$ such that in the diagram
$$\begin{array}{ccc}
A & \overset{\eta_A}\to & T S A \\
{}^g\downarrow && \downarrow^{T S g} \\
X &\overset{\eta_X}\to& T S X 
\end{array}$$
$\alpha\cdot g=\eta_A$ and $T S g \cdot \alpha=\eta_X$. Passing to adjuncts again, we find that $S g$ is also [[split epic]], since we can consider the diagram
$$\begin{array}{ccccc}
S A & \overset{S\eta_A}\longrightarrow & S T S A &\overset{\epsilon_{SA}}\longrightarrow & S A\\
{}^{S g}\downarrow && \phantom{aaa}\downarrow_{S T S g} &&\downarrow^{S g}\\
S X &\underset{S\eta_X}\longrightarrow & S T S X &\underset{\epsilon_{SX}}\longrightarrow & S X
\end{array}$$
and the commutativity
$$
S g \cdot \epsilon_{S A} \cdot S\alpha = \epsilon_{S X} S T S g \cdot S\alpha = \epsilon_{S X}\cdot S\eta_X = 1
$$
Hence $S g$ is an isomorphism; thus $g\in E_S$ as desired. $\blacksquare$


***
[[?]] [[Grothendieck inequality]] $&lt;>$
***
1. $[\mathcal{I},\mathcal{A}]$ is really just the underlying category with hom-collections given by $A_0(A,B)=V_0(I,\mathcal{A}(A,B))$.
2. $\mathcal{A}(-,-)$ is the fully faithful two-variable hom-functor from $A_0^{op}\times A_0\to V_0$, with $\mathcal{A}(f,g)$ defined as the composite $\mathcal{A}(B,C)\stackrel{l^{-1}r^{-1}}{\to}I\otimes\mathcal{A}(B,C)\otimes I\stackrel{f\otimes id\otimes g}{\to}\mathcal{A}(C,D)\otimes\mathcal{A}(B,C)\otimes\mathcal{A}(A,B)\stackrel{(\circ^{\mathcal{A}})^2}\mathcal{A}(A,D)$ in $V_0$
3. $[\mathcal{I},F]$ is the functor from $A_0$ to $B_0$ underlying the enriched functor $F$. This is defined by letting $Ff$ be the composite $I\stackrel{f}{\to}\mathcal{A}(A,B)\stackrel{F_{A,B}}\mathcal{B}(FA,FB)$ where $F_{A,B}$ is the family of morphisms in $V_0$ defining the enriched functor $F$.
4. The natural transformation $\bar F\colon\cat A(-,-)\to\cat B(F-,F-)$ has for its components exactly the maps $F_{A,B}$ above: i.e. $\bar F_{A,B}=F_{A,B}$.
*
*

category: meta


[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects ??? ????]]
[[!redirects Featured math : Quora]]