This entry is about the notion of spectrum in [[stable homotopy theory]]. For other uses of the term ''spectrum'' see [[spectrum - disambiguation]].


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea 

A [[topological space|topological]] spectrum is an object in the universal [[stable (∞,1)-category]] $Sp(Top) \simeq Sp(\infty Grpd)$ that stabilizes" the [[(∞,1)-category]] [[Top]] or $\simeq$ [[∞-Grpd]] of [[topological spaces]] or [[∞-groupoids]]: the [[stable (∞,1)-category of spectra]].

Recall that the central characterization of a [[stable (∞,1)-category]] is that all objects $A$ have a [[delooping]] object $\mathbf{B}A$ that is written $\Sigma A$ in this context and called the _suspension_ of $A$. Thus a spectrum is like a [[topological space]] or [[∞-groupoid]] that may be [[delooping|delooped]] indefinitely.

### Connective spectra

In fact all ordinary [[topological spaces]] and [[∞-groupoids]] that have the property that all their [[deloopings]] exist give rise to special examples of spectra.  These are called the

* **[[connective spectrum|connective spectra]]**

* or **infinite [[loop spaces]]** 

* or [[group object in an (infinity,1)-category|grouplike]] [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[∞-groupoid]]s.

Connective spectra form a [[sub-(∞,1)-category]] of spectra

$$
  Top \stackrel{\supset}{\leftarrow} ConnectSp(Top) \hookrightarrow Sp(Top)
  \,.
$$

There are objects in $Sp(Top)$, though, that do not come from "naively" delooping a space infinitely many times.  These are the **non-connective spectra**.  For general spectra there is a notion of [[homotopy groups]] of negative degree. The connective ones are precisely those for which all negative degree [[homotopy groups]] vanish.

Connective spectra are well familiar in as far as they are in the image of the [[nerve]] operation of the [[Dold-Kan correspondence]]: this identifies [[∞-groupoids]] that are not only connective spectra but even have a _strict_ symmetric monoidal [[group]] structure with non-negatively graded [[chain complex]]es of abelian groups. 

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

The free stabilization of the [[(∞,1)-category]] of non-negatively graded chain complexes is simpy the [[stable (∞,1)-category]] of arbitrary chain complexes. There is a stabilized Dold-Kan correspondence (see at _[[module spectrum]]_ the section _[stable Dold-Kan correspondence](module+spectrum#StableDoldKanCorrespondence)_ ) that identifies these with special objects in $Sp(Top)$. 

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

## Definition 

There are many "models" for spectra, all of which present the same homotopy theory (and in fact, nearly all of them are [[Quillen equivalence|Quillen equivalent]] [[model category|model categories]]).  

### Spectra, CW-spectra

A simple first definition is to define a spectrum $\mathbf{E}$ to be a sequence of pointed spaces $(E_n)_{n\in\mathbb{N}}$ together with structure maps $\Sigma{}E_n\to{}E_{n+1}$ (where $\Sigma$ denotes the [[reduced suspension]]).

There are various conditions that can be put on the spaces $E_n$ and the structure maps, for example if the spaces are CW-complexes and the structure maps are inclusions of subcomplexes, the spectrum is called a **CW-spectrum**.

Without any condition, this is just called a **spectrum**, or sometimes a **pre-spectrum**.

### $\Omega$-spectra
 {#OmegaSpectrum}

If $\Omega$ denotes the [[loop space]] functor on the category of pointed spaces, we know that $\Sigma$ is left adjoint to $\Omega$.
In particular, given a spectrum $\mathbf{E}$, the structure maps can be transformed into maps $E_n\to\Omega{}E_{n+1}$.
If these maps are isomorphisms (depending on the situation it can be weak equivalences or homeomorphisms), then $\mathbf{E}$ is called an **$\Omega$-spectrum**.

The idea is that $E_0$ contains the information of $\mathbf{E}$ in dimensions $k\ge 0$, $E_1$ contains the information of $\mathbf{E}$ in $k\ge -1$ (but shifted up by one, so that it is modeled by the $\ge 0$ information in the space $E_1$), and so on.

$\Omega$-spectra are special cases of spectra, and are in fact the fibrant objects for some model structure on the category of spectra.
Given any spectrum $\mathbf{E}$, it is easy to transform it into an equivalent $\Omega$-spectrum $\mathbf{F}$ (a fibrant replacement of $\mathbf{E}$) : just take $F_n=\lim_{m\to\infty}\Omega^m E_{n+m}$ and use the fact that $\Omega$ commutes with the filtered colimits.

### Coordinate-free spectrum 

A definition of spectrum consisting of spaces indexed by index sets less "coordinatized" than the integers is a 

* [[coordinate-free spectrum]].

See there for details.

### Combinatorial definition

There might be a type of categorical structure related to a spectrum in the same way that $\infty$-categories are related to $\infty$-groupoids.  In other words, it would contain $k$-cells for all integers $k$, not necessarily invertible.  Some people have called this conjectural object a **$Z$-category**.   "Connective" $Z$-categories could perhaps then be identified with stably monoidal $\infty$-categories.

One realization of this kind of idea is the notion of [[combinatorial spectrum]].

### General context

One can define $\Phi$-symmetric $F$-spectra in a category $C$, where $\Phi$ is a [[graded monoid]] in the [[category]] of [[groups]] and $F : C \to C$ is a $\Phi$-symmetric [[endofunctor]] of $C$.  Here we follow [Ayoub](#Ayoub).

1.  Let $\Phi$ be a [[graded monoid]] in the category of [[groups]].  Explicitly this is the data of [[groups]] $\Phi_n$ for all $n \in \mathbf{N}$ with morphisms $\Phi_m \times \Phi_n \to \Phi_{m+n}$ for all $m,n \ge 0$ (subject to various axioms...).  $\Phi$ will usually be either $\Sigma = (\Sigma_n)_n$, the [[graded monoid]] of [[symmetric groups]], or $1 = (1_n)_n$, the [[graded monoid]] of [[trivial group]]s.

2.  A **$\Phi$-[[symmetric sequence]]** in $C$ is a [[sequence]] of objects $(X_n)_{n \ge 0}$ together with [[actions]] $a_n : \Phi_n \to \Aut_C(X_n)$.  We write $Seq(\Phi, C)$ for the category of $\Phi$-[[symmetric sequences]].  See [[symmetric sequence]] for details.

3.  A **$\Phi$-symmetric endofunctor** of $C$ is an [[endofunctor]] $F : C \to C$ together with [[actions]] $\Phi_n \to Aut(F^n)$.  Usually $F$ will be the functor $T \otimes_C -$ induced by [[tensor product]] with some object $T$.

4.  Let $F : C \to C$ be a $\Phi$-symmetric [[endofunctor]].  A **$\Phi$-symmetric $F$-spectrum** in $C$ is a $\Phi$-[[symmetric sequence]] $(X_n)_{n \in \mathbf{N}}$ together with **assembly morphisms**
  $$ \gamma_n : F(X_n) \to X_{n+1} $$
such that the composite morphism
  $$ F^m(X_n) \to F^{m-1}(X_{n+1}) \to \cdots \to X_{m+n} $$
is $(\Phi_m \times \Phi_n)$-[[equivariant]].  (Note that $\Phi_m$ acts on $F^m$ by the definition of [[symmetric endofunctor]], and $\Phi_n$ acts on $X_n$ by the definition of [[symmetric sequence]].)  A morphism of $\Phi$-symmetric $T$-spectra $X = (X_n)_n \to Y = (Y_n)_n$ is a morphism of $\Phi$-[[symmetric sequences]] making the obvious [[diagrams]] [[commutative diagram|commute]].  We write $Spect^{\Phi}_F(C)$ for the category of $\Phi$-symmetric $F$-spectra in $C$.

5.  When $\Phi = \Sigma$, the [[graded monoid]] of [[symmetric groups]], $\Sigma$-symmetric $F$-spectra are called simply **symmetric $F$-spectra**.  When $\Phi = 1$, $1$-symmetric $F$-spectra are called simply **nonsymmetric $F$-spectra**.  When the endofunctor $F$ is given by $T \otimes -$ for some object $T \in C$, $F$-spectra are called $T$-spectra.

6.  Consider the [[evaluation]] functor
  $$ Ev^n : Spect_F^{\Phi}(C) \to C $$
which "evaluates" a symmetric spectrum at its $n$th component.  Assuming that $C$ admits appropriate [[colimits]] and $F$ commutes with them, $Ev^n$ admits a left adjoint
  $$ Sus^n : C \to \Spect_F^\Phi(C) $$
called the $n$th [[suspension]] functor.

7.  Let $T \in C$ be an object and consider the $\Sigma$-[[symmetric sequence]] $Sym(T)$ whose $n$th component is $Sym(T)_n = T^{\otimes n}$ (with the [[actions]] of $\Sigma_n$ by permuting the $n$ factors).

8.  **Proposition.**  $Sym(T)$ is a [[commutative]] [[ring object]] in the [[symmetric monoidal category]] $Seq(\Sigma, C)$.

9.  By the previous proposition there is a [[symmetric monoidal structure]] on $Mod_\ell(Sym(T))$ where $X \otimes Y$ is defined as the [[coequalizer]] of the diagram
  $$ X \otimes Sym(T) \otimes Y \rightrightarrows X \otimes Y. $$

10.  Note that one has a tautological [[equivalence of categories]]
  $$ \Spect^\Sigma_T(C) \stackrel{\sim}{\longrightarrow} \Mod_\ell(Sym(T)). $$
In particular one gets a [[symmetric monoidal structure]] on $Spect^\Sigma_T(C)$.

11.  **Proposition.** One has
  $$ Sus^p_T(X) \otimes Sus^q_T(Y) \simeq Sus^{p+q}_T(X \otimes Y) $$
for all $X,Y \in C$.  In particular, $Sus = Sus^0 : C \to \Spect^\Sigma_T(C)$ is a [[symmetric monoidal functor]].

## Examples 

* [[suspension spectrum]]

* [[sphere spectrum]]

* [[Eilenberg-MacLane spectrum]]

* [[K-theory spectrum]]

* [[elliptic spectrum]]

* [[tmf]]

* [[Thom spectrum]], [[complex cobordism spectrum]]


## Properties

### Stabilization

In direct analogy to how topological spaces form the archetypical example, [[Top]], of an [[(∞,1)-category]], spectra form the archetypical example $Sp(Top)$ of a [[stable (∞,1)-category]]. In fact, there is a general procedure for turning any [[pointed category|pointed]] [[(∞,1)-category]] $C$ into a stable $(\infty,1)$-category $Sp(C)$, and doing this to the category $Top_*$ of [[pointed object|pointed]] spaces yields $Sp(Top)$.

### Symmetric monoidal structure

* [[smash product of spectra]]

* [[symmetric monoidal smash product of spectra]]

### Closed structure

* [[mapping spectrum]]

### Model category structure

* [[model structure on spectra]]

## Related concepts

* [[sheaf of spectra]], [[parametrized spectrum]]

* [[ring spectrum]], [[algebra spectrum]], [[module spectrum]]

* [[zero spectrum]]

* [[finite spectrum]]

* [[p-local spectrum]]

* [[Bousfield localization of spectra]]

* [[motivic spectrum]]


[[!include k-monoidal table]]

## References

A general treatment is in the last chapter of

* [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique, I_. Ast&#233;risque, Vol. 314 (2008). Soci&#233;t&#233; Math&#233;matique de France. ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/THESE.PDF))
{#Ayoub}

Surveys include

* A. Elmendorf, I. Kriz, [[Peter May|P. May]], _Modern foundations for stable homotopy theory_, [pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf)
* [[John Greenlees]], _Spectra for commutative algebraists_, [arXiv:math/0609452](http://arxiv.org/abs/math/0609452)
* [[Stefan Schwede]], _An untitled book project
about symmetric spectra_, a book in progress, [dvi](http://www.math.uni-bonn.de/~schwede/SymSpec.dvi), [pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf)

* [[Robert Thomason]], _Symmetric Monoidal Categories Model All Connective Spectra_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.37.8193))

* [[John Adams]], _Infinite loop spaces_

[[!redirects spectra]]
[[!redirects prespectrum]]
[[!redirects prespectra]]
[[!redirects pre-spectrum]]
[[!redirects pre-spectra]]