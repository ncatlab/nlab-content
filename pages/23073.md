
# Full (unrestricted) comprehension

* table of contents
{: toc}

## Idea

The axiom or rule of **full** or **unrestricted comprehension** says that for any property $P$, there exists a set of all objects satisfying $P$:

$$ \{ x \mid P(x) \}. $$

[[set theory|Set theory]] with the unrestricted comprehension rule is called [[naive set theory]], and is inconsistent due to [[Russell's paradox]] and [[Curry's paradox]].  Here we mention several approaches to this issue.

## Restricted comprehension

Standard set theories such as [[ZFC]] avoid this paradox by replacing unrestricted comprehension with the [[axiom scheme of separation]] (or "restricted comprehension"), which restrictes $x$ to lie in some previously specified set $X$.

## Stratified comprehension

Set theories such as [[New Foundations]] instead replace comprehension by a rule of "stratified comprehension".  This permits a "set of all sets" but still appears to avoid paradox.

## Substructural logics

It is also possible to retain full comprehension but avoid paradox by modifying the ambient logic.  Passing to [[constructive logic]] doesn't help, and indeed the root issue has nothing to do with [[negation]] as such, since Curry's paradox can be stated without any negation.  One might think that [[paraconsistent logic]] would help, but many paraconsistent logics are still vulnerable to Curry's paradox.  Perhaps the most obvious culprit is the [[contraction rule]], and indeed [[linear logic]] (including some paraconsistent logics) can admit a full comprehension rule without explosion.

## Normal logics

Another possibility is to keep the contraction rule but restrict the use of the [[cut rule]].  It is not necessary to forbid all uses of cut, since many cuts can be normalized or eliminated.  Indeed, in ordinary consistent logic, *all* cuts can be eliminated; but in the presence of full comprehension they cannot all be.  Thus, another way to avoid paradox with full comprehension is to permit only proofs that can be normalized.

Note that unlike a restriction on contraction, this is a "global" restriction: the proofs of two lemmas can independently be valid, but their combination may no longer be so.  Similar "global" restrictions on logic were investigated by Fitch.

## References

### In linear logic

* Grishin, V. N., "Predicate and set theoretic calculi based on logic without contraction rules" (Russian), _Izvestiya Akademii Nauk SSSR Seriya Matematicheskaya_, 45(1): 47 &#8211; 68, 1981. English translation in Math. USSR Izv., 18(1): 41 &#8211; 59, 1982. ([math-net.ru](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=im&paperid=1547&option_lang=eng))

* [[Jean-Yves Girard]], Light Linear Logic, _Information and Computation_, 14(3):123-137, 2003. ([pdf.gz](http://iml.univ-mrs.fr/~girard/LLL.pdf.gz))

* [[Kazushige Terui]], Light Affine Set Theory: A Naive Set Theory of Polynomial Time, _Studia Logica: An International Journal for Symbolic Logic_, Vol. 77, No. 1 (Jun., 2004), pp. 9-40. ([jstor](http://www.jstor.org/stable/20016605)) ([pdf](http://www.kurims.kyoto-u.ac.jp/~terui/lastfin.pdf)).  See also Terui's slides, [Linear Logic and Naive Set Theory (Make our garden grow)](http://www.kurims.kyoto-u.ac.jp/~terui/summer3.pdf)

### Global restrictions

Several global restrictions were considered in

* [[Frederic Fitch]], *Symbolic Logic: An introduction*, 1952

* [[Frederic Fitch]], *A method for avoiding the Curry paradox*, in *Essays in Honor of Carl G. Hempel*, Reidel, Dordrecht, Holland 1969, pp. 255--265.

The notation therein is somewhat difficult to follow for a modern reader, especially due to the somewhat confused treatment of what nowadays would be called free and bound variables.  A more modern explanation of Fitch's restrictions can be found in:

* Susan Rogerson, _Natural deduction and Curry's paradox_, Journal of Philosophical Logic (2007) 36: 155--179. [pdf](https://link.springer.com/content/pdf/10.1007/s10992-006-9032-0.pdf)

The normalizability restriction is also discussed philosophically in

* Tennant, N.: *Proof and paradox*, Dialectica 36 (1982), 265-296

and other references (someone add!).

category: foundational axiom

[[!redirects full comprehension]]
[[!redirects full comprehension rule]]
[[!redirects axiom of full comprehension]]
[[!redirects axioms of full comprehension]]
[[!redirects axiom scheme of full comprehension]]
[[!redirects axiom schemes of full comprehension]]
[[!redirects axiom schema of full comprehension]]
[[!redirects axiom schemas of full comprehension]]
[[!redirects axiom schemata of full comprehension]]

[[!redirects unrestricted comprehension]]
[[!redirects unrestricted comprehension rule]]
[[!redirects axiom of unrestricted comprehension]]
[[!redirects axioms of unrestricted comprehension]]
[[!redirects axiom scheme of unrestricted comprehension]]
[[!redirects axiom schemes of unrestricted comprehension]]
[[!redirects axiom schema of unrestricted comprehension]]
[[!redirects axiom schemas of unrestricted comprehension]]
[[!redirects axiom schemata of unrestricted comprehension]]
