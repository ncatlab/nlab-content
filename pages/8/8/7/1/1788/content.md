+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

***




Consider now a morphism 

$$
  \array{
    X && \stackrel{f}{\to} && Y
    \\
    & {}_{\mathllap{f^\ast \chi}}\searrow &\swArrow& \swarrow_{\mathrlap{\chi}}
    \\
    && E Mod 
  }
$$

along which we want to integrate, with $\chi$ invertible $(\chi^\vee)^\vee \simeq \chi$.

Observe that we have the pair of [[adjoint triples]] of left/right [[Kan extensions]] and [[colimits]]/[[limits]]

$$  
  \array{
    X &\stackrel{f}{\to}& Y &\stackrel{p}{\to}& \ast
    \\
    \\
    Func(X, E Mod)
     &\stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^\ast}{\leftarrow}}{\underset{f_\ast}{\to}}}
     &
    Func(Y, E Mod)
     &\stackrel{\overset{p_!}{\to}}{\stackrel{\overset{p^\ast}{\leftarrow}}{\underset{p_\ast}{\to}}}
    &
    E Mod
  }
  \,.
$$

Notice that $f^\ast$ preserves duals, but $f_!$ may not. 

If $f_! f^\ast \chi^\vee$ is a [[dualizable object]],  say that a *choice of orientation* of $f$ in $\chi$-[[twisted cohomology]] is a choice of $\beta \colon X \to E Mod$ and an [[equivalence]]

$$
  PD 
   \;\colon \;
  \left( f_! f^\ast \chi^\vee
  \right)^\vee
  \simeq
  f_!\left(
    f^\ast \chi - \beta
  \right)
  \,.
$$
 

Then the $(f_! \dashv f^\ast)$ [[counit of an adjunction|counit]]

$$
  f_! f^\ast \chi^\vee \to  \chi^\vee
$$

induces the [[dual morphism]]

$$
  \chi 
    \longrightarrow
  \left(f_! f^\ast \chi^\vee \right)^\vee 
    \underoverset{\simeq}{PD}{\longrightarrow}
  f_!\left(
    f^\ast \chi - \beta
  \right)
$$

and under $\left[ p_! \left( - \right), (-) \right]$ this becomes

$$
  \left[p_! f_! \left(f^\ast \chi - \beta\right), E\right]
  \longrightarrow
  \left[p_! \chi , E\right]
$$

which is 

$$
  E^{\bullet + f^\ast \chi - \beta}(X)
  \longrightarrow
  E^{\bullet + \chi}(Y)
  \,.
$$

This we call the [[Umkehr map]] of $f$ induced by the orientation $PD$.








***

category: meta

[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects שנה טובה]]
[[!redirects Featured math : Quora]]