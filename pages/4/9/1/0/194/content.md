A _2-morphism_ is a [[k-morphism]] for $k = 2$: what goes between [[morphism|morphisms]] in an [[n-category]] with $n \ge 2$.

A globular $2$-morphism looks like this:

<center><a href="http://www.codecogs.com/eqnedit.php?latex=\xymatrix%20{%20a%20\ar%20@/^1pc/%20[rr]%20\ar%20@/_1pc/%20[rr]%20%26%20\scriptstyle%20\Downarrow%20%26%20b%20}"><img border="0" src="http://latex.codecogs.com/gif.latex?\xymatrix%20{%20a%20\ar%20@/^1pc/%20[rr]%20\ar%20@/_1pc/%20[rr]%20%26%20\scriptstyle%20\Downarrow%20%26%20b%20}" title="\xymatrix { a \ar @/^1pc/ [rr] \ar @/_1pc/ [rr] &amp; \scriptstyle \Downarrow &amp; b }" /></a></center>

A simplicial $2$-morphism looks like this:

$$
  \array{
    && b
    \\
    & \nearrow &\Downarrow& \searrow
    \\
    a &&\to&& c
  }
$$

A cubical $2$-morphism looks like this:

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
? Could there be a 2-morphism without the corresponding 1-morphism components?

=--


[[!redirects 2-morphism]]
[[!redirects 2-morphisms]]
