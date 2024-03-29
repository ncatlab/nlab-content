
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

Every [[(∞,1)-category]] $\mathcal{C}$ with [[finite (∞,1)-limits]] has a [[stabilization]] to a [[stable (∞,1)-category]] $Stab(\mathcal{C})$. This stabilization may be defined by abstract properties, but it may also be constructed explicitly as the category of _spectrum objects_ in $\mathcal{C}$.

In the special case that $\mathcal{C} = $ [[∞Grpd]] $\simeq L_{whe}$[[Top]], a spectrum object in $\mathcal{C}$ is a [[spectrum]] in the traditional sense. There is an evident generalization of the traditional notion of [[Omega-spectrum]] from [[Top]] to any $(\infty,1)$-category $\mathcal{C}$ with [[finite (∞,1)-limits]]: a spectrum object $X_\bullet$ is essentially a list of [[pointed objects]] $X_i$ together with [[equivalence in an (∞,1)-category|equivalences]] $X_i \to \Omega X_{i+1}$, from every object in the list to the [[loop space object]] of its successor. 

## Definition

### Via $\Omega$-spectrum objects

+-- {: .num_defn}
###### Definition

For $\mathcal{C}$ an [[(∞,1)-category]], a **prespectrum object**  of $\mathcal{C}$ is 

* a $(\infty,1)$-functor $X : \mathbb{Z} \times \mathbb{Z} \to \mathcal{C}$

* such that for all integers $i \neq j$ we have $X(i,j) = 0$ a [[zero object]] of $\mathcal{C}$

Notice that this definition is highly redundant. The point is that writing $X[n] \coloneqq X(n,n)$ a spectrum object is for all $n \in \mathbb{Z}$ a (homotopy) [[commuting diagram]]

$$
  \array{
    X[n] &\to& 0
    \\
    \downarrow && \downarrow
    \\
    0 &\to& X[n+1]
  }
    \,.
$$

Recalling that in an [[(infinity,1)-category]] with [[zero object]]

* $\Omega X[n+1]$ denotes the pullback of such a diagram;

* $\Sigma X[n]$ denotes the pushout of such a diagram

this induces maps

$$
  \alpha_n : \Sigma X[n] \to X[n+1]
$$

$$
  \beta_{n+1} : X[n] \to \Omega X[n+1]
  \,.
$$

A prespectrum object is

* a **spectrum object** if $\beta_m$ is an equivalence for all $m \in \mathbb{Z}$ (a __spectrum below $n$__, if $\beta_m$ is an equivalence for all $m \leq n$);

* a **suspension spectrum** if $\alpha_m$ is an equivalence for all $m \in \mathbb{Z}$ (a __suspension spectrum above $n$__, if $\alpha_m$ is an equivalence for all $m \geq n$).

=--

([StabCat](#StabCat))

One writes

* $Sp(\mathcal{C})$ for the [[full sub-(∞,1)-category]] of $Fun(\mathbb{Z} \times \mathbb{Z},C)$ on spectrum objects in $C$;

* $Stab(\mathcal{C}) \coloneqq Sp(\mathcal{C}_*)$ -- the **stabilization of $C$** for the $(\infty,1)$-category of spectrum objects in the $(\infty,1)$-category $C_*$ of [[pointed object]]s of $\mathcal{C}$.

### Via excisive functors
 {#ViaExcisiveFunctors}

Write $\infty Grpd_{fin}$ for the [[(∞,1)-category]] of [[finite homotopy types]], hence those freely generated by [[finite (∞,1)-colimits]] from the point. Write $\infty Grpd_{fin}^{\ast/}$ for the [[pointed object|pointed]] finite homotopy types.


+-- {: .num_defn}
###### Definition

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-limits]]. Then a **spectrum object** in $\mathcal{C}$ is a reduced (i.e. [[terminal object in an (infinity,1)-category|terminal object]]-preserving) [[excisive (∞,1)-functor]] of the form

$$
  \infty Grpd_{fin}^{\ast/} \longrightarrow \mathcal{C}
  \,.
$$

=--

([HigherAlg, def. 1.4.2.8 and around p. 823](#HigherAlg)).


+-- {: .num_remark}
###### Remark

This generalizes for instance to [[G-spectra]] ([Blumberg 05](#Blumberg05)).

=--

### In an ordinary category

One can define $\Phi$-symmetric $F$-spectra in a category $C$, where $\Phi$ is a [[graded monoid]] in the [[category]] of [[groups]] and $F : C \to C$ is a $\Phi$-symmetric [[endofunctor]] of $C$.  Here we follow [Ayoub](#Ayoub).

(One recovers the classical case described at [[spectrum]] by taking $C$ to be the [[category]] of [[pointed spaces]], $\Phi$ to be the trivial [[graded monoid]], and $F$ to be the [[suspension functor]].)

Let $\Phi$ be a [[graded monoid]] in the category of [[groups]].  Write $Seq(\Phi, C)$ for the category of $\Phi$-[[symmetric sequences]].  Let $F : C \to C$ be a $\Phi$-[[symmetric endofunctor]] of $C$.  (Usually $F$ will be the functor $T \otimes_C -$ induced by [[tensor product]] with some object $T$.)

A **$\Phi$-symmetric $F$-spectrum** in $C$ is a $\Phi$-[[symmetric sequence]] $(X_n)_{n \in \mathbf{N}}$ together with **assembly morphisms**
  $$ \gamma_n : F(X_n) \to X_{n+1} $$
such that the composite morphism
  $$ F^m(X_n) \to F^{m-1}(X_{n+1}) \to \cdots \to X_{m+n} $$
is $(\Phi_m \times \Phi_n)$-[[equivariant]].  (Note that $\Phi_m$ acts on $F^m$ by the definition of [[symmetric endofunctor]], and $\Phi_n$ acts on $X_n$ by the definition of [[symmetric sequence]].)  A morphism of $\Phi$-symmetric $T$-spectra $X = (X_n)_n \to Y = (Y_n)_n$ is a morphism of $\Phi$-[[symmetric sequences]] making the obvious [[diagrams]] [[commutative diagram|commute]].  We write $Spect^{\Phi}_F(C)$ for the category of $\Phi$-symmetric $F$-spectra in $C$.

When $\Phi = \Sigma$, the [[graded monoid]] of [[symmetric groups]], $\Sigma$-symmetric $F$-spectra are called simply **symmetric $F$-spectra**.  When $\Phi = 1$, $1$-symmetric $F$-spectra are called simply **nonsymmetric $F$-spectra**.  When the endofunctor $F$ is given by $T \otimes -$ for some object $T \in C$, $F$-spectra are called $T$-spectra.

When $C$ is a [[symmetric monoidal category]], there is an induced [[symmetric monoidal structure on spectrum objects]].

When $C$ is a sufficiently nice [[model category]], there are induced [[model structures on spectrum objects]].

## Properties

### As a model for stabilization

If $C$ is a pointed $(\infty,1)$-category with finite [[limit in quasi-categories|limits]], then $Sp(C)$ is a [[stable (infinity,1)-category]].

### Reflection into pre-spectrum objects

For $\mathcal{C}$ an [[(∞,1)-category]] with [[(∞,1)-pullbacks]] and [[(∞,1)-colimits]], then the inclusion of spectrum objects into prespectum objects 
should be a [[exact (∞,1)-functor|left exact]] [[reflective sub-(∞,1)-category]] inclusion ([Joyal 08, section 35](#Joyal08)).

$$
  Spec(\mathcal{C})
  \stackrel{\overset{lex}{\leftarrow}}{\hookrightarrow}
  PreSpec(\mathcal{C})
  \,.
$$

This implies in particular that the [[tangent (∞,1)-category]] of an [[(∞,1)-topos]]
is itself again an [[(∞,1)-topos]] ([Joyal 08, section 35.5](#Joyal08)), see at _[tangent (∞,1)-category -- Tangent (∞,1)-topos](tangent+%28infinity%2C1%29-category#TangentTopos)_ .

## Examples

* For $C = Top$, $Stab(C)$ is the $(\infty,1)$-category version of the classical stable homotopy category of spaces: the [[stable (infinity,1)-category of spectra]].

* In the [[equivariant homotopy theory]] of [[G-spaces]] a spectrum object is a _[[spectrum with G-action]]_.

* see also at _[[motivic spectrum]]_

## Related concepts

[[!include k-monoidal table]]

* [[stable homotopy type]]

* [[cospectrum]]

## References

Discussion in terms of [[stable (infinity,1)-categories]] is in 

* {#StabCat} [[Jacob Lurie]], section 8 of _[[Stable Infinity-Categories]]_
  
* {#HigherAlg} [[Jacob Lurie]], section 1.4.2 _[[Higher Algebra]]_

* {#Joyal08} [[André Joyal]], section 35  _Notes on Logoi_, 2008 ([pdf](http://www.math.uchicago.edu/~may/IMA/JOYAL/Joyal.pdf))

Discussion of [[model structure on spectra|model structures for spectrum objects]] includes

* {#Hovey00} [[Mark Hovey]], _Spectra and symmetric spectra in general model categories_ ([arXiv:0004051](http://arxiv.org/abs/math/0004051))
 

* [[Bjørn Ian Dundas]], [[Oliver Röndigs]], [[Paul Arne Østvær]], _Enriched functors and stable homotopy theory_,  Doc. Math., 8:409&#8211;488, 2003 ([EuDML](https://eudml.org/doc/123650))

  
A detailed treatment of the 1-categorical case is in the last chapter of

* {#Ayoub} [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique, I_. Ast&#233;risque, Vol. 314 (2008). Soci&#233;t&#233; Math&#233;matique de France. ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/THESE.PDF))


Generalization to [[G-spectra]] is in 

* {#Blumberg05} [[Andrew Blumberg]], _Continuous functors as a model for the equivariant stable homotopy category_ ([arXiv:math.AT/0505512](http://arxiv.org/abs/math.AT/0505512))




[[!redirects spectrum objects]]

[[!redirects prespectrum object]]
[[!redirects prespectrum objects]]

[[!redirects pre-spectrum object]]
[[!redirects pre-spectrum objects]]