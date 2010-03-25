#Contents#

+-- {: .standout}
This page is an informal/speculative discussion of an alternative (yet hopefully equivalent) definition of [[adjunction]].
=--

* tic
{: toc}

##Definition (Experimental)

Given [[categories]] $C$ and $D$, a pair of [[functors]] $F:C\to D$ and $G:D\to C$ form an **adjunction** if for any morphism $f:x\to y$ in $C$, there are morphisms 
$$G\circ F(x)\to y$$
and
$$G\circ F(y)\to x$$
such that the following diagram commutes
$$
 \array{
  x &\stackrel{f}{\to}& y
  \\
  \downarrow && \downarrow
  \\
  G\circ F(y) 
  &\stackrel{G\circ F(f)}{\leftarrow}&
  G\circ F(x)
 }.
$$