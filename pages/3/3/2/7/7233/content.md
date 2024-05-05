
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _$G_2$-structure_ on a [[manifold]] $X$ of [[dimension]] 7 is a choice of [[G-structure]] on $X$, for $G$ the [[exceptional Lie group]] [[G2]]. Hence it is a reduction of the [[structure group]] of the [[frame bundle]] of $X$ along the canonical (the defining) inclusion $G_2 \hookrightarrow GL(\mathbb{R}^7)$ into the [[general linear group]].

Given that $G_2$ is the [[subgroup]] of the [[general linear group]] on the [[Cartesian space]] $\mathbb{R}^7$ which preserves the [[associative 3-form]] on $\mathbb{R}^7$, a $G_2$ structure is a higher analog of an  [[almost symplectic structure]] under lifting from [[symplectic geometry]] to [[2-plectic geometry]] ([Ibort](#Ibort)).

A _$G_2$-manifold_ is a manifold equipped with $G_2$-structure that is [[integrability of G-structures|integrable to first order]], i.e. [[torsion of a G-structure|torsion-free]] (prop. \ref{CovariantlyConstantDefinite3FormMeansTorsionVanishes} below). This is equivalently a [[Riemannian manifold]] of [[dimension]] 7 with [[special holonomy]] group being the [[exceptional Lie group]] [[G2]]. 

$G_2$-manifolds may be understood as 7-dimensional [[analogs]] of real 6-dimensional [[Calabi-Yau manifolds]]. Accordingly the relation between [[Calabi-Yau manifolds and supersymmetry]] lifts from [[string theory]] to [[M-theory on G2-manifolds]].

## Definition
 {#Definition}

The definition of $G_2$-manifold stuctures proceeds in stages:

1. [$G_2$-structure](#G2Structures)

1. [Closed $G_2$-structure](#ClosedG2Structure)

1. [$G_2$-holonomy/manifold structure](#G2Holonomy)

and then there are 

* [Variant structures](#VariantsAndWeakenings).

### $G_2$-structure
 {#G2Structures}

\begin{definition}
\label{G2Structure}

For $X$ a [[smooth manifold]] of [[dimension]] $7$ a **$G_2$-structure** on $X$ is a [[G-structure]] for $G = $ [[G2]] $\hookrightarrow GL(7)$.

\end{definition}

+-- {: .num_remark #CanonicalRiemannianMetric}
###### Remark

Since the inclusion of $G_2$ into $GL(7)$ factors through [[special orthogonal group|$SO(6)$]] (see [here](G2#Orientation)), a $G_2$-structure induces an [[orthogonal structure]], hence a [[Riemannian metric]].

=--

Given the definition of [[G2]] as the [[stabilizer group]] of the [[associative 3-form]] on $\mathbb{R}^7$, there is accordingly an equivalent formulation of def. \ref{G2Structure} in terms of [[differential forms]]:


\begin{definition}
\label{Definite3Forms}

Write $\Lambda^3_+(\mathbb{R}^7)^\ast \hookrightarrow \Lambda^3(\mathbb{R}^7)^\ast $ for the [[orbit]] of the [[associative 3-form]] $\phi$ under the canonical $GL(7)$-[[action]]. Similarly for $X$ a [[smooth manifold]] of [[dimension]] 7, write 

$$
  \Omega^3_+(X) \hookrightarrow \Omega^3(X)
$$

for the subset of the set of [[differential 3-forms]] on those that, as [[sections]] to the exterior power of the [[cotangent bundle]], are pointwise in $\Lambda^3_+(\mathbb{R}^7)^\ast$. 

These are also called the _positive forms_ ([Joyce 00, p. 243](#Joyce00)) or the _[[definite differential forms]]_ ([Bryant 05, section 3.1.1](#Bryant05)) on $X$.

\end{definition}

(e.g. [Bryant 05, definition 2](#Bryant05))

+-- {: .num_prop #G2StructureViaDefinite3Form}
###### Proposition

A $G_2$-structure on $X$, def. \ref{G2Structure}, is equivalently 
a choice of [[definite 3-form]] $\sigma$ on $X$, def. \ref{Definite3Forms}.

=--

(e.g. [Joyce 00, p. 243](#Joyce00), [Bryant 05, section 3.1.1](#Bryant05))

Often it is useful to exhibit prop. \ref{G2StructureViaDefinite3Form} in the following way.

+-- {: .num_example #DefiniteFormsInTermsOfVielbeinFields}
###### Example

For $X$ a [[smooth manifold]] of [[dimension]] 7, write $Fr(X) \to X$ for its [[frame bundle]]. By the discussion at _[vielbein -- in terms of basic forms on the frame bundle](vielbein#InTermsOfBasicFormsOnFrameBundle)_ there is a universal $\mathbb{R}^7$-valued differential form on the total space of the frame bundle

$$
  E_u \in \Omega^1(Fr(X), \mathbb{R}^7)
$$

(whose components we write $(E_u^a)_{a = 1}^7$) such that given an [[orthogonal structure]] $i \colon Fr_O(X)\hookrightarrow Fr(X)$ and a local section $\sigma_i \colon (U_i \subset X) \to Fr_O(X)$ of orthogonal frames, then the [[pullback of differential forms]]

$$
  E_i \coloneqq \sigma_i^\ast i^\ast E_u
$$

is the corresponding local [[vielbein]] field. Hence one obtains a universal 3-form $\phi_u \in \Omega^3(Fr(x))$ on the frame bundle by setting

$$
  \phi_u \coloneqq \phi_{a b c} E_u^a \wedge E_u^b \wedge E_u^c
$$

with $(\phi_{a b c})$ the canonical components of the [[associative 3-form]] and with summation over repeated indices understood.

By construction this is such that on a [[chart]] $(U_i \subset X)$ any [[definite 3-form]], def. \ref{Definite3Forms}, restricts to the [[pullback of differential forms|pullback]] of $\phi_u$ via a [[section]] $\sigma_i \colon U_i \to Fr(X)$ and hence is of the form

$$
  \phi_{a b c} E_i^a \wedge E_i^b \wedge E_i^c
  \,.
$$

Conversely, given a 3-form $\sigma \in \Omega^3(X)$ such that on an [[atlas]] $(U_i \to X)$ over which the frame bundle trivializes it is of this form

$$
  \sigma|_{U_i} = \phi_{a b c} E_i^a \wedge E_i^b \wedge E_i^c
$$

then the $GL(7)$-valued transition functions $g_{i j}$ of the given local trivialization must factor through $G_2\hookrightarrow SO(7) \hookrightarrow GL(7)$ and hence exhibit a $G_2$-structure: because we have  $\sigma|_{U_i} = \sigma|_{U_j} \;\;\; on \;U_i \cap U_j$ and hence 

\[
  \label{Definite3FormsOnTwoPatches}
   \phi_{a b c} E_i^a \wedge E_i^b \wedge E_i^c
   =
   \phi_{a b c} E_j^a \wedge E_j^b \wedge E_j^c
   \;\;\;
    on \; U_i \cap U_j
  \,.
\]

But by the nature of the [universal vielbein](vielbein#InTermsOfBasicFormsOnFrameBundle), its local pullbacks are related by

$$
  E_j = g_{i j} E_i
$$

i.e. 

$$
  E_j^a = (g_{i j})^a{}_b E_i^b
$$

and hence (eq:Definite3FormsOnTwoPatches) says that

$$
   \phi_{a b c}
   =
   \phi_{a' b' c'} (g_{i j})^{a'}{}_a (g_{i j})^{b'}{}_b (g_{i j})^{c'}{}_c
   \;\;\;
    on \; U_i \cap U_j
$$

which is precisely the defining condition for $g_{i j}$ to take values in $G_2$.

Viewed this way, the [[definite 3-forms]] characterizing $G_2$-structures are an example of a more general kind of differential forms obtained from a constant form on some linear model space $V$ by locally contracting with a [[vielbein]] field. For instance on a [[super-spacetime]] solving the [[equations of motion]] of  [[11-dimensional supergravity]] there is a super-4-form part of the [[field strength]] of the [[supergravity C-field]] which is constrained to be locally of the form

$$
  \Gamma_{a b \alpha \beta} E_i^a \wedge E_i^b \wedge E_i^\alpha \wedge E_i^\beta
$$

for $(E^A)= (E^a, E^\alpha) = (E^a, \Psi^\alpha)$ the [[super-vielbein]].  See at _[Green-Schwarz action functional -- Membrane in 11d SuGra Background](Green-Schwarz+action+functional#MembraneIn11dSuGraBackground)_. Indeed, by the discussion there this 4-form is required to be [[covariant derivative|covariantly constant]], which is precisely the analog of $G_2$-manifold structure as in def. \ref{G2manifold}.

=--

References that write [[definite 3-forms]] in this form locally as $\phi_{a b c}E^a \wedge E^b \wedge E^c$ include ([BGGG 01 (2.9)](#BGGG01), ...).

The following is important for the analysis:

+-- {: .num_remark #Definition3FormsGiveOpenSubset}
###### Remark

The subset $\Lambda^3_+(\mathbb{R}^7)^\ast \hookrightarrow \Lambda^3(\mathbb{R}^7)^\ast $ in def. \ref{Definite3Forms} is an [[open subset]], hence $\phi$ is a _[[stable form]]_ (e.g. [Hitchin, def. 1.1](#Hitchin)).

=--

(e.g. [Joyce 00, p. 243](#Joyce00), [Bryant 05, 2.8](#Bryant05))

+-- {: .proof}
###### Proof

By definition of $G_2$ as the [[stabilizer group]] of the [[associative 3-form]], the [[orbit]] it generates under the $GL_+(7)$-action is the [[coset]] $GL_+(7)/G_2$. The [[dimension]] of this as a [[smooth manifold]] is 49-14 = 35. This is however already the full dimension $\left(7 \atop 3\right) = 35$ of the space of 3-forms in 7d that the orbit sits in. Therefore (since $G_+(7)/G_2$ does not have a [[manifold with boundary|boundary]]) the orbit must be an open subset.

=--



### Closed $G_2$-structure
 {#ClosedG2Structure}


+-- {: .num_defn #ClosedG2Structure}
###### Definition

A $G_2$-structure, def. \ref{G2Structure}, is called _closed_ if the definite 3-form $\sigma$ corresponding to it via prop. \ref{G2StructureViaDefinite3Form} is a closed differential form, $\mathbf{d}\sigma = 0$.

=--

(e.g. [Bryant 05, (4.31)](#Bryant05))

+-- {: .num_prop #ClosedG2StructureByAtlas}
###### Proposition

For a closed $G_2$-structure, def. \ref{ClosedG2Structure}, on a manifold $X$ there exists an [[atlas]] by [[open subsets]] 

$$\mathbb{R}^7 \underoverset{et}{f}{\leftarrow} U \underset{et}{\rightarrow} X$$ 

such that the globally defined 3-form $\sigma \in \Omega^3_+(X)$ is locally gauge equivalent to the canonical [[associative 3-form]] $\phi$

$$
  \sigma|_U = f^\ast \phi + \mathbf{d}\beta
$$

via a 2-form $\beta$ on $U$.

=--

(e.g. [Bryant 05, p. 21](#Bryant05))

This follows from the fact, remark \ref{Definition3FormsGiveOpenSubset}, that the definite 3-forms are an [[open subset]] inside all 3-forms: given a chart centered around any point then there is $\beta$ with $\mathbf{d}\beta$ vanishing at that point such that $\sigma|_U \simeq f^\ast \phi + \mathbf{d}\beta$ at that point. But since the $GL(7)$-action on $\phi$ is open, there is an open neighbourhood around that point where this is still the case.

+-- {: .num_remark #AtlasForClosedG2tructureInTermsOfHigherGeometry}
###### Remark

When regarding [[smooth manifolds]] in the wider context of [[higher differential geometry]], then the situation of prop. \ref{ClosedG2StructureByAtlas} corresponds to a diagram of [[formal smooth infinity-groupoids]] of the following form:

$$
  \array{
    && U
    \\
    & {}^{\mathllap{f}}\swarrow && \searrow
    \\
    \mathbb{R}^7 && \swArrow_{\mathrlap{\beta}} && X
    \\
    & {}_{\mathllap{\phi}}\searrow && \swarrow_{\mathrlap{\sigma}}
    \\
    && \flat_{dR}\mathbf{B}^3\mathbb{R}
  }
  \,,
$$

where $\flat_{dR}\mathbf{B}^3\mathbb{R}$ is the [[moduli infinity-stack|higher moduli stack]] of flat 3-forms with 2-form gauge transformations between them (and 1-form gauge transformation between these). The diagram expresses the 3-form $\sigma$ as a map to this moduli stack, which when restricted to the cover $U$ becomes gauge equivalent to the pullback of the [[associative 3-form]] $\phi$, similarly regarded as a map, to the cover, where the gauge equivalence is exhibited by a [[homotopy]]  (of maps of formal smooth $\infty$-groupoids) which is the 2-form $\beta$ on $U$.

=--




### $G_2$-holonomy / $G_2$-manifold
 {#G2Holonomy}

+-- {: .num_defn #G2manifold}
###### Definition/Proposition

A manifold $X$ equipped with a $G_2$-structure, def. \ref{G2Structure}, is called a **$G_2$-manifold** if the following equivalent conditions hold

1. we have

   1. $\mathbf{d} \omega = 0$ ([closed](#ClosedG2Structure))

   1. $\mathbf{d} \star_g \omega = 0$ (co-closed);

1. $\nabla^g \omega = 0$;

1. $(X,g)$ has [[special holonomy]] $Hol(g) \subset G_2$;

1. $Ric(g) = 0$ (vanishing [[Ricci curvature]]);

1. $R(g) = 0$ (vanishing [[scalar curvature]]);

1. $\tau = 0$ (vanishing [[torsion of a G-structure|torsion of the G2-structure]]).

Here

* $d$ is the [[de Rham differential]];

* $\omega$ is the 3-form $\omega$ corresponding to the given $G_2$-structure via prop. \ref{G2StructureViaDefinite3Form};

* $g$ is the induced [[Riemannian metric]], via remark \ref{CanonicalRiemannianMetric};

* $\star_g$ is the [[Hodge star operator]] of this metric;

* $\nabla^g$ is the [[covariant derivative]] of this metric;

=--

For the equivalence of the first items see for instance [Joyce 96, p. 294 (4 of 38)](#Joyce96), [Joyce 00, prop. 10.1.3](#Joyce00). For the equivalence to the vanishing curvature invariant see also [Bryant 05, corollary 1](#Bryant05), and for the equivalence to the vanishing [[torsion of a G-structure]] see [Bryant 05, prop. 2](#Bryant05).


+-- {: .num_remark}
###### Remark

The higher [[torsion of a G-structure|torsion invariants]] of $G_2$-structures do not necessarily vanish (contrary to the case for instance of [[symplectic structure]] and [[complex structure]], see at *[integrability of G-structures -- Examples](integrability+of+G-structures#Examples)*). Therefore, even in view of prop. \ref{CovariantlyConstantDefinite3FormMeansTorsionVanishes}, a $G_2$-manifold, def. \ref{G2manifold}, does not, in general admit an [[atlas]] by adapted [[coordinate charts]] equal to $(\mathbb{R}^7, \phi)$.

The space of second order torsion invariants of $G_2$-structures is discussed by [Bryant 05 (4.7)](#Bryant05).

=--


### Variants and weakenings
 {#VariantsAndWeakenings}

There are several variants of the definition of $G_2$-manifolds,
def.\ref{G2manifold}, given by imposing other constraints on the [[torsion of a Cartan connection|torsion]].

#### With skew-symmetric torsion

Discussion for totally skew symmetric [[torsion of a Cartan connection]] includes [Friedrich & Ivanov 01, theorem 4.7, theorem 4.8](#FriedrichIvanov01).


#### Weak $G_2$-holonomy
 {#WeakG2Holonomy}


+-- {: .num_defn #WeakG2Holonomy}
###### Definition

A 7-dimensional manifold is said to be of _weak $G_2$-holonomy_ if it carries a 3-form $\omega$ with the relation of def. \ref{G2manifold} generalized to

$$
  \mathbf{d} \omega 
  \;=\; 
  \lambda \star \omega
$$


and hence

$$
  \mathbf{d} \star \omega 
   \;=\; 
  0
$$

for $\lambda \in \mathbb{R}$. For $\lambda = 0$ this reduces to strict $G_2$-holonomy, by \ref{G2manifold}. 

=--

(See for instance [Bilal & Derendinger-Sfetsos 02](#BilalDerendingerSfetsos, [Bilal & Metzger 03](#BilalMetzger03).)

#### With ADE orbifold structure
 {#WithADEOrbifoldStructure}

When used as [[KK-compactification]]-fibers for [[M-theory on G2-manifolds]], then for quadi-realistic [[string phenomenology|phenomenology]] one needs to consider [[ADE orbifolds]] with "$G_2$-manifold" structure, i.e. [[G2-orbifolds]], also called _Joyce orbifolds_. Moreover, for [[F-theory]] purposes this $G_2$-orbifold is to be a [[fiber bundle|fibration]] by a [[K3 surface]] $X_{K3}$. 

For instance, the [[Cartesian product]] $X_{K3} \times T^3$ admits a $G_2$-manifold structure. There is a canonical [[special orthogonal group|SO(3)]]-[[action]] on the tangent spaces of $X_{K3} \times T^3$, given on $X_{K3}$ by rotation of the [[hyper-Kähler manifold]]-structure of $X_{K_3}$ and on $T^3$ by the standard rotation. For $K_{ADE}$ a [[finite group|finite]] [[subgroup]] of $SO(3)$, hence a finite group in the  [[ADE classification]], then $(X_{K3}\times T^3)/K_{ADE}$ is a [[G2-orbifold]] ([Acharya 1098, p.3](#Acharya98)). For $K_{ADE}$ _not_ a [[cyclic group]] then this has precisely one [[parallel spinor]].

In a local [[coordinate chart]] of $X_{K3}$ by $\mathbb{C}^2$ the orbifold $X_{K3}/K_{ADE}$ locally looks like $\mathbb{C}^2/{G_{ADE}}$, where now $G_{ADE}$ is a [[finite group|finite]] [[subgroup]] of [[special unitary group|SU(2)]]. Such local [[G2-orbifolds]] are discussed in some detail by [Atiyah & Witten 2001](#AtiyahWitten01). Families of examples are constructed in [Reidegeld 2015](#Reidegeld15).

Codimension-4 ADE singularities in $G_2$-manifolds are discussed by [Acharya & Gukov 2004, section 5.1](AcharyaGukov04) and [Barrett 2006](#Barrett06).

## Properties

### Existence

+-- {: .num_prop }
###### Proposition

A 7-manifold admits a $G_2$-structure, def. \ref{G2Structure}, precisely if it admits an [[orientation]] and a [[spin structure]].

=--

That orientability and spinnability is necessary follows directly from the fact that $G_2 \hookrightarrow GL(7)$ is connected and simply connected. That these conditions are already sufficient is due to ([Gray 69](#Gray69)), see also ([Bryant 05, remark 3](#Bryant05)).

### Metric structure

The canonical [[Riemannian metric]] $G_2$ manifold is [[Ricci tensor|Ricci flat]]. More generally a manifold of weak $G_2$-holonomy, def. \ref{WeakG2Holonomy}, with weakness parameter $\lambda$ is an [[Einstein manifold]] with [[cosmological constant]] $\lambda$. 

### As part of the Berger classification

[[!include special holonomy table]]

### As $\mathbb{O}$-Riemannian manifolds

[[!include normed division algebra Riemannian geometry -- table]]

### As exceptional geometry

[[!include Spin(8)-subgroups and reductions -- table]]


## Examples
 {#Examples}

### Metric cones

The [[metric cone over complex projective 3-space]] carries the [[mathematical structure|structure]] of  a [[G2-manifold]] whose [[Riemannian metric]] is [[invariant]] under the canonical [[Sp(2)]] [[action]] by left-[[matrix multiplication]] on homomogeneous coordinates in $\mathbb{H}^2 \simeq_{\mathbb{R}} \mathbb{C}^4 \to \mathbb{C}P^3$ ([Byant-Salamon 89](metric+cone+over+complex+projective+3-space#BryantSalamon89), see also [Acharya-Bryant-Salamon 20](metric+cone+over+complex+projective+3-space#AcharyaBryantSalamon20)).


### Resolution of Joyce orbifolds

[[compact topological space|compact]]$\,$[[G2-manifolds]]
by [[resolution of singularities]] in compact [[flat orbifolds]]

([Joyce 96](#Joyce96), [Joyce 00](#Joyce00))

(...) 

### Twisted connected sum construction
 {#TwistedConnectedSumConstruction}

[[compact topological space|compact]] [[G2-manifolds]]
by twisted [[connected sum]]-constructions

([Kovalev 00](#Kovalev00))


\begin{center}
\begin{imagefromfile}
  "file_name": "TwistedConnectedSumG2Manifold.jpg",
  "width": 680
\end{imagefromfile}
\end{center}

> graphics grabbed from [Klemm 16](#Klemm17)



## Applications

### In supergravity 

In [[string phenomenology]] [[model (in particle phyiscs)|models]] obtained from [[Kaluza-Klein mechanism|compactification]] of [[11-dimensional supergravity]]/[[M-theory on G2-manifolds]] (see for instance [Duff](#Duff)) can have attractive [[phenomenology|phenomenological]] properties, see for instance the _[[G2-MSSM]]_. 

## Related concepts

* [[associative submanifold]]

* [[Hitchin functional]]

* [[M-theory on G2-manifolds]], [[G2-MSSM]]

* [[topological M-theory]], [[topological membrane]]

* [[generalized G2-manifold]]

* [[Calabi-Yau manifold]]

* [[exceptional generalized geometry]]

## References

### General

General survey:

* [[Spiro Karigiannis]], _What is... a $G_2$-manifold_ ([pdf](http://www.ams.org/notices/201104/rtx110400580p.pdf))

* [[Spiro Karigiannis]], _$G_2$-manifolds -- Exceptional structures in geometry arising from exceptional algebra_ ([pdf](http://www.math.uwaterloo.ca/~karigian/talks/waterloo.pdf)) 

* {#Karigiannis14} [[Spiro Karigiannis]], _$G_2$-Conifolds: A survey_, 2014 ([pdf](http://www.math.uni-hamburg.de/sgstructures/hamburg-talk-2.pdf))

* {#Hitchin} [[Nigel Hitchin]], _Special holonomy and beyond_, Clay Mathematics Proceedings ([pdf](https://people.maths.ox.ac.uk/hitchin/hitchinlist/clay.pdf))



* {#Bryant05} [[Robert Bryant]], _Some remarks on $G_2$-structures_, [Proceedings of the 12th G&#246;kova Geometry-Topology Conference 2005](http://gokovagt.org/proceedings/2005), pp. 75-109 ([arXiv:math/0305124](https://arxiv.org/abs/math/0305124), [webpage](http://gokovagt.org/proceedings/2005/bryant.html), [pdf](http://gokovagt.org/proceedings/2005/ggt05-bryant.pdf))

The concept of $G_2$-manifolds goes back to 

* E. Bonan, (1966), _Sur les vari&#233;t&#233;s riemanniennes &#224; groupe d'holonomie G2 ou Spin(7)_, C. R. Acad. Sci. Paris 262: 127&#8211;129.

Non-compact $G_2$-manifolds were first  constructed in

* [[Robert Bryant]], [[Simon Salamon]],  _On the construction of some complete metrics with exceptional holonomy_, Duke Mathematical Journal 58: 829&#8211;850 (1989) ([euclid:dmj/1077307681](https://projecteuclid.org/euclid.dmj/1077307681))

See also:

* [[Simon Salamon]], Chapter 11 in: *Riemannian Geometry and Holonomy Groups*, Research Notes in Mathematics **201**, Longman (1989)


[[compact topological space|Compact]] $\;G_2$-manifolds were first found in:

* {#Joyce96} [[Dominic Joyce]], _Compact Riemannian 7-manifolds with holonomy $G_2$_, Journal of Differential Geometry **43** 2 (1996) &lbrack;[Euclid:jdg/1214458109](https://projecteuclid.org/euclid.jdg/1214458109)&rbrack;
 
* {#Joyce00} [[Dominic Joyce]], *Compact manifolds with special holonomy*, Oxford Mathematical Monographs (2000) &lbrack;[ISBN:9780198506010](https://global.oup.com/academic/product/compact-manifolds-with-special-holonomy-9780198506010?cc=us&lang=en&)&rbrack;

Review in:

* [[Dominic Joyce]], _Compact Riemannian manifolds with exceptional holonomy_, Surveys in Differential Geometry
Volume 6 (2001) ([doi:10.4310/SDG.2001.v6.n1.a3](https://dx.doi.org/10.4310/SDG.2001.v6.n1.a3))

* [Kovalev 2020](#Kovalev20)


The sufficiency of spin structure for $G_2$-structure is due to:

* {#Gray69} A. Gray, _Vector cross products on manifolds_, Trans. Amer. Math. Soc. 141 (1969), 465&#8211;504. 

and the [[compact twisted connected sum G2-manifolds]] due to:

* {#Kovalev00} [[Alexei Kovalev]], _Twisted connected sums and special Riemannian holonomy_, J. Reine Angew. Math. 565 (2003) ([arXiv:math/0012189](https://arxiv.org/abs/math/0012189))

Review includes

* {#Kovalev20} [[Alexei Kovalev]], *Constructions of compact $G_2$-holonomy manifolds*, in: *Lectures and Surveys on $G_2$-Manifolds and Related Topics*, Springer (2020) &lbrack;[arXiv:1909.11473](https://arxiv.org/abs/1909.11473), [doi:10.1007/978-1-0716-0577-6_2](https://doi.org/10.1007/978-1-0716-0577-6_2)&rbrack;

and from the point of view of [[M-theory on G2-manifolds]]:

* {#Klemm17} [[Albrecht Klemm]], _Effective Action from M-theory on twisted connected sums_, talk at Ascona Monte Verita, 6 July 2017 ([pdf](http://conf.itp.phys.ethz.ch/string17/talks/Klemm.pdf))

More compact examples are constructed in 

* {#JoyceKarigiannis07} [[Dominic Joyce]], [[Spiro Karigiannis]], _A new construction of compact $G_2$-manifolds by gluing families of Eguchi-Hanson spaces_ &lbrack;[arXiv:1707.09325](https://arxiv.org/abs/1707.09325)&rbrack;



The relation to [[multisymplectic geometry]]/[[2-plectic geometry]] is mentioned explicitly in 

* {#Ibort} Alberto Ibort, _Multisymplectic geometry: generic and exceptional_, _[Proceedings of the IX Fall workshop on geometry and physics](http://rsme.es/public/publi3.htm)_ ([[IbortMultisymplectic.pdf:file]])

  > (but beware of some mistakes in that article)

For more see the references at _[[exceptional geometry]]_.


[[!include G2-conifolds -- references]]


### $G_2$-Orbifolds
 {#ReferencesG2Orbifolds}

Discussion of [[G2-orbifolds]] includes

* {#Acharya98} [[Bobby Acharya]], _M theory, Joyce Orbifolds and Super Yang-Mills_, Adv.Theor.Math.Phys. 3 (1999) 227-248 ([arXiv:hep-th/9812205](http://arxiv.org/abs/hep-th/9812205))

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]] _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

* {#AcharyaGukov04} [[Bobby Acharya]], [[Sergei Gukov]], _M theory and Singularities of Exceptional Holonomy Manifolds_, Phys.Rept.392:121-189,2004 ([arXiv:hep-th/0409191](http://arxiv.org/abs/hep-th/0409191))

* {#Barrett06} Adam B. Barrett, _M-Theory on Manifolds with $G_2$ Holonomy_, 2006 ([arXiv:hep-th/0612096](http://arxiv.org/abs/hep-th/0612096))

* {#Reidegeld15} [[Frank Reidegeld]], _$G_2$-orbifolds from K3 surfaces with ADE-singularities_ ([arXiv:1512.05114](http://arxiv.org/abs/1512.05114), [spire:1409963](https://inspirehep.net/literature/1409963), [doi:10.17877/DE290R-18940](http://dx.doi.org/10.17877/DE290R-18940))

* [[Frank Reidegeld]], _K3 surfaces with a pair of commuting non-symplectic involutions_ ([arXiv:1809.07501](https://arxiv.org/abs/1809.07501))

* [[Bobby Acharya]], [[Andreas Braun]], Eirik Eik Svanes, Roberto Valandro,  _Counting Associatives in Compact $G_2$ Orbifolds_ ([arXiv:1812.04008](https://arxiv.org/abs/1812.04008))

* Daniel Platt, _Existence of torsion-free $G_2$-structures on resolutions of $G_2$-orbifolds using weighted Hölder norms_ ([arXiv:2011.00482](https://arxiv.org/abs/2011.00482))


### Moduli

Discussion of the [[moduli space]] of $G_2$-structures:


* {#GrigorianYau08} [[Sergey Grigorian]], [[Shing-Tung Yau]], _Local geometry of the $G_2$ moduli space_, Commun.Math.Phys.287:459-488,2009 ([arXiv:0802.0723](http://arxiv.org/abs/0802.0723))

* [[Spiro Karigiannis]], [[Naichung Conan Leung]], _Hodge Theory for G2-manifolds: Intermediate Jacobians and Abel-Jacobi maps_, Proceedings of the London Mathematical Society (3) 99, 297-325 (2009) &lbrack;[arXiv:0709.2987](http://arxiv.org/abs/0709.2987), [talk slides pdf](http://www.math.uwaterloo.ca/~karigian/talks/g2modulispace.pdf)&rbrack;

Relating to moduli of [[flat connections]] on [[tori]]:

* [[Bobby S. Acharya]], Daniel A. Baldwin, *Ricci Flat Metrics, Flat Connections and $G_2$-Manifolds* &lbrack;[arXiv:2312.12311](https://arxiv.org/abs/2312.12311)&rbrack;



### Variants and generalizations

Discussion of the more general concept of Riemannian manifolds equipped with [[covariant derivative|covariantly constant]] 3-forms is in 

* [[Hông Vân Lê]] , _Geometric structures associated with a simple Cartan 3-form_, J. of Geometry and Physics 70 (2013) 205--223 [arXiv:1103.1201](https://arxiv.org/abs/1103.1201)

### Relation to Killing spinors

Discussion of $G_2$-structures in view of the existence of [[Killing spinors]] includes

* {#FriedrichIvanov01} [[Thomas Friedrich]], Stefan Ivanov, _Parallel spinors and connections with skew-symmetric torsion in string theory_, AsianJ.Math.6:303-336,2002 ([arXiv:math/0102142](http://arxiv.org/abs/math/0102142))

### Application in supergravity

The following references discuss the role of $G_2$-manifolds in [[M-theory on G2-manifolds]]:

* {#Duff} [[Mike Duff]], _M-theory on manifolds of G2 holonomy: the first twenty years_ ([arXiv:hep-th/0201062](http://arxiv.org/abs/hep-th/0201062))
 

A survey of the corresponding [[string phenomenology]] for [[M-theory on G2-manifolds]] (see there for more) is in

* [[Bobby Acharya]], _$G_2$-manifolds at the CERN Large Hadron collider and in the Galaxy_, talk at _$G_2$-days_ (2012) ([pdf](http://www.mth.kcl.ac.uk/~tbmadsen/acharya.pdf))

See also

* {#BGGG01} [[Andreas Brandhuber]], [[Jaume Gomis]], [[Steven Gubser]], [[Sergei Gukov]], _Gauge Theory at Large N and New $G_2$ Holonomy Metrics_, Nucl.Phys. B611 (2001) 179-204 ([arXiv:hep-th/0106034](http://arxiv.org/abs/hep-th/0106034))

Weak $G_2$-holonomy is discussed in

* {#BilalDerendingerSfetsos} [[Adel Bilal]], J.-P. Derendinger, K. Sfetsos, _(Weak) $G_2$ Holonomy from Self-duality, Flux and Supersymmetry_, Nucl.Phys. B628 (2002) 112-132 ([arXiv:hep-th/0111274](http://arxiv.org/abs/hep-th/0111274))
 

* {#BilalMetzger03} [[Adel Bilal]], Steffen Metzger, _Compact weak $G_2$-manifolds with conical singularities_ ([arXiv:hep-th/0302021](http://arxiv.org/abs/hep-th/0302021))

* {#HouseMicu04} Thomas House, [[Andrei Micu]], _M-theory Compactifications on Manifolds with $G_2$ Structure_ ([arXiv:hep-th/0412006](http://arxiv.org/abs/hep-th/0412006))

For more on this see at _[[M-theory on G2-manifolds]]_

### Cohomology

An analysis of the [[de Rham complex]] of $G_2$ manifolds, and an analogue of [[Dolbeault cohomology]] is in

* Marisa Fernández, Luis Ugarte. *Dolbeault Cohomology for $G2$-Manifolds*. Geometriae Dedicata 70, 57–86 (1998). ([doi](https://doi.org/10.1023/A:1004940807017))




[[!redirects G2 manifolds]]
[[!redirects G2-manifold]]
[[!redirects G2-manifolds]]

[[!redirects G2 structure]]
[[!redirects G2-structure]]
[[!redirects G2 structures]]
[[!redirects G2-structures]]

[[!redirects G2-holonomy]]
[[!redirects G2-holonomies]]

[[!redirects weak G2-holonomy]]
[[!redirects weak G2 holonomy]]

[[!redirects twisted connected sum G2-manifold]]
[[!redirects twisted connected sum G2-manifolds]]

[[!redirects compact twisted connected sum G2-manifold]]
[[!redirects compact twisted connected sum G2-manifolds]]

[[!redirects compact twisted connected sum G2-manifold]]
[[!redirects compact twisted connected sum G2-manifolds]]


