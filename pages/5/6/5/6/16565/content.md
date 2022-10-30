
> this page is one chapter of _[[geometry of physics]]_

> previous chapters: _[[geometry of physics -- manifolds and orbifolds|manifolds and orbifolds]]_, _[[geometry of physics -- WZW terms|WZW terms]]_

***

> under construction

#Contents#
* table of contents
{:toc}

### Motivation and results

Consider $(X,g)$ a [[super-spacetime]] and $\omega$ a degree $(p+2)$-differential form on $X$ which is a [[geometry of physics -- WZW terms|WZW]] [[curvature form]]  [[definite form|definite]] on the [[super Lie algebra]] [[Lie algebra cohomology|cocycle]] 

$$
  \overline \psi \wedge \Gamma^{a_1 \cdots a_p} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
  \in 
  CE(\mathbb{R}^{d-1,1\vert N})
$$ 

for [[Green-Schwarz super p-brane sigma model]] with [[target space]] $X$.  Then the [Polyvector extensions](super+Poincare+Lie+algebra#PolyvectorExtensions)  

$$
  [Q_\alpha, Q_\beta] = (\Gamma^a C)_{\alpha\beta} P_a + (\Gamma^{a_1\cdots a_p}C)_{\alpha \beta} Z_{a_1\cdots a_p}
$$

of the [[super Lie algebra]] of [[super-isometries]]  of $(X,g)$ by [[charges]] $Z$ of [[Noether currents]] of the [[super p-brane sigma model]] are known as algebras of _[[BPS charges]]_. (The spacetime $(X,g,\omega)$ is called a _[[supergravity]] $\frac{1}{k}$-[[BPS state]]_ if the dimension of the space of [[supercharges]] $Q$ in the [[kernel]] of the above bracket is $\frac{1}{k}$th of that of [[super Minkowski spacetime]]). 

This is well understood in the literature ([Azc&#225;rraga-Gauntlett-Izquierdo-Townsend 89](#AGIT89)) for the case that $X$ is locally modeled on an ordinary [[super Minkowski spacetime]] and that the $p$-brane species is in the _old_ [[brane scan]] (e.g the [[type II superstrings]], the [[heterotic superstring]] and the [[M2-brane]], also e.g. the [[super 1-brane in 3d]] and the [[3-brane in 6d]], but not the [[D-branes]] and not the [[M5-brane]]). 

For the full story of [[string theory]] this needs to be refined in three ways (see [[schreiber:The brane bouquet|Fiorenza-Sati-Schreiber 13]]), and this has been left open in the literature, for previous lack of a [[higher differential geometry]] that could handle this:

1. For a genuine global definition of the [[Green-Schwarz super p-brane sigma model]] with target $(X,\omega)$, the WZW [[curvature]] form $\omega$ needs to be [[prequantization|prequantized]] to a globally well-defined [[geometry of physics -- WZW terms|WZW term]], a genuine [[cocycle]] in [[Deligne cohomology]] (a [[circle n-bundle with connection|circle (p1+1)-bundle with connection]]).

   (The need for this has broadly been ignored, one place where it is mentioned is ([Witten 86, p. 17](#Witten86)).)

1. For the inclusion of $p_2$-brane charges of $p_2$-branes on which $p_1$-branes may end (for $p_1 = 1$: [[type II strings]] ending on [[D-branes]], for $p_1= 2$ and $p_2 = 5$ [[M2-branes]] ending on [[M5-branes]]) then $X$ is to be locally modeled on an [[extended super Minkowski spacetime]], hence on a [[super formal smooth infinity-groupoid|super orbispace]], hence a curved spacetime now is an object in [[higher Cartan geometry]] and one needs to make sense of [[Noether currents]] there.

   (Arguments in this direction for the [[D-branes]] have been given in ([Hammer 97](BPS+state#Hammer97)) and for the [[M5-brane]] in ([Sorokin-Townsend 97](BPS+state#SorokinTownsend97)).)

1. For inclusion of non-infinitesimal isometries one needs the global structure of the full [[supergroup]] of BPS charges, not just its [[super Lie algebra]].

Here we discuss how to solve these problems in full generality. Specified to the situation in [[11-dimensional supergravity]] with [[M2-branes]] and [[M5-branes]] we find that the BPS charges traditionally seen in the [[M-theory super Lie algebra]] as living in [[ordinary cohomology]] $H^5(X) \oplus H^2(X)$ receive corrections by $d_4$-differentials of a [[Serre spectral sequence]] given by [[cup product]] with the class of the [[supergravity C-field]] in higher analogy to how [[D-brane charges]] are well known ([Maldacena-Moore-Seiberg 01](D-brane#MaldacenaMooreSeiberg01)) to be in [[ordinary cohomology]] only up to corrections of $d_3$-differential (and higher) in an [[Atiyah-Hirzebruch spectral sequence]] for [[twisted K-theory]],given by [[cup product]] with the class of the [[B-field]]. This supports the conjecture ([Sati 10](M5-brane+charge#Sati10)) that [[M5-brane charge]] should really be in [[twisted generalized cohomology|twisted]] [[elliptic cohomology]], since this is canonically twisted by these degree-4 classes [Ando-Blumberg-Gepner 10](tmf#ABG10).

We also close a gap in ([AGIT89](#AGIT89)): what is strictly derived there from the [[Noether theorem]] is extension of the [[supersymmetry]] algebra by [[differential forms]], while the argument that it is only the [[de Rham cohomology]] class of these forms that matters relies on physics intuition. We find here that the [[Lie algebra]] of [[conserved currents]] extending the (super-)isometry algebra is naturally not just a ([[super Lie algebra|super-]])[[Lie algebra]] but a ([[super L-infinity algebra|super-]])[[Lie n-algebra]] including higher order symmetries  of Noether symmetries. It is by quotienting these out when restricting the current Lie $n$-algebra to its lowest [[Postnikov tower|Postnikov stage]] that current forms pass to their de Rham equivalence classes.  Accordingly, the fully globalized current groups that we find are really ([[super smooth infinity-groupoid|super-]])[[smooth infinity-group|smooth n-groups]]. For instance the [[M-theory super Lie algebra]] is refines to a super Lie 6-group, where $6 = 5+1$ is the dimension of the [[M5-brane]] [[worldvolume]].

$\,$

We formulate the theory general abstractly in  the context of [[higher differential geometry]] given by an [[(∞,1)-topos]] $\mathbf{H}$ equipped with [[cohesion]] and [[differential cohesion]]. The application to [[supergravity]] takes place in the model $\mathbf{H} =$ [[SuperFormalSmooth∞Grpd]].

### Prerequisites

#### Homotopy stabilizer groups

(Recalled from _[[geometry of physics -- representations and associated bundles]]_.)


For $\mathbf{H}$ an [[(∞,1)-topos]],  $G\in \mathbf{H}$ an object equipped with [[∞-group]] structure, hence with a [[delooping]] $\mathbf{B}$G, and for $\rho$ an [[∞-action]] of $G$ on some $V$, exhibited by a [[homotopy fiber sequence]] of the form

$$
  \array{
    V &\stackrel{i}{\longrightarrow}& V/G
    \\
    && \downarrow^{\mathrlap{p_\rho}}
    \\
    && \mathbf{B}G
  }
  \,.
$$



+-- {: .num_defn #StabilizerInInfinityTopos}
###### Definition

Given a [[global element]] of $V$

$$
  x \colon \ast \to X 
$$

then the **stabilizer $\infty$-group** $Stab_\rho(x)$ of the $G$-action at $x$ is the [[loop space object]]

$$
  Stab_\rho(x) \coloneqq \Omega_{i(x)} (X/G)
 \,.
$$

=--

+-- {: .num_defn #StabilizerGroupAsFactorization}
###### Remark

Equivalently, def. \ref{StabilizerInInfinityTopos}, gives the [[loop space object]] of the [[1-image]] $\mathbf{B}Stab_\rho(x)$ of the morphism

$$
  \ast \stackrel{x}{\to} X \to X/G
  \,.
$$

As such the [[delooping]] of the stabilizer $\infty$-group sits in a [[1-epimorphism]]/[[1-monomorphism]] factorization $\ast \to \mathbf{B}Stab_\rho(x) \hookrightarrow X/G$ which combines with the homotopy fiber sequence of prop. \ref{InfinityAction} to a diagram of the form

$$
  \array{
    \ast &\stackrel{x}{\longrightarrow}& X &\stackrel{}{\longrightarrow}& X/G
    \\
    \downarrow^{\mathrlap{epi}} && & \nearrow_{\mathrlap{mono}} & \downarrow
    \\
    \mathbf{B} Stab_\rho(x)
    &=&
    \mathbf{B} Stab_\rho(x)
    &\longrightarrow&
    \mathbf{B}G
  }
 \,.
$$

In particular there is hence a canonical homomorphism of $\infty$-groups

$$
  Stab_\rho(x) \longrightarrow G
  \,.
$$

However, in contrast to the classical situation, this morphism is not in general a monomorphism anymore, hence the stabilizer $Stab_\rho(x)$ is not a _sub_-group of $G$ in general.

=--


#### Higher Kostant-Souriau extensions
 {#KSExtensions}

(Recalled from _[[geometry of physics -- prequantum geometry]]_)

Throughout, let $\mathbb{G} \in Grp(\mathbf{H})$ be a [[braided ∞-group]] equipped with a [[Hodge filtration]]. Write $\mathbf{B}\mathbb{G}_{conn}\in $ for the corresponding [[moduli stack]] of [[differential cohomology]].

+-- {: .num_example #StandardChoiceOfBGconn}
###### Example

For $\mathbf{H} = $ [[Smooth∞Grpd]] we have $\mathbb{G} = \mathbf{B}^p (\mathbb{R}/\Gamma)$ for $\Gamma = \mathbb{Z}$ is the [[circle n-group|circle (p+1)-group]]. Equipped with its standard Hodge filtration this gives $\mathbf{B}\mathbb{G}_{conn} = \mathbf{B}^p U(1)_{conn}$ presented via the [[Dold-Kan correspondence]] by the [[Deligne complex]] in degree $(p+2)$.

=--


+-- {: .num_defn #DifferentialConcretification}
###### Definition

For $X \in \mathbf{H}$, for 
 write 

$$
  conc \colon [X,\mathbf{B}\mathbb{G}_{conn}] \longrightarrow \mathbb{G}\mathbf{Conn}(X)
$$

for the [[differential concretification]] of the [[internal hom]].

=--

This is the proper [[moduli stack]] of $\mathbb{G}$-[[principal ∞-connections]] on $X$ in that a family $U \longrightarrow \mathbb{G}\mathbf{Conn}(X)$ is a _vertical_ $\mathbb{G}$-principal $\infty$-connection on $U \times X\to U$.

+-- {: .num_example }
###### Example

For $\mathbf{H} = $[[Smooth∞Grpd]] or =[[FormalSmooth∞Grpd]], for $\mathbb{G} = \mathbf{B}^p U(1)$ the [[circle n-group|circle (p+1)-group]] with its standard Hodge filtration as in example \ref{StandardChoiceOfBGconn}, then for $X$ any [[smooth manifold]] or [[formal smooth manifold]], $(\mathbf{B}^p U(1))\mathbf{Conn}(X)$ is presented via the [[Dold-Kan correspondence]] by the sheaf $U \mapsto Ch_\bullet$ of [[vertical differential form|vertical]] [[Deligne complexes]] on $U \times X$ over $U$. 

=--

+-- {: .num_defn }
###### Proposition

For $\mathbb{G}$ not [[0-truncated]] then the [[loop space object]] of the moduli stack of $\mathbb{G}$-principal $\infty$-connections on $X$ is the moduli stack of [[flat ∞-connections]] with gauge group $\Omega \mathbb{G}$

$$
  \Omega_0 (\mathbb{G}\mathbf{Conn}(X))
  \simeq
  (\Omega\mathbb{G})\mathbf{FlatConn}(X)
  \,.
$$

=--

+-- {: .num_prop #PrecompositionActionOnGConn}
###### Proposition

The canonical [[precomposition action|precomposition]] [[∞-action]] of the [[automorphism ∞-group]] $\mathbf{Aut}(X)$ on $[X,\mathbf{B}\mathbb{G}_{conn}]$ passes along $conc$ to an [[∞-action]] on $\mathbb{G}\mathbf{Conn}(X)$.

=--

+-- {: .num_defn #QuantomorphismGroup}
###### Definition


Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$ there are the following concepts in [[schreiber:Higher geometric prequantum theory|higher geometric prequantum theory]].


1. The **[[quantomorphism ∞-group]]**is the [[stabilizer ∞-group]] of $\nabla \in \mathbb{G}\mathbf{Conn}(X)$, def. \ref{DifferentialConcretification}, under the $\mathbf{Aut}(X)$-action of \ref{PrecompositionActionOnGConn};

   $$
     \mathbf{QuantMorph}(X,\nabla)
     \coloneqq
     \mathbf{Stab}_{\mathbf{Aut}(X)}(conc(\nabla))
     \,.
   $$

1. The **[[Hamiltonian symplectomorphism ∞-group]]** 


   $$
     \mathbf{HamSymp}(X,\nabla) \longrightarrow \mathbf{Aut}(X)
   $$ 

   is the [[1-image]] of the canonical morphism $\mathbf{QuantMorph}(X,\nabla) \longrightarrow \mathbf{Aut}(X)$ from remark \ref{StabilizerGroupAsFactorization}.

1. A **[[Hamiltonian action]]** of an [[∞-group]] $G$ on $(X,\nabla)$ is an [[∞-group]] homomorphism 

   $$
     \rho \colon G \longrightarrow \mathbf{HamSymp}(X)
      \;
   $$


1. An **[[∞-moment map]]**  is an $\infty$-group homomorphism 

   $$
     G \longrightarrow \mathbf{QuantMorph}(X,\nabla)
   $$

1. The **[[Heisenberg ∞-group]]** for a given Hamiltonian $G$-action $\rho$ is the [[homotopy pullback]] 

   $$
     \mathbf{Heis}_G(\nabla) \coloneqq \rho^\ast \mathbf{QuantMorph}(\nabla)
     \,.
   $$

=--

+-- {: .num_example }
###### Example

For $\mathbf{H} = $ [[Smooth∞Grpd]], for $X \in SmoothMfd \hookrightarrow \mathbf{H}$ a [[smooth manifold]] and for $\nabla$ a [[prequantum line bundle]] on $X$, then $\mathbf{QuantMorph}(X,\nabla)$ is Soriau's [[quantomorphism group]] covering the [[Hamiltonian diffeomorphism]] group. In the case that $(X, F_\nabla)$ is a [[symplectic vector space]] regarded as a linear symplectic manifold with Hamiltonian action on itself by translation, then $\mathbf{Heis}_{V}(\nabla)$ is the traditional [[Heisenberg group]].

=--


+-- {: .num_remark }
###### Remark

Since $\mathbf{HamSymp}(\nabla)\hookrightarrow \mathbf{Aut}(X)$ is by construction a [[1-monomorphism]], then given any $G$-action $\rho \colon G \longrightarrow \mathbf{Aut}(X)$ on $X$, not necessarily Hamiltonian, then the homotopy pullback $\rho^\ast \mathbf{QuantMorph}(\nabla)$ is the Heisenberg ∞-group of the maximal sub-$\infty$-group of $G$ which does act via Hamiltonian symplectomorphisms. Therefore we will also write $\mathbf{Heis}_G(\nabla)$ in this case.

=--

The following is the refinement of the [[Kostant-Souriau extension]] to [[higher differential geometry]]

+-- {: .num_prop }
###### Proposition

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, there is a [[homotopy fiber sequence]] of the form

$$
  \array{
     (\Omega \mathbb{G})\mathbf{FlatConn}(X)
     &\longrightarrow&
     \mathbf{QuantMorph}(X,\nabla)
     \\
     && \downarrow
     \\
     && \mathbf{HamSymp}(X,\nabla)
     &\stackrel{\mathbf{KS}}{\longrightarrow}&
     \mathbf{B} ((\Omega \mathbb{G})\mathbf{Conn}(X))
  }
$$

exhibiting the [[quantomorphism ∞-group]] as an [[∞-group extension]] of the [[Hamiltonian symplectomorphism ∞-group]] by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}$.

=--


+-- {: .num_cor }
###### Corollary

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, and for $\rho \colon G \longrightarrow$ a $G$-[[Hamiltonian action]], then there is a [[homotopy fiber sequence]]

$$
  \array{
     (\Omega \mathbb{G})\mathbf{FlatConn}(X)
     &\longrightarrow&
     \mathbf{Heis}_G(X,\nabla)
     \\
     && \downarrow
     \\
     && G
     &\stackrel{\mathbf{KS}(\rho)}{\longrightarrow}&
     \mathbf{B} ((\Omega \mathbb{G})\mathbf{Conn}(X))
  }
$$

exhibiting the [[Heisenberg ∞-group]] as an [[∞-group extension]] of the [[Hamiltonian symplectomorphism ∞-group]] by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}(\rho)$.


The class of the [[cocycle]] $\mathbf{KS}(\rho)$ is the [[obstruction]] to prequantizing $\rho$ to a [[moment map]] (the _[[classical anomaly]]_ of $\rho$, ); and the the [[Heisenberg ∞-group]] [[∞-group extension|extension]] of $G$ is the universal cancellation of this anomaly.

=--


#### Fiber $\infty$-bundles

(recalled from _[[geometry of physics -- representations and associated bundles]]_)

+-- {: .num_defn}
###### Definition

Given $V,E\in \mathbf{H}$, a _$V$-[[fiber ∞-bundle]]_ $E$ over $X$ is a [[bundle]] $E \in \mathbf{H}_{/X}$ such that there exists a [[cover]] (i.e. a [[1-epimorphism]]) $U \longrightarrow X$ and a [[homotopy pullback]] [[diagram]] of the form

$$
  \array{
    U \times V &\longrightarrow& E
    \\
    \downarrow && \downarrow
    \\
    U &\longrightarrow& X
  }
  \,.
$$

=--

+-- {: .num_defn #AssociatedBundles}
###### Definition

Given an [[∞-group]] $G$ and a $G$-[[∞-action]] on $V$, and given an $G$-[[principal ∞-bundle]] $P \in \mathbf{H}_{/X}$ [[modulating morphism|modulated]] by $\mathbf{c} \colon X \longrightarrow \mathbf{B}G$, then the _[[associated ∞-bundle]]_ is $V$-[[fiber ∞-bundle]] $E = P \times_G V$ which is the [[homotopy pullback]] in

$$
  \array{
     P \times_G V &\longrightarrow& V/G
     \\
     \downarrow && \downarrow
     \\
     X &\stackrel{\mathbf{c}}{\longrightarrow}& \mathbf{B}G
  }
  \,.
$$

A $V$-fiber bundle realized this way is said to have _structure group_ $G$.

=--


+-- {: .num_prop #FiberBundlesAreAssociated}
###### Proposition

Every $V$-[[fiber ∞-bundle]] is the [[associated ∞-bundle]], def. \ref{AssociatedBundles}, of some $\mathbf{Aut}(V)$-[[principal ∞-bundle]].

=--

+-- {: .num_defn #ReductionLiftOfStructureGroup}
###### Definition

Given a $G$-[[principal ∞-bundle]] $P$ [[modulating morphism|modulated]] by some $\mathbf{c}\colon X \longrightarrow \mathbf{B}G$, and given a [[homomorphism]] of [[∞-groups]] $H \hookrightarrow$, then a _[[reduction and lift of structure groups|reduction/lift of the structure group]]_ is a lift $\hat {\mathbf{c}}$ in 

$$

  \array{
    && \mathbf{B}G
    \\
    &{}^{\mathllap{\hat{\mathbf{c}}}}\nearrow& \downarrow
    \\
    X &\stackrel{\simeq}{\longrightarrow}& \mathbf{B}G
  }
  \,.
$$

Similarly for $V$-[[fiber ∞-bundles]] via def. \ref{AssociatedBundles}, prop. \ref{AssociatedBundles}.

=--

### Definite forms


+-- {: .num_prop #FunctionsOnTotalSpacesAreSectionsOfFunctionBundle}
###### Proposition

Given a a $V$-[[fiber ∞-bundle]] $E$ over $X$, and given any [[coefficient]] $A$, there is a [[natural equivalence]] beween 


* morphisms $E \longrightarrow A$;

* sections of the canonically [[associated ∞-bundle]] $P \times_{\mathbf{Aut}(V)} [V,A]$ over $X$.

=--

+-- {: .num_defn #DefiniteSection}
###### Definition

Given an $F$-[[fiber ∞-bundle]] $E$ over $X$, and a [[global element]] $x\colon \ast \to F$ then a [[section]] $\sigma$ of $E$ is _definite on $x$ if

$$
  \array{
    && \ast 
    \\
    & \nearrow & \downarrow^{\mathrlap{x}}
    \\
    X & \stackrel{\sigma}{\longrightarrow} & F/\mathbf{Aut}(F)
    \\
    & \searrow & \downarrow
    \\
    && \mathbf{B}\mathbf{Aut}(F)
  }
$$

=--

+-- {: .num_prop #DefiniteSectionsAndReductionOfStructureGroup}
###### Proposition

Choices of sections definite on $x$ are equivalent to [[reduction of structure groups|reductions of the structure group]], def. \ref{ReductionLiftOfStructureGroup}, along the [[stabilizer group]] map $Stab_\mathbf{Aut}(V)(x)\longrightarrow \mathbf{Aut}(V)$.


=--

+-- {: .num_defn #DefiniteParameterization}
###### Definition

Given $\mathbf{c} \colon V \longrightarrow A$, and given a $V$-[[fiber ∞-bundle]] $E$ over $X$, then a _definite parameterization of $\mathbf{c}$ over $E$_ is a $\mathbf{c}^E \colon E \longrightarrow A$ such that the section $\sigma_{\mathbf{c}^X}$ coresponding to it via prop. \ref{FunctionsOnTotalSpacesAreSectionsOfFunctionBundle} is definite on $\mathbf{c}$ in the sense of def. \ref{DefiniteSection}.

=--

+-- {: .num_defn #DefiniteGlobalization}
###### Definition

For $V$ an [[∞-group]], $\mathbf{L}\colon V \longrightarrow \mathbf{B}\mathbb{G}_{conn}$ a [[geometry of physics -- WZW terms|WZW term]], and for $X$ a $V$-[[geometry of physics -- manifolds and orbifolds]], then a _[[definite globalization of WZW terms|definite globalization]]_ of $\mathbf{L}$ over $X$ is 

1. A [[reduction of the structure group]], def. \ref{ReductionLiftOfStructureGroup}, of the [[frame bundle]] of $X$ along $\mathbf{Aut}_{Grp}(V) = \mathbf{Aut}^{\ast/}(\mathbf{B}V) \longrightarrow \mathbf{Aut}(V)$;

1. an $\mathbf{L}^X \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$ such that its pullback $T_{inf} X \to X \stackrel{\mathbf{L}^X}{\longrightarrow} \mathbf{B} \mathb{G}_{conn}$ to the [[infinitesimal disk bundle]] of $X$ is definite, def. \ref{DefiniteParameterization}, on $\mathbf{L}|_{\mathbb{D}^V} \in \mathbb{G}\mathbf{Conn}(\mathbb{D}^V)$, def. \ref{DifferentialConcretification}.

Since, according to prop. \ref{DefiniteSectionsAndReductionOfStructureGroup}, the second item in def. \ref{DefiniteGlobalization} implies a [[reduction of the structure group|lift/reduction of the structure group]] to $\mathbf{QuantMorph}(\mathbf{L}|_{\mathbb{D}^V})$, in total this requires a reduction/lift to the [[Heisenberg ∞-group]]

$$
  G =
  \mathbf{Heis}_{\mathbf{Aut}_{grp}(\mathbb{D}^V)}(\mathbf{L}|_{\mathbb{D}^V})
  \coloneqq
  \mathbf{QuantMorp}(\mathbf{L}|_{\mathbb{D}^V})
  \underset{\mathbf{Aut}(\mathbb{D}^V)}{\times}
  \mathbf{Aut}_{Grp}(\mathbb{D}^V)
 \,.
$$

This [[G-structure]] we require to be [[integrable G-structure|first order integrable] (with respect to the canonical left-invariant [[framed manifold|framing]] of $V$.)

=--

+-- {: .num_example}
###### Example

In $\mathbf{H} = $ [[SuperFormalSmooth∞Grpd]] and for $V$ being [[super Minkowski spacetime]] of bosonic [[dimension]] $d = 3,4,10,11$ regarded as the [[supersymmetry]] [[super-translation group]] in that dimension, and for $\mathbf{L} = \mathbf{L}$ the WZW term induced by differential Lie integration ([here](geometry+of+physics+--+WZW+terms#WZWTermFromLieIntegration))
 from the [[super Lie algebra]] [[Lie algebra cohomology|cocycles]] of the [[brane scan]] in these dimensions, then the [[Heisenberg ∞-group]] in def. \ref{DefiniteGlobalization} is a $\mathbf{B}(\mathbb{R}/\Gamma)$-[[∞-group extension]] of the [[Lorentz group]] in these dimensions.

This means that a choice of definite globalization of $\mathbf{L}_{string}$ over a [[supermanifold]] $X$ is in particular a choice of super-[[orthogonal structure]], hence a choice of [[graviton]] and of a [[gravitino]] [[field (physics)|field]]. 

The condition that this [[G-structure]] be first-order integrable with respect to the canonical left-invariant framing of [[super Minkowski spacetime]] then means that the [[supertorsion]] of this orthogonal structure vanishes.

For $d = 1$ this is the [[torsion constraint of supergravity]]. By ([Howe 97](torsion+constraints+in+supergravity#Howe97)) this implies that the above graviton and gravitino field satisfy the [[Einstein equations]] for bosonic backgrounds of [[11-dimensional supergravity]].

This in turn implies in particular that the [[curvature]] of the WZW term $\mathbf{L}$ is the fermionic component of the [[supergravity C-field]] [[field strength]]. This finally means that $\mathbf{L}$ itself is a consistent choice of [[prequantization]] of this hence a genuinely globally defined WZW term for the [[Green-Schwarz sigma model]] for the [[M2-brane]] with [[target space]] $X$.

=--




### BPS Charges


+-- {: .num_defn #BPSChargeGroup}
###### Definition

Given a definite globalization $\mathbf{L} \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$ of a WZW term, def. \ref{DefiniteGlobalization}, hence in particular a [[G-structure]] $\mathbf{g}$ on $X$ for $G =
  \mathbf{Heis}_{\mathbf{Aut}_{grp}(\mathbb{D}^V)}(\mathbf{L}|_{\mathbb{D}^V})$, then the corresponding _BPS charge group_ is the [[Heisenberg n-group]] of $\mathbf{L}^X$ over the [[isometry group]] of this $G$-structure:

$$
  BPS(X,\mathbf{g}, \mathbf{L})
  \coloneqq
  \mathbf{Heis}_{\mathbf{Iso}(X,\mathbf{g})}(\mathbf{L})
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $V$ [[super Minkowski spacetime]], then the [[super L-infinity algebra]] of $BPS(X,\mathbf{g}, \mathbf{L})$ is the [[Poisson bracket Lie n-algebra]] of $\omega = F_{\mathbf{L}}$ regarded as a [[pre-n-plectic form]] on $X$. This is an $L_\infty$-algebra extension of the 

=--


## References

* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], J.M. Izquierdo, [[Paul Townsend]], _Topological Extensions of the Supersymmetry Algebra for Extended Objects_, Phys. Rev. Lett. 63 (1989) 2443 ([spire](http://inspirehep.net/record/26393?ln=en))

* {#Witten86} [[Edward Witten]], _Twistor-like transform in ten dimensions_, Nuclear Physics B266 (1986)

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _Super Lie $n$-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields_, International Journal of Geometric Methods in Modern Physics, Volume 12, Issue 02 (2015) 1550018 (35 pages) ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))

* _[[schreiber:differential cohomology in a cohesive topos]]_