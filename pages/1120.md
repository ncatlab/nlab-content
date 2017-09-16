#Definition#

A [[category]] $C$ with a class of [[morphism]]s $W$ is said to admit a **category of right fractions** if

* $W$ is a [[wide subcategory]] of $C$
* (right Ore condition) Given an arrow $v:x\to z$ in $W$ and any arrow $f: y\to z$, there is an arrow $v':w \to y$ in $W$ and an arrow $f':w \to x$ in $C$ such that
$$
\begin{matrix}
  w& \stackrel{f'}{\to} & x \\
  v' \downarrow&&\, \downarrow v\\
  y &\underset{f}{\to} & z
\end{matrix}
$$
commutes
* (right cancelability) Given an arrow $v:x\to y$ in $W$ and a pair of [[parallel morphisms]] $f,g: y\to z$ such that $f\circ v = g \circ v$, there is an arrow $v':w\to x$ in $W$ such that $v'\circ f = v' \circ g$.

If the above conditions hold, then the [[hom-set]]s of the [[localization]] of $C$ at $W$ are given by equivalence classes of [[span|spans]].

#Remarks#

* This definition has a [[duality|dual]] version, a category of left fractions. Then the [[hom-set]]s are equivalence classes of [[cospan]]s.

+--{+ .query}
[[Zoran Škoda]] NO !!! This is NOT called category of left fractions.

Still the hom sets are spans, NOT cospans!!! The question is which leg of the span is in Ore system and which is general (that is which is denominator and which is denumerator), and accordingly for equivalence relation and so on.

The left Ore condition IS dual to right Ore condition (left Ore in a dual category). However you have to
use the rule from quantum mechanics for operators if you want to get the correct answer for category of fractions. 
That is conjugate $A$ to $D^{-1}AD$. That is dualize, perform the category of fractions and then dualize back the answer! Otherwise, with cospans, you would get that the localization functor is contravariant! In particular if you take the trivial left Ore system, with cospans the "localization" would be just taking opposite category, and the system which is simultenously left and right Ore would give nonunique answer!
=--


#References#

The above definition is due to Gabriel-Zisman in the book 

* Gabriel-Zisman, _Calculus of fractions and homotopy theory_



+-- {: .query}

[[Urs Schreiber|Urs]]: there is overlap/duplication here with the entry [[multiplicative system]]. The only difference in the axioms seems to be that in a [[multiplicative system]] all isomorphisms are required to be included.

we should probably merge the entries and make one a redirect to the other, or something -- any opinions?

[[Mike Shulman|Mike]]: The definition above is what I am accustomed to call a *calculus* of (left/right) fractions.  I thought the *category* of fractions referred to the resulting localization $C[W^{-1}]$.

Regarding terminology, in my experience "calculus of fractions" is the more common term.  I've never seen "multiplicative system" anywhere except Kashiwara-Schapira.  (People with differing experiences, please speak up.)  "Multiplicative system" sounds to me just like something that is closed under multiplication, which is precisely what it means in commutative ring theory.  I don't know anything about noncommutative ring theory, but this [wikipedia page](http://en.wikipedia.org/wiki/Ore_condition), at least, still uses "multiplicative" for "closed under multiplication" in the noncommutative case, with "right denominator set" for the calculus-of-fractions-like condition.


[[Tim Porter|Tim]]:  My experience is very much the same as Mike's. Note however the word 'admits' in the definition. I think Gabriel and Zisman chose the terminology very carefully so that $C[W^{-1}]$ is the localised category, but is not really 'the category of fractions'. They are extending the distinction between 'fractions' and 'rational numbers' that we often forget in causal speech. We should, perhaps,  use 'calculus' as Mike suggests. 

I should also point out that the dual notion gives the construction (as equivalence classes of cospans) not the universal property. That seems slightly 'evil' to me!

[[Zoran Škoda]]: Category of fractions is a particular case and construction of general "localized category". Mike is abolutely right, the outcome can be called category of fractions but not the data to start with! The initial data 
are "right calculus of fractions" or "calculus of right fractions".

On the other hand the standard definition says that all isomorphism are included, not that it is 
"wide subcategory" (by the way not a word used by practical
matematicians in algebra and homological algebra who are main practioners of categories of fractions). Multiplicative system for me could be (i say could be as it is not very standard but of occasional use) when both right and left Ore conditions) are satisfied, though this is not very in agreement with ring theory where a multiplicative set is just a set closed under multiplication (in agreement with wikipedia entry as Mike pointed out: as a person with several years of research in localization theory within ring theory I confirm this as absolutely standard) and an Ore subset in a ring is a multiplicative set  satisfying left and right Ore conditions (when I say plural in "conditions" I mean both the Ore condition and cancelability. As far as the difference between fractions and rational numbers as Tim pointed out, this is nice to have in mind, but it is not very customary in usage of categories. The ring theorists use term "ring of fractions" for all possible generalizations of classical passage from Z to Q, and this is absolutely standard in ring theory, so a resurrection of extreme care in category theory where a difference between skeletal category and a category is rarely important or appreciated would be a hypercorrection. 

[[Tim Porter|Tim]]: My point got lost there somehow. 

There are many constructions of the localised category $C[W^{-1}]$, (for instance one by Bauer and Dugundji a long time ago).  The G-Z notion allows one to calculate with fractions (i.e. spans or cospans) rather than with the long complicated zig-zags. The situation therefore admits a \emph{calculus} of fractions, as it allows \emph{calculation}. Then in that situation and almost that one only when all zig-zags reduce to spans or cospans is the localised category really a category of fractions. (There are other versions of a reduction to fractions which are also used of course, and they again do yield something that deserves to be called a 'category of fractions'. 

I do not think that all Gabriel style localisations of  rings are called rings of fractions.  I seem to remember that this was reserved for those contexts in which Ore-like conditions allowed one to work with generalised fractions as such. My vote would be to use Gabriel-Zisman style terminology, as near as possible, as that was strongly influenced by Gabriel's earlier work on localisations of abelian ctegories (and related stuff in topos theory).
=--
