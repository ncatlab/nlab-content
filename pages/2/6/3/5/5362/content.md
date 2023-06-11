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

Let $\mathbf{0}$ and $\mathbf{1}$ denote the [[initial object]] and [[terminal object]], respectively, of $Psh(A)$.  The terminlal presheaf $\mathbf{1}$ has two distinguished [[subobjects]] $\mathbf{0}\hookrightarrow \mathbf{1}$ and $\mathbf{1}\hookrightarrow \mathbf{1}$, which correspond to global points $\lambda^0,\lambda^1\in L(\mathbf{1})=Hom(\mathbf{1},L)$ of the subobject classifier.

\begin{definition}\label{LawvereInterval}
The triple $\mathfrak{L}=(L,\lambda^0,\lambda^1)$ is called the **Lawvere interval** for the [[topos]] $Psh(A)$. This object determines a [[cylinder functor]] given by taking the [[cartesian product]] with $L$, called the **Lawvere cylinder**.
\end{definition}
This is due to [Cisinski (2006), §1.3.9](#Cisinski06).

## Properties

\begin{proposition}
\label{LawvereIntervalIsFibrant}
With respect to any [[Cisinski model structure]] on $Psh(A)$, the subobject classifier $L$ (Def. \ref{LawvereInterval}) is [[fibrant object|fibrant]].
\end{proposition}
This is claimed at the end of [Cisinski (2006), §1.3.9](#Cisinski06) with reference to [[Sheaves in Geometry and Logic|MacLane & Moerdijk (1992), IV §10.1]], where an only vaguely similar statement about [[well-pointed toposes]] is discussed. We spell out the proof directly:
\begin{proof}
This follows since $L$ is equivalently the "monomorphism classifier" and using that in a [[Cisinski model structure]] the monomorphisms are precisely the [[cofibrations]].

The latter fact means that it is sufficient to show, given any [[monomorphism]] $A \hookrightarrow B$ and any [[morphism]] $A\to L$, that there exists a dashed [[lifting]] 

\begin{tikzcd}
  B 
    \ar[d, hook]
    \ar[r, "{ f }"] 
  & 
  L
  \\
  A
  \ar[ur, dashed, "{ \underline{f} }"{swap}]
\end{tikzcd}

(this will show even that $L \to \ast$ is an [[acyclic fibration]]).

Here $f \colon B \to L$ classifies a subobject of $B$, which we denote $C \hookrightarrow B$. The point now is that, with $B \hookrightarrow A$ being a monomorphism, the composite
$$
  C \hookrightarrow B \hookrightarrow A
$$
is a also subobject of $A$, and as such classified by some map to $L$, which we claim serves as the desired extension $\underline{f} \colon A \to L$. 
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

* the left rectangle is the [[fiber product]] $B \cap_A C$ computed via the [[pasting law for pullbacks]] to be isomorphic to $C$, using that $C$ is already a subobject of $A$.

This implies, again by the [[pasting law]], that the total square is a pullback, hence that the total bottom map classifies $C$. But $C$ was defined to be classified by $f$, 
and so the uniqueness of subobject classifying maps implies that the total bottom map equals $f$, which was to be shown. 
\end{proof}

For this reason, $\mathfrak{L}$ can be considered the universal [[cylinder object]] for [[Cisinski model structures]] on a presheaf topos.  


+-- {: .un_prop}
###### Proposition

Given any [[small set]] of monomorphisms in $Psh(A)$, there exists the smallest [[Cisinski model structure]] for which those monomorphisms are [[acyclic cofibrations]]. 

=--

By applying a theorem of [[Denis-Charles Cisinski]]. (...)


## Examples

Suppose $A=\Delta$ is the [[simplex category]], and  let $S$ consist only of the inclusion $\{1\}:\Delta^0\to\Delta^1$. Applying Cisinski's anodyne completion of $S$ by Lawvere's cylinder $\mathbf{\Lambda}_\mathfrak{L}(S,M)$, we get exactly the [[model structure for right fibrations|contravariant model structure]] on the category of simplicial sets.   

## References

* {#Cisinski06} [[Denis-Charles Cisinski]], *Les préfaisceaux comme types d'homotopie*, Astérisque **308** Soc. Math. France (2006), 392 pages &lbrack;[numdam:AST_2006__308__R1_0](http://www.numdam.org/item/?id=AST_2006__308__R1_0) [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf)&rbrack;
 


[[!redirects Lawvere intervals]]
[[!redirects Lawvere cylinder]]