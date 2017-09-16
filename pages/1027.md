For $f : A \to C$ and $g : B \to C$ two [[morphism]]s in a [[category]] $C$, the **fiber product** 
$A \times_C B$
of $A$ with $B$ over $C$ is, if it exists, [[generalized the|the]] [[pullback]]

$$
  \array{
     A \times_C B &\to& B
     \\
     \downarrow && \downarrow^g
     \\
     A &\stackrel{f}{\to}& C
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

+-- {: .query}

[[Chris Brav| Chris]]: I'd appreciate it if someone could add an explanation of fiber products as limits of compsimplicial diagrams $A \times B, A \times C \times B, A \times C \times C \times A,...$, making the coface maps explicit.

[[Urs Schreiber|Urs]]: I think it should work like this:

the first two coface maps are in full detail given by

$$
  A\times B
  \stackrel{(Id_A \circ p_1) \times (f\circ p_1) \times (Id_B \circ p_2)}{\to}
  A \times C \times B
$$

and

$$
  A\times B
  \stackrel{(Id_A \circ p_1) \times (g\circ p_2) \times (Id_B \circ p_2)}{\to}
  A \times C \times B
$$

With that it is clear that the fiber product 
$A \times_C B$ is the [[equalizer]] of these two maps, i.e. the limit over the diagram

$$
  A \times B \stackrel{\to}{\to}  A \times C \times B
 \,.
$$

I am guessing, but haven't really checked in detail that the further coface maps continue this: the "inner" ones come from the diagonal $C \to C \times C$ and the outer ones from $f$ and $g$ as above. So for instance the next three would be

$$
  A \times C \times B
  \stackrel{(Id_A \circ p_1) \times (f \circ p_1) \times ( Id_C\circ p_2) \times (Id_B \circ p_3)}{\to}
  A \times C  \times C \times B
$$

and

$$
  A \times C \times B
  \stackrel{(Id_A \circ p_1) \times (Id_C \times Id_C \circ p_2) \times (Id_B \circ p_3)}{\to}
  A \times C  \times C \times B
$$

and

$$
  A \times C \times B
  \stackrel{(Id_A \circ p_1) \times (Id_C \circ p_2) \times ( g \circ p_3) \times (Id_B \circ p_3)}{\to}
  A \times C  \times C \times B
$$

This way, unless I am making a mistake, the ordinary limit over the diagram 

$$
  A \times B \stackrel{\to}{\to}
  A \times C \times B
  \stackrel{\to}{\stackrel{\to}{\to}}
  A \times C \times C \times B
$$

would still be $A \times_C B$, but the homotopy limit would pick up the right first degree correction for the homotopy fiber product.




=--


