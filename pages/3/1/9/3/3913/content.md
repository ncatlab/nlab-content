
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Thom space** $Th(V)$ of a real [[vector bundle]] $V \to X$ over a [[topological space]] $X$ is the [[topological space]] obtained by first forming the disk bundle $D(V)$ of (unit) disks in the [[fibers]] of $V$ (with respect to a [[metric]] given by any choice of [[orthogonal structure]]) and then identifying to a point the [[boundaries]] of all the disks, i.e. forming the [[quotient topological space]] by the [[sphere bundle]] $S(V)$:

$$
  Th(V) \coloneq D(V)/S(V)
  \,.
$$

(N.B.: this is a quotient of the *total* spaces of the bundles taken in $Top$, not a bundle quotient in $Top/V$.) 

This is equivalently the [[mapping cone]]

$$
  \array{
    S(V) &\longrightarrow& *
    \\
    {}^{\mathllap{p}}\downarrow &\swArrow& \downarrow
    \\
    X & \longrightarrow & Th(V)
  }
$$

in [[Top]] of the [[sphere]] [[bundle]] of $V$. Therefore more generally, for $P \to X$ any [[n-sphere]]-[[fiber bundle]] over $X$ ([[spherical fibration]]), its Thom space is the the [[mapping cone]]

$$
  \array{
    P &\longrightarrow& *
    \\
    {}^{\mathllap{p}}\downarrow &\swArrow& \downarrow
    \\
    X & \longrightarrow & Th(P)
  }
$$

of the bundle projection.


For $X$ a [[compact topological space]], $Th(V)$ is a model for [[generalized the|the]] [[one-point compactification]] of the total space $V$.

The Thom space of the rank-$n$ [[universal vector bundle]] over the [[classifying space]] $B O(n)$ of the [[orthogonal group]] is usuelly denoted $M O(n)$. As $n$ ranges, these spaces form the [[Thom spectrum]].

## Definition 
 {#Definition}

+-- {: .num_defn #ThomSpace}
###### Definition

Let $X$ be a [[topological space]] and let $V \to X$ be a [[vector bundle]] over $X$ of [[rank]] $n$, which is [[associated bundle|associated]] to an [[orthogonal group|O(n)]]-[[principal bundle]]. Equivalently this means that $V \to X$ is the [[pullback]] of the [[universal vector bundle]] $E_n \to B O(n)$ over the [[classifying space]]. Since $O(n)$ preserves the [[metric]] on $\mathbb{R}^n$, by definition, such $V$ inherits the structure of a [[metric space]]-[[fiber bundle]]. With respect to this structure:

1. the **unit disk bundle** $D(V) \to X$ is the subbundle of elements of [[norm]] $\leq 1$;

1. the **unit sphere bundle** $S(V)\to X$ is the subbundle of elements of norm $= 1$;

   $S(V) \overset{i_V}{\hookrightarrow} D(V) \hookrightarrow V$;

1. the **Thom space** $Th(V)$ is the [[cofiber]] (formed in [[Top]] ([prop.](Top#DescriptionOfLimitsAndColimitsInTop))) of $i_V$ 

   $$
     Th(V) \coloneqq cofib(i_V)
   $$

   canonically regarded as a [[pointed topological space]].

$$
  \array{
    S(V) &\overset{i_V}{\longrightarrow}& D(V)
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& Th(V)
  }
  \,.
$$

If $V \to X$ is a general real vector bundle, then there exists an isomorphism to an $O(n)$-[[associated bundle]] and the Thom space of $V$ is, up to based [[homeomorphism]], that of this orthogonal bundle.

=--


+-- {: .num_remark}
###### Remark

If the [[rank]] of $V$ is positive, then $S(V)$ is non-empty and then the Thom space is the [[quotient topological space]]

$$
  Th(V) \simeq D(V)/S(V)
  \,.
$$

However, in the degenerate case that the [[rank]] of $V$ vanishes, hence the case that $V = X\times \mathbb{R}^0 \simeq X$, then $D(V) \simeq V \simeq X$, but $S(V) = \emptyset$. Hence now the [[pushout]] defining the cofiber is

$$
  \array{
    \emptyset &\overset{i_V}{\longrightarrow}& X
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& Th(V) \simeq X_*
  }
  \,,
$$

which exhibits $Th(V)$ as the [[coproduct]] of $X$ with the point, hence as $X$ with a basepoint freely adjoined.

$$
  Th(X \times \mathbb{R}^0) = Th(X) \simeq X_+
  \,.
$$

=--

## Properties
 {#Properties}

+-- {: .num_prop #ThomSpaceOfDirectSumAsQuotientOfThomSpacesOfPullbacks}
###### Proposition

Let $V_1,V_2 \to X$ be two real [[vector bundles]]. Then the Thom space (def. \ref{ThomSpace}) of the [[direct sum of vector bundles]] $V_1 \oplus V_2 \to X$ is expressed in terms of the Thom space of the [[pullbacks]] $V_2|_{D(V_1)}$ and $V_2|_{S(V_1)}$ of $V_2$ to the disk/sphere bundle of $V_1$ as

$$
  Th(V_1 \oplus V_2)
  \simeq
  Th(V_2|_{D(V_1)})/Th(V_2|_{S(V_1)})
  \,.
$$

=--

+-- {: .proof}
###### Proof

Notice that 

1. $D(V_1 \oplus V_2) \simeq D(V_2|_{Int D(V_1)}) \cup S(V_1)$;

1. $S(V_1 \oplus V_2) \simeq S(V_2|_{Int D(V_1)}) \cup Int D(V_2|_{S(V_1)})$.

(Since a point at radius $r$ in $V_1 \oplus V_2$ is a point of radius $r_1 \leq r$ in $V_2$ and a point of radius $\sqrt{r^2 - r_1^2}$ in $V_1$.)

=--

+-- {: .num_cor}
###### Corollary

For $V$ a vector bundle then the Thom space (def. \ref{ThomSpace}) of $\mathbb{R}^n \oplus V$, the [[direct sum of vector bundles]] with the trivial rank $n$ vector bundle, is [[homeomorphism|homeomorphic]] to the [[smash product]] of the Thom space of $V$ with the $n$-[[sphere]] (the $n$-fold [[reduced suspension]]).


$$
  Th(V \oplus \mathbb{R}^n) \simeq S^n \wedge Th(V) = \Sigma^n Th(V)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Apply prop. \ref{ThomSpaceOfDirectSumAsQuotientOfThomSpacesOfPullbacks} with $V_1 = \mathbb{R}^n$ and $V_2 = V$. Since $V_1$ is a trivial bundle, then

$$
  V_2|_{D(V_1)} \simeq V_2\times D^n
$$

(as a bundle over $X\times D^n$) and similarly

$$
  V_2|_{S(V_1)} \simeq V_2\times S^n
  \,.
$$


=--

+-- {: .num_example}
###### Example

In particular, if $\mathbb{R}^n \times X \to X$ is a trivial vector bundle of [[rank]] $n$, then 

$$
  Th(X \times \mathbb{R}^n) \simeq S^n \wedge X_+
$$

is the [[smash product]] of the $n$-[[sphere]] with $X$ with one base 
point freely adjoined (the $n$-fold [[suspension]]).

=--

+-- {: .num_remark}
###### Remark

This implies that for every vector bundle $V$ the sequence of spaces
$Th(\mathbb{R}^n \oplus V)$ forms a [[suspension spectrum]]: this is called the [[Thom spectrum]] of $V$.

=--

## Related concepts

* [[cobordism theory]]

* [[one-point compactification]]

* [[Thom spectrum]]

* [[Thom isomorphism]]

## References

The [[Thom isomorphism]] for Thom spaces was originally found in

* [[René Thom]],   _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_  Comm. Math. Helv. , 28  (1954)  pp. 17&#8211;86

For general discussion see

* [[Michael Atiyah]], _Thom complexes_, Proc. London Math. Soc. __11__  (1961)  pp. 291&#8211;310

* {#Rudyak98} [[Yuli Rudyak]], _On Thom spectra, orientability, and cobordism_, Springer 1998 [googB](http://books.google.hr/books?isbn=3540620435)

* [[eom]], _[Thom space](http://eom.springer.de/t/t092680.htm)_

* [[Dale Husemöller]], _Fibre bundles_ , McGraw-Hill  (1966)

* myyn.org [Thom space](http://myyn.org/m/article/thom-space), [Thom class](http://myyn.org/m/article/thom-class), [Thom isomorphism theorem](http://myyn.org/m/article/thom-isomorphism-theorem)

Also

* [[Robert Stong]], _Notes on cobordism theory_ , Princeton Univ. Press  (1968)

* W.B. Browder, _Surgery on simply-connected manifolds_ , Springer  (1972)


