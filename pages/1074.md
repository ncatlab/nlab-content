#Idea#

A category with _saturated multiplicative system_
is a special kind of [[homotopical category]].

A _saturated (left/right) multiplicative system_ 
on a [[category]] $C$ 
is a [[subcategory]] $S \subset C$ of 
[[weak equivalence|homotopical category]]s in $C$ that satisfies two
extra conditions which allows a convenient 
construction of the corresponding
[[homotopy category]] in terms of 
[[generalized morphism]]s. 

The saturated multiplicative system is a structure in between
a bare system of weak equivalences and the structure of a
[[model category]] (it is in fact considerably less structure
than present on a model category).

A non-saturated left (right) multiplicative system behaves
roughly like a collection of acyclic fibrations (acyclic cofibrations).
(See the examples below.)

#Definition#

A **left multiplicative system** in a [[category]] $C$ is
a [[subcategory]] $S \subset C$ such that

* every [[isomorphism]] in $C$ belongs to $S$, i.e.
$ Core(C) \subset S \subset C$;

* for every [[pullback]] diagram
$
  \array{
    && Y'
    \\
    && \downarrow^{t \in S}
    \\
    X &\stackrel{f}{\to}& Y
  }
$
with $t \in S$ there is a [[cone]]
$
  \array{
    X' &\stackrel{\exists}{\to}& Y'
    \\
    \downarrow^{\exists s \in S}
    && \downarrow^{t \in S}
    \\
    X &\stackrel{f}{\to}& Y
  }
$
with $s \in S$;

* for $\array{
  X \stackrel{\stackrel{f}{\to}}{\stackrel{g}{\to}}
  Y
}$
any two [[parallel morphisms]] and $Y \stackrel{t \in S}{\to} Z$
such that $t \circ f  = t \circ g$ there exists
$W \stackrel{s \in S}{\to} X$ such that $f \circ s = g \circ s$.


A **right multiplicative system** in $C$ is a left multiplicative system
in the [[opposite category]] $C^{op}$.

A **multiplicative system** in $C$ is a system that is both left
and right multiplicative.

A **saturated left multiplicative system** is a left multiplicative
system such that for all triples
$$
  X \stackrel{f}{\to}
  Y \stackrel{g}{\to}
  Z \stackrel{h}{\to}
  W
$$
of morphisms in $C$ we have that
$g \circ f \in S$ and $h \circ g \in S$ implies that $h \in S$.

#Homotopy category#

##Construction of the homotopy category##

The [[hom-set]]s in the [[homotopy category]] of a category $C$ with
respect to a left multiplicative system $S$ (i.e. the universal solution
to finding $Q : C \to C_S$ such that $Q(S) \subset Core(C_S)$) is
given by forming the colimit over maps out of an $S$-replacement over
the source object:
$$
  Hom_{C_s}(X,Y) = co\lim_{X' \stackrel{p \in S}{\to}X} Hom_C(X',Y)
  \,.
$$

For $S$ a right multiplicative system it is given instead by
the colimit over maps into an $S$-replacement under the target object
$$
  Hom_{C_s}(X,Y) = co\lim_{Y \stackrel{i \in S}{\to} Y'} Hom_C(X,Y')
  \,.
$$

For $S$ both a left and right multiplicative system both 
prescriptions coincide and are equivalent to taking a
colimit over replacements of both objects:
$$
  \begin{aligned}
    Hom_{C_s}(X,Y) &= 
      co\lim_{X' \stackrel{p \in S}{\to}X} Hom_C(X',Y)
    \\
      &= co\lim_{Y \stackrel{i \in S}{\to} Y'} Hom_C(X,Y')
    \\
      &= 
      co\lim_{X' \stackrel{p \in S}{\to}X, 
        Y \stackrel{i \in S}{\to} Y'} Hom_C(X',Y')
  \end{aligned}
  \,.
$$

## Properties of the homotopy category ##

Let $S$ be a right multiplicative system on $C$. Then

* The functor $Q : C \to C_S$ is right [[exact functor|exaxt]].

* The functor $Q : C \to C_S$ commutes with finite [[colimit]]s
and in particular with [[cokernel]]s as far as they exist in $C$.


So in particular $C_S$ admits all finite colimits if $C$ does.

##Derived functors ##

Recall from the discussion at [[derived functor]] that
with respect to the inclusion $Q : C \to C_S$ of 
$C$ into its homotopy category 

* [[generalized the|the]] **right derived functor** of any functor $F : C \to A$ is,
if it exists, [[generalized the|the]] left [[Kan extension]] $ R_S F := Lan_Q F$;

* if $R_S F$ exists it is called [[generalized the|the] 
**universal right derived functor** if for any functor $K : A \to A'$
we have $R_S (K \circ F) \simeq K \circ (R_S F)$ 
(in particular the left side exists).

and similarly

* [[generalized the|the]] **left derived functor** of any functor $F : C \to A$ is,
if it exists, [[generalized the|the]] right [[Kan extension]] $ L_S F := ran_Q F$.

Let now $S$ be a right multiplicative system on $C$ and $F : C \to A$
any functor.

**Proposition**

If there exists a full [[subcategory]] $\iota : I \hookrightarrow C$
such that

* every object $X$ of $C$ is connected by a morphism 
$X \stackrel{s \in S}{\to} X'$ to an object $X' \in I$;

* restricted to $I$ the functor $F$ is [[homotopical functor|homotopical]]
(sends all morphisms in $S|_I$ to isomorphisms);

then the right derived functor $R_S F : C_S \to A$ 

* exists;
* is universal;
* and its restriction to $I$ is isomorphic to the restriction of $F$ to $I$.

Explicitly, $R_S F$ is given by
$$
  R_S F \simeq R_{S} F|_I \circ \iota_S^{-1}
  \,,
$$
where $\iota_S : I_S \stackrel{\simeq}{\to} C_S$ is an equivalence of
categories and $\iota_S^{-1}$ a weak inverse.


**Proposition**

Assume that $A$ admits all small [[filtered category|filtered]]
[[colimit]]s and that for all $X \in C$ the category 
$$
  S^X =
  \left\{
    \array{
       && X
       \\ 
       & {}^{\in S}\swarrow && \searrow^{\in S}
       \\
       X' &&\to &6 X''
    }
  \right\}
$$
is [[cofinally small]]. Then

* $C_S$ is [[locally small]];

* for every functor $F : C \to A$ the right derived functor
exists and is given by
$
  R_S F(X)
  =
  co\lim_{X \stackrel{s \in S}{\to} X'} F(X')
$.



#Remarks#

* Some authors use the terms "left" and "right" multiplicative 
opposite to the convention here.

#Examples#

* For $C$ a [[category of fibrant objects]] and $\pi C$ its
category of morphisms modulo [[homotopy]], the collection of 
acyclic fibrations in $\pi C$ is a right multiplicative
system. 

* Given a [[null system]] $N$ in a [[triangulated category]] $C$
the collection of morphisms $f : X \to Y$ in $C$ such that
there is a distinguished triangle $X \to Y \to (Z \in N)$
is a multiplicative system in $C$. 

* For $S$ a [[site]], the collection of [[local epimorphism]]s
in $C = [S^{op},Set]$ with respect to the given [[Grothendieck topology]]
on $S$ is a left factorization system.

#References#

Section 7 of

* Kashiwara-Schapira, [[Categories and Sheaves]]


