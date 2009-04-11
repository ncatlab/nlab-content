The _well-ordering theorem_ states that every [[set]] may be [[well-order]]ed.  It is a theorem in the sense that it can be proved assuming the [[axiom of choice]].  On the other hand, the axiom of choice can instead be proved using the well-ordering theorem and the principle of [[excluded middle]].

# Statement and proof #

Given any [[set]] $S$, there exists a [[well-order|well order]] $\prec$ on $S$.

To prove this, ... read [Zermelo](http://gdz.sub.uni-goettingen.de/no_cache/en/dms/load/img/?IDDOC=28526) (in German).

# History #

Georg Cantor first developed [[set theory]] in the context of studying well-ordered sets of [[real number]]s and considered the well-ordering theorem a 'law of thought' ('Denkgesetz') without need of proof.

Ernst Zermelo gave a proof in 1904, but many mathematicians were concerned about the proof\'s validity.  Analysis of Zermelo\'s proof isolated the [[axiom of choice]] and led to that axiom\'s first explicit formulation (also by Zermelo).

That the well-ordering theorem is more of a *theorem* in need of a proof, while the axiom of choice is more of an *axiom* to be assumed without proof is, of course, a matter of opinion, but it\'s reflected in Jerry Bona\'s famous quotation:
>The Axiom of Choice is obviously true, the well-ordering principle obviously false, and who can tell about Zorn's lemma?
Ironically, in [[constructive mathematics]], the well-ordering principle is actually *weaker* than the full axiom of choice, as it does not imply excluded middle by itself.

+--{: .query}
At least, as far as I can tell it doesn\'t.  I\'ve never actually seen a metamathematical result proving this, however.

[[Mike Shulman|Mike]]: If "well-order" is interpreted in the classical sense "every nonempty set has a least element," then I believe it does imply full choice.  I don't know what happens if "well-order" is interpreted in the constructively reasonable sense.   I know that Zorn's lemma, even in the classical version, can be true in a non-Boolean topos, although it is not particularly useful without excluded middle.

_Toby_:  That\'s correct; any well-ordered set, even in the slightly weaker sense that every *inhabited* subset has a least element, must be a choice set (as you remarked at [[choice object]]).  One of us should add a note about that to this article.
=--

# Consequences #

If every set can be well-ordered, then the natural map from [[ordinal number]]s to [[cardinal number]]s is a [[surjection]].  Since these form proper classes, the ordinary axiom of choice will not split this surjection automatically; however, we can easily split it by assigning each cardinal number to the *smallest* ordinal number with that cardinality.  (This does require [[excluded middle]], however.)  In this way, a cardinal number may be *defined* to be an ordinal number that is _initial_: such that no smaller ordinal number has the same cardinality.

As in the argument above, the [[axiom of choice]] follows; given any [[surjection]] $f: A \to B$, place a well-ordering on $A$ and then split $f$ by mapping an element $y$ of $B$ to the smallest element $x$ of $A$ such that $y = f(x)$.  Again, this uses [[excluded middle]] to show that such a smallest element exists, so the well-ordering principle does not (seem to) imply the axiom of choice constructively.

To get the large (or "global") axiom of choice (that any surjection between proper classes splits), we need a large well-ordering theorem: that every proper class can be well-ordered.  The large principles do not follow from the small ones.