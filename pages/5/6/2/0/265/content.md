#Definition#

For $Core(C) \hookrightarrow W \hookrightarrow C$ a [[category with weak equivalences]], and for $F : C \to D$ any functor, the __left derived functor__ $L F$ of $F$ is the _right_ [[Kan extension]] of $F$ along the projection $p : C \to Ho_C$ to the [[homotopy category]]

$$
 \array{
   C &&\stackrel{F}{\to}&& D
   \\
   \downarrow^p &\Downarrow& \nearrow_{L F}
   \\
   Ho_C
 }
$$

(if it exists).  Dually, the __right derived functor__ $R F$ of $F$ is its _left_ Kan extension along $p$.  Note the reversal of handedness; this is unfortunate but unavoidable.

More generally, if $D$ is itself a category with weak equivalences, then by derived functors of $F$ we often mean derived functors of the composite

$$ C \stackrel{F}{\to} D \to Ho_D $$


#Remarks#

* By the universal property of $Ho_C$, functors $Ho_C \to D$ are equivalent to functors $C\to D$ which take weak equivalences to isomorphisms.  If $F$ itself takes weak equivalences to isomorphisms, then its left and right derived functors are both (isomorphic to) its unique extension along $p$.  In general, however, $L F$ and $R F$ are not extensions of $F$ even up to isomorphism.


* The Kan extensions involved here are _not_ "pointwise" ones, meaning that they are not computed by limits and colimits objectwise.  This means that they lack many of the good properties of ordinary Kan extensions.  

* In practice, derived functors are usually computed using fibrant and cofibrant replacements (see the entries on [[homotopy theory]] and [[model category]]) or, more generally, [[deformation retract|deformation retracts]].

* The connection to the [more elementary notion](http://en.wikipedia.org/wiki/Derived_functor) of derived functor in homological algebra that you may be used to is as follows. A functor $F:A \to B$ between [[abelian category|abelian categories]] induces a functor $Ch(F):Ch(A) \to Ch(B)$ between categories of [[chain complex|chain complexes]], each of which can be equipped with the class of [[quasi-isomorphism|quasi-isomorphisms]] as weak equivalences.  We obtain the usual derived functors of $F$ by taking the derived functor of $Ch(F)$ in the above sense, evaluating it at an object of $A$ regarded as a chain complex concentrated in degree zero, and then taking the homology of the resulting chain complex in $B$.
