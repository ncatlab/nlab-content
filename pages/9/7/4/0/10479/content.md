
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Differential algebraic K-theory is the [[differential cohomology]]-refinement of [[algebraic K-theory]].

In ([Bunke-Tamme 12](#BunkeTamme12)) this is realized effectively as the [[schreiber:differential cohomology in a cohesive topos]] of the [[tangent (∞,1)-topos]] of the [[cohesive (∞,1)-topos]]

$$
  \mathbf{H} \coloneqq Sh_\infty\left(SmthMfd, \mathbf{B} \right)
  \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  \mathbf{B}
$$

of [[∞-stacks]] on the [[site]] of [[smooth manifolds]] with values in turn in [[∞-stacks]]  over a [[site]] of [[arithmetic schemes]], hence by [[smooth ∞-groupoids]] but over a [[base (∞,1)-topos]] 

$$
  \mathbf{B}
  \coloneqq
  Sh_\infty\left(Sch_{\mathbb{Z}}\right)
$$ 

of algebraic [[∞-stacks]].

This may be regarded as sitting inside the [[smooth E-∞-groupoids]].

It is observed in this context that the [[Beilinson regulator]] in [[algebraic K-theory]] is naturally understood as a [[Chern character]] in this perspective of [[differential cohomology]] ([Bunke-Tamme 12](#BunkeTamme12)), which helps with studying it.



## Definition

### Absolute Hodge cohomology

+-- {: .num_defn #HodgeComplexOverComplexNumbers}
###### Definition

Write 

$$
  \Omega^\bullet_{\mathbb{C}} \in Stab(Sh_\infty(Sch_{\mathbb{C}}))
$$

for the [[chain complex]] of [[abelian sheaves]] (regarded as a [[sheaf of spectra]] under the [[stable Dold-Kan correspondence]]) which computes [[absolute Hodge cohomology]] of [[complex varieties]].

=--

([Bunke-Tamme 12, section 3.1](#BunkeTamme12))

+-- {: .num_defn #HodgeComplexOverIntegers}
###### Definition

Write 

$$
  \Omega^\bullet_{\mathbb{Z}} \coloneqq compl^\ast \Omega^\bullet_{\mathbb{C}} \in Stab(\mathbf{B})
$$

for the [[inverse image]] of $\Omega^\bullet_{\mathbb{C}}$ under the [[base change]] given by

$$
  compl
  \coloneqq
  (-)\times_{\mathbb{Z}}Spec(\mathbb{C}) 
  \;\colon\; 
  Sch_{\mathbb{Z}}\longrightarrow Sch_{\mathbb{C}}
  \,.
$$


=--

([Bunke-Tamme 12, section 3.2](#BunkeTamme12))

There is a resolution of 
$\Omega^\bullet_{\mathbb{Z}} \in Stab(\mathbf{B}) \stackrel{Disc}{\hookrightarrow} Stab(\mathbf{H})$ by a sheaf of complexes of differential forms on smooth manifolds tensored with $\Omega^\bullet_{\mathbb{Z}}$

$$
  \Omega^\bullet \in Stab(\mathbf{H})
$$

([Bunke-Tamme 12, (47)](#BunkeTamme12)).

+-- {: .num_defn #CyclesForHodgeComplexOverComplexNumbers}
###### Definition

While $\Omega^\bullet \simeq \Omega^\bullet_{\mathbb{Z}}$, below we use the chain-level truncation $\Omega^{\bullet \geq 0}$ which is no longer in the image of $Disc$, hence no longer a [[flat modality]]-[[modal type]].

=--


### Algebraic K-theory sheaf of spectra
 {#AlgebraicKTheorySheafOfSpectra}

Write 

$$
  \mathbf{Vect}_{lc} \in \mathbf{H}
$$

for the [[stack]] which to $X\times S \in SmthMfd \times Sch_{\mathbb{Z}}$ assigns the groupoid of locally free and locally finitely generated $pr_S^\ast \mathcal{O}_S$-[[modules]] (modules over the [[inverse image]] of the [[structure sheaf]] of $S$ under the [[projection]] map $X \times S \to S$).

This is a [[commutative monoid]] object with respect to [[direct sum]]. Write

$$
  K \coloneqq \mathcal{K}(\mathbf{Vect}_{lc}^{\oplus})
$$

for the stackification of the objectwise [[K-theory of a symmetric monoidal (∞,1)-category]]-construction.

This is the ordinary [[algebraic K-theory]] of [[schemes]], as in ([Thomason-Trobaugh 90](#ThomasonTrobaugh90)) ([Bunke-Tamme 12, section 3.3](#BunkeTamme12)), see at _[algebraic K-theory -- as the K-theory of algebraic vector bundles](algebraic%20K-theory#AsTheKTheoryOfAlgebraicVectorBundles)_.


### The refined Beilinson regulator
 {#RefinedBeilinsoRegulator}

There is a refinement of the [[Beilinson regulator]] to a smoothly parameterized version $\mathbf{K}$ of [[algebraic K-theory]]:

+-- {: .num_defn #TheBeilinsonRegulator}
###### Definition

(...)

$$
  r^{Beil} 
  \;\colon\;
  K 
    \longrightarrow
  \Omega^\bullet_{\mathbb{Z}}
$$

=--

As a homomorphism of [[spectrum objects]] this is ([Bunke-Tamme 12, def. 4.26](#BunkeTamme12)). As a homomorphism of [[E-∞ ring]] objects, this is ([Bunke-Tamme 13, def. 2.18](#BunkeTamme13)).

### Differential algebraic K-theory

Recall the discussion at _[[differential cohomology hexagon]]_.

+-- {: .num_defn #HodgeComplexOverComplexNumbers}
###### Definition

_Differential algebraic K-theory_ is the [[homotopy fiber product]]

$$
  \hat K \coloneqq K \underset{\Omega^\bullet}{\times} \Omega^{\bullet \geq 0}  \in Stab(\mathbf{H})
$$

of the inclusion of the non-negative degree truncation of the de Rham resolution of the absolute Hodge complex, def. \ref{CyclesForHodgeComplexOverComplexNumbers}, with the refined Beilinson regulator, def. \ref{TheBeilinsonRegulator}

$$
  \array{
    \hat K &\longrightarrow& \Omega^{\bullet \geq 0}
    \\
    \downarrow &(pb)& \downarrow
    \\
    K &\underset{r^{Beil}}{\longrightarrow}& \Omega^\bullet
  }
  \,.
$$

=--

([Bunke-Tamme 12, def. 5.1](#BunkeTamme12), [Bunke-Tamme 13, def. 3.1](#BunkeTamme13)).




## Applications

* differential refinement of [[Becker-Gottlieb transfer]] and its image under [[Borel regulators]]. See at _[[transfer index conjecture]]_.

## Related concepts

* [[differential K-theory]]

* [[differential form with logarithmic singularities]]

## References

Differential algebraic K-theory as above is introduced with application to [[higher regulator|higher]] [[Beilinson regulators]] in:

* {#BunkeTamme12} [[Ulrich Bunke]], [[Georg Tamme]], _Regulators and cycle maps in higher-dimensional differential algebraic K-theory_, Advances in Mathematics Volume 285, 5 November 2015, Pages 1853-1969
([arXiv:1209.6451](http://arxiv.org/abs/1209.6451), [doi:10.1016/j.aim.2015.08.004](https://doi.org/10.1016/j.aim.2015.08.004))
 
* [[Ulrich Bunke]], [[David Gepner]], _Differential function spectra, the differential Becker-Gottlieb transfer, and applications to differential algebraic K-theory_, Memoirs of the American Mathematical Society 2021 ([arXiv:1306.0247](http://arxiv.org/abs/1306.0247), [ISBN:978-1-4704-4685-7](https://bookstore.ams.org/cdn-1608276327798/memo-269-1316/))

* {#BunkeTamme13} [[Ulrich Bunke]], [[Georg Tamme]], _Multiplicative differential algebraic K-theory and applications_,  Ann. K-Theory 1(3): 227-258 (2016)   ([arXiv:1311.1421](http://arxiv.org/abs/1311.1421), [doi:10.2140/akt.2016.1.227](https://doi.org/10.2140/akt.2016.1.227))

Relevant references in ordinary [[algebraic K-theory]] include

* {#ThomasonTrobaugh90} [[Robert Thomason]] and Thomas Trobaugh, _Higher algebraic K-theory of schemes and of derived categories_, The Grothendieck Festschrift, Vol. III, Progr. Math., vol. 88, Birkhauser Boston, Boston, MA, 1990, pp. 247-435. MR 1106918 (92f:19001)
 

[[!redirects differential algebraic K-theory]]

[[!redirects differential algebraic K-theories]]

[[!redirects differential algebraic K-theories]]