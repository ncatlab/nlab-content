
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A locally constant [[sheaf]] $A$ over a [[topological space]] is a sheaf of [[section]]s of a [[covering space]] of $X$: there is a [[cover]] of $X$ by open subsets $\{U_i\}$ such that the [[inverse image|restrictions]] $A|_{U_i}$ are [[constant sheaf|constant sheaves]].

More elegantly said: locally constant sheaves are the sections of [[constant stack]]s:

Let $C = Core(FinSet)\in $ [[Grpd]] be the [[core]] of the [[category]] [[FinSet]] of finite set, let $const_C : Op(X)^{op} \to Grpd$ the presheaf constant on $C$, i.e. the [[functor]] on the [[opposite category]] of the [[category of open subsets]] of $X$ that sends everything to (the identity on) $C$. Then the [[constant stack]] on $C$ is the [[stackification]] $\bar const_C : Op(X)^{op} \to Grpd$.

Write then $X$ for the space $X$ regarded as a sheaf or trivial [[covering space]] over itself, i.e. the [[terminal object]] $X$ in sheaves and hence in stacks over $X$. Then by definition of stackification morphisms

$$
  X \to \bar const_C
$$

are represented by

* an open cover $\{U_i\}$ of $X$;

* over each $U_i$ a choice $F_i \in C$ of object in $C$, hence a finite set in $C$;

* over each double overlap $U_{i j} = U_i \cap U_j$ an morphism $g_{i j} : F_i|_{I_{i j}} \stackrel{\simeq}{\to} F_j|_{U_{i j}}$, hence a bijection of finite sets;

* such that on triple overlaps we have $g_{i k}|_{U_{i j k}}= g_{j k}|_{U_{i j k}}\circ g_{i j}|_{U_{i j k}}$.

Such data clearly is the local data for a [[covering space]] over $X$ with typical fiber any of the $F_i$.

## Applications

Locally constant sheaves are sheaves of sections of [[covering space]]s.

When used as coefficient objects in [[cohomology]] they are also called [[local system]]s.

The [[action]] of the [[fundamental groupoid]] $\Pi_1(X)$ on the fibers of a local system give rise to the notion of [[monodromy]].
This may be used to define [[homotopy group (of an infinity-stack)|homotopy groups of]] general objects in a [[topos]].

## Pattern


* A [[locally constant function]] is a section of a [[constant sheaf]];

* a **locally constant sheaf** is a section of a [[constant stack]];

* a [[locally constant stack]] is a section of (... and so on...)

* a [[locally constant ∞-stack]] is a section of a [[constant ∞-stack]].

A locally constant sheaf / $\infty$-stack is also called a [[local system]].




















[[!redirects locally constant sheaves]]