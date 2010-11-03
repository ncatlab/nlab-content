
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In the category [[Set]] a 'pullback' is a [[subset]] of the [[cartesian product]] of two [[set]]s.  Given a [[diagram]] of [[set]]s and [[function]]s like this:

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

This construction comes up, for example, when $A$ and $B$ are [[fiber bundle]]s over $C$: then $X$ as defined above is the [[product]] of $A$ and $B$ in the category of fiber bundles over $C$.  For this reason, a pullback is sometimes called a [[fibered product]].

Note that there are maps $p_A : X \to A$, $p_B : X \to B$ sending any $(a,b) \in X$ to $a$ and $b$, respectively.  These maps make this [[commuting diagram|square commute]]:

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

In fact, the pullback is the [[universal property|universal]] solution to finding a commutative square like this.  In other words, given _any_ [[commutative diagram|commutative square]] 

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

## Definition

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

Such a diagram is also called a *pullback diagram** or a [[cospan]].  If the [[limit]] exists, we obtain a commutative square

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

and [[generalized the|the]] object $x$ is also called the **pullback**. It is well defined up to unique [[isomorphism]]. It has the universal property already described above in the special case of the category $Set$.

The last commutative square above is called a __pullback square__.

The concept of pullback is dual to the concept of [[pushout]]: that is, a pullback in $C$ is the same as a pushout in the [[opposite category]] $C^{op}$.

## Properties

### As an equalizer

If [[product]]s exist in $C$, then the pullback

$$
  \array{
     a \times_c b &\to& a
     \\
     \downarrow && \downarrow^{\mathrlap{f}}
     \\
     b &\stackrel{g}{\to}& c
  }
$$

is equivalently the [[equalizer]]

$$
  a \times_c b \to a \times b \stackrel{\overset{f p_1}{\to}}{\underset{g p_2}{\to}}
  c
$$

of the two morphisms induced by $f$ and $g$ out of the [[product]] of $a$ with $b$.

### Pasting of pullbacks {#Pasting}

Consider a [[pasting diagram]] of the form

$$
  \array{
     a &\to& b &\to& c
     \\ 
     \downarrow && \downarrow && \downarrow
     \\
     d &\to& e &\to& f
  }
  \,.
$$

There are three commuting squares: the two inner ones and the outer one.

+-- {: .un_prop}
###### Proposition

Suppose the right-hand inner square is a pullback: then the left-hand one is a pullback if and only if the outer square is.

=--

+-- {: .proof}
_Proof_.  Pasting a morphism $x \to a$ with the outer square gives rise to a commuting square over the (composite) bottom and right edges of the diagram.  The square over the cospan in the left-hand inner square arising from $x \to a$ includes a morphism into $b$, which if $b$ is a pullback induces the same commuting square over $d \to e \to f$ and $c \to d$.  So one square is universal iff the other is.
=--


+-- {: .un_prop}
###### Proposition

The converse implication does not hold: it may happen that the outer and the left square are pullbacks, but not the right square. 

=--

For instance let $i : a \to b$ be a [[split monomorphism]] with [[retract]] $p : b \to a$ and consider

$$
  \array{
     a & \stackrel{=}{\to} & a & \stackrel{=}{\to} & a
     \\ 
     \downarrow^{\mathrlap{=}} && \downarrow^{\mathrlap{i}} && \downarrow^{\mathrlap{=}}
     \\
     a &\stackrel{i}{\to}& b &\stackrel{p}{\to}& a
  }
$$

Then the left square and  the outer rectangle are pullbacks but the right square cannot be a pullback unless $i$ was already an [[isomorphism]].





## See also:
* [[base change]]
* [[homotopy pullback]]
* [[2-limit]] for pullbacks in a [[2-category]]
* [[wide pullback]]

[[!redirects pullbacks]]
[[!redirects pullback square]]

[[!redirects pullback diagram]]