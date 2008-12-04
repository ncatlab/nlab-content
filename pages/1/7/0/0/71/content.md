#Idea#

Orientals are "oriented simplices": the $n$-th oriental is the simplicial $n$-simplex equipped with source and target relations, assigning to each $k$-face a set of $(k-1)$-faces called its source and a set of $(k-1)$-faces called its target, subject to some natural axioms. Each oriental freely generates (see below) a structure of a [[omega-category]] $O(\Delta^n)$, such that $k$-morphisms in $O(\Delta^n)$ are pasting diagrams of $k$-faces in $\Delta^n$.

One of the axioms is a [[globular set|globularity axiom]], which says that the source of a source (that is, the union of sources of all $(k-1)$-faces in the source of a $k$-face) equals the source of the target, and similarly that the target of a source equals the target of the target. Thus, orientals mediate between the [[simplicial set|simplicial]] and the [[globular set|globular]] world of [[higher category theory|infinity-categories]].

The first few orientals look as follows:

<img src="http://www.math.uni-hamburg.de/home/schreiber/pics/orientals.gif" alt=""/>

{:response: style="color:#930; font-size:0.9em;margin-left:2em;"}

{: response}Here's the same figure, in SVG. I think it looks better. Opinions may vary, however. -- Jacques

$$
\array{\arrayopts{\rowalign{center}}
O(\Delta^0) = & \{ 0\} \\
O(\Delta^1) = & \left\{ 0 \to 1\right\} \\
O(\Delta^2) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="6em" height="4em" viewBox="0 0 60 40">
 <defs>
  <marker id="svg295arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
  <marker id="svg296arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="6" markerHeight="3.5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
 </defs>
 <g font-size="10">
  <foreignObject x="25" y="0" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
  <foreignObject x="0" y="30" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
  <foreignObject x="50" y="30" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
 </g>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M10,30 23, 15"/>
   <path d="M35,12 48, 27"/>
   <path d="M15,37 45, 37"/>
  </g>
  <g stroke-width="2">
   <path stroke-width="4" d="M30,15 30,27"/>
   <path stroke="#FFF" d="M30,15 30,27" marker-end="url(#svg296arrowhead)"/>
  </g>
 </g>
</svg>
\end{svg}}
\right\}\\
O(\Delta^3) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="13em" height="5em" viewBox="0 0 130 50">
 <defs>
  <g id="myRect256">
   <g font-size="10">
    <foreignObject x="0" y="0" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
    <foreignObject x="0" y="40" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
    <foreignObject x="40" y="0" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
    <foreignObject x="40" y="40" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>3</mi></math></foreignObject>
   </g>
   <g fill="none" stroke="#000">
    <g marker-end="url(#svg295arrowhead)">
     <path d="M10,7 37, 7"/>
     <path d="M6,42 6, 17"/>
     <path d="M10,47 37, 47"/>
     <path d="M46,12 46, 37"/>
    </g>
   </g>
  </g>
 </defs>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myRect256" x="0" y="0"/>
 <g fill="none" stroke="#000">
  <path d="M11,43 38, 15" marker-end="url(#svg295arrowhead)"/>
  <g stroke-width="2">
   <path stroke-width="4" d="M12,12 20,20"/>
   <path stroke="#FFF" d="M12,12 20,20" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M40,18 27,40"/>
   <path stroke="#FFF" d="M40,18 27,40" marker-end="url(#svg296arrowhead)"/>
  </g>
 </g>
 <g fill="none" stroke="#000">
   <path stroke-width="5" d="M55,25 72,25"/>
   <path stroke-width="3" stroke="#FFF" d="M55,25 72,25" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="1" d="M55,25 72,25"/>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myRect256" x="80" y="0"/>
 <g fill="none" stroke="#000">
  <path d="M92,12 118, 39" marker-end="url(#svg295arrowhead)"/>
  <g stroke-width="2">
   <path stroke-width="4" d="M92,22 100,40"/>
   <path stroke="#FFF" d="M92,22 100,40" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M120,12 113,19"/>
   <path stroke="#FFF" d="M120,12 113,19" marker-end="url(#svg296arrowhead)"/>
  </g>
 </g>
</svg>
\end{svg}}\right\}\\
O(\Delta^4) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="28em" height="24em" viewBox="-35 0 245 240">
 <defs>
  <g id="myPent256">
   <g font-size="10">
    <foreignObject x="25" y="0" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
    <foreignObject x="0" y="30" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
    <foreignObject x="50" y="30" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>3</mi></math></foreignObject>
    <foreignObject x="13" y="60" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
    <foreignObject x="38" y="60" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>4</mi></math></foreignObject>
   </g>
   <g fill="none" stroke="#000" marker-end="url(#svg295arrowhead)">
    <path d="M8,32 25,13"/>
    <path d="M35,10 50,30"/>
    <path d="M54,41 48,57"/>
    <path d="M24,67 36,67"/>
    <path d="M16,62 8,45"/>
   </g>
  </g>
 </defs>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="0" y="0"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M10,36 45,36"/>
   <path d="M22,60 47,41"/>
  </g>
  <g stroke-width="2">
   <path stroke-width="4" d="M31,12 31,26"/>
   <path stroke="#FFF" d="M31,12 31,26" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M12,38 25,48"/>
   <path stroke="#FFF" d="M12,38 25,48" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M45,48 35,60"/>
   <path stroke="#FFF" d="M45,48 35,60" marker-end="url(#svg296arrowhead)"/>
  </g>
 </g>
 <g fill="none" stroke="#000">
   <path stroke-width="5" d="M60,35 100,35"/>
   <path stroke-width="3" stroke="#FFF" d="M60,35 100,35" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="1" d="M60,35 100,35"/>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="110" y="0"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M120,36 155,36"/>
   <path d="M122,41 147,60"/>
  </g>
  <g stroke-width="2">
   <path stroke-width="4" d="M141,12 141,26"/>
   <path stroke="#FFF" d="M141,12 141,26" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M125,47 135,58"/>
   <path stroke="#FFF" d="M125,47 135,58" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M160,38 143,48"/>
   <path stroke="#FFF" d="M160,38 143,48" marker-end="url(#svg296arrowhead)"/>
  </g>
 </g>
 <g fill="none" stroke="#000">
   <path stroke-width="5" d="M158,75 168,95"/>
   <path stroke-width="3" stroke="#FFF" d="M158,75 168,95" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="1" d="M158,75 168,95"/>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="160" y="80"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M172,119 195,140"/>
   <path d="M192,98 201,138"/>
  </g>
  <g stroke-width="2">
   <path stroke-width="4" d="M175,127 185,138"/>
   <path stroke="#FFF" d="M175,127 185,138" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M212,116 204,116"/>
   <path stroke="#FFF" d="M212,116 204,116" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M187,98 184,121"/>
   <path stroke="#FFF" d="M187,98 184,121" marker-end="url(#svg296arrowhead)"/>
  </g>
 </g>
 <g fill="none" stroke="#000">
   <path stroke-width="5" d="M168,140 118,175"/>
   <path stroke-width="3" stroke="#FFF" d="M168,140 118,175" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="1" d="M168,140 118,175"/>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="55" y="160"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M74,220 83,180"/>
   <path d="M87,178 96,218"/>
  </g>
  <g stroke-width="2">
   <path stroke-width="4" d="M86,187 86,216"/>
   <path stroke="#FFF" d="M86,187 86,216" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M63,196 71,196"/>
   <path stroke="#FFF" d="M63,196 71,196" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M107,196 99,196"/>
   <path stroke="#FFF" d="M107,196 99,196" marker-end="url(#svg296arrowhead)"/>
  </g>
 </g>
 <g fill="none" stroke="#000">
   <path stroke-width="5" d="M63,180 13,145"/>
   <path stroke-width="3" stroke="#FFF" d="M63,180 13,145" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="1" d="M63,180 13,145"/>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="-50" y="80"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M-31,140 -20,100"/>
   <path d="M-29,143 0,120"/>
  </g>
  <g stroke-width="2">
   <path stroke-width="4" d="M-40,116 -30,116"/>
   <path stroke="#FFF" d="M-40,116 -30,116" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M-15,97 -15,123"/>
   <path stroke="#FFF" d="M-15,97 -15,123" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="4" d="M-5,128 -15,140"/>
   <path stroke="#FFF" d="M-5,128 -15,140" marker-end="url(#svg296arrowhead)"/>
  </g>
 </g>
 <g fill="none" stroke="#000">
   <path stroke-width="5" d="M-3,99 11,79"/>
   <path stroke-width="3" stroke="#FFF" d="M-3,99 11,79" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="1" d="M-3,99 11,79"/>
 </g>
 <g fill="none" stroke="#000">
   <path stroke-width="7" d="M85,43 85,140"/>
   <path stroke-width="5" stroke="#FFF" d="M85,43 85,140" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="3" d="M85,43 85,140"/>
   <path stroke-width="1" stroke="#FFF" d="M85,43 85,140"/>
 </g>
</svg>
\end{svg}}
\right\}
}
$$

#Structures#

##As cosimplicial $\omega$-category##

The construction of orientals is designed to be compatible with face and degeneracy maps. Therefore the orientals arrange themselves into a cosimplicial [[omega-category]], i.e. a functor

$$
  O : \Delta \to \omega Cat
$$

from the [[simplicial category]] $\Delta$ to the category of [[omega-category|omega-categories]].

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

The nerve functor is faithful. This means that omega categories can be regarded as simplicial sets equipped with extra structure. The precise nature of this structure was identified by Dominic Verity ("complicial sets") in his work on the D&ouml;plicher-Roberts conjecture (citation needed). 

## Free $\omega$-Category on a simplicial set##

The $\omega$-nerve has a left [[adjoint]], the free $\omega$category on a simplicial set

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

#Relation to $\omega$-groupoids#

Regarding the standard $n$-simplex as a filtered space with the standard filtering, and denoting for $X$ a filtered space by $\Pi_\omega(X)$ the fundamental filter-respecting $\omega$-groupoid of $X$, we obtain a cosimplicial [[omega-category|omega-groupoid]]

$$
  \Pi_\omega(\Delta^{-})
  :
  \Delta \to \omega Groupoids
$$

+-- {: .query}

It should be true that $\Pi_\omega(\Delta^n)$ is the _free $\omega$-groupoid_ on $O(\Delta^n)$. Is that right?

=--



#Literature#

The orientals were introduced in

* Ross Street, _The algebra of oriented simplexes_, J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf)).

The $\omega$-groupoids $\Pi_\omega(\Delta^{n})$ are discussed in detail in

* Ronald Brown, Philip J. Higgins and Rafael Sivera, _Nonabelian algebraic topology_ ([pdf](http://www.bangor.ac.uk/~mas010/rbrsbookb-e-131008.pdf))

#Further resources#

We had related blog discussion in the following $n$-Caf&eacute;-entries:

* [Freely generated $\omega$-categories](http://golem.ph.utexas.edu/category/2008/10/freely_generated_categories.html)

* [Codescent and the van Kampen theorem](http://golem.ph.utexas.edu/category/2008/10/codescent_and_the_van_kempen_t.html)