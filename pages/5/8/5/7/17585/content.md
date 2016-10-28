
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[rational homotopy theory]], given a [[rational space]] modeled by a [[Sullivan model]] [[dg-algebra]], there is an explicit description of the Sullivan model of its [[free loop space]].

## Construction

+-- {: .num_prop #SullivanModelForTheFreeLoopSpace}
###### Proposition

Let $(\wedge^\bullet V, d_X)$ be a [[semifree dg-algebra]] being a [[minimal Sullivan model]] of a [[rational space|rational]] [[simply connected space]] $X$. Then a Sullivan model for the [[free loop space]] $\mathcal{L} X$ is given by

$$
  (\wedge^\bullet( V \oplus s V ), d_{\mathcal{L}X})
  \,,
$$

where

* $s V$ is the [[graded vector space]] obtained from $V$ by shifting degrees down by one: $deg(s v) = deg(v)-1$;

* $d_{\mathcal{L}X}$ is defined on elements $v$ of $V$ by 


  $$
    d_{\mathcal{L}X} v \coloneqq d v
  $$

  and on elements $s v$ of $s V$ by

  $$
    d_{\mathcal{L}X} s v \coloneqq - s ( d v )
    \,,
  $$

  where on the right $s \colon V \to s V$ is extended as a graded [[derivation]] $s \colon \wedge^2 V \to \wedge^\bullet (V \oplus s V) $.

=--

This is due to ([Vigu&#233;-Sullivan 76](#VigueSullivan76)). Review includes ([Felix-Halperin-Thomas 00, p. 206](#FelixHalperinThomas00), [Hess 06, example 2.5](#Hess06), [F&#233;lix-Oprea-Tanre 08, theorem 5.11](#FelixOpreaTanre08)).

+-- {: .num_remark}
###### Remark

The formula in prop. \ref{SullivanModelForTheFreeLoopSpace} is the same as that for the [[Weil algebra]] of the [[L-infinity algebra]] of wich $(\wedge^\bullet V,d_X)$ is the [[Chevalley-Eilenberg algebra]], except that here $s$ shifts _down_ whereas for the Weil algebra it shifts _up_.

=--

## Properties

### Homotopy quotient by $S^1$ and cyclic homology

+-- {: .num_prop #ModelForS1quotient}
###### Proposition

Given a [[Sullivan model]] $(\wedge^\bullet (V \oplus s V), d_{\mathcal{L}X})$ for a [[free loop space]] as in prop. \ref{SullivanModelForTheFreeLoopSpace}, then a Sullivan model for the [[homotopy quotient]] $\mathcal{L} X // S^1$ with respect to the canonical [[circle group]] action that rotates loops (i.e. for the [[Borel construction]] $\mathcal{L}X \times_{S^1} E S^1$) is given by

$$
  (\wedge^\bullet(  V\oplus s V \oplus \langle \omega_2\rangle ), d_{\mathcal{L}X/S^1})
$$

where 

* $\omega_2$ is in degree 2;

* $d_{\mathcal{L}X/S^1}$ is defined on generators $w \in V\oplus s V$ by

  $$
    d_{\mathcal{L}X/S^1} w
      \;\coloneqq\;
    d_{\mathcal{L}X} w + \omega_2 \wedge s w
    \,.
  $$

Moreover, the canonical sequence of morphisms of [[dg-algebras]]

$$
  (\wedge \omega_2, d = 0)
    \longrightarrow
  (\wedge^\bullet(  V\oplus s V \oplus \langle \omega_2\rangle ), d_{\mathcal{L}X/S^1})
    \longrightarrow
  (\wedge^\bullet(  V\oplus s V ), d_{\mathcal{L}X})  
$$

is a model for the rationalization of the [[homotopy fiber sequence]]

$$
  \mathcal{L}X 
    \longrightarrow
  \mathcal{L}X / / S^1
    \longrightarrow
  B S^1
$$

which exhibits the [[infinity-action]] (by the discussion there) of $S^1$ on $\mathcal{L}X$.

=--

This is due to ([Vigu&#233;-Burghelea 85, theorem A](#VigueBurghelea85)).


## Examples

### The 4-sphere and twisted de Rham cohomology
 {#4SphereAndTwistedDeRham}

+-- {: .num_example}
###### Example

Let $X = S^4$ be the [[4-sphere]]. The corresponding [[rational n-sphere]] has minimal Sullivan model

$$
  (\wedge^\bullet \langle g_4, g_7 \rangle, d)
$$

with 

$$
  d g_4 = 0\,,\;\;\;\; d g_7 = -\tfrac{1}{2} g_4 \wedge g_4
  \,.
$$

Hence prop. \ref{SullivanModelForTheFreeLoopSpace} gives for the rationalization of $\mathcal{L}S^4$ the model

$$
  ( \wedge^\bullet \langle \omega_4, \omega_6, h_3, h_7 \rangle  , d_{\mathcal{L}S^4} ) 
$$

with

$$
  \begin{aligned}
    d_{\mathcal{L}S^4} h_3 & = 0
    \\
    d_{\mathcal{L}S^4} \omega_4 & = 0
    \\
    d_{\mathcal{L}S^4} \omega_6 & = h_3 \wedge \omega_4
    \\
    d_{\mathcal{L}S^4} h_7 & = -\tfrac{1}{2} \omega_4 \wedge \omega_4
    \\
  \end{aligned}
$$

and prop. \ref{ModelForS1quotient} gives for the rationalization of $\mathcal{L}S^4 / / S^1$ the model

$$
  ( \wedge^\bullet \langle \omega_2, \omega_4, \omega_6, h_3, h_7 \rangle  , d_{\mathcal{L}S^4 / / S^1} ) 
$$

with 

$$
  \begin{aligned}
    d_{\mathcal{L}S^4 / / S^1} h_3 & = 0
    \\
    d_{\mathcal{L}S^4 / / S^1} \omega_2 & = 0
    \\
    d_{\mathcal{L}S^4 / / S^1} \omega_4 & = h_3 \wedge \omega_2 
    \\
    d_{\mathcal{L}S^4 / / S^1} \omega_6 & = h_3 \wedge \omega_4
    \\
    d_{\mathcal{L}S^4 / / S^1} h_7 & = -\tfrac{1}{2} \omega_4 \wedge \omega_4 + \omega_2 \wedge \omega_6
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Let $\hat \mathfrak{g} \to \mathfrak{g}$ be a [[central extension|central]] [[Lie algebra extension]] by $\mathbb{R}$ of a finite dimensional Lie algebra $\mathfrak{g}$, and let $\mathfrak{g} \longrightarrow b \mathbb{R}$ be the corresponding [[L-∞ algebra cohomology|L-∞ 2-cocycle]] with coefficients in the [[line Lie n-algebra|line Lie 2-algebra]] $b \mathbb{R}$, hence ([[schreiber:The brane bouquet|FSS 13, prop. 3.5]]) so that there is a [[homotopy fiber sequence]] of [[L-∞ algebras]]

$$
  \hat \mathfrak{g}
    \longrightarrow
  \mathfrak{g}
    \overset{\omega_2}{\longrightarrow}
  b \mathbb{R}
$$

which is dually modeled by

$$
  CE(\hat \mathfrak{g})
    =
  ( \wedge^\bullet ( \mathfrak{g}^\ast \oplus \langle e \rangle ), d_{\hat \mathfrak{g}}|_{\mathfrak{g}^\ast} = d_{\mathfrak{g}},\;  d_{\hat \mathfrak{g}} e = \omega_2)
  \,.
$$

For $X$ a space with [[Sullivan model]] $(A_X,d_X)$ write $\mathfrak{l}(X)$ for the corresponding [[L-∞ algebra]], i.e. for the $L_\infty$-algebra whose [[Chevalley-Eilenberg algebra]] is $(A_X,d_X)$:

$$
  CE(\mathfrak{l}X) = (A_X,d_X)
  \,.
$$

Then there is an [[isomorphism]] of [[hom-sets]]

$$
  Hom_{L_\infty Alg}( \hat \mathfrak{g}, \mathfrak{l}(S^4) )
  \;\simeq\;
  Hom_{L_\infty Alg/b \mathbb{R}}( \mathfrak{g}, \mathfrak{l}( \mathcal{L}S^4 / S^1 ) )
  \,,
$$

with $\mathfrak{l}(S^4)$ from prop. \ref{SullivanModelForTheFreeLoopSpace} and $\mathfrak{l}(\mathcal{L}S^4 //S^1)$ from prop. \ref{ModelForS1quotient},
where on the right we have homs in the [[slice category|slice]] over the [[line Lie n-algebra|line Lie 2-algebra]], via prop. \ref{ModelForS1quotient}.

Moreover, this isomorphism takes

$$
  \hat \mathfrak{g}
    \overset{(g_4, g_7)}{\longrightarrow}
  \mathfrak{l}(S^4) 
$$

to

$$
  \array{
    \mathfrak{g} 
      &&
      \overset{(\omega_2,\omega_4, \omega_6, h_3,h_7)}{\longrightarrow}
      &&
    \mathfrak{l}( \mathcal{L}X / S^1 )
    \\
    & 
    {}_{\mathllap{\omega_2}}\searrow 
      && 
    \swarrow_{\mathrlap{\omega_2}}
    \\
    && b \mathbb{R}
  }
  \,,
$$

where

$$
  \omega_4 = g_4 - h_3 \wedge e
  \;\,,
  \;\;\;
  h_7 = g_7 + \omega_6 \wedge e
$$

with $e$ being the central generator in $CE(\hat \mathfrak{g})$ from above, and where the equations take place in $\wedge^\bullet \hat \mathfrak{g}^\ast$ with the defining inclusion $\wedge^\bullet \mathfrak{g}^\ast \hookrightarrow \wedge^\bullet \mathfrak{g}^\ast$ understood.

=--

This is observed in ([Fiorenza-Sati-Schreiber 16](#FiorenzaSatiSchreiber16)), where it serves to formalize, on the level of [[rational homotopy theory]], the [[double dimensional reduction]] of [[M-branes]] in [[M-theory]] to [[D-branes]] in [[type IIA string theory]] (for the case that $\mathfrak{g}$ is type IIA [[super Minkowski spacetime]] $\mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}$ and $\hat \mathfrak{g}$ is 11d [[super Minkowski spacetime]] $\mathbb{R}^{10,1\vert \mathbf{32}}$, and the cocycles are those of [[schreiber:The brane bouquet]]).

+-- {: .proof}
###### Proof

By the fact that the underlying graded algebras are free, and since $e$ is a generator of odd degree, the given decomposition for $\omega_4$ and $h_7$ is unique.

Hence it is sufficient to observe that under this decomposition the defining equations

$$
  d g_4 = 0
  \,,\;\;\;
  d g_{7} = -\tfrac{1}{2} g_4 \wedge g_4
$$

for the $\mathfrak{l}S^4$-valued cocycle on $\hat \mathfrak{g}$ turn into the equations for a $\mathfrak{l} ( \mathcal{L}S^4 / S^1 )$-valued cocycle on $\mathfrak{g}$. This is straightforward:

$$
  \begin{aligned}
    & d_{\hat \mathfrak{g}} ( \omega_4 + h_3 \wedge e ) = 0
    \\
    \Leftrightarrow \;\;\;\;
    &
    d_{\mathfrak{g}} (\omega_4 - h_3 \wedge \omega_2) = 0
    \;\;\; and \;\;\;
    d_{\mathfrak{g}} h_3 = 0
    \\
    \Leftrightarrow \;\;\;\;
    &
    d_{\mathfrak{g}} \omega_4 = h_3 \wedge \omega_2
    \;\;\; and \;\;\;
    d_{\mathfrak{g}} h_3 = 0
  \end{aligned}
$$

as well as

$$
  \begin{aligned}
    & d_{\hat \mathfrak{g}} ( h_7 - \omega_6 \wedge e ) 
      = -\tfrac{1}{2}( \omega_4 + h_3 \wedge e ) \wedge (\omega_4 + h_3\wedge e)
   \\
    \Leftrightarrow \;\;\;\;
    &
    d_\mathfrak{g} h_7 - \omega_6 \wedge \omega_2
    =
    -\tfrac{1}{2}\omega_4 \wedge \omega_4
    \;\;\; and \;\;\;
    - d_\mathfrak{g} \omega_6 = - h_3 \wedge \omega_4 
    \\
    \Leftrightarrow \;\;\;\;
    &
    d_\mathfrak{g} h_7 = -\tfrac{1}{2}\omega_4 \wedge \omega_4  + \omega_6 \wedge \omega_2 
    \;\;\; and \;\;\;
    d_\mathfrak{g} h_6 = h_3 \wedge \omega_4
  \end{aligned}
$$

=--

### The 2-sphere

+-- {: .num_example}
###### Example

Let $X = S^2$ be the [[2-sphere]]. The corresponding [[rational n-sphere]] has minimal Sullivan model

$$
  (\wedge^\bullet \langle g_3, g_2 \rangle, d)
$$

with 

$$
  d g_2 = 0\,,\;\;\;\; d g_3 = -\tfrac{1}{2} g_2 \wedge g_2
  \,.
$$

Hence prop. \ref{SullivanModelForTheFreeLoopSpace} gives for the rationalization of $\mathcal{L}S^4$ the model

$$
  ( \wedge^\bullet \langle \omega^A_2, \omega^B_2, h_1, h_3 \rangle  , d_{\mathcal{L}S^2} ) 
$$

with

$$
  \begin{aligned}
    d_{\mathcal{L}S^2} h_1 & = 0
    \\
    d_{\mathcal{L}S^2} \omega^A_2 & = 0
    \\
    d_{\mathcal{L}S^2} \omega^B_2 & = h_1 \wedge \omega_2^A
    \\
    d_{\mathcal{L}S^2} h_3 & = -\tfrac{1}{2} \omega^A_2 \wedge \omega^A_2
  \end{aligned}
$$

and prop. \ref{ModelForS1quotient} gives for the rationalization of $\mathcal{L}S^2 / / S^1$ the model

$$
  ( \wedge^\bullet \langle \omega^A_2, \omega^B_2, \omega^C_2 h_1, h_3 , d_{\mathcal{L}S^2 / / S^1} ) 
$$

with 

$$
  \begin{aligned}
    d_{\mathcal{L}S^2} h_1 & = 0
    \\
    d_{\mathcal{L}S^2} \omega^A_2 & = \omega^C_2 \wedge h_1
    \\
    d_{\mathcal{L}S^2} \omega^B_2 & = h_1 \wedge \omega_2^A
    \\
    d_{\mathcal{L}S^2} \omega^C_2 & = 0
    \\
    d_{\mathcal{L}S^2} h_3 & = -\tfrac{1}{2} \omega^A_2 \wedge \omega^A_2 + \omega^C_2 \wedge \omega^B_2
  \end{aligned}
  \,.
$$

=--



## Related concepts

* [[Hochschild homology]], [[cyclic homology]]

## References

* {#VigueSullivan76} [[Micheline Vigué-Poirrier]], [[Dennis Sullivan]], _The homology theory of the closed geodesic problem_, J. Differential Geometry 11 (1976) 633-644.

* {#VigueBurghelea85} [[Micheline Vigué-Poirrier]], Dan Burghelea, _A model for cyclic homology and algebraic K-theory of 1-connected topological spaces_, J. Differential Geom. Volume 22, Number 2 (1985), 243-253 ([Euclid](https://projecteuclid.org/euclid.jdg/1214439821))

* {#FelixHalperinThomas00} [[Yves Félix]], [[Steve Halperin]] and J.C. Thomas, _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000. 

* {#Hess06} [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

* {#FelixOpreaTanre08} [[Yves Félix]], John Oprea, Daniel Tanre, _Algebraic models in geometry_, Oxford graduate texts in mathematics 17 (2008)

* A. Yu. Onishchenko and Th. Yu. Popelensky, _Rational cohomology of the free loop space of a simply connected 4-manifold_, J. Fixed Point Theory Appl. 12 (2012) 69&#8211;9 ([DOI 10.1007/s11784-013-0100-0](http://link.springer.com/article/10.1007/s11784-013-0100-0))

* [[Luc Menichi]], _Sullivan models and free loop space_, A short introduction to Sullivan models, with the Sullivan model of a free loop space and the detailed proof of Vigu&#233;-Sullivan theorem on the Betti numbers of free loop space. Workshop on free loop space &#224; Strasbourg, November 2008 (scanned notes [pdf](http://math.univ-angers.fr/perso/lmenichi/Sullivan_models_free_loop_space.pdf))

* {#FiorenzaSatiSchreiber16} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Rational sphere valued supercocycles in M-theory]]_, ([arXiv:1606.03206](https://arxiv.org/abs/1606.03206)) 

[[!redirects Sullivan models of free loop space]]

[[!redirects Sullivan model of the free loop space]]
[[!redirects Sullivan models of the free loop space]]

[[!redirects Sullivan model of a free loop space]]
[[!redirects Sullivan models of a free loop space]]

[[!redirects Sullivan models of free loop spaces]]
