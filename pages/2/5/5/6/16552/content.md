
> this entry is one chapter of _[[geometry of physics]]_

> previous chapters: _[[geometry of physics -- groups|groups]]_, _[[geometry of physics -- principal connections|principal connections]]_

> next chapter: _[[geometry of physics -- BPS charges|BPS charges]]_

***

#Contents#
* table of contents
{:toc}

## **WZW terms**

We had seen that in [[higher differential geometry]], then given any closed [[differential n-form|differential (p+2)-form]] $\omega \in \Omega^{p+2}_{cl}(X)$, it is natural to ask for a [[prequantization]] of it, namely for a [[circle n-bundle with connection|circle (p+1)-bundle with connection]] $\nabla$ (equivalently: [[cocycle]] in degree-$(p+2)$-[[Deligne cohomology]]) on $X$ whose [[curvature]] is $F_\nabla = \omega$. In terms of [[moduli stacks]] this means asking for lifts of the form

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

One such class arises in [[infinity-Lie theory]], where $\omega$ is a [[left invariant form]] on a [[smooth infinity-group]] given by a [[cocycle]] in [[L-∞ algebra cohomology]]. The [[prequantum n-bundles]] arising this way are the higher [[WZW terms]] discussed here.

In low degree of traditional [[Lie theory]] this appears as follows: On [[Lie groups]] $G$, those closed $(p+2)$-forms $\omega$ which are [[left invariant forms]] may be identified, via the general theory of [[Chevalley-Eilenberg algebras]], with degree $(p+2)$-[[cocycles]] $\mu$ in the [[Lie algebra cohomology]] of the [[Lie algebra]] $\mathfrak{g}$ corresponding to $G$. We have  $\omega = \mu(\theta)$where $\theta$ is the [[Maurer-Cartan form]] on $G$. These cocycles $\mu $ in turn may arise, via the [[van Est map]], as the [[Lie differentiation]] of a degree-$(p+2)$-[[cocycle]] $\mathbf{c} \colon \mathbf{B}G \to \mathbf{B}^{p+2}U(1)$ in the [[Lie group cohomology]] of $G$ itself, with [[coefficients]] in the [[circle group]] $U(1)$. 

This happens to be the case notably for $G$ a [[simply connected topological space|simply connected]] [[compact Lie group|compact]] [[semisimple Lie group]] such as [[special unitary group|SU]] or [[spin group|Spin]], where $\mu = \langle -,[-,-]\rangle$, hence $\omega = \langle \theta , [\theta,\theta]\rangle$, is the [[Lie algebra cohomology|Lie algebra 3-cocycle]] in [[transgression]] with the [[Killing form]] [[invariant polynomial]] $\langle -,-\rangle$. This is, up to normalization, a representative of the de Rham image of a generator $\mathbf{c}$ of $H^3(\mathbf{B}G, U(1)) \simeq H^4(B G, \mathbb{Z}) \simeq \mathbb{Z}$. 

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

whose higher [[Dixmier-Douady class]] class $ \int \Omega \mathbf{c} \in H^{p+2}(X,\mathbb{Z})$ is an [[integral cohomology]] lift of the [[real cohomology]] class encoded by $\omega$ under the [[de Rham isomorphism]]. In the example of [[spin group|Spin]] and $p = 1$ this extension is the [[string 2-group]].

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

Later, such WZW terms, or at least their curvature forms $\omega$, were recognized all over the place in [[quantum field theory]]. For instance the [[Green-Schwarz sigma-models for super p-branes]] each have an [[action functional]] that is the sum of the standard [[kinetic action]] plus a WZW term of degree $p+2$. 

In general WZW terms are "[[gauged WZW model|gauged]]" which means, as we will see, that they are not defined on the given [[smooth infinity-group]] $G$ itself, but on a bundle $\tilde G$ of [[differential cohomology|differential]] [[moduli stacks]] over that group, such that a map $\Sigma \to \tilde G$ is a pair consisting of a map $\Sigma \to G$ and of a [[higher gauge field]] on $\Sigma$ (a "tensor multiplet" of fields).

Here we discuss the general construction and theory of such higher WZW terms.

### Model layer

We discuss how every [[cocycle]] $\mu \colon \mathfrak{g} \to b^{p+1} \mathbb{R}$ in [[L-∞ algebra cohomology]] has a [[Lie integration]] to a higher WZW term of the form

$$
  \mathbf{L}_\mu \colon \tilde G \longrightarrow \mathbf{B}^{p+1}(\mathbb{R}/\Gamma)_{conn}
$$

where $\tilde G$ is a differential extension of the smooth $p+1$-group that is the universal [[Lie integration]] of $\mathfrak{g}$, and where $\Gamma \hookrightarrow \mathbb{R}$ is the group of [[periods]] of $\mu$ on that group.

This construction is a differential refinement of [[Lie integration]], so we start with recalling the relevant constructions and facts of Lie integration.

#### Lie integration

So let $\mathfrak{g}$ be an [[L-∞ algebra]] of [[finite type]].

Write 

* $CE(\mathfrak{g})$ for the [[Chevalley-Eilenberg algebra]] of an [[L-∞ algebra]] $\mathfrak{g}$;

* $\Delta^\bullet_{smth} \colon \Delta \to SmoothMfd$ for the [[cosimplicial object|cosimplicial]] [[smooth manifold]] [[manifold with corners|with corners]] which is in degree $k$ the standard $k$-simpliex $\Delta^k \hookrightarrow \mathbb{R}^{k+1}$;

* $\Omega^\bullet_{si}(\Delta_{smth}^k)$ for the [[de Rham complex]] of those [[differential forms]] on $\Delta_{smth}^k$ which have [[sitting instants]], in that in an [[open neighbourhood]] of the [[boundary]] they are constant perpendicular to any face on their value at that face;

* $\Omega^\bullet_{si}(U \times \Delta_{smth}^k)$ for $U \in SmoothMfd$ for the [[de Rham complex]] of differential forms on $U \times \Delta^k$ which when restricted to each point of $U$ have sitting instants on $\Delta^k$;

* $\Omega^\bullet_{vert,si}(U \times \Delta_{smth}^k)$ for the subcomplex of forms that in addition are [[vertical differential forms]] with respect to the projection $U \times \Delta^k \to U$.



+-- {: .num_defn #SimplicialLieIntegrationOfLinfinityAlgebra}
###### Definition

For $\mathfrak{g}$ an [[L-∞ algebra]], write

* $\exp(\mathfrak{g})_\bullet \in PreSmoothTypes = PSh(CartSp,sSet)$

  for the [[simplicial presheaf]]

  $$
    \exp(\mathfrak{g}) 
    \colon 
    (U \times k) \mapsto Hom_{dgAlg}( CE(\mathfrak{g}), \Omega^\bullet_{vert,si}(U \times \Delta_{smth}^k) )
    \,.
  $$

  which is the universal _[[Lie integration]]_ of $\mathfrak{g}$;

* $\flat_{dR}\exp(\mathfrak{g})_\bullet \in PreSmoothTypes = PSh(CartSp,sSet)$

  for the [[simplicial presheaf]]

  $$
    \flat_{dR}\exp(\mathfrak{g})_\bullet
    \;\colon\;
    (U \times k) \mapsto 
    Hom_{dgAlg}( CE(\mathfrak{g}), \Omega^{\bullet\geq 1, \bullet}_{si}(U \times \Delta^k_{smth}) )
  $$

  of those differential forms on $U \times \Delta^\bullet$ with at least one leg along $U$;

* $\Omega^1_{flat}(-,\mathfrak{g}) 
   \coloneqq 
   \flat_{dR}\exp(\mathfrak{g})_0
  \longrightarrow \flat_{dR}\exp(\mathfrak{g})_\bullet$

  for the canonical inclusion of the degree-0 piece, regarded as a simplicial constant simplicial presheaf.

=--

+-- {: .num_example #ExamplesOfLieIntegration}
###### Example

From the discussion at _[[Lie integration]]_:

1. $\Omega^1_{flat}(-,b^{p+1}\mathbb{R}) = \mathbf{\Omega}^{p+2}_{cl}$;

1. for $\mathfrak{g}$ an ordinary [[Lie algebra]], then for the [[simplicial skeleton|2-coskeleton]]

   $$
     cosk_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G_\bullet
   $$

   for $G$ the simply connected [[Lie group]] associated to $\mathfrak{g}$ by traditional [[Lie theory]]. If $\mathfrak{g}$ is furthermore a [[semisimple Lie algebra]], then also

   $$
     cosk_3 \exp(\mathfrak{g}) \simeq \mathbf{B}G_\bullet
   $$

1. for $\mathfrak{g} = b^{p}\mathbb{R}$ the [[line Lie n-algebra|line Lie p+1]]-algebra, then 

   $$
     \exp(b^p \mathbb{R}) \simeq \mathbf{B}^{p+1}\mathbb{R}
     \,.
   $$


=--

+-- {: .num_remark #LieIntegrationIsFunctorial}
###### Remark

The constructions in def. \ref{SimplicialLieIntegrationOfLinfinityAlgebra} are clearly [[functor|functorial]]: given a [[homomorphism]] of [[L-∞ algebras]]

$$
  \mu \;\colon\; \mathfrak{g} \longrightarrow \mathfrak{h}
$$


it prolongs to a homomorphism of presheaves

$$
  \mu \colon \Omega^1_{flat}(-,\mathfrak{g})
  \longrightarrow \Omega^1(-,\mathfrak{h})
$$

and of [[simplicial presheaves]]

$$
  \exp(\mu)
  \;\colon\;
  \exp(\mathfrak{g})
  \longrightarrow
  \exp(\mathfrak{h})
$$

etc.


=--

+-- {: .num_example #LInfinityCocyclesAsMorphisms}
###### Example

A degree-$(p+2)$-[[L-∞ cocycle]] $\mu$ on an [[L-∞ algebra]] $\mathfrak{g}$ is a homomorphism of the form

$$
  \mu \colon \mathfrak{g} \longrightarrow b^{p+1}\mathbb{R}
$$

to the [[line Lie n-algebra|line Lie (p+2)-algebra]] $b^{p+1}\mathbb{R}$.
The [[formal dual]] of this is the homomorphism of [[dg-algebras]]

$$
  CE(\mathfrak{g}) \longleftarrow CE(b^{p+1}\mathbb{R}) \colon \mu^\ast
$$

which manifestly picks a $d_{CE(\mathfrak{g})}$-closed element in $CE^{p+2}(\mathfrak{g})$.

Precomposing this $\mu^\ast$ with a flat [[L-∞ algebra valued differential form]]

$$
  A \in \Omega^1_{flat}(X,\mathfrak{g}) = Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet(X))
$$

yields, by example \ref{ExamplesOfLieIntegration}, a plain closed $(p+2)$-form

$$
  \mu^\ast A \in \Omega^{p+2}_{cl}(X)
  \,.
$$

=--

+-- {: .num_defn #GroupOfPeriods}
###### Definition

Given an [[L-∞ cocycle]]

$$
  \mu \colon \mathfrak{g} \longrightarrow b^{p+1}\mathbb{R}
  \,,
$$

as in example \ref{LInfinityCocyclesAsMorphisms}, 
then its _group of [[periods]]_ is the [[discrete group|discrete]] additive [[subgroup]] $\Gamma \hookrightarrow \mathbb{R}$ of those [[real numbers]] which are [[integration of differential forms|integrations]]

$$
  \int_{\partial \Delta^{p+3}_{smth}} \mu^\ast A \in \mathbb{R}
$$

of the value of $\mu$, as in example \ref{LInfinityCocyclesAsMorphisms}, 
on [[L-∞ algebra valued differential forms]]

$$
  A \in \Omega^1_{flat}(\partial \Delta^{p+3}_{smth})
  \,,
$$

over the [[boundary of a simplex|boundary of the (p+3)-simplex]] (which are forms with sitting instants on the $(p+2)$-dimensional faces that glue together; without restriction of generality we may simply consider forms on the $(p+2)$-[[sphere]] $S^{p+2}$).

=--


+-- {: .num_prop #TruncatedLieIntegrationOfCocycle}
###### Proposition

Given an [[L-∞ cocycle]] $\mu \colon \mathfrak{g} \to b^{p+1}\mathbb{R}$, 
as in example \ref{LInfinityCocyclesAsMorphisms},
then the universal Lie integration of $\mu$, via def. \ref{SimplicialLieIntegrationOfLinfinityAlgebra} and remark \ref{LieIntegrationIsFunctorial}, descends to the $(p+2)$-[[coskeleton]]

$$
  \mathbf{B}G_\bullet \coloneqq cosk_{p+2}\exp(\mathfrak{g})
$$

up to quotienting the coefficients $\mathbb{R}$ by the 
group of [[periods]] $\Gamma$ of $\mu$, def. \ref{GroupOfPeriods}, to yield the bottom morphism in

$$
  \array{
     \exp(\mathfrak{g}) &\stackrel{\exp(\mu)}{\longrightarrow}&
     \mathbf{B}^{p+2}\mathbb{R}
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}G_\bullet
     &\stackrel{\mathbf{c}}{\longrightarrow}&
     \mathbf{B}^{p+2} (\mathbb{R}/\Gamma)_\bullet
  }
  \,.
$$

=--

This is fairly immediate from the definitions, detailed discussion is in ([FSS 12](Lie+integration#FSS12)). 

Here and in the following we are freely using example \ref{ExamplesOfLieIntegration} to identify $\exp(b^{p+1}\mathbb{R}) \simeq \mathbf{B}^{p+2}\mathbb{R}$. Establishing this is the only real work in prop. \ref{TruncatedLieIntegrationOfCocycle}.


#### The WZW terms

+-- {: .num_prop #HodgeFiltrationRefinementFromLInfinityCocycles}
###### Proposition

For $\mu \colon \mathfrak{g}\longrightarrow b^{p+1}\mathbb{R}$
an [[L-∞ cocycle]], then there is the following canonical [[commuting diagram]] of [[simplicial presheaves]]

$$
   \array{
    \Omega^1_{flat}(-,G)
    &\stackrel{\mu}{\longrightarrow}&
    \Omega^2_{cl}(-,\mathbb{G})
    \\
    \downarrow && \downarrow
    \\
    \flat_{dR}\mathbf{B}G
    &\stackrel{\flat_{dR} \mathbf{c}}{\longrightarrow}&
    \flat_{dR}\mathbf{B}^2 \mathbb{G}
  }
  \;\;\;
  \coloneqq
  \;\;\;
  \array{
    \Omega^1_{flat}(-,\mathfrak{g})
    &\stackrel{\mu}{\longrightarrow}&
    \mathbf{\Omega}^{p+2}_{cl}
    \\
    \downarrow && \downarrow
    \\
    \flat_{dR}\exp(\mathfrak{g})_\bullet
    &
    \stackrel{\flat_{dR}\exp(\mu)}{\longrightarrow}
    &
    \flat_{dR}\mathbf{B}^{p+2}\mathbb{R}
    \\
    \downarrow && \downarrow
    \\
    \flat_{dR}\mathbf{B}G
    &\stackrel{\flat_{dR}\mathbf{c}}{\longrightarrow}&
    \flat_{dR}\mathbf{B}^{p+2}\mathbb{R}
  }
$$

which is given 

* on the top by def. \ref{SimplicialLieIntegrationOfLinfinityAlgebra}, 
example \ref{ExamplesOfLieIntegration},
remark \ref{LieIntegrationIsFunctorial}, 

* on the bottom by prop. \ref{TruncatedLieIntegrationOfCocycle},

Moreover, this presents a 
refinement of the canonical [[Hodge filtration]] on $\mathbf{B}^{p}(\mathbb{R}/\Gamma)$, def. \ref{RefinementOfHodgeFiltration}, 
along the cocycle $\mathbf{c}$ which Lie integrates $\mu$
via prop. \ref{TruncatedLieIntegrationOfCocycle}.

=--

+-- {: .num_defn #DifferentiallyTiwstedGroup}
###### Definition

Write

$$
  \tilde G
  \coloneqq
  G \underset{\flat_{dR}\mathbf{B}G}{\times} \mathbf{\Omega}^1_{flat}(-,\mathfrak{g})
$$

for the [[homotopy pullback]] of the left vertical morphism in prop. \ref{HodgeFiltrationRefinementFromLInfinityCocycles} along (the [[modulating morphism]] for) the [[Maurer-Cartan form]] $\theta_G$ of $G$, i.e. for the object sitting in a homotopy Cartesian square of the form

$$
  \array{
    \tilde G &\stackrel{\theta_{\tilde G}}{\longrightarrow}&  \mathbf{\Omega}^1_{flat}(-,\mathfrak{g})
    \\
    \downarrow && \downarrow
    \\
    G &\stackrel{\theta_G}{\longrightarrow}& \flat_{dR}\mathbf{B}G
  }
  \,.
$$

=--


+-- {: .num_example #ExamplesForTildeGInModLayer}
###### Example

For the special case that $G$ is an ordinary [[Lie group]], then $\flat_{dR}\mathbf{B}G \simeq \Omega^{1}_{flat}(-,\mathfrak{g})$, hence in this case the morphism being pulled back in def. \ref{DifferentiallyTiwstedGroup} is an [[equivalence]], and so in this case nothing new happens, we get $\tilde G \simeq G$.

On the other extreme, when $G = \mathbf{B}^{p}U(1)$ is the [[circle n-group|circle (p+1)-group]], then def. \ref{DifferentiallyTiwstedGroup} reduces to the [[homotopy pullback]] that characterizes the [[Deligne complex]] and hence yields

$$
  \widetilde{\mathbf{B}^p U(1)}
  \simeq
  \mathbf{B}^p U(1)_{conn}
  \,.
$$

This shows that def. \ref{DifferentiallyTiwstedGroup} is a certain non-abelian generalization 
of [[ordinary differential cohomology]]. We find further characterization of this below in corollary \ref{TildeHatGIsDifferentialModuliBundle}, see remark \ref{InterpretationOfTildeHatG}.


=--

+-- {: .num_remark}
###### Remark

From example \ref{ExamplesForTildeGInModLayer}
one see the conceptial meaning of def. \ref{DifferentiallyTiwstedGroup}:


For $G$ a [[Lie group]], then the de Rham coefficients are just globally defined differential forms, $\flat_{dR}\mathbf{B}G \simeq \Omega^1_{flat}(-,\mathfrak{g})$ (by the discussion [here](smooth+infinity-groupoid+--+structures#deRhamWithCoefficientsInBOfLieGroup)), and in particular therefore the [[Maurer-Cartan form]] $\theta_G \colon G \to \flat_{dR}\mathbf{B}G$ is a globally defined differential form. This is no longer the case for general [[smooth ∞-groups]] $G$. In general, the [[Maurer-Cartan forms]] here is a [[cocycle]] in [[hypercohomology]], given only locally by differential forms, that are glued nontrivially, in general, via [[gauge transformations]] and [[higher gauge transformations]] given by lower degree forms.

But the WZW terms that we are after are supposed to be [[prequantizations]] of globally defined Maurer-Cartan forms. The homotopy pullback in def. \ref{DifferentiallyTiwstedGroup} is precisely the [[universal construction]] that enforces the existence of a globally defined Maurer-Cartan form for $G$, namely  $\theta_{\tilde G} \colon \tilde G \to \Omega^1_{flat}(-,\mathfrak{g})$.

=--


+-- {: .num_defn #WZWTermFromLieIntegration}
###### Definition

Given an [[nLab:L-∞ cocycle]] $\mu \colon \mathfrak{g}\longrightarrow b^{p+1}\mathbb{R}$, then via prop. \ref{HodgeFiltrationRefinementFromLInfinityCocycles}, prop. \ref{TruncatedLieIntegrationOfCocycle} and using the [[nLab:natural transformation|naturality]] of the [[nLab:Maurer-Cartan form]], we have a morphism of [[nLab:cospan]] [[nLab:diagrams]] of the form

$$
  \array{
    \Omega^1_{flat}(-,\mathfrak{g})
    &\stackrel{\mu}{\longrightarrow}&
    \mathbf{\Omega}^{p+2}_{cl}
    \\
    \downarrow && \downarrow
    \\
    \flat_{dR} \mathbf{B}G
    &\stackrel{\flat_{dR}\mathbf{c}}{\longrightarrow}&
    \flat_{dR}\mathbf{B}^{p+2}\mathbb{R}
    \\
    \uparrow^{\mathrlap{\theta_G}} && \uparrow^{\mathrlap{\theta_{\mathbf{B}^{p+1}(\mathbb{R}/\Gamma)}}}
    \\
    G &\stackrel{\Omega \mathbf{c}}{\longrightarrow}&
    \mathbf{B}^{p+1} (\mathbb{R}/\Gamma)
  }
  \,.
$$

By the homotopy fiber product characterization of the [[nLab:Deligne complex]] this yields a morphism of the form

$$
  \mathbf{L}_{WZW}^{\mu}
   \;\colon\;
   \tilde G
   \longrightarrow
   \mathbf{B}^{p+1}(\mathbb{R}/\Gamma)_{conn}
  \,.
$$

which [[nLab:modulating morphisms|modulates]] a [[nLab:circle n-bundle with connection|p+1-connection]]/[[nLab:Deligne cohomology|Deligne cocycle]] on the differentially extended smooth $\infty$-group $\tilde G$ from def. \ref{DifferentiallyTiwstedGroup}.

This we call the _WZW term_ obtained by universal Lie integration from $\mu$.

=--

Essentially this construction originates in ([[schreiber:The brane bouquet|FSS 13]]).

+-- {: .num_remark}
###### Remark

The WZW term of def. \ref{WZWTermFromLieIntegration} is a [[prequantization]] of 

$$
  \omega \coloneqq \mu(\theta_{\tilde G})
$$

$$
  \array{
     && \mathbf{B}^{p+1}(\mathbb{R}/\Gamma)_{conn}
     \\
     & {}^{\mathllap{\mathbf{L}_{WZW}^\mu}}\nearrow & \downarrow^{\mathrlap{F_{(-)}}}
     \\
     \tilde G
     &\stackrel{\mu(\theta_{\tilde G})}{\longrightarrow}& \mathbf{\Omega}^{p+2}
  }
  \,.
$$


=--


#### Consecutive WZW terms and twists
 {#ConsecutiveWZWTermsAndTwists}

More generally, one has a sequence of [[L-∞ cocycles]], each defined on the extension that is classified by the previous one -- a [[schreiber:The brane bouquet|bouquet]] of cocycles.

In each stage, for $\mu_1 \colon \mathfrak{g}\to b^{p_1+1}\mathbb{R}$ a cocycle and $\hat {\mathfrak{g}} \to \mathfrak{g}$ the extension that it classifies (its [[homotopy fiber]]), then the next cocycle is of the form $\mu_2 \colon \hat \mathfrak{g} \to b^{p_2+1}\mathbb{R}$

$$
  \array{
    \hat {\mathfrak{g}} &\stackrel{\mu_2}{\longrightarrow}& b^{p_2+1}\mathbb{R}
    \\
    \downarrow
    \\
    \mathfrak{g} &\stackrel{\mu_1}{\longrightarrow}& b^{p_1+1}\mathbb{R}
  }
  \,.
$$


+-- {: .num_lemma #CharacterizationOfLInfinityHomotopyFibers}
###### Lemma

The [[homotopy fiber]] $\hat \mathfrak{g} \to \mathfrak{g}$ of $\mu_1$ is given by the ordinary [[pullback]]

$$
  \array{
    \hat \mathfrak{g} &\longrightarrow& e b^{p_1} \mathbb{R}
    \\
    \downarrow && \downarrow 
    \\
    \mathfrak{g} &\stackrel{\mu_1}{\longrightarrow}& b^{p_1+1}\mathbb{R}
  }
  \,,
$$ 

where $e b^{p_1}\mathbb{R}$ is defined by its [[Chevalley-Eilenberg algebra]] 
$CE(e b^{p_1}\mathbb{R})$ being the [[Weil algebra]] of $b^{p_1}\mathbb{R}$, which is the [[free construction|free]] differential graded algebra on a generator in degree $p_1$, and where the right vertical map takes that generator to 0 and takes its free image under the differential to the generator of $CE(b^{p_1+1}\mathbb{R})$.

=--

+-- {: .proof}
###### Proof

This follows with the [recognition principle for L-∞ homotopy fibers](model+structure+for+L-infinity+algebras#HomotopyFiberProducts).

=--

+-- {: .num_cor #PullbackOfDifferentialFormCoefficients}
###### Corollary


A [[homotopy fiber sequence]] of [[L-∞ algebras]] $\hat \mathfrak{g} \to \mathfrak{g}\stackrel{\mu}{\longrightarrow} b^{p+1}\mathbb{R}$ induces a  [[homotopy pullback]] diagram of the the associated objects of [[L-∞ algebra valued differential forms]], def. \ref{SimplicialLieIntegrationOfLinfinityAlgebra}, of the form

$$
  \array{
    \mathbf{\Omega}^1_{flat}(-,\hat {\mathfrak{g}})
    &\stackrel{}{\longrightarrow}&
    \mathbf{\Omega}^{p+1}
    \\
    \downarrow && \downarrow^{\mathbf{d}}
    \\
    \mathbf{\Omega}^1_{flat}(-,\mathfrak{g})
    &\stackrel{\mu}{\longrightarrow}&
    \mathbf{\Omega}^{p+2}_{cl}
  }
$$



(hence an ordinary [[pullback]] of [[presheaves]], since these are all simplicially constant).

=--

+-- {: .proof}
###### Proof

The construction $\mathfrak{g} \mapsto Hom_{dgAlg}(CE(\mathfrak{g}), \Omega^\bullet(-))$ preserves [[pullbacks]] ($CE$ is an anti-equivalence onto its image, pullbacks of (pre-)-sheaves are computed objectwise, the [[hom-functor]] preserves pullbacks in the covariant argument).

Observe then (see the discussion at _[[L-∞ algebra valued differential forms]]), that while

$$
  \mathbf{\Omega}^{p+2}_{cl} \simeq Hom_{dgAlg}(CE(b^{p+1}), \Omega^\bullet(-))
$$

we have

$$
  \mathbf{\Omega}^{p+1} \simeq Hom_{dgAlg}(W(b^{p}), \Omega^\bullet(-))
  \,.
$$

With this the statement follows by
lemma \ref{CharacterizationOfLInfinityHomotopyFibers}.

=--

+-- {: .num_defn #ConsecutiveCocycles}
###### Definition

We say that a pair of [[L-∞ cocycles]] $(\mu_1, \mu_2)$ is _consecutive_ if the domain of the second is the extension ([[homotopy fiber]]) defined by the first

$$
  \array{
    \hat {\mathfrak{g}} &\stackrel{\mu_2}{\longrightarrow}& b^{p_2+1}
    \\
    \downarrow
    \\
    \mathfrak{g} &\stackrel{\mu_1}{\longrightarrow}& b^{p_1+1}\mathbb{R}
  }
$$

and if the truncated [[Lie integrations]] of these cocycles via prop. \ref{TruncatedLieIntegrationOfCocycle} preserves the extension property in that also

$$
  \hat G \to G \stackrel{\Omega \mathbf{c}_1}{\longrightarrow} \mathbf{B}^{p_1+1}(\mathbb{R}/\Gamma_1)
$$

is a [[homotopy fiber sequence]] of [[smooth homotopy types]].

=--

+-- {: .num_remark}
###### Remark

The issue of the second clause in def. \ref{ConsecutiveCocycles} is to do with the truncation degrees: the universal untruncated [[Lie integration]] $\exp(-)$ preserves homotopy fiber sequences, but if there are non-trivial cocycles on $\mathfrak{g}$ in between $\mu_1$ and $\mu_2$, for $p_2 \gt p_1$, then these will remain as nontrivial homotopy groups in the higher-degree truncation $\mathbf{B}G_{2} \coloneqq \tau_{p_2}\exp(\hat\mathfrak{g})$ (see [Henriques 06, theorem 6.4](Lie+integration#Henriques)) but they will be truncated away in $\mathbf{B}G_1 \coloneqq \tau_{p_1}\exp(\mathfrak{g})$ and will hence spoil the preservation of the homotopy fibers through Lie integration. 

Notice that extending along consecutive cocycles is like the extension stages in a [[Whitehead tower]].

=--

Given two consecutive [[L-∞ cocycles]] $(\mu_1,\mu_2)$, def. \ref{ConsecutiveCocycles}, let

$$
  \mathbf{L}_1 \colon \tilde G \longrightarrow \mathbf{B}^{p_1+1}(\mathbb{R}/\Gamma_1)_{conn}
$$


and

$$
  \mathbf{L}_2 \colon \widetilde {\hat G} \longrightarrow \mathbf{B}^{p_2+1}(\mathbb{R}/\Gamma_2)_{conn}
$$

be the WZW terms obtained from the two cocycles via def. \ref{WZWTermFromLieIntegration}.


+-- {: .num_prop #ConsecutiveWZWTermsFromConsecutiveLInfinityCocycles}
###### Proposition

There is a [[homotopy pullback]] square in [[smooth homotopy types]] of the form

$$
  \array{
     \widetilde {\hat G}
     &\stackrel{}{\longrightarrow}&
     \mathbf{\Omega}^{p_1+1}
     \\
     \downarrow && \downarrow
     \\
     \tilde G
     &\stackrel{\mathbf{L}_1}{\longrightarrow}&
     \mathbf{B}^{p_1+1}(\mathbb{R}/\Gamma_1)_{conn}
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

Consider the following [[pasting]] composite

$$
  \array{
    \mathbf{\Omega}^{p_1+1}
    &\longrightarrow&
    \ast
    &\longleftarrow&
    \ast
    \\
    {}^{\mathllap{\mathbf{d}}}\downarrow &\swArrow& \downarrow && \downarrow
    \\
    \mathbf{\Omega}^{p_1+2}
    &\longrightarrow&
    \flat_{dR}\mathbf{B}^{p_1+2}\mathbb{R}
    &\stackrel{\theta_{\mathbf{B}^{p_1}(\mathbb{R}/\Gamma_1)}}{\longleftarrow}&
    \mathbf{B}^{p_1+1}\mathbb{R}
     \\
     \uparrow^{\mathrlap{\mu_1}} && \uparrow^{\mathrlap{\flat_{dR} \mathbf{B}G}} && \uparrow^{\mathrlap{\Omega \mathbf{c}_1}}
     \\
     \mathbf{\Omega}^1_{flat}(-,\mathfrak{g})
     &\stackrel{}{\longrightarrow}&
     \flat_{dR}\mathbf{B}G
     &\stackrel{\theta_G}{\longleftarrow}&
     G
  }
  \,,
$$

where 

* the top left square is the evident homotopy;

* the bottom left square is from prop. \ref{HodgeFiltrationRefinementFromLInfinityCocycles}

* the right square is the naturality of the [[Maurer-Cartan form]] construction.

Under forming [[homotopy limits]] over the _horizontal_ cospan diagrams here, this turns into 

$$
  \array{
     \mathbf{\Omega}^{p_1+1}
     \\
     \downarrow
     \\
     \mathbf{B}^{p_1+1}(\mathbb{R}/\Gamma_1)_{conn}
     \\
     \uparrow^{\mathrlap{\mathbf{L}_1}}
     \\
     \tilde G
  }
$$

by prop. \ref{WZWTermByUniversality}. On the other hand, forming homotopy limits _vertically_ this turns into

$$
  \array{
    \mathbf{\Omega}^1_{flat}(-,\hat \mathfrak{g})
    &\longrightarrow&
    \flat_{dR}\mathbf{B}G_2
    &\stackrel{\theta_{\hat G}}{\longleftarrow}&
    \hat G
  }
$$

(on the left by corollary \ref{PullbackOfDifferentialFormCoefficients}, on the right by the second clause in def. \ref{ConsecutiveCocycles}).

The homotopy limit over that last [[cospan]], in turn, is $\widetilde{\hat G}$. This implies the claim by the fact that homotopy limits commute with each other.

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{ConsecutiveWZWTermsFromConsecutiveLInfinityCocycles} says how consecutive pairs of $L_\infty$-cocycles Lie integrate suitably to consecutive pairs of WZW terms.


=--

+-- {: .num_cor #TildeHatGIsDifferentialModuliBundle}
###### Corollary

In the above situation there is a [[homotopy fiber sequence]] of the form

$$
  \array{
    \mathbf{B}^{p_1}(\mathbb{R}/\Gamma_1)_{conn}
    &\longrightarrow&
    \widetilde {\hat G}
    \\
    && \downarrow
    \\
    && \tilde G
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{ConsecutiveWZWTermsFromConsecutiveLInfinityCocycles} and the [[pasting law]], the [[homotopy fiber]] of $\widetilde {\hat G} \to \tilde G$ is equivalently the homotopy fiber of $\mathbf{\Omega}^{p_1+1}\to \mathbf{\Omega}^{p_1+2}_{cl}$

$$
  \array{
     \mathbf{B}^{p_1}(\mathbb{R}/\Gamma_1)_{conn} &\longrightarrow&
     \widetilde {\hat G}
     &\stackrel{}{\longrightarrow}&
     \mathbf{\Omega}^{p_1+1}
     \\
     \downarrow && \downarrow && \downarrow
     \\
     \ast
     &\longrightarrow&
     \tilde G
     &\stackrel{\mathbf{L}_1}{\longrightarrow}&
     \mathbf{B}^{p_1+1}(\mathbb{R}/\Gamma_1)_{conn}
  }
  \,.
$$

=--

+-- {: .num_remark #InterpretationOfTildeHatG}
###### Remark

Corollary \ref{TildeHatGIsDifferentialModuliBundle} says that $\widetilde {\hat G}$ is a [[bundle]] of [[moduli stacks]] for [[differential cohomology]] over $\tilde G$. This means that maps

$$
  \Sigma \longrightarrow \widetilde{\hat G}
$$

(which are the [[field (physics)|fields]] of the higher [[WZW model]] with WZW term $\mathbf{L}_2$) are pairs of plain maps $\phi \colon \Sigma \to \tilde G$ together with a differential cocycle on $\Sigma$, i.e. a $p_1$-form connection on $\Sigma$, which is twisted by $\phi$ in a certain way.

This oocurs for the (properly globalized) [[Green-Schwarz super p-brane sigma models]] of all the [[D-branes]] and of the [[M5-brane]]. For the D-branes $p_1 = 1$ and so there is a 1-form connection on their [[worldvolume]], the [[Chan-Paton gauge field]]. For the [[M5-brane]] $p_1 = 2$ and so there is a 2-form connection on its worldvolume, the [[self-dual higher gauge field]] in 6d.

=--


### Semantic layer

We discuss the general abstract formulation of WZW terms in a [[cohesive (infinity,1)-topos]].

Throughout, let 

* $\mathbf{H}$ an [[cohesive (∞,1)-topos]];

* $\mathbb{G} \in \mathbf{H}$ be an object equipped with the structure of a [[braided ∞-group]], i.e. with specified double [[delooping]] $\mathbf{B}^2 \mathbb{G}$.

* $\Omega^2_{cl}(-,\mathbb{G}) \to \cdots \to \flat_{dR}\mathbf{B}\mathbb{G}$ a chosen [[Hodge filtration]];

* $G \in \mathbf{H}$ be any object equipped with [[∞-group]] structure, i.e. with specified [[delooping]] $\mathbf{B}G$;

* $\mathbf{c} \;\colon\; \mathbf{B}G \longrightarrow \mathbf{B}^2 \mathbb{G}$ a morphism, hence a [[cocycle]] in the [[group cohomology]] of $G$ with [[coefficients]] in $\mathbb{G}$.


Write

* $\mathbf{B}\mathbb{G}_{conn} \coloneqq \mathbf{B}\mathbb{G} \underset{\flat_{dR}\mathbf{B}^2 \mathbb{G}}{\times} \Omega^2_{cl}(-,\mathbb{G})$

  for the induced [[coefficients]] for $\mathbb{G}$-[[differential cohomology]], as discussed at _[[geometry of physics -- principal connections]]_;

* $\hat G \to G$ for the [[infinity-group extension]] classified by $\mathbf{c}$.

#### Refinement of Hodge filtrations

+-- {: .num_defn #RefinementOfHodgeFiltration}
###### Definition

A _refinement of the [[Hodge filtration]]_ of $\mathbb{G}$ along the cocycle $\mathbf{c}$ is a choice of [[0-truncated]] object $\Omega^1_{flat}(-,G) \in \mathbf{H}$ and a completion to a diagram

$$
  \array{
    \Omega^1_{flat}(-,G)
    &\stackrel{\mu}{\longrightarrow}&
    \Omega^2_{cl}(-,\mathbb{G})
    \\
    \downarrow && \downarrow
    \\
    \flat_{dR}\mathbf{B}G
    &\stackrel{\flat_{dR} \mathbf{c}}{\longrightarrow}&
    \flat_{dR}\mathbf{B}^2 \mathbb{G}
  }
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

For $G$ an ordinary [[Lie group]], then $\mu$ may be taken to be the [[Lie algebra cohomology|Lie algebra cocycle]] corresponding to $\mathbf{c}$ and then $\tilde G \simeq G$.

On the opposite extreme, for $G = \mathbf{B}^p U(1)$ itself with $\mathbf{c}$ the identity, then $\tilde G = \mathbf{B}^pU (1)_{conn}$ is the [[coefficients]] for [[ordinary differential cohomology]] (the [[Deligne complex]] under [[Dold-Kan correspondence]] and [[infinity-stackification]]).

Hence a more general case is a fibered product of these two, where $\tilde G$ is such that a map $\Sigma \longrightarrow \tilde G$ is equivalently a pair consisting of a map $\Sigma \to G$ and of differential $p$-form data on $\Sigma$. This is the case of relevance for WZW models of [[super p-branes]] with "tensor multiplet" fields on them, such as the [[D-branes]] and the [[M5-brane]].

=--

#### WZW terms

+-- {: .num_prop #WZWTermByUniversality}
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

+-- {: .proof}
###### Proof

The morphism in question is the image under forming [[homotopy limits]] of the morphism of [[cospan]] diagrams

$$
  \array{
     \Omega^1_{flat}(-,G) &\stackrel{\mu}{\longrightarrow}& \Omega^2_{cl}(-,\mathbb{G})
     \\
     \downarrow && \downarrow
     \\
     \flat_{dR}\mathbf{B}G
     &\stackrel{\flat_{dR}\mathbf{c}}{\longrightarrow}&
     \flat_{dR}\mathbf{B}^2 \mathbb{G}
     \\
     \uparrow^{\mathrlap{\theta_G}} &&  \uparrow^{\mathrlap{\theta_{\mathbf{B}\mathbb{G}}}}
     \\
     G &\stackrel{\Omega \mathbf{c}}{\longrightarrow}& \mathbf{B}\mathbb{G}
  }
  \,,
$$ 

where the top square is from def. \ref{RefinementOfHodgeFiltration} and where the bottom square is the naturality square of the [[homotopy fiber sequence]] that defines the [[Maurer-Cartan forms]] (see [here](Maurer-Cartan+form#OnCohesiveHomotopyTypes)).

=--

#### Definite globalization of WZW terms

...[[definite globalization of WZW terms]]...

### Syntax layer

## References

* _[[schreiber:differential cohomology in a cohesive topos]]_ ([pdf](https://dl.dropboxusercontent.com/u/12630719/dcct.pdf))