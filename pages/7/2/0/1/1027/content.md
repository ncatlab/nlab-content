For $f : A \to C$ and $g : B \to C$ two [[morphism]]s in a [[category]] $C$, the **fiber product** 
$A \times_C B$
of $A$ with $B$ over $C$ is, if it exists, [[generalized the|the]] [[pullback]]

$$
  \array{
     A \times_C B &\to& B
     \\
     \downarrow && \downarrow
     \\
     A &\to& C
  }
  \,.
$$

This term comes from thinking of $A$ and $B$ as [[bundle]]s over $C$; then the fiber of $A \times_C B$ over a [[generalized element]] $x$ of $C$ is the [[product]] of the fibers of $A$ and $B$ over $x$.  In other words, the fiber product is the product taken fiber-wise.

Of course, the fiber of $A$ at the generalized element $x: I \to C$ is itself a pullback $I \times_C A$; the terminology depends on your point of view.

#Examples#

In $C =$ [[Set]] the fiber product is given by the usual formula
$$
  A \times_C B = 
  \left\{
    (a,b) \in A \times B \;|\;
    f(a) = g(b) 
  \right\}
  \,.
$$

>[[Chris Brav| Chris]]: I'd appreciate it if someone could add an explanation of fiber products as limits of compsimplicial diagrams $A \times B, A \times C \times B, A \times C \times C \times A,...$, making the coface maps explicit.