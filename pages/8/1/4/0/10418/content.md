
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

### In terms of patchwise $G$-structure

In ([Lott 90, page 4 of the exposition](#Lott90)) gives the following characterization of integrable $G$-structure, one that does not use differential forms.

Let $V$ be a linear local model space, e.g. a [[vector space]] or [[super vector space]]. Write $GL(V)$ for its [[general linear group]]. Consider a [[group]] [[homomorphism]] $G \longrightarrow GL(V)$.

Now fix a [[G-structure]] $\mathbf{c}_V$ on $V$ itself.

Then a [[G-structure]] $\mathbf{c}$ on a [[manifold]] $X$ modeled on $V$ (e.g. a [[smooth manifold]] or [[supermanifold]]) is called integrable if

1. there exists [[cover]] $\{U_i \hookrightarrow X\}$ by [[open subsets]]  $U_i \hookrightarrow V$;

1. such that the $G$-structure $\mathbf{c}$ on $X$ restricts on each patch to the default $G$-structure $\mathbf{c}_0$ on $V$:

   $$
     \mathbf{c}|_{U_i} \simeq \mathbf{c}_0|_{U_i}
     \,.
   $$

For instance if $G$-structure is modeled by $G$-subbundles $P$ of the [[frame bundle]] (as discussed at _[G-structure -- In terms of subbundles of the frame bundle](G-structure#InTermsOfSubbundlesOfTheFrameBundle)_ ), then it is integrable if each $P \hookrightarrow Fr(X)$ restricts on each patch to $P_0 \hookrightarrow Fr(V)$

$$
  \array{
     P_0|_{U_i} &\hookrightarrow& Fr(U_i)
     \\
     {}^{\mathllap{\simeq}}\downarrow && \downarrow
     \\
     P|_{U_i}
  }
$$


## Examples
For instance 

* a $GL(n,\mathbb{C}) \to GL(2n,\mathbb{R})$-[[G-structure|structure]] is an _[[almost complex structure]]_ and the integrability condition makes it a genuine [[complex structure]].

* a $Sp(n) \hookrightarrow GL(2n)$-[[G-structure|structure]] is an _[[almost symplectic structure]]_ and the integrability condition makes it a genuine [[symplectic structure]].

## Properties

### Existence and torsion

The [[obstruction]] for a $G$-structure to be integrable is its [[torsion of a G-structure]].

## References

* {#Guillemin65} [[Victor Guillemin]], _The integrability problem for $G$-structures, Trans. Amer. Math. Soc. 116 (1965), 544&#8211;560. ([JSTOR](http://www.jstor.org/stable/1994134))

Discussion with an eye towards [[torsion constraints in supergravity]] is in

* {#Lott90} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_, Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

Discussion with an eye towards [[special holonomy]] is in

* {#Joyce00} [[Dominic Joyce]], _Compact manifolds with special holonomy_, Oxford University Press 2000

See also the references at _[[torsion of a Cartan connection]]_ and at _[[torsion constraints in supergravity]]_.


