##The idea

In the category [[Set]] a 'pullback' is a subset of the cartesian product of two sets.  Given a diagram of sets and functions like this:
$$
  \array{
     && A &&&& B
      \\
      & 
      && {}_{f}\searrow
       &
       & \swarrow_g
      && 
     \\
     
     &&&&
     C
     &&&&
     
  }
$$
the 'pullback' of this diagram is the subset $X \subseteq A \times B$ consisting of pairs $(a,b)$ such that $f(a) = g(b)$.  

This construction comes up, for example, when $A$ and $B$ are fiber bundles over $C$: then $X$ as defined above is the product of $A$ and $B$ in the category of fiber bundles over $C$.  For this reason, a pullback is sometimes called a [[fibered product]].

Note that there are maps $p_A : X \to A$, $p_B : X \to B$ sending any $(a,b) \in X$ to $a$ and $b$, respectively.  These maps make this square commute:
$$
  \array{
     &&&& X 
     \\& 
    &&
      {}^{p_A}\swarrow
      && \searrow^{p_B}
    \\
     && A &&&& B
      \\
      &
      && {}_f\searrow
       &
       & \swarrow_{g}
      &&
     \\
     &&&&
     C
     &&&&
  }
$$

In fact, the pullback is the [[universal property|universal]] solution to finding a commutative square like this.  In other words, given _any_ commutative square 
$$
  \array{
     &&&& Y
     \\& 
    &&
      {}^{q_A}\swarrow
      && \searrow^{q_B}
    \\
     && A &&&& B
      \\
      &
      && {}_f\searrow
       &
       & \swarrow_{g}
      &&
     \\
     &&&&
     C
     &&&&
  }
$$
there is a unique function $h: X \to Y$ such that 
$$ q_A h = p_A $$
and
$$ q_B h = p_B .$$
Since this universal property expresses the concept of pullback purely arrow-theoretically, we can formulate it in any category.  It is, in fact, a simple special case of a [[limit]].

##Definition

A **pullback** is a [[limit]] of a [[diagram]] like this:
$$
  \array{
     && a &&&& b
      \\
      & 
      && {}_{f}\searrow
       &
       & \swarrow_g
      && 
     \\
     
     &&&&
     c
     &&&&
     
  }
$$
Such a diagram is called a [[cospan]].  If the limit exists, we obtain a commutative square
$$
  \array{
     &&&& x 
     \\& 
    &&
      {}^{p_a}\swarrow
      && \searrow^{p_b}
    \\
     && a &&&& b
      \\
      &
      && {}_f\searrow
       &
       & \swarrow_{g}
      &&
     \\
     &&&&
     c
     &&&&
  }
$$
and the object $x$ is also called the **pullback**.  It has the universal property already described above in the special case of the category $Set$.

The last commutative square above is called a __pullback square__.

Note that the concept of pullback is dual to the concept of [[pushout]]: that is, a pullback in $C$ is the same as a pushout in $C^{op}$.

## See also:
* [[base change]]
* [[homotopy pullback]]
* [[2-limit]] for pullbacks in a [[2-category]]
* [[wide pullback]]

[[!redirects pullbacks]]
[[!redirects pullback square]]