
#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Orientals are "oriented simplices": the $n$-th oriental is the simplicial $n$-simplex equipped with source and target relations, assigning to each $k$-face a set of $(k-1)$-faces called its source and a set of $(k-1)$-faces called its target, subject to some natural axioms. Each oriental freely generates (see below) a structure of a [[strict omega-category]] $O(\Delta^n)$, such that $k$-morphisms in $O(\Delta^n)$ are pasting diagrams of $k$-faces in $\Delta^n$.

One of the axioms is a [[globular set|globularity axiom]], which says that the source of a source (that is, the union of sources of all $(k-1)$-faces in the source of a $k$-face) equals the source of the target, and similarly that the target of a source equals the target of the target. Thus, orientals mediate between the [[simplicial set|simplicial]] and the [[globular set|globular]] world of [[higher category theory|infinity-categories]].

The first few orientals look as follows:

+-- {: .query}
{:response: style="color:#930; font-size:0.9em;margin-left:2em;"}
{:response2: style="font-size:0.9em;margin-left:3em;"}


{: response}Here's the same figure, in SVG. I think it looks better. Opinions may vary, however. -- Jacques

In principle I think the SVG is great, always better than embedded images. This particular one is rendering a bit weird though on my screen; the letters are covered up. 

{: response}
Weird! Renders rather differently in MovableType versus in Instiki. So much for portability! Anyway, this version should look better. -- Jacques

{: response2}
Mmm I think it might be a bit better but it's still not rendering quite right. The last few pixels of each equation as well as some of the numbers seem to be getting cut off. -- Bruce

Need a diagrams package for Instiki. I had an idea based on modifying itexml to translateterms eg. in an \xymatrix formula into MathML, but _leave the & symbols alone_. Now you have an interim XHTML page with MathML on it, with the commutative diagrams rendered in math but not displayed in a matrix format. Then you get javascript to query the HTML elements, ask them "what is your size?". It uses this information to lay out a diagram, resulting in the final HTML page with the diagram layed out. -- Bruce

=--

$$
\array{\arrayopts{\rowalign{center}}
O(\Delta^0) = & \{ 0\} \\
O(\Delta^1) = & \left\{ 0 \to 1\right\} \\
O(\Delta^2) = & \left\{
\array{\begin{svg}
[[!include oriental/Delta2]]
\end{svg}}
\right\}\\
O(\Delta^3) = & \left\{
\array{\begin{svg}
[[!include oriental/Delta3]]
\end{svg}}\right\}\\
O(\Delta^4) = & \left\{
\array{\begin{svg}
[[!include oriental/Delta4]]
\end{svg}}
\right\}
}
$$

##As cosimplicial $\omega$-category##

The construction of orientals is designed to be compatible with face and degeneracy maps. Therefore the orientals arrange themselves into a cosimplicial [[omega-category]], i.e., a functor
$$
  O : \Delta \to \omega Cat
$$
from the [[simplex category]] $\Delta$ to the category of [[strict omega-category|strict omega-categories]].

#Applications#

## $\omega$-Nerve ##

The $\omega$-nerve $N(C)$ of an [[omega-category]] $C$ is a simplicial set which generalizes the [[nerve]] of an ordinary category: the collection of $k$-simplices in $N(C)$ is the collection of images of the $k$-th oriental $O_k$ in $C$, i.e.

$$
  (N(C))_k := Hom_{\omega Cat}(O([k]), C)
  \,.
$$

This naturally extends to a functor

$$
  N : \omega Cat \stackrel{Hom_{\omega Cat}(O([-_2]),-_1)}{\to}
  SimplicialSets
  \,.
$$

The nerve functor is faithful. This means that omega categories can be regarded as simplicial sets equipped with extra structure. The precise nature of this structure was identified by Dominic Verity in terms of [[complicial set]]s in his work on the [Doplicher-Roberts conjecture](http://golem.ph.utexas.edu/string/archives/000711.html). 

## Free $\omega$-Category on a simplicial set##

The $\omega$-nerve has a [[adjoint functor|left adjoint]], the free $\omega$category on a simplicial set

$$
  F : SimplicialSets \to \omega Cat
$$

given by the [[end|coend]]

$$
  F(S_\bullet) := \int^{[n] \in \Delta} S_n \cdot
   O([n])
  \,.
$$

(Here one uses that $\omega Cat$ is naturally tensored over $Sets$: the notation $S_n \cdot O([n])$ refers to a coproduct of an $S_n$-indexed collection of copies of $O([n])$. See also [[enriched category theory]].)

Because the nerve functor is faithful, the counit of the adjunction $F \dashv N$, 

$$\varepsilon_C: F N C \to C,$$ 

is an epimorphism for omega categories $C$. 

+-- {: .query}

Is $F$ faithful? It seems to be... If not, how does it fail to be faithful? 

=--

##Descent and codescent##

The orientals $O(\Delta^{(n)})$, as well as the $\Pi_\omega(\Delta^{(n)})$ play a central role in the description of [[descent|descent and codescent]] in [[omega-category|omega-categorical terms]].



#Relation to $\omega$-groupoids#

Regarding the standard $n$-simplex as a filtered space with the standard filtering, and denoting for $X$ a filtered space by $\Pi_\omega(X)$ the fundamental filter-respecting $\omega$-groupoid of $X$, we obtain a cosimplicial [[omega-groupoid|omega-groupoid]]

$$
  \Pi_\omega(\Delta^{-})
  :
  \Delta \to \omega Grpd
$$

+-- {: .query}

It should be true that $\Pi_\omega(\Delta^n)$ is the _free $\omega$-groupoid_ on $O(\Delta^n)$. Is that right?

=--



#Literature#

The orientals were introduced in

* Ross Street, _The algebra of oriented simplexes_, J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf)).

The $\omega$-groupoids $\Pi_\omega(\Delta^{n})$ are discussed in detail in

* Ronald Brown, Philip J. Higgins and Rafael Sivera, _Nonabelian algebraic topology_ ([pdf](http://www.bangor.ac.uk/~mas010/pdffiles/rbrsbookb-e040609.pdf))

#Further resources#

We had related blog discussion in the following $n$-Caf&#233;-entries:

* [Freely generated $\omega$-categories](http://golem.ph.utexas.edu/category/2008/10/freely_generated_categories.html)

* [Codescent and the van Kampen theorem](http://golem.ph.utexas.edu/category/2008/10/codescent_and_the_van_kempen_t.html)

[[!redirects orientals]]