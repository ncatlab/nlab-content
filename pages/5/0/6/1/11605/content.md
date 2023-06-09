
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Traditionally the $(k+1)$st _intermediate Jacobian variety_ $J^{k+1}(\Sigma)$ of a [[complex analytic space]] $\Sigma$ is the [[quotient]] of its [[ordinary cohomology]] in degree $2k+1$ with [[real number]] [[coefficients]] by that with [[integer]] coefficients

$$
  J^{k+1}(\Sigma) \coloneqq H^{2k+1}(\Sigma, \mathbb{R}) / H^{2k+1}(\Sigma, \mathbb{Z})
  \,.
$$

This space naturally carries the structure of a [[complex manifold]] (in fact two such structures, named after Griffiths and after Weil) and this complex analytic space, which is in fact a _[[complex torus]]_, is properly what is called the $(k+1)$st _intermediate Jacobian variety_ of $\Sigma$. This terminology derives from the term _[[Jacobian variety]]_ which is the (historically earlier) special case for $k = 0$ and $dim_{\mathbb{C}}(\Sigma) = 1$.

Notice that, conceptually, we may (cf. at *[[Deligne cohomology]]* the [exact sequences](Deligne+cohomology#ExactSequenceForCurvatureAndCharacteristicClass) and generally at *[[differential cohomology hexagon]]*):

* think of $H^{2k+1}(\Sigma,\mathbb{R})$ as the space of those [[circle n-bundle with connection|$n$-form connections]] on $\Sigma$ which are both [[flat infinity-connection|flat]] and have trivial [[underlying]] [[line n-bundle|line $n$-bundle]];

* think of $H^{2k + 1}(\Sigma,\mathbb{Z})$ as the group of "large" (i.e.: not connected to the identity) [[higher gauge field|higher]] [[gauge transformations]] acting on these gauge fields;

* hence understand $J^{k+1}(\Sigma)$ as the [[moduli space]] of flat $n$-form connections on trivial underlying line $n$-bundles.

This turns out to be a natural and  useful perspective on intermediate Jacobians: _Deligne's theorem_ (discussed as theorem \ref{DeligneTheorem} below) characterizes the intermediate Jacobians as subgroups of the relevant [[Deligne cohomology]] group of $\Sigma$, where [[Deligne cohomology]] is a model for [[ordinary differential cohomology]] that classifies these [[circle n-bundle with connection|line n-bundles with connection]]. Moreover, as discussed in Rem. \ref{AsFiberOf0TruncationOnFractureSquare} below, Deligne's theorem in the formulation of [Esnault & Viehweg (1988)](#EsnaultViehweg88) may be rephrased such as to manifestly give a formal incarnation of the the statement that $J^{k+1}(\Sigma)$ is just that subgroup of the Deligne complex given by [[circle n-bundle with connection|line $n$-connections]] with trivial [[curvature]] and trivial [[underlying]] [[line n-bundle|line $n$-bundle]].

This formulation, in turn, has an evident generalization from [[ordinary differential cohomology]] to general (namely [[Whitehead-generalized cohomology|Whitehead-generalized]]) [[differential cohomology]], which we discuss further [below](#GeneralDescripion).

This perspective on intermediate Jacobians from [[higher gauge theory]] also faithfully reflects their role in fundamental [[physics]] (in [[quantum field theory]] and [[string theory]]) &lbrack;[Witten (1996)](#Witten96), [Hopkins & Singer (2002)](#HopkinsSinger02)&rbrack;. Here [[higher dimensional Chern-Simons theory]] has as [[field (physics)|fields]] certain [[higher gauge fields]] specified by some type of [[differential cohomology]], and the [[connected components]] of its [[phase space]] (of solutions to the [[equations of motion]]) is precisely the corresponding intermediate Jacobian. Moreover the [[transgression]] of the higher Chern-Simons [[action functional]] produces a [[line bundle]] on the intermediate Jacobian, which is the [[prequantum line bundle]] of the theory. By [[geometric quantization]] one has to choose a [[Kähler polarization]] for this line bundle and the Weil complex structure on $J^{k+1}(\Sigma)$ is precisely that.
In terms of [[complex geometry]] this state of affairs directly translates into the statement that the Weil intermediate Jacobians are [[polarized varieties]]. In fact they are [[principally polarized variety|principally polarized]], which on the physics side corresponds to the [[metaplectic correction]] of the [[Kähler polarization]] used for [[geometric quantization]]. The [[holomorphic section]] of the resulting [[Theta characteristic]] on the intermediate Jacobian is physically the [[partition function]] of [[self-dual higher gauge theory]] on $\Sigma$ (see there for more) which mathematically is the corresponding [[theta function]].

By way of these deep relations intermediate Jacobians play an important role in ([[higher geometry|higher]]) [[geometry]].

## Definition

### For differential ordinary cohomology
 {#InComplexGeometry}

#### The underlying real manifold

Let $\Sigma$ be a [[projective variety|projective]] [[smooth variety|smooth]] [[complex variety]] (see at _[[GAGA]]_). 

+-- {: .num_defn #PlainIJacobian}
###### Definition

For $k \in \mathbb{N}$ the _$k$th intermediate Jacobian_ of $\Sigma$ is, as a [[real manifold]], the [[quotient]]

$$
  J^{k+1}(\Sigma) 
    \coloneqq 
  H^{2k+1}(\Sigma,\mathbb{R})/H^{2k+1}(\Sigma,\mathbb{Z})
$$

of the [[ordinary cohomology|ordinary]] [[cohomology groups]] of $X$ with [[coefficients]] in the [[abelian groups]] of [[real numbers]] and of [[integers]], respectively, induced by the canonical inclusion $\mathbb{Z} \hookrightarrow \mathbb{R}$.

=--

Here $H^{2k+1}(\Sigma,\mathbb{R})$ is naturally a [[vector space]] over the [[real numbers]] and this is what induces the [[smooth manifold]]-structure on the quotient. 

For the purpose of eventually equipping this with the [[structure]] of a [[complex manifold]] one may realizes it as the quotient of the [[complex vector space]] of [[complex cohomology|complex]] [[ordinary cohomology]], as follows:

+-- {: .num_remark}
###### Remark

A real [[differential form]] 

$$
  \alpha 
  \;\in\; 
  \Omega^{2k+1}_{\mathbb{R}}(\Sigma)
$$

is, by the [[Hodge theorem]], a sum of complex differential forms in homogeneous [[Dolbeault complex|Dolbeault bidegree]] of the form

$$
  \alpha 
  \;=\; 
   \alpha^{2k+1,0}+ \alpha^{2k,1} 
     + 
     \cdots 
      + 
     \alpha^{k+1,k}
      +
     \overline{\alpha^{k+1,k}} 
     + 
     \cdots
     +
     \overline{\alpha^{2k,1}} + \overline{\alpha^{2k+1,0}}
  \,,
$$

where

$$
  \overline{(-)} 
  \;\colon\; 
  \Omega^{p,q}(\Sigma)\longrightarrow \Omega^{q,p}(\Sigma)
$$

is the [[antilinear function]] on complex differential forms given by [[complex conjugation]].

=--

It follows with the [[de Rham theorem]] that:

+-- {: .num_prop #AsQuotientByHodgeFiltering}
###### Proposition

There is a canonical [[isomorphism]] of [[real vector spaces]]

$$
  H^{2k+1}(\Sigma, \mathbb{R}) 
   \;\simeq\; 
  H^{2k+1}(\Sigma,\mathbb{C})/(F^{k+1} H^{2k+1}(\Sigma,\mathbb{C}))
 \,,
$$

where 

$$
  F^{k+1} H^{2k+1}(\Sigma,\mathbb{C}) 
  \;\coloneqq\; 
  \underset{p \geq k+1}{\oplus} H^{p,2k+1-p}(\Sigma)
$$

is the $(k+1)$st stage in the [[Hodge filtration]] of $H^{2k+1}(\Sigma,\mathbb{C})$. 

=--

Hence an equivalent way of writing the intermediate Jacobian (still as a real manifold) is as the [[quotient space]] of the real manifold underlying a complex vector space, as follows:

+-- {: .num_prop}
###### Proposition

The intermediate Jacobian of def. \ref{PlainIJacobian} is equivalently

$$
  J^{k+1}(\Sigma)
  \;\simeq\;
   H^{2k+1}(\Sigma,\mathbb{C})
   /
  \big(
    F^{k+1} H^{2k+1}(\Sigma, \mathbb{C}) 
    \,\oplus\, 
    H^{2k+1}(\Sigma,\mathbb{Z})
  \big)
  \,.
$$

=--

Yet one more reformulation is useful when properly working in [[complex analytic geometry]]/[[GAGA]]:

+-- {: .num_defn #ModuliOfHolomorphickConnections}
###### Definition

Write $\big(\mathbf{B}^k \mathbb{G}_a\big)_{conn}$ for the [[abelian sheaf]] of [[chain complexes]] on [[site]] of [[complex manifolds]] which assigns the truncated [[de Rham complexes]] of [[holomorphic differential forms]]:

$$
  \big(\mathbf{B}^k \mathbb{G}_a\big)_{conn}
  \;\coloneqq\;
  \left(
    \mathcal{O}
     \stackrel{\partial }{\to}
    \Omega^{1}
      \stackrel{\partial}{\to}
      \cdots
      \stackrel{\partial}{\to}
    \Omega^{k}
  \right)
$$

regarded as sitting in degrees $k$ to 0.

=--

(e.g. [Esnault & Viehweg (1988), top of p. 14](#EsnaultViehweg88))

+-- {: .num_prop #ReplacingHodgeFiltrationQuotientByHolomorphicConnections}
###### Proposition

The quotient in prop. \ref{AsQuotientByHodgeFiltering}
is equivalently the [[abelian sheaf cohomology|abelian sheaf]] 
[[hypercohomology]] with [[coefficients]]
in $\mathbf{B}^{2k}\mathbb{G}_a$ of def. \ref{ModuliOfHolomorphickConnections}:

$$
  H^{2k+1}\big(
    \Sigma
    ,\,
    \mathbb{C}
  \big)
  /
  F^{k+1} 
  H^{2k+1}(\Sigma, \mathbb{C})
  \;\simeq\;
  \Big[
    \Sigma
    ,\, 
    \mathbf{B}^k\big(\mathbf{B}^k \mathbb{G}_a\big)_conn 
  \Big]
  \,.
$$

=--

(e.g. [Esnault & Viehweg (1988), 2.5 b)](#EsnaultViehweg88)).


There are two canonical ways of equipping $H^{2k+1}(\Sigma,\mathbb{C})$, and hence the above quotient, with the structure of a [[complex manifold]]. Sometimes these agree, but in general they do not, and hence they go by different names:

1. *[Griffith intermediate Jacobian](#GriffithIntermediateJacobian)*,

1. *[Weil intermediate Jacobian](#WeilIntermediateJacobian)*.


#### Characterization as Hodge-trivial Deligne cohomology
 {#CharacterizationAsHodgeTrivialDeligneCohomology}

A theorem due to [[Pierre Deligne]] says that the intermediate Jacobian $J^k(\Sigma)$ is characterised as being the [[fiber]] of a canonical map from ([[complex analytic geometry|complex analytic]]) [[Deligne cohomology]] to the $k$th [[Hodge filtration]] of [[integral cohomology]]. 


+-- {: .num_defn #HodgeCohomologyClasses}
###### Definition

The group $Hdg^{k+1}(\Sigma)$ of _[[Hodge cocycle|Hodge cohomology classes]]_ is the subgroup of $\mathbb{Z}(k+1)$-cohomology classes whose image in complex cohomology is in the $(k+1)$st stage of the [[Hodge filtration]], hence the group sitting in the following [[pullback]] diagram

$$
  \array{
     Hdg^{k+1}(\Sigma) 
       &\longrightarrow& 
     F^{k+1} H^{2k+2}(\Sigma;\,\mathbb{C})
     \\
     \Big\downarrow 
     &{}^{{}_{(pb)}}& 
     \Big\downarrow
     \\
     H^{2k+2}\big(\Sigma;\,\mathbb{Z}(k+1)\big)
       &\longrightarrow&
     H^{2k+2}(\Sigma;\,\mathbb{C})
     \mathrlap{\,.}
  }
$$

=--

The following says this in a [[complex analytic geometry|complex analytic]]-way that generalizes:

+-- {: .num_prop #HodgeCyclesAsPullbackOfHolomorphic}
###### Proposition

Equivalently, the Hodge cohomology classes of def. \ref{HodgeCohomologyClasses} are given by the [[pullback]]

$$
  \array{
     Hdg^{k+1}(\Sigma) 
       &\longrightarrow& 
     H^{2k+2}\big(\Sigma;\, \Omega^{\bullet \geq k+1}\big)
     \\
     \Big\downarrow && \Big\downarrow
     \\
     H^{2k+2}\big(\Sigma;\,\mathbb{Z}(k+1)\big)
       &\longrightarrow&
     H^{2k+2}(\Sigma;\,\mathbb{C})
  }
  \,,
$$

where now in the top right we have the [[abelian sheaf cohomology|abelian sheaf]] [[hypercohomology]] with [[coefficients]] in the [[holomorphic de Rham complex]], truncated (but otherwise unshifted) as indicated.

=--

([Esnault & Viehweg (1988), section 7.8](#EsnaultViehweg88))

+-- {: .num_theorem #DeligneTheorem}
###### Theorem
**(Deligne)**

As an [[abelian group]] the intermediate Jacobian $J^k(\Sigma)$, def. \ref{PlainIJacobian}, is the [[fiber]] of the canonical map from [[Deligne cohomology]] to Hodge cohomology classes, has as fitting into a [[short exact sequence]] of the following form:

$$
  0 
    \to 
  J^{k+1}(\Sigma)
    \longrightarrow
  H^{2k+2}\big(\Sigma;\, \mathbb{Z}(k+1)_{D}\big) 
    \longrightarrow 
  Hdg^{k+1}(\Sigma) 
    \to 
  0
  \,.
$$

=--

(e.g. [Esnault & Viehweg (1988), (7.9)](#EsnaultViehweg88); [Peters & Steenbrink (2008), lemma 7.20](#PetersSteenbrink08))

+-- {: .proof}
###### Proof

Use prop. \ref{ReplacingHodgeFiltrationQuotientByHolomorphicConnections} and the [characteristic long exact sequences](ordinary%20differential%20cohomology#CurvatureAndCharClass) of [[ordinary differential cohomology]].

=--


+-- {: .num_remark #AsFiberOf0TruncationOnFractureSquare}
###### Remark

The [[fiber product]]-incarnation of $Hdg^{k+1}(\Sigma)$ in prop. \ref{HodgeCyclesAsPullbackOfHolomorphic} is noteworthy in that it
is analogous to the [[homotopy fiber]]-characterization of the 
holomorphic [[Deligne complex]] itself.

Consider the following [[diagram]] of [[sheaves of chain complexes]]
on the site $SteinSp$ of [[Stein manifolds]] (see at _[[complex analytic ∞-groupoid]]_ for more on this):

$$
  \array{
    \mathbb{Z}(p)[-2k-2]
     && &&
     \Omega^{\bullet \geq k+1}[-2k-2]
     \\
     & \searrow && \swarrow
     \\
     && \mathbb{C}[-2k-2]
  }
  \,.
$$

This is just of the form as discussed in some detail at _[[circle n-bundle with connection]]_ and also at _[[differential cohomology diagram]]_ in the section on _[Deligne coefficients](differential+cohomology%20diagram#DeligneCoefficients)_. In particular the [[homotopy limit]] over this diagram -- hence the [[homotopy fiber]] of the two maps -- is a version of the [[Deligne complex]]:

$$
  \array{
     &&\mathbb{Z}(p)_D[-2k-2]
     \\
     && = 
     \\
     &&(\mathbb{Z}(p) \to \mathcal{O} \to \Omega^1 \to \cdots \to \Omega^{k} \to 0 \to \cdots)[-2k-2]
     \\
     & \swarrow && \searrow
    \\
    \mathbb{Z}(p)[-2k-2]
     && (hpb) &&
     \Omega^{\bullet \geq k+1}[-2k-2]
     \\
     & \searrow && \swarrow
     \\
     && \mathbb{C}[-2k-2]
  }
  \,.
$$

Since [[homotopy pullbacks]] are preserved by foming [[mapping spaces]] into them, this statement holds true after evaluating on $\Sigma$ (which produces the [[Cech cohomology|Cech-]][[Deligne complexes]]). Forming the [[n-truncated object of an (infinity,1)-category|0-truncation]] $\tau_0$ of the result gives the differential cohomology group $H^{2k+2}(\Sigma, \mathbb{Z}(k+1)_{D})$ 
appearing in theorem \ref{DeligneTheorem}.

Alternatively, first passing to the 0-truncation of the diagram and then producing the pullback yields the Hodge cocycle group of prop. \ref{HodgeCyclesAsPullbackOfHolomorphic}.

Accordingly, the statement of theorem \ref{DeligneTheorem} may equivalently be rephrased in the following more suggestive way:

the intermediate Jacobian $J^{k+1}(\Sigma)$ is the [[fiber]] in

$$
  J^{k+1}(\Sigma)
   \longrightarrow
  \tau_0\left(
     [\Sigma,\mathbb{Z}(p)[-2k-2]]
     \underset{[\Sigma, \mathbb{C}[-2k-2]]}{\times}
     \Omega^{\bullet \geq k+1}[-2k-2]
  \right)
  \longrightarrow
  \tau_0 [\Sigma,\mathbb{Z}(p)[-2k-2]]
   \underset{\tau_0 [\Sigma, \mathbb{C}[-2k-2]]}{\times}
  \tau_0 [\Sigma, \Omega^{\bullet \geq k+1}[-2k-2]]
  \,.
$$

=--

This formulation of the intermediate Jacobian has a
straightforward generalization from [[ordinary differential cohomology]] to [[differential cohomology|differential]] [[Whitehead-generalized cohomology]]. This we turn to [below](#GeneralDescripion).


#### The Griffith complex structure
 {#GriffithIntermediateJacobian}

The [[isomorphism]]

$$
  H^{2k+1}(\Sigma , \mathbb{C})
  \simeq 
  H^{2k+1}(\Sigma , \mathbb{R})\otimes_{\mathbb{R}} (\mathbb{C})
$$

induces a [[complex manifold]] structure on $H^{2k+1}(\Sigma , \mathbb{C})$ and hence the structure of a [[complex torus]] on $k$th intermediate Jacobian as defined above. This is the structure originally defined in ([Griffiths 68a](#Griffiths68a), [Griffiths 68b](#Griffiths68b)) and hence called the _Griffith intermediate Jacobian_.  Reviews include ([Walls (2012)](#Walls12), [Esnault & Viehweg (1988), section 7.8](#EsnaultViehweg88)).


#### The Weil complex structure
 {#WeilIntermediateJacobian}

There is another natural [[complex structure]] on $H^{2k-1}(X, \mathbb{R})/H^{2k-1}(X, \mathbb{Z})$, equipped with that it is called the _Weil intermediate Jacobian_.

Let as before $n \,\coloneqq\, dim_{\mathbb{C}}(\Sigma)$.
Choose a [[Hermitian manifold]] structure on $\Sigma$. Then [[Serre duality]] on forms of total odd degree

$$
  \bar \star \;\colon\; \Omega^{p,2k+1-p}(\Sigma) \longrightarrow \Omega^{n-p-2k-1,p}(\Sigma)
$$

is an [[antilinear function]] which squares to -1. Therefore

$$
 i \bar \star \;\colon\;  H^{2k+1}(\Sigma,\mathbb{C}) \to  H^{2k+1}(\Sigma,\mathbb{C})
$$

is a [[real structure]] on $H^{2k+1}(\Sigma,\mathbb{C})$. This hence defines a [[complex manifold]] structure on $H^{2k+1}(\Sigma,\mathbb{C})$ and hence on the above [[quotient]] which is the intermediate Jacobian $J^{k+1}(\Sigma)$. As such this is the _Weil intermediate Jacobian_.

#### The polarized mid-dimensional Weil (Lazzeri) intermediate Jacobian
 {#MidDimensionalWeilIntermediateJacobian}

The Weil intermediate Jacobian is particularly interesting in mid degree, hence if

$$
  n =dim_{\mathbb{C}}(\Sigma) = 2k+1
$$

then for $J^{k+1}(\Sigma)$. This case is also known as _Lazzeri's Jacobians_ see ([Rubei 98](#Rubei98)).

In this case the [[intersection pairing]] 

$$
  (\alpha, \beta) \mapsto \int_{\Sigma}\alpha \wedge \beta
$$

defines a [[symplectic form]], for which the [[Hodge star]] operator is a compatible [[complex structure]] and hence the [[Serre duality]]-pairing

$$
  (\alpha, \beta) \mapsto \int_{\Sigma}\alpha \wedge \star \beta
$$

is the corresponding [[Kähler manifold|Kähler]]. This makes the Weil intermediate Jacobian a [[polarized variety]].

Notice that the holomorphic coordinates in

$$
  ker \tfrac{1}{2}( 1 + i \bar \star  ) \in H^{2k+1}(\Sigma, \mathbb{C})
$$

may be thought of as the mid-degree [[self-dual higher gauge fields]] on $\Sigma$. From this point of view the above is the [[Kähler polarization]] of the [[prequantum line bundle]] on [[higher dimensional Chern-Simons theory]] in dimension $4k+3$.


#### The intermediate Jacobian of a Hodge structure

By prop. \ref{AsQuotientByHodgeFiltering} above
the intermediate Jacobian is defined by the canonical 
[[Hodge filtering]] on complex [[ordinary cohomology]].
The definition obtained this way directly generalizes to 
other [[Hodge structures]] $H$ and hence one
speaks more generally of the intermediate Jacobian

$$
  J(H)= H_{\mathbb{C}}/(H_\mathbb{Z}\oplus F^{k+1})
$$

if $H$ has weight $2k+1$.

(e.g. [Peters-Steenbrink 08, example 3.30, section 7.1.2](#PetersSteenbrink08))


### For differential generalized cohomology
 {#GeneralDescripion}

#### General construction

> under construction, see also ([Hopkins-Quick 12](#HopkinsQuick12))...

The formulation of the traditional intermediate 
Jacobian by remark \ref{AsFiberOf0TruncationOnFractureSquare}
above suggest the following generalization.

(We use notation from _[[differential cohomology hexagon]]_).

Given any [[differential cohomology]] [[spectrum]] $\hat E$ (hence a [[spectrum object]]) in a [[cohesive (∞,1)-topos]] $\mathbf{H}$, it sits in its [[differential cohomology hexagon]] part of which is the [[homotopy pullback]]

$$
  \array{
    && \flat_{dR} \hat E
    \\
    & {}^{\mathllap{\theta_{\hat E}}}\nearrow && \searrow
    \\
    \hat E && && \Pi \flat_{dR} \hat E
    \\
    & \searrow && \nearrow_{\mathrlap{ch_{\hat E}}}
    \\
    && \Pi \hat E
  }
  \,.
$$

Hence for any $\Sigma$ also the [[mapping spectra]]

$$
  \array{
    && [\Sigma, \flat_{dR} \hat E]
    \\
    & {}^{\mathllap{\theta_{\hat E}}}\nearrow && \searrow
    \\
    [\Sigma, \hat E] && && [\Sigma, \Pi \flat_{dR} \hat E]
    \\
    & \searrow && \nearrow_{\mathrlap{ch_{\hat E}}}
    \\
    && [\Sigma, \Pi \hat E]
  }
  \,.
$$


Write $\tau_0 \colon \mathbf{H}\to \mathbf{H}$ for the [[n-truncated object in an (infinity,1)-category|0-truncation]] map and consider the [[fiber product]] $Hdg(\Sigma,E)$ in

$$
  \array{
    && \tau_0 [\Sigma, \flat_{dR} \hat E]
    \\
    & {}^{\mathllap{\theta_{\hat E}}}\nearrow && \searrow
    \\
    Hdg(\Sigma,\hat E) && && \tau_0 [\Sigma, \Pi \flat_{dR} \hat E]
    \\
    & \searrow && \nearrow_{\mathrlap{ch_{\hat E}}}
    \\
    && \tau_0[\Sigma, \Pi \hat E]
  }
  \,.
$$

We may call this the _Hodge cohomology_ of $\Sigma$ with coefficients in $\hat E$.
The evident morphism of diagrams induces a morphism

$$
  [\Sigma, \hat E]\longrightarrow Hdg(\Sigma, \hat E)
$$

and the [[homotopy fiber]] of that 

$$
  \mathbf{J}(\Sigma,\hat E)
    \longrightarrow  
   [\Sigma, \hat E]\longrightarrow Hdg(\Sigma, \hat E)
$$

we may call the _intermediate Jacobian $\infty$-stack_ of $\Sigma$ with coefficients in $\hat E$.

Notice that by commutativity of [[homotopy pullbacks]] with [[homotopy fibers]], this is equivalently the homotopy pullback in

$$
  \array{
    && ker([\Sigma,\flat_{dR}\hat E] \to \tau_0[\Sigma,\flat_{dR}\hat E] )
    \\
    & \nearrow && \searrow
    \\
    \mathbf{J}(\Sigma,\hat E) && && ker([\Sigma,\Pi \flat_{dR}\hat E] \to \tau_0[\Sigma,\Pi \flat_{dR}\hat E] )

    \\
    & \searrow && \nearrow
    \\
    && ker([\Sigma,\Pi\hat E] \to \tau_0[\Sigma,\Pi\hat E] )
  }
  \,.
$$

In this form this manifestly says that $\mathbf{J}(\Sigma,\hat E)$ is precisely the differential cohomology theory of $\Sigma$ obtained from $\hat E$ by restricting to trivial curvature and trivial underlying $\Pi(E)$-cohomology.

#### For complex K-theory 
 {#ForComplexKTheory}

Intermediate Jacobians of [[K-theory]] classes were considered in the [[physics]]-style literature in ([Witten 99, section 4.3](#Witten99), [Moore-Witten 99, section 3](#MooreWitten99), [DMW 00, section 7.1](#MW00), [Belov-Moore 06b, section 5](#BelovMooreII)) as a means for [[quantization]] of the [[RR-field]] in [[type II superstring theory]] as a [[self-dual higher gauge theory]] (see there at _[Examples -- RR-fields in 10d](self-dual%20higher%20gauge%20theory#RRFieldsin10d)_). A mathematical discussion inspired by this is in ([MPS 11](#MPS11)).





## Properties

### Relation between the Griffiths and the Weil complex structure
 {#RelationBetweenGriffithsAndWeilStructure}

While the Griffiths complex structure on the intermediate Jacobian is not K&#228;hler/not an [[polarized variety|algebraic polarization]] as the Weil complex structure is, it still has an [[p-convex polarization]] and there is a [[symplectomorphism]] which is an [[isomorphism]] between the Griffiths and the Weil intermediate Jacobians as real symplectic manifolds

$$
  (J^{k+1}(X), \omega_{Griffiths})
  \simeq
  (J^{k+1}(X), \omega_{Weil})
  \,.
$$

This is due to ([Griffiths 68b](#Griffiths68b)), recalled as [Griffiths 12 (2.6)](#Griffiths12)

(...)

### Cycle map / Abel-Jacobi map

The intermediate Jacobians receive canonical maps from cycles (...)
See at _[[Abel-Jacobi map]]_.

### Polarization

For a [[Hodge manifold]] the intermediate Jacobian canonically inherits the structure of a [[polarized variety]]. (...)


### Theta-characteristics

A certain [[square root]] of the [[canonical bundle]] on intermediate Jacobians -- hence a [[Theta characteristic]] -- in dimension $2k+1$ thought of as [[moduli spaces]] of (flat) [[circle n-bundles with connection|circle (2k+1)-bundles with connection]] yields the [[partition function]] of [[self-dual higher gauge theory]].  ([Witten 96](#Witten96), [Hopkins-Singer 02](#HopkinsSinger02)).


### Relation to Artin-Mazur formal groups
 {#RelationToArtinMazurFormalGroups}

By theorem \ref{DeligneTheorem} the [[formal geometry]]
of intermediate Jacobians around their canonical point is equivalently the [[deformation theory]] of [[Deligne cohomology]]/[[line n-bundles with connection]]. This is given by (when it exists) the [[Artin-Mazur formal group]]
for [deformations of Deligne cohomology](Artin-Mazur+formal+group#DeformationsOfDeligneCohomology) (see there).

## Examples

The two extreme cases of intermediate Jacobians $J^k(\Sigma)$ with minimal $k = 0$ and maximal $k = dim_{\mathbb{C}}(\Sigma)= 1$ go by special names, the

* [Picard variety](#ExamplePicard)

* [Albanese variety](#ExampleAlbanese)

respectively.

Of special interest are also the intermediate Jacobian

* [of Calabi-Yau varieties](#ExampleCY).

### $k = 0$: the Picard variety $J^1(\Sigma)$
 {#ExamplePicard}

+-- {: .num_prop #J1IsPicard}
###### Proposition

The intermediate Jacobian $J^1(\Sigma)$, def. \ref{PlainIJacobian}, of a [[complex curve]] ($dim_{\mathbb{C}}(\Sigma) = 1$) coincides with the connected component $Pic_0(\Sigma)$ of the [[Picard variety]] $Pic(\Sigma)$ of $\Sigma$, hence with the [[Jacobian variety]] $Jac(\Sigma)$:

$$
  J^1(\Sigma) = Pic_0(\Sigma) = Jac(\Sigma)
  \,.
$$

=--

First consider the elementary proof by direct inspection (e.g. [Polishchuk 03, section 16.4](#Polishchuk03)):

+-- {: .proof}
###### Proof

Notice that the canonical map 

$$
  H^1(\Sigma,\mathbb{R})
  \hookrightarrow 
  H^1(\Sigma, \mathbb{C})
  \to
  H^{0,1}(\Sigma)
  \stackrel{\simeq}{\to} H^1(\Sigma, \mathcal{O}_{\Sigma})
$$ 

is an [[isomorphism]]. The first map is induced by the splitting $H^1(\Sigma, \mathbb{C}) \simeq H^1(\Sigma,\mathbb{R})\oplus i H^1(\Sigma,\mathbb{R})$ given by [[complexification]] and the second by the splitting $H^1(\Sigma,\mathbb{C}) \simeq H^{0,1}(\Sigma)\oplus H^{1,0}(\Sigma)$ of [[Dolbeault cohomology]], the last map is the [[Dolbeault isomorphism]].

Therefore by the [[long exact sequence in cohomology]] of the [[exponential exact sequence]] we have that

$$
  \begin{aligned}
  J^1(\Sigma)
  & \coloneqq
  H^1(\Sigma, \mathbb{R})/H^1(\Sigma, \mathbb{Z})
  \\
  & \simeq
  H^1(\Sigma,\mathcal{O}_{\Sigma})/H^1(\Sigma, \mathbb{Z}) 
  \\
  & \simeq
  ker(H^1(\Sigma, \mathcal{O}^\times_{\Sigma})\to H^2(\Sigma, \mathbb{Z}))
  \\
  & = 
  Pic_0(\Sigma)
  \end{aligned}
$$

is the connected component of the [[Picard variety]] of $\Sigma$.

=--

Alternatively, prop. \ref{J1IsPicard}
derives from theorem \ref{DeligneTheorem} as follows:

+-- {: .proof}
###### Proof

Since $k = 0$ then $\mathbf{B}^2\mathbb{Z}(k+1)_D\simeq \mathbf{B}\mathbb{G}_m$ is just the universal moduli stack of line bundles without connection and so $H^{2k+2}(\Sigma, \mathbb{Z}(k+1)_D ) \simeq H(\Sigma,\mathbf{B}\mathbb{G}_m)$ is the full [[Picard variety]]. The fiber in the exact sequence in theorem \ref{DeligneTheorem} then restricts this to the elements which have trivial [[first Chern class]], hence the [[Jacobian variety]].

=--

+-- {: .num_remark #GeneralizationToModuliOfGPrincipalConnections}
###### Remark

There is a [[non-abelian cohomology|non-abelian]] generalization of this statement that the [[moduli space of flat connections|moduli space of]] real bundles with flat connections is equivalently a moduli space of complex-analytic bundles, but without connection. This is a corollary of the [[Narasimhan-Seshadri theorem]] (for $dim_{\mathbb{C}}\Sigma = 1$) or of the [[Donaldson-Uhlenbeck-Yau theorem]] (for [[Kähler manifolds]] $\Sigma$) and generally of the [[Kobayashi-Hitchin correspondence]] (for arbitrary complex $\Sigma$), stated for instance as ([Scheinost-Schottenloher 96, corollary 1.16](#ScheinostSchottenloher96)):

the moduli space of [[flat connection|flat]] [[special unitary group|SU(n)]]-[[principal connections]] on $\Sigma$ is equivalently the moduli space of [[special linear group|SL(n,C)]]-[[holomorphic vector bundles]] which have vanishing [[Chern classes]] and are [[stable vector bundle|semi-stable]].

=--


### $k = n-1$: Albanese variety 
 {#ExampleAlbanese}

For $\Sigma$ any space of complex dimension 
$n \coloneqq dim_{\mathbb{C}}(\Sigma)$ then 
with $k = n-1$ the $(k+1)$st intermediate Jacobian 
is built from cohomology in degree one less than the real dimension of $\Sigma$:

$$
  J^{n-1}(\Sigma) = H^{2k-1}(\Sigma,\mathbb{R})/H^{2k-1}(\Sigma, \mathbb{Z})
  \,.
$$

This $(n-1)$st intermediate Jacobian is known as the _[[Albanese variety]]_ of $\Sigma$.


### Of Calabi-Yau varieties
 {#ExampleCY}

A review of intermediate Jacobians of [[Calabi-Yau varieties]] of ([[complex manifold|complex]]) [[dimension]] 3 is in ([Baarsma 11, section 2](#Baarsma11)).

The (real) dimensional of the intermediate Jacobian of a CY3 $X$ is 

$$
  dim (J(X)) = 2(1+ h^{1,2})
$$

(e.g. [Baarsma 11, (2.21)](#Baarsma11))

Hence the intermediate Jacobian of a rigid CY3 (with $h^{1,2} = 0$) is an [[elliptic curve]] (e.g. [BKNPP 09, (1.8)](#BKNPP09)).

### $n = 3$: supergravity C-field

For the moment see at _[[7d Chern-Simons theory]]_ and at _[[M5-brane]]_.

### $n = 3$: type II 3-form 

For the [[RR-field]] component in degree 4 of [[type IIA superstring theory]]: ([Morrison 95](#Morrison95))


## Related concepts

[[!include moduli of higher lines -- table]]


## References

### In ordinary differential cohomology

#### General

The definition of the Griffith intermediate Jacobian is due to

* {#Griffiths68a} [[Phillip Griffiths]], _Periods of integrals on algebraic manifolds. I_ Construction and properties of the modular varieties", American Journal of Mathematics 90 (2): 568&#8211;626, (1968) &lbrack;doi:10.2307/2373545, ISSN 0002-9327, JSTOR 2373545, MR 0229641&rbrack;

* {#Griffiths68b} [[Phillip Griffiths]], _Periods of integrals on algebraic manifolds. II_ Local study of the period mapping", American Journal of Mathematics 90 (3): 805&#8211;865 (1968) &lbrack;doi:10.2307/2373485, ISSN 0002-9327, JSTOR 2373485, summary:[[GriffithsPeriodsSummary.pdf:file]], MR 0233825 &rbrack;


A review including also the Weil complex structure is in 

* {#Griffiths12} [[Phillip Griffiths]], section 1 of _Some results on algebraic cycles on algebraic manifolds_, Proceedings of the International Conference on Algebraic Geometry, Tata Institute (Bombay), 2012 ([web](http://publications.ias.edu/node/181), [pdf](http://publications.ias.edu/sites/default/files/someresultsonalg.pdf))

For $k = 0$ but with generalization to non-abelian [[moduli space of flat connections]] the Grifiths-like follows also with the [[Donaldson-Uhlenbeck-Yau theorem]] as discussed in 

* {#ScheinostSchottenloher96} Peter Scheinost, [[Martin Schottenloher]], pp. 154 (11 of 76) of _Metaplectic quantization of the moduli spaces of flat and parabolic bundles_, J. reine angew. Mathematik, 466 (1996) ([web](https://eudml.org/doc/153753)) 

The mid-dimensional case was discussed in unpublished work by Lazzeri, see

* {#Rubei98} Elena Rubei, _Lazzeri's Jacobian of oriented compact riemannian manifolds_ ([arXiv:math/9812110](http://arxiv.org/abs/math/9812110))

The relation of the intermediate Jacobian to [[Deligne cohomology]] (Deligne's theorem) due to [[Pierre Deligne]] is discussed in

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], Section 7 of: _Deligne-Beilinson cohomology_, in: [[Michael Rapoport]], [[Norbert Schappacher]], [[Peter Schneider]] (eds.), _[[Beilinson's Conjectures on Special Values of L-Functions]]_  Perspectives in Mathematic **4**, Academic Press, Inc. (1988) &lbrack;ISBN:978-0-12-581120-0, [[EsnaultViehweg-DeligneBeilinsonCohomology.pdf:file]]&rbrack;

Reviews and surveys include

* [[eom]], _[Intermediate Jacobian](http://www.encyclopediaofmath.org/index.php/Intermediate_Jacobian)_


* Wikipedia, _[Intermediate Jacobian](http://en.wikipedia.org/wiki/Intermediate_Jacobian)_

* {#Walls12} [[Patrick Walls]], _Intermediate Jacobians and Abel-Jacobi maps_, 2012 ([[WallsJacobian.pdf:file]])

* {#Brylinski07} [[Jean-Luc Brylinski]], around theorem I 1.5.11 of _Loop Spaces, Characteristic Classes and Geometric Quantization_ Springer, 2007

* [[Arnaud Beauville]], _Vari&#233;t&#233;s de Prym et jacobiennes interm&#233;diaire_,  Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 10 no. 3 (1977), p. 309-391   ([pdf](http://math.unice.fr/~beauvill/pubs/prym.pdf)) ([jstor]( http://www.numdam.org/item?id=ASENS_1977_4_10_3_309_0))

* Valentin Zakharevich, _Mixed Intermediate Jacobians_, 2012 ([pdf](http://www.algant.eu/documents/theses/zakharevich.pdf))

* {#Polishchuk03} [[Alexander Polishchuk]], _Abelian varieties, Theta functions and the Fourier transform_, Cambridge University Press (2003) ([pdf](http://math1.unice.fr/~beauvill/pubs/poli.pdf))

Discussion of the generalization to [[Hodge structures]] includes

* {#PetersSteenbrink08} [[Chris Peters]], [[Jozef Steenbrink]], _[[Mixed Hodge Structures]]_, Ergebisse der Mathematik (2008) ([pdf](http://www.arithgeo.ethz.ch/alpbach2012/Peters_Steenbrinck))

* [pdf](http://www-fourier.ujf-grenoble.fr/~peters/world.f/Torino.pdf)

#### For Calabi-Yau 3-folds

Discussion of intermediate Jacobians of [[Calabi-Yau 3-folds]] includes

* C. Herbert Clemens, [[Phillip Griffith]], _The intermediate Jacobian of the cubic threefold_, Annals of Mathematics Second Series, Vol. 95, No. 2 (Mar., 1972), pp. 281-356 ([JSTOR](http://www.jstor.org/stable/1970801))

* [[Claire Voisin]] ([pdf](http://www.math.polytechnique.fr/~voisin/Articlesweb/griffithsgroup.pdf))

* [[Andreas Höring]], _Minimal classes on the intermediate Jacobian of a generic cubic threefold_, 2008 ([pdf](http://math.unice.fr/~hoering/articles/a5-intermediate.pdf))

In [[positive number|positive]] [[characteristic]]:

* {#GeerKatsura03} [[Gerard van der Geer]], T. Katsura, _On the height of Calabi-Yau varieties in positive characteristic_ ([arXiv:math/0302023](http://arxiv.org/abs/math/0302023))

Applications in [[string theory]]:

* {#Morrison95} [[David Morrison]], section 4 of _Mirror Symmetry and the Type II String_, Nucl.Phys.Proc.Suppl. 46 (1996) 146-155 ([arXiv:hep-th/9512016](http://arxiv.org/abs/hep-th/9512016))

* {#DDP06} Diaconescu, [[Ron Donagi]], [[Tony Pantev]], _Intermediate Jacobians and ADE Hitchin Systems_ ([arXiv:hep-th/0607159](http://arxiv.org/abs/hep-th/0607159))

* {#BKNPP09} Ling Bao, Axel Kleinschmidt, Bengt E. W. Nilsson, Daniel Persson, Boris Pioline, _Instanton Corrections to the Universal Hypermultiplet and Automorphic Forms on SU(2,1)_, Commun. Num. Theor. Phys. 4 (1), 187-266 (2010) ([arXiv:0909.4299](http://arxiv.org/abs/0909.4299))

* {#Baarsma11} A. Baarsma, _The hypermultiplet moduli space of compactified type IIA string theory_, Master Thesis, Utrecht 2011 ([web](http://dspace.library.uu.nl/handle/1874/203182))


The relation of Theta characteristics on [[intermediate Jacobians]] to [[self-dual higher gauge theory]] was first recognized in 

* {#Witten96} [[Edward Witten]], *Five-Brane Effective Action In M-Theory*, J. Geom. Phys. **22** (1997) 103-133 &lbrack;[arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234)&rbrack;

and the argument there was made rigorous in 

* {#HopkinsSinger02} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_ (2005)

### For generalized cohomology

Intermediate Jacobians of [[K-theory]] classes were discussed in the [[physics]] literature context of [[self-dual higher gauge theory]] for [[RR-fields]] in

* {#Witten99} [[Edward Witten]], _Duality Relations Among Topological Effects In String Theory_, JHEP 0005:031,2000 ([arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086))

* {#MooreWitten99} [[Gregory Moore]], [[Edward Witten]], _Self-Duality, Ramond-Ramond Fields, and K-Theory_, JHEP 0005:032,2000 ([arXiv:hep-th/9912279](http://arxiv.org/abs/hep-th/9912279))

* {#MW00} D. Diaconescu, [[Gregory Moore]], [[Edward Witten]], _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv.Theor.Math.Phys.6:1031-1134,2003 ([arXiv:hep-th/0005090](http://arxiv.org/abs/hep-th/0005090)), summarised in _A Derivation of K-Theory from M-Theory_ ([arXiv:hep-th/0005091](http://arxiv.org/abs/hep-th/0005091))

* {#BelovMooreII} Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv:hep-th/0611020](http://arxiv.org/abs/hep-th/0611020))

A mathematical discussion inspired by this is in 


* {#MPS11} [[Stefan Müller-Stach]], Chris Peters, Vasudevan Srinivas, _Abelian varieties and theta functions associated to compact Riemannian manifolds; constructions inspired by superstring theory_ ([arXiv:1105.4108](http://arxiv.org/abs/1105.4108), [pdf slides](http://www-fourier.ujf-grenoble.fr/~peters/world.f/Torino.pdf))

A discussion of intermediate Jacobians for any rationally periodic [[generalized (Eilenberg-Steenrod) cohomology]] theory is in 

* {#HopkinsQuick12} [[Michael Hopkins]], [[Gereon Quick]], _Hodge filtered complex bordism_ ([arXiv:1212.2173](http://arxiv.org/abs/1212.2173))
 
[[!redirects intermediate Jacobians]]

[[!redirects higher Jacobian]]
[[!redirects higher Jacobians]]


[[!redirects Griffith intermediate Jacobian]]
[[!redirects Griffith intermediate Jacobians]]

[[!redirects Weil intermediate Jacobian]]
[[!redirects Weil intermediate Jacobians]]