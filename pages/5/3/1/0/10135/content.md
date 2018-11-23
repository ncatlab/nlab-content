
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

On general grounds, since [[orbifolds]] $\mathcal{X}$ are special cases of [[stacks]] ([[topological stacks]], [[differentiable stacks]], ...), there is an evident definition of [[cohomology]] of (i.e. on) orbifolds, given by forming ([[stable homotopy group|stable]]) [[homotopy groups]] of [[derived hom-spaces]] 

$$
  H^\bullet(\mathcal{X}, A)
  \;\coloneqq\;
  \pi_\bullet \mathbf{H}( \mathcal{X}, A )
$$

into any desired [[coefficient]] [[∞-stack]] (or [[sheaf of spectra]]) $A$.

More specifically, often one is interested in viewing orbifold cohomology as a variant of [[Bredon cohomology|Bredon]] [[equivariant cohomology]], based on the idea that the [[cohomology]] of a global [[homotopy quotient]] orbifold 


\[
  \label{GlobalQuotientOrbifold}
  \mathcal{X} 
    \;\simeq\; 
  X \sslash G
\] 

for a given $G$-[[action]] on some [[manifold]] $X$, should coincide with the $G$-[[equivariant cohomology]] of $X$. However, such an identification (eq:GlobalQuotientOrbifold) is not unique: For $G \subset K$ any closed [[subgroup]], we have an [[equivalence in an (∞,1)-category|equivalence]] of [[stacks]]

\[
  \label{EquivalenceOfOrbifolds}
  X \sslash G
  \;\simeq\;
  \big( X \times_G K \big) \sslash K
  \,.
\]

(This issue was maybe first highlighted in [Pronk-Scull 07, p. 1](#PronkScull07)).

This means that if one is to regard orbifold cohomology as a variant of [[Bredon cohomology|Bredon]] [[equivariant cohomology]], then one needs to work "globally" with respect to choices of [[isotropy groups]], in the sense of _[[global equivariant homotopy theory]]_, where one considers equivariance with respect to "all [[compact Lie groups]] at once", in a suitable sense. (This point is highlighted for instance in [Schwede 18, p. ix-x](#Schwede18).)

### In terms of stacks
 {#InTermsOfStacks}

We may make this more explicit in the case where one considers the class of orbifolds $\mathcal{X}$ whose [[isotropy groups]] are any [[finite group|finite]] [[subgroup]] $G \overset{\iota}{\hookrightarrow} G_{glob}$ of a fixed [[compact Lie group]] $G_{glob}$. Such orbifolds carry canonical morphisms to the [[delooping]] stack $\mathbf{B}G_{glob}$, which are locally, for global quotients $\mathcal{X} \simeq X \sslash G$, given by

$$
  \rho
  \;\colon\;
  X \sslash G 
    \overset{ (X \to \ast) \sslash G }{\longrightarrow} 
  \mathbf{B}G 
    \overset{ \mathbf{B} \iota }{\longrightarrow} 
  \mathbf{B}G_{glob}
$$

which is [[faithful functor|faithful]] (i.e. [[0-truncated morphism of an (∞,1)-category|0-truncated]]).

By the general discussion at _[[∞-action]]_ any such morphism exhibits an [[∞-action]] of $G_{glob}$ on the [[homotopy fiber]] $hofib(\rho)$ of $\rho$, together with an [[equivalence in an (∞,1)-category|equivalence]]

\[
  \label{GlobalHomotopyFiberOfOrbifold}
  hofib(\rho)\sslash G_{glob}
  \;\simeq\;
  X \sslash G
  \,.
\]

But that [[homotopy fiber]] is directly computed to be 

\[
  \label{HomotopyFiberOfGlobalQuotientExhibitedAsOrbifold}
  \begin{aligned}
    hofib(\rho) 
      & \simeq  
    \ast 
      \times_{\mathbf{B}G_{glob}} 
    \big( \mathbf{B}G_{glob} \big)^{\Delta[1]} 
      \times_{\mathbf{B}G_{glob}} 
    \left( X \sslash G\right)
    \\
    & \simeq \big( X \times G_{glob} \big) / G
    \\
    & \simeq
    X \times_G G_{glob}
    \,,
  \end{aligned}
  \;\;\;\;\;
  \left\{
  \;\;\;
  \array{
    && \ast
    \\
    & {}^{\mathllap{g_{glob}}}\swarrow && \searrow^{\mathrlap{ g_{glob} \cdot g }}
    \\
    \ast && \underset{ g }{\longrightarrow} && \ast
    \\
    x && \underset{g}{\longrightarrow} &&  g(x)
  }
  \;\;\;
  \right\}
\]

where in the first step we used the [[factorization lemma]], and the remaining steps follow by direct inspection. Plugging this back into (eq:GlobalHomotopyFiberOfOrbifold) yields the equivalence (eq:EquivalenceOfOrbifolds) for $G \hookrightarrow K \coloneqq G_{glob}$. 

In conclusion, if $\mathcal{X}$ is any [[orbifold]], i.e. not necessarily a global homotopy quotient $X_i \sslash G_i$, but locally of this form for each $G_i$ some finite subgroups of $G_{glob}$, then it comes with a canonical [[0-truncated morphism of an (∞,1)-category|0-truncated morphism]] of topological stacks $\mathcal{X} \overset{\rho}{\to} \mathbf{B}G_{glob}$, and so for $\mathcal{A} \overset{}{\to} \mathbf{B}G_{glob} $ any [[coefficient]] [[∞-stack]] in the [[slice (∞,1)-topos|slice]] over $\mathbf{B}G_{glob}$, we may take the global equivariant orbifold cohomology to be given by [[homotopy classes]] of morphisms in the [[slice (∞,1)-topos|slice]]:

\[
  \label{CocyclesInTheSlice}
  H_{glob}(\mathcal{X}, \mathcal{A} )
  \;\coloneqq\;
  \pi_0 \mathbf{H}_{/ \mathbf{B}G_{glob}}
  \big(
    \mathcal{X}, \mathcal{A}
  \big)
  \,.
\]

Cocycles in this "global equivariant" cohomology are then such that on each  chart of the form $U_i \sslash G_i$ they restrict to cocycles in $G_i$-[[equivariant cohomology]] of $U_i$, in a way that is compatible with the above re-identifications (eq:EquivalenceOfOrbifolds).

Notice that if also the [[coefficient]] $\mathcal{A} \overset{}{\to} \mathbf{B} G_{glob}$ is [[faithful functor|faithful]] ([[0-truncated morphism of an (∞,1)-category|0-truncated]]) as an object in the [[slice (∞,1)-topos|slice]], then, by the [[orthogonal factorization system|orthogonality]] of the [[(n-connected, n-truncated) factorization system]] for $n = 0$, there is a [[contractible space]] of [[homotopies]] $\phi$ in the data for a cocycle

$$
  \array{
    \mathcal{X} 
      && 
      \overset{ \phantom{AA} c \phantom{AA} }{\longrightarrow} && 
    \mathcal{A}
    \\
    & {}_{\mathllap{\rho}}\searrow &\swArrow_{\phi}& \swarrow_{\mathrlap{f}}
    \\
    && \mathbf{B}G_{glob}
  }
  \phantom{AAA}
  =
  \phantom{AAA}
  \array{
    \mathcal{X} 
      &\overset{ \phantom{A} c \phantom{A} }{\longrightarrow}& 
    \mathcal{A}
    \\
    {}^{=}\big\downarrow & \swArrow_{\exists !} & \big\downarrow{}^{\mathrlap{f}}
    \\
    \mathcal{X} 
      &\underset{ \phantom{A} \rho \phantom{A} }{\longrightarrow}&
    \mathbf{B}G_{glob}
  }
$$

Moreover, in this case the cocyle morphism $c$ itself is necessarily [[faithful functor|faithful]] ([[0-truncated morphism of an (∞,1)-category|0-truncated]]). This means that the [[full sub-(∞,1)-category]] of the [[slice (∞,1)-category]] on the [[0-truncated morphism of an (∞,1)-category|fatihful/0-truncated morphisms]] is equivalently the non-full sub $\infty$-category of the corresponding domain [[∞-stacks]], but with [[0-truncated morphism of an (∞,1)-category|fatihful/0-truncated morphisms]] between them:

\[
  \label{Faithful}
  \mathbf{H}_{/\mathbf{B}G_{glob}}
  \big(
    \mathcal{X}, \mathcal{A}
  \big)
  \;\simeq\;
  \mathbf{H}^{faith}
  \big(
    \mathcal{X}, \mathcal{A}
  \big)
  \,,
\]

which hence gives an equivalent description of the global equivariant orbifold cohomology in (eq:CocyclesInTheSlice) in this case.

Of course if $\mathcal{A} \to \mathbf{B}G$ is 0-truncated, this only give cohomology in degree 0. To get back to the full cohomology, observe that for [[n-localic (infinity,1)-topos|0-localic]] $\mathbf{H}$ (i.e. with a plain 1-categorical [[site]] of definition)  the previous argument generalizes immediately to the [[internal homs]]

$$
  [-,-]_{\mathbf{B}G}
  \;\colon\;
  \mathbf{H}^{op}_{/\mathbf{B}G} \times \mathbf{H}_{/\mathbf{B}G}
    \longrightarrow
  \mathbf{H}
$$

$$
  [-,-]
  \;\colon\;
  \mathbf{H}^{op} \times \mathbf{H}
    \longrightarrow
  \mathbf{H}
$$


as

\[
  \big[
    \mathcal{X}, \mathcal{A}
  \big]_{\mathbf{B}G}
  \;\simeq\;
  \big[
    \mathcal{X}, \mathcal{A}
  \big]^{faith}
  \,,
\]

From these then one re-obtains cohomology by applying the [[shape modality]]/[[shape via cohesive path ∞-groupoid|cohesive path ∞-groupoid]] $&#643;$.

$$
\begin{aligned}
  &#643;
  \big[
    \mathcal{X}, \mathcal{A}
  \big]_{/\mathbf{B}G}
  & \simeq
  &#643;
  \left(
    \big[
      \mathcal{X}, \mathcal{A}
    \big]^{faith}
  \right)
  \,,
\end{aligned}
$$


This perspective paves the way to the equivalent description in terms of systems of fixed point loci:

$\,$

### In terms of systems of fixed point loci
 {#InTermsOfSystemsOfFixedPointLoci}

A key point of [[global equivariant homotopy theory]] is to generalize [[Elmendorf's theorem]] to this global situation, and express maps between [[topological stacks]], as above, in terms of [[(∞,1)-presheaves]] of [[fixed point]]-loci parameterized over on a suitable [[orbit category]]. 

In [[global equivariant homotopy theory]] the plain [[orbit category]] $Orb_G$ used in $G$-[[equivariant cohomology|equivariant]] [[Bredon cohomology]] is replaced by the [[global orbit category]] $Orb_{glb}$ whose [[objects]] are the [[delooping]] [[stacks]] $\mathbf{B}G \coloneqq \ast\sslash G$ and whose morphisms are the [[faithful functor|faithful]]/[[0-truncated morphism of an (∞,1)-category|0-truncated]] morphisms between these. Then any [[stack]] $\mathcal{X}$ ([[orbifold]], [[orbispace]]) becomes an [[(∞,1)-presheaf]] $y \mathcal{X}$ over $Orb_{glb}$ by the evident "external [[Yoneda embedding]]"

$$
  y \mathcal{X}
  \;\coloneqq\;
  \Pi [ \mathbf{B}G, \mathcal{X}]^{faith}
  \,.
$$

([Henriques-Gepner 07, 4.1](#HenriquesGepner07), [Rezk 14, 4.5](#Rezk14))

Notice that, by the condition of faithfulness, a morphism of the form $\ast \to \mathbf{B}G \to \mathcal{X}$ necessarily hits a $G$-[[fixed point]] of $\mathcal{X}$, i.e. a point whose [[isotropy group]] contains $G$. In this sense $y \mathcal{X}$ is the _global system of fixed point loci_ of $\mathcal{X}$.


The generalization of [[Elmendorf's theorem]] to global equivariant homotopy theory, hence to the application of orbifold cohomology, is now the statement that this construction induces [[equivalence in an (∞,1)-category|equivalences]] of cocycle [[∞-groupoids]]

\[
  \label{GlobalElmendorfTheorem}
  \Pi
  [ 
    \mathcal{X}, \mathcal{A}
  ]^{faith}
  \;\simeq\;
  PSh_{\infty}(Orb_{glb}) ( y \mathcal{X}, y \mathcal{X} )
  \,.
\]

This is the statement of [Henriques-Gepner 07, main theorem (4) on p. 5 in version (2) according to p. 8](#HenriquesGepner07).
With particular emphasis on its application to orbifold cohomology, this is highlighted in ([Schwede 17, Introduction](#Schwede17), [Schwede 18, p. ix-x](#Schwede18)). See also [Rezk 14, section 4](#Rezk14).

In summary, under the _Gepner-Henriques global Elmendorf theorem_, the definition of global equivariant orbifold cohomology according to (eq:CocyclesInTheSlice) becomes equivalent, via (eq:Faithful) and (eq:GlobalElmendorfTheorem), to the cohomology in  the [[(∞,1)-topos]] over the [[global orbit category]]

$$
  H(\mathcal{X}, \mathcal{A})
  \;\;\simeq\;\;
  \pi_0
  PSh_\infty(Orb_{glb})( y\mathcal{X}, y \mathcal{A} )
  \,.
$$




## Related concepts

* [[orbifold]]

* [[Gromov-Witten theory]]


History

According to [Abramovich 05, p. 42](#Abramovich05):

> On December 7, 1995 [[Maxim Kontsevich]] delivered a history-making lecture at Orsay, titled _String Cohomology_. This is what is now know, after [Chen-Ruan 00](#ChenRuan00), as _orbifold cohomology_, Kontsevich's lecture notes described the orbifold and  [[quantum cohomology]] of a global quotient [[orbifold]]. Twisted sectors, the age grading, and a version of orbifold stable maps for global quotients are all there.

The same lecture also introduced _[[motivic integration]]_.

## References
 
Discussion of orbifold cohomology in the context of [[Bredon cohomology|Bredon]]/[[global equivariant homotopy theory|global]] [[equivariant cohomology]] includes

* {#PronkScull07} [[Dorette Pronk]], [[Laura Scull]], _Translation Groupoids and Orbifold Bredon Cohomology_, Canad. J. Math. 62(2010), 614-645 ([arXiv:0705.3249](https://arxiv.org/abs/0705.3249), [doi:10.4153/CJM-2010-024-1](https://doi.org/10.4153/CJM-2010-024-1))


* {#Schwede17} [[Stefan Schwede]], _Orbispaces, orthogonal spaces, and the universal compact Lie group_ ([arXiv:1711.06019](https://arxiv.org/abs/1711.06019))

* {#Schwede18} [[Stefan Schwede]], _[[Global homotopy theory]]_, New Mathematical Monographs, 34 Cambridge University Press, 2018
([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

related to results of

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_, 2014



See also

* {#ChenRuan00} Weimin Chen, [[Yongbin Ruan]], _A New Cohomology Theory for Orbifold_, Commun. Math. Phys. 248 (2004) 1-31 ([arXiv:math/0004129](http://arxiv.org/abs/math/0004129))
 
* {#Abramovich05} [[Dan Abramovich]], _Lectures on Gromov-Witten invariants of orbifolds_ ([arXiv:math/0512372](http://arxiv.org/abs/math/0512372))


[[!redirects orbifold cohomologies]]

[[!redirects orbifold cohomology group]]
[[!redirects orbifold cohomology groups]]

[[!redirects orbispace cohomology]]
[[!redirects orbispace cohomologies]]

[[!redirects orbispace cohomology group]]
[[!redirects orbispace cohomology groups]]

