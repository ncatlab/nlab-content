
# Axioms of replacement and collection
* table of contents
{: toc}


## Idea

>_Zwei &#228;quivalente Vielheiten sind entweder beide 'Mengen' oder beide inkonsistent._ [[Georg Cantor]] (1899)[^Cant]

[^Cant]: _'Two equivalent multiplicities either are both "sets" or are both inconsistent'_, letter to Dedekind from 28th July 1899 ([Cantor 1932](#Cantor99), p.444). This is suggested as an early formulation of the axiom of replacement by van Heijenoort (1967, p.113). A categorical formalization of Cantor's idea as an extension for [[ETCS]] is given in [McLarty (2004)](#McLarty).

**Axioms of collection** and replacement are axiom schemata in [[set theory]] that permit to construct new sets from other already given sets thereby contributing substantially to the size of the set-theoretic universe and hence are seen as 'strong' axioms.

The most famous of these schemata is the **axiom of replacement**[^name] of [[Zermelo-Fraenkel set theory]] that was suggested by A. Fraenkel and formulated by [[Thoralf Skolem|T. Skolem]] in 1922. Given a unary operation $F$ and a set $x$ it permits to collect all $F(y)$ for $y\in x$ into a new set.

[^name]: The term 'replacement', or 'Ersetzungsaxiom' in German, is apparently due to [Fraenkel (1922)](#Fraenkel22) and was intended as a provisory terminology until the final formalization of Zermelo's notion of a 'definite property' which was identified with a first-order formula in the language of set theory by Skolem in the same year (and independently earlier by [[Hermann Weyl|H. Weyl]]).

The resulting expansiveness of the set-theoretic universe is somewhat peripheral to the practice of 'ordinary' mathematics and therefore a [[structural set theory]] like [[ETCS]] can omit replacement without incurring a great loss[^etcs]. Even in the context of a ZF-equivalent material set theory the axiom of replacement can be traded in for a [[reflection principle]][^bellmach].

[^bellmach]: See [Bell-Machover 1977](#BellMach77), p.495.

[^etcs]: It is possible, however, to augment a categorical set theory with a version of replacement if necessary as shown in ([Osius 1974](#Osius74), section 9) resulting in a system with the full strength of ZF. According to [McLarty (2004)](#McLarty04), Osius' ideas go back to discussions between Lawvere and the Berkeley logicians on reflection principles in 1963. McLarty's paper proposes another equivalent way to flesh out replacement categorically!

Axioms of replacement and collection become useful, however, whenever [[recursion|recursively]] constructing a set that is 'larger' than any set known before:

>what the axiom of replacement is mainly needed for in mathematical practice is to define families of sets indexed by some set I carrying some inductive structure as, typically, the set $N$ of natural numbers.[^streicher]

[^streicher]: [[Thomas Streicher]] ([2005, p.79](#Streicher05)). See there for further discussion of the role of replacement for _mathematics beyond $V_{\omega +\omega}$_ and the handling of similar iterated collection processes in toposes by universes.

There are many variations on these axiom schemata, but any given system should only need one.


## Statements

In general, these axioms apply to a [[binary relation]] that relates elements of one [[set]] $A$ to arbitrary sets.  However, we do *not* expect that the relation itself be an object in the theory; really, we have an axiom schema with one axiom for every binary [[predicate]] of the proper form.  We will write this predicate as $\phi(x,Y)$, where $x$ stands for an elment of $A$ and $Y$ stands for any set.  (Note that there may well be other free variables in the predicate.)

Generally, $\phi$ will need to be an [[entire relation]] for the axiom to apply; that is, the axiom has as a hypothesis that, for every $x \in A$, there is some $Y$ such that $\phi(x,Y)$ holds.  In versions called 'replacement' instead of 'collection', $\phi$ also needs to be [[functional relation|functional]]; that is, the axiom has the hypothesis that, for every $x \in A$, there is a *unique* $Y$ such that $\phi(x,Y)$ holds.  Thus, most of the 'replacement' versions only make sense if the language has a notion of [[equality]] of sets.

So much for the hypothesis of the axiom; the conclusion asserts the existence of a [[family of sets]] to which appropriate $Y$s belong.  In a material set theory, we can simply state the existence of set $\mathcal{F}$ such that certain $Y \in \mathcal{F}$.  In a structural set theory, we state the existence of an index set $I$, a total set $E$, and a function $f\colon E \to I$ such that each [[fibre]] $f^*(x)$ for $x \in I$ is equal to (or at least isomorphic to) certain $Y$.  (Often we can take $I$ to be $A$, but that does not come into the statement of the axioms.)

+-- {: .query}
Who wants to write out some of these?
=--


## Lawvere on replacement

>A question that has been much of a "foundational" interest, though of hardly any significance for the practice of algebra, topology, functional analysis, etc. is whether, for a given $T$, all imaginable families of sets parametrized by $T$ can be represented by $E\to T$ for some $E$ and some mapping; if "imaginable" is interpreted to mean "definable", an affirmative answer to this question is essentially equivalent (for abstract, constant sets) to the postulation of the so-called "replacement schema", whereas if $\mathcal{S}$ is considered as an object in some larger realm, an affirmative answer means that $\mathcal{S}$ itself has "inaccessible cardinality". However, in view of practice and in view of the role of $\mathcal{S}$ as a limiting case of the general notion of continuously variable sets, it seems appropriate to simply define "an internal-to-$\mathcal{S}$ $T$-parametrized family of objects of $\mathcal{S}$" to mean just a morphism of $\mathcal{S}$ with domain $T$.  [Lawvere (1976, p.121)](#Lawvere76)

See also the remarks on pages 721 and 727 of ([Lawvere 2000](#Lawvere00)).


## Related discussion

* [[Thomas Streicher]], [[William Lawvere]], [[Colin McLarty]] et al, *Categorical formulations of replacement*, March 2008. ([link](http://www.mta.ca/~cat-dist/archive/2008/08-3))

* MO-discussion: _Who needs Replacement anyway ?_  ([link](http://mathoverflow.net/questions/208711/who-needs-replacement-anyway))

* Akihiro Kanamori (2012). _In Praise of Replacement_. The Bulletin of Symbolic Logic 18:1 (2012 March).  [pdf](http://math.bu.edu/people/aki/20.pdf).


## Related entries

* [[Zermelo-Fraenkel set theory]]

* [[reflection principle]]

* [[axiom of choice]]

* [[ETCS]]

* [[large cardinals]]


## References

* {#BellMach77}[[John Bell|J. L. Bell]], M. Machover, *A Course in Mathematical Logic*, North-Holland Amsterdam 1977. (ch. 10, &#167;5)

* {#Cantor99}[[Georg Cantor]], *Brief an Dedekind vom 22. Juli 1899*, pp.443-447 in Cantor, _Gesammelte Abhandlungen_, Springer Berlin 1932.  English transl. pp.113-117 of van Heijenoort (ed.), _From Frege to G&#246;del_ , Harvard UP 1967.

* {#Fraenkel22}A. Fraenkel, *Zu den Grundlagen der Cantor-Zermeloschen Mengenlehre*, Math. Ann. **86** (1922) pp.230-237. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002268760))

* [[Harvey Friedman|H. J. Friedman]], *Higher Set Theory and Mathematical Practice*, Ann. Math. Logic **2** (1971) pp.326-357.

* [[André Joyal]], [[Ieke Moerdijk]], *A categorical theory of cumulative hierarchies of sets*, C. R. Math. Rep. Acad. Sci. Canada **13** (1991) pp.55-58.

* {#Lawvere76}[[F. William Lawvere]], *Variable Quantities and Variable Structures in Topoi*, pp.101-131 in Heller, Tierney (eds.), _Algebra, Topology and Category Theory: a Collection of Papers in Honor of Samuel Eilenberg_ , Academic Press New York 1976.

* {#Lawvere00}[[F. William Lawvere]], *Comments on the development of topos theory*, pp.715-734 in Pier (ed.),  _Development of Mathematics 1950 - 2000_ , Birkh&#228;user Basel 2000. ([tac reprint](http://www.tac.mta.ca/tac/reprints/articles/24/tr24abs.html))

* {#McLarty04}[[Colin McLarty]], *Exploring Categorical Structuralism*, Phil. Math. **12** no.3 (2004) pp.37-53. ([pdf](http://www.cwru.edu/artsci/phil/PMExploring.pdf))

* D. A. Martin, *Borel determinacy*, Ann. Math. **102** (1975) pp.363-371.

* {#Osius74}[[Gerhard Osius]], *Categorical Set Theory: A Characterization of the Category of Sets*, JPAA **4** (1974) pp.79-119.

* [[Thoralf Skolem]], *[[Some remarks on axiomatized set theory|Einige Bemerkungen zur axiomatischen Begründung der Mengenlehre]]*, Mathematikerkongressen i Helsingfor 4-7 Juli 1922. English transl. pp.290-301 of van Heijenoort (ed.), _From Frege to G&#246;del_ , Harvard UP 1967.

* [[Thomas Streicher]], *Universes in Toposes*, pp.78-90 in Crosilla, Schuster (eds.), _From Sets and Types to Topology and Analysis_ , Oxford UP 2005. ([preprint](http://www.mathematik.tu-darmstadt.de/~streicher/NOTES/UniTop.pdf))

* [[Paul Taylor]], *[[Practical Foundations of Mathematics]]*, Cambridge UP 1999. (ch. 9)

* George Tourlakis, *Lectures in Logic and Set Theory*, Volume 2: _Set Theory_, Cambridge University Press (2003). (section III.8)


[[!redirects axiom of replacement]]
[[!redirects axioms of replacement]]
[[!redirects axiom scheme of replacement]]
[[!redirects axiom schemes of replacement]]
[[!redirects axiom schema of replacement]]
[[!redirects axiom schemas of replacement]]
[[!redirects axiom schemata of replacement]]
[[!redirects replacement axiom]]
[[!redirects replacement axioms]]
[[!redirects replacement axiom scheme]]
[[!redirects replacement axiom schemes]]
[[!redirects replacement axiom schema]]
[[!redirects replacement axiom schemas]]
[[!redirects replacement axiom schemata]]

[[!redirects axiom of collection]]
[[!redirects axioms of collection]]
[[!redirects axiom scheme of collection]]
[[!redirects axiom schemes of collection]]
[[!redirects axiom schema of collection]]
[[!redirects axiom schemas of collection]]
[[!redirects axiom schemata of collection]]
[[!redirects collection axiom]]
[[!redirects collection axioms]]
[[!redirects collection axiom scheme]]
[[!redirects collection axiom schemes]]
[[!redirects collection axiom schema]]
[[!redirects collection axiom schemas]]
[[!redirects collection axiom schemata]]


category: foundational axiom
