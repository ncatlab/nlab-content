#Idea#

The axioms of a _semi-abelian_ category are supposed to capture the properties of the categories of [[group]]s, [[ring]]s, [[algebra]]s as nicely as the axioms of an [[abelian category]] captures the properties of the category of abelian groups and of modules.


#Definition#

A [[category]] $C$ is **semi-abelian** if it

* has a [[zero object]];

* has finite [[coproduct]]s

* is [[exact category|Barr-exact]];

* is [[Bourn-protomodular]].

Equivalently, a [[category]] $C$ is **semi-abelian** if

* it has a [[zero object]];

* it has [[pullback]]s of (split) [[monomorphism]]s;

* it has [[coequalizer]]s of [[kernel pair]]s;

* [[regular epimorphism]]s are stable under [[pullback]];

* [[congruence|equivalence relations]] are effective.

+--{: .query}
[[Mike Shulman|Mike]]: Can someone explain more about why those are equivalent?  How does the second set of axioms imply the existence of finite limits and finite coproducts?
=--

#Remarks#

* In its most general form, the [[Dold-Kan correspondence]] holds for simplicial objects in semi-abelian categories.

+--{: .query}
[[Urs Schreiber|Urs]]: Or so [[Tim Porter|Tim]] seemed to indicate. It would be nice to have more details on this statement.

[[Tim Porter|Tim]]: The reference is

D. Bourn, 2007, Moore normalisation and Dold-Kan theorem for semi-Abelian categories , in 
Categories in algebra, geometry and mathematical physics , volume 431 of Contemp. Math., 
105 &#8211; 124, Amer. Math. Soc., Providence, RI.

Dominique's formulation is very pretty. The Moore complex functor is monadic when the basic category is semi-Abelian (Th. 1.4. p.113) Of course for simplicial GROUPS, the  monad on chain complexes f groups gives the hypercrossed complexes of Carrasco and Cegarra, but here they fall out from the theory.  On the down side there is no analysis as yet of the actual form of this monad as far as I know.  I may be wrong. There is a beginning of such a thing in the paper.

=--



#Examples#

* Every [[abelian category]] is semi-abelian.

* The category [[Grp]] of [[group]]s (not just abelian groups) is semi-abelian but not [[abelian category|abelian]].



#References#


* George Janelidze, L&#225;zl&#243;e M&#225;rki, Walter Tholen, _Semi-Abelian Categories_ ([web](http://citeseer.ist.psu.edu/old/janelidze00semiabelian.html))