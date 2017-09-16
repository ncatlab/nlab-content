# Idea #

Recall that a [[Kan complex]] is a special [[simplicial set]] that [[homotopy hypothesis|behaves like]] a combinatorial model for a [[topological space]].


The _simplicial homotopy groups_ of a Kan complex are accordingly the combinatorial analog of the [[homotopy group]]s of [[topological space]]s: instead of being maps from topological sphere modulo maps from topological disks, they are maps from the [[boundary of a simplex]] modulo those from the [[simplex]] itself. 

Accordingly, the definition of the discussion of simplicial homotopy groups is essentially literally the same as that of ordinary [[homotopy group]]s.  One technical difference is for instance that the definition of the group structure is slightly more non-immediate for simplicial homotopy groups than for topological homotopy groups (see below).


#Definition# 

Recall the classical [[model structure on simplicial sets]]. Let $X$ be a fibrant simplicial set, i.e. a [[Kan complex]].  

Define


* the **0th simplicial homotopy groupoid** $\Pi_0(X)$ to be the [[discrete category|discrete groupoid]] on the _set_ $(X_0/X_1)$ of connected components of $X$,

  * for every $x \in X_0$ the [[pointed set]] $\pi(X,x)$ to be the set $(X_0/X_1)$ of connected components of $X$ with point the connected component $[x]$ of $x \in X_0$;

+-- {: .query}
  I would like the set of connnected components to be the simplicial homotopy $0$-group*oid* $\Pi_0(X)$, while the $0$th simplicial homotopy 'group' itself is (like the following) a property of a *pointed* space: $\pi_0(X,x)$ is the [[pointed set]] $\Pi_0(X)$ equipped with the component of $x$ as point.  That way, the $n$th simplicial homotopy group is really an $n$-[[k-tuply groupal n-groupoid|tuply groupal]] set, as I\'ve done at [[homotopy group]].  (This also becomes strictly a special case of the general definition below, not an exception.)  ---Toby

*  [[Tim Porter|Tim]]: Good point.  In fact the simplicial homotopy groups are defined for _pointed_ simplicial sets, not for arbitrary ones. The traditional terminology is sloppy, since there is usually a caveat that everything is connected, except when it is not, that is.
 
   On the other hand, the idea of a 0th simplicial homotopy *group* is incorrect as it is not a group. Perhaps the trick of putting inverted commas to indicate that it is 'as if but not really' could be used.  

   Of course, there are really two homotopy theories, the pointed one and the non-pointed one.  The first leads to groups, the second to groupoids.

[[Urs Schreiber|Urs]]: I have now tried to implement Toby's comment, as far as it applies to the above. I am not sure though precisely what [[Tim Porter|Tim]]'s comment about pointed simplicial sets is aiming at: if we have a pointed simplicial set we can just talk about $\pi_n(X)$, true, but here we are being more general and talk about $\pi_n(X,x)$ for all $x  \in X$. No? 

*  [[Tim Porter|Tim]]: My point is that the intro refers to the _homotopy groups_ of a Kan complex.  The body of the entry makes it clear that there is one such for each vertex of the Kan complex, which is what Toby is considering. *Homotopy group of $X$* is thus a misnomer. (I am being pedantic in other words!) Saying the n-th homotopy group of $X$ at $x$ does not get around the difficulty, since then one is specifying a pointed complex not just the complex itself.

   I think that Toby's viewpoint is excellent. Perhaps the homotopy group(oids)s are really 'relative' concepts, i.e.  defined for $X$ and a cofibration, $A\to X$, and the usual ones just have $A$ a point. (If I remember rightly this viewpoint was the one adopted by Baues at least to some extent.) The usual groupoidal case is with the terminal cofibration.  I think that this idea is linked to the fact that SSet is monadic over SplitAugSSet, but that can be a very stark but useful viewpoint to adopt. (It would not be favoured by most algebraic topologists however!) 
 
[[Urs Schreiber|Urs]]: I see. Sure, sounds good. Do you want to go ahead and change the terminology as you deem appropriate?

I might have just one minor quibble: while I'd be fine with it, I have to say that it seems that of the following two equivalent sentences, the former is less awkward:

* a morphism $f : X \to Y$ of fibrant simplicial sets is a weak equivalences precisely if it induces an isomorphism on all homotopy groups based at all points of $X$

* a morphism $f : X \to Y$ of fibrant simplicial sets is a weak equivalences precisely if for all  possible ways to interpret $X$ as a pointed simplicial space and for the corresponding structure of a pointed simplicial space induced by $f$ on $Y$, the morphism induces an isomorphism of homotopy groups.

But okay, I am not dogmatic about issues at that fine-grained level of pedantery.

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
there is naturally the structure of a group on $\pi_n(X,x)$ for all $x \in X_0$, $n \geq 1$ that this is an abelian group for all $n \geq 2$.

**Definition (group structure on $\pi_n(X,x)$)**
  
...

**Lemma**

For $n \geq 2$ all the groups $\pi_n(X,x)$ are abelian.


# Weak homotopy equivalences of Kan simplicial sets#

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