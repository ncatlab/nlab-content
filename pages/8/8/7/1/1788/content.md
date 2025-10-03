> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak



***


## Idea

By reference to the [[superembedding formalism]] for [[super p-branes]], the existence of "$L_p$-branes" has been argued &lbrack;[Howe & Sezgin 1997, p. 8](#HoweSezgin97a)&rbrack;, for small natural numbers $p$, with the following properties:

The $p+4$-dimensional [[target spacetime]] $X^{p+4}$ carries [[flux densities]] 

$$
  \begin{aligned}
    G_2 & \in \Omega^2_{dR}\big(X^{p+4}\big)
    \\
    G_{p+1} & \in \Omega^{p+1}_{dR}\big(X^{p+4}\big)
    \\
    G_{p+2} & \in \Omega^{p+2}_{dR}\big(X^{p+4}\big)
    \mathrlap{\,,}
  \end{aligned}
$$

subject to the [[Bianchi identities]]

$$
  \begin{aligned}
    \mathrm{d} G_2 & = 0
    \\
    \mathrm{d} G_{p+1} & = 0
    \\
    \mathrm{d} G_{p+2} & = G_2 \wedge G_{p+1} 
    \,,
  \end{aligned}
$$

and on the brane's [[worldvolume]] 

$$
  \Sigma^{p+1} 
    \xrightarrow{\phantom{-}\phi\phantom{-}} 
  X^{p+4}
$$ 

there is a flux density 

$$
  \begin{aligned}
    F_p & \in \Omega^p_{dR}(X^{p+1})
  \end{aligned}
$$

satisfying the [[Bianchi identity]]

$$
  \begin{aligned}
    \mathrm{d} \, F_p 
    & = \phi^\ast G_{p+1}
    \,.
  \end{aligned}
$$

In [Howe, Raetzel & Sezgin 19 98, p 3](#HoweRaetzelSezgin98) this is claimed for $p \in \{1,2,3,4,5\}$. The followup article [Howe, Raetzel & Rudychev 1999](#HoweRaetzelRudychev99) considers it for $p \in \{3,4,5\}$.

## References

* {#HoweSezgin97a} [[Paul S. Howe]], [[Ergin Sezgin]], p. 8 of:  *Superbranes*, Phys. Lett. B **390** (1997) 133-142 &lbrack;[arXiv:hep-th/9607227](https://arxiv.org/abs/hep-th/9607227), <a href="https://doi.org/10.1016/S0370-2693(96)01416-5">doi:10.1016/S0370-2693(96)01416-5</a>&rbrack;

* {#HoweRaetzelSezgin98} [[Paul S. Howe]], O. Raetzel, [[Ergin Sezgin]], pp. 3-4 of: *On Brane Actions and Superembeddings*, JHEP 9808 (1998) 011 &lbrack;[arXiv:hep-th/9804051](https://arxiv.org/abs/hep-th/9804051), [doi:10.1088/1126-6708/1998/08/011](https://doi.org/10.1088/1126-6708/1998/08/011)&rbrack;

* {#HoweRaetzelRudychev99} [[Paul S. Howe]], O. Raetzel, I. Rudychev, [[Ergin Sezgin]]: *L-branes*, Class. Quant. Grav. **16** (1999) 705-722 &lbrack;[arXiv:hep-th/9810081](https://arxiv.org/abs/hep-th/9810081), [doi:10.1088/0264-9381/16/3/006](https://doi.org/10.1088/0264-9381/16/3/006)&rbrack;

* [[Steven Duplij]]: *L-Brane*, in *Concise Encyclopedia of Supersymmetry*, Springer (2004) 225 &lbrack;[doi:10.1007/1-4020-4522-0_294](https://doi.org/10.1007/1-4020-4522-0_294), [[Duplij-LBrane.pdf:file]]&rbrack; 




**Orientations of Orbi-K-Theory measuring Topological Phases and Brane Charges**

In [[theoretical physics]], [[Chern insulator|Chern phases]] of [[topological phases of matter|topological]] [[quantum materials]], as well as [[brane]] [[charges]] on [[11D supergravity]] [[orbifolds]], have famously been argued to be classified by ([[orbifold K-theory|orbi]]) [[topological K-theory]], or possibly by other [[Whitehead-generalized cohomology theory|stable]] and, notably, [[complex-oriented cohomology theory|complex-oriented]] [[cohomology theories]], such as [[cobordism cohomology|stable Cobordism]] or [[elliptic cohomology]]. 

However, closer inspection reveals that the fine-grained "[fragile](topological+phase+of+matter#ReferencesUnstableClassificationOfTopologicalPhases)" classification in both cases plausibly is in ([[equivariant Cohomotopy|orbi]]) [[Cohomotopy]], which is the primordial "unstable" or [[non-abelian cohomology|nonabelian]] [[generalized cohomology]]. Coarsening should take the latter (fragile) to the former (stable) cohomology along an extraordinary [[cohomology operation]]. But what then is the role of [[complex-oriented cohomology|complex orientation]] on the stable side?

We observe here (i) that over [[nodal lines]] in the [[Brillouin torus]]/on [[probe brane|probe]] [[M5-branes]] in [[D=11 supergravity|11D]] [[spacetime]], the [[cohomotopy|cohomotopical]] [[topological phase of matter|phases]]/[[D-brane charge|charges]] lift through the [[complex Hopf fibration|complex]]/[[quaternionic Hopf fibration|quaternionic]] [[Hopf fibration]], and (ii) that observing this fragile situation in stable cohomology means equivalently to ask for universal [[complex oriented cohomology|complex]]/[[quaternionic oriented cohomology|quaternionic]] [orientation in four/ten dimensions](complex+oriented+cohomology+theory#ReferencesFiniteStageOrientations)!

Then we give an elegant concrete realization of such [four/ten-dimensional](complex+oriented+cohomology+theory#ReferencesFiniteStageOrientations) [[complex oriented cohomology|complex]]/[[quaternionic oriented cohomology|quaternionic]] orientation in [[Sp(1)|$Sp(1)$]]/[[Sp(2)|$Sp(2)$]]-[[equivariant K-theory]], using [real division-algebraic tools](geometry+of+physics+--+supersymmetry#RealSpinRepresentationViaNormedDivisionAlgebra) with a [new model](twisted+equivariant+K-theory#SS25) of [[twisted equivariant K-theory]] in [[cohesive (infinity,1)-topos|cohesive homotopy theory]]; and we explain this as an extraordinary character map from [[equivariant Cohomotopy|equivariant]] [[Cohomotopy]]-[[twisted Cohomotopy]] to [[equivariant K-theory|equivariant]] [[relative K-theory]].





\linebreak

A universal [[real oriented cohomology theory|real]], [[complex oriented cohomology theory|complex]] or [[quaternionic oriented cohomology theory|quaternionic]] "[[orientation in generalized cohomology|orientation]]" of ([[vector bundles]] in) a [[multiplicative cohomology theory|multiplicative]]$\;$[[generalized cohomology theory]] is well-known to be a [[cohomology class|class]] on [[infinite projective space|$\mathbb{K}P^\infty$]] which restricts to [[unit|unity]] on [[projective line|$\mathbb{K}P^1$]], for [[real normed division algebra|$\mathbb{K} \in 
\{$]][[real numbers|$\mathbb{R}$]], [[complex numbers|$\mathbb{C}$]], [[quaternions|$\mathbb{H}$]]$\}$, respectively. Over the [[octonions]], [[octonions|$\mathbb{O}$]], the highest [[octonionic projective space|projective space]] to exist is [[octonionic projective plane|$\mathbb{O}P^2$]], but classes on $\mathbb{K}P^2$ restricting to unity on $\mathbb{K}P^1$ are known to still give ["$(3 dim_{\mathbb{R}}(\mathbb{K})-2)$-dimensional" orientations](complex+oriented+cohomology+theory#ReferencesFiniteStageOrientations) for $\mathbb{K} \in 
\{\mathbb{R}, \mathbb{C},\mathbb{H} \}$. We highlight that this notion of orientation thus generalizes to $\mathbb{K} = \mathbb{O}$. Using [2-component $\mathbb{K}$-spinor formalism](geometry+of+physics+--+supersymmetry#RealSpinRepresentationViaNormedDivisionAlgebra) for [[real normed division algebra|$\mathbb{K} \in 
\{\mathbb{R}, \mathbb{C},\mathbb{H}, \mathbb{O}\}$]], known from higher dimensional [[supergravity]], we give a unified construction of canonical [$(3 dim_{\mathbb{R}}(\mathbb{K})-2)$-dimensional $\mathbb{K}$-orientations](complex+oriented+cohomology+theory#ReferencesFiniteStageOrientations) of [[complex K-theory]], [[equivariant K-theory|equivariant]] with respect to [[finite group|finite]] [[subgroups]] of the [[spin groups]] $U(\mathbb{K},2)$. We close with an outlook on application to [[physics]], where these orientations serve as extraordinary [[Dold-Chern character map|character maps]] from unstable  [[equivariant Cohomotopy|equivariant]] [[Cohomotopy]] to [[equivariant K-theory|equivariant]]$\;$[[complex K-theory]], both for $\mathbb{K}$-[[Chern insulator|Chern phases]] of [[crystalline topological insulator|crystalline]] [[topological phases of matter|topological]] [[quantum materials]], as well as for [[geometry of physics -- flux quantization|proper flux quantized]] [[charges]] on [[orbifold]] [[M-branes]].

### Tautological $\mathbb{K}$-line bundle

We discuss the [[tautological line bundle|tautological $\mathbb{K}$-line bundles]] over the [[projective space]] $\mathbb{K}P^1$, for $\mathbb{K} \in \{\mathbb{R}, \mathbb{C}, \mathbb{H}, \mathbb{O}\}$ (one of [[Hurwitz theorem|the four real normed division algebras]]: the [[real numbers]], [[complex numbers]], [[quaternions]] or [[octonions]]), hence topologically over

* the tautological [[real vector bundle|real line bundle]] over  [[circle]] $\mathbb{R}P^1 \sim S^1$, 

* the tautological [[complex vector bundle|complex line bundle]] over the [[2-sphere]] $\mathbb{C}P^1 \sim S^2$

* the tautological [[quaternionic vector bundle|quaternionic line bundle]] over the [[4-sphere]] $\mathbb{H}P^1 \sim S^4$

* the tautological [[octonionic line bundle]] over the [[8-sphere]] $\mathbb{O}P^1 \sim S^8$

(...)



(...)

HW interval end in hidd3n sectors



$$
  F_2 = 
  F_2^{X^3}
  + 
  F_0 \mathrm{d}t \wedge \mathrm{d}v
$$

$$
  \star F_2
  = 
  \ell_v
  \star_3 F_2^{X^3} \wedge \mathrm{d}t \wedge \mathrm{d}v
  +
  \tfrac{1}{\ell_v}
  \star_3 F_0
$$

$$
  \underset{\underset{\ell_v \to 0}{\longrightarrow}}{\lim}
  \,
  \mathrm{d} \star F_2 
  = 0
$$

$$
  F_2
  \wedge 
  F_2
  =
  F_2^{X^3} \wedge F_2^{X^3}
  +
  2 F_2^{X^3} F_0 \mathrm{d}t \wedge \mathrm{d}v 
$$
