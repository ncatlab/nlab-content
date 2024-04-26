
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
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

In general, a _Freund-Rubin compactification_ &lbrack;[Freund & Rubin 1980](#FreundRubin80)&rbrack; is a [[Kaluza-Klein compactification]] of a theory of [[gravity]] coupled to ([[higher gauge field|higher]]) [[gauge fields]] with [[flux]] ([[field strength]]) on the compact [[fiber]] spaces such that the result is stable (a basic example of [[moduli stabilization]] via [[flux compactification]]).

One example are [[Kaluza-Klein compactifications]] of 6d [[Einstein-Maxwell theory]] with [[magnetic flux]] on a 2-dimensional [[fiber]] space ([[sphere]] or [[torus]]) ([RDSS 83](#RDSS83)). This serves these days as a toy example for [[flux compactifications]] and [[moduli stabilization]] in [[string theory]].
 
In the [[string theory]] literature often _the Freund-Rubin compactification_ refers by default to a [[Kaluza-Klein mechanism|Kaluza-Klein compactification]] of [[11-dimensional supergravity]] on a [[manifold]] $X_7$  of [[dimension]] 7 (in the original [[model (in theoretical physics)|model]] a round [[7-sphere]]) with non-vanishing constant 4-form [[field strength]] ("flux") of the [[supergravity C-field]] in the remaining four dimensional [[anti-de Sitter spacetimes]] $AdS_4$ (see also at *[[super AdS spacetime]]*).

If $X_7$ has [[weak G2 holonomy]] with weakness parameter/[[cosmological constant]] $\lambda$ the scale of the flux, then this yields $N = 1$ [[supersymmetry]] in the [[effective QFT]] in four dimensions, discussed at _[[M-theory on G2-manifolds]]_. The [[KK-reduction]] on the circle fiber of these solutions to [[type IIA supergravity]] yields type IIA sugra on [[complex projective space]] $\mathbb{C}P^3$ ([Nilsson-Pope 84](#NilssonPope84), [ABJM 08](#ABJM08))

If $X_7 = S^7/G_{ADE}$ is an [[orbifold]] of the round [[7-sphere]] by an finite group $G_{ADE} \subset SU(2)$ in the [[ADE-classification]], then Freund-Rubin describes the [[near horizon geometry]] of coincident black [[M2-branes]] at an [[ADE-singularity]], see at _[M2-brane -- As a black brane](M2-brane#AsABlackBrane)_.

## Details
 {#Details}

Consider a $D \geq 3$-dimensional spacetime which is the [[product manifold|product]] 

$$
  X^{(D)} \;=\; X^{(s)} \times Y^{(D-s)}
$$

of 

1. a [[Lorentzian manifold]] $X^{(s)}$, for $2 \leq s \leq D-2$, 

1. a [[Riemannian manifold]] $Y^{(D-s)}$, 

and assume that both factors are [[Einstein manifolds]] by themselves, in that their [[Ricci tensors]] are of the form

$$
  \begin{array}{l}
    Ric_{a b}
    \;=\;
    \tfrac
      {\mathrm{R}_s}
      {s}
    \, 
    \eta_{a b}
    \\
    Ric_{i j}
    \;=\;
    \tfrac
      {\mathrm{R}_{D-s}}
      {D-s}
    \,
    \delta_{i j}
    \,.
  \end{array}
$$

for $\mathrm{R}_s, \mathrm{R}_{D-s} \,\in\, \mathbb{R}$, to be determined.

Then the total [[scalar curvature]] $\mathrm{R} \equiv g^{\mu \nu} Ric_{\mu \nu}$ is

$$
  \mathrm{R}
  \;=\;
  \mathrm{R}_s + \mathrm{R}_{D-s}
  \,,
$$

and the non-vanishing components of the [[Einstein tensor]] $G \equiv Ric - \tfrac{1}{2}\mathrm{R}g$ are

$$
  \begin{array}{l}
    G_{a b}
    \;=\;
    \Big(
      \big(\tfrac{1}{s} - \tfrac{1}{2}\big)
      \mathrm{R}_s
      -
      \tfrac{1}{2} 
      \mathrm{R}_{D-2}
    \Big)
    \,
    \eta_{a b}
    \\
    G_{i j}
    \;=\;
    \Big(
      -\tfrac{1}{2}
      \mathrm{R}_s
      +
      \big(
        \tfrac{1}{D-s}
        -
        \tfrac{1}{2}
      \big)
      \mathrm{R}_{D-2}
    \Big)
    \,
    \delta_{i j}
    \,.
  \end{array}
$$

Next assume that the "matter" content is that of a [[higher gauge field]] with degree-$s$ [[flux density]] homogeneously extended over $X^{(s)}$:

$$
  F_{a_1 \cdots a_s}
  \;\equiv\;
  f\,
  \epsilon_{a_1 \cdots a_s}
$$

for some $f \in \mathbb{R}$, and all other components vanishing.

Then the [[stress-energy tensor]] 

$$
  T_{\mu \nu}
  \;=\;
  \big(
    \tfrac{1}{2s}
    F_{\mu_1 \cdots \mu_s}
    F^{\mu_1 \cdots \mu_s}
    \,
    g_{\mu \nu}
    -
    F_{\mu \, \mu_1 \cdots \mu_{s-1}}
    F_{\nu}{}^{ \mu_1 \cdots \mu_{s-1} }
  \big)
$$

has non-vanishing components

$$
  \begin{array}{l}
    T_{a b}
    \;=\;
    f^2
    \underset{
      +\,\tfrac{(s-1)!}{2}
    }{
      \underbrace{
      \big(
        (s-1)!
        -
        \tfrac{s!}{2s}
      \big)
      }
    }
    \,
    \eta_{a b}
    \\
    T_{i j}
    \;=\;
    f^2
    \underset{
      -\,\tfrac{(s-1)!}{2}
    }{
    \big(
      \underbrace{
          -
          \tfrac{s!}{2s}
      }
    \big)
    }
    \,
    \eta_{i j}
    \mathrlap{\,.}
  \end{array}
$$

Therefore the [[Einstein equation]] $G \;=\; T$ says in this case that

$$
  \begin{array}{rcl}
      \big(
        \tfrac{1}{s} - \tfrac{1}{2}
      \big)
      \mathrm{R}_s
      -
      \tfrac{1}{2}\mathrm{R}_{D-s}
    &=&
     + \tfrac{(s-1)!}{2}\, f^2
    \\
      -\tfrac{1}{2} \mathrm{R}_s
      +
      \big(
        \tfrac{1}{D-s}
        -
        \tfrac{1}{2}
      \big)
      \mathrm{R}_{D-s}
    &=&
     - \tfrac{(s-1)!}{2} \, f^2
    \mathrlap{\,.}
  \end{array}
$$

The unique solution to this system of [[linear equations]] for $\mathrm{R}_s$, $\mathrm{R}_{D-s}$ is

$$
  \begin{array}{rcl}
    \mathrm{R}_s
    &=&
    +
    \,
    \frac
      { s (D - s - 1) }
      { D - 2 }  
    \,
    (s-1)!
    \,
    f^2
    \\
    \mathrm{R}_{D-s}
    &=&
    -
    \,
    \frac
      { (s-1)(D-s) }
      { D-2 }
    \,
    (s-1)!
    \,
    f^2
    \mathrlap{\,.}
  \end{array}
$$

This is the result originally reported in [Freund & Rubin 1980 (7)](#FreundRubin80) (stated there in slightly larger generality --- except that they seem to drop the joint factor of $(s-1)!$; but for $s=2$ the factor disappears and we get their equation (4) on the nose.)


## Related concepts

* [[Kaluza-Klein mechanism]]

* [[M-theory on G2-manifolds]], [[G2-MSSM]]

* [[AdS-CFT]]


## References

The original article is 

* {#FreundRubin80} [[Peter Freund]], M. A. Rubin, _Dynamics Of Dimensional Reduction_, Phys. Lett. B **97** 2 (1980) 233-235 &lbrack;<a href="https://doi.org/10.1016/0370-2693(80)90590-0">doi:10.1016/0370-2693(80)90590-0</a>&rbrack;


Early developments:

* [[Francois Englert]], _Spontaneous Compactification of Eleven-Dimensional Supergravity_, Phys. Lett. B **119** 4-6 (1982) 339-342 &lbrack;[spire:180130](http://inspirehep.net/record/180130), <a href="https://doi.org/10.1016/0370-2693(82)90684-0">doi:10.1016/0370-2693(82)90684-0</a>&rbrack;

* {#DAuriaFré83} [[Riccardo D'Auria]], [[Pietro Fré]]: *Spontaneous generation of symmetry in the spontaneous compactification of $D=11$ supergravity*, Physics Letters B **121** 2–3 (1983) 141-146 &lbrack;<a href="https://doi.org/10.1016/0370-2693(83)90903-6">doi:10.1016/0370-2693(83)90903-6</a>&rbrack;

* [[Riccardo D'Auria]], [[Pietro Fre]], [[Peter van Nieuwenhuizen]], _Symmetry Breaking in $d=11$ Supergravity on the Parallelized Seven Sphere_, Phys. Lett. B 122 (1983) 225 ([spire:181634](https://inspirehep.net/literature/181634), <a href="https://doi.org/10.1016/0370-2693(83)90689-5">doi:10.1016/0370-2693(83)90689-5</a>)

* {#DuffNilssonPope86} [[Mike Duff]], [[Bengt Nilsson]], [[Christopher Pope]], *Kaluza-Klein supergravity*, Physics Reports **130** 1–2 (1986) 1-142 &lbrack;[spire:229417](https://inspirehep.net/record/229417), <a href="https://doi.org/10.1016/0370-1573(86)90163-8">doi:10.1016/0370-1573(86)90163-8</a>&rbrack;


Identification as [[near horizon geometries]] of [[black brane|black]] [[M2-branes]]:

* {#Page83} [[Don Page]], _Classical stability of round and squashed seven-spheres in eleven-dimensional supergravity_, Phys. Rev. D 28, 2976 (1983) ([spire:14480](http://inspirehep.net/record/14480) [doi:10.1103/PhysRevD.28.2976](https://doi.org/10.1103/PhysRevD.28.2976))

* {#DuffStelle91} [[Mike Duff]], [[Kellogg Stelle]], _Multi-membrane solutions of $D = 11$ supergravity_, Phys. Lett. B 253, 113 (1991) ([spire:299386](http://inspirehep.net/record/299386), <a href="https://doi.org/10.1016/0370-2693(91)91371-2">doi:10.1016/0370-2693(91)91371-2</a>)


See also

* [[Hermann Nicolai]], [[Krzysztof Pilch]], _Consistent truncation of $d = 11$ supergravity on $AdS_4 \times S^7$_, JHEP 03 (2012) 099 ([arXiv:1112.6131](http://arxiv.org/abs/1112.6131))


A classification of symmetric solutions is discussed in

* [[José Figueroa-O'Farrill]], _Symmetric M-Theory Backgrounds_ ([arXiv:1112.4967](http://arxiv.org/abs/1112.4967))

* Linus Wulff, _All symmetric space solutions of eleven-dimensional supergravity_ ([arXiv:1611.06139](https://arxiv.org/abs/1611.06139))


The class of Freund-Rubin compactifications of 6d [[Einstein-Maxwell theory]] down to 4d is due to

*  {#RDSS83} S. Randjbar-Daemi, [[Abdus Salam]] and J. A. Strathdee, _Spontaneous Compactification In Six-Dimensional Einstein-Maxwell Theory_, Nucl. Phys. B 214, 491 (1983) ([spire](https://inspirehep.net/record/182427/))

now a popoular toy example for [[flux compactifications]] and [[moduli stabilization]] in [[string theory]].


Textbook account (in [[D'Auria-Fre formulation of supergravity|D'Auria-Fré formulation]]):

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], volume 2, chapters V.4-V.8 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991) &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), ch V.4: [[CastellaniDAuriaFre-ChV4.pdf:file]]&rbrack;

Discussion of compactification along the fibration $S^1 \to S^7 \to \mathbb{C}P^3$ is in

* {#NilssonPope84} [[Bengt Nilsson]], [[Christopher Pope]], _Hopf Fibration of Eleven-dimensional Supergravity_, Class.Quant.Grav. 1 (1984) 499 ([Spire](http://inspirehep.net/record/202535/))

* {#ABJM08} [[Ofer Aharony]], Oren Bergman, Daniel Louis Jafferis, [[Juan Maldacena]], _$N=6$ superconformal Chern-Simons-matter theories, M2-branes and their gravity duals_ ([arXiv:0806.1218](http://arxiv.org/abs/0806.1218), [[ABJM model]])

Discussion of the case that $X_7$ is an [[orbifold]] or has other [[singularities]] (the case of interest for realistic [[phenomenology]] in [[M-theory on G2-manifolds]]) includes

* [[Bobby Acharya]], [[Frederik Denef]], C. Hofman, [[Neil Lambert]], _Freund-Rubin Revisited_ &lbrack;[arXiv:hep-th/0308046](http://arxiv.org/abs/hep-th/0308046), [spire:625121](https://inspirehep.net/literature/625121)&rbrack;

Specifically, discussion of an [[ADE classification]] of 1/2 [[BPS state|BPS]]-compactifications on $S^7/\Gamma$ for a [[finite group]] $\Gamma$ is in 

* [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], [[Sunil Gadhia]], [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))


Discussion of [[weak G2 holonomy]] on $X_7$ is in 

* [[Adel Bilal]], J.-P. Derendinger, K. Sfetsos, _(Weak) $G_2$ Holonomy from Self-duality, Flux and Supersymmetry_, Nucl.Phys. B628 (2002) 112-132 ([arXiv:hep-th/0111274](http://arxiv.org/abs/hep-th/0111274))

See also:

* [[Ergin Sezgin]], _11D Supergravity on $AdS_4 \times S^7$ versus $AdS_7 \times S^4$_ ([arXiv:2003.01135](https://arxiv.org/abs/2003.01135))



[[!redirects Freund-Rubin compactifications]]