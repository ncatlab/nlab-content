
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

$Spec(\mathbb{S})$ is the spectrum, in the sense of [[spectrum of a commutative ring]] in [[E-∞ geometry]], of the [[sphere spectrum]] $\mathbb{S}$, in the sense of [[stable homotopy theory]], regarded canonically as the [[initial object in an (∞,1)-category|initial]] [[E-∞ ring]].

This is the refinement to [[E-∞ arithmetic geometry]] of what [[Spec(Z)]] is in [[arithmetic geometry]].

It is the absolute base space, in that it is the [[terminal object in an (∞,1)-category|terminal object]] among [[E-∞ schemes]]. Notably for $E$ any other [[E-∞ ring]], then the essentially unique $E_\infty$-ring homomorphism $\mathbb{S} \longrightarrow E$ (the unit, exhibiting $E$ as an [[E-∞ algebra]] over $\mathbb{S}$) corresponds to an essentially unique morphism

$$
  Spec(E) \longrightarrow Spec(\mathbb{S})
  \,.
$$ 

The [[1-image]] of such a morphism is known as (the [[formal dual]] of) the $E$-[[nilpotent completion]] of $\mathbb{S}$. 

For instance for $E = $ [[HA|H]]$\mathbb{F}_p$, then the 1-image of $Spec(H\mathbb{F}_p) \to Spec(\mathbb{S})$ is $Spec(\mathbb{S}_{(p)})$, the [[formal dual]] of the [[p-completion]] of $\mathbb{S}$, hence the [[infinitesimal neighbourhood]] of $(p)$ in $Spec(S)$. The tool that computes $\mathbb{S}_{(p)}$ (hence the $p$-primary [[stable homotopy groups of spheres]]) by regarding it this way is the original $\mathbb{F}_p$-[[Adams spectral sequence]].

Or for instance for $E = $ [[MU]], then the 1-image of $Spec(MU) \to Spec(\mathbb{S})$ is already all of $Spec(S)$, hence $Spec(MU)$ is [[covering]]. The tool that computes $\mathbb{S}$, hence the full [[stable homotopy groups of spheres]], using this covering is the [[MU]]-[[Adams spectral sequence]], hence the [[Adams-Novikov spectral sequence]].

See at _[Adams spectral sequence -- As derived descent](Adams%20spectral%20sequence#DefinitionInHigherAlgebra)_ for more on this.


## Related concepts

* [spectrum of the category of spectra](prime+spectrum+of+a+symmetric+monoidal+stable+%28?,1%29-category#OfCategoryOfSpectra)

* [[Spec(Z)]]

* [[moduli stack of formal groups]]

* [[chromatic homotopy theory]]