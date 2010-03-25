This page is a result of the following question originally asked at [[adjunction]]:

+-- {: .query}
[[Eric]]: Is it true that given categories $C$ and $D$ that functors $F:C\to D$ and $G:D\to C$ form an adjunction if the following diagram commutes for all morphisms $f:x\to y$ in $C$?

$$
 \array{
  x &\stackrel{f}{\to}& y
  \\
  \uparrow && \uparrow
  \\
  G\circ F(y) 
  &\stackrel{G\circ F(f)}{\leftarrow}&
  G\circ F(x)
 }
$$

If so, is that an "if and only if" so that you can define adjunctions this way? If so, this would, in my opinion, be the most digestible way to define adjunctions for "scientists and engineers".
=--


#Contents#

+-- {: .standout}
This page is an informal/speculative discussion of an alternative (yet hopefully equivalent) definition of [[adjunction]].
=--

* tic
{: toc}


## Definition (Experimental)

Given [[categories]] $C$ and $D$, a pair of [[functors]] $F:C\to D$ and $G:D\to C$ form an **adjunction** if for every morphism $f:x\to y$ in $C$, there are morphisms 
$$G\circ F(x)\to y$$
and
$$G\circ F(y)\to x$$
such that the following diagram commutes
$$
 \array{
  x &\stackrel{f}{\to}& y
  \\
  \uparrow && \uparrow
  \\
  G\circ F(y) 
  &\stackrel{G\circ F(f)}{\leftarrow}&
  G\circ F(x)
 }.
$$


## Response from Toby

You need to say more than just that *there are* morphisms that make these diagrams commute.  Whether $F \vdash G$ is an adjunction is not actually a property but a structure; we need to say *how* they are an adjunction.  That is, you have to pick the family of morphism $G(F(x)) \to y$ in advance.

But then you can make it work, I believe ... although I\'m pretty sure that you need more commutative diagrams than the one that you\'ve drawn.  That is, an __adjunction__ $\eta$ from $F$ to $G$ consists of a family of maps $\eta_f\colon G(F(x)) \to y$, one for each morphism $f\colon x \to y$, such that

*  a bunch of diagrams commute.

I have to think about whether this works and what diagrams you need.

[[Eric]]: Thanks Toby. I would be surprised if it were this simple, but I drew some pictures based on the diagram in Goldblatt, and I think this works. 

[[Eric]]: Note, I had some typos in the original version of the diagram, but it should be correct now. Or it least it now matches the diagram on my paper :)