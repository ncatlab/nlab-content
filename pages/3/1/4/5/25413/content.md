[[!redirects geometric computad]]

# Contents 
* table of contents 
{: toc}

## Idea 

Geometric $n$-computads are [[free object|free]] [[geometric n-category| geometric n-categories]], whose notion of composition is modelled on [[manifold diagram|manifold diagrams]]. Geometric $n$-computads are a model for a [[semistrict n-category|semistrict]] flavor of [[n-categories]].

## Definition

\begin{terminology} We will say a [[manifold diagram|manifold $k$-diagram]] $(\mathbb{R}^k,f)$ is a *stratum $k$-type* if the diagram is of the form $(\mathrm{Cone}(S^{k-1}), \mathrm{cone}(\partial f))$. We call $(S^{k-1},\partial f)$ the *type boundary* of $f$.
\end{terminology}

Let $\mathcal{E} : \mathbf{Strat} \to \mathbf{Pos}$ denote the [entrance path poset functor](https://ncatlab.org/nlab/show/stratified+space#the_category_of_stratifications), that maps stratified spaces to their entrance path posets.

\begin{defn} A *geometric $n$-computad* is an $[n]$-graded set $C$ together with, for each $c \in C_i$, a stratum type $(\mathbb{R}^i, f_c)$ and a 'labeling' function $l_c : \mathcal{E}_0 f_c \to C_{\leq i}$ with $l_c\{0\} = c$, such that $k$-strata $s$ in $f_c$ have stratum type $f_{l_c(s)}$ and $l_{l_c(s)}$ factors through $l_c$ by the induced map $\mathcal{E}_0 f_{l_c(s)} \to \mathcal{E}_0 f_c$. 
\end{defn}

In words, a computad $C$ is a bunch of '$i$-morphisms' (indexed by the sets $C_i$) for $i \leq n$, and each morphism has a stratum type whose boundary is consistently labeled in lower-dimensional morphisms.

## Remarks

* The remarkable observation about geometric computads is the following.  Classically, [building computads](https://ncatlab.org/nlab/show/computad#globular_computads) is an inductive *two-step* process: namely, usually one constructs computads inductively by, in the $n$th step, adding generating $n$-morphisms with boundary in existing $(n-1)$-morphisms, and *then* passing to the closure under composition and coherence conditions (which, passing back and forth between "new composites" and "new coherences" is often a pretty infinite process). In geometric computads, this is process becomes unnecessary: boundaries of $n$-morphisms are manifold $(n-1)$-diagrams (or, if you work dually, cell $(n-1)$-diagrams) which already can express all the composites and isotopies you could possibly need. This makes geometric computads *really* easy to work with.

* While it is straight-forward to define geometric computads (and related notions, such as their functors and certain transformations), a comprehensive theory of computads is still in development.

## Related pages 

* [[manifold diagram]]

* [[geometric n-category]]

* [[homotopy.io]]
 

## References 

A definition and further discussion can be found in

* {#Dorn23} [[Christoph Dorn]], _Nine short stories about geometric higher categories_, 2023 ([pdf](https://cxdorn.github.io/assets/pdfs/nine-stories.pdf))

The notion has been the topic of several talks and blog posts.

* [[Christoph Dorn]], [From trusses to geometric computads to combinatorial manifold diagrams](https://cxdorn.github.io/research/trusses/) (2022)

* {#functors} [[Christoph Dorn]], [The categorical Pontryagin-Thom construction](https://cxdorn.github.io/tcptc/) (2022) contains definitions of functors and certain transformations of geometric computads.

The finitely generated case can be efficiently manipulated using the proof-assistant [[homotopy.io]]

* [[Jamie Vicary]] et. al, [Introducing homotopy.io: A proof assistant for geometrical higher category theory](https://tqft.math.tecnico.ulisboa.pt/seminars?id=6607) (2022)

[[!redirects geometric n-computad]]
[[!redirects geometric computads]]