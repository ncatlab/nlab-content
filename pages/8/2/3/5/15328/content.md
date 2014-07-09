
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

_Lindstr&#246;m's theorem_, or more precisely, Lindstr&#246;m's theorems, are important results in [[abstract model theory]] due to the Swedish logician [[Per Lindström]] that give syntax-free characterizations of (classical untyped) [[first-order logic]] ('syntax-free' in the sense of not referring to the specific [[syntax|syntactic]] make up of the formulas).

###The first theorem of Lindstr&#246;m###
This  ([[semantics|semantic]]) version of Lindstr&#246;m's characterization is the best known and is usually meant when one speaks of ' _the_ theorem of Lindstr&#246;m' . It states that the validity of the downward [[Löwenheim-Skolem theorem]] (a sentence that holds in some [[model]] already holds in an at most countable model) and the [[compactness theorem]] (a set of sentences has a model if every finite subset has a model) characterizes up to expressive power standard [[first-order logic]] among all [[formal logic|logics]] satisfying certain regularity conditions[^fine]:

[^fine]: These conditions formalize some classical background assumptions on logical systems like the restriction of semantics to standard set-theoretic structures and the existence of [[negation]] in the sense that for every sentence $\varphi$ there is $\psi$ such that $\mathfrak{A}\models\varphi$ iff not $\mathfrak{A}\models\psi$.

A gain in expressive power comes at the price of the loss of the validity of at least one of these theorems e.g. in [[second-order logic]] both theorems fail to hold. 

_Jon Barwise_ (1977, p.45, cf. below) has called the first Lindstr&#246;m theorem 

>one of the first, and still most striking, results in abstract model theory.

###The second theorem of Lindstr&#246;m###
The _second_ Lindstr&#246;m theorem is of a more proof-theoretic nature and involves the concept of an _effective logical system_ which draws on [[computability theory]]. It achieves a characterization of standard first-order logic in the class of all effective regular logical systems by the two properties of having an enumerable set of tautologies and validity of the L&#246;wenheim-Skolem theorem.

##Discussion##
These results are sometimes viewed as an explanation of the privileged role that standard first-order logic plays in mathematical logic.

In the end, what lesson one draws from them (once the classical background assumptions accepted), largely hinges on how one assesses the role of the _[[Löwenheim-Skolem theorem]]_ in mathematical logic, which enjoys a rather controversial status and has encountered skepticism already by _Thoralf Skolem_, the man himself. This scepticism is clearly present in the following comment by _Hao Wang_ (1974, quoted after Flum(1985), pp.77-78):

>..what is established (by Lindstr&#246;m's theorem) is not that first-order logic is the only possible logic but rather that is the only possible logic when we in a sense deny the reality to the concept of uncountability ... 

Further alternative characterizations and extensions to other logics are known and constitute the field of [[abstract model theory]].


## Related concepts

* [[predicate logic]]

* [[higher order logic]]

* [[Löwenheim-Skolem theorem]]

* [[compactness theorem]]

* [[abstract model theory]]

## References

* [[Per Lindström]]: _On Extensions of Elementary Logic_, Theoria 35 pp.1-11 (1969)

* Barwise (ed.): _Handbook of Mathematical Logic_ , Elsevier Amsterdam 1977.

A textbook account of the results appears in:

* Ebbinghaus, Flum, Thomas : _Einf&#252;hrung in die mathematische Logik_, Wissenschaftliche Buchgesellschaft Darmstadt 1986.

A more recent overview of Lindstr&#246;m's results can be found here:

* [[Jouko Väänänen]], _Lindstr&#246;m's Theorem_ . Ms. ([pdf](http://www.math.helsinki.fi/logic/opetus/lt/lindstrom_theorem1.pdf))

Further material (including a discussion of the broader implications of Lindstr&#246;m's results for logic) can be found in

* J&#246;rg Flum, _Characterizing Logics_ , ([pdf](http://projecteuclid.org/download/pdf_1/euclid.pl/1235417268)), chap. III of

* Barwise, Feferman (eds.), _Model-theoretic Logics_ , Springer Heidelberg 1985 ([toc](http://projecteuclid.org/euclid.pl/1235417263#toc))

[[!redirects Lindström theorem]]
[[!redirects Lindström's theorems]]
[[!redirects Lindström-theorem]]
[[!redirects Lindström-theorems]]
[[!redirects Lindstrom's theorem]]
[[!redirects Lindström's Theorem]]
[[!redirects Lindstrom's Theorem]]