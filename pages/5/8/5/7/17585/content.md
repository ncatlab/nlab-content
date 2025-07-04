
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

In [[rational homotopy theory]], given a [[rational topological space]] modeled by a [[Sullivan model]] [[dg-algebra]], there is an explicit description of the Sullivan model of its [[loop space]], ([[free loop space]] or [[based loop space]]).

This is a special case of [[Sullivan models of mapping spaces]].


## Construction

### For the free loop space
 {#ConstructionForFreeLoopSpace}

+-- {: .num_prop #SullivanModelForTheFreeLoopSpace}
###### Proposition
**([[Sullivan model]] for [[free loop space]])**

Let $(\wedge^\bullet V, d_X)$ be a [[semifree dg-algebra]] being a [[minimal Sullivan model]] of a [[rational space|rational]] [[simply connected space]] $X$. Then a Sullivan model for the [[free loop space]] $\mathcal{L} X$ is given by

$$
  \big(
    \wedge^\bullet( V \oplus s V )
    ,\, 
    d_{\mathcal{L}X}
  \big)
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

This is due to [Vigu&#233; & Sullivan 1976](#VigueSullivan76). Review includes [Felix, Halperin & Thomas 2000, p. 206](#FelixHalperinThomas00), [Hess 2006, ex. 2.5](#Hess06), [F&#233;lix, Oprea & Tanre 2008, thm. 5.11](#FelixOpreaTanre08).

+-- {: .num_remark}
###### Remark

The formula in prop. \ref{SullivanModelForTheFreeLoopSpace} is akin to that that for the [[Weil algebra]] of the [[L-infinity algebra|$L_\infty$-algebra]] of which $(\wedge^\bullet V,d_X)$ is the [[Chevalley-Eilenberg algebra]], except that here $s$ shifts _down_, whereas for the Weil algebra it shifts _up_.

=--


### For the based loop space
 {#ConstructionForBasedLoopSpace}

The [above](#ConstructionForFreeLoopSpace) result for the Sullivan model of free loop spaces implies also the models for based loop spaces, as follows.

For $X$ a [[pointed topological space]] and for the [[circle]] $S^1$ regarded as [[pointed topological space|pointed]] by any base point $\ast \to S^1$  there is the following [[homotopy fiber sequence]] which exhibits the [[based loop space]] as the [[homotopy fiber]] of the [[evaluation map]] out of the [[free loop space]]:

$$
  \Omega X 
  \overset{fib(ev_\ast)}{\longrightarrow}
  \mathcal{L}X 
  \overset{ ev_\ast }{\longrightarrow}
  X
  \,.
$$

With the dgc-algebra model from Prop. \ref{SullivanModelForTheFreeLoopSpace} for $\mathcal{L}X$ it follows that the dgc-algebra model for the based loop space is the [[homotopy cofiber]] [[dgc-algebra]] $(\wedge^\bullet( s V ), d_{\Omega X})$ in

$$
  (\wedge^\bullet( s V ), d_{\Omega X})
  \overset{ cofib\big( (ev_\ast)^\ast \big) }{\longleftarrow}
  (\wedge^\bullet( V \oplus s V ), d_{\mathcal{L}X})
  \overset{ (ev_\ast)^\ast }{\longleftarrow}
  (\wedge^\bullet V, d_X)
  \,.
$$

Since the inclusion on the right is manifestly a [[relative Sullivan algebra]], hence a [[cofibration]] in the projective [[model structure on dgc-algebras]], and since the latter is [[left proper model category|left proper]] (see [there](model+structure+on+dg-algebras#Properness)), the [[homotopy cofiber]] is represented by the ordinary [[cofiber]], which is readily read off:

\begin{prop}\label{SullivanModelForBasedLoopSpace}
**([[Sullivan model]] for [[based loop space]])**
\linebreak
For $X$ a [[connected topological space|connected]] and [[simply connected topological space]] with [[Sullivan model]] $(\wedge^\bullet V, d_X)$, the Sullivan model 
$(\wedge^\bullet( s V ), d_{\Omega X})$ 
of its [[based loop space]] $\Omega X$
is the dgc-algebra obtained from $(\wedge^\bullet V, d_X)$ by shifting down all generators in degree by 1, and by keeping only the co-unary component of the [[differential]].
\end{prop}

(cf. also [Félix, Halperin & Thomas 2000 p 143](#FelixHalperinThomas00))

\begin{remark}\label{PontrjaginProductOnHomologyOfBasedLoopSpace}
  While Prop. \ref{SullivanModelForBasedLoopSpace} says that the rational [[Whitehead brackets]] of a loop space all vanish (as generally for any [[H-space]], see [there](H-space#RationalHomotopy)), the [[ordinary homology]] of a loop space inherits another product, namely the [[Pontrjagin product]], and this makes (see [there](Pontrjagin+ring#RelationToWhiteheadProduct)) the homology form the [[universal enveloping algebra]] of the binary [[Whitehead bracket]] [[super Lie algebra]] of the original space.
\end{remark}


## Properties

### Homotopy quotient by $S^1$


+-- {: .num_prop #ModelForS1quotient}
###### Proposition

Given a [[Sullivan model]] $(\wedge^\bullet (V \oplus s V), d_{\mathcal{L}X})$ for a [[free loop space]] as in prop. \ref{SullivanModelForTheFreeLoopSpace}, then a Sullivan model for the [[cyclic loop space]], i.e. for the [[homotopy quotient]] $\mathcal{L} X \sslash S^1$ with respect to the canonical [[circle group]] action that rotates loops (i.e. for the [[Borel construction]] $\mathcal{L}X \times_{S^1} E S^1$) is given by

$$
  \Big(
    \wedge^\bullet(  
       V\oplus s V \oplus \langle \omega_2\rangle 
    )
    ,\, 
    d_{\mathcal{L}X/S^1}
  \Big)
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

is a model for the [[rationalization]] of the [[homotopy fiber sequence]]

$$
  \mathcal{L}X 
    \longrightarrow
  \mathcal{L}X \sslash S^1
    \longrightarrow
  B S^1
$$

which exhibits the [[infinity-action]] (by the discussion there) of $S^1$ on $\mathcal{L}X$.

=--

This is due to ([Vigu&#233;-Burghelea 85, theorem A](#VigueBurghelea85)).


\begin{example}\label{SullivanModelOfCyclicLoopOfEm}
**([[Sullivan model]] of [[cyclic loop space]] of [[Eilenberg-MacLane space|EM-space]])**
\linebreak
For $n \geq 1$ consider the [[Eilenberg-MacLane space]] 
$X \,=\, B^{n+1} \mathbb{Q}$, whose [[Sullivan model of a classifying space]] is

$$
  CE\big(
    \mathfrak{l}
    B^{n+1} \mathbb{Q}
  \big)
  \;\;
  =
  \;\;
  \mathbb{Q}[c_{n+1}]
  \big/
  \big(
    \mathrm{d} \, c_{n+1}  \;=\; 0
  \big)
  \,.
$$


Notice -- from [this Prop](free+loop+space+of+classifying+space#FreeLoopSpaceOfClassifyingSpaceOfSimplicialAbelianGroup) at *[[free loop space of classifying space]]* -- that its [[free loop space]] is the [[product]]

$$
  \mathcal{L}
  \; 
  B^{n+1} \mathbb{Q}
  \;\simeq\;
  B^{n} \mathbb{Q}
  \,\times\,
  B^{n+1} \mathbb{Q}
  \,.
$$

Now Prop. \ref{ModelForS1quotient} shows that the corresponding [[cyclic loop space]] is as in the middle item here:

$$
  \begin{array}{ccc}
  B^n \mathbb{Q}
  &\longrightarrow&
  \Big(
    \overset{
      B^{n} \mathbb{Q} 
      \,\times\,
      B^{n+1} \mathbb{Q}
    }{
      \overbrace{
        \mathcal{L} \;B^{n+1} \mathbb{Q}
      }
    }
  \Big) 
  \sslash S^1
  &\longrightarrow&
  B^n \mathbb{Q}
  \\
  \left(
  \begin{array}{lcl}
    d & c_{n} & = 0
  \end{array}
  \right)  
  &
  \longleftarrow
  &
  \left(
  \begin{array}{lcl}
    d & c_{n+1} & = \omega_2 \wedge c_n
    \\
    d & c_{n} & = 0
    \\
    d & \omega_2 & = 0
  \end{array}
  \right)
  &
  \longleftarrow
  &
  \left(
  \begin{array}{lcl}
    d & c_{n} & = 0
  \end{array}
  \right)  
  \end{array}
$$

Incidentally, as indicated by the full diagram, this readily shows that $\big(\mathcal{L}\, B^{n+1} \mathbb{Q}\big) \sslash S^1$ [[retraction|retracts]] onto $B^{n} \mathbb{Q}$.
\end{example}





### Relation to Hochschild- and cyclic-homology
  {#RelationToHochschildHomology}

Let $X$ be a [[simply connected topological space|simply connected]] [[topological space]]. 

The [[ordinary cohomology]] $H^\bullet$ of its [[free loop space]] is the [[Hochschild homology]] $HH_\bullet$ of its [[singular cohomology|singular chains]] $C^\bullet(X)$:

$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( C^\bullet(X) )
  \,.
$$

Moreover the $S^1$-equivariant cohomology of the loop space, hence the ordinary cohomology of the [[cyclic loop space]] $\mathcal{L}X \sslash S^1$ is the [[cyclic homology]] $HC_\bullet$ of the singular chains:

$$
  H^\bullet(\mathcal{L}X \sslash S^1)
    \simeq
  HC_\bullet( C^\bullet(X) )
$$

([Jones 87, Thm. A](cyclic+homology#Jones87), review in [Loday 92, Cor. 7.3.14](cyclic+homology#Loday92), [Loday 11, Sec 4](cyclic+homology#Loday11))

If the [[coefficients]] are [[rational numbers|rational]], and $X$ is of [[finite type]] then by prop. \ref{SullivanModelForTheFreeLoopSpace} and prop. \ref{ModelForS1quotient}, and the general statements at _[[rational homotopy theory]]_, the [[cochain cohomology]] of the above [[minimal Sullivan models]] for $\mathcal{L}X$ and $\mathcal{l}X/S^1$ compute the rational [[Hochschild homology]] and [[cyclic homology]] of (the cochains on) $X$, respectively. 


In the special case that the [[topological space]] $X$ carries the structure of a [[smooth manifold]], then the singular cochains on $X$ are equivalent to the [[dgc-algebra]] of [[differential forms]] (the [[de Rham algebra]]) and hence in this case the statement becomes that 


$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( \Omega^\bullet(X) )
  \,.
$$

$$
  H^\bullet(\mathcal{L}X \sslash S^1)
    \simeq
  HC_\bullet( \Omega^\bullet(X) )
  \,.
$$

This is known as _[[Jones' theorem]]_ ([Jones 87](#Jones87))

An [[(infinity,1)-category theory|infinity-category theoretic]] proof of this fact is indicated at _[Hochschild cohomology -- Jones' theorem](Hochschild+cohomology#JonesTheorem)_.


## Examples

### Free loop space of the 4-sphere 
 {#4SphereAndTwistedDeRham}

We discuss the Sullivan model for the free and cyclic loop space of the [[4-sphere]]. This may also be thought of as the [[cocycle space]] for [[rational Cohomotopy|rational 4-Cohomotopy]], see [FSS16, Section 3](#FiorenzaSatiSchreiber16).

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

and prop. \ref{ModelForS1quotient} gives for the rationalization of $\mathcal{L}S^4 \sslash S^1$ the model

$$
  ( \wedge^\bullet \langle \omega_2, \omega_4, \omega_6, h_3, h_7 \rangle  , d_{\mathcal{L}S^4 \sslash S^1} ) 
$$

with 

\[
  \label{CERelationsForCyclicLoopSpaceOfS4}
  \begin{aligned}
    d_{\mathcal{L}S^4 \sslash S^1} h_3 & = 0
    \\
    d_{\mathcal{L}S^4 \sslash S^1} \omega_2 & = 0
    \\
    d_{\mathcal{L}S^4 \sslash S^1} \omega_4 & = h_3 \wedge \omega_2 
    \\
    d_{\mathcal{L}S^4 \sslash S^1} \omega_6 & = h_3 \wedge \omega_4
    \\
    d_{\mathcal{L}S^4 \sslash S^1} h_7 & = -\tfrac{1}{2} \omega_4 \wedge \omega_4 + \omega_2 \wedge \omega_6
  \end{aligned}
  \,.
\]

=--

\begin{remark}\label{RelationOfCycS4ToTwistedDeRhamCohomology}
  **(relation to [[twisted de Rham cohomology]])** \linebreak
  The equations (eq:CERelationsForCyclicLoopSpaceOfS4) imply that [[dg-algebra]] [[homomorphisms]] of the form
  $$
    CE
    \Big(
      \mathfrak{l}
      \big(
        (\mathcal{L}S^4) \sslash S^1
      \big)
    \Big)
    \xrightarrow{\;\;AA\;\;}
    \Omega^\bullet_{dR}(X^f)
  $$
  into the [[de Rham dg-algebra]] of a [[smooth manifold]] $X^f$ of [[dimension of a manifold|dimension]] $\leq 7$ are equivalently [[cocycles]] in the degree-3 [[twisted de Rham complex]] of $X^7$ (together with any 7-form, if $dim = 7$), for 3-twist given by the image of the general $h_3$. 

This suggests a relation between the cyclification of $S^4$ to the [[twisted Chern character]] on [[twisted K-theory]] (a relation further explored in [[schreiber:Gauge enhancement of Super M-Branes|BMSS 2019]]).
\end{remark}

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

with $\mathfrak{l}(S^4)$ from prop. \ref{SullivanModelForTheFreeLoopSpace} and $\mathfrak{l}(\mathcal{L}S^4 \sslash S^1)$ from prop. \ref{ModelForS1quotient},
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

This is observed in ([Fiorenza-Sati-Schreiber 16](#FiorenzaSatiSchreiber16), [FSS 16b](#FSS16b)), where it serves to formalize, on the level of [[rational homotopy theory]], the [[double dimensional reduction]] of [[M-branes]] in [[M-theory]] to [[D-branes]] in [[type IIA string theory]] (for the case that $\mathfrak{g}$ is type IIA [[super Minkowski spacetime]] $\mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}$ and $\hat \mathfrak{g}$ is 11d [[super Minkowski spacetime]] $\mathbb{R}^{10,1\vert \mathbf{32}}$, and the cocycles are those of [[schreiber:The brane bouquet]]).

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


### Free loop space of the 2-sphere

+-- {: .num_example}
###### Example

Let $X = S^2$ be the [[2-sphere]]. The corresponding [[rational n-sphere]] has minimal Sullivan model

$$
  \big(\wedge^\bullet \langle g_3, g_2 \rangle, d\big)
$$

with 

$$
  d g_2 = 0\,,\;\;\;\; d g_3 = -\tfrac{1}{2} g_2 \wedge g_2
  \,.
$$

Hence prop. \ref{SullivanModelForTheFreeLoopSpace} gives for the rationalization of $\mathcal{L}S^2$ the model

\[
  \label{SullivanModelForLS2}
  \big( 
    \wedge^\bullet 
    \langle 
       \omega^A_2, \omega^B_2, h_1, h_3 
    \rangle, 
     d_{\mathcal{L}S^2} 
  \big) 
\]

with

\[
  \label{DifferentialInSullivanModelForLS2}
  \begin{aligned}
    d_{\mathcal{L}S^2} h_1 & = 0
    \\
    d_{\mathcal{L}S^2} \omega^A_2 & = 0
    \\
    d_{\mathcal{L}S^2} \omega^B_2 & = h_1 \wedge \omega_2^A
    \\
    d_{\mathcal{L}S^2} h_3 & = -\tfrac{1}{2} \omega^A_2 \wedge \omega^A_2
  \end{aligned}
\]

and prop. \ref{ModelForS1quotient} gives for the rationalization of $\mathcal{L}S^2 \sslash S^1$ the model

$$
  ( \wedge^\bullet \langle \omega^A_2, \omega^B_2, \omega^C_2, h_1, h_3 , d_{\mathcal{L}S^2 \sslash S^1} ) 
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

It follows in particular that:
\begin{corollary}\label{FundamentalGroupAnd1HomologyOfLS2}
  The [[fundamental group]] of the [[free loop space]] of the [[2-sphere]] is the [[integers]]:
  \[
    \label{FundamentalGroupOfLS2}
    \pi_1\big( \mathcal{L} S^2 \big)
    \;\simeq\;
    \mathbb{Z}
  \]
  as is its first [[ordinary homology]] [[homology group|group]] with [[integer]] [[coefficients]]:
  \[
    \label{Integral1HomologyOfLS2}
    H_1\big( \mathcal{L} S^2 ;\, \mathbb{Z} \big)
    \;\simeq\;
    \mathbb{Z}
    \,.
  \]
\end{corollary}
(The second statement (eq:Integral1HomologyOfLS2) is also part of [Cohen, Jones & Yan 2004 Thm. 2](string+topology#CohenJonesYan04).)
\begin{proof}
  A general fact about [[minimal Sullivan models]] is that the $\mathbb{Q}$-[[linear span]] of their algebra generators is [[linear isomorphism|linearly isomorphic]] to the [[rationalization]] of the [[homotopy groups]] of the corresponding space. Since the Sullivan model for $\mathcal{L} S^2$ has a single generator in degree 1, according to (eq:SullivanModelForLS2), this implies that 
\[
  \label{RationalFundamentalGroupsOfLS2}
  \pi_1\big(
    \mathcal{L}S^2
  \big) \otimes_{{}_{\mathbb{Z}}}
  \mathbb{Q}
  \;\simeq\;
  \mathbb{Q}
  \,.
\]

At the same time, the [[evaluation]] [[homotopy fiber sequence]] which characterizes the based [[loop space]]

$$
  \Omega S^2 
    \longrightarrow 
  \mathcal{L}S^2
    \xrightarrow{\; ev \;}
  S^2
$$

induces the [[long exact sequence of homotopy groups]] which reads in parts:

$$
  \underset{\mathbb{Z}}{\underbrace{
    \pi_2(S^2)
  }}
  \longrightarrow
  \underset{\mathbb{Z}}{\underbrace{
    \pi_1 \Omega S^2
  }}
  \longrightarrow
    \pi_1 \mathcal{L} S^2
  \longrightarrow
  \underset{1}{\underbrace{
    \pi_1 S^2
  }}
  \mathrlap{\,.}
$$
Here, [[group homomorphism|homomorphy]] implies that the left map is given by multiplication with some $n \in \mathbb{N}$,
and then [[exact sequence|exactness]] implies that
$$
  \pi_1 \mathcal{L} S^2 
  \;\simeq\;
  \mathbb{Z}/n
$$
is a [[cyclic group]].
But since the [[rationalization]] of [[cyclic groups]] is
$$
  (\mathbb{Z}/n)
  \otimes_{{}_{\mathbb{Z}}}
  \mathbb{Q}
  \;\simeq\;
  \left\{
  \begin{array}{ccl}
    \mathbb{Q} &\vert& n = 0
    \\
    0 &\vert& \text{otherwise,}
  \end{array}
  \right.
$$
comparison with (eq:RationalFundamentalGroupsOfLS2) implies the first claim (eq:FundamentalGroupOfLS2). From this, the second claim (eq:Integral1HomologyOfLS2) follows by the [[Hurewicz theorem]] ([this Prop.](Hurewicz+theorem#HurewiczTheoremInDegreeOne)). 
\end{proof}
\begin{remark}
Incidentally, note that the second statement of Cor. \ref{FundamentalGroupAnd1HomologyOfLS2} is compatible with that single generator of degree 1 in (eq:SullivanModelForLS2) being closed, according to (eq:DifferentialInSullivanModelForLS2), implying as such already that $H_1(\mathcal{L}S^2; \mathbb{Q}) \simeq \mathbb{Q}$.
\end{remark}



\linebreak

### Iterated based loop spaces of $n$-spheres
 {#IteratedLoopSpacesOfNSpheres}

By iterating the Sullivan model construction for the [[based loop space]] from Prop. \ref{SullivanModelForBasedLoopSpace} and using the [[Sullivan models of n-spheres]] we have that:

+-- {: .num_prop #SullivanModelsOfMapsFromSkToSnFornLargerk}
###### Proposition
**([[Sullivan models]] for [[iterated loop spaces]] of [[n-spheres]])**

The [[Sullivan model]] of the $k$-fold [[iterated based loop space]] $\Omega^k S^n $ of the [[n-sphere]] for $k \lt n$ is 

$$
  CE\mathfrak{l}
  \big(
    \Omega^k S^n
  \big)
  \;=\;
  \left\{
  \array{
    \left( 
      \array{
        d\,\omega_{n-k} & = 0
      }
    \right)
    &\vert&
    n \;\text{is odd}
   \\
    \left( 
      \array{
        d\,\omega_{n-k} & = 0
        \\
        d\,\omega_{2n-1-k} & = 0
      }
    \right)
    &\vert&
    n \;\text{is even}
  }
  \right.
  \phantom{AAAA}
  \text{for}\; k \lt n
  \,.
$$

=--

(see also [Kallel-Sjerve 99, Prop. 4.10](#KallelSjerve99))

For the edge case $\Omega^D S^D$ the above formula does not apply, since $\Omega^{D-1} S^D$ is not [[simply connected topological space|simply connected]] (its [[fundamental group]] is $\pi_1\big( \Omega^{D-1}S^D \big) = \pi_0 \big(\Omega^D S^D\big) = \pi_D(S^D) = \mathbb{Z}$, the 0th [[stable homotopy group of spheres]]). 

But:

+-- {: .num_example #RationalModelsForBasedMappingSpaceSDToSD}
###### Example   

The rational model for $\Omega^D S^D$ follows from [this Prop.](Sullivan+model+of+mapping+space#RationalHomotopyTypeOfMapsNSphereToNsphere) by realizing the pointed mapping space as the [[homotopy fiber]] of the [[evaluation map]] from the free mapping space:

$$
  \array{
    \mathllap{
      \Omega^D S^D
      \simeq
    \;}
    Maps^{\ast/\!}\big( S^D, S^D\big)
    \\
    \big\downarrow^{\mathrlap{fib(ev_\ast)}}
    \\
    Maps(S^D, S^D)
    \\
    \big\downarrow^{\mathrlap{ev_\ast}}
    \\
    S^D
  }
$$

This yields for instance the following examples.

In odd dimensions:

\begin{xymatrix}
    \mathrm{Maps}^{\ast/\!}
    \big(
      S^3, S^3
    \big)
    \ar[d]^-{ \mathrm{fib}_{(\mathrm{ev}_\ast)} }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \underset{
      n \in \mathbb{Z}
    }{\sqcup}
    \ast
    \ar@{^{(}->}[d]
    \\
    \mathrm{Maps}
    \big(
      S^3, S^3
    \big)
    \ar[d]^-{ \mathrm{ev}_\ast }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \underset{
      n  \in \mathbb{Z}
    }{\sqcup}
    S^3
    \ar[d]^-{ (\mathrm{id}_{S^3})_{n \in \mathbb{N}} }
    \\
    S^3
    \ar@{=}[r]
    &
    S^3
\end{xymatrix}

In even dimensions:

(In the following $h_{\mathbb{K}}$ denotes the [[Hopf fibration]] of the [[division algebra]] $\mathbb{K}$, hence $h_{\mathbb{C}}$ denotes the [[complex Hopf fibration]] and $h_{\mathbb{H}}$ the [[quaternionic Hopf fibration]].)

\begin{xymatrix}
    \mathrm{Maps}^{\ast/\!}
    \big(
      S^2, S^2
    \big)
    \ar[d]^-{ \mathrm{fib}_{(\mathrm{ev}_\ast)} }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \underset{
      n \in \mathbb{Z}
    }{\sqcup}
    S^1
    \ar@{^{(}->}[d]
    \\
    \mathrm{Maps}
    \big(
      S^2, S^2
    \big)
    \ar[d]^-{ \mathrm{ev}_\ast }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \big(
      S^2 \times S^1
    \big)
    \sqcup
    \big(
      \underset{
        n \neq 0  \in \mathbb{Z}
      }{\sqcup}
      S^3
    \big)
    \ar[d]^-{
      \big(
        p_1, (h_{\mathbb{C}})_{n \neq 0 \in \mathbb{N}}
      \big)
    }
    \\
    S^2
    \ar@{=}[r]
    &
    S^2
\end{xymatrix}


\begin{xymatrix}
    \mathrm{Maps}^{\ast/\!}
    \big(
      S^4, S^4
    \big)
    \ar[d]^-{ \mathrm{fib}_{(\mathrm{ev}_\ast)} }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \underset{
      n \in \mathbb{Z}
    }{\sqcup}
    S^3
    \ar@{^{(}->}[d]
    \\
    \mathrm{Maps}
    \big(
      S^4, S^4
    \big)
    \ar[d]^-{ \mathrm{ev}_\ast }
    \ar@{}[r]|-{ \simeq_{\mathbb{Q}} }
    &
    \big(
      S^4 \times S^3
    \big)
    \sqcup
    \big(
      \underset{
        n \neq 0  \in \mathbb{Z}
      }{\sqcup}
      S^7
    \big)
    \ar[d]^-{ 
      \big(
        p_1, (h_{\mathbb{H}})_{n \neq 0 \in \mathbb{N}} 
      \big)
    }
    \\
    S^4
    \ar@{=}[r]
    &
    S^4
\end{xymatrix}



=--


## Related concepts

* [[Hochschild homology]]

* [[cyclic homology]]

* [[rational model of mapping spaces]]

* [[rational Cohomotopy]]

[[!include Sullivan models -- examples]]



## References

The original result is due to 

* {#VigueSullivan76} [[Micheline Vigué-Poirrier]], [[Dennis Sullivan]]: _The homology theory of the closed geodesic problem_, J. Differential Geometry **11** (1976) 633-644.

* {#VigueBurghelea85} [[Micheline Vigué-Poirrier]], Dan Burghelea: *A model for cyclic homology and algebraic K-theory of 1-connected topological spaces*, J. Differential Geom. **22** 2 (1985) 243-253 &lbrack;[euclid:jdg/1214439821](https://projecteuclid.org/euclid.jdg/1214439821)&rbrack;


Examples:

* Bitjong Ndombol & M. El Haouari, *The free loop space equivariant cohomology algebra of some formal spaces*, Mathematische Zeitschrift **266** (2010) 863–875 ([doi:10.1007/s00209-009-0602-z](https://doi.org/10.1007/s00209-009-0602-z))

* Kentaro Matsuo, *The Borel cohomology of the loop space of a homogeneous space*, Topology and its Applications **160** 12 (2013) 1313-1332 ([doi:10.1016/j.topol.2013.05.001](https://doi.org/10.1016/j.topol.2013.05.001))

Review:

* {#FelixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]]: _Rational Homotopy Theory_, Graduate Texts in Mathematics **205** Springer (2000) &lbrack;[doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9)&rbrack;

* {#Hess06} [[Kathryn Hess]], example 2.5 of _Rational homotopy theory: a brief introduction_ ([math.AT/0604626](http://arxiv.org/abs/math.AT/0604626))

* {#FelixOpreaTanre08} [[Yves Félix]], John Oprea, [[Daniel Tanre]], _Algebraic models in geometry_, Oxford graduate texts in mathematics 17 (2008)

* A. Yu. Onishchenko and Th. Yu. Popelensky, _Rational cohomology of the free loop space of a simply connected 4-manifold_, J. Fixed Point Theory Appl. 12 (2012) 69&#8211;9 ([DOI 10.1007/s11784-013-0100-0](http://link.springer.com/article/10.1007/s11784-013-0100-0))

* [[Luc Menichi]], _Sullivan models and free loop space_, A short introduction to Sullivan models, with the Sullivan model of a free loop space and the detailed proof of Vigu&#233;-Sullivan theorem on the Betti numbers of free loop space. Workshop on free loop space &#224; Strasbourg, November 2008 (scanned notes [pdf](http://math.univ-angers.fr/perso/lmenichi/Sullivan_models_free_loop_space.pdf))

* {#Menichi13} [[Luc Menichi]], *Rational homotopy -- Sullivan models*, in: *Free Loop Spaces in Geometry and Topology*, IRMA Lect. Math. Theor. Phys., EMS (2015) &lbrack;[arXiv:1308.6685](https://arxiv.org/abs/1308.6685), [doi:10.4171/153](https://doi.org/10.4171/153)&rbrack;

* Somnath Basu, section 3.1 of: *Of Sullivan models, Massey products, and twisted Pontrjagin products*, Journal of Homotopy and Related Structures **10** 2 (2015) 239-273 &lbrack;[arXiv:1209.3226](https://arxiv.org/abs/1209.3226), [doi:10.1007/s40062-013-0057-0](https://doi.org/10.1007/s40062-013-0057-0)&rbrack;

* {#FiorenzaSatiSchreiber16} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]: _[[schreiber:Rational sphere valued supercocycles in M-theory|Rational sphere valued supercocycles in M-theory and type IIA string theory]]_, Journal of Geometry and Physics, Volume 114, Pages 91-108 (2017) ([arXiv:1606.03206](https://arxiv.org/abs/1606.03206))


* {#FSS16b} [[nLab:Domenico Fiorenza]], [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[schreiber:T-Duality from super Lie n-algebra cocycles for super p-branes]]_ ([arXiv:1611.06536](https://arxiv.org/abs/1611.06536))

General background on [[Hochschild homology]] and [[cyclic homology]] is in

* {#Jones87} [[John D.S. Jones]], _Cyclic homology and equivariant homology_, Invent. Math. __87__, 403-423 (1987) ([pdf](https://math.berkeley.edu/~nadler/jones.pdf))

* {#Loday98} [[Jean-Louis Loday]], _Cyclic homology_, Grundlehren Math.Wiss. __301__, Springer (1998)

* {#Loday11} [[Jean-Louis Loday]], _Free loop space and homology_ ([arXiv:1110.0405](https://arxiv.org/abs/1110.0405))

The case of [[iterated based loop spaces]] of [[n-spheres]] is discussed also in

* {#KallelSjerve99} [[Sadok Kallel]], [[Denis Sjerve]], _On Brace Products and the Structure of Fibrations with Section_, 1999 ([pdf](https://www.math.ubc.ca/~sjer/brace.pdf), [[KallelSjerv99.pdf:file]])

[[!redirects Sullivan models of loop spaces]]

[[!redirects Sullivan model of free loop space]]
[[!redirects Sullivan models of free loop space]]
[[!redirects Sullivan model of free loop spaces]]

[[!redirects Sullivan model of the free loop space]]
[[!redirects Sullivan models of the free loop space]]

[[!redirects Sullivan model of a free loop space]]
[[!redirects Sullivan models of a free loop space]]

[[!redirects Sullivan models of free loop spaces]]
[[!redirects Sullivan model for free loop space]]
[[!redirects Sullivan models for free loop space]]
[[!redirects Sullivan model for free loop spaces]]
[[!redirects Sullivan models for free loop spaces]]


[[!redirects Sullivan model of based loop space]]
[[!redirects Sullivan models of based loop spaces]]

[[!redirects Sullivan model for based loop space]]
[[!redirects Sullivan models for based loop spaces]]



