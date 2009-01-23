#The idea

In the category [[Set]] a 'pushout' is a quotient of the disjoint union of two sets.  Given a diagram of sets and functions like this:

$$
  \array{
 &&&&
     C
     &&&&
      \\
      & 
      && f \swarrow
       &
       & \searrow g
      && 
     \\
&& A &&&& B
  }
$$

the 'pushout' of this diagram is the set $X$ obtained by taking the disjoint union $A + B$ and identifying $a \in A$ with $b \in B$ if there exists $x \in C$ such that $f(x) = a$ and $g(x) = b$.  

This construction comes up, for example, when $C$ is the intersection of the sets $A$ and $B$, and $f$ and $g$ are the obvious inclusions.  Then the pushout is just the union of $A$ and $B$.

Note that there are maps $i_A : A \to X$, $i_B : B \to X$ such that $i_A(a) = [a]$ and $i_B(b) = [b]$ respectively.  These maps make this square commute:

$$
  \array{
 &&&&
     C
     &&&&
      \\
      & 
      && f \swarrow
       &
       & \searrow g
      && 
     \\
&& A &&&& B
\\
      & 
      && {}_{i_A}\searrow
       &
       & \swarrow_{i_B}
      && 
     \\
&&&&
     X
     &&&&
  }
$$

In fact, the pullback is the [[universal property|universal]] solution to finding a commutative square like this.  In other words, given _any_ commutative square 

$$
  \array{
 &&&&
     C
     &&&&
      \\
      & 
      && f \swarrow
       &
       & \searrow g
      && 
     \\
&& A &&&& B
\\
      & 
      && {}_{j_A}\searrow
       &
       & \swarrow_{j_B}
      && 
     \\
&&&&
     Y
     &&&&
  }
$$

there is a unique function $h: Y \to X$ such that 
$$ h j_A = i_A $$
and
$$ h j_A = i_B .$$
Since this universal property expresses the concept of pullback purely arrow-theoretically, we can formulate it in any category.  It is, in fact, a simple special case of a [[colimit]].  

#Definition

A **pushout** is a [[colimit]] of a [[diagram]] like this:

$$
  \array{
 &&&&
     c
     &&&&
      \\
      & 
      && f \swarrow
       &
       & \searrow g
      && 
     \\
&& a &&&& b
  }
$$

Such a diagram is called a [[span]].  If the colimit exists, we obtain a commutative square

$$
  \array{
 &&&&
     c
     &&&&
      \\
      & 
      && f \swarrow
       &
       & \searrow g
      && 
     \\
&& a &&&& b
\\
      & 
      && {}_{i_a}\searrow
       &
       & \swarrow_{i_b}
      && 
     \\
&&&&
     x
     &&&&
  }
$$

and the object $x$ is also called the **pushout**.  It has the universal property already described above in the special case of the category $Set$.

Note that the concept of pushout is dual to the concept of [[pullback]]: that is, a pushout in $C$ is the same as a pullback in $C^{op}$.
