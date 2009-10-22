#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

For $X$ and $Y$ [[topological spaces]], a continuous map $X \to Y$ induces (in particular) two [[functors]]

* the [[direct image]] $f_* : Sh(X) \to Sh(Y)$


* the [[inverse image]] $f^* : Sh(Y) \to Sh(X)$

between the corresponding  [[Grothendieck topos|Grothendieck topoi]] of [[sheaf|sheaves]] on $X$ and $Y$. These are such that:

* $f^*$ is [[adjoint functor|left adjoint]] to $f_*$, so $f^*$ preserves all small [[colimits]] and $f_*$ preserves all small [[limits]].

* furthermore, $f^*$ is [[exact functor|left exact]] in that it preserves finite [[limits]].

Morever, if $X$ and $Y$ are 
[[sober space|sober]] [[topological spaces]]
every pair of functors with these properties comes uniquely from a continuous map $X \to Y$ (see the theorem below).

A _geometric morphism_ between arbitrary [[topos|topoi]] is the direct generalization of this situation.

Another motivation of the concept comes from the the fact that a [[functor]] such as $f^*$ that preserves finite [[limits]] and arbitrary [[colimits]] (since it is a [[adjoint functor|left adjoint]]) necessarily preserves all constructions in [[geometric logic]].  See also [[classifying topos]].



#Definition#

If $E$ and $F$ are [[topos|toposes]], a **geometric morphism** $f:E\to F$ consists of an pair of [[adjoint functors]] $(f^*,f_*)$
$$
  f_* : E \to F
$$
$$
  f^* : F \to E
  \,,
$$

such that the left adjoint $f^*:F \to E$ preserves finite [[limits]].



#Remarks#

* Since [[Grothendieck topos|Grothendieck toposes]] satisfy the (dual) hypotheses of Freyd's special [[adjoint functor theorem]], any functor $f^*$ between Grothendieck toposes which preserves all small colimits must have a right adjoint.  Therefore, a geometric morphism between Grothendieck toposes could equivalently be defined as a functor preserving finite limits and all small colimits.


#Surjections and embeddings#

A geometric morphism $f : E \to F$ is a **surjection** if $f^*$ is [[faithful functor|faithful]].  It is an **[[geometric embedding|embedding]]** if $f_*$ is [[full and faithful functor|fully faithful]].

+--{: .un_prop}
###### Proposition
Up to equivalence, every [[geometric embedding|embedding]] of toposes is of the form 
$$
  Sh_j(E) \to E
  \,,
$$
where $Sh_j(E)$ is the topos of [[sheaf|sheaves]] with respect to a [[Lawvere-Tierney topology]] $j : \Omega \to \Omega$ on $E$.
=--

This means in particular that fully faithful geometric morphisms into [[Grothendieck topos|Grothendieck topoi]] are an equivalent way of encoding a [[Grothendieck topology]]. 

+--{: .un_prop}
###### Proposition
Up to equivalence, every surjection of topoi is of the form 
$$ E \to E_G $$
where $E_G$ is the category of coalgebras for a finite-limit-preserving [[comonad]] on $E$.
=--

Every geometric morphism $f:E\to F$ factors, uniquely up to equivalence, as a surjection followed by an embedding.  There are two ways to produce this factorization: either construct $E_G$ where $G= f^*f_*$ is the comonad induced by the adjunction $f^*\dashv f_*$, or construct $Sh_j(F)$ where $j$ is the smallest Lawvere-Tierney topology on $F$ such that $f$ factors through $Sh_j(F)$.  In fact, surjections and embeddings form a 2-categorical [[orthogonal factorization system]] on the 2-category of topoi.

#Examples#

* For $E$ any [[topos]] and $k : B \to A$ any morphism in $E$ there is the [[base change|change-of-base]] functor of [[over category|over categories]] 
$$
  k^* (E/A) \to (E/B)
$$
by [[pullback]]. As described at [[dependent product]] this functor has both a [[left adjoint]] $\coprod_k : E/B \to E/A$ as well as a [[right adjoint]] $\prod_k : E/A \to E/B$.  Therefore
$$
  (\Pi_k, k^*) : E/B \leftrightarrow E/B
$$

is a geometric morphism.


# Geometric morphisms of sheaf topoi #

For $X$ a [[topological space]], write $Sh(X) := Sh(Op(X))$ as usual for the [[topos]] given by the [[category of sheaves]] on the [[category of open subsets]] $Op(X)$ with the standard [[coverage]]

+-- {: .un_lemma}
###### Lemma

For every continuous map $f : X \to Y$ of [[Hausdorff space|Hausdorff]] [[topological spaces]] with the induced [[functor]] $f^{-1} : Op(Y) \to Op(X)$ of [[sites]], the [[direct image]]

$$
  f_* : Sh(X) \to Sh(Y)
$$

and the [[inverse image]]

$$
  f^* : Sh(Y) \to Sh(X)
$$

constitute a geometric morphism 

$$
   f : Sh(X) \to Sh(Y)
$$

(denoted by the same symbol, by convenient abuse of notation). 

This map $Hom_{Top}(X,Y) \to GeomMor(Sh(X),Sh(Y))$ is an bijection of sets.

=--

+-- {: .proof}
###### Proof

That the induced pair $(f^*, f_*)$ forms a geometric morphism is (or should eventually be) discussed at [[inverse image]].

We now show that the map is a bijection, i.e. that every geometric morphism of of sheaf topoi arises this way from a continuous function. We follow page 348 of

* MacLane-Moerdijk, [[Sheaves in Geometry and Logic]].

One reconstructs the continuous map $f : X \to Y$ from a geometric morphism $f : Sh(X) \to Sh(Y)$ as follows.

Write ${*} = Y \in Sh(Y)$ for the sheaf on $Op(Y)$ constant on the singleton set, the [[terminal object]] in $Sh(Y)$.

Notice that since the [[inverse image]] $f^*$ preserves finite [[limits]], every [[subobject]] $U_Y \hookrightarrow {*}$ is taken by $f^*$ to a subobject $U_X \hookrightarrow X$, obtained by applying $f^*$ to the [[pullback]] diagram 

$$
  \array{
    U_Y &\to& {*} = Y
    \\
    \downarrow && \downarrow
    \\
    {*} = Y &\to& \Omega
  }
$$

that characterizes the subobject $U_Y$ in the [[topos]].

But, as the notation already suggests, the subobjects of $X,Y$ are just the open sets, i.e. the representable sheaves.

This yields a _function_ $f^* : Obj(Op(Y)) \to Obj(Op(X))$ from open subsets to open subsets of which we know by assumption that it preserves finite limits and arbitrary colimits, i.e. finite intersections and arbitrary unions of open sets.

Using this define a function $\bar f : X \to Y$ of the sets underlying the topological spaces $X$ and $Y$ by setting

$$
  (\bar f(x) = y)
  \Leftrightarrow
  \forall V \ni y: x \in f^*(V)  
  \,.
$$

This yields a well defined function for the following reasons:

* there is at most one $y$ satisfying this equation: if $y_1 \neq y_2$ both satisfy it, there are, by assumption of $Y$ being [[Hausdorff space|Hausdorff]], neighbourhoods $V_1 \ni y_1$ and $V_2 \ni y_2$ such that (using that $f^*$ preserves limits hence intersections) $f^*(V_1) \cap f^*(V_2) = f^*(V_1 \cap V_2) = \emptyset$, which contradicts the assumption.

* there is at least one $y$ satisfying this equation: again by contradiction: if there were none then every $y \in Y$ has a neighbourhood $V_y$ with $x \not\in f^*(V_y)$, so that similarly to above we conclude with $x \not\in \cup_{y \in Y} f^*(V_y) = f^*(\cup_y V_y) = f^*(Y) = X$ again a contradiction.

So our function $\bar f : X \to Y$ is well defined and satisfies $\bar f^{-1}(U_Y) = f^*(U_Y)$ for every open set $U_Y \in Obj(Op(Y))$. In particular it is therefore a continuous map.

It remains to check that this map reproduces the geometric morphism that we started with. For that we compute its [[direct image]] on any sheaf $A \in Sh(X)$ as

$$
  \begin{aligned}
    \bar f_*(A) : U_Y &\mapsto A(\bar f^{-1}(U_Y))
    \\
    & \simeq Hom_{Sh(X)}(\bar f^{-1}(U_Y),A)
    \\
    & = Hom_{Sh(X)}(f^* V, E)
    \\
    & \simeq Hom_{Sh(X)}(V, f_* E)
    \\
    & \simeq (f_* A)(U_Y)
  \end{aligned}
$$

=--

+-- {: .un_cor}
###### Corollary

The points $x \in X$ of the topological space $X$ are in canonical bijection with the points of $Sh(X)$ in the sense of [[point of a topos]].

=--

#References#

Geometric morphisms are the topic of section VII of

* Saunders MacLane and Ieke Moerdijk, [[Sheaves in Geometry and Logic]].

Embeddings and surjections are discussed in section VII.4.

[[!redirects geometric morphisms]]