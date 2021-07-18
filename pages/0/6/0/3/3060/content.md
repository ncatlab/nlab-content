#Contents#
* table of contents
{:toc}


##Idea 

According to the usual definition, a [[functor]] $F\colon C \to D$ is __finitary__ if it preserves all [[filtered colimits]].  An important property is that a [[monadic category]] (over [[Set]]) is [[finitary monadic category|finitary]] (in other words, given by a [[Lawvere theory]]) if and only if its [[forgetful functor]] is finitary.

A slightly weaker definition is used in _The [[Joy of Cats]]_; there, $F$ is __finitary__ if it maps every [[directed colimit]] in $C$ to a jointly [[epimorphism|epic]] diagram (but not necessarily a universal one) in $D$.  With this definition, an [[algebraic category]] is [[finitary algebraic category|finitary]] if and only if its [[forgetful functor]] is finitary.  The previous result also holds, since the two definitions are equivalent for monads on [[Set]].

[[!redirects finitary category]]