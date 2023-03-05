
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

> The interesting conception of the [[propositions-as-types]] principle is what I call _Brouwer's Dictum_, which states that all of mathematics, including the concept of a proof, is to be derived from the concept of a *[[constructive mathematics|construction]]*, a [[computation]] classified by a [[type]].  In [[intuitionistic mathematics]] proofs are themselves "first-class" mathematical objects that inhabit [[type|types]] that may as well be identified with the [[proposition]] that they prove.  Proving a proposition is no different than constructing a [[program]] of a type.  In this sense [[logic]] is a branch of [[mathematics]], the branch concerned with those constructions that are proofs.  And mathematics is itself a branch of [[computer science]], since according to Brouwer's Dictum all of mathematics is to be based on the concept of computation.  But notice as well that there are many more constructions than those that correspond to proofs.  [[natural number|Numbers]], for example, are perhaps the most basic ones, as would be any [[inductive type|inductive]] or [[coinductive type|coinductive]] types, or even more exotic objects such as Brouwer's own [[choice sequence]]s.  From this point of view the [[judgement]] $t\in A$ stating that $t$ is a [[term|construction]] of type $A$ is of fundamental importance, since it encompasses not only the formation of "ordinary" mathematical constructions, but also those that are distinctively intuitionistic, namely mathematical proofs.

> An often misunderstood point that must be clarified before we continue is that the concept of proof in [[intuitionistic logic|intuitionism]] is *not* to be identified with the concept of a *formal proof* in a fixed formal system.  What constitutes a proof of a [[proposition]] is a *[[judgement]]*, and there is no reason to suppose _a priori_ that this judgement ought to be [[decidable judgment|decidable]].  It should be possible to recognize a proof when we see one, but it is not required that we be able to *rule out* what is a proof in all cases.  In contrast formal proofs are inductively defined and hence fully circumscribed, and we expect it to be decidable whether or not a purported formal proof is in fact a formal proof, that is whether it is well-formed according to the given inductively defined rules.  But the upshot of [[incompleteness theorem|Gödel's theorem]] is that as soon as we fix the concept of formal proof, it is immediate that it is not an adequate conception of proof _simpliciter_, because there are propositions that are true, which is to say have a proof, but have no *formal proof* according to the given rules.  The concept of truth, even in the intuitionistic setting, eludes formalization, and it will ever be thus.  Putting all this another way, according to the intuitionistic viewpoint (and the mathematical practices that it codifies), there is no truth other than that given by proof.  Yet the rules of proof cannot be given in decidable form without missing the point. ([Harper](#Harper))


## Definition

* [In type theory](#Proof)

* [Formal proofs](#FormalProof)


### In type theory
 {#Proof}

In [[type theory]], a [[proposition]] is identified with the [[type]] of all its proofs (the _[[propositions as types]]_-aspect of [[computational trinitarianism]]). 
Here a proof consists of exhibiting a [[term]] of the corresponding type (showing that it is [[inhabited]]), hence a proof is a typing [[judgement]] for a term of the type representing the proposition.

See also _[[proofs as programs]]_.


### Formal proofs
 {#FormalProof}

A [[formal proof]] is whatever is called a 'proof' in a formal system; a formal system for [[mathematics]] then gives rules for producing a proof in the above sense.  Typically, a formal system is [[induction|inductively]] defined, and hence its proofs are fully circumscribed; this is the case for [[deductive systems]] such as [[natural deduction]], [[sequent calculus]], and [[Hilbert systems]].  [[incompleteness theorem|Gödel's theorem]] suggests, however, that no such system can encapsulate all of mathematics.



## Relation to observation in physics
 {#RelationToObservationInPhysics}

In ([Jaffe-Quinn 93, p. 2](JaffeQuinn93)) it was claimed that

> {#JaffeQuinnProofIsObservation} the role of rigorous [[proof]] in mathematics is functionally [[analogy|analogous]] to the role of [[experiment]] in the natural sciences 

+-- {: .un_remark} 
###### Remarks 
After making this statement about proof as observation, the article by Jaffe-Quinn goes further to suggest that the analogue in physics of speculation and conjecture in mathematics is the realm of theoretical physics, and then maybe even further in suggesting that mathematics could reasonably be purely "theoretical" in this sense. These further claims were considered faulty by several authors ([math/9404229](http://arxiv.org/abs/math/9404229)). 

([[Saunders MacLane]] in particular argued for theorems and proofs as the final goal of a piece of developed mathematics, and emphasized the explanatory function of proofs. This in contrast with experiment in physics, which is neither considered as the final goal nor as playing an explanatory role.) 

While all this does contradict some of Jaffe-Quinn's claims, it may still harmonize with the statement [above](#JaffeQuinnProofIsObservation). Indeed, another perspective on the claim is that finding a proof is an observational or witnessing act, which resonates with the nature of proof in [[constructive mathematics]], such as made manifest in the [[propositions as types]]-paradigm. This perspective sees proof as something more than merely establishing the truth of a proposition. 

> ... to show that a proposition is true in type theory corresponds to exhibiting an element $[$ [[term]] $]$ of the type corresponding to that proposition. We regard the elements of this type as _evidence_ or _witnesses_ that the proposition is true. (They are sometimes even called _proofs_... (from [[Homotopy Type Theory -- Univalent Foundations of Mathematics]], section 1.11)

Thus a proof *qua* witness is a construction, and in more elaborated developments (for instance in [[intensional type theory]]) a formal proof is itself a mathematical object, with internal mathematical structure. 
=-- 

## Proof methods
 {#ProofMethods}

* [[refutation by contradiction]]

* [[proof by contradiction]], 


## Libraries of formal proofs
 {#LibrariesOfFormalProofs}

Libraries of [[formal proofs]] formalized in some [[proof assistant]]:

* [[UniMath project]]

* [[Xena project]]

* [[ForMath project]]

* [[Archive of Formal Proofs]]

* [[The QED Project]]



## Related concepts


* [[computational trinitarianism]]


* [[proof theory]]

\linebreak

[[!include mathematical statements --- contents]]


\linebreak


[[!include proof assistants and formalization projects -- list]]



## References

General introduction to the notion of proof in modern rigorous mathematics:

* {#Girard89} [[Jean-Yves Girard]] (translated and with appendiced by [[Paul Taylor]] and [[Yves Lafont]]), *Proofs and Types*, Cambridge University Press (1989) &lbrack;[ISBN:978-0-521-37181-0](), [webpage](http://www.paultaylor.eu/stable/Proofs+Types.html), [pdf](https://www.paultaylor.eu/stable/prot.pdf)&rbrack;

* {#Quinn2009} [[Frank Quinn]]: *Proof Projects for Teachers* (2009) &lbrack;[pdf](https://personal.math.vt.edu/fquinn/education/pfs4teachers0.pdf), [[Quinn-ProofProjects.pdf:file]]&rbrack;


A brief exposition of the notion of proof and formal proof in [[constructive mathematics]]/[[type theory]] is in 

* {#Harper} [[Robert Harper]], _Extensionality, Intensionality, and Brouwer's Dictum_, August 2012 ([web](http://existentialtype.wordpress.com/2012/08/11/extensionality-intensionality-and-brouwers-dictum/))


* [[Robert Harper]], _Constructive Mathematics is not Meta-Mathematics_, July 2013 ([web](http://existentialtype.wordpress.com/2013/07/10/constructive-mathematics-is-not-meta-mathematics/))

Discussion of formal proof in view of [[proof assistants]]:

* [[Thomas Hales]], _Formal proof_, Notices of the AMS **55** 11 (2008) 1370-1379 &lbrack;[pdf](http://www.ams.org/notices/200811/tx081101370p.pdf)&rbrack;

* John Harrison, _Formal proof -- theory and practice_ ([pdf](http://www.ams.org/notices/200811/tx081101395p.pdf))

* [[Jeremy Avigad]], Kevin Donnelly, David Gray, Paul Raff, _A formally verified proof of the prime number theorem_ ([arXiv:cs/0509025](http://arxiv.org/abs/cs/0509025))

* [[Jeremy Avigad]], John Harrison, _Formally Verified Mathematics_, Communications of the ACM, Vol. 57 No. 4, Pages 66-75 ([web](http://cacm.acm.org/magazines/2014/4/173219-formally-verified-mathematics/fulltext))

* [[Jeremy Avigad]], _Formal verication, interactive theorem proving, and automated reasoning_ (2014) ([pdf](http://www.andrew.cmu.edu/user/avigad/Talks/baltimore.pdf))

A discussion of the relation of mathematical proof to [[phenomenology]] of [[theories]] of [[physics]] is in 
 
* {#Miquel} [[Alexandre Miquel]], _The experimental effectiveness of mathematical proof_ ([pdf](http://perso.ens-lyon.fr/alexandre.miquel/publis/effectiveness.pdf))

Discussion of the statistics and *reception* of formal proof:

* {#ViteriDeDeo22} Scott Viteri, Simon DeDeo, *Epistemic Phase Transitions in Mathematical Proofs*, Cognition **225** (2022) 105120 &lbrack;[arxiv:2004.00055](https://arxiv.org/abs/2004.00055), [doi:10.1016/j.cognition.2022.105120](https://doi.org/10.1016/j.cognition.2022.105120)&rbrack;


Texts on genuine [[proof theory]] include

*  [[Richard Statman]], _[[Structural Complexity of Proofs]]_, 1974


Projects aiming to formalize parts of mathematics include

* [[ForMath]]

* [[The QED Project]]

* [Xena](https://xenaproject.wordpress.com/2018/10/07/what-is-the-xena-project/) (by [[Kevin Buzzard]])

Consideration of the relation of mathematical proof to physics icludes

* {#JaffeQuinn93} [[Arthur Jaffe]], [[Frank Quinn]], _"Theoretical Mathematics": Towards a cultural synthesis of mathematics and theoretical physics_, Bulletin of the AMS, Volume 29,Number 1, July 1993 ([arXiv:math/9307227](http://arxiv.org/abs/math/9307227))


[[!redirects proof]]
[[!redirects proofs]]

[[!redirects formal proof]]
[[!redirects formal proofs]]

[[!redirects rigorous proof]]
[[!redirects rigorous proofs]]

