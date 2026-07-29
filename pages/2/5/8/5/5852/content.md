
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


\tableofcontents


## Statement

\begin{theorem}\label{MaschkeTheorem}
**(Maschke's theorem)**
Given a [[finite group]] $G$ and a [[field]] $k$, then the following equivalent statements hold iff the [[characteristic]] of $k$ does not divide [[order of a group|order]] ${\vert G \vert}$:

1. every $G$-[[linear representation]] is [[completely reducible representation|completely reducible]] in that it is a [[direct sum]] of [[irreducible representations]],
   > (this is, in modern paraphrase, the statement in the title of [Maschke 1899](#Maschke1899))

2. the [[group algebra]] $k[G]$ is [[semisimple algebra|semisimple]] 

\end{theorem}

If the [[ground ring|base]] $k$ is just a [[commutative unital ring]], then there is the following statement:

\begin{theorem}
\label{MaschkeOverRings}
If ${|G|}\cdot 1_k$ is invertible in $k$, then an [[exact sequence]] of $k[G]$-[[modules]] [[split exact sequence|splits]] iff it splits after applying the [[forgetful functor]] from $k[G]$-modules to $k$-modules (and the splitting in ${}_{k[G]}Mod$ can be [[functor|functorially]] constructed from the splitting in ${}_{k}Mod$).
\end{theorem}


If $k$ is a [[field]], it follows that $k[G]$ is [[semisimple algebra|semisimple]], so that Thm. \ref{MaschkeOverRings} can be understood as a generalization of Maschke's theorem \ref{MaschkeTheorem}. This is also one of the motivations for the concept of *[[separable functors]]*.

The importance of the classical Maschke's theorem is that much is known about the structure of [[semisimple rings]] (starting with, e.g., [[Wedderburn's theorem]]).

## Related entries

* [[separable functor]]

## Literature

Named after:

* H. Maschke: *Ueber den arithmetischen Charakter der Coefficienten der Substitutionen endlicher linearer Substitutionsgruppen*, Math. Ann. **50** (1898) 492--498 \[<a href="https://doi.org/10.1007/BF01444297">doi:10.1007/BF01444297</a>\] 

* {#Maschke1899} H. Maschke: *Beweis des Satzes, dass diejenigen endlichen linearen Substitutionsgruppen, in welchen einige durchgehends verschwindende Coefficienten auftreten, intransitiv sind*, Math. Ann. **52** (1899) 363--368 \[<a href="https://doi.org/10.1007/BF01476165">doi:10.1007/BF01476165</a>\]


Textbook accounts:

* {#Serre77} [[Jean-Pierre Serre]]; section 1, Thms. 1, 2 in: *Linear Representations of Finite Groups*, Graduate Texts in Mathematics **42**, Springer (1977) &lbrack;[doi:10.1007/978-1-4684-9458-7](https://doi.org/10.1007/978-1-4684-9458-7), [pdf](https://www.math.tau.ac.il/~borovoi/courses/ReprFG/Hatzagot.pdf)&rbrack;
  > (stated just over the complex numbers)


* David S. Dummit, Richard M. Foote; §8.1 Thm. 1 (p. 849) in:   *Introduction  to the Representation Theory of Finite Groups*, part VI of: *Abstract Algebra*, Wiley (2003) &lbrack;[ISBN:978-0-471-43334-7](https://www.wiley.com/en-us/Abstract+Algebra%2C+3rd+Edition-p-9780471433347), [pdf](https://rksmvv.ac.in/wp-content/uploads/2021/04/David_S_Dummit_Richard_M_Foote_Abstract_Algeb_230928_225848.pdf)&rbrack;

See also:

* Wikipedia, *[Maschke's theorem](http://en.wikipedia.org/wiki/Maschke%27s_theorem)*


[[!redirects Maschke theorem]]
[[!redirects Maschke's theorem]]
[[!redirects Maschke\'s theorem]]
[[!redirects Maschke's theorem]]
