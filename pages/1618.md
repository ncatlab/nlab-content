#Definition#

A **point $x$ of a [[topos]] $E$** is a [[geometric morphism]]
$$
  x : Set \to E
  \,.
$$

That is, it\'s a [[global element]] of the topos.

## points of sheaf topoi ##

For the special case that $E = Sh(X)$ is the [[category of sheaves]] on a [[category of open subsets]] $Op(X)$ of a [[topological space]] $X$ this notion of point of a topos comes from the ordinary notion of points of $X$.

For notice that

* $Set = Sh(*)$ is simply the [[topos]] of [[sheaf|sheaves]] on a one-[[point]] [[topological space|space]].  

* [[geometric morphism]]s $f : Sh(Y) \to Sh(X)$ between [[category of sheaves|sheaf topoi]] are in bijection with continmuous functions of topological spaces $f : Y \to X$ (denoted by the same letter, by convenient abuse of notation).

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

By definition of [[geometric morphism]]s, taking the stalk at $x$ is [[left adjoint]] to forming the skyscraper sheaf at $x$:

for all $S \in Set$ and $A \in Sh(X)$ we have
$$
  Hom_{Set}(stalk_x(A), S) \simeq
  Hom_{Sh(X)}(A, skysc_x(S))
  \,.
$$


## points of classifying topoi ##

On the other hand, if $E$ is the [[classifying topos]] of a [[geometric theory]] $T$, then a point of $E$ is the same as a model of $T$ in $Set$.


#References#

section 7.5 of 

* MacLane Moerdijk, [[Sheaves in Geometry and Logic]]
