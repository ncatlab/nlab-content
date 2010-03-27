
<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **2-morphism** in an [[n-category]] is a [[k-morphism]] for $k = 2$: it is a higher morphism between ordinary 1-[[morphism]]s.

So in the hierachty of $n$-categories, the first step where 2-morphisms appear is in a [[2-category]]. This includes cases such as [[bicategory]], [[2-groupoid]] or [[double category]].

## Shapes 

There are different [[geometric shapes for higher structures]]: [[globe]]s, [[simplex|simplices]], [[cube]]s, etc. Accordingly, 2-morphisms mayappear in different guises:

A **globular** $2$-morphism looks like this:

<center><a href="http://www.codecogs.com/eqnedit.php?latex=\xymatrix%20{%20a%20\ar%20@/^1pc/%20[rr]%20\ar%20@/_1pc/%20[rr]%20%26%20\scriptstyle%20\Downarrow%20%26%20b%20}"><img border="0" src="http://latex.codecogs.com/gif.latex?\xymatrix%20{%20a%20\ar%20@/^1pc/%20[rr]%20\ar%20@/_1pc/%20[rr]%20%26%20\scriptstyle%20\Downarrow%20%26%20b%20}" title="\xymatrix { a \ar @/^1pc/ [rr] \ar @/_1pc/ [rr] &amp; \scriptstyle \Downarrow &amp; b }" /></a></center>


A **simplicial** $2$-morphism looks like this:

$$
  \array{
    && b
    \\
    & \nearrow &\Downarrow& \searrow
    \\
    a &&\to&& c
  }
$$

A **cubical** $2$-morphism looks like this:

$$\array{
a & \to & b \\
\downarrow & \Downarrow & \downarrow \\
c & \to & d
}
$$

Of course, using [[identity morphisms]] and [[composition]], we can turn one into the other; which is more fundamental depends on what [[geometric shape for higher categories]] you use.

+--{.query}
[[Eric]]: Are there any consistency requirements for a 2-morphism? For example, in the bigon above, if $f:a\to b$, $g:a\to b$, and $\alpha:f\to g$, are there requirements on $\alpha:f\to g$ regarding $f$ and $g$? For example, should $\alpha$ come with component 1-morphisms $\alpha_a:a\to a$ and $\alpha_b:b\to b$ such that 
$$\alpha_a\circ g = f\circ\alpha_b$$
or maybe
$$\alpha_a\circ g \simeq f\circ\alpha_b$$
? Could there be a 2-morphism without the corresponding 1-morphism components?

[[Urs Schreiber]]: in any given [[2-category]] you have to specify which 2-morphisms exactly there are supposed to be, what $ \alpha $ exactly you allow between $f$ and $g$. When you ask about components, it seems you are thinking of 2-morphisms specifically in the 2-category [[Cat]]. Here, yes, th allowed 2-morphisms are those that are [[natural transformation]]s between their source and target 1-morphisms, which are [[functor]]s.

=--


## Examples

* in the [[2-category]] [[Cat]], 2-morphisms are [[natural transformation]]s between functors.

* In a [[path 2-groupoid]] 2-morphisms are certain surfaces or images of surfaces in a space, going between paths in that space.

[[!redirects 2-morphism]]
[[!redirects 2-morphisms]]
