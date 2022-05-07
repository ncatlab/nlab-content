
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Bockstein homomorphism_ is a [[connecting homomorphism]] induced from a [[short exact sequence]] whose injective map is given by multiplication with an [[integer]].

The archetypical examples are the Bockstein homomorphisms induced this way from the short exact sequence

$$
  \mathbb{Z} 
    \stackrel{\cdot 2}{\to} 
  \mathbb{Z}
    \stackrel{}{\to}
  \mathbb{Z}/2\mathbb{Z}
  \,.
$$

These relate notably degree-$n$ [[cohomology]]  with [[coefficients]] in $\mathbb{Z}_2$ (such as [[Stiefel-Whitney classes]]) to cohomology with integral coefficients in degree $n+1$ (such as [[integral Stiefel-Whitney classes]]).

## Definition

Let $A$ be an [[abelian group]] and $m$ be an [[integer]]. Then multiplication by $m$

$$
  A \stackrel{m\cdot}{\to} A
$$

induces a [[short exact sequence]] of abelian groups

$$
  0\to A/A_{m-tors} \stackrel{m\cdot}{\to} A \to A/m A\to 0,
$$

where $A_{m-tors}$ is the subgroup of $m$-[[torsion subgroup|torsion elements]] of $A$,
and so a long [[fiber sequence]]

$$
\cdots \mathbf{B}^n (A/A_{m-tors}) \to \mathbf{B}^n A \to \mathbf B^n(A/ m A) \to \mathbf{B}^{n+1} (A/A_{m-tors}) \to \cdots
$$

of [[∞-groupoid]]s, where $\mathbf{B}^n(-)$ denotes the $n$-fold [[delooping]] (hence $\mathbf{B}^n A$ is the [[Eilenberg-MacLane object]] on $A$ in degree $n$).

This induces, in turn, for any object $X \in \mathbf{H}$ (for $\mathbf{H}$ the ambient [[(∞,1)-topos]], such as [[Top]] $\simeq$ [[∞Grpd]]) , a long [[fiber sequence]]

$$
\cdots \mathbf{H}(X,\mathbf{B}^n (A/A_{m-tors})) \to \mathbf{H}(X,\mathbf{B}^n A) \to \mathbf{H}(X,\mathbf B^n(A/ m A)) \stackrel{\beta_m}{\to} \mathbf{H}(X,\mathbf{B}^{n+1} (A/A_{m-tors})) \to \cdots
$$

of [[cocycle]] [[∞-groupoids]].

Here the [[connecting homomorphisms]] $\beta_m$ are called the **Bockstein homomorphisms**. 

Notice that often this term is used to refer only to the image of the above in [[cohomology]], hence to the image of $\beta_m$ under [[0-truncated|0-truncation]]/[[homotopy group|0th homotopy group]] $\pi_0$:

$$
 \beta_m : H^n(X,A/ m A) \to H^{n+1}(X,(A/A_{m-tors}))
  \,.
$$




## Examples
  {#Examples}

+-- {: .num_example #Mod2BocksteinIntoIntegralCohomology} 
###### Example
**(mod 2 Bockstein homomorphism into [[integral cohomology]])**

The Bockstein homomorphism $\beta$ for the sequence 

$$
  \mathbb{Z} 
    \stackrel{\cdot 2}{\longrightarrow} 
  \mathbb{Z} 
    \stackrel{mod\, 2}{\longrightarrow} 
  \mathbb{Z}/2\mathbb{Z}
$$ 

serves to define [[integral Stiefel-Whitney classes]] 

$$
  W_{n+1} \coloneqq \beta w_n
$$ 

in degree $n+1$ from $\mathbb{Z}/2\mathbb{Z}$-valued [[Stiefel-Whitney classes]] in degree $n$.

=--

+-- {: .num_example #Mod2BocksteinIntoMod2Cohomology} 
###### Example
**(first [[Steenrod square]])**

The Bockstein homomorphism for the sequence

$$
  \mathbb{Z}/2\mathbb{Z}
    \overset{\cdot 2}{\longrightarrow}
  \mathbb{Z}/4\mathbb{Z}
    \overset{mod\, 2}{\longrightarrow}
  \mathbb{Z}/2\mathbb{Z}
$$

is also called the _first [[Steenrod square]]_, denoted $Sq^1$.

This is often equivalently denoted $\beta$, as in example \ref{Mod2BocksteinIntoIntegralCohomology}. The difference between the two is just the mod-2 reduction in their codomain:

$$
  \label{Mod2BocksteinSequences}
  \array{
    \mathbb{Z}
      &\overset{\cdot 2}{\longrightarrow}&
    \mathbb{Z}
      &\overset{mod\, 2}{\longrightarrow}&
    \mathbb{Z}/2\mathbb{Z}
      &\simeq&
    \mathbb{Z}/2\mathbb{Z}
      &\overset{\beta}{\longrightarrow}&
    B \mathbb{Z}
    \\
    \downarrow^{\mathrlap{id}}
      &&
    \downarrow^{\mathrlap{mod\, 4}}
      &&
    \downarrow^{\mathrlap{id}}
      &&
    \downarrow^{ id }
      &&
    \downarrow^{\mathrlap{B(mod\, 2)}}
    \\
    \mathbb{Z}/2\mathbb{Z}
      &\underset{\cdot 2 }{\longrightarrow}&
    \mathbb{Z}/4\mathbb{Z}
      &\underset{mod\, 2}{\longrightarrow}&
     \mathbb{Z}/2\mathbb{Z}
      &\simeq&
     (\mathbb{Z}/4\mathbb{Z})/(\mathbb{Z}/2\mathbb{Z})
       &\underset{Sq^1}{\longrightarrow}&
     B (\mathbb{Z}/2\mathbb{Z})
  }
$$


More generally, for $p$ any [[prime number]] the multiplication by $p$ on $\mathbb{Z}_{p^2}$ induces the short exact sequence $\mathbb{Z}/p\mathbb{Z} \to \mathbb{Z}/{p^2}\mathbb{Z} \to \mathbb{Z}/p\mathbb{Z}$. The corresponding Bockstein homomorphism $\beta_p$ appears as one of the generators of the mod $p$ [[Steenrod algebra]].

=--

+-- {: .num_example #IntegralSteenrodSquares}
###### Example
**([[integral Steenrod squares]])**

For [[odd natural numbers|odd]] $2n + 1 \in \mathbb{N}$ defines the [[integral Steenrod squares]] to be

$$
  Sq^{2n + 1}_{\mathbb{Z}}
  \;\coloneqq\;
  \beta \circ Sq^{2n}
  \,.
$$

By example \ref{Mod2BocksteinIntoMod2Cohomology} and by the first [[Adem relation]] $Sq^1 \circ Sq^{2n} = Sq^{2n+1}$ ([this example](Steenrod+square#CompositionWithSq1)) these indeed are lifts of the odd [[Steenrod squares]]:

$$
  (mod\, 2) \circ Sq^{2n + 1}_{\mathbb{Z}}
  \;=\;
  Sq^{2n+1}
  \,,
$$

because, by (eq:Mod2BocksteinSequences) we have

$$
  \array{
    Sq^{2n+1}_{\mathbb{Z}}
    &\colon&
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
      &\overset{Sk^{2n}}{\longrightarrow}&      
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
      &\overset{ \beta }{\longrightarrow}&
    B^{\bullet + 2n + 1} \mathbb{Z}
    \\
    &&
    \downarrow^{ id }  
    &&
    \downarrow^{ id }
      &&
    \downarrow^{\mathrlap{B^{k + 2 n + 1}(mod\, 2)}}
    \\
    Sq^{2n+1}
    &\colon&
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
      &\underset{Sk^{2n}}{\longrightarrow}&   
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
       &\underset{  Sq^1 }{\longrightarrow}&
    B^{\bullet + 2n + 1} (\mathbb{Z}/2\mathbb{Z})
  }
$$

=--


When $A=\mathbb{Z}$, the equivalence $\vert \mathbf{B}^{n+1}\mathbb{Z} \vert \cong \vert \mathbf{B}^n U(1)\vert$ (which holds in ambient contexts such as $\mathbf{H} = $ [[ETop∞Grpd]] or [[Smooth∞Grpd]] under [[geometric realization]] $\vert - \vert : ETop \infty Grpd \stackrel{\Pi}{\to} \infty Grpd \stackrel{\simeq}{\to} Top$) identifies the morphisms $\mathbf{B}^n(\mathbb{Z}_m)\to \mathbf{B}^{n+1}\mathbb{Z}$ with the morphisms $\mathbf{B}^n(\mathbb{Z}_m)\to \mathbf{B}^{n} U(1)$ induced by the inclusion of the subgroup of $m$-th roots of unity into $U(1)$. This identifies the Bockstein homomorphism $\beta_m: H^n(X;\mathbb{Z}_m)\to H^{n+1}(X;\mathbb{Z})$ with the natural homomorphism  $H^n(X;\mathbb{Z}_m)\to H^{n}(X;U(1))$.

More in detail:

+-- {: .num_example #Mod2BocksteinAndExponentialExactSequence}
###### Example
**(mod 2 [[Bockstein homomorphism]] and the [[exponential exact sequence]])**

Let 

1. $\beta \;\colon\; \mathbb{Z}/2\mathbb{Z} \longrightarrow B \mathbb{Z}$ be the ordinare Bockstein homomorphism

1. $\iota\coloneqq (\cdot \pi) \;\colon\; \mathbb{Z}/2\mathbb{Z} \hookrightarrow U(1)$ the canonical inclusion;

1. $\delta \;\colon\; U(1) \longrightarrow B\mathbb{Z}$ the classifying map.

Then 

$$
  \beta
  \;=\;
  \delta \circ \iota
  \,.
$$ 

Because

$$
  \array{
    \mathbb{Z}
      &\overset{\cdot 2}{\longrightarrow}&
    \mathbb{Z}
      &\overset{mod\, 2}{\longrightarrow}&
    \mathbb{Z}/2\mathbb{Z}
      &\simeq&
    \mathbb{Z}/2\mathbb{Z}
      &\overset{\beta}{\longrightarrow}&
    B \mathbb{Z}
    \\
    \downarrow^{\mathrlap{id}}
      &&
    \downarrow^{\mathrlap{\cdot \pi}}
      &&
    \downarrow^{\mathrlap{\cdot \pi}}
      &&
    \downarrow^{\iota \coloneqq \mathrlap{\cdot \pi}}
      &&
    \downarrow^{\mathrlap{id}}
    \\
    \mathbb{Z}
      &\underset{\cdot 2 \pi}{\longrightarrow}&
    \mathbb{R}
      &\underset{mod\, 2\pi}{\longrightarrow}&
     U(1)
      &\simeq&
     \mathbb{R}/2\pi\mathbb{Z}
       &\underset{\delta}{\longrightarrow}&
     B \mathbb{Z}
  }
$$

=--

+-- {: .num_prop #SteenrodSquaresAndDBCupProductOnOddClasses}
###### Proposition
**([[Deligne-Beilinson cup product]] on odd-degree [[ordinary differential cohomology]])**

Let

$$
  \hat H
  \;\colon\;
  X \longrightarrow \mathbf{B}^{2n} U(1)_{conn})
$$ 

be a class in [[ordinary differential cohomology]] with underlying class in odd degree

$$
  [H]
  \;\colon\;
  X 
    \overset{\hat H}{\longrightarrow}
  \mathbf{B}^{n} U(1)_{conn}
    \overset{\chi}{\longrightarrow} 
  B^{2n+1} \mathbb{Z}
$$ 

This implies that its [[Beilinson-Deligne cup product]] with itself satisfies

$$
  \hat H \hat \cup \hat H = - \hat H \hat \cup \hat H
$$

hence

$$
  2 \hat H \hat \cup \hat H \;\simeq\; 0
$$

hence 

$$
  2 [H] \cup [H] \;\simeq\; 0
$$

hence that the ordinary [[cup product]] $[H] \cup [H]$ is a 2-torsion class. Let then 

$$
  j
  \;\colon\;
  \mathbf{B}^{4n+1} \mathbb{Z}/2\mathbb{Z}
    \overset{
      B^{4n+1} (\iota)
    }{\hookrightarrow}
  \flat \mathbf{B}^{4n+1}  U(1)
    \longrightarrow
  \mathbf{B}^{4n+1} U(1)_{conn}
$$

with $\iota$ from example \ref{Mod2BocksteinAndExponentialExactSequence}.

Then 

$$
  \hat H  \hat \cup \hat H
  \;\simeq\;
  j Sq^{2n}([H]_{mod\,2})
  \,.
$$

This is a [[differential cohomology]]-refinement of the first [[Adem relation]] $Sq^1 \circ Sq^{2n} = Sq^{2n+1}$ on the [[Steenrod squares]] ([this example](Steenrod+square#CompositionWithSq1)) in that, by example \ref{Mod2BocksteinAndExponentialExactSequence}, its image in ordinary cohomology with coefficients in $\mathbb{Z}/2\mathbb{Z}$ is

$$
  \array{
    ([H]  \cup [H])_{mod 2}
     & \simeq & 
    \underset{
      \beta
    }{
    \underbrace{
      Sq^1
    }}
    \circ Sq^{2n}([H]_{mod\,2})
    \\
    =
    \\
    [H]_{mod\, 2} \cup [H]_{mod,2}
    \\
    =
    \\
    Sq^{2n+1}([H]_{mod\, 2})
  }
  \,.
$$

=--

This was first observed in ([Gomi 08](#Gomi08)). Streamlined proofs are given in ([Bunke 12, propblem 3.106](#Bunke12), [Grady-Sati 16, prop. 22](#GradySati16)).



## Related concepts

* [[Steenrod squares]], [[cohomology operation]]

* [[Bockstein spectral sequence]]

## References

Original references include

* [[Meyer Bockstein]],  

  _Universal systems of $\nabla$-homology rings_, C. R. (Doklady) Acad. Sci. URSS (N.S.) 37 (1942), 243&#8211;245, MR0008701

  _A complete system of fields of coefficients for the $\nabla$-homological dimension_ ,  C. R. (Doklady) Acad. Sci. URSS (N.S.) (1943),  38: 187&#8211;189, MR0009115

* [[Meyer Bockstein]],  _Sur la formule des coefficients universels pour les groupes d'homologie_ ,  Comptes Rendus de l'acad&#233;mie des Sciences. S&#233;rie I. Math&#233;matique (1958),  247: 396&#8211;398, MR0103918

The relation to the [[Beilinson-Deligne cup product]] is discussed in

* {#Gomi08} [[Kiyonori Gomi]], _Differential  characters  and  the  Steenrod  squares_, In Groups of diffeomorphisms, volume 52 of Adv. Stud. Pure Math., pages 297?308. Math. Soc. Japan, Tokyo, 2008

* {#Bunke12} [[Ulrich Bunke]], problem 3.106 in _Differential cohomology_ ([arXiv:1208.3961](https://arxiv.org/abs/1208.3961))


* [[Daniel Grady]], [[Hisham Sati]], prop. 22 in: _Primary operations in differential cohomology_, Adv. Math. 335 (2018), 519-562 ([arXiv:1604.05988](https://arxiv.org/abs/1604.05988), [doi:10.1016/j.aim.2018.07.019](https://www.sciencedirect.com/science/article/pii/S0001870818302676?via%3Dihub))

[[!redirects Bockstein homomorphisms]]
[[!redirects Bockstein morphism]]
[[!redirects Bockstein morphisms]]
[[!redirects Bockstein operation]]
[[!redirects Bockstein operations]]