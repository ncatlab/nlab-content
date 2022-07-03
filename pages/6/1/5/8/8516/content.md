
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

4. Showing that there are only finitely many abelian varieties (up to isomorphism) isogenous to a fixed abelian variety $A$ by relating the Faltings height to the moduli-theoretic height (for which there are only finitely many points of bounded height) then studying how the Faltings height changes under isogeny. This makes use of the Hodge-Tate decomposition from [[p-adic Hodge theory]].

## Relation to other statements

The Mordell conjecture is implied by the [[abc conjecture]]. (See there.)

The Mordell conjecture implies [[Tate's isogeny theorem]].

See also [[Vojta's conjecture]].

## References

The Mordell conjecture originates in 

* [[Louis Mordell]],  _On the rational solutions of the indeterminate equation of the third and fourth degrees_, Proc. Cambridge Philos. Soc. 21: 179&#8211;192 (1922)

It was proven in

* [[Gerd Faltings]], _Endlichkeitss&#228;tze f&#252;r abelsche Variet&#228;ten &#252;ber Zahlk&#246;rpern_, Inventiones Mathematicae 73 (3): 349&#8211;366 (1983) doi:10.1007/BF01388432. 
 {#Faltings}

Seminar notes on Faltings' proof:

* {#BhattSnowden} [[Bhargav Bhatt]] and [[Andrew Snowden]] (organizers) _Faltings' proof of the Mordell conjecture_ (seminar notes) [pdf](https://web.math.princeton.edu/~takumim/Mordell.pdf)

Reviews include

* Spencer Bloch, _The Proof of the Mordell Conjecture_, Math. Int. **6** no.2 (1984) p.41-47.

* [[Barry Mazur]], _Abelian varieties and the Mordell-Lang conjecture_ ([pdf](http://library.msri.org/books/Book39/files/mazur.pdf))

* Enrico Bombieri, _The Mordell conjecture revisited_, _Annali della Scuola Normale Superiore di Pisa - Classe di Scienze_,  S&#233;r. 4, 17 no. 4 (1990), p. 615-640 ([Numdam](http://www.numdam.org/item?id=ASNSP_1990_4_17_4_615_0))

Encyclopedia entries are in

* Encyclopedia of Mathematics, _[Mordell conjecture](http://www.encyclopediaofmath.org/index.php/Mordell_conjecture)_

* Wikipedia, _[Faltings' theorem](http://en.wikipedia.org/wiki/Mordell_conjecture#CITEREFMordell1922)_

The relation to [[anabelian geometry]] originates in

* [[Alexandre Grothendieck]], letter to [[Faltings]] (1983) ([pdf](http://www.math.jussieu.fr/~leila/grothendieckcircle/GtoF.pdf))
 {#Grothendieck}

The Weil quote stems from

* {#Weil79}[[André Weil]], _Œuvres Scientifiques - Collected Papers Volume III_, Springer Heidelberg 1979. (p.454)

[[!redirects Mordell's conjecture]]

[[!redirects Mordell Conjecture]]


