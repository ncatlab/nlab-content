#Idea#

The concept of _colimit_ is that [[duality|dual]] to a limit:

a colimit of a [[diagram]] is, if it exists, the [[representable functor|co-classifying space]] for morphisms _out_ of that diagram.

We have

* the notion of _colimit_ generalizes the notion of (direct) _sum_;

* the notion of _weighted colimit_ generalizes the notion of _weighted (direct) sum_.

(There are more remarks on this listed at [[nInsights]]).

Sometimes colimits (or some colimits) are called [[inductive limit]]s.


#Definition#

A [[colimit]] in a category $C$ is the same as a [[limit]] in the [[opposite category]], $C^{op}$.

More precisely, for $F : D^{op} \to C^{op}$ a functor, its [[limit]] $\lim F$ is the colimit of 
$F^{op} : D \to C$.


#Examples# 

Here are some important examples of colimits:

* A colimit of the [[diagram|empty diagram]] is an [[initial object]].
* A colimit of a diagram consisting of two (or more) objects is their [[coproduct]].
* A colimit of a [[span]] is a [[pushout]].
* A colimit of two (or more) [[parallel morphisms]] is a [[coequalizer]].

#Weighted colimits#

A [[weighted colimit]] in $C$ is a 
[[weighted limit]] in $C^{op}$.

