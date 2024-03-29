
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[physics]] the [[critical locus]] of the [[action functional]], hence the [[solution]] space to the [[partial differential equation|partial differential]] [[equations of motion]] is often called the _shell_, or the _physical shell_ (the [[diffiety]] corresponding to the PDE of motion). 

This terminology derives from the case of the free [[relativistic particle]] propagating in [[Minkowski spacetime]], for which the space of solutions is the hyperbola of vectors whose [[Minkowski metric|Minkowski norm square]] is the [[mass]] of the particle. This hyperbola is naturally called the _mass shell_.

It is common to use the adjective "on-shell" for statements that apply after restriction to the shell, and "off-shell" for statements that apply generally. 

For instance [[Noether's theorem]] gives for each symmetry of a [[local Lagrangian]] an _on-shell [[conserved current]]_, namely a differential form on spacetime, depending on the field configurations, which is closed (only, in general) if the given field configuration satisfies its equations of motion. Such a differential form which is closed even if the equations of motion do not hold would be called an _off-shell conserved current_.

## Details

In terms of [[variational calculus]] the field configurations are encoded by a [[field bundle]] $E$ over [[spacetime]]/[[worldvolume]] $\Sigma$ as being the [[sections]] of this bundle. The shell then is encoded by a sub-bundle 

$$
  \array{
    \mathcal{E} &&\hookrightarrow && J^\infty_\Sigma E
    \\
    & \searrow && \swarrow
    \\
    && \Sigma
  }
$$

of the [[jet bundle]] $J^\infty_\Sigma E$ of $E$, namely the subbundle of those pointwise field configurations with those jets (derivatives) that do solve the equations of motion (see at _[[diffiety]]_).

This way a field configuration given by a section $\phi$ of $E$ is a solution to the equations of motion precisely if its [[jet prolongation]], being a section of $J^\infty_\Sigma E$ comes from a section of $\mathcal{E}$ under this inclusion.

If one thinks of all this not as happening in the [[category]] of [[bundles]] over $\Sigma$ but in the category $PDE_\Sigma$ of [[partial differential equations]] over $\Sigma$, then the above inclusion becomes simply $\iota \colon \mathcal{E} \hookrightarrow E$, where now $E$ is thought of as the trivial partial differential equation on its sections, the one for which each section is a solution. Then a field configuration is just a morphism $\phi : \Sigma \longrightarrow E$ in $PDE_\Sigma$, and this is a solution precisely if it factors through the inclusion of the shell:

$$
  \array{
    && \mathcal{E}
    \\
    & {}^\mathllap{\phi_{sol}}{\nearrow} & \downarrow^{\mathrlap{\iota}}
    \\
    \Sigma &\underset{\phi}{\longrightarrow}& E
  }
$$

Accordingly, a [[variational bicomplex|horizontal form]] $J \in \Omega^{p}_H(E) \hookrightarrow \Omega^{p+1}(J^\infty_\Sigma E)$ is an _on-shell [[conserved current]]_ if it becomes horizontally closed after restriction to the shell:

$$
  \iota^\ast d_H J = 0
  \,.
$$

## Properties

For $(E,\mathbf{L})$ a [[Lagrangian field theory]], let $\mathcal{E}^\infty \hookrightarrow J^\infty_\Sigma(E)$ be the prolonged shell.

The following is intuitively obvious but not entirely trivial to prove:

+-- {: .num_prop #InfinitesialSymmetryOfTheLagrangianIsAlsoSymmetryOfTheShell}
###### Proposition
**([[infinitesimal symmetry of the Lagrangian]] is also symmetry of the shell)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]]. Then if $\hat v$ is the prolongation of an [[evolutionary vector field]] which is an [[infinitesimal symmetry of the Lagrangian]] in that the [[Lie derivative]] of $\mathbf{L}$ along $\hat v$ is [[horizontal derivative|horizontally exact]], then the [[flow]] of $\hat v$ preserves the prolonged shell.

=--

([Olver 95, theorem 5.53](#Olver95))

## References

* _[Higher prequantum geometry II: The principle of extremal action -- comonadically](https://www.physicsforums.com/insights/higher-prequantum-geometry-ii-principle-extremal-action-comonadically/)_


* {#Olver95} [[Peter Olver]], _Applications of Lie groups to differential equations_, Springer; _Equivalence, invariants, and symmetry_, Cambridge Univ. Press (1995) &lbrack;[doi:10.1007/978-1-4684-0274-2](https://doi.org/10.1007/978-1-4684-0274-2)&rbrack;


[[!redirects shells]]

[[!redirects on-shell]]
[[!redirects off-shell]]

[[!redirects mass shell]]
[[!redirects mass shells]]

[[!redirects prolonged shell]]
