# Axioms of replacement and collection
* table of contents
{: toc}

## Idea

>_Zwei &#228;quivalente Vielheiten sind entweder beide 'Mengen' oder beide inkonsistent._ [[Georg Cantor]] (1899)[^Cant]

[^Cant]: _'Two equivalent multiplicities either are both "sets" or are both inconsistent'_, letter to Dedekind from 28th July 1899 ([Cantor 1932](#Cantor99), p.444). This is suggested as an early formulation of the axiom of replacement by van Heijenoort (1967, p.113).

The **axiom of replacement** is an axiom scheme of [[Zermelo-Fraenkel set theory]] that was suggested by A. Fraenkel and formulated by [[Thoralf Skolem|T. Skolem]] in 1922. Given a unary operation $F$ and a set $x$ it permits to collect all $F(y)$ for $y\in x$ into a new set.

Similar processes of collection and the resulting axioms of replacement occur elsewhere in [[set theory]] where they are seen as a part of the 'strong' axioms. The resulting expansiveness of the set-theoretic universe is somewhat peripheral to the practice of 'ordinary' mathematics and therefore a [[structural set theory]] like [[ETCS]] can omit replacement without incurring a great loss[^etcs]. Even in the context of a ZF-equivalent material set theory the axiom of replacement can be treated in for a [[reflection principle]] (cf. [Bell-Machover 1977](#BellMach77), p.495).

[^etcs]: It is possible, however, to augment an ETCS-like categorical set theory with a version of replacement if necessary as shown in ([Osius 1974](#Osius74), section 9) resulting in a system with the full strength of ZF.

Axioms of replacement and collection become useful, however, whenever [[recursion|recursively]] constructing a set that is 'larger' than any set known before e.g. for the construction of [[large cardinal|large cardinals]]. 

There are many variations on these axiom schemata, but any given system should only need one.


## Statements

In general, these axioms apply to a [[binary relation]] that relates elements of one [[set]] $A$ to arbitrary sets.  However, we do *not* expect that the relation itself be an object in the theory; really, we have an axiom schema with one axiom for every binary [[predicate]] of the proper form.  We will write this predicate as $\phi(x,Y)$, where $x$ stands for an elment of $A$ and $Y$ stands for any set.  (Note that there may well be other free variables in the predicate.)

Generally, $\phi$ will need to be an [[entire relation]] for the axiom to apply; that is, the axiom has as a hypothesis that, for every $x \in A$, there is some $Y$ such that $\phi(x,Y)$ holds.  In versions called 'replacement' instead of 'collection', $\phi$ also needs to be [[functional relation|functional]]; that is, the axiom has the hypothesis that, for every $x \in A$, there is a *unique* $Y$ such that $\phi(x,Y)$ holds.  Thus, most of the 'replacement' versions only make sense if the language has a notion of [[equality]] of sets.

So much for the hypothesis of the axiom; the conclusion asserts the existence of a [[family of sets]] to which appropriate $Y$s belong.  In a material set theory, we can simply state the existence of set $\mathcal{F}$ such that certain $Y \in \mathcal{F}$.  In a structural set theory, we state the existence of an index set $I$, a total set $E$, and a function $f\colon E \to I$ such that each [[fibre]] $f^*(x)$ for $x \in I$ is equal to (or at least isomorphic to) certain $Y$.  (Often we can take $I$ to be $A$, but that does not come into the statement of the axioms.)

...

## Related entries

* [[Zermelo-Fraenkel set theory]]

* [[reflection principle]]

* [[axiom of choice]]

* [[ETCS]]

## References

* MO-discussion: _Who needs Replacement anyway ?_ . ([link](http://mathoverflow.net/questions/208711/who-needs-replacement-anyway))

* {#BellMach77}[[John Bell|J. L. Bell]], M. Machover, _A Course in Mathematical Logic_ , North-Holland Amsterdam 1977. (ch. 10,&#167;5)

* {#Cantor99}[[Georg Cantor]], _Brief an Dedekind vom 22. Juli 1899_ , pp.443-447 in Cantor, _Gesammelte Abhandlungen_ , Springer Berlin 1932.  English transl. pp.113-117 of van Heijenoort (ed.), _From Frege to G&#246;del_ , Harvard UP 1967.

* A. Fraenkel, _Zu den Grundlagen der Cantor-Zermeloschen Mengenlehre_ , Math. Ann. **86** (1922) pp.230-237. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002268760))

* [[André Joyal]], [[Ieke Moerdijk]], _A categorical theory of cumulative hierarchies of sets_, C. R. Math. Rep. Acad. Sci. Canada **13** (1991) pp.55-58.

* {#Osius74}[[Gerhard Osius]], _Categorical Set Theory: A Characterization of the Category of Sets_ , JPAA **4** (1974) pp.79-119.

* [[Thoralf Skolem]], _Einige Bemerkungen zur axiomatischen Begr&#252;ndung der Mengenlehre_ , Mathematikerkongressen i Helsingfor 4-7 Juli 1922. English transl. pp.290-301 of van Heijenoort (ed.), _From Frege to G&#246;del_ , Harvard UP 1967.

* George Tourlakis, _Lectures in Logic and Set Theory, Volume 2: Set Theory_, Cambridge University Press (2003). (section III.8)


[[!redirects axiom of replacement]]
[[!redirects axioms of replacement]]
[[!redirects axiom scheme of replacement]]
[[!redirects axiom schemes of replacement]]
[[!redirects axiom schema of replacement]]
[[!redirects axiom schemas of replacement]]
[[!redirects axiom schemata of replacement]]

[[!redirects axiom of collection]]
[[!redirects axioms of collection]]
[[!redirects axiom scheme of collection]]
[[!redirects axiom schemes of collection]]
[[!redirects axiom schema of collection]]
[[!redirects axiom schemas of collection]]
[[!redirects axiom schemata of collection]]

category: foundational axiom
