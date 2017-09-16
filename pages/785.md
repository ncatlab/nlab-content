#Idea#

A **homotopy pullback** is a [[pullback]] in the context of [[homotopy coherent category theory]].

#Definition#

Let $C$ be a [[homotopical category]] with a notion of [[homotopy limit]]s at least over [[pullback]] diagrams 
$X \to Z \leftarrow Y$.

A [[commutative square]] 
$$
  \array{
   W & \to& Y
   \\
    \downarrow && \downarrow
   \\
   Y &\to& X
  }
$$
in $C$ is a [[homotopy pullback]] square if the induced morphism $W \to holim(X \to Z \leftarrow Y)$ from $W$ to the [[homotopy limit]] is a [[weak equivalence]].

#Homotopy fiber product#

In many contexts one can make concrete sense of homotopy pullbacks without invoking or even requiring the full machinery of [[homotopy limit]]s.

Let $C$ be a [[closed monoidal homotopical category]] with [[interval object]] $I$ such that for every object $Z$ of $C$ the object $[I,Z]$ is a [[path object]] for $Z$. 

+-- {: .un_defn}
###### Definition

For $X \to Z \leftarrow Y$ a diagram
the **homotopy fiber product** $X \times_{Z^I} Y$ of $X$ with $Y$ over $Z$ is the (ordinary) [[limit]]

$$
  \array{
     X \times_{Z^I} Y
     &\to&\to& \to& X
     \\
     \downarrow
     &&&& 
     \downarrow
     \\
     \downarrow
     &
     &
     [I,Z]
     &\stackrel{d_1}{\to}&
     Z
     \\
     \downarrow
     &
     &
     \downarrow^{d_0}
     \\
     X
     &
     \to
     &
     Z
  }
  \,.
$$


=--

Notice that the morphism $Z \to [I,Z]$ which is a [[section]] of $d_0, d_1 : [I,Z] \to Z $ by the axioms of [[interval object]] induces a canonical morphism
$$
  X \times_{Z^I} Y \to X \times_Z Y
  \,.
$$

In this concrete setup
a [[commutative square]] 
$$
  \array{
   W & \to& Y
   \\
    \downarrow && \downarrow
   \\
   Y &\to& X
  }
$$
in $C$ is a [[homotopy pullback]] square if the induced morphism 
$$
  W \to X \times_Z Y \to X \times_{Z^I} Y
$$ 
from $W$ to the [[homotopy limit]] is a [[weak equivalence]].

In this form the homotopy pullback appears for instance on [p. 28](http://www-math.mit.edu/~lurie/papers/cobordism.pdf#page=28) of 

* Jacob Lurie, _On the classification of TFT_ ([pdf](http://www-math.mit.edu/~lurie/papers/cobordism.pdf))

for the case $C = $ [[Top]] with its canonical [[interval object]].

##Homotopy fiber product in categories of fibrant objects#

Expressing the homotopy pullback in terms of a homotopy fiber product induced from an [[interval object]] is useful also for $C$ a [[category of fibrant objects]]. Further details on that case are described in [section 5](http://ncatlab.org/schreiber/files/nacqFeb14.pdf#page=21) of [[schreiber:Nonabelian cocycles and their sigma model QFTs]].