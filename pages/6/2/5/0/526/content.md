
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
 {#Examples}

\begin{example}
**(coassociative coalgebras)**
A comonoid object in [[VectorSpaces]] (with its usual [[tensor product of vector spaces]]) is called a *[[coalgebra]]*. 

(Beware though that the term "coalgebra" is overused in many ways, for instance in *[[coalgebras for endofunctor]]*. To be more specific to the linear-algebraic context one can say *[[coassociative coalgebra]]*.)
\end{example}

\begin{example}\label{InACartesianMonoidalCategory}
**(cartesian comonoids)**
\linebreak
Every [[set]] carries a *unique* [[structure]] of a comonoid in the category of [[Sets]] with respect to the usual [[cartesian product]].  

Generally, every object $X \,\in\, \mathcal{C}$ in a [[cartesian monoidal category]] $(\mathcal{C}, \ast, \times)$ becomes (see also [there](cartesian+monoidal+category#ComonoidObjects)) a ([[cocommutative coalgebra|cocommutative]]) comonoid by taking the

* counit to be the [[terminal object|terminal morphism]] $ X \xrightarrow{\exists !} \ast$

* coproduct to be the [[diagonal morphism]] $diag_X \,\colon\, X \to X \times X$. 

The analogous statement remains true for [[cartesian monoidal (infinity,1)-categories]] (see [there](https://ncatlab.org/nlab/show/cartesian+monoidal+infinity,1-category#CoalgebraObjects)).
\end{example}

Obvious as Exp. \ref{InACartesianMonoidalCategory} may be, it plays a somewhat profound role in various contexts: 

\begin{example}
**([[suspension spectra|suspension]] [[coring spectra]])**
\linebreak
In the case of [[topological spaces]] or other models of  classical [[homotopy types]], and using that the [[suspension spectrum]]-construction is a [[strong monoidal functor]], Exp. \ref{InACartesianMonoidalCategory} implies the remarkable fact that [[suspension spectra]] carry [[coring spectrum]]-[[structure]] via [smash-monoidal diagonals](suspension+spectrum#SmashMonoidalDiagonals).

\end{example}



## Related concepts

* [[cocategory]]

* [[coalgebra]]

* [[co-associativity]]

* [[co-unitality]]

* [[gs-monoidal category]]

[[!include reader-writer (co)monads -- table]]


[[!redirects comonoid]]
[[!redirects comonoids]]
[[!redirects comonoid object]]
[[!redirects comonoid objects]]

[[!redirects co-monoid]]
[[!redirects co-monoids]]