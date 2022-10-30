+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
#### Stable Homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The collection of [[spectra]] form an [[(∞,1)-category]] $Sp(\infty Grpd)$ which is in fact a [[stable (∞,1)-category]]. Indeed, it is the _[[universal property]]_ [[stabilization]] of the $(\infty,1)$-category [[∞Grpd]], equivalently of the [[simplicial localization]] of the category [[Top]] at the [[weak homotopy equivalences]].

$Sp(\infty Grpd)$ plays a role in [[stable homotopy theory]] analogous to the role played by the 1-[[category]] [[Ab]] of [[abelian groups]] in [[homological algebra]], or rather of the [[category of chain complexes]] $Ch_\bullet(Ab)$ of abelian groups.

## Definition

In the context of [[(infinity,1)-category|(∞,1)-categories]] a [[spectrum]] is a [[spectrum object]] in the [[(∞,1)-category]] $L_{whe} Top_*$ of pointed [[topological spaces]].

Recall that [[spectrum objects]] in the [[(infinity,1)-category]] $C$ form a [[stable (∞,1)-category]] $Sp(C)$.

The [[stable (∞,1)-category]] of [[spectrum object]]s in $L_{whe} Top_*$ is the **stable $(\infty,1)$-category of spectra**

$$
  Stab(L_{whe}Top) := Sp(L_{whe}Top_*)
  \,.
$$

## Properties

### Monoidal structure

* With the [[smash product of spectra]] $Sp(L_{whe}Top_*)$ becomes a [[symmetric monoidal (∞,1)-category]].

  * an [[algebra in an (infinity,1)-category|algebra object]] in $Sp(L_{whe}Top_*)$ with respect to this monoidal structure is an [[associative ring spectrum]];

  * a [[commutative algebra in an (infinity,1)-category|commutative algebra object]] in $Sp(L_{whe}Top_*)$ with respect to this monoidal structure is a [[commutative ring spectrum]];


### Prime spectrum and Morava K-theory

The [[prime spectrum of a monoidal stable (∞,1)-category]] for [[p-localization|p-local]] and [[finite spectra]] is labeled by the [[Morava K-theories]]. This is the content of the _[[thick subcategory theorem]]_.

### Model category presentation

There are several [[presentable (infinity,1)-category|presentations]] of the $(\infty,1)$-category of spectra by [[model categories of spectra]]. In particular there are [[symmetric smash product of spectra|symmetric]] [[monoidal model categories]] where the [[smash product of spectra]] is presented by an ordinary [[tensor product]], so that [[A-∞ rings]], [[E-∞ rings]] and [[∞-modules]] are presented by 1-categorical [[monoid objects]] and [[module objects]], respectively ("[[brave new algebra]]"). See at:

[[model structure on spectra]], [[symmetric monoidal smash product of spectra]]

* [[symmetric spectrum]], [[model structure on symmetric spectra]]

* [[orthogonal spectrum]], [[model structure on orthogonal spectra]]

* [[S-module]], [[model structure on S-modules]]



## References

the stable $(\infty,1)$-category of spectra is described in section 9 of 

* [[Jacob Lurie]], [[Stable Infinity-Categories]] .

Its monoidal structure is described in section 4.2

* [[Jacob Lurie]], [[higher algebra|Noncommutative algebra]].

That this is a symmetric monoidal structure is described in section  6 of

* [[Jacob Lurie]], [[higher algebra|Commutative algebra]].

[[!redirects stable (∞,1)-category of spectra]]

[[!redirects (∞,1)-category of spectra]]
[[!redirects (infinity,1)-category of spectra]]

[[!redirects symmetric monoidal (∞,1)-category of spectra]]
[[!redirects symmetric monoidal (infinity,1)-category of spectra]]