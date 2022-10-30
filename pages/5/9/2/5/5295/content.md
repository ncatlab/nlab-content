
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
 {#Idea}

_Intuitionistic mathematics_ (often abbreviated INT) is the earliest full-blown variety of [[constructive mathematics]], done according to the mathematical principles developed by [[L.E.J. Brouwer]] through his philosophy of _intuitionism_.

+--{: .standout}
Beware that this terminology is not consistent across mathematics.  Not infrequently the word "intuitionistic" is used to refer simply to [[constructive mathematics]] in general, or to [[constructive logic]], or to [[predicative mathematics|impredicative]] [[set theory]] done in constructive logic.  This page is about *Brouwer's intuitionism*, which is a specific variety of constructive mathematics that (unlike "neutral" constructive mathematics) uses axioms that [[contradiction|contradict]] [[classical mathematics]]. For more on this see at _[Terminology](#Terminology)_ below.
=--

The first main philosophical idea is that mathematical truth (a true statement) can only be attained in one's mind, by carefully arranging one's concepts and constructions in such a way that there remains absolutely no doubt that every aspect of the statement is verified, unambiguously, without reliance on any 'outside' assumption, for instance about the platonic nature of reality. (The [[principle of excluded middle]] is such an assumption, and Brouwer gave mathematical counterexamples to its validity, eventually leading to the foundational crisis in mathematics (Grundlagenstreit) around 1930, and Brouwer's conflict with Hilbert).

The second main philosophical idea is that the mind works over time. One does not have everything ready and done from the start. Infinity is a (perceived) idealized property of time, but one cannot have completed any infinite process or construction on any given day. Infinity is potential, not actual. 

The main mathematical idea then becomes that we can only build mathematical structures and truths starting from the natural numbers $0, 1, ...$ (where the dots indicate potential, not actual infinity). Natural numbers are definite and precise, but most real numbers, such as $\pi$, have a very different nature. We can only form something that we call '$\pi$' through a never-finished process of approximation.

Nonetheless, a substantial part of mathematics can be built up ('constructed') in this way. What mainly differentiates intuitionistic mathematics from [[constructive mathematics]] are two added axioms.  

Brouwer 'deduced' two axiomatic insights, notably 'continuous choice' and transfinite induction (in difficult language, calling it the `Bar Theorem' and giving a 'proof'). 'Continuous choice' conflicts with classical mathematics, the Bar Theorem is classically true. 

Kleene & Vesley (in _Foundations of Intuitionistic Mathematics_, 1965) offered a clean axiomatic approach which is nowadays called FIM. Kleene proved that FIM is equiconsistent with classical mathematics. Kleene also proved that theorems of FIM are recursively [[realizability|realizable]], which shows the computational content of FIM.


## Terminology
 {#Terminology}


Terminological ambiguity is often present in [[constructive mathematics]] and its varieties. Intuitionistic mathematics (INT) includes [[axioms]] that contradict [[classical logic]]; but people in non-foundational disciplines often use "intuitionistic" to mean roughly the same as "[[constructive|constructive mathematics]]" (say: mathematics without the [[principle of excluded middle]], usually with computational/algorithmic content and some restriction on impredicativity, but nothing added that contradicts classical mathematics).  


There are a variety of ways to use the term 'intuitionistic'.  We list them here, roughly from the most specific to the most general, and contrast (where appropriate) with the term 'constructive':

*  __Intuitionism__ is an early-20th-century [[philosophy of mathematics]] developed by [[Brouwer]], according to which [[mathematics]] is a free creation of a mind, and valid results are about what that mind creates (rather than about an external reality, as in [[platonism]], or about nothing, as in [[formalism]]).  From this controversial starting point, Brouwer drew even more controversial conclusions about both [[mathematics]] and [[logic]] (which he saw as derived from mathematics, rather than conversely as in [[logicism]]).  Intuitionism is one particular philosophy of [[constructivism]].

*  __Intuitionistic mathematics__ is the mathematics along the lines of the mathematics that Brouwer came up with.  However, it\'s not necessary to accept Brouwer\'s philosophy to practise intuitionistic mathematics; conversely, one may accept Brouwer\'s philosophical starting place but not his conclusions about the resulting mathematics.  Intuitionistic mathematics is one particular variety of [[constructive mathematics]].

   One example of intuitionistic mathematics (which nicely shows that intuitionism is not a matter of "belief" but of subject) is type II [[computable mathematics]] (see for instance [Bauer 05, section 4.3.1](#Bauer05)).

*  __[[intuitionistic set theory|Intuitionistic set theory]]__ is a [[set theory]], generally proffered as a [[foundation of mathematics]], intended to capture intuitionistic mathematics.  As the terminology is usually used (for example in the name of IZF, [[IZF|intuitionistic Zermelo-Frankel set theory]]), 'intuitionistic' means that [[excluded middle]] fails but [[power sets]] are included (making it [[impredicative mathematics|impredicative]]).  In contrast, 'constructive' set theory (such as CZF, [[CZF|constructive Zermelo-Frankel set theory]]) has [[function sets]] but not power sets (making it [[weakly predicative mathematics|weakly predicative]]).  The former is technically convenient, but the latter is better motivated.  That said, Brouwer\'s mathematics was even more predicative, making *both* of these set theories stronger than he would accept.

*  __[[intuitionistic type theory|Intuitionistic type theory]]__ is generally proffered as a [[foundation of mathematics]] that is (in most of its forms) both [[constructivism|constructive]] and [[predicativism|predicative]].  For purposes of comparing type theory to set theory, it might be nice if 'intuitionistic' and 'constructive' were distinguished for type theories as they are for set theories, but they aren\'t.  (Then again, there was never much sense in making that distinction for set theories using that terminology.)

There is variant of the [[NuPrl]] type theory with choice sequences [PDF](http://www.nuprl.org/html/Nuprl2Coq/continuity.pdf).

*  __[[Intuitionistic logic]]__ is the [[logic]] that intuitionistic mathematics, set theory, and type theory use, which lacks the principle of [[excluded middle]]; other forms of [[constructive mathematics]] also use intuitionistic logic, which is therefore also known as _constructive logic_.


## Mathematical principles

Brouwer never accepted a complete axiomatisation of intuitionistic mathematics.  However, we can identify several principles, which may not (even historically) be complete.

*  In hindsight, we may say that inuitionistic mathematics is done in a [[pretopos]] identified as [[Set]].

*  We have the [[axiom of infinity]] and [[countable choice]], as in [[classical mathematics]].

*  We have the classically false principles of [[continuity principle|continuity]] and [[continuous choice]].

*  We have the [[fan theorem]] and [[bar theorem]], which are classically true but fail in [[Russian constructivism]].

*  There\'s also some stuff about [[choice sequences]] that is highly philosophical, involving mathematical principles such as the [[Brouwer-Kripke scheme]].

Although it\'s not enough to derive all of the above, much of the essence of intuitionistic mathematics, or at least intuitionistic [[analysis]], can be summarized in the theorem that every (set-theoretic) [[function]] from the [[unit interval]] to the [[real line]] is [[uniformly continuous map|uniformly continuous]].


## Feel

In intuitionistic mathematics, already [[set theory]] behaves a lot like [[topology]], a point stressed by [[Frank Waaldijk]] ([web](http://www.fwaaldijk.nl/mathematics.html)). He uses the [[Kleene-Vesley]] system.  Fourman's [[continuous truth]] makes this remark precise using [[topos theory]].

Although intuitionistic mathematics does not accept all [[function sets]] (much less [[power sets]]), it seems to allow for both [[induction|inductive]] and [[coinduction|coinductive]] structures; see [a Caf&#233; comment](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html#c020731).
The reluctance to add function spaces is similar to the problem of function spaces in topology; see [[nice category of spaces]].

## Related concepts

* [[constructive mathematics]]

* [[intuitionistic type theory]]

* [[realizability]]


## References
 {#References}

The roots of Brouwer's intuitionism are apparently in his PhD thesis

* [[L.E.J. Brouwer]], _Over de Grondslagen der Wiskunde, PhD thesis_, Universiteit van Amsterdam, 1907.

Then an axiomatization of intuitionistic mathematics is given in

* [[Stephen Kleene]], R. E. Vesley, _The foundations of intuitionistic mathematics_, North-Holland (1965)

in terms of [[realizability]] (the [[Kleene-Vesley topos]]), and hence intuitionistic mathematics is shown to be consistent.

General reviews include

* Stanford Encyclopedia of Philosophy, _[Intuitionism in the Philosophy of Mathematics](http://plato.stanford.edu/entries/intuitionism/)

Reviews with further developments include for instance

* [[Frank Waaldijk]], _On the foundations of constructive mathematics -- especially in relation to the theory of continuous functions_  ([web](http://www.fwaaldijk.nl/mathematics.html#onthefoundations))

  (with a focus on [[constructive analysis]]).

For more see also the references at _[[constructive mathematics]]_.

That [[computable mathematics]] is an incarnation of intuitionistic mathematics is spelled out in the lecture notes below:

* {#Bauer05} [[Andrej Bauer]], around section 4,3.1 in _Realizability as connection between constructive and computable mathematics_, in T. Grubba, P. Hertling, H. Tsuiki, and [[Klaus Weihrauch]], (eds.) _CCA 2005 - Second International Conference on Computability and Complexity in Analysis_, August 25-29,2005, Kyoto, Japan, ser. Informatik Berichte, , vol. 326-7/2005. FernUniversit&#228;t Hagen, Germany, 2005, pp. 378&#8211;379. ([pdf](http://math.andrej.com/data/c2c.pdf))

Discussion of basic [[topology]] in intuitionistic mathematics is in

* {#Waaldijk96} [[Frank Waaldijk]], _modern intuitionistic topology_, 1996 ([pdf](http://www.fwaaldijk.nl/modern%20intuitionistic%20topology.pdf))


General comments on intuitionistic mathematics/logic as the natural language for [[physics]] are in

* [[Andrej Bauer]], _[Intuitionistic mathematics for physics](http://math.andrej.com/2008/08/13/intuitionistic-mathematics-for-physics/)_, August 2008

For more on [[physics]] formalized in intuitionistic mathematics (notably in [[topos theory]]) see at _[[geometry of physics]]_.


[[!redirects intuitionistic mathematics]]
[[!redirects intuitionism]]
