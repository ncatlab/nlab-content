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

##Attempt #2

### Definition (Experimental)

##Attempt #1

### Definition (Experimental)

+-- {: .standout}
>Note the **Crash!** below. This definition is not correct. I think something like this should work, but I need to think about it.
=--

Given [[categories]] $C$ and $D$, a pair of [[functors]] $F:C\to D$ and $G:D\to C$ form an **adjunction** if for every morphism $f:x\to y$ in $C$, there are component morphisms 
$$\eta_{y x}: G\circ F(x)\to y$$
and
$$\eta_{x y}: G\circ F(y)\to x$$
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

Note that since $G\circ F:C\to C$ is an [[endofunctor]], there are component morphisms
$$\alpha_x: x\to G\circ F(x)$$
and
$$\alpha_y: y\to G\circ F(y)$$ 
such that the following diagram also commutes:
$$
 \array{
  x &\stackrel{f}{\to}& y
  \\
  \downarrow && \downarrow
  \\
  G\circ F(x) 
  &\stackrel{G\circ F(f)}{\rightarrow}&
  G\circ F(y)
 }.
$$

Putting the two commuting squares together, we have a commuting square with commuting (upward) diagonals giving rise to additional commuting triangles.

These commuting diagrams give rise to the following relations:

* $\eta_{y x}\circ \alpha_x = f$

* $\alpha_y\circ\eta_{y x} = G\circ F(f)$

* $[G\circ F(f)]\circ\alpha_x = \alpha_y\circ f$

* $\eta_{x y}\circ [G\circ F(f)]\circ\alpha_x = 1_x$

* $f\circ\eta_{x y}\circ\alpha_y = 1_y.$

Note: I'm not sure if these are independent or not (need to count how many independent equations we get!), but it is instructive to note:

$$\eta_{x y}\circ \alpha_y\circ\eta_{y x}\circ\alpha_x = 1_x$$

and

$$\eta_{y x}\circ\alpha_x\circ\eta_{x y}\circ \alpha_y = 1_y$$

which means 

$$\eta_{y x}\circ\alpha_x = \left(\eta_{x y}\circ \alpha_y\right)^{-1}.$$

**CRASH!**

I'll need to check, but unless I made some algebra mistake, this last statement might kill the whole idea. Since
$$f = \eta_{y x}\circ\alpha_x,$$
then the above statement says $f$ has an inverse.

### Response from Toby

You need to say more than just that *there are* morphisms that make these diagrams commute.  Whether $F \vdash G$ is an adjunction is not actually a property but a structure; we need to say *how* they are an adjunction.  That is, you have to pick the family of morphism $G(F(x)) \to y$ in advance.

But then you can make it work, I believe ... although I\'m pretty sure that you need more commutative diagrams than the one that you\'ve drawn.  That is, an __adjunction__ $\eta$ from $F$ to $G$ consists of a family of maps $\eta_f\colon G(F(x)) \to y$, one for each morphism $f\colon x \to y$, such that

*  a bunch of diagrams commute.

I have to think about whether this works and what diagrams you need.

[[Eric]]: Thanks Toby. I would be surprised if it were this simple, but I drew some pictures based on the diagram in Goldblatt, and I think this works. 

[[Eric]]: Note, I had some typos in the original version of the diagram, but it should be correct now. Or it least it now matches the diagram on my paper :)

>I\'m pretty sure that you need more commutative diagrams than the one that you\'ve drawn.

We get another commuting square from the fact that $G\circ F$ is an endofunctor. I've now drawn that above. When you put the two together, it gives you a bunch of additional commuting triangles, but everything follows from the one first simple diagram.

[[Eric]]: Hi Toby (and anyone else who may stop by). Note the **Crash!** above. The definition cannot be correct as stated. I probably won't give up though. I think instead of saying the diagram commutes, I need to say something about "commuting up to a 2-morphism" or "there is a 2-morphism such that" blah blah.