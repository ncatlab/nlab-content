#Idea#

Orientals are "oriented simplices": the $n$-th oriental is the simplicial $n$-simplex equipped with source and target relations, assigning to each $k$-face a set of $(k-1)$-faces called its source and a set of $(k-1)$-faces called its target, subject to some natural axioms. Each oriental freely generates (see below) a structure of a [[strict omega-category]] $O(\Delta^n)$, such that $k$-morphisms in $O(\Delta^n)$ are pasting diagrams of $k$-faces in $\Delta^n$.

One of the axioms is a [[globular set|globularity axiom]], which says that the source of a source (that is, the union of sources of all $(k-1)$-faces in the source of a $k$-face) equals the source of the target, and similarly that the target of a source equals the target of the target. Thus, orientals mediate between the [[simplicial set|simplicial]] and the [[globular set|globular]] world of [[higher category theory|infinity-categories]].

The first few orientals look as follows:

<img src="http://www.math.uni-hamburg.de/home/schreiber/pics/orientals.gif" alt=""/>

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


The first few orientals look as follows:

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
  <marker id="svg296arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="4" markerHeight="2.5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
 </defs>
 <g font-size="10">
  <foreignObject x="25" y="-2" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
  <foreignObject x="0" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
  <foreignObject x="50" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
 </g>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M10,30 23, 15"/>
   <path d="M35,12 48, 27"/>
   <path d="M15,37 45, 37"/>
  </g>
  <g>
   <path stroke-width="3" d="M30,15 30,27" marker-end="url(#svg296arrowhead)"/>
   <path stroke="#FFF" d="M30,15 30,27"/>
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
    <foreignObject x="0" y="-3" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
    <foreignObject x="0" y="37" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
    <foreignObject x="40" y="-3" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
    <foreignObject x="40" y="37" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>3</mi></math></foreignObject>
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
  <g stroke-width="3" marker-end="url(#svg296arrowhead)">
   <path d="M12,12 20,20"/>
   <path d="M40,18 27,40"/>
  </g>
  <g stroke="#FFF">
   <path d="M12,12 20,20"/>
   <path d="M40,18 27,40"/>
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
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M92,20 100,38"/>
    <path d="M120,12 113,19"/>
   </g>
   <g stroke="#FFF">
    <path d="M92,20 100,38"/>
    <path d="M120,12 113,19"/>
   </g>
  </g>
 </g>
</svg>
\end{svg}}\right\}\\
O(\Delta^4) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="28em" height="23em" viewBox="-35 0 245 230">
 <defs>
  <g id="myPent256">
   <g font-size="10">
    <foreignObject x="25" y="-2" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
    <foreignObject x="0" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
    <foreignObject x="50" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>3</mi></math></foreignObject>
    <foreignObject x="13" y="57" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
    <foreignObject x="38" y="57" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>4</mi></math></foreignObject>
   </g>
   <g fill="none" stroke="#000" marker-end="url(#svg295arrowhead)">
    <path d="M8,32 25,13"/>
    <path d="M35,10 52,28"/>
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
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M31,12 31,26"/>
    <path d="M12,38 25,48"/>
    <path d="M45,48 35,60"/>
   </g>
   <g stroke="#FFF">
    <path d="M31,12 31,26"/>
    <path d="M12,38 25,48"/>
    <path d="M45,48 35,60"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="110" y="0"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M120,36 155,36"/>
   <path d="M122,41 147,60"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M141,12 141,26"/>
    <path d="M125,47 135,58"/>
    <path d="M162,38 145,48"/>
   </g>
   <g stroke="#FFF">
    <path d="M141,12 141,26"/>
    <path d="M125,47 135,58"/>
    <path d="M162,38 145,48"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="160" y="80"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M172,119 195,140"/>
   <path d="M194,98 201,138"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M175,127 185,138"/>
    <path d="M212,116 206,116"/>
    <path d="M189,98 184,121"/>
   </g>
   <g stroke="#FFF">
    <path d="M175,127 185,138"/>
    <path d="M212,116 206,116"/>
    <path d="M189,98 184,121"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="55" y="160"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M74,220 83,180"/>
   <path d="M87,178 96,218"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M86,187 86,216"/>
    <path d="M63,196 71,196"/>
    <path d="M107,196 99,196"/>
   </g>
   <g stroke="#FFF">
    <path d="M86,187 86,216"/>
    <path d="M63,196 71,196"/>
    <path d="M107,196 99,196"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="-50" y="80"/>
 <g fill="none" stroke="#000">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M-31,140 -22,100"/>
   <path d="M-29,143 -3,120"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M-40,116 -35,116"/>
    <path d="M-17,97 -17,123"/>
    <path d="M-5,128 -15,140"/>
   </g>
   <g stroke="#FFF">
    <path d="M-40,116 -35,116"/>
    <path d="M-17,97 -17,123"/>
    <path d="M-5,128 -15,140"/>
   </g>
  </g>
 </g>
 <g fill="none" stroke="#000">
  <g stroke-width="5">
   <path d="M60,35 100,35"/>
   <path d="M158,75 168,90"/>
   <path d="M118,190 168,155"/>
   <path d="M3,150 43,185"/>
   <path d="M-3,95 11,79"/>
  </g>
  <g stroke-width="3" stroke="#FFF" marker-end="url(#svg296arrowhead)">
    <path d="M158,75 168,90"/>
    <path d="M60,35 100,35"/>
    <path d="M118,190 168,155"/>
    <path d="M3,150 43,185"/>
    <path d="M-3,95 11,79"/>
  </g>
  <g stroke-width="1">
   <path d="M60,35 100,35"/>
   <path d="M158,75 168,90"/>
   <path d="M118,190 168,155"/>
   <path d="M3,150 43,185"/>
   <path d="M-3,95 11,79"/>
  </g>
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

The nerve functor is faithful. This means that omega categories can be regarded as simplicial sets equipped with extra structure. The precise nature of this structure was identified by Dominic Verity ("complicial sets") in his work on the D&ouml;plicher-Roberts conjecture (citation needed). 

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

The orientals $O(\Delta^{(n)})$, as well as the $\Pi_\omega(\Delta^{(n)})$ play a central role in the description of [[descent and codescent]] in [[omega-category|omega-categorical terms]].



#Relation to $\omega$-groupoids#

Regarding the standard $n$-simplex as a filtered space with the standard filtering, and denoting for $X$ a filtered space by $\Pi_\omega(X)$ the fundamental filter-respecting $\omega$-groupoid of $X$, we obtain a cosimplicial [[omega-groupoid|omega-groupoid]]

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