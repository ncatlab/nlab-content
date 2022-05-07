
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _double dimensional reduction_ is a variant of [[Kaluza-Klein mechanism]] combined with [[fiber integration]] in the presence of [[branes]]: given a [[spacetime]] of [[dimension]] $d+1$ in which a $p+1$-[[brane]] propagates, its KK-reduction results in a $d$-dimensional effective spacetime containing a $p+1$-brane together with a "doubly reduced" $p$-brane, which is the reduction of those original $(p+1)$-brane configurations that [[wrapped brane|wrapped]] the cycle along which the KK-reduction takes place.

## Definition
 {#Definition}

### Via fiber integration in ordinary differential cohomology



Let $\mathbf{H}$ be the [[smooth infinity-groupoid|smooth topos]]. For $p+1 \in \mathbb{N}$ write $\mathbf{B}^{p+1}U(1)_{conn} \in \mathbf{H}$ for the universal [[moduli stack]] of [[circle n-bundles with connection]] (given by the [[Deligne complex]]). 

Notice that [[fiber integration in ordinary differential cohomology]] has the following stacky incarnation (see [here](fiber+integration+in+ordinary+differential+cohomology#ViaSmoothHomotopyType)):

+-- {: .num_prop}
###### Proposition

For $\Sigma$ an [[orientation|oriented]] [[closed manifold]] of [[dimension]] $k \leq p+1$, then [[fiber integration]] in [[ordinary differential cohomology]] is reflected by a morphism of the form

$$
  \array{
    [\Sigma, \mathbf{B}^{p+1}U(1)_{conn}]
    &\stackrel{\int_\Sigma}{\longrightarrow}&
    \mathbf{B}^{p+1-k}U(1)_{conn}
    \\
    \downarrow^{[\Sigma,curv]} && \downarrow^{curv}
    \\
    [\Sigma,\mathbf{\Omega}^{p+2}]
    &\stackrel{\int_\Sigma}{\longrightarrow}&
    \mathbf{\Omega}^{p+2-k}
  }
  \,,
$$

where the vertical morphisms are the [[curvature]] maps and the bottom morphims reflects ordinary [[fiber integration]] of [[differential forms]].

=--

+-- {: .num_defn #DoubleDimensionalReductionForDifferentialCocycles}
###### Definition

Given a [[cocycle]] 

$$
  \nabla \;\colon\; X \times \Sigma \longrightarrow \mathbf{B}^{p+1}U(1)_{conn}
  \,,
$$

on the [[Cartesian product]] of some [[smooth space]] $X$ with $\Sigma$, then its _double dimensional reduction_ is the cocycle on $X$ which is given by the composite

$$
  X \longrightarrow [\Sigma, X \times \Sigma]
  \stackrel{[\Sigma,\nabla]}{\longrightarrow}
  [\Sigma,\mathbf{B}^{p+1}U(1)_{conn}]
  \stackrel{\int_\Sigma}{\longrightarrow}
  \mathbf{B}^{p+1-k}U(1)_{conn}
  \,,
$$

where the first morphism is the [[unit of an adjunction|unit]] of the ([[Cartesian product]] $\dashv$ [[internal hom]])-[[adjunction]].

=--

### Via cyclic loop spaces
 {#ViaCyclicLoopSpaces}

We discuss here a formalization of double dimensional reduction via cyclification adjunction ([FSS 16, section 3](#FSS16), [BMSS 18, section 2.2](#BMSS18)). For more see at _[[geometry of physics -- fundamental super p-branes]]_ the _[section on double dimensional reduction](geometry+of+physics+--+fundamental+super+p-branes#DoubleDimensionalReduction)_.

+-- {: .num_prop #GeneralReduction}
###### Proposition

Let $\mathbf{H}$ be any  [[(∞,1)-topos]] and let $G$ be an [[∞-group]] in $\mathbf{H}$. Then the right [[base change]]/[[dependent product]] along the canonical point inclusion $\ast \to \mathbf{B}G$ into the [[delooping]] of $G$ takes the following form: There is a pair of [[adjoint ∞-functors]] of the form

$$
  \mathbf{H}
    \underoverset
      {\underset{[G,-]/G}{\longrightarrow}}
      {\overset{hofib}{\longleftarrow}}
      {\bot}
  \mathbf{H}_{/\mathbf{B}G}
  \,,
$$


where

* $[G,-]$ denotes the [[internal hom]] in $\mathbf{H}$,

* $[G,-]/G$ denotes the [[homotopy quotient]] by the [[conjugation action|conjugation]] [[∞-action]] for $G$ equipped with its canonical [[∞-action]] by left multiplication and the argument
regarded as equipped with its trivial $G$-$\infty$-action (for $G = S^1$ the [[circle group]] this is the [[cyclic loop space]] construction).

Hence for

* $\hat X \to X$ a $G$ [[principal ∞-bundle]]

* $A$ a [[coefficient]] object, such as for some [[differential cohomology|differential]] [[generalized cohomology theory]]

then there is a [[natural equivalence]]


$$
  \underset{
    \text{original} \atop \text{fluxes}
  }{
  \underbrace{
    \mathbf{H}(\hat X\;,\; A)
  }
  }
    \;\;
    \underoverset
      {\underset{oxidation}{\longleftarrow}}
      {\overset{reduction}{\longrightarrow}}
      {\simeq}
    \;\;
  \underset{
     \text{doubly} \atop { \text{dimensionally reduced} \atop \text{fluxes} }
  }{
  \underbrace{
    \mathbf{H}_{/\mathbf{B}G}(X \;,\; [G,A]/G)
  }
  }
$$

given by

$$
  \left(
     \hat X \longrightarrow A
  \right)
  \;\;\;
    \leftrightarrow
  \;\;\;
  \left(
    \array{
       X && \longrightarrow && [G,A]/G
       \\
       & \searrow && \swarrow
       \\
       && \mathbf{B}G
    }
  \right)
$$

=--

+-- {: .proof #DimensionalReductionAbstractly}
###### Proof


First observe that the [[conjugation action]] on $[G,X]$ is the [[internal hom]] in
the [[(∞,1)-category]] of $G$-[[∞-actions]] $Act_G(\mathbf{H})$.
Under the [[equivalence of (∞,1)-categories]]

$$
  Act_G(\mathbf{H}) \simeq \mathbf{H}_{/\mathbf{B}G}
$$

(from [NSS 12](geometry+of+physics+-+fundamental+super+p-branes#NSS12)) then $G$ with its canonical [[∞-action]] is $(\ast \to \mathbf{B}G)$
and $X$ with the trivial action is $(X \times \mathbf{B}G \to \mathbf{B}G)$.

Hence

$$
  [G,X]/G
    \simeq
  [\ast, X \times \mathbf{B}G]_{\mathbf{B}G}
  \;\;\;\;\;
  \in
   \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

Actually, this is the very definition of what $[G,X]/G \in \mathbf{H}_{/\mathbf{B}G}$ is to mean in the first place, abstractly.

But now since the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G}$ is itself [[cartesian closed (infinity,1)-category|cartesian closed]], via

$$
  E \times_{\mathbf{B}G}(-)
  \;\;\;
   \dashv
  \;\;\;
  [E,-]_{\mathbf{B}G}
$$

it is immediate that
there is the following sequence of [[natural equivalences]]

$$
  \begin{aligned}
   \mathbf{H}_{/\mathbf{B}G}(Y, [G,X]/G)
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(Y, [\ast, X \times \mathbf{B}G]_{\mathbf{B}G})
   \\
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(
     Y \times_{\mathbf{B}G} \ast,
     \underset{p^\ast X}{\underbrace{X \times \mathbf{B}G }}
  )
  \\
  & \simeq
  \mathbf{H}(
     \underset{hofib(Y)}{\underbrace{p_!(Y \times_{\mathbf{B}G} \ast)}},
     X
  )
  \\
  & \simeq
  \mathbf{H}(hofib(Y),X)
  \end{aligned}
$$

Here $p \colon \mathbf{B}G \to \ast$ denotes the terminal morphism and $p_! \dashv p^\ast$
denotes the [[base change]] along it.


=--




## Examples

### Reduction on the circle
 {#ReductionOnTheCircle}

+-- {: .num_example #ReductionOnTheCircle}
###### Example

When $\Sigma = S^1$ is the [[circle]], and we think of $X \times S^1$ as a [[spacetime]] of [[11-dimensional supergravity]], then $\nabla \colon X \times S^1 \to \mathbf{B}^3 U(1)_{conn}$ may represent the [[supergravity C-field]] as a cocycle in ordinary differential cohomology. Then its double dimensional reduction in the sense of def. \ref{DoubleDimensionalReductionForDifferentialCocycles} is the differential cocycle representing the [[B-field]] on $X$, in the sense of [[string theory]].

=--

+-- {: .num_remark #Cyclotomic}
###### Remark

For $\Sigma = S^1$ a circle as in example \ref{ReductionOnTheCircle}, then the morphism $X \longrightarrow [\Sigma, X \times \Sigma]$ in def. \ref{DoubleDimensionalReductionForDifferentialCocycles} sends each point of $X$ to the loop in $X\times S^1$ that winds identically around the copy of $S^1$ at that point. Hence in this case it would make sense to consider, more generally, for each $p \in \mathbb{Z}$ the "order $p$" double dimensional reduction, given by the operation where one instead considers the map that lets the loop wind $p$ times around the $S^1$.

The resulting double dimensional reduction is just $p$-times the original one, so in a sense nothing much is changed, but maybe it is suggestive that now we are looking at the space of $C_p$-[[fixed points]] of the [[free loop space]] (for $C_p$ the [[cyclic group]] of order $p$). In [[E-infinity geometry]] this fixed-point structure on the [[free loop spaces]] makes the derived function algebras -- the [[topological Hochschild homology]] of the original function algebras -- be [[cyclotomic spectra]].

=--



### For general super $p$-branes

Double dimensional reduction for the super-$p$-[[branes]] in $D$ dimensions which are described by the [[Green-Schwarz action functional]] corresponds to moving down and left the diagonals in the brane scan table of consistent such branes:

[[branescan.gif:pic]]

In particular 

* the [[superstring]] of [[type IIA string theory]] appears as the double dimensional reduction of the [[M2-brane]] in the [[KK-compactification]] from [[11-dimensional supergravity]]/[[M-theory]] down to 10-dimensional [[type II supergravity]]/[[type II string theory]]. 

* the [[D4-brane]] appears as the double dimensional reduction of the [[M5-brane]] under this process;

* the double dimensional reduction of the [[super 2-brane in 4d]] is [[super 1-brane in 3d]] (see there).

### From M-branes to F-branes

* [[duality between M-theory and type IIA string theory]]

[[!include F-branes -- table]]

## Related concepts

* [[cyclic loop space]], [[cyclic loop stack]]

* [[caloron correspondence]]

## References
 {#References}

Formalization of double dimensional reduction is discussed in [[rational homotopy theory]] in

* {#FSS16} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 3 of  _[[schreiber:T-Duality from super Lie n-algebra cocycles for super p-branes]]_, ATMP Volume 22 (2018) Number 5 ([arXiv:1611.06536](https://arxiv.org/abs/1611.06536))

and in full [[homotopy theory]] in

* {#BMSS18} [[Vincent Braunack-Mayer]], [[Hisham Sati]], [[Urs Schreiber]], Section 2.2 of:  _[[schreiber:Gauge enhancement of Super M-Branes|Gauge enhancement of Super M-Branes via rational parameterized stable homotopy theory]]_, Communications in Mathematical Physics 371: 197 (2019) ([arXiv:1806.01115](https://arxiv.org/abs/1806.01115), [doi:10.1007/s00220-019-03441-4](https://doi.org/10.1007/s00220-019-03441-4))

Exposition is in

* {#Schreiber16} [[Urs Schreiber]], [Section 4](https://ncatlab.org/schreiber/show/Super+Lie+n-algebra+of+Super+p-branes#DoubleDimensionalReduction) of _[[schreiber:Super Lie n-algebra of Super p-branes]]_, talks at [Fields, Strings, and Geometry Seminar](http://www.surrey.ac.uk/maths/news/seminars/fsg/), Surrey, 5th-9th Dec. 2016

and further discussion in 

* {#Alfonsi19} [[Luigi Alfonsi]], _Global Double Field Theory is Higher Kaluza-Klein Theory_, Fortsch. d. Phys. 2020 ([arXiv:1912.07089](https://arxiv.org/abs/1912.07089), [doi:10.1002/prop.202000010](https://doi.org/10.1002/prop.202000010))

* [[Luigi Alfonsi]], _The puzzle of global Double Field Theory: open problems and the case for a Higher Kaluza-Klein perspective_ ([arXiv:2007.04969](https://arxiv.org/abs/2007.04969))


### Reduction of membrane to string

The concept of double dimensional reduction was introduced, for the case of the reduction of the [[supermembrane]] in 11d to the [[Green-Schwarz superstring]] in 10d, in

* {#DuffHoweInamiStelle87} [[Michael Duff]], [[Paul Howe]], T. Inami, [[Kellogg Stelle]], _Superstrings in $D=10$ from Supermembranes in $D=11$_, Phys. Lett. B191 (1987) 70 and in [[Michael Duff]] (ed.) _[[The World in Eleven Dimensions]]_ 205-206 (1987) ([spire:245249](http://inspirehep.net/record/245249))

The above "brane scan" table showing the double dimensional reduciton pattern of the super-$p$-branes given by the [[Green-Schwarz action functional]] (see there for more references on this) is taken from 

* {#Duff} [[Michael Duff]], _Supermembranes: the first fifteen weeks_ CERN-TH.4797/87 (1987) ([scan](http://ccdb4fs.kek.jp/cgi-bin/img/allpdf?198708425))
 



### Reduction of M5-brane to D4-brane

The [[double dimensional reduction]] of the [[M5-brane]] to the [[D4-brane]]:

* [[Paul Townsend]], _D-branes from M-branes_, Phys. Lett. B373 (1996) 68-75 ([arXiv:hep-th/9512062](https://arxiv.org/abs/hep-th/9512062))

* {#APPS97a} [[Mina Aganagic]], [[Jaemo Park]], Costin Popescu, [[John Schwarz]], Section 6 of _World-Volume Action of the M Theory Five-Brane_, Nucl.Phys. B496 (1997) 191-214 ([arXiv:hep-th/9701166](http://arxiv.org/abs/hep-th/9701166))

* {#APPS97b} [[Mina Aganagic]], [[Jaemo Park]], Costin Popescu, [[John Schwarz]], Section 6 of _Dual D-Brane Actions_, Nucl. Phys. B496 (1997) 215-230 ([arXiv:hep-th/9702133](https://arxiv.org/abs/hep-th/9702133))

* [[Neil Lambert]], Constantinos Papageorgakis, Maximilian Schmidt-Sommerfeld, _M5-Branes, D4-Branes and Quantum 5D super-Yang-Mills_, JHEP 1101:083 (2011) ([arXiv:1012.2882](http://arxiv.org/abs/1012.2882))

* {#Witten11} [[Edward Witten]], _Fivebranes and Knots_ ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216)) 
 
### Reduction of M-Waves and MK6s

* [[José Figueroa-O'Farrill]], [[Joan Simón]], _Supersymmetric Kaluza-Klein reductions of M-waves and MKK-monopoles_, Class. Quant. Grav.19:6147-6174, 2002 ([arXiv:hep-th/0208108](https://arxiv.org/abs/hep-th/0208108))

### Reduction of black M2s and black M5s

* [[José Figueroa-O'Farrill]], [[Joan Simón]], _Supersymmetric Kaluza-Klein reductions of M2 and M5-branes_, Adv. Theor. Math. Phys. 6:703-793, 2003 ([arXiv:hep-th/0208107](https://arxiv.org/abs/hep-th/0208107))

[[!redirects double dimensional reductions]]

[[!redirects double dimensional reduction]]
