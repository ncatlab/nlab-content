## Definition

A **constant functor** $\Delta(d):C\to D$ is a [[functor]] that maps each object of $C$ to a fixed object $d\in D$ and each morphism of $C$ to the identity morphism of that fixed object.

Note that a constant functor can be expressed as the composite
$$C \stackrel{!}{\to} 1 \stackrel{[d]}{\to} D.$$ 

Here $1$ is a [[terminal category]] (exactly one object and exactly one morphism, namely the identity), and $[d]$ denotes the unique functor from $1$ with $F(\bullet) = d$ and $F(Id_\bullet) = Id_d$. 

+--{.query}
[[Eric]]: Is there a standard notation for constant functor? I had originally written $d!:C\to D$ which is kind of fitting given the composite, i.e. $d! = [d]\circ !$. If there is no established standard, I may change it. Opinions?

_Toby_:  I don\'t think that there is.  Sometimes people write it $K_d$, $const_d$, or even just $d$.

[[Mike Shulman]]: $\Delta d$ is fairly common too, I think.
=--
