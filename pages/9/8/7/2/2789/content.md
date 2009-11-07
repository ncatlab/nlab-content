##Discussion##

[[Eric]]: For some reason, I always thought a natural transformation was a more general map between functors $\alpha:F\Rightarrow G$, where
$$F:A\to B\quad\text{and}\quad G:C\to D.$$

Then $\alpha(F):C\to D$ is a functor and we'd probably also want **2-component** functors $\alpha_C:A\to C$ and $\alpha_D:B\to D$ such that the following diagram commutes
$$ 
  \array{ 
    A 
    & 
    \stackrel{F}{\to} 
    & 
    B 
    \\ 
    \mathllap{\scriptsize{\alpha_C}}\downarrow 
    &\mathllap{\scriptsize{\alpha}}\Downarrow & 
    \downarrow\mathrlap{\scriptsize{\alpha_D}}
    \\ C 
    & 
    \stackrel{G}{\to} & D 
  }
$$
If this is not a natural transformation, is there another name for it?

When $A = C$ and $B = D$, this should coincide with the usual definition. If so, why don't we define natural transformation in this more general way? It seems more "natural" to me.

[[Urs Schreiber]]: I suppose your 2-arrow in the middle labeled $\alpha$ is supposed to be a natural transformation (in the standard sense)? 

Then this is a square in the 2-category of categories. Such squares appear in turn as the _components_ of [[lax natural transformation]]s of 2-functors into [[Cat]].

[[Eric]]: Thanks. I was hesitant to put that 2-arrow in there. I'm still learning this stuff and am on shaky ground. But no. That 2-arrow is not supposed to be a natural transformation in the traditional sense because it is not a map between functors with the same domain and codomain. It is tempting to say we might want $\alpha_D\circ F\Rightarrow\alpha_C\circ G$ to be a natural transformation in the traditional sense though.

_Toby_:  That arrow certainly *looks* to me like a $2$-arrow from $\alpha_D\circ F$ to $\alpha_C\circ G$.  Unless it has no particular meaning and is just labelling the entire square as $\alpha\colon F \Rightarrow G$.  In any case, there is the question of what, if anything, goes between $\alpha_D\circ F$ and $\alpha_C\circ G$.  If nothing, then I would call such a thing a __square__ of functors.  If something more interesting, see my answer at [[ericforgy:Natural Transformation]] (which I saw first).

_Todd_: Here's one way of considering how the standard notion of natural transformation is the "right" one. Just as in topology we would like to consider the "space of all continuous maps $X \to Y$" from one space to another as a topological space, and the right notion of topology so we get an appropriate universal property, we want the same thing here. So the term analogous to "space" is "category", the term analogous to "continuous map" is "functor", and the term analogous to "space of all continuous maps from one space to another" or "function space" is "category of all functors from one category to another" or "functor category". And there should be a universal property which gives the right such category. 

In the end, if $D^C$ denotes the functor category, the universal property provides an equivalence between functors $X \to D^C$ and functors $X \times C \to D$. Pursuing this, let's figure out what morphisms in $D^C$ should look like. In an ordinary category $Y$, a morphism in $Y$ corresponds to a functor $\mathbf{2} \to Y$, where $\mathbf{2}$ is a category with two objects $0, 1$ and exactly one nonidentity arrow $0 \to 1$. So morphisms in $D^C$ should correspond to functors $\mathbf{2} \to D^C$. And the universal property says these are equivalent to functors $\mathbf{2} \times C \to D$. Now: if you carefully work through what functors of that form give you, you get precisely the notion of natural transformation. This is an exercise well worth working out. 

This is how you know the notion of natural transformation is morally the "right" one. 

[[Urs Schreiber]]: I added above a subsection on this characterization in terms of the cartesian closed monoidal structure on $Cat$.

[[Eric]]: I think I got it. 

Given two functors $F:A\to B$ and $G:C\to D$, let $\alpha:F\Rightarrow G$ together with component functors $\alpha_C:A\to C$ and $\alpha_D:B\to D$ be a map such that 
$$\alpha_D\circ F\Rightarrow G\circ\alpha_C$$
is a natural transformation (in the standard sense). Does this guy have a name?

The reason why I bring this up is that I do not like bigons. Bigons are not a good shape for doing computational geometry, geometric realization, etc. So before I could finally grok what a [[cone]] was, I had to draw a bunch of diagrams. These diagrams were bigons. Yucky!

Thanks Todd. That was a valiant effort, but didn't manage to convince me (I have a thick skull!). I still like this more general definition. Given topological spaces $W,X,Y,Z$, we could also be interested in studying spaces $(W\to X)\Rightarrow (Y\to Z)$. What you described would then be a special case where $W=Y$ and $X=Z$.

Here is my attempt to formalize an alternative definition:

***

>##Definition##

>Given categories $A$,$B$,$C$,$D$ and functors $F:A\to B$,$G:C\to D$ a __natural transformation__ $\alpha:F \Rightarrow G$ 
$$ 
  \array{ 
    A 
    & 
    \stackrel{F}{\to} 
    & 
    B 
    \\ 
    \mathllap{\scriptsize{\alpha_C}}\downarrow 
    &\mathllap{\scriptsize{\alpha}}\Downarrow & 
    \downarrow\mathrlap{\scriptsize{\alpha_D}}
    \\ C 
    & 
    \stackrel{G}{\to} & D 
  }
$$
>assigns functors $\alpha_C:A\to C$ and $\alpha_D:B\to D$ called **component functors** and for any morphism $f:x\to y$ in $A$ assigns morphisms $\alpha_x:\alpha_D\circ F(x)\to G\circ\alpha_C(x)$ and $\alpha_y:\alpha_D\circ F(y)\to G\circ\alpha_C(y)$ in $D$ called **component morphisms** such that the following diagram commutes in $D$:
$$ 
  \array{ 
    \alpha_D\circ F(x) 
    & 
    \stackrel{\alpha_D\circ F(f)}{\to} 
    & 
    \alpha_D\circ F(y) 
    \\ 
    \mathllap{\scriptsize{\alpha_x}}\downarrow 
    && 
    \downarrow\mathrlap{\scriptsize{\alpha_y}} 
    \\ G\circ\alpha_C(x) 
    & 
    \stackrel{G\circ\alpha_C(f)}{\to} & G\circ\alpha_C(y) 
  }
$$

***

Again, this reduces to the traditional definition when $\alpha_C$ and $\alpha_D$ are identity functors. What do you think? If this doesn't already have a name (it probably does), what would be a good name for it?

_Toby_:  This is exactly what I was talking about at [[ericforgy:Natural Transformation]].  I would call it a __lax commutative square of functors__.

[[Eric]]: Ok, but this seems to be "rotated $45^\circ$" relative to what you said there. Here $\alpha:F\Rightarrow G$ is a map between functors (not composites functors) with distinct domains and codomains having component functors $\alpha_C$, $\alpha_D$ and component morphisms $\alpha_x$, $\alpha_y$. I'm trying to emphasize the map $\alpha:F\Rightarrow G$. Now, I'm trying to think about how I might reinterpret functors in this way so that we can iterate the process to higher degrees.

_Urs_: no, the $\alpha$ the way you defined it _is_ a transformation between the composite functors: it is precisely a natural transformation from $\alpha_D \circ F$ to $G \circ \alpha_C$

_Toby_:  You are right that it is rotated *conceptually*, but what I wrote there was also supposed to be rotated conceptually.  The thing itself is indifferent to being from $F$ to $G$, but once you declare (conceptually) that it is to be something from $F$ to $G$, then what you have is a morphism in an arrow $2$-category, as I wrote there.

[[Eric]]: Thanks Toby. Here is a prepared remark with a comment below:

***

I wrote the definition down intentionally so that the composite _is_ a natural transformation, but I hope I can convince you that $\alpha:F\Rightarrow G$ is _not_ a natural transformation because the domains and codomains of $F$ and $G$ do not coincide (which they must to be a standard natural transformation). I'll call it something else then. How about "sheet transformations"?

>##Definition##

>Given categories $A$,$B$,$C$,$D$ and functors $F:A\to B$,$G:C\to D$ a __sheet transformation__ $\alpha:F \Rightarrow G$ 
$$ 
  \array{ 
    A 
    & 
    \stackrel{F}{\to} 
    & 
    B 
    \\ 
    \mathllap{\scriptsize{\alpha_C}}\downarrow 
    &\mathllap{\scriptsize{\alpha}}\Downarrow & 
    \downarrow\mathrlap{\scriptsize{\alpha_D}}
    \\ C 
    & 
    \stackrel{G}{\to} & D 
  }
$$
>assigns functors $\alpha_C:A\to C$ and $\alpha_D:B\to D$ called **component functors** such that
$$\alpha_D\circ F\Rightarrow G\circ\alpha_C$$
>is a **natural transformation**.

***

>The thing itself is indifferent to being from $F$ to $G$, but once you declare (conceptually) that it is to be something from $F$ to $G$, then what you have is a morphism in an arrow $2$-category, as I wrote there.

Interesting! That means a morphism in a arrow 2-category is the same thing as a "sheet transformation" (or vice versa :))

Urs: it seems to me what you are getting is is the relation between 2-categories and [[double category|double categories]]: a double category is a gadget whose 2-cells are squares not bigons. Every 2-category yields a double category by precisely the kind of operation that you are describing: take the squares of the double category to be things built from four 1-morphisms and one 2-morphism in the 2-category. Indeed, as a 2-morphism in the 2-category it is something that goes between the composites of the 1-morphisms, but the resulting square itself in the double category is indeed a 2-morphism to be regarded as going from the top horizontal to the bottom horizontal 1-morphism.

_Toby_:  Don\'t you have to talk about a [[double bicategory]] to get something nontrivial to fill the squares?  I may have this wrong, but that\'s how I remember it.

[[Mike Shulman]]: No, a double bicategory is just a double category in which both composition operations are only associative and unital up to isomorphism.  Sometimes I feel like "double categories" should really have been called "double 2-categories," since they have nontrivial 2-cells.  So it is true that what Eric is interested in are just the 2-cells in the double category $Sq(Cat)$ of "squares" or "quintets" in $Cat$.  As such, they have two different composition operations given by pasting.

Another way to describe it is that these are the morphisms in the 2-category $2Cat_{oplax}(\mathbf{2},Cat)$, where for 2-categories $A$ and $B$, $2Cat_{oplax}(A,B)$ denotes the 2-category whose objects are 2-functors $A\to B$ and whose morphisms are [[oplax natural transformations]], and $\mathbf{2}$ denotes the [[walking arrow]].  Thus an object of $2Cat_{oplax}(\mathbf{2},Cat)$ is a 2-functor $\mathbf{2}\to Cat$, i.e. a functor, and a morphism is an oplax natural transformation, which is precisely what you've described.  Composition of morphisms in $2Cat_{oplax}(\mathbf{2},Cat)$ is one of the above compositions in the double category $Sq(Cat)$.
