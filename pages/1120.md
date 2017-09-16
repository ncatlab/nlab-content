#Definition#

A pair $(C,W)$ of a [[category]] $C$ and a class of [[morphism]]s $W$ is said to be a **calculus of right fractions** or a **right Ore system** (in $C$) or to **admit a category of right fractions** if

* it is a [[wide subcategory]] of $C$ (= $W$ contains all identities of $C$; for localization conditions without loss of generality one may add a stronger condition: $W$ contains all isomorphisms in $C$) 
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

If the above conditions hold, then a [[localization]] of $C$ at $W$ can be realized by taking the same objects as in $C$
and the [[hom-set]] $C[W^{-1}](a,b)$ is realized by equivalence classes of [[span|spans]] whose left leg is in $W$: $a\stackrel{v}\leftarrow a'\stackrel{f}\rightarrow b$ is equivalent to $a\stackrel{w}\leftarrow a''\stackrel{g}\rightarrow b$ iff there exists $\bar{a}$
and morphisms $s:\bar{a}\to a'$, $t:\bar{a}\to a''$ such that $f\circ s = g\circ t$ and $v\circ s = w\circ t$. The equivalence class of $a\stackrel{v}\leftarrow a'\stackrel{f}\rightarrow b$ is simply denoted by $f\circ v^{-1}$. 

The equivalence classes compose as follows: take a representative $a\stackrel{v}\leftarrow a'\stackrel{f}\rightarrow b$
and representative  $b\stackrel{u}\leftarrow b'\stackrel{h}\rightarrow c$; then by the Ore condition
there exist morphism $z:d\to a'$ and $k:d\to b'$ where $z\in  W$ such that $f\circ z= u\circ k$. 
The composition $(k\circ u^{-1})\circ (f\circ v^{-1})$ is the equivalence class of the span
$a\stackrel{v\circ z}\leftarrow d\stackrel{h\circ k}\rightarrow c$. One proves that this definition does not depend on the choice of representatives, and that it is associative with units $1_a\circ 1^{-1}_a$. The localization functor sends a morphism $p : a\to b$ to $p\circ 1^{-1}_a$.

#Remarks#

* This definition has a [[duality|dual]] version, a category of left fractions. Then the [[hom-set]]s are equivalence classes of [[cospan]]s (spans in opposite category). More precisely, the localization $W^{-1}C$ of $C$ at the calculus of left fractions $(C,W)$ may be realized 
as the opposite category $(C^{\mathrm{op}}[(W^{\mathrm{op}})^{-1}])^{\mathrm{op}}$
to the localization of the opposite category $C^{\mathrm{op}}$ at the calculus of right fractions $(C^{\mathrm{op}},W^{\mathrm{op}})$ 
(hence two dualizations are involved).

+--{+ .query}
[[Zoran Škoda]] 
I just had a discussion with Urs, where he pointed to the usual picture with another view of double dualization, taking indeed cospans but RIGHT ones. But this is the same as taking one more dualization as I explained before. So
I will give up on complaining to cospans, it is OK if one understands it as doing both dualizations simultaneously (left vs right leg and span vs cospan). Simialrly in ring theory right Ore localization is obtained by taking the opposite of left Ore localizations in the opposite ring. In any case TWO dualizations are involved. Otherwise we would get opposite category as localization at trivial Ore system. 

By the way, GZ call left what we call right and other way around, the convention here is the one generalizing the ring theory convention where composition is multiplication in the usual order. I do not know what to do about it. The entry [[multiplicative system]] has left what is here right. 
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

[[Zoran Škoda]]: I did not say that "all Gabriel style localisations of rings are called rings of fractions", but on the other hand, it is not reserved for Ore construction 
only (you have zillions of other constructions, for example Martindale ring of fractions). I just said that in th ering theory "extending the distinction between 'fractions' and 'rational numbers' " is already not customary, and in category setup it will be even further from this hypercorrection. I think it is common and sensible to distinguish between general localized category and category of fractions when introducing the concepts. In practice, most of the time we use the case with Ore conditions; I personally in papers/applications always write localization, never the long terms in special cases, but if I teach I will teach with making the distinctions. 

[[Mike Shulman|Mike]]: Would anyone object to the following course of action?

1. Create [[calculus of fractions]] which combines the current contents of this page with those of [[multiplicative system]].
1. Make this page say "A category of fractions is a [[localization]] that is constructed using a [[calculus of fractions]]."
1. Make [[multiplicative system]] be about multiplicative systems in rings, with a comment that it is occasionally used to mean a [[calculus of fractions]].
=--
