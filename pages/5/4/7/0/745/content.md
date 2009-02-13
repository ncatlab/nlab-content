# Definition #

If $f:C\to E$ and $g:D\to E$ are [[functor]]s, their **comma category** is the category $(f/g)$ (also written $(f\downarrow g)$ or $(f,g)$) whose

* [[object]]s are triples $(c,d,\alpha)$ where $c\in C$, $d\in D$, and $\alpha:f(c)\to g(d)$ is a morphism in $E$, and whose
* [[morphism]]s from $(c_1,d_1,\alpha_1)$ to $(c_2,d_2,\alpha_2)$ are pairs $(\beta,\gamma)$, where $\beta:c_1\to c_2$ and $\gamma:d_1\to d_2$ are morphisms in $C$ and $D$, respectively, such that $\alpha_2 . f(\beta) = g(\gamma) . \alpha_1$.


# Examples #

* If $f$ and $g$ are both the identity functor of a category $C$, then $(f/g)$ is the category $C ^{\mathbf{2}} $ of arrows  in $C$.

* If $f$ is the identity functor of $C$ and $g$ is the inclusion $1\to C$ of an object $c\in C$, then $(f/g)$ is the [[slice category]] $C/c$.

* Likewise if $g$ is the identity and $f$ is the inclusion of $c$, then $(f/g)$ is the [[under category|coslice category]] $c/C$.


# 2-categorical properties #

The comma category $(f/g)$ comes with a canonical 2-cell in the square

+--{: style="text-align:center"}
<svg xmlns="http://www.w3.org/2000/svg" width="10em" height="10em" viewBox="-20 0 150 140">
 <desc>Comma Square</desc>
 <defs>
  <marker id="svg295arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
 </defs>
 <g font-size="16" markdown="1">
  <foreignObject x="-10"  y="0" width="45" height="25">$(f/g)$</foreignObject>
  <foreignObject x="100"  y="0" width="20" height="20">$C$</foreignObject>
  <foreignObject x="0"  y="100" width="20" height="20">$D$</foreignObject>
  <foreignObject x="100"  y="100" width="20" height="20">$E$</foreignObject>
  <foreignObject x="110"  y="50" width="20" height="20">$f$</foreignObject>
  <foreignObject x="50"  y="110" width="20" height="25">$g$</foreignObject>
  <foreignObject x="60"  y="60" width="20" height="25">$\alpha$</foreignObject>
 </g>
 <g fill="none" stroke="#000" stroke-width="1.5" marker-end="url(#svg295arrowhead)">
   <line x1="40" y1="10" x2="90" y2="10"/>
   <line x1="30" y1="110" x2="90" y2="110"/>
   <line y1="30" x1="10" y2="90" x2="10"/>
   <line y1="30" x1="110" y2="90" x2="110"/>
   <line x1="65" y1="55" x2="55" y2="65"/>
 </g>
</svg>
=--
which is universal in the [[2-category]] [[Cat]]; that is, it is an example of a [[2-limit]] (in fact, it is a [[strict 2-limit]]).  Squares with the same universal property in an arbitrary 2-category are called _comma squares_ and their top left vertex is called a [[comma object]].


# Remarks #

The terminology "comma category" is a holdover from the original notation $(f,g)$ for such a category, which generalises $(x,y)$ or $C(x,y)$ for a [[hom-set]].

+--{.query}
It\'s a very natural notation, as it generalises the notation $(x,y)$ (or $[x,y]$ as is now more common) for a [[hom-set]].  But personally, I like $(f \rightarrow g)$ (or $(f \searrow g)$ if you want to differentiate from a cocomma category, but that seems an unlikely confusion), as it is a category of arrows from $f$ to $g$.
&#8212;[[Toby Bartels]]

[[Mike Shulman|Mike]]:  Perhaps.  I never write $(x,y)$ for a hom-set, only $A(x,y)$ or $hom_A(x,y)$ where $A$ is the category involved, and this is also the common practice in nearly all mathematics I have read.  I have seen $[x,y]$ for an internal-hom object in a [[closed monoidal category]], and for a hom-set in a [[homotopy category]], but not for a hom-set in an arbitrary category.

I would be okay with calling the comma category (or more generally the [[comma object]]) $E(f,g)$ or $hom_E(f,g)$ _if_ you are considering it as a discrete fibration from $A$ to $B$.  But if you are considering it as a _category_ in its own right, I think that such notation is confusing.  I don't mind the arrow notations, but I prefer $(f/g)$ as less visually distracting, and evidently a generalization of the common notation $C/x$ for a [[slice category]].

_Toby_: Well, I never stick '$E$' in there unless necessary to avoid amibiguity. I agree that the slice-generalising notation is also good. I\'ll use it too, but I edited the text to not denigrate the hom-set generalising notation so much.
=--

# Further reading #

[a low-tech description with several special cases identified in somewhat archaic terminology](http://toby.bartels.name/notes/#comma)
