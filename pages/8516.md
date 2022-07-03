
#Contents#
* table of contents
{:toc}

## Idea

>Il s’agit là d’une question qu’un arithméticien ne peut guère manquer de se poser; on n’aperçoit d’ailleurs aucun motif sérieux de parier pour ou contre. Peut-être dira-t-on que l’existence d’une infinité de solutions rationnelles pour une équation $f(x,y)=0$, en l’absence d’une raison algébrique qui la justifie, est infiniment peu probable. Mais ce n’est pas un argument.... (André Weil, [Commentaire 1979](#Weil79))

The _Mordell conjecture_ or _Falting's theorem_ is a statement about the [[finite set|finiteness]] of [[rational points]] on an [[algebraic curve]] over a [[number field]] of [[genus]] $g \gt 1$.

Its statement motivated the introduction of [[anabelian geometry]] ([Grothendieck](#Grothendieck)).

The Mordell conjecture completed a classification of the behavior of rational points on curves over $\mathbb{Q}$. For genus 0 one has no points, or something isomorphic to $\mathbb{P}^1$ and hence infinitely many. For genus 1, the [[Mordell-Weil theorem]] tells us it is either empty or a finitely generated [[abelian group]] (sometimes finite, sometimes infinite). To finish off this type of classification the Mordell conjecture shows that only the finite case can occur for higher genus.

This result also implies many non-trivial results. For example, fix a finite set of primes $S$, a dimension $n$, and a [[polarization degree]] $d$. There are only finitely many [[abelian varieties]] of dimension $n$ and polarization degree $d$ with [[bad reduction]] inside $S$. This result is so interesting that a whole industry popped up asking what other varieties this type of behavior occurs for. It seems to work for [[K3]]s.

## Sketch of Faltings' proof

We follow the seminar notes [BhattSnowden](#BhattSnowden).

The proof proceeds along the following steps:

1. Using _Parshin's trick_ and passing to the [[Jacobian variety]] to reduce the Mordell conjecture to the _Shafarevich conjecture_ that there are only finitely many [[abelian varieties]] of dimension $g$ and polarization degree $d$ with good reduction outside a fixed set of places $S$.

2. Using the semisimplicity of the [[Tate module]] and the _isogeny theorem_
$$Hom_{K}(A,B)\otimes\mathbb{Z}_{\ell}\cong Hom_{G_{K}}(T_{\ell}(A),T_{\ell}(B))$$
for abelian varieties $A$ and $B$ over $K$, to prove the Shafarevich conjecture. The idea is that there are only finitely many possibilities for the Tate module, which shows finiteness up to isogeny; a height argument then shows finiteness up to isomorphism.

3. Showing that the semisimplicity of the Tate module and the isogeny theorem will follow if there are only finitely many abelian varieties (up to isomorphism) isogenous to a fixed abelian variety $A$ (follows a strategy originally used by Tate to prove the analogous result over finite fields).

4. Showing that there are only finitely many abelian varieties (up to isomorphism) isogenous to a fixed abelian variety $A$ by relating the Faltings height to the moduli-theoretic height (for which there are only finitely many points of bounded height) using [[Arakelov theory]] then studying how the Faltings height changes under isogeny. This makes use of the Hodge-Tate decomposition from [[p-adic Hodge theory]].

## Other proofs

Other proofs of the Mordell conjecture using different methods have been given by [[Paul Vojta]] ([Vojta91](#Vojta91)) and [[Enrico Bombieri]] ([Bombieri90](#Bombieri90)). Recently another proof involving period mappings together with o-minimality methods was given by [[Brian Lawrence]] and [[Akshay Venkatesh]] ([LawrenceVenkatesh18](#LawrenceVenkatesh18)).

## Effective Mordell conjecture

Faltings' proof of the Mordell conjecture determines the finiteness of the rational points but it does not find the set of rational points. The latter problem is also known as the _effective Mordell conjecture_. An approach towards this has been proposed by [[Minhyong Kim]] and is related to his proposed [[arithmetic gauge theory]] (see also [Balakrishnan19]({#Balakrishnan19}) for a survey). 

## Relation to other statements

The Mordell conjecture is implied by the [[abc conjecture]]. (See there.)

The Mordell conjecture implies [[Tate's isogeny theorem]].

See also [[Vojta's conjecture]].

## References

The Mordell conjecture originates in 

* [[Louis Mordell]],  _On the rational solutions of the indeterminate equation of the third and fourth degrees_, Proc. Cambridge Philos. Soc. 21: 179&#8211;192 (1922)

It was proven in

* {#Faltings83} [[Gerd Faltings]], *Endlichkeitssätze für abelsche Varietäten über Zahlkörpern*, Inventiones Mathematicae **73** 3 (1983) 349-366  &lbrack;[doi:10.1007/BF01388432](https://doi.org/10.1007/BF01388432)&rbrack;
 

Seminar notes on Faltings' proof:

* {#BhattSnowden} [[Bhargav Bhatt]], [[Andrew Snowden]] (org.): _Faltings' proof of the Mordell conjecture_ (seminar notes, 2016) &lbrack;[pdf](https://web.math.princeton.edu/~takumim/Mordell.pdf), [[BhattSnowden-FaltingsProofofMordell.pdf:file]]&rbrack;

Other proofs after Faltings:

* {#Vojta91} [[Paul Vojta]], 1991, _Siegel's theorem in the compact case_, Ann. of Math. 133 (3): 509–548.

* {#Bombieri90} [[Enrico Bombieri]], _The Mordell conjecture revisited_, _Annali della Scuola Normale Superiore di Pisa - Classe di Scienze_,  S&#233;r. 4, 17 no. 4 (1990), p. 615-640 &lbrack;[numdam:ASNSP_1990_4_17_4_615_0](http://www.numdam.org/item?id=ASNSP_1990_4_17_4_615_0)&rbrack;

* {#LawrenceVenkatesh18} [[Brian Lawrence]], [[Akshay Venkatesh]]: _Diophantine problems and $p$-adic period mappings_,  Invent. math. **221** (2020) 893–999  &lbrack;[arxiv:1807.02721](https://arxiv.org/abs/1807.02721), [doi:10.1007/s00222-020-00966-7](https://doi.org/10.1007/s00222-020-00966-7)&rbrack;

Reviews:

* [[Spencer Bloch]], _The Proof of the Mordell Conjecture_, Math. Int. **6** 2 (1984) 41-47 &lbrack;[pdf](https://link.springer.com/content/pdf/10.1007/BF03024155.pdf), [doi:10.1007/BF03024155](https://doi.org/10.1007/BF03024155)&rbrack;

* [[Barry Mazur]], _Abelian varieties and the Mordell-Lang conjecture_ ([pdf](http://library.msri.org/books/Book39/files/mazur.pdf))

A survey of two approaches to the effective Mordell conjecture:

* {#Balakrishnan19} [[Jennifer Balakrishnan]],  A. J. Best, F. Bianchi, [[Brian Lawrence]], J. S. Müller, N. Triantafillou, J. Vonk: *Two recent $p$-adic approaches to the (effective) Mordell conjecture*, in: *Arithmetic L-Functions and Differential Geometric Methods* Progress in Mathematics **338** Birkhäuser (2021) &lbrack;[arxiv:1910.12755](https://arxiv.org/abs/1910.12755), [doi:10.1007/978-3-030-65203-6_2]( https://doi.org/10.1007/978-3-030-65203-6_2)&rbrack;

Encyclopedia entries:

* [[Encyclopedia of Mathematics]], _[Mordell conjecture](http://www.encyclopediaofmath.org/index.php/Mordell_conjecture)_

* Wikipedia, _[Faltings' theorem](http://en.wikipedia.org/wiki/Mordell_conjecture#CITEREFMordell1922)_

The relation to [[anabelian geometry]] originates in

* [[Alexandre Grothendieck]], letter to [[Faltings]] (1983) ([pdf](http://www.math.jussieu.fr/~leila/grothendieckcircle/GtoF.pdf))
 {#Grothendieck}

The Weil quote stems from

* {#Weil79}[[André Weil]], _Œuvres Scientifiques - Collected Papers Volume III_, Springer Heidelberg 1979. (p.454)

[[!redirects Mordell's conjecture]]

[[!redirects Mordell Conjecture]]


