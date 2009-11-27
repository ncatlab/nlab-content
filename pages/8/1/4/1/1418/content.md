An object $X$ of a category $C$ is said to be [[finitely presentable object|finitely presentable]] (or finitary, sometimes called [[compact object|compact]]) if the [[representable functor]] $C(X,-)$ preserves [[filtered colimits]]. Write $C_{fp}$ for the full subcategory of $C$ on the finitely presentable objects.

+--{: .query}
[[Mike Shulman|Mike]]: Do people really call finitely presentable _objects_ "finitary"?  I've only seen that word applied to functors (those that preserve filtered colimits).
=--

A category $C$ satisfying (any of) the following equivalent conditions is said to be __locally finitely presentable__ (or **lfp**):

1. $C$ has all small [[colimit|colimits]], the category $C_{fp}$ is [[essentially small category|essentially small]], and any object in $C$ is a [[filtered colimit]] of the canonical diagram of finitely presentable objects mapping into it.
1. $C$ is the category of models for a finitary [[essentially algebraic theory]].
   +-- {: .query}
   Does this essentially algebraic theory also have to be finitary?; that is, if it\'s an [[algebraic theory]], then it\'s a [[Lawvere theory]]?  ---Toby

   [[Mike Shulman|Mike]]: Yes, it certainly has to be finitary.  Possibly the standard meaning of "essentially algebraic" implies finitarity, though, I don't know.

   _Toby_:  I wouldn\'t use 'algebraic' that way; see [[algebraic theory]].
   =--
1. $C$ is equivalent to the category of finite-limit-preserving functors $D \to Set$ for some small category $D$ with finite limits.
1. $C_{fp}$ has finite colimits, and the restricted [[Yoneda embedding]] $C\hookrightarrow [C_{fp}^{op},Set]$ identifies $C$ with the category of finite-limit-preserving functors $C_{fp}^{op} \to Set$.
1. $C$ is the category of models for a finite limit [[sketch]].

Replacing "finite" by "of cardinality less than $\kappa$" everywhere, for some [[cardinal number]] $\kappa$, results in the notion of a [[locally presentable category]].

###Examples###

* [[Set]], Graph, [[Pos]], [[Cat]], [[Ab]] are all lfp.

* [[Top]], [[FinSet]] are not lfp.

[[!redirects locally finitely presentable categories]]
