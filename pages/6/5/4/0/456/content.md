
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

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



## Definition

If $E$ and $F$ are [[topos|toposes]], a **geometric morphism** $f:E\to F$ consists of an pair of [[adjoint functors]] $(f^*,f_*)$
$$
  f_* : E \to F
$$
$$
  f^* : F \to E
  \,,
$$

such that the left adjoint $f^*:F \to E$ preserves finite [[limits]].

If moreover the [[inverse image]] $f^*$ has also a [[left adjoint]] $f_! : F \to E$, then $f$ is an [[essential geometric morphism]].

**Remark.** Since [[Grothendieck topos|Grothendieck toposes]] satisfy the (dual) hypotheses of Freyd's special [[adjoint functor theorem]], any functor $f^*$ between Grothendieck toposes which preserves all small colimits must have a right adjoint.  Therefore, a geometric morphism between Grothendieck toposes could equivalently be defined as a functor preserving finite limits and all small colimits.


## Special classes of geometric morphisms

There are vrious extra properties of a geometric moprhisms that are relevant. 

* [[direct image]]/[[inverse image]]

* [[global section|global sections]]

* [[geometric embedding]]

* [[locally connected geometric morphism]]

  * [[essential geometric morphism]]

  * [[connected geometric morphism]]

* [[local geometric morphism]]

* [[bounded geometric morphism]]

* [[base change]]

* [[etale geometric morphism]]

* [[localic geometric morphism]]

* [[hyperconnected geometric morphism]]

* [[cohesive topos|cohesive morphism]]

The following subsections describe some more.

### Surjections and embeddings

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


### Global sections and constant sheaves

For every topos $E$, there is a geometric morphism

$$
  \Gamma : E  \stackrel{\leftarrow}{\to} Set : const
$$

called the [[global section]]s functor. It is given by the [[hom-set]] out of the [[terminal object]]

$$
  \Gamma(-) = Hom_E({*}, -)
$$

and hence assigns to each object $A\in E$ its set of [[global element]]s $\Gamma(A) = Hom_E(*,A)$. If $E$ is a [[Grothendieck topos]] then one thinks of $A$ as a [[sheaf]] and of $\Gamma(A)$ as its set of **global sections**.

The [[left adjoint]] $const : Set \to E$ of the global section functor is the canonical [[Set]]-[[copower|tensoring]] functor

$$
  \otimes : Set \times E \to E
$$

applied to the [[terminal object]]

$$
  const = (-)\otimes {*} : Set \to E
$$

which sends a set $S$ to the [[coproduct]] of $|S|$ copies of the terminal object

$$
  S \otimes {*} = \coprod_{s \in S} {*}
  \,.
$$

This is called the **constant object** of $E$ on the set $S$. Notably when $E$ is a [[Grothendieck topos|sheaf topos]] this is the **[[constant sheaf]]** on $S$. 

The [[left adjoint]]ness is just the defining property of the [[copower|tensoring]]

$$
  Hom_E(const S, A) \simeq Hom_E(S \otimes {*},A)
  \simeq
  Hom_{Set}(S, Hom_E(*,A))
  \,.
$$

This left adjoint preserves [[product]]s, using that colimits in a  topos are stable by base change (see [[commutativity of limits and colimits]])

$$
   \left( \coprod_{s_1 \in S_1} *\right)
   \times
   \left( \coprod_{s_2 \in S_2} *\right)
   =
   \coprod_{s_1 \in S_1}  \left(* \times \left( \coprod_{s_2 \in S_2} *\right)\right)
   =
   \coprod_{s_1 \in S_1}  \left( \coprod_{s_2 \in S_2} *\right)
   =
   \coprod_{s_1 \in S_1} \coprod_{s_2 \in S_2} *
   =
   \coprod_{s \in S_1 \times S_2} *
$$

and it preserves [[equalizer]]s and therefore [[limit]]s. So it is left exact and we do have a geometric morphism.



### Point of a topos

For $E$ a topos, a geometric morphism 

$$
  x : Set \to E
$$

is called a [[point of a topos]].


### Change-of-base

For $E$ any [[topos]] and $k : B \to A$ any morphism in $E$ there is the [[base change|change-of-base]] functor of [[over category|over categories]] 
$$
  k^* : (E/A) \to (E/B)
$$
by [[pullback]]. As described at [[dependent product]] this functor has both a [[left adjoint]] $\coprod_k : E/B \to E/A$ as well as a [[right adjoint]] $\prod_k : E/A \to E/B$.  Therefore
$$
  (\Pi_k, k^*) : E/B \leftrightarrow E/B
$$

is a geometric morphism. Hence $(\Pi_k \dashv k^* \dashv \coprod_k)$ is an [[essential geometric morphism]].

### Sheafification

A [[category of sheaves]] is a [[geometric embedding]] into a presheaf topos

$$
  Sh(C) \hookrightarrow PSh(C)
  \,.
$$


### Geometric morphisms of sheaf topoi 
{#sheaftopoi}

Geometric morphisms between [[localic topoi]] are equivalent to [[continuous maps]] of [[locales]], which in turn are equivalent to continuous maps of [[topological spaces]] if you restrict to [[sober spaces]].

Unrolling this: For $X$ a [[topological space]], write $Sh(X) := Sh(Op(X))$ as usual for the [[topos]] given by the [[category of sheaves]] on the [[category of open subsets]] $Op(X)$ with the standard [[coverage]]

+-- {: .un_lemma}
###### Lemma

For every continuous map $f : X \to Y$ of [[sober space|sober]] [[topological spaces]] with the induced [[functor]] $f^{-1} : Op(Y) \to Op(X)$ of [[sites]], the [[direct image]]

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

We now show that every geometric morphism of sheaf toposes arises this way from a continuous function, at least up to isomorphism.  (In fact, more is true: the category of geometric morphisms $Sh(X)\to Sh(Y)$ is equivalent to the poset of continuous functons $X\to Y$ with the [[specialization ordering]].)  We follow page 348 of

* MacLane-Moerdijk, _[[Sheaves in Geometry and Logic]]_ .

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

This yields a _function_ $f^* : Obj(Op(Y)) \to Obj(Op(X))$ from open subsets to open subsets.  By assumption, this preserves finite limits and arbitrary colimits, i.e. finite intersections and arbitrary unions of open sets.  In other words, it is a [[frame|frame homomorphism]], and thus can be regarded as a morphism $X\to Y$ of [[locales]].

We can now use this to define a function $\bar f : X \to Y$ of the sets underlying the topological spaces $X$ and $Y$ by setting

$$
  (\bar f(x) = y)
  \Leftrightarrow
  \forall V \ni y: x \in f^*(V)  
  \,.
$$

This yields a well defined function for the following reasons (which for the moment we spell out in the case where $Y$ is [[Hausdorff space|Hausdorff]], although the result should hold ---and furthermore, hold [[constructive mathematics|constructively]]--- whenever $Y$ is sober):

* there is at most one $y$ satisfying this equation: if $y_1 \neq y_2$ both satisfy it, there are, by assumption of $Y$ being [[Hausdorff space|Hausdorff]], neighbourhoods $V_1 \ni y_1$ and $V_2 \ni y_2$ such that (using that $f^*$ preserves limits hence intersections) $f^*(V_1) \cap f^*(V_2) = f^*(V_1 \cap V_2) = \emptyset$, which contradicts the assumption.

* there is at least one $y$ satisfying this equation: again by contradiction: if there were none then every $y \in Y$ has a neighbourhood $V_y$ with $x \not\in f^*(V_y)$, so that similarly to above we conclude with $x \not\in \cup_{y \in Y} f^*(V_y) = f^*(\cup_y V_y) = f^*(Y) = X$ again a contradiction.

+-- {: .query}
Am I right that what we are really need of our space here is not necessarily that it be Hausdorff but simply that it be [[sober space|sober]]?  (Then the nonconstructive aspects of the argument ---which is what made me look at this--- come in only because the theorem that a Hausdorff space must be sober is not constructively valid.)  ---Toby

[[Mike Shulman]]: Yes, that's exactly right.  All the complication defining $\bar f$ above is just an unrolled way of saying that geometric morphisms between [[locale|localic]] topoi are equivalent to continuous maps of locales, which are equivalent to continuous functions if you have sober spaces.  I think that should be clarified.

_Toby_:  OK, I added a paragraph at the beginning of the example to clarify this.  I still need to rewrite the argument immediately above to apply to sober spaces.  (Everything else seems to go through exactly the same.)
=--

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


## References

Geometric morphisms are the topic of section VII of

* [[Saunders MacLane]] and [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ .

Embeddings and surjections are discussed in section VII.4.

Geometric morphisms are defined in section A4 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

The special classes of geometric morphisms are discussed in section C3.

[[!redirects geometric morphisms]]