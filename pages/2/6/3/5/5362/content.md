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

Let $\mathbf{0}$ and $\mathbf{1}$ denote the [[initial object]] and [[terminal object]], respectively, of $Psh(A)$.  The presheaf $1$ has exactly two [[subobject]]s $\mathbf{0}\hookrightarrow \mathbf{1}$ and $\mathbf{1}\hookrightarrow \mathbf{1}$.  These determine the unique two elements $\lambda^0,\lambda^1\in L(\mathbf{1})=Hom(\mathbf{1},L)$.      

We call the triple $\mathfrak{L}=(L,\lambda^0,\lambda^1)$ the **Lawvere interval** for the [[topos]] $Psh(A)$.  This object determines a unique [[cylinder functor]] given by taking the [[cartesian product]] with an object.  We will call this endofunctor the **Lawvere cylinder** .

## Properties

+-- {: .un_prop}
###### Proposition

With respect to the [[Cisinski model structure]] on $Psh(A)$, the object $L$ is fibrant.

=--

+-- {: .proof}
###### Proof

Given any [[monomorphism]] $A\to B$ and any morphism $A\to L$, there exists a lifting $B\to L$.  

To see this, notice that the morphism $A\to L$ classifies a subobject $C\hookrightarrow A$.  However, composing this with the [[monomorphism]] $A\hookrightarrow B$, this monomorphism is classified by a morphism $B\to L$ making the diagram commute.  

=--

For this reason, $\mathfrak{L}$ can be considered the universal cylinder object for Cisinski model structures on a presheaf topos.  


+-- {: .un_prop}
###### Proposition

Given any [[small set]] of monomorphisms in $Psh(A)$, there exists the smallest [[Cisinski model structure]] for which those monomorphisms are trivial cofibrations. 

=--

By applying a theorem of [[Denis-Charles Cisinski]]. (...)


## Examples

Suppose $A=\Delta$ is the [[simplex category]], and  let $S$ consist only of the inclusion $\{1\}:\Delta^0\to\Delta^1$. Applying Cisinski's anodyne completion of $S$ by Lawvere's cylinder $\mathbf{\Lambda}_\mathfrak{L}(S,M)$, we get exactly the [[model structure for right fibrations|contravariant model structure]] on the category of simplicial sets.   

[[!redirects Lawvere intervals]]