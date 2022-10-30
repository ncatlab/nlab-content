
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An __$H$-space__ ("H" for [[Heinz Hopf|Hopf]], as in _[[Hopf construction]]_) is a [[magma]] in the [[homotopy category]] of [[topological spaces]] [[Ho(Top)]], or in the homotopy category category $Ho(Top)_*$ of pointed spaces,  which has a [[unit]] up to [[homotopy]]. 


An **$H$-monoid** is a [[monoid object]] in [[Ho(Top)]], hence an $H$-space is an $H$-monoid if the product of the magma is [[associativity|associative]] up to [[homotopy]]. 

An __$H$-group__ is a [[group object]] in [[Ho(Top)]], so an $H$-monoid is an $H$-group if has also a [[inverses]] up to homotopy.

To continue in this pattern, one could say that an **H-category** is an [[Ho(Top)]]-[[enriched category]].

Notice that here the homotopies for units, associativity etc. are only required to _exist_ for an H-space, not required to be equipped with higher [[coherence|coherent]] homotopies. An $H$-monoid equipped with such higher and coherent homotopies  is instead called a _strongly homotopy associative_ space or  _$A_\infty$-[[A-infinity space|space]]_ for short.  If it has only higher homotopies up to level $n$, it is called an $A_n$-[[A-n space|space]].

A better name for an $H$-space might be be $H$-[[unitoid]], but it is rarely used. The $H$ stands for [[Heinz Hopf]], and reflects the sad fact that the natural name 'homotopy group' was [[homotopy group|already occupied]]; Hopf and A. Borel found necessary algebraic conditions for a space to admit an $H$-space structure.

There are dual notions of $H$-counitoid (or $H'$-space, or [[co-H-space]]), $H$-comonoid (or $H'$-monoid) and $H$-[[cogroup]] (or $H'$-group) having co-operations with the usual identities up to homotopy. 

## Examples

The main example of an $H$-group is the [[loop space]] $\Omega X$ of a space $X$, which however is naturally even an [[A-infinity space]]. 

(The main example of an [[co-H-space|H-cogroup]] in $Top_*$ is the [[suspension]] $S X= S^1\wedge X$ of a pointed topological space $X$. )

The only [[n-spheres]] $S^n$ which have $H$-space structure are those for $n = 0,1,3,7$, and their H-space structure is given by identifying them as the unit spheres in one of the four [[normed division algebras]] ([[real numbers]], [[complex numbers]], [[quaternions]], [[octonions]]) and taking the product to be that induced by the algebra product. 

An example of an H-space that does not lift to an [[A-infinity space]] is the [[7-sphere]] $S^7$. It can't be delooped because its [[delooping]] would have [[cohomology group]] a [[polynomial ring]] on a generator in degree 8, and this is impossible by mod $p$ [[Steenrod operations]] for any odd $p$. The 7-sphere is also not an $H$-group.

If $K$ is an $H$-group then for any topological space $X$, the set of [[homotopy classes]] $[X,K]$ has a natural group structure in the strict sense; analogously if $K'$ is an $H$-cogroup then $[K',X]$ has a group structure. If there is more than one $H$-group structure on a space, then the induced group structures on the set of homotopy classes coincide. 

If an $H$-space is equivalent to a [[delooping|deloopable one]], then it is a [[groupoid object in an (infinity,1)-category|group object in the (∞,1)-category]] [[Top]]. In other words, in that case, the associativity and other axioms hold up to **coherent homotopy**. 

For more details see at [[loop space]].

## Properties

### Relation to $A_\infty$-spaces

Given an [[A-∞ space]] in the [[(∞,1)-category]] [[∞Grpd]]/[[Top]], its image in the corresponding [[homotopy category of an (∞,1)-category]] [[Ho(Top)]] in an $H$-space. Conversely, refining an H-space to a genuine $A_\infty$-space means lifting the structure of a [[monoid object in an (∞,1)-category]] from the [[homotopy category of an (∞,1)-category|homotopy category]] [[Ho(Top)]] to the genuine [[(∞,1)-category]] [[∞Grpd]]/[[Top]].

Further discussion of this is also at _[loop space -- Homotopy associative structure](loop+space#AInfinityStructure)_

## Related concepts

* [[topological monoid]]

* [[group completion]]

## References

Introduction and survey includes

* {#Arkowitz11} [[Martin Arkowitz]], _H-Spaces and Co-H-Spaces_, chapter 2 in _Introduction to homotopy theory_, Springer 2011 ([pdf](file:///C:/Users/Sony/Downloads/9781441973283-c1.pdf))

The terminology $H$-space is a definition in a Chapter IV, Section 1 (dedicated to loop spaces) of 

* [[Jean-Pierre Serre]], _Homologie singuli&#232;re des espaces fibr&#233;s. Applications._, Ann. Math. __54__ (1951), 425--505. 

Some other papers in the 1950s include

* [[Edwin Spanier]], [[Henry Whitehead]], _On fibre spaces in which the fibre is contractible_, Comment. Math. Helv. __29__, 1955, 1--8.

* Arthur H. Copeland, _On $H$-spaces with two nontrivial homotopy groups_, Proc. AMS __8__, 1957, 109--129.

* M. Sugawara:
  * _$H$-spaces and spaces of loops_, Math. J. Okazama Univ, __5__, 1955, 5--11;
  * _A condition that a space is an $H$-space_, Math. J. Okayama Univ. __6__, 1957, 109--129;
  * _A condition that a space is group-like_, Math. J. Okayama Univ. __7__, 1957, 123--149.

* F. I. Karpelevi&#269;, A. L. Oni&#353;&#269;ik, _Algebra of homologies of space of paths_, Dokl. Akad. Nauk. SSSR, (N.S.), 106 (1956), 967--969. MR0081478

The theory of $H$-spaces was widely established in the 1950s and studied by Serre, Postnikov, Spanier, Whitehead, Dold, Eckmann and Hilton and many others. 

The deloopable case has more coherent structure which has been discovered few years later in J. Stasheff's thesis and published in

* [[Jim Stasheff]], _Homotopy associative $H$-spaces I, II_, Trans. Amer. Math. Soc. 108, 1963, 275-312 

For a historical account see

* John McCleary, _An appreciation of the work of Jim Stasheff_ ([pdf](http://www.math.unc.edu/Faculty/jds/jds.pdf))

The description in terms of [[groupoid object in an (∞,1)-category]] is due to 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

see last remark of section 6.1.2 .

Wikipedia\'s definition (at time of this writing, and phrased in the language of [[homotopy theory]]) is rather a [[unitoid]] object in the $(\infty,1)$-category [[Top]].

* MathOverflow: [homotopy-associative-h-space-and-coh-space](http://mathoverflow.net/questions/16711/homotopy-associative-h-space-and-coh-space)

See also

* [[John Adams]], _Finite $H$-Spaces and Lie groups_, Journal of Pure and Applied Algebra 19 (1980) 1-8 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/adamse8.pdf))

[[!redirects H-spaces]]

[[!redirects H-monoid]]
[[!redirects H-monoids]]

[[!redirects H-group]]
[[!redirects H-groups]]

[[!redirects H-category]]
[[!redirects H-categories]]


[[!redirects H-unitoid]]
[[!redirects H-cogroup]]
[[!redirects H-comonoid]]


