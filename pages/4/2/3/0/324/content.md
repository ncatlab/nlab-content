
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

## The walking cospan

The **[[walking]] [[cospan]]** or **(2,0)-[[horn]] category** is the [[category]] $\Lambda_0^2$ which consists of three objects $0, 1, 2 \in \Lambda_0^2$ and two morphisms $h_{02}:\mathrm{hom}_{\Lambda_0^2}(0, 2)$ and $h_{12}:\mathrm{hom}_{\Lambda_0^2}(1, 2)$. 

The category $\Lambda_0^2$ is also called the **(2,0)-horn preorder** or the **(2,0)-horn poset** because $\Lambda_0^2$ can be shown to be a [[poset]]. 

Every cospan in a category $C$ is represented by a [[functor]] $F:\Lambda_0^2 \to C$ from the walking cospan to $C$. 

In [[dependent type theory]], given a [[directed interval]] $\mathbb{I}$, the **(2,0)-horn type** representing the walking cospan is defined as the type of pairs of elements $i, j:\mathbb{I}$ such that $i = 1$ or $j = 1$. 

$$\Lambda_0^2 \coloneqq \sum_{i:\mathbb{I}} \sum_{j:\mathbb{I}} (i = 1) \vee (j = 1)$$

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
