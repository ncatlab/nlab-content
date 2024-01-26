
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

* table of contents
{: toc}


## Definition

Given a [[category]] $C$ and an [[object]] $c \in C$, the __under category__ (also called __coslice category__) $c \downarrow C$ (alternative notations include $C^{c/}$ and $c/C$ and sometimes, confusingly, $c\backslash C$) is the category whose

* objects are morphisms in $C$ starting at $c$; $c \to d$

* morphisms are commuting triangles 
$
 \array{
    && c
    \\
    & \swarrow && \searrow
    \\
    d_1 &&\to && d_2
  }
  \,.
$

The under category $c\downarrow C$ is a kind of [[comma category]]; it is the strict pullback 

$$
 \array{
  c \big\downarrow C
  &\to&
  pt
  \\
  \big\downarrow
  &&
  \big\downarrow^{\mathrlap{pt \mapsto c}}
  \\
  [I,C]
  &\stackrel{d_0}{\to}&
  C
 } 
$$
in [[Cat]], where

* $I$ is the [[interval category]] $\{0 \to 1\}$;

* $[I,C]$ is the [[closed monoidal category|internal hom]] in [[Cat]], which here is the [[arrow category]] $Arr(C)$;

* the functor $d_0$ is evaluation at the left end of the interval;

* $pt$, the point, is the terminal category, the 0th [[oriental]], the 0-globe;

* the right vertical morphism maps the single object of the point to the object $c$.

The left vertical morphism $c \downarrow C \to C$ is the forgetful morphism which forgets the tip of the triangles mentioned above.

The [[duality|dual]] notion is an [[over category]].


## Examples

\begin{example}
If $0$ is an [[initial object]] in $\mathbf{C}$, then $0\downarrow\mathbf{C}$ is isomorphic to $\mathbf{C}$.
\end{example}

\begin{example}\label{PointedObjects}
**([[pointed objects]])** \linebreak

If $C$ has a [[terminal object]] $\ast \,\in\, C$, then the coslice $C^{\ast/}$ is known as the category of *[[pointed objects]]* in $C$. For instance:

* the category of [[pointed sets]], is the coslice of [[Set]] under the [[singleton]] set,

* the category of [[pointed topological spaces]] is the coslice of [[Top]] under the [[point space]],

* the category of [[pointed simplicial sets]] is the coslice of [[sSet]] under the [[0-simplex]].


If $C$ is a [[monoidal category]] with [[tensor unit]] $I \,\in\, C$, then the coslice $I \downarrow C$ is also known as the category of *[[pointed objects in a monoidal category]]*. For instance:

* the category of [[pointed abelian groups]] is the coslice of [[Ab]] under the additive group of [[integers]],

* the category of [[pointed modules]] is the coslice of [[Mod]] under the additive module of the [[ground ring]]

* the category of [[bi-pointed object|bi-pointed sets]] is the coslice of $Set_*$, the [[category of pointed sets]], under the [[boolean domain]]. 

* the category of [[pointed endofunctors]] is a coslice of and [[endofunctor|endo]]-[[functor category]] under the [[identity functor]].

Generally, for any $c \in C$ one may think of the $c$-coslice category as the category of "$c$-pointed objects".
\end{example}

\begin{example}
The category of [[commutative algebras]] over a [[field]] $F$ is the coslice under $F$ of the category [[CRing]] of [[commutative rings]].
\end{example}



## Properties

### Limits and colimits
 {#LimitsAndColimits}


+-- {: .num_prop}
###### Proposition

If $C$ is a [[category]] with all [[limits]], then a  [[limit]] in any of its [[under categories]] $t/C$ is computed as a limit in the underlying category $C$.

In detail: 

Let $F \colon D \to t/C$ be any [[functor]]. 

Then, the [[limit]] over $p \circ F$ in $C$ is the image under the evident projection $p \colon t/C \to C$ of the limit over $F$ itself:

$$
  p(\lim F)  \simeq \lim (p F)
$$

and $\lim F$ is uniquely characterized by $\lim (p F)$.

=--
 
+-- {: .proof}
###### Proof

Over a morphism $\gamma : d \to d'$ in $D$ the limiting cone over $p F$  (which exists by assumption) looks like

$$
  \array{
    && \lim p F
    \\
    & \swarrow && \searrow
    \\
    p F(d) &&\stackrel{p F(\gamma)}{\to}&& p F(d') 
  }
$$


By the universal property of the limit this has a unique
lift to a cone in the [[under category]] $t/C$ over $F$:

$$
  \array{
    && t 
    \\
    & \swarrow &\downarrow & \searrow
    \\
    && \lim p F
    \\
    \downarrow & \swarrow && \searrow & \downarrow
    \\
    p F(d) &&\stackrel{p F(\gamma)}{\to}&& p F(d') 
  }
$$


It therefore remains to show that this is indeed a limiting cone over $F$. Again, this is immediate from the universal property of the limit in $C$. For let $t \to Q$ be another cone over $F$ in $t/C$, then $Q$ is another cone over $p F$ in $C$ and we get in $C$ a universal morphism $Q \to \lim p F$

$$
  \array{
    && t
    \\
    & \swarrow & \downarrow & \searrow
    \\
    && Q
    \\
    \downarrow & \swarrow &\downarrow & \searrow & \downarrow
    \\
    && \lim p F
    \\
    \downarrow & \swarrow && \searrow & \downarrow
    \\
    p F(d) &&\stackrel{p F(\gamma)}{\to}&& p F(d') 
  }
$$


A glance at the diagram above shows that
the composite $t \to Q \to \lim p F$ constitutes a morphism
of cones in $C$ into the limiting cone over $p F$. Hence it must equal our morphism $t \to \lim p F$, by the universal property of $\lim p F$, and hence the above diagram does commute as indicated.

This shows that the morphism $Q \to \lim p F$
which was the unique one giving a cone morphism on $C$ does lift to a
cone morphism in $t/C$, which is then necessarily unique, too.  This demonstrates the required universal property of $t \to \lim p F$ and 
thus identifies it with $\lim F$.


=--

+-- {: .num_remark}
###### Remark

One often says "$p$ [[reflected limit|reflects limits]]" to express the conclusion of this proposition. A conceptual way to consider this result is by appeal to a more general one: if $U: A \to C$ is [[monadic functor|monadic]] (i.e., has a left adjoint $F$ such that the canonical comparison functor $A \to (U F)-Alg$ is an equivalence), then $U$ both reflects and preserves limits. In the present case, the projection $p: A = t/C \to C$ is monadic, is essentially the category of algebras for the monad $T(-) = t + (-)$, at least if $C$ admits binary coproducts. (Added later: the proof is even simpler: if $U: A \to C$ is the underlying functor for the category of algebras of an _endofunctor_ on $C$ (as opposed to algebras of a monad), then $U$ reflects and preserves limits; then apply this to the endofunctor $T$ above.) 

=--


## Related concepts

* [[over-category]] 

  * [[slice category]] 

  * **under category** 

  * [[over topos]]


* [[over (∞,1)-category]],

  * [[model structure on an over category]] 

  * [[over-(∞,1)-topos]]

## References

Discussion in the generality of [[(infinity,1)-categories|$(\infty,1)$-categories]]:

* [[Jacob Lurie]], Rem. 1.2.5.9 in: *[[Higher Topos Theory]]*, Annals of Mathematics Studies **170**, Princeton University Press (2009) &lbrack;[pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf)&rbrack;



[[!redirects under category]]
[[!redirects under-category]]
[[!redirects undercategory]]
[[!redirects coslice category]]
[[!redirects co-slice category]]
[[!redirects under categories]]
[[!redirects under-categories]]
[[!redirects undercategories]]
[[!redirects coslice categories]]
[[!redirects co-slice categories]]
[[!redirects co-slice]]