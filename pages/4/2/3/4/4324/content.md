
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### General 

A **connective spectrum** is a [[connective object]] in the [[stable (infinity,1)-category of spectra|stable $\infty$-category of spectra]],  hence a [[spectrum]] $S$ whose [[homotopy group of a spectrum|homotopy groups]] in all [[negative number|negative]] degrees are [[trivial groups|trivial]]: $\pi_{\bullet \lt 0}(S) \,=\, 0$.

These are equivalently:

* [[infinite loop spaces]];

* [[group object in an (infinity,1)-category|grouplike]]$\;$ [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[∞-groupoids]];

* [[abelian ∞-groups]].

Connective spectra form a [[sub-(∞,1)-category]] of [[spectra]]

$$
  Top \stackrel{\supset}{\leftarrow} ConnectSp(Top) \hookrightarrow Sp(Top)
  \,.
$$

There are objects in [[Spectra]], though, that do not come from "naively" [[delooping]] a [[topological space]] infinitely many times.  These are the **non-connective spectra**.  For general spectra there is a notion of [[homotopy groups]] of negative degree. The connective ones are precisely those for which all negative degree [[homotopy groups]] vanish.

### Strict 

There is a subclass of connective spectra that are equivalent to possibly-more-familiar objects, namely nonnegatively graded [[chain complexes]], via the [[Dold-Kan correspondence]]. This identifies [[∞-groupoids]] that are not only connective spectra but even have a _strict_ symmetric monoidal [[group]] structure with non-negatively graded [[chain complex]]es of abelian groups. 

$$
 \array{
  Ch_+ &\stackrel{Dold-Kan \; nerve}{\to}&
  ConnectSp(\infty Grp) \subset \infty Grpd
  \\
  (\cdots A_2 \stackrel{\partial}{\to} A_1 \stackrel{\partial}{\to} A_0 \to 0 \to 0 \to \cdots)
  &\stackrel{}{\mapsto}&
  N(A_\bullet)
 }
$$

The [[homology]] groups of the chain complex correspond precisely to the [[homotopy groups]] of the corresponding [[topological space]] or [[∞-groupoid]].

The free stabilization of the [[(∞,1)-category]] of non-negatively graded chain complexes is simpy the [[stable (∞,1)-category]] of arbitrary chain complexes. There is a [[stable Dold-Kan correspondence]] that identifies these with special objects in $Sp(Top)$. 

$$
 \array{
  Ch &\stackrel{Dold-Kan \; nerve}{\to}&
   Sp(\infty Grp) 
  \\
  (\cdots A_2 \stackrel{\partial}{\to} A_1 \stackrel{\partial}{\to} A_0 \stackrel{\partial}{\to} A_{-1} 
  \stackrel{\partial}{\to} A_{-2} \to \cdots)
  &\stackrel{}{\mapsto}&
  N(A_\bullet)
 }
$$

So it is the homologically nontrivial parts of the chain complexes in negative degree that corresponds to the non-connectiveness of a spectrum.

## Properties


### Inclusion into all spectra
 {#InclusionIntoAllSpectra}

The inclusion 

$$
  Spectra_{\geq 0} \hookrightarrow Spectra
$$

of the [[full sub-(∞,1)-category]] of connective spectra into the [[(∞,1)-category of spectra]] preserves small [[(∞,1)-colimits]]. Moreover, $Spectra_{\geq 0}$ is generated under small [[(∞,1)-colimits]] by the [[sphere spectrum]]. 

These statements prolong to [[sheaves of spectra]].

e.g. ([[Spectral Schemes|Lurie, "Spectral Schemes", example 1.23]])

### Connective cover
 {#ConnectiveCover}

By the [above](#InclusionIntoAllSpectra), connective spectra form a [[coreflective sub-(∞,1)-category]] of the [[(∞,1)-category of spectra]]. The [[right adjoint|right]] [[adjoint (∞,1)-functor]] $\tau_{\geq 0}$ from spectra to connective spectra is called the _[[connective cover]]_ construction, part of the canonical [[t-structure]] on spectra (see [there](t-structure#CanonicalTStructureOnSpectra)).


## Related concepts

* [[connective object]], [[connective cover]]

* [[t-structure]]

* [[model structure for connective spectra]]

## Literature

* [[Jacob Lurie]], pp. 150 in: *[[Higher Algebra]]*

[[!include k-monoidal table]]



[[!redirects connective spectra]]