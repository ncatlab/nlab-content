#Definition#

A **point $x$ of a [[topos]] $E$** is a [[geometric morphism]]
$$
  x : Set \to E
  \,.
$$

That is, it\'s a [[global element]] of the topos.

+--{.query}
Zoran: now one can redefine easily each functor by taking isomorphic representatives. So, in this definition one clearly does not count isomorphic geometric morphisms, or instead of adjoint functors takes classes of isomorphisms of them. Right ? 

Todd: How much does it matter? It matters if for example you want to say that points of $Sh(X)$, $X$ a sober space, are in bijection with points of $X$. Otherwise one can just refer back to equivalence of categories, unless you see a problem with that. 

=--

## points of sheaf topoi ##

For the special case that $E = Sh(X)$ is the [[category of sheaves]] on a [[category of open subsets]] $Op(X)$ of a [[topological space]] $X$ this notion of point of a topos comes from the ordinary notion of points of $X$.

For notice that

* $Set = Sh(*)$ is simply the [[topos]] of [[sheaf|sheaves]] on a one-[[point]] [[topological space|space]].  

* [[geometric morphisms]] $f : Sh(Y) \to Sh(X)$ between [[category of sheaves|sheaf topoi]] are in a bijection with continuous functions of topological spaces $f : Y \to X$ (denoted by the same letter, by convenient abuse of notation).

It follows that for $E = Sh(X)$ points of $E$ in the sense of points of topoi are in bijection with the ordinary points of $X$.

The action of the [[direct image]] $x^* : Set \to Sh(X)$ and the [[inverse image]] $x_* : Sh(X) \to Set$ of a point $x : Set \to Sh(X)$ of a sheaf topos have special interpretation and relevance:

* The [[direct image]] of a set $S$ under the point $x : {*} \to X$ is, by definition of [[direct image]] the sheaf
  $$
    x_*(S) : (U \subset X) \mapsto S(x^{-1}(U)) = 
    \left\{
      \array{
        S & if x \in U
        \\
        {*} & otherwise
      }
    \right.
  $$
 This is the [[skyscraper sheaf]] $skysc_x(S)$ with value $S$ supported at $X$. (In the first line on the right in the above we identify the set $S$ with the unique sheaf on the point it defines. Notice that $S(\emptyset) = pt$).

* The [[inverse image]] of a sheaf $A$ under the point $x : {*} \to X$ is by definition of [[inverse image]] (see the [[Kan extension]] formula discussed there), the set
  $$
    \begin{aligned}
       x^*(A) & = 
       colim_{{*} \to x^{-1}(V)} A(V)
       \\
       &=
       colim_{V\subset X| x \in V} F(V)
    \end{aligned}
    \,.
  $$
  This is the [[stalk]] of $A$ at he point $x$,
  $$
    x^*(-) = stalk_x(-)
    \,.
  $$

By definition of [[geometric morphisms]], taking the stalk at $x$ is [[left adjoint]] to forming the skyscraper sheaf at $x$:

for all $S \in Set$ and $A \in Sh(X)$ we have
$$
  Hom_{Set}(stalk_x(A), S) \simeq
  Hom_{Sh(X)}(A, skysc_x(S))
  \,.
$$


## points of classifying topoi ##

On the other hand, if $E$ is the [[classifying topos]] of a [[geometric theory]] $T$, then a point of $E$ is the same as a model of $T$ in [[Set]].

#enough points#

A [[topos]] is said to have **enough points** if isomorphy can be tested [[stalk]]wise.

More precisely: if it is true that every morphism $f : A \to B$ such that for every point $p$ of the topos the morphism of [[stalks]] $p^* f : p^* A \to p^* B$ is an isomorphism implies already that $f$ itself is an isomorphism.


##Examples##

* For $X$ any [[topological space]], the  [[category of sheaves|topos of sheaves]] on (the [[category of open subsets]] of) $X$ has enough points: a morphism of sheaves is a mono-/epi-/isomorphism precisely if it is so on every [[stalk]]. 

+--{.query}

_Todd_: I don't have much time to think about this now, but I doubt this is true. A "point" of $Sh(X)$ corresponds to a closed irreducible set of $X$, and there may be very few of these. The claim is true though if $X$ is sober. 

=-- 

* Let $Diff$ be a [[small category]] version of the category of smooth manifolds (for instance take it to be the category of manifolds embedded in $\mathbb{R}^\infty$). Then the sheaf topos $Sh(Diff)$ has precisely one point $p_n$ per natural number $n \in \mathbb{N}$ , corresponding to the $n$-ball: the [[stalk]] of a sheaf on $Diff$ at that point is the colimit over the result of evaluating the sheaf on all $n$-dimensional smooth balls.

  This is discussed for instance on p. 36 of 

  * Dan Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

  in the context of the [[model structure on simplicial presheaves]].

#References#

section 7.5 of 

* MacLane Moerdijk, [[Sheaves in Geometry and Logic]]

[[Note on Formatting|✄]]

[[!redirects point of topos]]