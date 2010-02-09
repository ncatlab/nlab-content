
#Contents#
* automatic table of contents goes here
{:toc} 

## Definition

A **section** of a [[morphism]] $f : A \to B$ in some [[category]] is a **right-[[inverse]]**: a [[morphism]] $\sigma : B \to A$ such that
$$
  f \circ g : B \stackrel{\sigma}{\to} A \stackrel{f}{\to} B
$$
equals the [[identity morphism]] on $B$.

## Split idempotents

In the case case that $f$ has a section $\sigma$, $f$ may also be called a [[retraction]] or **cosection** of $\sigma$, $B$ may be called a [[retract]] of $A$, and the entire situation is said to split the [[idempotent]]
$$
  A \stackrel{f}{\to} B \stackrel{\sigma}{\to} A
  \,.
$$

A **[[split epimorphism]]** is a morphism that *has* a section; a **[[split monomorphism]]** is a morphism that *is* a section.

A fork diagram 
$$A \underoverset{\partial_0}{\partial_1}{\rightrightarrows} B \overset{p}{\rightarrow} C $$

is a **split fork** if the morphism $p$ is a retract, in the category of arrows, of the morphism $\partial_1$, via a section of the pair $(\partial_0,p):\partial_1\to p$. In other words, there exist a pair (section) $(t,s):p\to\partial_1$ of $(\partial_0,p)$ such that the diagram 
$$\array{
B &\stackrel{t}\rightarrow & A&\stackrel{\partial_0}\rightarrow &B\\
\downarrow p &&\downarrow {\partial_1} &&\downarrow p\\
C&\stackrel{s}\rightarrow & B&\stackrel{p}\rightarrow& C
}$$
commutes and its both horizontal composites are identities. It is easy to check that every split fork is a [[coequalizer]], which is then called a **split coequalizer**.
Clearly any functor sends a split coequalizer to a split coequalizer, hence every split coequalizer is an **[[absolute coequalizer]]** (coequalizer stable under all functors).

## Sections of bundles and sheaves

If one thinks of $f : A \to B$ as a [[bundle]] then its sections are sometimes called [[global section]]s. This leads to a notion of global sections of [[sheaves]] and further of objects in a general [[topos]]. See 

* [[global section]]

for more on this.


[[!redirects sections]]
[[!redirects cross section]]
[[!redirects cross-section]]
[[!redirects right inverse]]
[[!redirects right-inverse]]
[[!redirects cross sections]]
[[!redirects cross-sections]]
[[!redirects right inverses]]
[[!redirects right-inverses]]