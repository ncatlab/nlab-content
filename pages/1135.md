
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


# Semiabelian categories
* table of contents
{: toc}

## Idea

The notion of _semi-abelian category_ is supposed to capture the properties of [[categories]] such as that of [[groups]], [[rng|rings without unit]], [[associative algebras]] without [[unit]], [[Lie algebras]], etc.; in generalization of how the notion of _[[abelian categories]]_ captures the properties of the categories of [[abelian groups]] and of [[modules]], etc.

\begin{remark}
Here it is important to consider rings and algebras without [[unit]] (really: not necessarily having a [[unit]]), since otherwise there is no [[zero object]], and also to allow [[ideals]] to appear as subrings-without-unit. 

Note that the category of rings with unit  is still [[protomodular category|protomodular]].
\end{remark}




## Definition

A [[category]] $C$ is **semi-abelian** if it

* is [[exact category|Barr-exact]] (hence [[regular category|regular]] and in particular has [[finite limits]]);

* has a [[zero object]];

* has [[finite product|finite]] [[coproducts]]; and

* is [[protomodular category|protomodular]].

In other words, it is a [[homological category]] which is [[Barr-exact]] and has finite [[coproducts]].


Equivalently, $C$ is semi-abelian if:

* it has finite [[product]]s and [[coproduct]]s and a [[zero object]];

* it has [[pullback]]s of [[monomorphism]]s (or even only of [[split monomorphism]]s);

* it has [[coequalizer]]s of [[kernel pair]]s;

* [[regular epimorphism]]s are stable under [[pullback]];

* [[congruence|equivalence relations]] are effective; and

* the _Split Short [[five lemma|Five Lemma]]_ holds: 

+-- {: .un_defn #SplitShortFiveLemma}
###### Definition
**(split short five lemma)**

Given a [[commutative diagram]]

$$
 \array{
    L & \overset{l}{\to} & F & \overset{q}{\to} & C
   \\
   {}^{\mathllap{u}}\downarrow 
     && \downarrow^{\mathrlap{w}} && \downarrow^{\mathrlap{v}} 
   \\
    K & \underset{k}{\to} & E& \underset{p}{\to} & B
   }
$$

where 

* $p$ and $q$ are [[split epimorphism]]s 

* and $l$ and $k$ are their [[kernel]]s, 

then if $u$ and $v$ are [[isomorphism]]s so is $w$.

=--

To see that the second list of axioms implies the existence of finite limits, observe that the pullback
$$\array{P & \to & A\\
  \downarrow && \downarrow^f\\
  B& \underset{g}{\to} & C}$$
can be computed as the pullback
$$\array{P & \to & A\times B\\
  \downarrow && \downarrow^{(1,1,f)}\\
  A\times B& \underset{(1,1,g)}{\to} & A\times B\times C}$$
in which both legs are split monics.  Filling in one of the equivalent definitions of Barr-exactness, the equivalence of the two lists of axioms reduces to showing that in a Barr-exact category with coproducts and a zero object, protomodularity is equivalent to the Split Short Five Lemma; see the paper referenced below for a proof.




## Examples


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

* The categories of [[crossed module|crossed modules]], [[crossed complex]]es, and their friends are semi-abelian; see example 4.2.6 of the Van der Linden paper referenced below.

* the category of cocommutative Hopf algebras over a field. Was proven in papers by Gran/Kadjo/Vercruysse and Gran/Sterck/Vercruyse

## Properties

### General

(...)


### Dold--Kan correspondence

* The analogue of a [[Dold–Kan correspondence]] holds for [[simplicial object]]s in semi-abelian categories.



## References

* [[George Janelidze]], L&aacute;szl&oacute; M&aacute;rki, [[Walter Tholen]], _Semi-abelian categories_, J. Pure Appl. Alg. __168__, 2-3 (2002) 367-386, <a href="http://dx.doi.org/10.1016/S0022-4049(01)00103-7">doi</a>

* [[Dominique Bourn]], [[Francis Borceux]], [[Mal'cev, protomodular, homological and semi-abelian categories]], Kluwer 2004.

* Dominique Bourn, [[Maria Manuel Clementino]], _Categorical and topological aspects of semi-abelian theories_ , lecture notes Haute Bodeux 2007. ([pdf](http://www.math.yorku.ca/~tholen/HB07BournClementino.pdf))

* [[Tim Van der Linden]], _Homology and homotopy in semi-abelian categories_, [math/0607100](http://arxiv.org/abs/math/0607100).


[[!redirects semi-abelian category]]
[[!redirects semi-abelian categories]]
[[!redirects semiabelian category]]
[[!redirects semiabelian categories]]