
> this page is one chapter of _[[geometry of physics]]_

> previous chapters: _[[geometry of physics -- manifolds and orbifolds|manifolds and orbifolds]]_, _[[geometry of physics -- WZW terms|WZW terms]]_, _[[geometry of physics -- supergeometry|supergeometry]]_

***


#Contents#
* table of contents
{:toc}

## Motivation and results

Consider $(X,g)$ a [[super-spacetime]] and $\omega$ a degree-$(p+2)$ [[differential form]] on $X$ which is a [[geometry of physics -- WZW terms|WZW]] [[curvature form]]  [[definite form|definite]] on the [[super Lie algebra]] [[Lie algebra cohomology|cocycle]] 

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

1. For the inclusion of charges of $p_2$-branes on which $p_1$-branes may end (for $p_1 = 1$: [[type II strings]] ending on [[D-branes]], for $p_1= 2$ and $p_2 = 5$ [[M2-branes]] ending on [[M5-branes]]) then $X$ is to be locally modeled on an [[extended super Minkowski spacetime]], hence on a [[super formal smooth infinity-groupoid|super orbispace]], hence a curved spacetime now is an object in [[higher Cartan geometry]] and one needs to make sense of [[Noether currents]] there.

   (Arguments in this direction for the [[D-branes]] have been given in ([Hammer 97](BPS+state#Hammer97)) and for the [[M5-brane]] in ([Sorokin-Townsend 97](BPS+state#SorokinTownsend97)).)

1. For inclusion of non-infinitesimal isometries one needs the global structure of the full [[supergroup]] of BPS charges, not just its [[super Lie algebra]].

Here we discuss how to solve these problems in full generality ([Sati-Schreiber 15](#SatiSchreiber15)). Specified to the situation in [[11-dimensional supergravity]] with [[M2-branes]] and [[M5-branes]] we find that the BPS charges traditionally seen in the [[M-theory super Lie algebra]] as living in [[ordinary cohomology]] $H^2(X) \oplus H^5(X)$ of spacetime $X$ receive corrections by $d_4$-differentials of a [[Serre spectral sequence]] given by [[cup product]] with the class of the [[supergravity C-field]]. This is in higher analogy to how [[D-brane charges]] are well known ([Maldacena-Moore-Seiberg 01](D-brane#MaldacenaMooreSeiberg01)) to be in [[ordinary cohomology]] only up to corrections of the $d_3$-differential (and higher) in an [[Atiyah-Hirzebruch spectral sequence]] for [[twisted K-theory]], given by [[cup product]] with the class of the [[B-field]]. This supports the conjecture ([Sati 10](M5-brane+charge#Sati10)) that [[M5-brane charge]] should really be in [[twisted generalized cohomology|twisted]] [[elliptic cohomology]], since this is what is canonically twisted by these degree-4 classes ([Ando-Blumberg-Gepner 10](tmf#ABG10)). (Realizing this fully amounts to refining the term $\mathbf{L}_{M5}^X$ that we construct in [[ordinary differential cohomology]] [below](#M5BraneChargesInAnM2BraneCondensate) to ellitptic differential cohomology. Discussion of that refinement is beyond the scope of this page here.)

We also close a gap in ([AGIT89](#AGIT89)): what is strictly derived there from the [[Noether theorem]] is extension of the [[supersymmetry]] algebra by [[differential forms]], while the argument that it is only the [[de Rham cohomology]] class of these forms that matters relies on physics intuition. We find here that the [[Lie algebra]] of [[conserved currents]] extending the (super-)isometry algebra is naturally not just a ([[super Lie algebra|super-]])[[Lie algebra]] but a ([[super L-infinity algebra|super-]])[[Lie n-algebra|Lie (p+1)-algebra]] including higher order symmetries of Noether symmetries. It is by quotienting these out when restricting the current Lie $n$-algebra to its lowest [[Postnikov tower|Postnikov stage]] that current forms pass to their de Rham equivalence classes.  Accordingly, the fully globalized current groups that we find are really ([[super smooth infinity-groupoid|super-]])[[smooth infinity-group|smooth n-groups]]. For instance the [[M-theory super Lie algebra]] is refines to a super Lie 6-group, where $6 = 5+1$ is the dimension of the [[M5-brane]] [[worldvolume]].

$\,$

We formulate the theory general abstractly in  the context of [[higher differential geometry]] given by an [[(∞,1)-topos]] $\mathbf{H}$ equipped with [[cohesion]] and [[differential cohesion]]. The application to [[supergravity]] takes place in the model $\mathbf{H} =$ [[SuperFormalSmooth∞Grpd]].

### Prerequisites


For ease of reference, we recall here some definitions and propositions form previous chapters of _[[geometry of physics]]_ which we need for the discussion of BPS charge groups below.

#### $\infty$-Representations and associated $\infty$-bundles

> recalled from _[[geometry of physics -- representations and associated bundles]]_

+-- {: .num_defn #FiberBundle}
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


#### Homotopy stabilizer groups

> recalled from _[[geometry of physics -- representations and associated bundles]]_


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

> recalled from _[[geometry of physics -- prequantum geometry]]_, following ([FRS 13a](#FRS13a))

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

For $\mathbb{G} \simeq \mathbf{B}\mathbb{G}'$ then the [[loop space object]] of the moduli stack of $\mathbb{G}$-principal $\infty$-connections on $X$ is the moduli stack of [[flat ∞-connections]] with gauge group $\Omega \mathbb{G}$

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


1. The **[[quantomorphism ∞-group]]** is the [[stabilizer ∞-group]] of $\nabla \in \mathbb{G}\mathbf{Conn}(X)$, def. \ref{DifferentialConcretification}, under the $\mathbf{Aut}(X)$-action of \ref{PrecompositionActionOnGConn};

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
     \rho \colon G \longrightarrow \mathbf{HamSymp}(X,\nabla)
      \;
   $$


1. An **[[∞-moment map]]**  is an $\infty$-group homomorphism 

   $$
     G \longrightarrow \mathbf{QuantMorph}(X,\nabla)
   $$

1. The **[[Heisenberg ∞-group]]** for a given Hamiltonian $G$-action $\rho$ is the [[homotopy pullback]] 

   $$
     \mathbf{Heis}_G(X,\nabla) \coloneqq \rho^\ast \mathbf{QuantMorph}(X,\nabla)
     \,.
   $$

=--

+-- {: .num_example }
###### Example

For $\mathbf{H} = $ [[Smooth∞Grpd]], for $X \in SmoothMfd \hookrightarrow \mathbf{H}$ a [[smooth manifold]] and for $\nabla$ a [[prequantum line bundle]] on $X$, then $\mathbf{QuantMorph}(X,\nabla)$ is Soriau's [[quantomorphism group]] covering the [[Hamiltonian diffeomorphism]] group. In the case that $(X, F_\nabla)$ is a [[symplectic vector space]] $X = V$ regarded as a linear symplectic manifold with Hamiltonian action on itself by translation, then $\mathbf{Heis}_{V}(X,\nabla)$ is the traditional [[Heisenberg group]].

=--


+-- {: .num_remark }
###### Remark

Since $\mathbf{HamSymp}(X,\nabla)\hookrightarrow \mathbf{Aut}(X)$ is by construction a [[1-monomorphism]], given any $G$-action $\rho \colon G \longrightarrow \mathbf{Aut}(X)$ on $X$, not necessarily Hamiltonian, then the homotopy pullback $\rho^\ast \mathbf{QuantMorph}(X,\nabla)$ is the Heisenberg ∞-group of the maximal sub-$\infty$-group of $G$ which does act via Hamiltonian symplectomorphisms. Therefore we will also write $\mathbf{Heis}_G(X,\nabla)$ in this case.


=--

The following is the refinement of the [[Kostant-Souriau extension]] to [[higher differential geometry]]

+-- {: .num_prop #TheQuantomorphismGroupExtension}
###### Proposition

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, there is a [[homotopy fiber sequence]] of the form

1. if $\mathbb{G}$ is [[0-truncated]] then

   $$
     \array{
        \mathbb{G}\mathbf{ConstFunct}(X)
        &\longrightarrow&
        \mathbf{QuantMorph}(X,\nabla)
        \\
        && \downarrow
        \\
        && \mathbf{HamSymp}(X,\nabla)
        &\stackrel{\mathbf{KS}}{\longrightarrow}&
        \mathbf{B} (\mathbb{G}\mathbf{ConstFunct}(X))
    }
   $$


1. if $\mathbb{G} \simeq \mathbf{B}\mathbb{G}'$ then

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
        \mathbf{B} ((\Omega \mathbb{G})\mathbf{FlatConn}(X))
    }
   $$

exhibiting the [[quantomorphism ∞-group]] as an [[∞-group extension]] of the [[Hamiltonian symplectomorphism ∞-group]] by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}$.

=--

([FRS13a](#FRS13a))

+-- {: .num_example }
###### Example

In $\mathbf{H} = $ [[Smooth∞Grpd]], let $\mathbb{G} = \mathbf{B}^p U(1)$ be the [[circle n-group|circle (p+1)-group]] and let $X \in SmoothMfd \hookrightarrow Smooth \infty Grpd$ be [[n-connected topological space|p-connected]], then $(\Omega\mathbf{B}^p U(1))\mathbf{FlatConn}(X)\simeq \mathbf{B}^{p}U(1)$. Hence here prop. \ref{TheQuantomorphismGroupExtension} gives

   $$
     \array{
        \mathbf{B}^{p}U(1)
        &\longrightarrow&
        \mathbf{QuantMorph}(X,\nabla)
        \\
        && \downarrow
        \\
        && \mathbf{HamSymp}(X,\nabla)
        &\stackrel{\mathbf{KS}}{\longrightarrow}&
        \mathbf{B}^{p+1}U(1)
    }
  $$
 
=--


+-- {: .num_cor #KSExtensionForHeis}
###### Corollary

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, and for $\rho \colon G \longrightarrow \mathbf{HamSymp}(X,\nabla)$ a $G$-[[Hamiltonian action]], then there is a [[homotopy fiber sequence]]

1. if $\mathbb{G}$ is [[0-truncated]] then

   $$
     \array{
        \mathbb{G}\mathbf{ConstFunct}(X)
        &\longrightarrow&
        \mathbf{Heis}_G(X,\nabla)
        \\
        && \downarrow
        \\
        && G
        &\stackrel{\mathbf{KS}(\rho)}{\longrightarrow}&
        \mathbf{B} (\mathbb{G}\mathbf{ConstFunct}(X))
    }
   $$


1. if $\mathbb{G} \simeq \mathbf{B}\mathbb{G}'$ then

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
        \mathbf{B} ((\Omega \mathbb{G})\mathbf{FlatConn}(X))
    }
   $$

exhibiting the [[Heisenberg ∞-group]] as an [[∞-group extension]] of the $G$ by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}(\rho)$.


The class of the [[cocycle]] $\mathbf{KS}(\rho)$ is the [[obstruction]] to prequantizing $\rho$ to a [[moment map]] (the _[[classical anomaly]]_ of $\rho$); and the the [[Heisenberg ∞-group]] [[∞-group extension|extension]] of $G$ is the universal cancellation of this anomaly.

=--



### Definite forms
 {#DefiniteForms}

The concept of extending a closed [[differential form]] defined on a [[Cartesian space]] $\mathbb{R}^n$ to a _[[definite form]]_ on an $n$-dimensional manifold is familiar from [[special holonomy]] manifolds. For instance a definite globalization of the [[associative 3-form]] on $\mathbb{R}^7$ to a 7-manifold induces and is induced by a [[G₂-structure]]. But by the discussion at _[[geometry of physics -- prequantum geometry]]_, whenever we see a closed differential form we have to ask whether it is the [[curvature]] of a [[cocycle]] in [[differential cohomology]], hence we have to ask for a higher [[prequantization]]. Here we consider the concept of [[definite forms]] prequantized to such _[[definite globalizations of WZW terms]]_. 


+-- {: .num_prop #FunctionsOnTotalSpacesAreSectionsOfFunctionBundle}
###### Proposition

Given a $V$-[[fiber ∞-bundle]] $E$ over $X$, def. \ref{FiberBundle}, and given any [[coefficient]] $A$, there is a [[natural equivalence]] beween 


* morphisms $E \longrightarrow A$;

* [[sections]] of the canonically [[associated ∞-bundle]] $P \times_{\mathbf{Aut}(V)} [V,A]$ over $X$.

=--

+-- {: .num_defn #DefiniteSection}
###### Definition

Given a $V$-[[nLab:fiber ∞-bundle]] $E$ over $X$, and a [[nLab:global element]] $x\colon \ast \to V$ then a [[nLab:section]] $\sigma$ of $E$ is _definite on $x$ if there exists a [[nLab:1-epimorphism]] $U \to X$ and a diagram

$$
  \array{
    U &\longrightarrow& \ast 
    \\
    \downarrow & \swArrow & \downarrow^{\mathrlap{x}}
    \\
    X & \stackrel{\sigma}{\longrightarrow} & V/\mathbf{Aut}(V)
    \\
    & \searrow & \downarrow
    \\
    && \mathbf{B}\mathbf{Aut}(V)
  }
  \,.
$$

=--

+-- {: .num_prop #DefiniteSectionsAndReductionOfStructureGroup}
###### Proposition

Choices of sections definite on $x$ are equivalent to [[reduction of structure groups|reductions of the structure group]], def. \ref{ReductionLiftOfStructureGroup}, along the [[stabilizer group]] map $Stab_\mathbf{Aut(V)}(x)\longrightarrow \mathbf{Aut}(V)$.


=--

+-- {: .num_defn #DefiniteParameterization}
###### Definition

Given $\mathbf{c} \colon V \longrightarrow A$, and given a $V$-[[fiber ∞-bundle]] $E$ over $X$, then a _definite parameterization of $\mathbf{c}$ over $E$_ is a $\mathbf{c}^E \colon E \longrightarrow A$ such that the section $\sigma_{\mathbf{c}^X}$ coresponding to it via prop. \ref{FunctionsOnTotalSpacesAreSectionsOfFunctionBundle} is definite on $\mathbf{c}$ in the sense of def. \ref{DefiniteSection}.

=--

+-- {: .num_defn #DefiniteGlobalization}
###### Definition

For $V$ an [[∞-group]], $\mathbf{L}\colon V \longrightarrow \mathbf{B}\mathbb{G}_{conn}$ a [[geometry of physics -- WZW terms|WZW term]], and for $X$ a [[geometry of physics -- manifolds and orbifolds|V-manifold]], then a _[[definite globalization of WZW terms|definite globalization]]_ of $\mathbf{L}$ over $X$ is 

1. A [[reduction of the structure group]], def. \ref{ReductionLiftOfStructureGroup}, of the [[frame bundle]] of $X$ along 

  $$
    \mathbf{Aut}_{Grp}(\mathbb{D}^V) = \mathbf{Aut}^{\ast/}(\mathbf{B}\mathbb{D}^V) \longrightarrow \mathbf{Aut}(\mathbb{D}^V) = GL(V)
    \,,
  $$

  for $\mathbb{D}^V$ [[generalized the|the]] [[infinitesimal disk]] in $V$;

1. an $\mathbf{L}^X \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$ such that its pullback $T_{inf} X \to X \stackrel{\mathbf{L}^X}{\longrightarrow} \mathbf{B} \mathbb{G}_{conn}$ to the [[infinitesimal disk bundle]] of $X$ is definite, def. \ref{DefiniteParameterization}, on $\mathbf{L}|_{\mathbb{D}^V} \in \mathbb{G}\mathbf{Conn}(\mathbb{D}^V)$, def. \ref{DifferentialConcretification}.

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

This [[G-structure]] we require to be [[integrable G-structure|first order integrable]] (with respect to the canonical left-invariant [[framed manifold|framing]] of $V$.)

=--

+-- {: .num_example}
###### Example

Let $\mathbf{H} = $ [[Smooth∞Grpd]]. 

1. For $\mathbf{L}\colon T^\ast \mathbb{R}^n \to \mathbf{B}U(1)_{conn}$ the [[Liouville-Poincaré 1-form]] $\theta = \sum_{i = 1}^n p_i d q^i$ (regarded as a [[principal connection]] on the trivial [[circle bundle]]), then a definite globalization of $\mathbf{L}$ is a [[symplectic manifold]] equipped with a [[prequantum line bundle]].


1. for $\mathbf{L}\colon \mathbb{R}^7 \longrightarrow \mathbf{B}^3 U(1)_{conn}$ a potential for the [[associative 3-form]], then a definite globalization is a manifold with [[G₂-structure]] $(X,\omega_3)$ equipped with a [[bundle gerbe with connection]] whose 3-form curvature is $\omega_3$.

=--

+-- {: .num_example #11dSugreEquationsOfMotionFromDefiniteGlobalization}
###### Example

In $\mathbf{H} = $ [[SuperFormalSmooth∞Grpd]] and for $V$ being [[super Minkowski spacetime]] of bosonic [[dimension]] $d = 3,4,10,11$ regarded as the [[supersymmetry]] [[super-translation group]] in that dimension, and for $\mathbf{L} = \mathbf{L}$ the WZW term induced by differential Lie integration ([here](geometry+of+physics+--+WZW+terms#WZWTermFromLieIntegration))
 from the [[super Lie algebra]] [[Lie algebra cohomology|cocycles]] of the [[brane scan]] in these dimensions, then the [[Heisenberg ∞-group]] in def. \ref{DefiniteGlobalization} is a $\mathbf{B}(\mathbb{R}/\Gamma)$-[[∞-group extension]] of the [[Lorentz group]] in these dimensions.

This means that a choice of definite globalization of $\mathbf{L}_{string}$ over a [[supermanifold]] $X$ is in particular a choice of super-[[orthogonal structure]], hence a choice of [[graviton]] and of a [[gravitino]] [[field (physics)|field]]. 

The condition that this [[G-structure]] be first-order integrable with respect to the canonical left-invariant framing of [[super Minkowski spacetime]] then means that the [[supertorsion]] of this orthogonal structure vanishes.

For $d = 1$ this is the [[torsion constraint of supergravity]]. By ([Candiello-Lechner 93](torsion+constraints+in+supergravity#CandielloLechner93), [Howe 97](torsion+constraints+in+supergravity#Howe97)) this implies that the above graviton and gravitino field satisfy the [[Einstein equations]] for bosonic backgrounds of [[11-dimensional supergravity]].

This in turn implies in particular that the [[curvature]] of the WZW term $\mathbf{L}$ is the fermionic component of the [[supergravity C-field]] [[field strength]]. This finally means that $\mathbf{L}$ itself is a consistent choice of [[prequantization]] of this hence a genuinely globally defined WZW term for the [[Green-Schwarz sigma model]] for the [[M2-brane]] with [[target space]] $X$.

=--




### BPS Charges

Once a $V$-manifold $X$ is equipped with a definite globalization $\mathbf{L}^X$ of a WZW term $\mathbf{L}$, according to \ref{DefiniteGlobalization}, and hence also with a [[G-structure]] $\mathbf{g}$ for $G$ the suitable [[homotopy stabilizer group]] of $\mathbf{L}$ on [[infinitesimal disks]], then the [[automorphism ∞-group]] $\mathbf{Aut}(X)$ is naturally "[[spontaneously broken symmetry|broken]]" to the [[homotopy stabilizer group]] of this extra data. The stabilizer of the $G$-structure itself yields the [[isometry group]] $\mathbf{Iso}(X,\mathbf{g})$, but since the higher WZW term has in general [[higher gauge symmetries]], the total homotopy stabilizer of the triple $(X,\mathbf{g},\mathbf{L}^{X})$ is a [[Heisenberg ∞-group|Heisenberg]] [[∞-group extension]] of that. Since for the case of applications to [[supergravity]] (examples \ref{11dSugreEquationsOfMotionFromDefiniteGlobalization}, \ref{M5ChargeExtensions} below) the [[0-truncated|0-truncation]] of this [[∞-group extension]] turns out to be the extension by [[BPS charges]], we here speak, for lack of any other established term, generally of _BPS charge groups_ for homotopy stabilizers of definitely globalized higher WZW terms. 

#### For a single $p$-brane species

+-- {: .num_defn #BPSChargeGroup}
###### Definition

Given a definite globalization $\mathbf{L}^X \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$ of a WZW term, def. \ref{DefiniteGlobalization}, hence in particular a [[G-structure]] $\mathbf{g}$ on $X$ for $G =
  \mathbf{Heis}_{\mathbf{Aut}_{grp}(\mathbb{D}^V)}(\mathbf{L}|_{\mathbb{D}^V})$, then the corresponding _BPS charge group_ is the [[Heisenberg n-group]], def. \ref{QuantomorphismGroup}, of $\mathbf{L}^X$ over the [[isometry group]] of this $G$-structure:

$$
  BPS(X,\mathbf{g}, \mathbf{L})
  \coloneqq
  \mathbf{Heis}_{\mathbf{Iso}(X,\mathbf{g})}(X,\mathbf{L}^X)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

For $V$ [[super Minkowski spacetime]], then the [[super L-∞ algebra]] of $BPS(X,\mathbf{g}, \mathbf{L})$, def. \ref{BPSChargeGroup} is the [[Poisson bracket L-∞ algebra]] $\mathfrak{Pois}(X,\omega)$ of $\omega = F_{\mathbf{L}}$ regarded as a [[pre-n-plectic form|pre-(p+1)-plectic form]] on $X$. See the discussion in ([FRS 13b, section 4](#FRS13b)).

=--

Accordingly we find $L_\infty$-algebraic versions of the higher Kostant-Heisenberg $\infty$-extensions of prop. \ref{LieKSExtension}:

+-- {: .num_prop #LieKSExtension}
###### Proposition


There is a [[homotopy fiber sequence]] in the [[homotopy theory of L-∞ algebras]] of the form

$$

  \array{
    \mathbf{H}(X,\flat \mathbf{B}^p \mathbb{R})
    &\longrightarrow&
    \mathfrak{Pois}_{Iso(X,g)}(X,\omega)
    \\
    && \downarrow
    \\
    && HamIso(X,g,\omega)
    &\stackrel{ks}{\longrightarrow}&
    \mathbf{B}\mathbf{H}(X,\flat \mathbf{B}^p \mathbb{R})
  }
$$

which exhibits the [[Poisson bracket L-∞ algebra]] as an  [[L-∞ algebra extension]] of the Lie algebra of $\omega$-Hamiltonian [[Killing vectors]] and [[Killing spinors]] by the truncated [[de Rham complex]] 

$$
  \mathbf{H}(X,\flat \mathbf{B}^p \mathbb{R})
  \simeq
  (\Omega^0(X)\stackrel{d}{\to} \Omega^1(X)\stackrel{d}{\to} \cdots \stackrel{d}{\to} \Omega^p_{cl}(X))
$$


in degree $p$, regarded as an abelian $L_\infty$-algebra.

=--

([FRS 13b, theorem 3.3.1](#FRS13b))

+-- {: .num_remark}
###### Remark

By ([FRS 13b, theorem 4.2.2](#FRS13b)) $\mathfrak{Pois}(X,\omega)$
has a model by the [[dg-Lie algebra]]
([FRS 13b, def./prop. 4.2.1](#FRS13b)). Its bracket in degree-0
([FRS 13b, equation (4.2.1)](#FRS13b)) is the bracket
of [[Noether currents]] for $\omega$ regarded as a WZW curvature as
considered in ([AGIT 89](#AGIT89)).

=--

But $\mathfrak{Pois}(X,\omega)$ encodes also the 
higher order currents between these currents, which get quotiented out
when passing to its degree-0 [[Postnikov stage]]:


+-- {: .num_prop #0TruncationOfHigherPoissonBracket}
###### Proposition

For connective [[L-∞ algebras]], 0-truncation yields a [[functor]]

$$
  \tau_0
  \colon
  L_\infty Alg_{\geq 0}
  \longrightarrow
  LieAlg
$$

to [[Lie algebras]]. Under this functor this higher Kostant-Soriau extension
of prop. \ref{LieKSExtension} becomes a [[Lie algebra extension]]

$$
  0 \to H^p_{dR}(X) \longrightarrow \tau_0 \mathfrak{Pois}(X,\omega)
  \longrightarrow 
  Ham(X,\omega)
  \to
  0
$$

of the [[Hamiltonian vector fields]] by the degree-$p$ [[de Rham cohomology]] group
of $X$, regarded as an abelian Lie algebra.

=--


#### For $p_1$-branes ending on $p_2$-branes

Consider now two
[consecutive WZW terms](http://ncatlab.org/nlab/show/geometry+of+physics+--+WZW+terms#ConsecutiveWZWTermsAndTwists)

$$
  \array{
    \widetilde{\hat V} &\stackrel{\mathbf{L}_2}{\longrightarrow}&
    \mathbf{B}(\mathbb{G}_2)_{conn}
    \\
    \downarrow
    \\
    V &\stackrel{\mathbf{L}_1}{\longrightarrow}&
    \mathbf{B}(\mathbb{G}_1)_{conn}
  }
$$

with $\mathbf{L}_2$ defined on the differential refinement of the [[∞-group]] extension 

$$
  \array{
    \mathbb{G} &\longrightarrow& \hat V
    \\
    && \downarrow
    \\
    && V &\stackrel{}{\longrightarrow}& \mathbf{B}\mathbb{G}
  }
$$


which is the underlying $\mathbb{G}$-[[principal ∞-bundle]] underlying $\mathbf{L}_1$.

$$
  \array{
    \widetilde{\hat V} &\stackrel{}{\longrightarrow}&
    \Omega^1(-,\mathbb{G})
    \\
    \downarrow &(pb)& \downarrow
    \\
    V &\stackrel{\mathbf{L}_1}{\longrightarrow}&
    \mathbf{B}(\mathbb{G}_1)_{conn}
  }
$$


+-- {: .num_prop #ExtendedSpacetimeIsConsistent}
###### Proposition

Given two [consecutive WZW terms](http://ncatlab.org/nlab/show/geometry+of+physics+--+WZW+terms#ConsecutiveWZWTermsAndTwists), $(\mathbf{L}_1,\mathbf{L}_2)$
and given a define globalization, 
def. \ref{DefiniteGlobalization}, of $\mathbf{L}_1$ over a $V$-manifold $X$ 
then 

1. the isometry action canonically lifts from $X$ to to the extended spacetime $\widetilde{\hat X}$

  $$
    \array{
       \widetilde {\hat X} &\longrightarrow& \Omega^1(-\mathbb{G})
       \\
       \downarrow &(pb)& \downarrow 
       \\
       X &\stackrel{\mathbf{L}_1}{\longrightarrow}& 
       \mathbf{B}\mathbb{G}_{conn}
     }
     \,;
   $$

1. the [[infinitesimal disks]] in $\widetilde {\hat X}$ are equivalent to those of $\widetilde {\hat V}$.

=--

+-- {: .num_defn #BPSGroupForConsecutiveWZWTerms}
###### Definition


By this proposition it is consistent to ask for a _consecutive_ definitite globalization of two consecutive WZW term

$$
  \array{
    \widetilde{\hat X} &\stackrel{\mathbf{L}_2^X}{\longrightarrow}&
    \mathbf{B}(\mathbb{G}_2)_{conn}
    \\
    \downarrow
    \\
    X &\stackrel{\mathbf{L}_1^X}{\longrightarrow}&
    \mathbf{B}(\mathbb{G}_1)_{conn}
  }
  \,.
$$

The _BPS charge $\infty$-group_ of this setup is

$$
  \mathbf{BPS}(X,\mathbf{g}, \mathbf{L}_1^X, \mathbf{L}_2^X)
  \coloneqq
  \mathbf{Heis}_{\mathbf{Iso}(X,\mathbf{g})}(\widetilde {\hat X},\mathbf{L}_2^X)
  \,.
$$

=--

By cor. \ref{KSExtensionForHeis} this is an [[∞-group extension]] of $\mathbf{Iso}(X,\mathbf{g})$ by
$\mathbb{G}_2\mathbf{FlatConn}(\widetilde{\hat X})$.
Forgetting the differential part of the twist, this extension group receives a map from  $\mathbb{G}_2\mathbf{FlatConn}({\hat X})$.


### Example: M5-brane charges in an M2-brane condensate
 {#M5BraneChargesInAnM2BraneCondensate}

+-- {: .num_example #M5ChargeExtensions}
###### Example

Consider again $\mathbf{H}= $ [[SuperFormalSmooth∞Grpd]] as in example \ref{11dSugreEquationsOfMotionFromDefiniteGlobalization}.

From the [[odd line|super point]] $\mathbb{R}^{0|1} \in \mathbf{H}$ there emanates a [[schreiber:The brane bouquet|bouquet]] of consecutive [[super L-∞ algebra]] [[L-∞ algebra extensions|extensions]], part of which looks as follows ([FSS 13](#FSS13)):

<div style="float:left;margin:0 10px 10px 0;"><img src="https://dl.dropboxusercontent.com/u/12630719/BraneBouquet.JPG" alt="the brane bouquet" /></div>

We now concentrate on the branch of this classified by the cocycles $\mu_4$ for the [[M2-brane]], and $\mu_7$ for the [[M5-brane]]:

$$
  \array{
    \mathfrak{m}5\mathfrak{brane}
    \\
    \downarrow
    \\
    \mathfrak{m}2\mathfrak{brane}
    &\stackrel{\mu_7\coloneqq\overline{\psi}\Gamma^{a_1 \cdots a_5}\wedge \psi \wedge e_{a_1}\wedge \cdots \wedge e_{a_5} + c_3\wedge \mu_4}{\longrightarrow}&
    b^6 \mathbb{R}
    \\
    \downarrow
    \\
    \mathbb{R}^{10,1\vert \mathbf{32}}
    &\stackrel{\mu_4 \coloneqq \overline{\psi}\Gamma^{a_1 a_2}\wedge \psi \wedge e_{a_1}\wedge e_{a_2}}{\longrightarrow}&
    b^2 \mathbb{R}
  }
$$

Here $\mathfrak{m}2\mathfrak{brane}$ denotes the "[[supergravity Lie 3-algebra]]" regarded as an [[extended super Minkowski spacetime]] and $\mathfrak{m}5\mathfrak{brane}$ denotes the "[[supergravity Lie 6-algebra]]". Both hooks $\array{\downarrow \\ & \rightarrow}$ in the diagram are [[homotopy fiber sequences]] in the [[homotopy theory of L-∞ algebras|homotopy theory of super L-∞ algebras]].

By the discussion at _[geometry of physics -- WZW terms -- Consecutive WZW terms](geometry+of+physics+--+WZW+terms#ConsecutiveWZWTermsAndTwists)_, following ([FSS 13](#FSS13)) applying differentially refined [[Lie integration]] to this yields two consecutive higher WZW terms of the form

$$
  \array{
     \mathbf{B}^{2}(\mathbb{R}/\Gamma_1)_{conn} &\longrightarrow& \widetilde {\hat{\mathbb{R}}}^{10,1\vert \mathbf{32}}
     &\stackrel{\mathbf{L}_{M5}}{\longrightarrow}&
     \mathbf{B}^{5} (\mathbb{R}/\Gamma_2)_{conn}
     \\
     && \downarrow
     \\
     && \mathbb{R}^{10,1\vert \mathbf{32}}
     &\stackrel{\mathbf{L}_{M2}}{\longrightarrow}&
     \mathbf{B}^2 (\mathbb{R}/\Gamma_1)_{conn}
  }
  \,.
$$

(Here by the [[van Est isomorphism]] we do not notationally distinguish [[super Minkowski spacetime]] regarded as a [[super Lie algebra]] or a [[super Lie group]].)


By example \ref{11dSugreEquationsOfMotionFromDefiniteGlobalization} 
a choice of definite globalization of $\mathbf{L}_{M2}$ is equivalent to bosonic solution $(X,\mathbf{g})$ to the [[Einstein equations]] of [[11-dimensional supergravity]] equipped with a compatible globally defined WZW term $\mathbf{L}_{M2}^X$ for the [[M2-brane]] [[Green-Schwarz sigma model]] with [[target space]] $X$.

By prop. \ref{ExtendedSpacetimeIsConsistent} this defines an 
extended superspacetime $\widetilde{\hat X}$ which is a [[higher Cartan geometry]] of locally modeled on the [[supergravity Lie 3-algebra]] on which the local [[M5-brane]] [[Green-Schwarz sigma model]] is defined, and hence may ask for a choice of definite globalization of that 


$$
  \array{
     \widetilde {\hat{X}}
     &\stackrel{\mathbf{L}^X_{M5}}{\longrightarrow}&
     \mathbf{B}^{5} (\mathbb{R}/\Gamma_2)_{conn}
     \\
     \downarrow
     \\
     X
     &\stackrel{\mathbf{L}^X_{M2}}{\longrightarrow}&
     \mathbf{B}^2 (\mathbb{R}/\Gamma_1)_{conn}
  }
  \,.
$$

This is now a globally well defined background for the M5-brane sigma model
and def. \ref{BPSGroupForConsecutiveWZWTerms} determines its BPS-char super-6-group.
By corollary \ref{KSExtensionForHeis} this is a super 6-group extension
of the [[superisometry group]] of $(X,\mathbf{g})$ by 
$(\mathbf{B}^5 (\mathbb{R}/\Gamma_2))\mathbf{FlatConn}(\widetilde{\hat X})$.


By the discussion at _[geometry of physics -- WZW terms -- Consecutive WZW terms](geometry+of+physics+--+WZW+terms#ConsecutiveWZWTermsAndTwists)_ the extended spacetime $\widetilde {\hat X}$ here is such that smooth maps into it

$$
  \Sigma \longrightarrow \widetilde{\hat X}
$$

(which are the [[field (physics)|fields]] of the [[M5-brane]] [[sigma model]] with WZW term $\mathbf{L}^X_{M5}$) are equivalently pairs, consisting of

1. a smooth function $\phi \colon \Sigma \longrightarrow X$ into the actual spacetime $X$;

1. a [[cocycle]] $\nabla$ in $\phi$-twisted degree-3 [[Deligne cohomology]] on $\Sigma$, hence a [[B-field|2-form gauge field]] on $\Sigma$, subject to certain compatibility conditions with the function $\phi$.

The first item here is the evident [[sigma model]] field, the second 2-form field is part of the "tensor multiplet" on the [[M5-brane]], exhibiting the Green-Schwarz sigma-model for the M5-brane as a _higher_ [[gauged WZW model]].

Now to consider the BPS charge group of $\mathbf{L}^X_{M5}$, def. \ref{BPSGroupForConsecutiveWZWTerms}. By corollary \ref{KSExtensionForHeis} this is an [[∞-group extension]] of the [[super-isometry group]] of the 11-dimensional [[super spacetime]] by the moduli stack $(\mathbf{B}^5 U(1))\mathbf{FlatConn}(\widetilde{\hat X})$ of flat 5-form connection on the extended spacetime.

This receives a map $(\mathbf{B}^5 U(1))\mathbf{FlatConn}(\hat X) \longrightarrow (\mathbf{B}^5 U(1))\mathbf{FlatConn}(\widetilde{\hat X})$ from the moduli of 5-form connections of the extended spacetime $\hat X$ (which is $\widetilde{\hat X}$. This consists of the cohomological data without the _differential_ cohomologica data in $\mathbf{L}_{M2}^X$): it is the $\mathbf{B}^2 (\mathbb{R}/\Gamma_1)$-[[principal ∞-bundle]] which sits in the [[homotopy fiber sequence]] of the form

$$
  \array{
    \mathbf{B}^2 (\mathbb{R}/\Gamma_1)
    &\longrightarrow&
    \hat X
    \\
    && \downarrow
    \\
    && X &\stackrel{\mathbf{DD}(\mathbf{L}_{M2}^X)}{\longrightarrow}&
    \mathbf{B}^3 (\mathbb{R}/\Gamma_1)
  }
  \,.
$$



Under [[Lie differentiation]] as in prop. \ref{0TruncationOfHigherPoissonBracket} $(\mathbf{B}^5 U(1))\mathbf{FlatConn}(\widetilde{\hat X})$ turns into
$(\mathbf{B}^5 \mathbb{R})\mathbf{FlatConn}(\widetilde{\hat X})$ hence into $\mathbf{H}(\hat X, \flat \mathbf{B}^5 \mathbb{R})$. Under the [[adjunction]] between [[shape modality]] $\int$ and [[flat modality]] $\flat$, this is the degree-5 real cohomology of the [[geometric realization]] of $\hat X$. This in turns is a [[Eilenberg-MacLane space|K(Z,3)]]-fibration $\int \hat X \to \int X$ over the underlying bare [[homotopy type]] of spacetime $X$ which is classified by the integral degree-4 class which is the higher [[Dixmier-Douady class]] $DD(\mathbf{L}_{M5}^X) $ of $\mathbf{L}_{M2}^{X}$.

The degree-5 real cohomology of such a fibration is computed by a
[[Serre spectral sequence]]. By the discussion at _[Eilenberg-MacLane space -- cohomology of EM spaces](Eilenberg-Mac+Lane+space#CohomologyOfEMSpaces)_ only very few entries in this spectral sequence contribute, and the result is the middle cohomology of this sequence

$$
  H^1(X) \stackrel{(0,d_4)}{\longrightarrow} H^2(X) \oplus H^5(X)
  \stackrel{(d_4,0)}{\longrightarrow}
  H^6(X)
$$

where $d_4 \propto (-)\cup DD(\mathbf{L}_{M2}^X)$ is given by taking the [[cup product]] with the class of the M2-WZW term.

This is the group of M2-brane and M5-brane charges with corrections by global effects, in the corrected [[M-theory super Lie algebra]] for the superspacetime $(X,g)$.

=--

## References

* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], J.M. Izquierdo, [[Paul Townsend]], _Topological Extensions of the Supersymmetry Algebra for Extended Objects_, Phys. Rev. Lett. 63 (1989) 2443 ([spire](http://inspirehep.net/record/26393?ln=en))

* {#Witten86} [[Edward Witten]], _Twistor-like transform in ten dimensions_, Nuclear Physics B266 (1986) ([spire](http://inspirehep.net/record/214192?ln=en))

* {#FRS13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_ ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))

* {#FRS13b} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_, Homology, Homotopy and Applications, Volume 16 (2014) Number 2, p. 107 &#8211; 142  ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_, International Journal of Geometric Methods in Modern Physics, Volume 12, Issue 02 (2015) 1550018 ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))

* {#SatiSchreiber15} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Lie n-algebras of BPS charges]]_ ([arXiv:1507.08692](http://arxiv.org/abs/1507.08692))

All details and proofs for the above are in

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([pdf](https://dl.dropboxusercontent.com/u/12630719/dcct.pdf))