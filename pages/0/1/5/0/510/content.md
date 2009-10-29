<div class="rightHandSide toc">
[[!include stable homotopy theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

A [[topological space|topological]] spectrum is an object in the universal [[stable (∞,1)-category]] $Sp(Top) \simeq Sp(\infty Grpd)$ that "stabilizes" the [[(∞,1)-category]] [[Top]] or $\simeq$ [[∞-Grpd]] of [[topological spaces]] or [[∞-groupoids]]: the [[stable (∞,1)-category of spectra]].

Recall that the central characterization of a [[stable (∞,1)-category]] is that all objects $A$ have a [[delooping]] object $\mathbf{B}A$ that is written $\Sigma A$ in this context and called the _suspension_ of $A$. Thus a spectrum is like a [[topological space]] or [[∞-groupoid]] that may be [[delooping|delooped]] indefinitely.

In fact all ordinary [[topological spaces]] and [[∞-groupoids]] that have the property that all their [[deloopings]] exist give rise to special examples of spectra.  These are called the

* **connective spectra**

* or **infinite [[loop spaces]]** 

* or [[groupal n-groupoid|grouplike]] [[k-tuply monoidal n-category|stably monoidal]] $\infty$-[[∞-groupoid|groupoids]]

* or [[symmetric monoidal (∞,1)-category|symmetic monoidal ∞-groupoids]].

Connective spectra form a sub [[(∞,1)-category]] of spectra

$$
  Top \stackrel{\supset}{\leftarrow} ConnectSp(Top) \hookrightarrow Sp(Top)
  \,.
$$

There are objects in $Sp(Top)$, though, that do not come from "naively" delooping a space infinitely many times.  These are the **non-connective spectra**.  For general spectra there is a notion of [[homotopy groups]] of negative degree. The connective ones are precisely those for which all negative degree [[homotopy groups]] vanish.

Non-connective spectra are well familiar in as far as they are in the image of the [[nerve]] operation of the [[Dold-Kan correspondence]]: this identifies [[∞-groupoids]] that are not only connective spectra but even have a _strict_ symmetric monoidal [[group]] structure with non-negatively graded [[chain complex]]es of abelian groups. 

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

The free stabilization of the [[(∞,1)-category]] of non-negatively graded chain complexes is simpy the [[stable (∞,1)-category]] of arbitrary chain complexes. There is a stabilized Dold-Kan correspondence that identifies these with special objects in $Sp(Top)$. 

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

# Definition #

There are many "models" for spectra, all of which present the same homotopy theory (and in fact, nearly all of them are [[Quillen equivalence|Quillen equivalent]] [[model category|model categories]]).  

## $\Omega$-spectra #

One fairly simple, and quite useful, approach is to define a spectrum $E$ to be a [[sequence]] of [[pointed object|based]] spaces $E_n$, for all natural numbers $n$, together with isomorphisms $E_n \cong \Omega E_{n+1}$, where $\Omega$ denotes the based [[loop space]].  The idea is that $E_0$ contains the information of $E$ in dimensions $k\ge 0$, $E_1$ contains the information of $E$ in $k\ge -1$ (but shifted up by one, so that it is modeled by the $\ge 0$ information in the space $E_1$), and so on.

This is called an **$\Omega$-spectrum**.

## Coordinate-free spectrum ##

A definition of spectrum consisting of spaces indexed by index sets less "coordinatized" than the integers is a 

* [[coordinate-free spectrum]].

See there for details.

## combinatorial definition ##

There might be a type of categorical structure related to a spectrum in the same way that $\infty$-categories are related to $\infty$-groupoids.  In other words, it would contain $k$-cells for all integers $k$, not necessarily invertible.  Some people have called this conjectural object a **$Z$-category**.   "Connective" $Z$-categories could perhaps then be identified with stably monoidal $\infty$-categories.

One realization of this kind of idea is the notion of [[combinatorial spectrum]].


#Remarks#

* In direct analogy to how topological spaces form the archetypical example, [[Top]], of an [[(∞,1)-category]], spectra form the archetypical example $Sp(Top)$ of a [[stable (∞,1)-category]]. In fact, there is a general procedure for turning any [[pointed category|pointed]] [[(∞,1)-category]] $C$ into a stable $(\infty,1)$-category $Sp(C)$, and doing this to the category $Top_*$ of [[pointed object|pointed]] spaces yields $Sp(Top)$.

#Examples of spectra#

* [[Eilenberg-MacLane spectrum]]

* [[K-theory spectrum]]

* [[tmf]]



[[!redirects spectra]]