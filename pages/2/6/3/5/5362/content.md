[[!redirects lawvere interval]]
[[!redirects lawvere interval]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $A$ be a [[small category]], and let $Psh(A)=Set^{A^{op}}$ be the [[category of presheaves]] on $A$. Since $Psh(A)$ is a [[Grothendieck topos]], it has a unique [[subobject classifier]], $L$.  

Let $\mathbf{0}$ and $\mathbf{1}$ denote the [[initial object]] and [[terminal object]], respectively, of $Psh(A)$.  The terminlal presheaf $\mathbf{1}$ has two distinguished [[subobjects]] $\mathbf{0}\hookrightarrow \mathbf{1}$ and $\mathbf{1}\hookrightarrow \mathbf{1}$, which correspond to global points $\lambda^0,\lambda^1\in L(\mathbf{1})=Hom(\mathbf{1},L)$ of the subobject classifier.

\begin{definition}
\label{LawereInterval}
The triple $\mathfrak{L}=(L,\lambda^0,\lambda^1)$ is called the **Lawvere interval** for the [[topos]] $Psh(A)$. This object determines a [[cylinder functor]] given by taking the [[cartesian product]] with $L$, called the **Lawvere cylinder**.
\end{definition}
This is due to [Cisinski (2006), §1.3.9](#Cisinski06).

## Properties

+-- {: .un_prop}
###### Proposition

With respect to any [[Cisinski model structure]] on $Psh(A)$, the object $L$ (Def. \ref{LawereInterval} is [[fibrant object|fibrant]].

=--

+-- {: .proof}
###### Proof

This follows from the fact that $L$ is a [[subobject classifier]], hence a "monomorphism classifier" and that in a [[Cisinski model structure]] the monomorphisms are precisely the [[cofibrations]].

The latter fact means that it is sufficient to show, given any [[monomorphism]] $A \to B$ and any [[morphism]] $A\to L$, that there exists a dashed [[lifting]] 

\begin{tikzcd}
  A 
    \ar[d, hook]
    \ar[r] 
  & 
  L
  \\
  B
  \ar[ur, dashed]
\end{tikzcd}

First, the morphism $A\to L$ classifies a subobject $C\hookrightarrow A$.  Moreover, composing this with the [[monomorphism]] $A\hookrightarrow B$, the resulting monomorphism (now a subobject of $B$) is classified by a morphism $B\to L$ making the diagram commute.  

=--

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