
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In any [[category]], a **cospan** is a diagram like this:
$$
  \array{
     && a &&&& b
      \\
      & 
      && {}_{f}\searrow
       &
       & \swarrow_g
      && 
     \\     
     &&&&
     c
     &&&&
  }
$$


A cospan in the category $C$ is the same as a [[span]] in the [[opposite category]] $C^{op}$.  So, all general facts about cospans in $C$ are general facts about spans in $C^{op}$, and the reader may turn to the entry on [[span|spans]] to learn more.

A cospan that admits a [[cone]] is called a [[quadrable cospan]].

### In type theoretic approaches to synthetic $(\infty,1)$-category theory

In [[simplicial type theory]], [[parametric type theory|binary parametric]] [[observational type theory]], and other type theoretic approaches to synthetic $(\infty,1)$-category theory, a cospan in a synthetic $(\infty,1)$-category $C$ can be defined as the following:

* a [[record]] consisting of objects (elements of [[types]]) $x:C$, $y:C$, and $z:C$ and morphisms (elements of [[hom types]]) $g:\mathrm{hom}_C(y, z)$ and $h:\mathrm{hom}_C(x, z)$

* a function $k:\Lambda_0^2 \to C$ from the **(2,0)-[[horn]] type** $\Lambda_0^2$ to $C$, where $\Lambda_0^2$ is defined in terms of the [[directed interval]] as the type of pairs of elements $i, j:\mathbb{I}$ such that $i = 1$ or $j = 1$. 

$$\Lambda_0^2 \coloneqq \sum_{i:\mathbb{I}} \sum_{j:\mathbb{I}} (i = 1) \vee (j = 1)$$

## The walking cospan

The **[[walking]] [[cospan]]** or **(2,0)-[[horn]] category** is the [[category]] $\Lambda_0^2$ which consists of three objects $0, 1, 2 \in \Lambda_0^2$ and two morphisms $h_{02}:\mathrm{hom}_{\Lambda_0^2}(0, 2)$ and $h_{12}:\mathrm{hom}_{\Lambda_0^2}(1, 2)$. 

The category $\Lambda_0^2$ is also called the **(2,0)-horn preorder** or the **(2,0)-horn poset** because $\Lambda_0^2$ can be shown to be a [[poset]]. 

Every cospan in a category $C$ is represented by a [[functor]] $F:\Lambda_0^2 \to C$ from the walking cospan to $C$. 

In type theoretic approaches to synthetic $(\infty,1)$-category theory, the **(2,0)-[[horn]] type** $\Lambda_0^2$ defined above plays the role of the walking cospan. 

## Properties

### Right quotients

Following the notion of a right [[quotient]] of two elements in a [[monoid]], we can define in [[category]] the notion of a *right quotient* of a cospan in a category. 

A **right quotient** of a cospan $g:\mathrm{hom}_A(y, z)$ and $h:\mathrm{hom}_A(x, z)$ is a morphism $f:\mathrm{hom}_A(x, y)$ such that $h$ is the [[unique composite]] of $f$ and $g$, $g \circ f = h$. 

Given a morphism $f:\mathrm{hom}_A(x, y)$, the cospan $(f, \mathrm{id}_y)$ is always right divisible with right quotient $f$. A [[section]] is a right quotient of the span $(\mathrm{id}_y, f)$. 

## The bicategory of cospans

Cospans in a category $V$ with small colimits form a [[bicategory]] whose objects are the objects of $V$, whose morphisms are cospans between two objects, and whose 2-morphisms $\eta$ are commuting diagrams of the form

$$
  \array{
    && S
    \\
    & {}^{\sigma_{S}}\nearrow && \nwarrow^{\tau_S}
    \\
    a &&\downarrow^\eta&& b
    \\
    & {}_{\sigma_T}\searrow
    && \swarrow_{\tau_T}
    \\
    && T
  }
  \,.
$$

The category of cospans from $a$ to $b$ is naturally a [[enriched category|category enriched in]] $V$: for

$$
  \array{
    && S
    \\
    & {}^{\sigma_{S}}\nearrow && \nwarrow^{\tau_S}
    \\
    a &&&& b
    \\
    & {}_{\sigma_T}\searrow
    && \swarrow_{\tau_T}
    \\
    && T
  }
$$

two parallel cospans in $V$, the $V$-object 
${}_a[S,T]_b$
of morphisms between them is the pullback

$$
  \array{
    {}_a[S,T]_b
     &\to&
     pt
    \\
    \downarrow && \downarrow^{\sigma_T \times \tau_T}
    \\
    [S,T] &\stackrel{\sigma_S^* \times \sigma_T^*}{\to}& 
    [a \sqcup b, T]
  }
$$

formed in analogy to the enriched hom of [[pointed object]]s. The [[initial object]] of $V$ is the [[coproduct]] of $a$ and $b$.

If $V$ has a terminal object, $pt$, then cospans from $pt$ to itself are [[bi-pointed object]]s in $V$.

##Related concepts

* [[cospan cotrace]]
* [[multi-cospan]]
* [[Cospans in Algebraic Topology]]
* [[multispan]]
* the [cograph of a function](http://ncatlab.org/nlab/show/graph+of+a+function#cograph)
* the [[cograph of a functor]]

* [[sink]], [[cosink]]

* [[product]], [[coproduct]]

* [[horn]]

* [[span]], [[cospan]]

* [[composable pair]]

* [[composite]]

* [[commutative triangle]]

* [[isomorphism]]

[[!include notions of walking structure]]

##References

Topological cospans and their role as models for [[cobordism]]s are discussed in

* Marco Grandis, _Collared cospans, cohomotopy and TQFT (Cospans in algebraic topology, II)_ ([pdf](http://www.dima.unige.it/~grandis/wCub2.pdf))

[[!redirects cospan]]
[[!redirects cospans]]
[[!redirects opspan]]
[[!redirects opspans]]
[[!redirects co-span]]
[[!redirects co-spans]]

[[!redirects walking cospan]]
[[!redirects walking cospans]]

[[!redirects walking co-span]]
[[!redirects walking co-spans]]

[[!redirects free-standing cospan]]
[[!redirects free-standing cospans]]

[[!redirects free-standing co-span]]
[[!redirects free-standing co-spans]]

[[!redirects free-living cospan]]
[[!redirects free-living cospans]]

[[!redirects free-living co-span]]
[[!redirects free-living co-spans]]

[[!redirects (2,0)-horn category]]
[[!redirects (2,0)-horn categories]]

[[!redirects (2,0)-horn preorder]]
[[!redirects (2,0)-horn preorders]]

[[!redirects (2,0)-horn proset]]
[[!redirects (2,0)-horn prosets]]

[[!redirects (2,0)-horn poset]]
[[!redirects (2,0)-horn posets]]

[[!redirects (2,0)-horn type]]
[[!redirects (2,0)-horn types]]

[[!redirects right quotient]]
[[!redirects right divisible]]
[[!redirects right divisibility]]

[[!redirects right divisible span]]
[[!redirects right divisible spans]]

[[!redirects right divisible correspondence]]
[[!redirects right divisible correspondences]]

[[!redirects right divisibility in a category]]
[[!redirects right divisible in a category]]

[[!redirects cospan in simplicial type theory]]
[[!redirects cospans in simplicial type theory]]

[[!redirects cospan in an (infinity,1)-category]]
[[!redirects cospans in an (infinity,1)-category]]
