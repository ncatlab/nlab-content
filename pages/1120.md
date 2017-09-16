#Definition#

A [[category]] $C$ with a class of [[morphism]]s $W$ is said to admit a **category of right fractions** if

* $W$ is a [[wide subcategory]] of $C$
* Given an arrow $v:x\to z$ in $W$ and any arrow $f: y\to z$, there is an arrow $v':w \to y$ in $W$ and an arrow $f':w \to x$ in $C$ such that
$$
\begin{matrix}
  w& \stackrel{f'}{\to} & x \\
  v' \downarrow&&\, \downarrow v\\
  y &\underset{f}{\to} & z
\end{matrix}
$$
commutes
* Given an arrow $v:x\to y$ in $W$ and a pair of [[parallel morphisms]] $f,g: y\to z$ such that $f\circ v = g \circ v$, there is an arrow $v':w\to x$ in $W$ such that $v'\circ f = v' \circ g$.

If the above conditions hold, then the [[hom-set]]s of the [[localization]] of $C$ at $W$ are given by equivalence classes of [[span|spans]].

#Remarks#

* This definition has a [[duality|dual]] version, a category of left fractions. Then the [[hom-set]]s are equivalence classes of [[cospan]]s.


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
=--
