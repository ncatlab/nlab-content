
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

The **slice category** or **over category** $\mathbf{C}/c$ of a [[category]] $\mathbf{C}$ over an object $c \in \mathbf{C}$ has 

* objects that are all arrows $f \in \mathbf{C}$ such that $cod(f) = c$, and

* morphisms $g: X \to X' \in \mathbf{C}$ from $f:X \to c$ to $f': X' \to c$ such that $f' \circ g = f$.

$$
  C/c
  =
  \left\lbrace
    \array{
       X &&\stackrel{g}{\to}&& X'
       \\
       & {}_f \searrow && \swarrow_{f'}
       \\   
       && c
    }
  \right\rbrace
$$


The slice category is a special case of a [[comma category]].

There is a [[forgetful functor]] $U_c: \mathbf{C}/c \to \mathbf{C}$ which maps an object $f:X \to c$ to its domain $X$ and a morphism $g: X \to X' \in \mathbf{C}/c$ (from $f:X \to c$ to $f': X' \to c$ such that $f' \circ g = f$) to the morphism $g: X \to X'$.

The [[duality|dual]] notion is an [[under category]].


## Examples 

* If $\mathbf{C} = \mathbf{P}$ is a [[partial order|poset]] and $p \in \mathbf{P}$, then the slice category $\mathbf{P}/p$ is the [[down set]] $\downarrow (p)$ of elements $q \in \mathbf{P}$ with $q \leq p$. 

* If $1$ is a [[terminal object]] in $\mathbf{C}$, then $\mathbf{C}/1$ is isomorphic to $\mathbf{C}$.

## Properties

### Relation to codomain fibration

The assignment of overcategories $C/c$ to objects $c \in C$ extends to a [[functor]]

$$
  C/(-) : C \to Cat
  \,,
$$

Under the [[Grothendieck construction]] this functor corresponds the the [[codomain fibration]]

$$
  cod : [I,C] \to C
$$

from the [[arrow category]] of $C$.  (Note that unless $C$ has [[pullbacks]], this functor is not actually a [[Grothendieck fibration|fibration]], though it is always an opfibration.)

### Adjunctions on overcategories
 {#Adjunction}

+-- {: .num_prop}
###### Proposition

Let

$$
  (L \dashv R) : D \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
     C
$$

be a pair of [[adjoint functor]]s, where the category $C$ has all [[pullback]]s. 

Then for every object $X \in C$ there is induced a pair of adjoint functors between the slice categories

$$
  (L/X \dashv R/X) 
   : D/(L X) \stackrel{\overset{L/X}{\leftarrow}}{\underset{R/X}{\to}}
     C/X
$$

where

* $L/X$ is the evident induced functor;

* $R/X$ is the composite

  $$
    R/X : D/{L X} \stackrel{R}{\to} C/{(R L X)} \stackrel{i_{X}^*}{\to}
     C/X
  $$

  of the evident functor induced by $R$ with the [[pullback]] along the $(L \dashv R)$-[[unit of an adjunction|unit]] at $X$.

=--




### Presheaves on over-categories and over-categories of presheaves {#RelWithPresheaves}

Let $C$ be a [[category]], $c$ an [[object]] of $C$ and let $C/c$ be the [[over category]] of $C$ over $c$. Write
$PSh(C/c) = [(C/c)^{op}, Set]$ for the [[category of presheaves]] on $C/c$ and write
$PSh(C)/Y(y)$ for the [[over category]] of [[presheaf|presheaves]] on $C$ over the presheaf $Y(c)$, where $Y : C \to PSh(c)$ is the [[Yoneda embedding]]. 

+-- {: .num_prop}
###### Proposition


There is an [[equivalence]] of categories

$$
  e : PSh(C/c) \stackrel{\simeq}{\to} PSh(C)/Y(c)
  \,.
$$

=--


+-- {: .proof}
###### Proof

The functor $e$ takes $F \in PSh(C/c)$ to the presheaf
$F' : d \mapsto \sqcup_{f \in C(d,c)} F(f)$ which is equipped with the natural transformation $\eta : F' \to Y(c)$ with component map $\eta_d \sqcup_{f \in C(d,c)} F(f) \to C(d,c)$.

A weak inverse of $e$ is given by the functor 
$$
  \bar e : PSh(C)/Y(c) \to PSh(C/c)
$$
which sends
$
  \eta : F' \to Y(C))
$ to $F \in PSh(C/c)$ given by
$$
  F : (f : d \to c) \mapsto F'(d)|_c
  \,,
$$
where $F'(d)|_c$ is the [[pullback]]
$$
  \array{
     F'(d)|_c &\to& F'(d)
     \\
     \downarrow && \downarrow^{\eta_d}
     \\
     pt &\stackrel{f}{\to}& C(d,c)
  }
  \,.
$$ 

=--


+-- {: .num_example}
###### Example

Suppose the presheaf $F \in PSh(C/c)$ does not actually depend on the morphsims to $C$, i.e. suppose that it factors through the forgetful functor from the [[over category]] to $C$:
$$
  F : (C/c)^{op} \to C^{op} \to Set
  \,.
$$

Then
$
  F'(d) = \sqcup_{f \in C(d,c)} F(f)
  = \sqcup_{f \in C(d,c)} F(d)
  \simeq
  C(d,c) \times F(d) 
$
and hence $F ' = Y(c) \times F$ with respect to the [[closed monoidal structure on presheaves]].

=--

See also [[functors and comma categories]].

For the analog statement in [[(∞,1)-category]] theory see
 <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-category+of+(infinity%2C1)-presheaves#interaction_with_forming_overcategories_19">(∞,1)-category of (∞,1)-presheaves -- Interaction with overcategories</a>

at [[(∞,1)-category of (∞,1)-presheaves]].


### Limits and colimits
 {#LimitsAndColimits}

+-- {: .num_prop}
###### Proposition

A  [[limit]] in an [[under category]] is computed as a limit in the underlying category.

Precisely: let $C$ be a [[category]], $t \in C$ an [[object]], and $t/C$ the corresponding [[under category]], and $p : t/C \to C$ the obvious projection.

Let $F : D \to t/C$ be any [[functor]]. Then, if it exists, the [[limit]] over $p \circ F$ in $C$ is the image under $p$ of the limit over $F$:

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

+-- {: .num_prop }
###### Proposition

For $\mathcal{C}$ a [[category]], $X \;\colon\; \mathcal{D} \longrightarrow \mathcal{C}$ a [[diagram]], $\mathcal{C}_{/X}$ the [[comma category]] (the over-category if $\mathcal{D}$ is the point) and $F \;\colon\; K \to \mathcal{C}_{/X}$ a [[diagram]] in the [[comma category]], then the [[limit]] $\underset{\leftarrow}{\lim} F$ in $\mathcal{C}_{/X}$ coincides with the limit $\underset{\leftarrow}{\lim} F/X$ in $\mathcal{C}$. 
 
=--

For a proof see at [[(∞,1)-limit]]  _[here](limit+in+a+quasi-category#InOvercategories)_.

### Initial and terminal objects

As a special case of the above discussion of limits and colimits in a 
slice $\mathcal{C}_{/X}$ we obtain the following statement, which of 
course is also immediately checked explicitly.

+-- {: .num_cor }
###### Corollary

* If $\mathcal{C}$ has an initial object $\emptyset$, then $\mathcal{C}_{/X}$ has an [[initial object]], given by $\langle \emptyset \to X\rangle$.

* The [[terminal object]] of $\mathcal{C}_{/X}$ is $\mathrm{id}_X$.

=--




## Related concepts

* **over-category** 

  * [[slice category]] 

  * [[under category]] 

  * [[over topos]]

* [[slice 2-category]]

* [[over (∞,1)-category]],

  * [[model structure on an over category]] 

  * [[over-(∞,1)-topos]]

[[!redirects over category]]
[[!redirects over categories]]
[[!redirects over-category]]
[[!redirects over-categories]]
[[!redirects overcategories]]
[[!redirects slice category]]
[[!redirects slice categories]]
