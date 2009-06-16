# Idea #

Recall that a [[Kan complex]] is a special [[simplicial set]] that [[homotopy hypothesis|behaves like]] a combinatorial model for a [[topological space]].


The _simplicial homotopy groups_ of a Kan complex are accordingly the combinatorial analog of the homotopy groups of topological spaces: instead of being maps from topological sphere modulo maps from topological disks, they are maps from the [[boundary of a simplex]] modulo those from the [[simplex]] itself.


#Definition# 

Recall the classical [[model structure on simplicial sets]]. Let $X$ be a fibrant simplicial set, i.e. a [[Kan complex]].  

Define

* the **0th simplicial homotopy group** $\pi_0(X) := X_0/X_1$ of $X$  to be the set of connected components of it;

+-- {: .query}
  I would like the set of connnected components to be the simplicial homotopy $0$-group*oid* $\Pi_0(X)$, while the $0$th simplicial homotopy 'group' itself is (like the following) a property of a *pointed* space: $\pi_0(X,x)$ is the [[pointed set]] $\Pi_0(X)$ equipped with the component of $x$ as point.  That way, the $n$th simplicial homotopy group is really an $n$-[[k-tuply groupal n-groupoid|tuply groupal]] set, as I\'ve done at [[homotopy group]].  (This also becomes strictly a special case of the general definition below, not an exception.)  ---Toby

*  [[Tim Porter|Tim]]: Good point.  In fact the simplicial homotopy groups are defined for _pointed_ simplicial sets, not for arbitrary ones. The traditional terminology is sloppy, since there is usually a caveat that everything is connected, except when it is not, that is.
 
   On the other hand, the idea of a 0th simplicial homotopy *group* is incorrect as it is not a group. Perhaps the trick of putting inverted commas to indicate that it is 'as if but not really' could be used.  

   Of course, there are really two homotopy theories, the pointed one and the non-pointed one.  The first leads to groups, the second to groupoids.
=--

* for every $n \geq 1$ and $x \in X_0$ the **$n$th simplicial homotopy group** of $X$ at $x$ to be the set 

  * of equivalence classes of morphism
  $$
    \alpha : \Delta^n \to X
  $$ 
  from the simplicial $n$-[[simplex]] $\Delta^n$ to $X$, 

    * such that they fit into the diagram
    $$
      \array{
        \partial \Delta^n &\to&  \Delta^0
        \\
        \downarrow && \downarrow
        \\
        \Delta^n &\stackrel{\alpha}{\to}& X
      };
    $$
    meaning that all of the boundary of $\Delta^n$ maps to the single point $x$;

  * where two such maps $\alpha, \alpha'$ are taken to be equivalent is they are related by a [[simplicial homotopy]] $\eta$
    $$
      \array{
        \Delta^n
        \\
        \downarrow^{i_0} & \searrow^{\alpha}
        \\
        \Delta^n \times \Delta^1
        &\stackrel{\eta}{\to}&
        X
        \\
        \uparrow^{i_1} & \nearrow_{\alpha'}
        \\
        \Delta^n 
      }
    $$

   * that fixes the boundary
     $$
       \array{
         \partial \Delta^n \times \Delta^1 
         &\to&
         \Delta^0
         \\
         \downarrow && \downarrow
         \\
         \Delta^n  \times \Delta^1
         &\stackrel{\eta}{\to}&
         X
       }
       \,.
     $$


One shows as in the case for topological spaces that 

* there is naturally the structure of a group on $\pi_n(X,x)$ for all $x \in X_0$, $n \geq 1$;

  * that this is an abelian group for all $n \geq 2$.


For $X$ and $Y$ [[model structure on simplicial sets|fibrant]] simplicial sets, i.e. [[Kan complex]]es, a morphism $f : X \to Y$ is a weak eqivalence with respect to the classical [[model structure on simplicial sets]] if 

$$
  f_* : \pi_0(X) \to \pi_0(Y)
$$

and

$$
  f_* : \pi_n(X,x) \to \pi_n(Y,f(x))
$$

are [[isomorphism]]s.


#References#

[chapter 1](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-1.dvi) of 

* **GoerJard**, Goerss, Jardine, _Simplicial homotopy theory_ 