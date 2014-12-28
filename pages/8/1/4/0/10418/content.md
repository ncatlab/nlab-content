
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[G-structure]] one may ask if it is "integrable" in that a certain [[torsion of a G-structure]] vanishes ([[torsion of a Cartan connection]]).

## Definition
 {#Definition}

A $G$-structure is called _locally flat_ ([Sternberg 64, section VII, def. 2.4](#Sternberg64)) or _integrable_ (e.g. [Alekseevskii](#Alekseevskii)) if it is locally equivalent to the standard $G$-structure on the given model space (see also [Lott 90, page 4 of the exposition](#Lott90)).

Let $V$ be a linear local model space, e.g. a [[vector space]] or [[super vector space]]. Write $GL(V)$ for its [[general linear group]]. Consider a [[group]] [[homomorphism]] $G \longrightarrow GL(V)$.

Let $\mathbf{c}_V$ be the _standard flat $G$-structure_ on $V$ (see at _[G-Structure -- Examples -- Standard flat G-structure](G-structure#TheStandardFlatGStructure)_).

Then a [[G-structure]] $\mathbf{c}$ on a [[manifold]] $X$ modeled on $V$ (e.g. a [[smooth manifold]] or [[supermanifold]]) is called integrable if

1. there exists [[cover]] $\{U_i \hookrightarrow X\}$ by [[open subsets]]  $U_i \hookrightarrow V$;

1. such that the $G$-structure $\mathbf{c}$ on $X$ restricts on each patch to the default $G$-structure $\mathbf{c}_0$ on $V$:

   $$
     \mathbf{c}|_{U_i} \simeq \mathbf{c}_0|_{U_i}
     \,.
   $$

### In terms of subbundles

For instance if $G$-structure is modeled by $G$-subbundles $P$ of the [[frame bundle]] (as discussed at _[G-structure -- In terms of subbundles of the frame bundle](G-structure#InTermsOfSubbundlesOfTheFrameBundle)_ ), then it is integrable if each $P \hookrightarrow Fr(X)$ restricts on each patch to $P_0 \hookrightarrow Fr(V)$

$$
  \array{
     P_0|_{U_i} &\hookrightarrow& Fr(V)|_{U_i}
     \\
     {}^{\mathllap{\simeq}}\downarrow && \downarrow
     \\
     P|_{U_i} &\hookrightarrow& Fr(X)|_{U_i}
  }
  \,.
$$


### In terms of differential cohesion
 {#IntermOfDifferentialCohesion}

> under construction

We discuss the concept in the generality of [[higher differential geometry]], formalized in [[differential cohesion]].

So let $\mathbf{H}$ be a [[differential cohesive (∞,1)-topos]].

Let $\mathbb{A}^n \in \mathbf{H}$ be a local model space. such that its synthetic [[frame bundle]] is trivializable and trivialized $Fr(\mathbb{A}^n) \simeq \mathbb{A}^n \times \mathbb{D}^n$  with typical fiber $\mathbb{D}^n \hookrightarrow \mathbb{A}^n$ the [[formal disk]] around any point (as determined by the [[infinitesimal shape modality]]. This may be the [[infinitesimal neighbourhood]] of a point of any order $k$, and accordingly we'll get order $k$-integrability of $G$-structures).

We write

$$
  GL(n) \coloneqq \mathbf{Aut}(\mathbb{D}^n)
$$

for the [[automorphism ∞-group]] of $\mathbb{D}^n$. (When $\mathbb{D}^n$ is the first order [[infinitesimal neighbourhood]] then this is indeed the [[general linear group]], when $\mathbb{D}^n$ is rather the order-$k$ infinitesimal neighbourhood or the full [[formal neighbourhood]] for $k = \infty$, then this is rather $GL^k(n)$. )


Let $X$ be any [[étale groupoid]] modeled on $\mathbb{A}^n$, i.e. $X \in \mathbf{H}$ and there exists a morphism $\coprod_i \mathbb{A}^n \to X$ which is [[formally étale morphism|formally étale]] and [[1-epimorphism|1-epi]].

Then by the discussion at [Frame bundle -- In differential cohesion](frame+bundle#InDifferentialCohesion) the [[frame bundle]] of $X$ is [[modulating morphism|modulated]] by a morphism

$$
  \tau_X \colon X \longrightarrow \mathbf{B}GL(n)
  \,.
$$

Now let $G \in Grp(\mathbf{H})$ be any [[∞-group]] object and $G \to GL(n)$ a [[homomorphism]], hence 

$$
  G\mathbf{struc} \colon \mathbf{B}G \to \mathbf{B}GL(n)
$$ 

any morphism.

Then a _[[G-structure]]_ on $X$ is a diagram in $\mathbf{H}$ of the form

$$
  \array{
     X && \stackrel{\mathbf{c}}{\longrightarrow} && \mathbf{B}G
     \\
     & {}_{\mathllap{\tau_X}}\searrow &\swArrow_{\mathrlap{\simeq}}& \swarrow_{\mathrlap{G\mathbf{Struc}}}
     \\
     && \mathbf{B}GL(n)
  }
$$

hence is a morphism

$$
  \mathbf{c} \colon \tau_X \longrightarrow G\mathbf{Struc}
$$

in the [[slice (∞,1)-topos|slice]] over $\mathbf{B}GL(n)$. In fact $G\mathbf{Struc}\in \mathbf{H}_{/\mathbf{B}GL(n)}$ is the [[moduli ∞-stack]] of such $G$-structures.

The double [[slice (∞,1)-topos|slice]] $(\mathbf{H}_{/\mathbf{B}GL(n)})_{/G\mathbf{Struc}}$ is the [[(∞,1)-category]] of such $G$-structures.

Now by assumption on $\mathbb{A}^n$ it carries the trivial $G$-structure, which we denote by

$$
  \mathbf{c}_0 \colon \tau_{\mathbb{A}^n} \longrightarrow G\mathbf{Struc}
  \,.
$$

The $G$-structure $\mathbf{c}$ is _integrable_ (torsion-free) if 

1. there exists a [[formally étale morphism|formally étale]] [[1-epimorphism|cover]] $\coprod_i U_i \to X$;

   and a [[formally étale morphism]] $q \colon \mathbb{A}^n \longleftarrow \coprod_i U_i$

1. such that this extends to a morphism of $G$-structures 

   $$
      \mathbf{c}_0 \longleftarrow q^\ast \mathbf{c}_0 \longrightarrow \mathbf{c}
   $$


This means that for each $i \in I$ there is a diagram

$$
  \array{
    \tau_{\mathbb{A}^n}
     &\stackrel{}{\longleftarrow}& 
    \tau_{U_i} 
     & \stackrel{}{\longrightarrow} & \tau_X
    \\
    & {}_{\mathllap{\mathbf{c}_0}}\searrow  & 
    {}^{\mathllap{q_i^\ast\mathbf{c}_0}}\downarrow 
    & \swarrow_{\mathrlap{\mathbf{c}}}
    \\
    && G\mathbf{Struc}
  }
$$

in $\mathbf{H}_{/\mathbf{B}GL(n)}$, where the image of the top morphisms  under $\underset{\mathbf{B}GL(n)}{\sum}$ are the given patches $\mathbb{A}^n \leftarrow U_i \to X$.

## Properties

### In terms of adapted coordinate systems

A $G$-structure on $X$ is integrable previsely if there exists an [[atlas]] of $X$ by [[coordinate charts]] with the property that their canonical [[frame fields]] are $G$-frames.

([Sternberg 64, section VII, exercise 2.1](#Sternberg64))

## Examples
For instance 

* a $GL(n,\mathbb{C}) \to GL(2n,\mathbb{R})$-[[G-structure|structure]] is an _[[almost complex structure]]_ and the integrability condition makes it a genuine [[complex structure]].

* a $Sp(n) \hookrightarrow GL(2n)$-[[G-structure|structure]] is an _[[almost symplectic structure]]_ and the integrability condition makes it a genuine [[symplectic structure]].

## Properties

### Existence and torsion

The [[obstruction]] for a $G$-structure to be integrable is its [[torsion of a G-structure]].

## References

* {#Sternberg64} [[Shlomo Sternberg]], chapter VII of _Lectures on differential geometry_, Prentice-Hall (1964)

* {#Guillemin65} [[Victor Guillemin]], _The integrability problem for $G$-structures, Trans. Amer. Math. Soc. 116 (1965), 544&#8211;560. ([JSTOR](http://www.jstor.org/stable/1994134))

* {#Alekseevskii} D. V: Alekseevskii, _$G$-structure on a manifold_ in M. Hazewinkel (ed.) _Encyclopedia of Mathematics, Volume 4_


Discussion with an eye towards [[torsion constraints in supergravity]] is in

* {#Lott90} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_, Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

Discussion with an eye towards [[special holonomy]] is in

* {#Joyce00} [[Dominic Joyce]], _Compact manifolds with special holonomy_, Oxford University Press 2000

See also the references at _[[torsion of a Cartan connection]]_ and at _[[torsion constraints in supergravity]]_.

[[!redirects integrability of G-structures]]

[[!redirects integrable G-structure]]
[[!redirects integrable G-structures]]

[[!redirects integrable G-stucture]]
[[!redirects integrable G-stuctures]]
