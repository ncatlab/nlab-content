+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Wess-Zumino-Witten theory
+--{: .hide}
[[!include infinity-Wess-Zumino-Witten theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Wess-Zumino-Witten model** (or **WZW model** for short, also called  **Wess-Zumino-Novikov-Witten** model, or short **WZNW** model) is a 2-dimensional [[sigma-model]] [[quantum field theory]] whose target space is a [[Lie group]].

This may be regarded as the boundary theory of [[Chern-Simons theory]] for Lie group $G$.

The [[vertex operator algebra]]s corresponding to the WZW model are [[current algebra]]s.

## Action functional
 {#ActionFunctional}

For $G$ a [[Lie group]], the [[configuration space]] of the WZW over a 2-[[dimension]]al [[manifold]] $\Sigma$ is the space of [[smooth function]]s $g : \Sigma \to G$.

The [[action functional]] of the WZW [[sigma-model]] is the sum of two terms, a kinetic term and a topological term

$$
  S_{WZW} = S_{kin} + S_{top}
  \,.
$$



### Kinetic term
 {#KineticTerm}

The Lie group canonically carries a [[Riemannian metric]] and the kinetic term is the standard one for [[sigma-model]]s on Riemannian [[target space]]s.


### Topological term -- WZW term
 {#TopologicalTerm}

#### For the 2d WZW model
 {#WZWTermFor2dModel}

In [[higher differential geometry]], then given any closed [[differential n-form|differential (p+2)-form]] $\omega \in \Omega^{p+2}_{cl}(X)$, it is natural to ask for a [[prequantization]] of it, namely for a [[circle n-bundle with connection|circle (p+1)-bundle with connection]] $\nabla$ (equivalently: [[cocycle]] in degree-$(p+2)$-[[Deligne cohomology]]) on $X$ whose [[curvature]] is $F_\nabla = \omega$. In terms of [[moduli stacks]] this means asking for lifts of the form

$$
  \array{
    && \mathbf{B}^{p+1}U(1)_{conn}
    \\
    &{}^{\mathllap{\nabla}}\nearrow& \downarrow^{\mathrlap{F_{(-)}}}
    \\
    X
    &\stackrel{\omega}{\longrightarrow}&
   \mathbf{\Omega}^{p+2}_{cl}
  }
$$ 

in the [[homotopy theory]] of [[smooth homotopy types]].

This immediately raises the question for natural classes of examples of such prequantizations. 

One such class arises in [[infinity-Lie theory]], where $\omega$ is a [[left invariant form]] on a [[smooth infinity-group]] given by a [[cocycle]] in [[L-infinity algebra cohomology]]. The [[prequantum n-bundles]] arising this way are the higher [[WZW terms]] discussed here.

In low degree of traditional [[Lie theory]] this appears as follows: On [[Lie groups]] $G$, those closed $(p+2)$-forms $\omega$ which are [[left invariant forms]] may be identified, via the general theory of [[Chevalley-Eilenberg algebras]], with degree $(p+2)$-[[cocycles]] $\mu$ in the [[Lie algebra cohomology]] of the [[Lie algebra]] $\mathfrak{g}$ corresponding to $G$. These in turn may arise, via the [[van Est map]], as the [[Lie differentiation]] of a degree-$(p+2)$-[[cocycle]] $\mathbf{c} \colon \mathbf{B}G \to \mathbf{B}^{p+2}U(1)$ in the [[Lie group cohomology]] of $G$ itself, with [[coefficients]] in the [[circle group]] $U(1)$. 

This happens to be the case notably for $G$ a [[simply connected topological space|simply connected]] [[compact Lie group|compact]] [[semisimple Lie group]] such as [[special unitary group|SU]] or [[spin group|Spin]], where $\mu = \langle -,[-,-]\rangle$ is the [[Lie algebra cohomology|Lie algebra 3-cocycle]] in [[transgression]] with the [[Killing form]] [[invariant polynomial]] $\langle -,-\rangle$. This is, up to normalization, a representative of the de Rham image of a generator $\mathbf{c}$ of $H^3(\mathbf{B}G, U(1)) \simeq H^4(B G, \mathbb{Z}) \simeq \mathbb{Z}$. 

Generally, by the discussion at _[[geometry of physics -- principal bundles]]_, the cocycle $\mathbf{c}$ [[modulating morphism|modulates]] an [[infinity-group extension]] which is a [[circle n-group|circle p-group]]-[[principal infinity-bundle]] 

$$
  \array{
     \mathbf{B}^p U(1) &\longrightarrow& \hat G
     \\
     && \downarrow
     \\
     && G &\stackrel{\Omega\mathbf{c}}{\longrightarrow}& \mathbf{B}^{p+1}U(1)
  }
$$

whose higher [[Dixmier-Douady class]] class $ \int \Omega \mathbf{c} \in H^{p+2}(X,\mathbb{Z})$ is an integral lift of the real cohomology class encoded by $\omega$ under the [[de Rham isomorphism]]. In the example of [[spin group|Spin]] and $p = 1$ this extension is the [[string 2-group]].

Such a [[Lie theory|Lie theoretic]] situation is concisely expressed by a diagram of [[smooth homotopy types]] of the form

$$
  \array{
     && &\longrightarrow& \mathbf{B}^{p+1}U(1)
     \\
     &{}^{\mathllap{\Omega \mathbf{c}}}\nearrow& &\swArrow_\simeq& \downarrow^{\mathrlap{\theta_{\mathbf{B}^p U(1)}}}
     \\
     G &\stackrel{\omega}{\longrightarrow}& \mathbf{\Omega}_{cl}^{p+2} &\stackrel{}{\longrightarrow}& \flat_{dR}\mathbf{B}^{p+2}\mathbb{R}
  }
  \,,
$$

where $\flat_{dR}\mathbf{B}^{p+2}\mathbb{R} \simeq \flat_{dR}\mathbf{B}^{p+2}U(1)$ is the [de Rham coefficients](cohesive+infinity-topos+--+structures#deRhamCohomology) (see also at _[[geometry of physics -- de Rham coefficients]]_) and where the homotopy filling the diagram is what exhibits $\omega$ as a de Rham representative of $\Omega \mathbf{c}$.

Now, by the very [[homotopy pullback]]-characterization of the [[Deligne complex]] $\mathbf{B}^{p+1}U(1)_{conn}$ ([here](Deligne+cohomology#TheExactDifferentialCohomologyHexagon)), such a diagram is equivalently a [[prequantization]] of $\omega$:

$$
  \array{
     && \mathbf{B}^{p+1}U(1)_{conn} &\longrightarrow& \mathbf{B}^{p+1}U(1)
     \\
     &{}^\mathllap{\nabla}\nearrow& \downarrow &\swArrow_\simeq& \downarrow^{\mathrlap{\theta_{\mathbf{B}^p U(1)}}}
     \\
     G &\stackrel{\omega}{\longrightarrow}& \mathbf{\Omega}_{cl}^{p+2} &\stackrel{}{\longrightarrow}& \flat_{dR}\mathbf{B}^{p+2}\mathbb{R}
  }
  \,.
$$

For $\omega = \langle -,[-,-]\rangle$ as above, we have $p= 1$ and so $\nabla$ here is a [[circle n-bundle with connection|circle 2-bundle with connection]], often referred to as a [[bundle gerbe]] [[connection on a bundle gerbe|with connection]]. As such, this is also known as the _WZW gerbe_ or similar.

This terminology arises as follows. In ([Wess-Zumino 84](Wess-Zumino-Witten+model#WessZumino71)) the [[sigma-model]] for a [[string]] propagating on the [[Lie group]] $G$ was considered, with only the standard [[kinetic action]] term. Then in ([Witten 84](Wess-Zumino-Witten+model#Witten84)) it was observed that for this [[action functional]] to give a [[conformal field theory]] after [[quantization]], a certain [[higher gauge theory|higher gauge]] [[interaction term]] has to the added. The resulting [[sigma-model]] came to be known as the _[[Wess-Zumino-Witten model]]_ or _WZW model_ for short, and the term that Witten added became the _WZW term_. In terms of [[string theory]] it describes the propagation of the [[string]] on the group $G$ subject to a [[force]] of [[gravity]] given by the [[Killing form]] [[Riemannian metric]] and subject to a [[B-field]] [[higher gauge field|higher gauge force]] whose [[field strength]] is $\omega$.  In ([Gawedzki 87](Wess-Zumino-Witten+model#Gawedzki87)) it was observed that when formulated properly and generally, this WZW term is the [[surface holonomy]] functional of a [[connection on a bundle gerbe]] $\nabla$ on $G$. This is equivalently the $\nabla$ that we just motivated above.

Later WZW terms, or at least their curvature forms $\omega$, were recognized all over the place in [[quantum field theory]]. For instance the [[Green-Schwarz sigma-models for super p-branes]] each have an [[action functional]] that is the sum of the standard [[kinetic action]] plus a WZW term of degree $p+2$. 

In general WZW terms are "[[gauged WZW model|gauged]]" which means, as we will see, that they are not defined on the give [[smooth infinity-group]] $G$ itself, but on a bundle $\tilde G$ of differential moduli stacks over that group, such that a map $\Sigma \to \tilde G$ is a pair consisting of a map $\Sigma \to G$ and of a [[higher gauge field]] on $\Sigma$ (a "tensor multiplet" of fields).



#### Generally
 {#FormalizationGenerally}

The following ([FSS 12](#FSS12), [dcct](#dcct)) is a general axiomatization of WZW terms in [[cohesive (infinity,1)-topos|cohesive homotopy theory]].

In an ambient [[cohesive (∞,1)-topos]] $\mathbf{H}$, let $\mathbb{G}$ be a [[sylleptic ∞-group]], equipped with a [[Hodge filtration]], hence in particular with a chosen morphism

$$
  \iota \colon
  \mathbf{\Omega}^2_{cl}(-,\mathbb{G})
  \longrightarrow
  \flat_{dR} \mathbf{B}^2 \mathbb{G}
$$

to its [de Rham coefficients]()

+-- {: .num_defn #RefinementOfHodgeFiltration}
###### Definition

Given an [[∞-group]] object $G$ in $\mathbf{H}$ and given a [[group cohomology|group cocycle]]

$$
  \mathbf{c} \colon \mathbf{B}G \longrightarrow \mathbf{B}^2 \mathbb{G}
  \,,
$$

then a _refinement of the [[Hodge filtration]]_ of $\mathbb{G}$ along $\mathbf{c}$ is a completion of the [[cospan]] formed by $\flat_{dR}\mathbf{c}$ and by $\iota$ above to a [[diagram]] of the form

$$
  \array{
     \mathbf{\Omega}^1_{flat}(-,G)
     &\stackrel{\mu}{\longrightarrow}&
     \mathbf{\Omega}^2_{cl}(-,\mathbb{G})
     \\
     \downarrow && \downarrow^{\mathrlap{\iota}}
     \\
     \flat_{dR}\mathbf{B}G
     &\stackrel{\flat_{dR}\mathbf{c}}{\longrightarrow}&
     \flat_{dR}\mathbf{B}^2 \mathbb{G} 
  }
  \,.
$$

We write $\tilde G$ for the [[homotopy pullback]] of this refinement along the [[Maurer-Cartan form]] $\theta_G$ of $G$

$$
  \array{
    \tilde G &\stackrel{\theta_{\tilde G}}{\longrightarrow}& \mathbf{\Omega}^1_{flat}(-,G)
    \\
    \downarrow && \downarrow
    \\
    G &\stackrel{\theta_G}{\longrightarrow}& \flat_{dR}\mathbf{B}G
  }
  \,.
$$

=--

+-- {: .num_example}
###### Example

Let $\mathbf{H} = $ [[Smooth∞Grpd]] and $\mathbb{G} = \mathbf{B}^p U(1)$ the [[circle n-group|circle (p+1)-group]].

For $G$ an ordinary [[Lie group]], then $\mu$ may be taken to be the [[Lie algebra cohomology|Lie algebra cocycle]] corresponding to $\mathbf{c}$ and $\tilde G \simeq G$.

On the opposite extreme, for $G = \mathbf{B}^p U(1)$ itself with $\mathbf{c}$ the identity, then $\tilde G = \mathbf{B}^pU (1)_{conn}$ is the [[coefficients]] for [[ordinary differential cohomology]] (the [[Deligne complex]] under [[Dold-Kan correspondence]] and [[infinity-stackification]]).

Hence a more general case is a fibered product of these two, where $\tilde G$ is such that a map $\Sigma \longrightarrow \tilde G$ is equivalently a pair consisting of a map $\Sigma \to G$ and of differential $p$-form data on $\Sigma$. This is the case of relevance for WZW models of [[super p-branes]] with "tensor multiplet" fields on them, such as the [[D-branes]] and the [[M5-brane]].

=--

+-- {: .num_prop}
###### Proposition

In the situation of def. \ref{RefinementOfHodgeFiltration} there is an essentially unique [[prequantum n-bundle|prequantization]] 

$$
  \mathbf{L}_{WZW}
  \colon
  \tilde G
  \longrightarrow 
  \mathbf{B}^2 \mathbb{G}_{conn}
$$ 

of the closed differential form 

$$
  \mu(\theta_{\tilde G})
  \colon
  \tilde G
  \stackrel{\theta_{\tilde G}}{\longrightarrow}
  \mathbf{\Omega}^1_{flat}(-,G)
  \stackrel{\mu}{\longrightarrow}
  \mathbf{\Omega}^2_{cl}(-,\mathbb{G})
$$

whose underlying $\mathbb{G}$-[[principal ∞-bundle]] is [[modulating morphism|modulated]] by the [[looping and delooping|looping]] $\Omega \mathbf{c}$ of the original cocycle.

This we call the _WZW term_ of $\mathbf{c}$ with respect to the chosen refinement of the Hodge structure.

=--



## Properties
 {#Properties}

### Equations of motion
 {#EquationsOfMotion}

The [[variational calculus|variational derivative]] of the WZW [[action functional]] is

$$
  \delta S_{WZW}(g)
  =
  -\frac{k}{2 \pi i }
 \int_\Sigma \langle (g^{-1}\delta g), \partial (g^{-1}\bar \partial g)  \rangle 
  \,.
$$

Therefore the classical [[equations of motion]] for function $g \colon \Sigma \to G$ are

$$
  \partial(g^{-1}\bar \partial g)
  = 0
  \;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;
  \bar \partial(g \partial g^{-1}) = 0
 \,.
$$

The space of solutions to these equations is small. However, discussion of the [[quantization]] of the theory ([below](#HolographyAndRigorousConstruction)) suggests to consider these equations with the real [[Lie group]] $G$ replaced by its [[complexification]] to the  [[complex Lie group]] $G({\mathbb{C}})$. Then the general solution to the equations of motion above has the form

$$
  g(z,\bar z) 
  =
  g_{\ell}(z) g_r(\bar z)^{-1}
$$

where hence $g_{\ell} \colon \Sigma \to G(\mathbb{C})$ is any [[holomorphic function]] and $g_r$ similarly any anti-holomorphic function.

(e.g. [Gawedzki 99 (3.18), (3.19)](#Gawedzki99))

### Holography and Rigorous construction
 {#HolographyAndRigorousConstruction}

By  the [[AdS3-CFT2 and CS-WZW correspondence]] (see there for more details) the 2d WZW [[CFT]] on $G$ is related to $G$-[[Chern-Simons theory]] in $3d$.

In fact a rigorous constructions of the $G$-WZW model as a [[rational 2d CFT]] is via the [[FRS-theorem on rational 2d CFT]], which constructs the model as a [[boundary field theory]] of the $G$-[[Chern-Simons theory]] as a [[3d TQFT]] incarnated via a [[Reshetikhin-Turaev construction]].

### D-branes for the WZW model
 {#DBranes}

The characterization of [[D-brane]] [[submanifolds]] for the [[open string]] WZW model on a [[Lie group]] $G$ comes from two consistency conditions:

1. geometrical condition:

   For the open string [[CFT]] to still have [[current algebra]] [[worldsheet]] symmetry, hence for half the current algebra symmetry of the closed WZW string to be preserved, the [[D-brane]] [[submanifolds]] need to be [[conjugacy classes]] of the group manifold (see e.g. [Alekseev-Schomerus](#AlekseevSchomerus) for a brief review and further pointers). These conjugacy classes are therefore also called the **symmetric D-branes**.

   Notice that these conjugacy classes are equivalently the [[leaves]] of the [[foliation]] induced by the canonical [[Cartan-Dirac structure]] on $G$, hence (by the discussion at [[Dirac structure]]), the leaves induced by the  [[Lagrangian dg-submanifold|Lagrangian sub-Lie 2-algebroids]] of the [[Courant Lie 2-algebroid]]  which is the [[higher gauge groupoid]] (see there) of the background [[B-field]] on $G$.(It has been suggested by [[Chris Rogers]] that such a foliation be thought of as a higher real [[polarization]].) 

1. cohomological condition: 

   In order for the Kapustin-part of the [[Freed-Witten-Kapustin anomaly]] of the [[worldsheet]] [[action functional]] of the open WZW string to vanish, the D-brane must be equipped with a [[Chan-Paton gauge field]], hence a [[twisted unitary bundle]] ([[bundle gerbe module]]) of some rank $n \in \mathbb{N}$ for the restriction of the ambient [[B-field]] to the brane. 

   For [[simply connected topological space|simply connected]] Lie groups only the rank-1 Chan-Paton gauge fields and their direct sums play a role, and their existence corresponds to a trivialization of the underlying $\mathbf{B}U(1)$-[[principal 2-bundle]] ($U(1)$-[[bundle gerbe]]) of the restriction of the [[B-field]] to the brane. There is then a discrete finite collection of symmetric D-branes = [[conjugacy classes]] satisfying this condition, and these are called the **integral symmetric D-branes**. ([Alekseev-Schomerus](#AlekseevSchomerus), [Gawedzki-Reis](#GW)). As observed in [Alekseev-Schomerus](#AlekseevSchomerus), this may be thought of as identifying a D-brane as a variant kind of a [[Bohr-Sommerfeld leaf]].

   More generally, on non-simply connected group manifolds there are nontrivial higher rank [[twisted unitary bundles]]/[[Chan-Paton gauge fields]] over conjugacy classes and hence the cohomological "integrality" or "Bohr-Sommerfeld"-condition imposed on symmetric D-branes becomes more refined ([Gawedzki 04](#Gawedzki04)).

In summary, the [[D-brane]] [[submanifolds]] in a Lie group which induce an [[open string]] WZW model that a) has one [[current algebra]] symmetry and b) is [[Freed-Witten-Kapustin anomaly|Kapustin-anomaly]]-free are precisely the [[conjugacy class]]-submanifolds $G$ equipped with a [[twisted unitary bundle]] for the restriction of the background [[B-field]] to the conjugacy class.

### Quantization

on [[quantization]] of the WZW model, see at 

* [[quantization of loop groups]],

* [[equivariant elliptic cohomology]]

* [[quantization of Chern-Simons theory]]


## Related concepts

* [[geometry of physics -- WZW terms]]

* [[current algebra]], [[affine Lie algebra]]

* [[Knizhnik-Zamolodchikov equation]]

* [[coset WZW model]]

* [[gauged WZW model]]

* [[parameterized WZW model]]

* [[higher dimensional WZW model]]

* [[Green-Schwarz action functional]]

* [[analytically continued Wess-Zumino-Witten theory]]

## References
 {#References}

### Original references

The Wess-Zumino gauge-coupling term goes back to

* {#WessZumino71} [[Julius Wess]], [[Bruno Zumino]], _Consequences of anomalous ward identities_. Phys. Lett. 37B, 95 (1971)

and was understood as yielding a 2-dimensional [[conformal field theory]] in 

* {#Witten84} [[Edward Witten]], _Non-Abelian bosonization in two dimensions_ Commun. Math. Phys. 92, 455 (1984)

* {#KnizhnikZamolodchikov85} [[Vadim Knizhnik]], [[Alexander Zamolodchikov]], _Current algebra and Wess-Zumino model in two dimensions_, Nucl. Phys. B 247, 83-103 (1984)

and hence (a possible part of) a [[string theory]] [[vacuum]]/[[target space]] in

* [[Doron Gepner]], [[Edward Witten]], _String theory on group manifolds_, Nucl. Phys. B 278, 493-549 (1986) ([spire](http://inspirehep.net/record/230076?ln=en))

The WZ term on $\Sigma_2$ was understood in terms of an integral of a 3-form over a cobounding manifold $\Sigma_3$ in 

* [[Edward Witten]], _Global aspects of current algebra_. Nucl. Phys. B223, 422 (1983)

for the case that $\Sigma_2$ is [[closed manifold|closed]], and generally, in terms of [[surface holonomy]] of [[bundle gerbes]]/[[circle 2-bundles with connection]] in

* {#Gawedzki87} [[Krzysztof Gaw?dzki]] _Topological Actions in two-dimensional Quantum Field Theories_, in [[Gerard 't Hooft]] et. al (eds.) _Nonperturbative quantum field theory_ Cargese 1987 proceedings,  ([web](http://inspirehep.net/record/257658?ln=de))
  

* [[Giovanni Felder]] , [[Krzysztof Gaw?dzki]], A. Kupianen, _Spectra of Wess-Zumino-Witten models with arbitrary simple groups_. Commun. Math. Phys. 117, 127 (1988)

* [[Krzysztof Gaw?dzki]], _Topological actions in two-dimensional quantum field theories_. In: Nonperturbative quantum field theory. 'tHooft, G. et al. (eds.). London: Plenum Press 1988

as the [[surface holonomy]] of a [[circle 2-bundle with connection]]. See also the references at _[[B-field]]_ and at _[[Freed-Witten anomaly cancellation]]_.

For the fully general understanding as the [[surface holonomy]] of a [[circle 2-bundle with connection]] see the references [below](#ReferencesRelationToGerbesAndCS).

See also 

* [[Edward Witten]], _On holomorphic factorization of WZW and coset models_, Comm. Math. Phys. Volume 144, Number 1 (1992), 189-212. ([Euclid](http://projecteuclid.org/euclid.cmp/1104249222))

### Introductions and surveys

An survey of and introduction to the topic is in 

* Patrick Meessen, _Strings Moving on Group Manifolds: The WZW Model_ ([pdf](http://www.unioviedo.es/hepth/people/Patrick/fysica/zooi/WZW_ClassMunoz.pdf))

A classical textbook accounts include

* [[Bojko Bakalov]], [[Alexander Kirillov]], chapter 7 ([ps.gz](http://www.math.sunysb.edu/~kirillov/tensor/chapter7.ps.gz)) of _Lectures on tensor categories and modular functor_ ([web](http://www.math.sunysb.edu/~kirillov/tensor/tensor.html))

* P. Di Francesco, P. Mathieu, D. S&#233;n&#233;chal, _Conformal field theory_, Springer 1997

A basic introduction also to the super-WZW model (and with an eye towards the corresponding [[2-spectral triple]]) is in

* {#FroehlichGawedzki93} [[Jürg Fröhlich]], [[Krzysztof Gaw?dzki]], _Conformal Field Theory and Geometry of Strings_,  extended lecture notes for lecture given at the Mathematical Quantum Theory Conference, Vancouver, Canada, August 4-8 ([arXiv:hep-th/9310187](http://arxiv.org/abs/hep-th/9310187))


A useful account of the WZW model that encompasses both its [[action functional]] and [[path integral]] quantization as well as the [[current algebra]] aspects of the QFT is in

* {#Gawedzki99} [[Krzysztof Gawedzki]], _Conformal field theory: a case study_ in Y. Nutku, C. Saclioglu, T. Turgut (eds.) _Frontier in Physics_ 102, Perseus Publishing (2000) ([hep-th/9904145](http://xxx.lanl.gov/abs/hep-th/9904145))

This starts in section 2 as a warmup with describing the 1d QFT of a particle propagating on a group manifold. The [[Hilbert space]] of [[states]] is expressed in terms of the [[Lie theory]] of $G$ and its [[Lie algebra]] $\mathfrak{g}$.

In section 4 the [[quantization]] of the 2d WZW model is discussed in analogy to that. In lack of a full formalization of the quantization procedure, the author uses the loop algebra $\mathcal{l} \mathfrak{g}$ --  the [[affine Lie algebra]] -- of $\mathfrak{g}$ as the evident analog that replaces $\mathfrak{g}$ and discusses the [[Hilbert space]] [[space of states|of states]] in terms of that. He also indicates how this may be understood as a space of [[sections]] of a ([[prequantum line bundle|prequantum]]) [[line bundle]] over the [[loop group]].


See also

* L. Feh&#233;r, L. O'Raifeartaigh, P. Ruelle, I. Tsutsui, A. Wipf, _On Hamiltonian reductions of the Wess-Zumino-Novikov-Witten theories_, Phys. Rep. __222__ (1992), no. 1, 64 pp. [MR93i:81225](http://www.ams.org/mathscinet-getitem?mr=1192998), <a href="http://dx.doi.org/10.1016/0370-1573(92)90026-V">doi</a>

* [[Krzysztof Gawedzki]], Rafal Suszek, [[Konrad Waldorf]], _Global gauge anomalies in two-dimensional bosonic sigma models_ ([arXiv:1003.4154](http://arxiv.org/abs/1003.4154))

* Paul de Fromont, [[Krzysztof Gaw?dzki]], Cl&#233;ment Tauber, _Global gauge anomalies in coset models of conformal field theory_ ([arXiv:1301.2517](http://arxiv.org/abs/1301.2517))

### Relation to gerbes and Chern-Simons theory
 {#ReferencesRelationToGerbesAndCS}


Discussion of [[circle n-bundle with connection|circle 2-bundles with connection]] (expressed in terms of [[bundle gerbes]]) and discussion of the WZW-background [[B-field]] ([[WZW term]]) in this language is in 

* [[Krzysztof Gawedzki]], Nuno Reis, _WZW branes and gerbes_, Rev.Math.Phys. 14 (2002) 1281-1334 ([arXiv:hep-th/0205233](http://arxiv.org/abs/hep-th/0205233))
 {#GW}

* [[Christoph Schweigert]], [[Konrad Waldorf]], _Gerbes and Lie Groups_, in _Trends and Developments in Lie Theory_, Progress in Math., Birkh&#228;user ([arXiv:0710.5467](http://arxiv.org/abs/0710.5467))

Discussion of how this 2-bundle arises from the [[Chern-Simons circle 3-bundle]] is in

* [[Alan Carey]], Stuart Johnson, [[Michael Murray]], [[Danny Stevenson]], [[Bai-Ling Wang]], _Bundle gerbes for Chern-Simons and Wess-Zumino-Witten theories_ 	Commun.Math.Phys. 259 (2005) 577-613 ([arXiv:math/0410013](http://arxiv.org/abs/math/0410013))


and related discussion is in

* [[Konrad Waldorf]], _Multiplicative Bundle Gerbes with Connection_ , 	Differential Geom. Appl. 28(3), 313-340 (2010) ([arXiv:0804.4835](http://arxiv.org/abs/0804.4835))

See also Section 2.3.18 and section 4.7 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_  ([pdf slides](http://ncatlab.org/schreiber/files/Erlangen2011Schreiber.pdf)).

### Partition functions

* [[Terry Gannon]], _Partition Functions for Heterotic WZW Conformal Field Theories_, Nucl.Phys. B402 (1993) 729-753 ([arXiv:hep-th/9209042](http://arxiv.org/abs/hep-th/9209042))

### D-branes for the WZW model
 {#ReferencesDBranes}

A characterization of [[D-branes]] in the WZW model as those [[conjugacy classes]] that in addition satisfy an integrality ([[Bohr-Sommerfeld quantization|Bohr-Sommerfeld]]-type) condition missed in other parts of the literature is stated in 

* {#AlekseevSchomerus} [[Anton Alekseev]], [[Volker Schomerus]], _D-branes in the WZW model_, Phys.Rev.D60:061901,1999 ([arXiv:hep-th/9812193v2](http://arxiv.org/abs/hep-th/9812193v2))
 

The refined interpretation of the integrality condition as a choice of trivialization of the underling [[principal 2-bundle]]/[[bundle gerbe]] of the [[B-field]] over the brane was then noticed in section 7 of 

* [[Krzysztof Gawedzki]], Nuno Reis, _WZW branes and gerbes_, Rev.Math.Phys. 14 (2002) 1281-1334 ([arXiv:hep-th/0205233](http://arxiv.org/abs/hep-th/0205233))

The observation that this is just the special rank-1 case of the more general structure provided by a [[twisted unitary bundle]] of some rank $n$ on the D-brane ([[gerbe module]]) which is twisted by the restriction of the [[B-field]] to the D-brane -- the [[Chan-Paton gauge field]] --  is due to

* {#Gawedzki04} [[Krzysztof Gawedzki]], _Abelian and non-Abelian branes in WZW models and gerbes_, Commun.Math.Phys. 258 (2005) 23-73 ([arXiv:hep-th/0406072](http://arxiv.org/abs/hep-th/0406072)).
 

The observation that the "multiplicative" structure of the WZW-[[B-field]] (induced from it being the [[transgression]] of the [[Chern-Simons circle 3-bundle|Chern-Simons circle 3-connection]] over the [[moduli stack]] of $G$-[[principal connections]]) induces the [[Verlinde ring]] fusion product structure on symmetric D-branes equipped with [[Chan-Paton gauge fields]] is discussed in 

* [[Alan Carey]], [[Bai-Ling Wang]], _Fusion of symmetric $D$-branes and Verlinde rings_, Commun. Math. Phys.277:577-625 (2008) ([arXiv:math-ph/0505040](http://arxiv.org/abs/math-ph/0505040))

The image in [[K-theory]] of these [[Chan-Paton gauge fields]] over conjugacy classes is shown to generate the [[Verlinde ring]]/the [[positive energy representations]] of the [[loop group]] in 

* [[Eckhard Meinrenken]], _On the quantization of conjugacy classes_,  	Enseign. Math. (2) 55 (2009), no. 1-2, 33-75 ([arXiv:0707.3963](http://arxiv.org/abs/0707.3963))

Formalization of WZW terms in [[cohesive (infinity,1)-topos|cohesive homotopy theory]] is in 

* {#dcct} _[[schreiber:differential cohomology in a cohesive topos]]_

### Relation to dimensional reduction of Chern-Simons

One can also obtain the WZW-model by [[KK-reduction]]
from [[Chern-Simons theory]].

E.g.

* [[Matthias Blau]], G. Thompson, _Derivation of the Verlinde Formula from Chern-Simons Theory and the G/G model_, Nucl.Phys. B408 (1993) 345-390 ([arXiv:hep-th/9305010](http://arxiv.org/abs/hep-th/9305010))

A discussion in [[higher differential geometry]] via [[transgression]] in [[ordinary differential cohomology]] is in 

* _[[schreiber:Extended higher cup-product Chern-Simons theories]]_

* _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_

### Relation to extended TQFT

Relation to [[extended TQFT]] is discussed in 

* [[Dan Freed]], _[[4-3-2 8-7-6]]_

The formulation of the [[Green-Schwarz action functional]] for [[superstrings]] (and other [[branes]] of [[string theory]]/[[M-theory]]) as WZW-models (and [[schreiber:∞-Wess-Zumino-Witten theory|∞-WZW models]]) on ([[super L-∞ algebra]] [[L-∞ extensions]] of) the [[super translation group]] is in 

* {#FSS12} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_, International Journal of Geometric Methods in Modern Physics, Volume 12, Issue 02 (2015) 1550018  ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))

### In solid state physics 

Discussion of [[symmetry protected topological order]] phases of matter in [[solid state physics]] via higher WZW models is in 

* {#CGLW11} Xie Chen, Zheng-Cheng Gu, Zheng-Xin Liu, [[Xiao-Gang Wen]], _Symmetry protected topological orders and the group cohomology of their symmetry group_, Phys. Rev. B 87, 155114 (2013) [arXiv:1106.4772](http://arxiv.org/abs/1106.4772); A short version in Science __338__, 1604-1606 (2012) [pdf](http://dao.mit.edu/~wen/pub/dDSPTsht.pdf)


[[!redirects WZW model]]
[[!redirects WZW-model]]

[[!redirects Wess-Zumino-Witten-model]]

[[!redirects WZW models]]
[[!redirects WZW-models]]

[[!redirects Wess-Zumino-Witten-models]]

[[!redirects Wess-Zumino model]]
[[!redirects Wess-Zumino-model]]

[[!redirects Wess-Zumino models]]
[[!redirects Wess-Zumino-models]]

[[!redirects WZW theory]]
[[!redirects WZW-theory]]

[[!redirects Wess-Zumino-Novikov-Witten model]]
[[!redirects Wess-Zumino-Novikov-Witten models]]

[[!redirects WZNW model]]
[[!redirects WZNW models]]
[[!redirects WZNW-model]]
[[!redirects WZNW-models]]
[[!redirects WZNW theory]]
[[!redirects WZNW-theory]]

[[!redirects Wess-Zumino-Witten-theory]]

[[!redirects WZW theories]]

[[!redirects WZW-theories]]

[[!redirects Wess-Zumino-Witten-theories]]

[[!redirects Wess-Zumino theory]]
[[!redirects Wess-Zumino-theory]]

[[!redirects Wess-Zumino theories]]
[[!redirects Wess-Zumino-theories]]

[[!redirects 2d WZW model]]

[[!redirects Wess-Zumino-Witten theory]]

[[!redirects WZW term]]
[[!redirects WZW terms]]
[[!redirects WZW-term]]
[[!redirects WZW-terms]]


[[!redirects WZW gerbe]]
[[!redirects WZW gerbes]]

[[!redirects Wess-Zumino-Witten sigma model]]
[[!redirects Wess-Zumino-Witten sigma models]]