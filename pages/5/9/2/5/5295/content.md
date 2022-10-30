
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Intuitionistic mathematics
* table of contents
{: toc}

## Idea

Intuitionistic mathematics is a variety of [[constructive mathematics]] done according to the principles accepted by [[L.E.J. Brouwer]] and his philosophy of intuitionism.


## Terminology

There are a variety of ways to use the term 'intuitionistic'.  We list them here, roughly from the most specific to the most general, and contrast (where appropriate) with the term 'constructive':

*  __Intuitionism__ is an early-20th-century [[philosophy of mathematics]] developed by Brouwer, according to which [[mathematics]] is a free creation of a mind, and valid results are about what that mind creates (rather than about an external reality, as in [[platonism]], or about nothing, as in [[formalism]]).  From this starting point, Brouwer developed a very controversial style of mathematics and even [[logic]], which he saw as derived from mathematics (rather than conversely, as in [[logicism]]).  Intuitionism is one particular philosophy of [[constructivism]].

*  __Intuitionistic mathematics__ is the mathematics that Brouwer came up with.  However, it\'s not necessary to accept Brouwer\'s philosophy to practise intuitionistic mathematics; conversely, one may accept Brouwer\'s philosophical starting place but not his conclusions about the resulting mathematics.  Intuitionistic mathematics is one particular variety of [[constructive mathematics]].

   One example of intuitionistic mathematics (which nicely shows that intuitionism is not a matter of "belief" but of subject) is [[computable mathematics]] (see for instance [Bauer 05, section 4.3.1](#Bauer05)).

*  __[[intuitionistic set theory|Intuitionistic set theory]]__ is a [[set theory]], generally proffered as a [[foundation of mathematics]], in which [[excluded middle]] fails but [[power sets]] are included (making it [[impredicative mathematics|impredicative]]).  In contrast, _constructive_ set theory has [[function sets]] but not power sets (making it [[weakly predicative mathematics|weakly predicative]]).  Neither of these actually captures the level of predicativity of intuitionistic mathematics.

*  __[[intuitionistic type theory|Intuitionistic type theory]]__ is a [[set theory]], generally proffered as a [[foundation of mathematics]], which is usually [[predicative mathematics|predicative]].  For purposes of comparing type theory to set theory, it might be nice if 'intuitionistic' and 'constructive' were distinguished for type theories as they are for set theories, but they aren\'t.  (Then again, there was never much sense in that distinction for set theories, or at least not for making it using that terminology.)

*  __[[Intuitionistic logic]]__ is the [[logic]] that intuitionistic mathematics, set theory, and type theory use, which lacks the principle of [[excluded middle]]; other forms of constructive mathematics also use intuitionistic logic, which is also known as _constructive logic_.


## Mathematical principles

Brouwer never accepted a complete axiomatisation of intuitionistic mathematics.  However, we can identify several principles, which may not (even historically) be complete.

*  In hindsight, we may say that inuitionistic mathematics is done in a [[pretopos]] identified as [[Set]].

*  We have the [[axiom of infinity]] and [[countable choice]], as in [[classical mathematics]].

*  We have the classically false principles of [[continuity principle|continuity]] and [[continuous choice]].

*  We have the [[fan theorem]] and [[bar theorem]], which are classically true but fail in [[Russian constructivism]].

*  There\'s also some stuff about [[choice sequence]]s that I don\'t really understand.

Although it\'s not enough to derive all of the above, much of the essence of intuitionistic mathematics, or at least intuitionistic [[analysis]], can be summarized in the theorem that every (set-theoretic) [[function]] from the [[unit interval]] to the [[real line]] is [[uniformly continuous map|uniformly continuous]].


## Feel

In intuitionistic mathematics, already [[set theory]] behaves a lot like [[topology]], a point stressed by [[Frank Waaldijk]] ([web](http://www.fwaaldijk.nl/mathematics.html)).

Although intuitionstic mathematics does not accept all [[function sets]] (much less [[power sets]]), it seems to allow for both [[induction|inductive]] and [[coinduction|coinductive]] structures; see [a Caf&#233; comment](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html#c020731).


## Related concepts

* [[constructive mathematics]]

* [[intuitionistic type theory]]

* [[realizability]]

## References
 {#References}

The roots of Brouwer's intuitionism are apparently in his PhD thesis

* [[L.E.J. Brouwer]], _Over de Grondslagen der Wiskunde, PhD thesis_, Universiteit
van Amsterdam, 1907.

Then an axiomatization of intuitionistic mathematics is given in

* [[Stephen Kleene]], R. E. Vesley, _The foundations of intuitionistic mathematics_,North-Holland (1965)

in terms of [[realizability]] (the [[Kleene-Vesley topos]]), and hence intuitionistic mathematics is shown to be consistent.

General reviews include

* Stanford Encyclopedia of Philosophy, _[Intuitionism in the Philosophy of Mathematics](http://plato.stanford.edu/entries/intuitionism/)
_
Reviews with further developments include for instance

* [[Frank Waaldijk]], _On the foundations of constructive mathematics -- especially to the theory of continuous functions_  ([pdf](http://www.fwaaldijk.nl/foundations+of+constructive+mathematics.pdf))

  (with a focus on [[constructive analysis]]).

For more see also the references at _[[constructive mathematics]]_.

That [[computable mathematics]] is an incarnation of intuitionistic mathematics is spelled out in the lecture notes

* {#Bauer05} [[Andrej Bauer]], around section 4,3.1 in _Realizability as connection between constructive and computable mathematics_, in T. Grubba, P. Hertling, H. Tsuiki, and [[Klaus Weihrauch]], (eds.) _CCA 2005 - Second International Conference on Computability and Complexity in Analysis_, August 25-29,2005, Kyoto, Japan, ser. Informatik Berichte, , vol. 326-7/2005. FernUniversit&#228;t Hagen, Germany, 2005, pp. 378&#8211;379. ([pdf](http://math.andrej.com/data/c2c.pdf))

General comments on intuitionistic mathematics/logic as the natural language for [[physics]] are in

* [[Andrej Bauer]], _[Intuitionistic mathematics for physics](http://math.andrej.com/2008/08/13/intuitionistic-mathematics-for-physics/)_, August 2008

For more on [[physics]] formalized in intuitionistic mathematics (notably in [[topos theory]]) see at _[[geometry of physics]]_.

[[!redirects intuitionistic mathematics]]
[[!redirects intuitionism]]