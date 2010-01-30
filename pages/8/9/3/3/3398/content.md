# Preservation of limits
* table of contents
{: toc}


## Idea

If $J\colon I \to C$ is a [[diagram]] and $x$ is its [[limit]] in $C$, then we may na&#239;vely say that this limit is _preserved_ by a [[functor]] $F\colon C \to D$ if $F(x)$ is the limit of the [[composite]] diagram $I \overset{J}\to C \overset{F}\to D$.  However, it is not enough to state this at the level of objects; we also need to impose some coherence conditions, preserving the entire universal [[cone]].


## Definitions

Let $J\colon I \to C$ be a [[diagram]] and let $F\colon C \to D$ be a [[functor]].

Recall (see [[limit]]) that a [[cone]] over $J$ in $C$ may be defined as an [[object]] $x$ of $C$ together with a [[natural transformation]] to $J$ from the composite $\const^I_x\colon I \overset{!}\to \mathbf{1} \overset{\{x\}}\to C$, where $\mathbf{1}$ is the [[terminal category]].  Then a [[terminal object]] in the category of these cones (if it exists) is a [[limit]] of $J$ in $C$.  Thus, a limit consists of an object $x$ and a natural transformation $\eta\colon \const^I_x \to J$.

The functor $F$ __preserves__ the limit $(x,\eta)$ if $(F(x),F\cdot\eta)$ is a limit of functor $F \circ J$ in $D$.  (Here, $F\cdot\eta\colon \const^I_{F(x)} \to F \circ J$ is a [[whiskering]].)

Dually, $F$ __preserves__ a [[colimit]] of $J$ if $F^\op\colon C^\op \to D^\op$ preserves it as a limit of $J^\op\colon I\op \to C^\op$.


## Examples

Let $I$ be the [[empty category]], so that a limit of the unique functor $J\colon I \to C$ is a [[terminal object]] $1$.  Then $F$ preserves this terminal object if and only if $F(1)$ is a terminal object of $D$.

Let $I$ be the category $\mathbf{2}$, so that $J$ picks out two objects $a$ and $b$ of $C$ and the limit of $J$ is a [[product]] $a \times b$ of $a$ and $b$.  Note that this product comes equipped with product projections $\pi\colon a \times b \to a$ and $\rho\colon a \times b \to b$.  Then $F$ preserves this product if and only if $F(a \times b)$ is a product of $F(a)$ and $F(b)$ and furthermore the product projections are $F(\pi)$ and $F(\rho)$.

A functor that preserves all small limits in $C$ that exist is __[[continuous functor]]__.  Usually this term is only used when $C$ has all small limits, i.e. is a [[complete category]].


## Preservation of limits that don\'t exist

Sometimes we want to say that a functor $F$ preserves a class of limits without assuming that these limits exist.  We could interpret this to mean that $F$ preserves all those limits in the class that happen to exist, but this might be a very weak condition.

Alternatively, we could use the [[Yoneda lemma]] (assuming that the categories are [[locally small category|locally small]]) to interpret it as saying that the functor $- \otimes F\colon [C^\op,Set] \to [D^\op,Set]$ (the left [[Kan extension]] of the composite $C \to D \hookrightarrow [D^\op,Set]$ along the Yoneda embedding $C\hookrightarrow [C^\op,Set]$) preserves all the relevant limits.  Note that all small limits exist in the [[presheaf category]] $[C^\op,Set]$, and that the Yoneda embedding preserves and reflects all limits.  Therefore, if $C$ and $D$ do have the relevant limits, this condition is equivalent to asking that $F$ preserve them in the ordinary sense.

For example, a [[flat functor]] is one which preserves all finite limits in this generalised sense.

+-- {: .query}
This is still a little vague, but I\'m not certain what is exactly the right way to say it.
=--


[[!redirects preserved limit]]
[[!redirects preserved limits]]
[[!redirects preserves limits]]
[[!redirects preservation of limits]]
[[!redirects preserved colimit]]
[[!redirects preserved colimits]]
[[!redirects preserves colimits]]
[[!redirects preservation of colimits]]
