#Idea#

The _Kan extension_ of a [[functor]]
$F : C \to D$ with respect to a functor
$$
 \array{
  C
  \\
  \downarrow^p
  \\
  C'
 }
$$

is, if it exists, the "best approximation" to extending the domain of $F$ through $p$ from $C$ to $C'$.


#Definition#

The functor $p : C \to C'$ induces, by precomposition, a functor between [[functor category|functor categories]]
$$
  p^* : [C',D] \to [C,D]
  \,.
$$

The [[left adjoint]] to $p^*$ is **left Kan extension** of functors
$$
  Lan : [C,D] \to [C',D]
  \,,
$$
and the [[right adjoint]] is **right Kan extension** of functors
$$
  Ran : [C,D] \to [C',D]
  \,.
$$


#More details#


Precomposition with $p$ yields a pullback functor
on [[functor category|functor categories]]
$$
 p^* : [E,D] \to [C,D]
 \,.
$$

* The image $Ran F := L_{p^*}$ of $F$ under the [[left adjoint]]
$L_{p^*}$ of $p^*$ is the **right Kan extension** of $F$.

* The image $Lan F := R_{p^*}$ of $F$ under the [[right adjoint]]
$R_{p^*}$ of $p^*$ is the **left Kan extension** of $F$.
$$
  \array{
    C &&\stackrel{F}{\to}& D
    \\
    \downarrow & \Downarrow& \nearrow_{Lan F}
    \\
    E
  }
$$

$$
  \array{
    C &&\stackrel{F}{\to}& D
    \\
    \downarrow & \Uparrow& \nearrow_{Ran F}
    \\
    E
  }
$$



(...)

#References#

Chapter 4 of

* G.M. Kelly, _Basic Concepts of Enriched Category Theory_, 
 Cambridge University Press, Lecture Notes in Mathematics 64, 1982,  Republished in:
Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))


