
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **comonoid** (or __comonoid object__) in a [[monoidal category]] $\mathcal{M}$ is a [[monoid in a monoidal category|monoid object]] $C$ in the [[opposite category]] $\mathcal{M}^{op}$ (which canonically becomes a monoidal category via the same [[tensor product]] operation as in $\mathcal{M}$).

With the usual definition of [[monoids]] as having a [[unit]], this means that a comonoid $C$ is equipped with a *counit*, which in [[string diagram]]-notation for $\mathcal{M}$ is of this form:

\begin{tikzcd}[row sep=15pt]
  C
  \ar[d, phantom, "\multimap"{rotate=-90, scale=1.8}, "{\scalebox{.7}{co-unit}}"{xshift=16pt, yshift=6pt}]
  \\
  {}
\end{tikzcd}


One speaks of a **unital comonoid** (or __unital comonoid object__; [[internalization|internal to]] [[Vect]] also called an *[[augmented algebra|augmented]] [[coalgebra]]*) if $C$ is in addition equipped with a morphism $\eta \colon I \rightarrow C$ 

\begin{tikzcd}[row sep=15pt]
  {}
  \ar[d, phantom, "\multimap"{rotate=90,, scale=1.8}, "{\scalebox{.7}{unit}}"{xshift=10pt, yshift=-4pt}]
  \\
  C
\end{tikzcd}

which verifies the properties that the [[unit]] would verify if $C$ was a [[bimonoid]], ie. in [[string diagrams]]:

<img src="/nlab/files/unital-comonoid.png"/>





## Examples

For example, a comonoid in [[Vect]] (with its usual [[tensor product]]) is called a [[coalgebra]].  Every set can be made into a comonoid in [[Set]] (with the [[cartesian product]]) in a unique way.  More generally, every object in a [[cartesian monoidal category]] can be made into a comonoid in a unique way.


## Related concepts

* [[coalgebra]]

* [[co-associativity]]

* [[co-unitality]]

[[!redirects comonoid]]
[[!redirects comonoids]]
[[!redirects comonoid object]]
[[!redirects comonoid objects]]

[[!redirects co-monoid]]
[[!redirects co-monoids]]