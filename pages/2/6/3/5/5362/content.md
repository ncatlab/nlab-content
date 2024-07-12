[[!redirects lawvere interval]]
[[!redirects lawvere interval]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

Let $A$ be a [[small category]], and let $Psh(A)=Set^{A^{op}}$ be the [[category of presheaves]] on $A$. Since $Psh(A)$ is a [[Grothendieck topos]], it has a unique [[subobject classifier]], $L$.  

Let $\mathbf{0}$ and $\mathbf{1}$ denote the [[initial object]] and [[terminal object]], respectively, of $Psh(A)$.  The terminal presheaf $\mathbf{1}$ has two distinguished [[subobjects]] $\mathbf{0}\hookrightarrow \mathbf{1}$ and $\mathbf{1}\hookrightarrow \mathbf{1}$, which correspond to global points $\lambda^0,\lambda^1\in L(\mathbf{1})=Hom(\mathbf{1},L)$ of the subobject classifier.

\begin{definition}\label{LawvereInterval}
The triple $\mathfrak{L}=(L,\lambda^0,\lambda^1)$ is called the **Lawvere interval** for the [[topos]] $Psh(A)$. This object determines a [[cylinder functor]] given by taking the [[cartesian product]] with $L$, called the **Lawvere cylinder**.
\end{definition}
This is due to [Cisinski (2006), §1.3.9](#Cisinski06).

By Prop. \ref{LawvereIntervalIsFibrant} below, the Lawvere interval $\mathfrak{L}$ may be regarded as the universal [[cylinder object]] for [[Cisinski model structures]] on presheaf toposes.  


## Properties

The Lawvere cylinder is universal in the sense that any $L$-homotopy lifts to a homotopy for any other good [[cylinder object]].

\begin{proposition}
Let $A$ be an object of a topos. Given a diagram
$$
A \amalg A \stackrel{(\delta^0, \delta^1)}{\to} C \stackrel{\sigma}{\to} A
$$
where the copies of $A$ are disjoint [[subobjects]] of $C$ splitting $\sigma$, then there is a morphism of cylinders $C \to L \times A$.
\end{proposition}
\begin{proof} 
  Let $\chi^i : C \to L$ be the characteristic function for $\delta^i$. That the copies of $A$ are disjoint subobjects implies $\chi^0 \leq \neg \chi^1$, and so $\chi^0 \vee \chi^1 \leq\chi^1 \vee \neg \chi^1$.

  Since $x \mapsto x \vee \neg x$ is the characteristic function of $\lambda : 1 \amalg 1 \to L$, the morphism $(\chi^1, \sigma) : C \to L \times A$ pulls $A \times \lambda$ back to a subobject containing $\delta$. Compatibility with $\sigma$ is obvious, and so it is a morphism of cylinder objects.
\end{proof}

In a topos, [[lifting problems]] against [[monomorphisms]] can be described in terms of [[partial maps]], giving an elementary characterization of [[trivial fibrations]]:

\begin{proposition} Let $p : X \to S$. Suppose the [[partial map classifier]] $X \hookrightarrow \mathrm{Opt}_S(X)$ exists in the [[slice category]] over $S$. Then $\mathrm{Opt}_S(X)$ represents the presheaf (in $A$) of diagrams of the form
\begin{tikzcd}
  B \arrow[d, hook] \arrow[r] & X \arrow[d, "p"]
  \\
  A \arrow[r] & S
\end{tikzcd}
modulo the identification of equivalent subobjects $B \subseteq A$.
\end{proposition}

\begin{corollary} If $p : X \to S$ is an arrow in a topos $\mathbf{E}$, it has the [[right lifting property]] against monomorphisms iff the restriction $X \times L \to \mathrm{Opt}_S(X)$ is a split epi.
\end{corollary}
\begin{proof} $X \times L$ represents the presheaf (in $A$) of all such diagrams that have a filler $A \to X$, since $X \to A$ determines the lower triangle and from that, $X \to L$ determines the upper triangle.

Thus $p$ has the claimed property iff $X \to L \to \mathrm{Opt}_S(X)$ represents an epimorphism of presheaves, which is equivalent to being a split epi.
\end{proof}

\begin{proposition} If $p : X \to S$ is an arrow in a topos $\mathbf{E}$, it has the [[right lifting property]] against monomorphisms iff the insertion $X \hookrightarrow \mathrm{Opt}_S(X)$ has a retraction.
\end{proposition} 
\begin{proof} By the properties of [[partial map classifier]]s, every lifting problem has a unique factorization
\begin{tikzcd}
  B \arrow[d, hook] \arrow[r] & X \arrow[r, equals] \arrow[d, hook] & X \arrow[d, "p"]
  \\
  A \arrow[r] & \mathrm{Opt}_S(X) \arrow[r] & S
\end{tikzcd}
where the left square is a pullback. So $p$ has the right lifting property against the mono $X \to \mathrm{Opt}_S(X)$ iff it has the right lifting property against all monos.
\end{proof}

\begin{corollary} If $p : X \to S$ is an arrow in a topos $\mathbf{E}$, then $ X \hookrightarrow \mathrm{Opt}_S(X) \to S $
is a factorization into a monomorphism followed by a morphism with the [[right lifting property]] against monomorphisms.
\end{corollary}
\begin{proof} In any topos (in particular $\mathbf{E}_{/S}$), the both inclusions $\mathrm{Opt}(X) \hookrightarrow \mathrm{Opt}(\mathrm{Opt}(X))$ are split by the operation of taking the intersection of domains.
\end{proof}
The argument spelled out in the case of $X = 1$ and $\mathrm{Opt}(X) = L$ is spelled out in

\begin{proposition}
\label{LawvereIntervalIsFibrant}
The [[subobject classifier]] in any [[topos]] is an [[injective object]], whence the Lawvere interval $L$ (Def. \ref{LawvereInterval}) is a [[fibrant resolution]] of the [[terminal object]] in any [[Cisinski model structure]] on $Psh(A)$.
\end{proposition}
This is highlighted at the end of [Cisinski (2006), §1.3.9](#Cisinski06) with reference (up to a typo) to [[Sheaves in Geometry and Logic|MacLane & Moerdijk (1992), IV §10.1]]:
\begin{proof}
Recall that for $L$ to be an [[injective object]] means that every solid [[span]] as below, where the vertical [[map]] is a [[monomorphism]], admits a dashed [[lifting]] as shown:

\begin{tikzcd}
  B 
    \ar[d, hook]
    \ar[r, "{ f }"] 
  & 
  L
  \ar[d, gray]
  \\
  A
  \ar[ur, dashed, "{ \underline{f} }"{swap}]
  \ar[r, gray]
  &
  \color{gray}\ast
\end{tikzcd}

Since in a [[Cisinski model structure]], by definition, the monomorphisms are precisely the [[cofibrations]], injective objects here are equivalently those for which the [[terminal object|terminal]] [[map]] $L \to \ast$ is an [[acyclic cofibration]].

Hence assuming the solid diagram above, we show the existence of $\underline{f}$:

Here $f \colon B \to L$ classifies a subobject of $B$, which we denote $C \hookrightarrow B$. The point now is that, with $B \hookrightarrow A$ being a monomorphism, the composite
$$
  C \hookrightarrow B \hookrightarrow A
$$
exhibits $C$ also as a subobject of $A$, which as such is classified by some map $\underline{f} \colon A \to L$, and we claim that this serves as the desired extension. 
To see that indeed this $\underline{f}$ makes the above triangle commute, consider the following [[commuting diagram]]:

\begin{tikzcd}
  C
  \ar[d, hook]
  \ar[r, equals]
  \ar[dr, phantom, "{ \scalebox{.6}{(pb)} }"]
  &
  C 
    \ar[d, hook]
    \ar[r] 
    \ar[ddr, phantom, "{ \scalebox{.6}{(pb)} }"]
  & 
  \ast 
    \ar[dd]
  \\
  B 
  \ar[r, equals]
  \ar[d, equals]
  \ar[dr, phantom, "{ \scalebox{.6}{(pb)} }"]
  & 
  B \ar[d, hook]
  &
  \\
  B \ar[r, hook]
  &
  A \ar[r, "{ \underline{f} }"{swap}] & L
\end{tikzcd}

Here 

* the right rectangle is the [[pullback]] square that witnesses $\underline{f}$ as the classifying map of $C \hookrightarrow A$, by definition,

* the left rectangle is the [[fiber product]] $B \cap_A C$ computed via the [[pasting law for pullbacks]] to be isomorphic to $C$, using that $C$ is already a subobject of $A$ (which gives the factorization in the middle) and then using (for the two squares on the left) that:

  1. the [[fiber product]] of a monomorphism with itself is its [[domain]] ([this Prop.](monomorphism#BasicCharacterizationOfMonomorphisms)),

  1. [[isomorphisms]] are preserved by pullback ([this Prop.](pullback#PullbackPreservesMonomorphisms)).

This implies, again by the [[pasting law]], that the total square is a pullback, hence that the total bottom map classifies $C$. But $C$ was defined to be classified by $f$, 
and so the uniqueness of subobject classifying maps implies that the total bottom map equals $f$, which was to be shown. 
\end{proof}



 

## References

* {#Cisinski06} [[Denis-Charles Cisinski]], *Les préfaisceaux comme types d'homotopie*, Astérisque **308** Soc. Math. France (2006), 392 pages &lbrack;[numdam:AST_2006__308__R1_0](http://www.numdam.org/item/?id=AST_2006__308__R1_0) [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf)&rbrack;
 


[[!redirects Lawvere intervals]]
[[!redirects Lawvere cylinder]]