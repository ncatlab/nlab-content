#Idea#

The axioms of a _semi-abelian_ category are supposed to capture the properties of the categories of [[group]]s, [[ring]]s without unit, [[algebra]]s without unit, Lie algebras, as nicely as the axioms of an [[abelian category]] captures the properties of the category of abelian groups and of modules.

+--{: .query}
[[Mike Shulman|Mike]]: Why only rings without units (that is, rngs)?  Intuitively, what important properties do the above listed examples share that are not shared by rings with units?

[[Zoran Skoda]]: I want to know the answer as well. It might be something in the self-dual axioms. For unital rings artinian implies noetherian but not other way around; though the definitions of the two notions are dual.

_Toby_:  The category of unital rings and unitary ring homomorphisms has no zero object.

[[Mike Shulman|Mike]]: Ah, right.  Is it protomodular?  I think I will understand this definition better from some non-examples that violate each clause individually.
=--


#Definition#

A [[category]] $C$ is **semi-abelian** if it

* is [[exact category|Barr-exact]] (hence [[regular category|regular]] and in particular has finite [[limit]]s);

* has a [[zero object]];

* has finite [[coproduct]]s; and

* is [[Bourn-protomodular category|Bourn-protomodular]].

+--{: .query}
[[Mike Shulman|Mike]]: I was about to create the link to Bourn-protomodular category, but then I wondered whether we should just say "protomodular"---is there a reason to disambiguate it with the prefix "Bourn-"?  We (sometimes) say "Barr-exact" to avoid confusion with [[Quillen exact category|Quillen-exact]]; is there any ambiguity for "protomodular?"

[[Zoran Skoda]]: I think not, I saw just one notion of protomodular so far (unlike word semi-abelian which has been  used for some other things, mainly before the now accepted dominant notion); besides the notion is mainly used by one and the same community (unlike word exact category which lives with different meanings in completely different societies of mathematicians). I think no need to call it Bourn-protomodular; of course the entry should have pointers to the original references and short mention of the optional modifier, I think. 
=--

Equivalently, $C$ is semi-abelian if:

* it has finite products and coproducts and a [[zero object]];

* it has [[pullback]]s of [[monomorphism]]s (or even only of [[split monomorphism]]s);

* it has [[coequalizer]]s of [[kernel pair]]s;

* [[regular epimorphism]]s are stable under [[pullback]];

* [[congruence|equivalence relations]] are effective; and

* the _Split Short Five Lemma_ holds: given a commutative diagram
$$\array{L & \overset{l}{\to} & F & \overset{q}{\to} & C\\
  ^u\downarrow && \downarrow^w && \downarrow^v \\
  K & \underset{k}{\to} & E& \underset{p}{\to} & B}$$
where $p$ and $q$ are [[split epimorphism]]s and $l$ and $k$ are their [[kernel]]s, if $u$ and $v$ are [[isomorphism]]s then so is $w$.

To see that the second list of axioms implies the existence of finite limits, observe that the pullback
$$\array{P & \to & A\\
  \downarrow && \downarrow^f\\
  B& \underset{g}{\to} & C}$$
can be computed as the pullback
$$\array{P & \to & A\times B\\
  \downarrow && \downarrow^{(1,1,f)}\\
  A\times B& \underset{(1,1,g)}{\to} & A\times B\times C}$$
in which both legs are split monics.  Filling in one of the equivalent definitions of Barr-exactness, the equivalence of the two lists of axioms reduces to showing that in a Barr-exact category with coproducts and a zero object, protomodularity is equivalent to the Split Short Five Lemma; see the paper referenced below for a proof.


#Remarks#

* In its most general form, the [[Dold-Kan correspondence]] holds for [[simplicial object]]s in semi-abelian categories.


#Examples#

* Every [[abelian category]] is semi-abelian.  Conversely, a semi-abelian category is abelian if and only if it is [[additive category|additive]] (since any exact additive category is abelian), and if and only if its opposite is semi-abelian.

* The category [[Grp]] of not-necessarily-abelian [[group]]s is semi-abelian but not [[abelian category|abelian]].  So are the categories of rings without units, algebras without units, Lie algebras, and many other sorts of algebras.  (The category of rings with unit is not semi-abelian since it lacks a zero object.)

* More generally, the category of internal [[group object]]s in any exact category is semi-abelian as soon as it has finite coproducts.  For instance, this applies to internal groups in any [[topos]] with a [[natural numbers object|NNO]].

* The opposite of any [[topos]], such as $Set^{op}$, is Barr-exact and protomodular, but obviously lacks a zero object.

* The category of Heyting semilattices

* The category of (ordinary) Lie algebras

* The category $Set_*$ of [[pointed set]]s is Barr-exact with finite coproducts and a zero object, but is not semi-abelian: protomodularity and the Split Short Five Lemma fail to hold.

* If $C$ is exact and protomodular with finite colimits, then for any $x\in C$ the [[over category|over]]-[[under category|under]] category $(x/C/x)$ is semi-abelian.  For example, the opposite of the category of [[pointed object|pointed objects]] in a [[topos]] is semi-abelian, and in particular, $Set_*^{op}$ is semi-abelian.

+-- {: .query}

[[Urs Schreiber|Urs]]: how can I understand that this (has to?) involve the opposite category?

[[Mike Shulman|Mike]]: Well, as the previous example shows, $Set_*$ itself is not semi-abelian.  The way I'm thinking of it is that a surjection of pointed sets is not determined by its kernel, but an injection of pointed sets is determined by its cokernel.

=--


* The categories of [[crossed module|crossed modules]], [[crossed complex]]es, and their friends are semi-abelian; see example 2.6(4) of the paper referenced below.


#References#


* George Janelidze, L&#225;szl&#243;e M&#225;rki, Walter Tholen, _Semi-Abelian Categories_ ([web](http://citeseer.ist.psu.edu/old/janelidze00semiabelian.html))

* Dominique Bourn, Francis Borceux, _Mal'cev, protomodular, homological and semi-abelian categories_, Kluwer 2004.

[[!redirects semiabelian category]]
[[!redirects semiabelian categories]]
[[!redirects semi-abelian categories]]