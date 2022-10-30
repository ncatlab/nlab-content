##The Idea##

A 'monoidal category' is a [[category]] equipped with some notion of 'tensor product'.  A good example is the category [[Vect]], where we can take the tensor product, not only of vector spaces, but also of linear maps: given linear maps $f : V \to W$ and $f' : V' \to W'$, we get a linear map

$$ f \otimes f': V \otimes V' \to W \otimes W' $$

The same category can often be made into a monoidal category in more than one way.  For example the category [[Set]] can be made into a monoidal category with cartesian [[product]] or disjoint union (i.e. [[coproduct]]) as the 'tensor product'.   We can also make [[Vect]] into a monoidal category with direct sum is the 'tensor product' --- this may seem perverse, but it's actually very useful.

For any monoidal category $M$, the operation of tensor product is actually a [[functor]]

$$\otimes : M \times M \to M$$

This functor, which we can think of as a kind of 'multiplication', makes $M$ into a [[vertical categorification|vertically categorified]] version of a [[monoid]].  This explains the term 'monoidal category'.

##Definition##  

A **monoidal category** is a [[category]] $M$ equipped with a [[functor]]
$$ \otimes : M \times M \to M $$
called the **tensor product**, an object
$$ 1 \in M $$
called the **unit object**, a natural isomorphism
$$ a_{x,y,z} : (x \otimes y) \otimes z \to x \otimes (y \otimes z) $$
called the **associator**, a natural isomorphism
$$ \lambda_x : 1 \otimes x \to x $$
called the **left unitor**, and a natural isomorphism 
$$  \rho_x : x \otimes 1 \to x $$
called the **right unitor**, which must satisfy a couple of equations, most notably the **pentagon identity**:

+--{: style="text-align:center"}
<svg xmlns="http://www.w3.org/2000/svg" width="30em" height="20em" viewBox="0 0 480 320">
 <desc>Pentagon Identity</desc>
 <defs>
  <marker id="svg295arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="5" orient="auto">
   <path d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
 </defs>
 <g font-size="16" markdown="1">
  <foreignObject x="180"  y="0" width="120" height="20">$(w\otimes x)\otimes(y\otimes z)$</foreignObject>
  <foreignObject x="0"  y="120" width="120" height="20">$((w\otimes x)\otimes y)\otimes z$</foreignObject>
  <foreignObject x="360"  y="120" width="120" height="20">$w\otimes (x\otimes(y\otimes z))$</foreignObject>
  <foreignObject x="60"  y="300" width="120" height="20">$(w\otimes (x\otimes y))\otimes z$</foreignObject>
  <foreignObject x="320"  y="300" width="120" height="20">$w\otimes ((x\otimes y)\otimes z)$</foreignObject>
  <foreignObject x="80"  y="50" width="60" height="24">$a_{w\otimes x,y,z}$</foreignObject>
  <foreignObject x="350"  y="50" width="60" height="24">$a_{w,x,y\otimes z}$</foreignObject>
  <foreignObject x="10"  y="210" width="70" height="24">$a_{w,x,y}\otimes 1_{z}$</foreignObject>
  <foreignObject x="410"  y="210" width="70" height="24">$1_w\otimes a_{x,y,z}$</foreignObject>
  <foreignObject x="215"  y="290" width="60" height="24">$ a_{w,x\otimes y,z}$</foreignObject>
 </g>
 <g fill="none" stroke="#000" stroke-width="1.5" marker-end="url(#svg295arrowhead)">
   <line x1="70" y1="120" x2="230" y2="25"/>
   <line x1="250" y1="25" x2="410" y2="120"/>
   <line x1="60" y1="140" x2="110" y2="300"/>
   <line x1="370" y1="300" x2="420" y2="150"/>
   <line x1="180" y1="315" x2="310" y2="315"/>
 </g>
</svg>
=--  

(Hey!  Where did the pentagon identity go???)

A monoidal category is said to be **strict** if the associator, left unitor and right unitors are all identity morphisms.  

There is a [[strict 2-category]] MonCat with:

* monoidal categories as objects,
* [[monoidal functor]]s as morphisms, 
* [[monoidal natural transformation]]s as 2-morphisms.

One version of Mac Lane's Coherence Theorem states that in MonCat, every monoidal category is [[equivalence|equivalent]] to a strict one.

##References##

The definition of monoidal category can be found on [John Armstrong's blog](http://unapologetic.wordpress.com/2007/06/28/monoidal-categories/) and [Wikipedia](http://en.wikipedia.org/wiki/Monoidal_category).

For definitions of all the concepts mentioned above, including a precise description of the 'couple of equations' alluded to above, see:

* John Baez, [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

It would be nice if you, dear reader, would add all these definitions to the $n$Lab!   The [LaTeX code](http://math.ucr.edu/home/baez/qg-fall2004/texfiles/definitions.tex) is available if you want.

For an elementary introduction to monoidal categories using string diagrams, see:

* John Baez and Mike Stay, [Physics, topology, logic and computation: a Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf).

##Where the Definition Comes From##

The definition of monoidal category looks rather complicated at first sight, so it is natural to wonder if there is some magic wand we can wave that makes it appear automatically.  For example, one might wonder if we can define monoidal categories using [[internalization]].  

In fact a *strict* monoidal category is just a [[monoid]] internal to the category [[Cat]].  Unfortunately this definition is circular, since to define a monoid internal to [[Cat]], we need to use the fact that [[Cat]] is a monoidal category!  Furthermore, hardly any of the monoidal categories in nature are strict. So, we need to weaken the definition of monoidal category, and this is where the subtleties come in: we need the associator, left unitor, and right unitor to satisfy some 'coherence laws' --- e.g. the pentagon identity.  

But _where do the coherence laws come from?_  

In fact, these are precisely what we need to make any diagram built solely by tensoring, associators, and unitors commute.  This fact is another version of Mac Lane's Coherence Theorem.  Mac Lane proved it in the same paper where he originally defined the concept of monoidal category.

There are indeed 'magic wands' that automatically produce the definition of monoidal category, but most of these magic wands  are so heavy that only more advanced wizards can lift them.  

For example, you can define a monoidal category to be a [[pseudomonoid]] internal to the 2-category [[Cat]] --- but nobody knew how to define these concepts until they knew what a monoidal category is!

Two other closely related approaches involve [[2-monad|2-monad theory]] and [[homotopy theory]].  

To make the first one work, the magic words to say are "there is a 2-monad whose algebras are strict monoidal categories, and a (non-strict) monoidal category is a pseudo-algebra for that 2-monad."  This doesn't give you the definition of monoidal categories that we're used to, though; it gives you the [[bias|unbiased]] version.

To make the second magic wand work, the magic words to say are "there is a monad/operad/etc. in [[Cat]] whose algebras are strict monoidal categories, and the monad/operad/etc. whose algebras are (non-strict) monoidal categories is a cofibrant replacement for that one."  Since cofibrant replacements are usually defined only up to equivalence, this one also doesn't determine the usual definition uniquely.  There is a "canonical" choice, but again it gives you the unbiased version.  The equation "cofibrant = [[flexibility|flexible]]" says that these two magic wands are doing essentially the same thing.

Of course, both are also sort of a cheat, since in order to prove that the biased and unbiased definitions are equivalent, you need to have the [[coherence theorem]] for the biased definition.  However, it's only because of the coherence theorem that we can say definitely that the usual set of complicated-looking diagrams is "correct."  The approach using lax $\infty$-functors really only postpones this question, since you also need a coherence theorem to show that the definition of lax $\infty$-functor is "correct."  So perhaps there is no magic wand after all, at least not one that produces the _specific_ diagrams in the usual biased definition of monoidal category.

However, if we temporarily ignore the unitors and focus on the associator, we may ask _where does the pentagon identity come from?_  And one answer to this is provided by the Stasheff polytopes, which can be nicely obtained using Ross Street's theory of orientals.   For instance the pentagon diagram above is nothing but the [[oriental|4th oriental]]! The tensor product itself is the second oriental, and the associator the third.  The following section explains this in a bit more detail.

##Relation to lax functors, orientals and descent##

One can understand the structure of a monoidal category as a special simple case of the general notion of "lax $\infty$-functor", also known -- up to the issue of invertible versus non-invertible structure morphisms -- as the notion of $\infty$-categorical [[descent and codescent|descent]] and as the notion of [[anafunctor|infinity-anafunctor]].

This may be familiar from the special simple case of a _monoid_ in any bicategory $C$, which can be identified with a lax functor 

$$
  A : pt \to C
$$

from the point to $C$. This lax functor sends the point to some object of $C$, sends the [[identity]] morphism on the point to some [[endomorphism]] of that object. The unitor of the lax functor gives the product on that endomorphism and the coherence of the unitor is the associativity condition on this product.

This is part of a more general principle. A lax[[monoid]] in any tricategory would again be a lax functor from the point to that tricategory. 

And a monoidal category can be regarded as a pseudomonoid in the tricategory $\mathbf{B}Cat$, which has a single object, categories as 1-morphisms with the composition of 1-morphisms being the standard cartesian [[tensor product]] on categories.

Evidently, in the fully general context of weak $\infty$-categories it becomes increasingly hard to state what a lax functor into a given $\infty$-category should be: it will involve a plethora of structure morphisms and their coherences. One task of [[higher category theory]] is to organize this mess into something pretty and then to deal with this problem.

But before being intimidated by the problem in its most general form, it may pay to understand it in slightly simplified situations. One such slightly simplified setup is that of _strict_ $\infty$-categories, usually known as $\omega$-categories or [[strict omega-category|strict omega-categories]].

For that case, Ross Street has given a general combinatorial formula for the $\infty$-coherence law of the general monoidal structure: this is encoded in the [[oriental|orientals]], which are nothing but the standard simplicial simplices, but equipped with extra information about source and targets of all faces.

See the picture of the [[oriental|first five orientals]]. We can read off the above definition of a monoidal category from them as follows:

* identify the monoidal category $M$ itself with the first oriental, just an arrow;

* identify the ambient product $M \times M$ with the juxtaposition of two such arrows;

* identify the tensor product $M \otimes M \to M$ with the second oriental: a triangular cell going from the concatenation of two arrows to a single arrow;

* identify the _associator_ with the third oriental, the tetrahedron: a map from one way to compose three arrows (=copies of $M$) to the other way of doing this;

* identify the pentagon identity with the fourth oriental. In general, the fourth oriental is itself a nontrivial 4-cell, but assume now that the big arrow in the middle of that is the identity. This makes what in general would be the _pentagonator_ the _pentagon identity_ in this case.

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


This shows that it is a bit of an illusion to think of a _pentagon_ identity: the full geometric shape is really a 4-dimensional tetrahedron (the 4-simplex) whose five tetrahedral faces are the five vertices of the pentagon identity.


We can formulate this identification of structure morphisms and coherence laws with orientals more formally using the general notion of [[descent and codescent|descent]], which was indeed the original motivation for conceiving the orientals. The descent $\infty$-category $Desc(Y,A)$ (constructed in terms of orientals) can be regarded as a way to formalize "lax $\infty$-functor from $Y$ to $A$".

Indeed, using observations pretty much as just sketched, one finds that for $C$ a 2-category that

$$
  Desc(pt, C) \simeq WeakMonoids(C)
$$

and for $C$ the 3-category $\mathbf{B}Cat$ we have

$$
  Desc(pt, \mathbf{B}Cat) \simeq LaxMonCat
  \,,
$$

where the 2-category on the right is defined as $MonCat$ above, but with the associator not required to be an isomorphism.

##Remark: pseudo versus lax, orientals versus unorientals##

In closing, it should be remarked that the fact that everything here is _lax_ instead of _pseudo_ is related to a curious property of the orientals: the $n$th oriental for $n \ge 1$ _fails_ to be weakly equivalent to the point. As a result, the objects of $Desc(pt, C)$ are not quite $\omega$-[[anafunctor]]s from the point to $C$, since they do not map out of a proper hypercover of $C$. In the strict notion of descent as used in most of the literature, the orientals would hence provide something _more general_ than ordinary descent, which in its generality is lacking some properties usually required of descent.

We can remedy this by replacing in the definition of the descent $\infty$-category $Desc(Y,C)$ the orientals by another cosimplicial $\infty$-category, one which _is_ equivalent to the point in each degree. Doing so and then going through the above discussion will make _all_ the structure maps appeaing have inverses. But this will also apply to the monoidal product itself, then, which is usually not desired.  

##Discussion##

_[[John Baez|John]] says:_ I have attempted to work all the above discussion into the main article.  If we are reasonably happy with my attempt, we can perhaps delete the discussion above.

_Toby_: For the record, I\'m happy with that.

_Mike_: Me too.

_John_: Since Urs and Eric expressed no opinion, I'm deleting the 'above discussion'.  We can always go back in time if we want to revive it.