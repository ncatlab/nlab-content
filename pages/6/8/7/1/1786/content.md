
An __$H$-space__ is a [[magma]] in the category of topological spaces $Top$, or in the category $Top_*$ of pointed spaces,  which has a unit up to homotopy. An $H$-space is an __$H$-monoid__ if the product of the magma is associative up to homotopy, and an __$H$-group__ if it has also an inverse up to homotopy.

A better name for an $H$-space would be $H$-[[unitoid]], but it is rarely used. The $H$ stands for [[Heinz Hopf]], and reflects the sad fact that the natural name 'homotopy group' was [[homotopy group|already occupied]]; Hopf and A. Borel found necessary algebraic conditions for a space to admit an $H$-space structure.

+-- {: .query}
Does 'unitoid' generically mean a magma with identity?  I can\'t verify this, but it would be convenient to have such a term.  ---Toby

Good question. Postnikov in his 1980-s course of homotopy theory, talks about internal unitoids in a fixed category before modifying the notion to H-version; however he does complaint that in the universal algebra the term is not standardized. -- Zoran

Thanks, that\'s something to start with at least.  ---Toby
=--

The main example of an $H$-group is the [[loop space]] $\Omega X$ of a space $X$. There are dual notions of $H$-counitoid (or $H'$-space, or co-$H$-space), $H$-comonoid (or $H'$-monoid) and $H$-[[cogroup]] (or $H'$-group) having co-operations with the usual identities up to homotopy. The main example of an $H$-cogroup in $Top_*$ is the [[suspension]] $S X= S^1\wedge X$ of a pointed topological space $X$. 

If $K$ is an $H$-group then for any topological space $X$, the set of homotopy classes $[X,K]$ has a natural group structure in the strict sense; analogously if $K'$ is an $H$-cogroup then $[K',X]$ has a group structure. If there is more than one $H$-group structure on a space, then the induced group structures on the set of homotopy classes coincide. 

If an $H$-space is equivalent to a [[delooping|deloopable one]], then it is a [[groupoid object in an (infinity,1)-category|group object in the (∞,1)-category]] [[Top]]. In other words, in that case, the associativity and other axioms hold up to **coherent homotopy**. 

For more details see 

* [[loop space]].


#References#

The terminology $H$-space is a definition in a Chapter IV, Section 1 (dedicated to loop spaces) of 

* J. P. Serre, _Homologie singuli&#232;re des espaces fibr&#233;s. Applications._, Ann. Math. __54__ (1951), 425--505. 

Some other papers in the 1950s include

* E. H. Spanier, J. H, C, Whitehead, _On fibre spaces in which the fibre is contractible_, Comment. Math. Helv. __29__, 1955, 1--8.

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

* [[Jacob Lurie]], [[Higher Topos Theory]]

see last remark of section 6.1.3 .

Wikipedia\'s definition (at time of this writing, and phrased in the language of [[homotopy theory]]) is rather a [[unitoid]] object in the $(\infty,1)$-category [[Top]].


[[!redirects H-spaces]]
[[!redirects H-monoid]]
[[!redirects H-group]]
[[!redirects H-unitoid]]
[[!redirects H-cogroup]]
[[!redirects H-comonoid]]