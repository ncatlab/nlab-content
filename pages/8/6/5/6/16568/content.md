

> this page is one chapter in _[[geometry of physics]]_

> previous chapter: _[[geometry of physics -- principal connections|principal connections]]_;

> next chapter: _[[geometry of physics -- BPS charges|BPS charges]]_

***

#Contents#
* table of contents
{:toc}

## **Prequantum geometry**

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

For $\mathbf{H} = $ [[Smooth∞Grpd]], for $X \in SmoothMfd \hookrightarrow \mathbf{H}$ a [[smooth manifold]] and for $\nabla$ a [[prequantum line bundle]] on $X$, then $\mathbf{QuantMorph}(X,\nabla)$ is Soriau's [[quantomorphism group]] covering the [[Hamiltonian diffeomorphism]] group. In the case that $(X, F_\nabla)$ is a [[symplectic vector space]] regarded as a linear symplectic manifold with Hamiltonian action on itself by translation, then $\mathbf{Heis}_{V}(X,\nabla)$ is the traditional [[Heisenberg group]].

=--


+-- {: .num_remark }
###### Remark

Since $\mathbf{HamSymp}(X,\nabla)\hookrightarrow \mathbf{Aut}(X)$ is by construction a [[1-monomorphism]], then given any $G$-action $\rho \colon G \longrightarrow \mathbf{Aut}(X)$ on $X$, not necessarily Hamiltonian, then the homotopy pullback $\rho^\ast \mathbf{QuantMorph}(X,\nabla)$ is the Heisenberg ∞-group of the maximal sub-$\infty$-group of $G$ which does act via Hamiltonian symplectomorphisms. Therefore we will also write $\mathbf{Heis}_G(X,\nabla)$ in this case.


=--

The following is the refinement of the [[Kostant-Souriau extension]] to [[higher differential geometry]]

+-- {: .num_prop #TheQuantomorphismGroupExtension}
###### Proposition

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, the there is a [[homotopy fiber sequence]] of the form

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
        \mathbf{B} ((\Omega \mathbb{G})\mathbf{Conn}(X))
    }
   $$

exhibiting the [[quantomorphism ∞-group]] as an [[∞-group extension]] of the [[Hamiltonian symplectomorphism ∞-group]] by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}$.

=--

+-- {: .num_example }
###### Example

In $\mathbf{H} = $ [[Smooth∞Grpd]], let $\mathbb{G} = \mathbf{B}^p U(1)$ be the [[circle n-group|circle (p+2)-group]] and let $X \in SmoothMfd \hookrightarrow Smooth \infty Grpd$ be [[n-connected topological space|(p+1)-connected]], then $(\mathbf{B}^p U(1))\mathbf{FlatConn}(X)\simeq \mathbf{B}^{p+1}U(1)$. Hence here prop. \ref{TheQuantomorphismGroupExtension} gives

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

Given a $\mathbb{G}$-[[principal ∞-connection]] $\nabla \colon X \longrightarrow \mathbf{B}\mathbb{G}_{conn}$, and for $\rho \colon G \longrightarrow$ a $G$-[[Hamiltonian action]], then there is a [[homotopy fiber sequence]]

1. if $\mathbb{G}$ is [[0-truncated]] then

   $$
     \array{
        \mathbb{G}\mathbf{ConstFunct}(X)
        &\longrightarrow&
        \mathbf{Heis}_G(X,\nabla)
        \\
        && \downarrow
        \\
        && \mathbf{HamSymp}(X,\nabla)
        &\stackrel{\mathbf{KS}(\rhp)}{\longrightarrow}&
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
        && \mathbf{HamSymp}(X,\nabla)
        &\stackrel{\mathbf{KS}(\rho)}{\longrightarrow}&
        \mathbf{B} ((\Omega \mathbb{G})\mathbf{Conn}(X))
    }
   $$

exhibiting the [[Heisenberg ∞-group]] as an [[∞-group extension]] of the [[Hamiltonian symplectomorphism ∞-group]] by the [[moduli stack]] of $\Omega \mathbb{G}-$[[flat ∞-connections]], classified by a [[cocycle]] $\mathbf{KS}(\rho)$.


The class of the [[cocycle]] $\mathbf{KS}(\rho)$ is the [[obstruction]] to prequantizing $\rho$ to a [[moment map]] (the _[[classical anomaly]]_ of $\rho$); and the the [[Heisenberg ∞-group]] [[∞-group extension|extension]] of $G$ is the universal cancellation of this anomaly.

=--


## References

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_

