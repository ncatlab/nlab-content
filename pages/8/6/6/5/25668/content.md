
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of *[[center]] of a [[monoid]]* has a [[horizontal categorification]] to a notion of *center of a category*.

## Definition
 
For $\mathcal{C}$ a [[category]], its *center* $Z(\mathcal{C})$ is defined to be the [[commutative monoid]] 

$$
  Z(\mathcal{C})
  \;\coloneqq\;
  [\mathcal{C},\mathcal{C}]\big(
    Id_\mathcal{C}
    ,\,
    Id_\mathcal{C}
  \big)
$$ 

of [[endomorphism|endo]]-[[natural transformation]] of the [[identity functor]] $Id_C \,\colon\, C \to C$, i.e. the [[endomorphism monoid]] of $Id_C$ in the [[functor category]] $[C,C]$.  

If $\mathcal{C}$ carries extra [[structure]] this may be inhereted by its center. Notably the center of an [[additive category]] is not just a [[commutative monoid]] but a [[commutative ring]]: the [[endomorphism ring]] of the [[identity functor]]. For more on this see at *[[center of an additive category]]*.

## Examples

\begin{example}
  For $A$ an ordinary monoid and $\mathbf{B}A$ it [[delooping]]-category, the ordinary [[center]] of $A$ is naturally identified with the category theoretic center of $\mathbf{B}A$.
\end{example}

\begin{proposition}
For a [[generator]] $G$ of a [[category]] $\mathcal{C}$ there is an embedding of $Z(\mathcal{C})$ into the monoid $Hom(G,G)$ given by $\eta\mapsto\eta _G$. In particular, if $Hom(G,G)$ or $Z(Hom(G,G))$ is trivial, as happens e.g. for $Set$ with $G=\ast$, then so is $Z(\mathcal{C})$. 
\end{proposition}
&lbrack;[Hoffmann (1975)](#Hoffmann75)&rbrack;

\begin{proposition}
For [[Cauchy completion|Cauchy complete]] $\mathcal{C}$ the [[idempotent]] elements of $Z(\mathcal{C})$ correspond precisely to the _quintessential localizations_ of $\mathcal{C}$.
\end{proposition} 
&lbrack;[Johnstone (1996)](#Johnstone96)&rbrack;

## Related concepts

* [[center]], [[center of a monoid]]

* [[center of an additive category]]

* [[Drinfeld center]]


## References

* {#Hoffmann75} [[Rudolf-E. Hoffmann]], *Über das Zentrum einer Kategorie*, Math. Nachr. **68** (1975) 299-306 &lbrack;[doi:10.1002/mana.19750680122](https://doi.org/10.1002/mana.19750680122)&rbrack;

* {#Johnstone96} [[Peter Johnstone]], _Remarks on Quintessential and Persistent Localizations_, TAC **2** 8 (1996) 90-99. &lbrack;[tac:2-08](http://www.tac.mta.ca/tac/volumes/1996/n8/2-08abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf)&rbrack;

See also:

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Center_(category_theory)">Center (category theory)</a>*

[[!redirects centers of categories]]

