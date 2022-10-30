
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **well-ordering theorem** is a famous result in [[set theory]] stating that every [[set]] may be [[well-order|well-ordered]].

Fundamental for [[Georg Cantor| G. Cantor's]] approach to transfinite arithmetic it was an open problem until [[Ernst Zermelo|E. Zermelo]] gave a proof in 1904 using the [[axiom of choice]] to which it is in fact equivalent if one admits the principle of [[excluded middle]].

Hence, classically, it is one of the many equivalent formulations of the axiom of choice like e.g. [[Zorn's lemma]].

## Statement and proof 

Given any [[set]] $S$, there exists a [[well-order]] $\prec$ on $S$.

The first proof was given in ([Zermelo 1904](#Zermelo04)).


## Consequences 

If every set can be well-ordered, then the natural map from [[ordinal number]]s to [[cardinal number]]s is a [[surjection]].  Since these form proper classes, the ordinary axiom of choice will not split this surjection automatically; however, we can easily split it by assigning each cardinal number to the *smallest* ordinal number with that cardinality.  (This does require [[excluded middle]], however.)  In this way, a cardinal number may be *defined* to be an ordinal number that is _initial_: such that no smaller ordinal number has the same cardinality.

As in the argument above, the [[axiom of choice]] follows; given any [[surjection]] $f: A \to B$, place a well-ordering on $A$ and then split $f$ by mapping an element $y$ of $B$ to the smallest element $x$ of $A$ such that $y = f(x)$.  Again, this uses [[excluded middle]] to show that such a smallest element exists, so the well-ordering principle does not (seem to) imply the axiom of choice constructively.

To get the large (or "global") axiom of choice (that any surjection between proper classes splits), we need a large well-ordering theorem: that every proper class can be well-ordered.  The large principles do not follow from the small ones.

## History 

**Georg Cantor** first developed [[set theory]] in the context of studying well-ordered sets of [[real number]]s whence the validity of the well-ordering principle became important for his theory of [[ordinal numbers]]. In his 1883 paper he calls it a _'fundamental and weighty law of thought that is remarkable for his generality'_ and promised to come back to it later ([Cantor 1932](#Cantor32), p.169). In the following, he announced proofs but they failed to materialize so that he was forced to take it as an assumption.[^choice] 

[^choice]:This contrasts with Cantor's attitude towards the axiom of choice which he used implicitly but never thematised explicitly. In fact, the full explicit awareness of the use of the axiom choice in mathematics had to await the controversy over Zermelo's well-ordering theorem in 1904 (with some anticipation by G. Peano and B. Levi earlier).

Consequently, the well-ordering principle ended as 'a very strange claim' second on [[Hilbert's problems|Hilbert's millenium list]] of open problems in mathematics in 1900. Then in 1904, the Hungarian mathematician J. K&#246;nig announced a proof that the [[continuum]] could not be well-ordered but had to retract the proof.

Soon afterwards in 1904, [[Ernst Zermelo]] finally gave a proof using the [[axiom of choice]] following a suggestion by E. Schmidt. The proof, albeit correct, was met with heavy criticism by prominent mathematicians so that Zermelo published a new proof and a defense of the contested axiom of choice in 1908.

The attempt to make explicit the set-theoretic assumptions in the proof led him to publish his axioms for set theory in the same year which became later a part of [[Zermelo-Fraenkel set theory]]. Hence the 1904ff controversy proved to become a _decisive watershed for the development of modern mathematics_: triggering the advent of set-theoretic [[foundation of mathematics]] and putting the problem of non-constructive methods of proof on the agenda. 

## Assessment

That the well-ordering theorem is more of a *theorem* in need of a proof, while the axiom of choice is more of an *axiom* to be assumed without proof is, of course, a matter of opinion, but it\'s reflected in Jerry Bona\'s famous quotation:
>The Axiom of Choice is obviously true, the well-ordering principle obviously false, and who can tell about [[Zorn's lemma]]?

Ironically, in [[constructive mathematics]], the well-ordering principle is (seemingly) actually *weaker* than the full axiom of choice, as it does not imply excluded middle by itself.  It does, however, imply the full axiom of choice (and hence excluded middle) if by 'well-order' we mean a _classical_ [[well-order]], in the sense that every inhabited subset has a least element, rather than the constructively sensible notion of well-order that merely permits inductive proofs. [[Zorn's lemma]] is likewise constructively weaker than the axiom of choice, although it is not particularly useful without excluded middle.

+--{: .query}
At least, as far as I can tell it doesn\'t.  I\'ve never actually seen a metamathematical result proving this, however.

[[Mike Shulman|Mike]]: If "well-order" is interpreted in the classical sense "every nonempty set has a least element," then I believe it does imply full choice.  I don't know what happens if "well-order" is interpreted in the constructively reasonable sense.   I know that Zorn's lemma, even in the classical version, can be true in a non-Boolean topos, although it is not particularly useful without excluded middle.

_Toby_:  That\'s correct; any well-ordered set, even in the slightly weaker sense that every *inhabited* subset has a least element, must be a choice set (as you remarked at [[choice object]]).  One of us should add a note about that to this article.

_Mike_: It would be nice to have different words to distinguish between "constructively correctly well-ordered" and "classically well-ordered."  The [[Elephant]], at least, uses "well-ordered" for the classical notion which implies choice; do most practicing constructivists use the constructively sensible notion?

_Toby_:  Shockingly many constructivists aren\'t aware how to fix the definition (which is highly non-predicative anyway).  Some use the no-infinite-descending-chains version for the purpose of doing Burali-Forti, but it\'s not good for anything else.  Since the existence of any 'classically' well-ordered set with two non-equal elements implies excluded middle already, many constructivists consider the concept useless.  So basically, constructivists either have to do it right or not at all.

We have '[[choice object|choice set]]' for 'classically well-order*able* set', so maybe we could say 'choice order' or something for 'classical well-order'.  (Obviously, those constructivists who say 'choice set' for a [[projective object|projective set]] wouldn\'t use this term.)  There may be more terms in Paul Taylor\'s [paper](http://paultaylor.eu/ordinals/#intso) on various kinds of ordinals in constructive mathematics (as isomorphism classes of well-ordered sets are not the only useful kind), which I\'ve never fully read.

But I think that 'classically well-ordered' should be all right.  By default, 'well-ordered' should mean the constructively correct notion, since this is what constructivists need and classical mathematicians don\'t care.  The only place where 'classically well-ordered' needs to be said is here (and possibly at [[axiom of choice]]), in the definition section of [[well-order]], and perhaps in statements about well-ordered sets that aren\'t constructively valid (if adding 'classically' will make them constructively valid), but even that is kind of pointless and it\'s simpler just to say that the result is not constructively valid and useful.

[[Mike Shulman|Mike]]: I've started trying to uniformize terminology among these pages, using 'classical well-order' where appropriate.  I agree that 'well-order' should mean the constructively correct notion, but I don't want to alienate non-constructivists by hiding the definition they are familiar with in comments about constructivism.  So I'm trying to isolate the comments about constructivism a bit.  I think this query box could probably be deleted now.

_Toby_:  Well, constructivists are used to being isolated.  At least we give the good definitions *first*, so that\'s a big improvement!  (^_^)
=--

## Related entries

* [[Zorn's lemma]]

* [[axiom of choice]]

* [[Hartogs number]]

## References

The original proof is in

* [[Ernst Zermelo]], _Beweis, da&#223; jede Menge wohlgeordnet werden kann_ , Mathematische Annalen **59** (1904) pp.514-516. ([gdz](http://gdz.sub.uni-goettingen.de/no_cache/en/dms/load/img/?IDDOC=28526))
 {#Zermelo04}

The second proof together with an eloquent defense of the axiom of choice can be found in

* [[Ernst Zermelo]], _Neuer Beweis f&#252;r die M&#246;glichkeit einer Wohlordnung_ , Mathematische Annalen **65** (1908) pp.107-128. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002261952)) {#Zermel08}

Cantor's texts are collected together with comments by Zermelo in

* [[Ernst Zermelo]] (ed.), _Georg Cantor - Gesammelte Abhandlungen Mathematischen und Philosophischen Inhalts_ , Springer Berlin 1932. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/toc/?PPN=PPN237853094)) {#Cantor32}

English versions of Zermelo's papers are in

* J. van Heijenoort (ed.), _From Frege to G&#246;del - A Source Book in Mathematical Logic 1879-1931_ , Harvard UP 1967.

On the relation between AC and the well-ordering principle in general toposes see

* [[Peter Freyd]], _Choice and Well-ordering_ , APAL **35** (1987) pp.149-166.

* M.-M. Mawanda, _Well-ordering and Choice in Toposes_ , JPAA **50** (1988) pp.171-184.

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. II_, Oxford UP 2002. (D4.5, pp.987-998)

* J. Todd Wilson, "An Intuitionistic version of Zermelo's proof that every choice set can be well-ordered", J. Symbolic Logic, 66:3 (2001), 1121--1126; ([JSTOR](http://www.jstor.org/stable/2695096): paywalled), [formalization in the Lean Theorem Prover] (https://github.com/lambdacalculator/lean-choice).


[[!redirects well-ordering theorem]]
[[!redirects well-ordering principle]]