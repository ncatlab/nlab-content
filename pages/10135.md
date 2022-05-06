
> under construction

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
  \pi_0 \mathbf{H}_{/\mathbf{B}G_{glob}}
  \big(
    \mathcal{X}, \mathcal{A}
  \big)
  \,.
\]

Cocycles in this "global equivariant" cohomology are then such that on each  chart of the form $U_i \sslash G_i$ they restrict to cocycles in $G_i$-[[equivariant cohomology]] of $U_i$, in a way that is compatible with the above re-identifications (eq:EquivalenceOfOrbifolds).

(...)

(...)



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

