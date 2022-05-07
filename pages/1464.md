+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In general, [[limit]]s and [[colimit]]s do not commute.  It is therefore of interest to list the special conditions under which certain limits do commute with certain colimits. 

## Definition

Let $C$ and $D$ be (usually [[small category|small]]) categories, and $E$ a category that has both $C$-colimits and $D$-limits.  Then for any functor $F \colon C \times D \to E$, there is a canonical morphism

$$
  \label{FormulaForCommutativityOfLimitsOverColimits}
   colim_C lim_D F 
  \to
   lim_D colim_C F.
$$

We say that **$C$-colimits commute with $D$-limits in $E$** if this is an [[isomorphism]] for all such $F$.  This is equivalent to both of the statements:

* The functor $colim_C : [C,E] \to E$ [[preserved limit|preserves]] (i.e. "commutes with") $D$-limits.
* The functor $lim_D : [D,E] \to E$ preserves $C$-colimits.

## Examples

### Preservation by functor categories and localizations

If $C$-colimits commute with $D$-limits in $E$, then the same is true in any [[functor category]] $[J,E]$, since limits and colimits in the latter are both pointwise in $E$.

Also, if $C$-colimits commute with $D$-limits in $E$, and if $E'$ is a [[reflective subcategory]] of $E$ with a reflector $L$ that preserves $D$-limits, then $C$-colimits also commute with $D$-limits in $E'$.  This follows because the functor $colim_C : [C,E'] \to E'$ factors as the composite $[C,E'] \hookrightarrow [C,E] \xrightarrow{colim_C} E \xrightarrow{L} E'$ in which all three functors preserve $D$-limits.

### Filtered colimits commute with finite limits 
 {#FilteredColimitsCommuteWithFiniteLimits}

In $Set$, [[filtered category|filtered]] colimits commute with finite limits.  In fact, $C$ is a [[filtered category]] *if and only if* $C$-colimits commute with finite limits in $Set$.  More generally, filtered colimits commute with [[L-finite category|L-finite]] limits.

By the above remarks, it follows that filtered colimits commute with finite limits in any [[Grothendieck topos]].

### Sifted colimits commute with finite products
  {#SiftedColimitsCommuteWithFiniteProducts}

Again in [[Set]] (and hence also in any [[Grothendieck topos]]), [[sifted category|sifted colimits]] commute with [[finite products]]. In fact, this is usually taken to be the definition of a [[sifted category]], and then a theorem of [Gabriel-Ulmer 71](sifted+colimit#GabrielUlmer71) characterizes sifted categories as those for which the [[diagonal functor]] $C \to C \times C$ is a [[final functor]].

As a special case, [[categories with finite products are cosifted]].

For more on this see at _[[distributivity of products and colimits]]_.

### Taking orbits under the action of a finite group commutes with cofiltered limits

This means that if $G$ is a finite group, $C$ is a small cofiltered category and $F : C \to G Set$ is a functor, the canonical map

$$ (\lim F)/G \to \lim_{j \in F} (F(j)/G) $$

is an isomorphism. This fact is mentioned by Andr&#233; Joyal in _Foncteurs analytiques et esp&#232;ces de structures_; a proof can be found [here](http://www.matem.unam.mx/~omar/notes/fingrpcomm.html).

### Coproducts commute with connected limits

+-- {: .num_example #CoproductsCommutingWithConnectedLimits}
###### Proposition

Let  $A$ be a [[set]], $C$ a [[connected category]], and $F \colon C\times A \longrightarrow Set$ a [[functor]]. Then the canonical morphism

$$ 
  \underset{a\in A}{\coprod} \underset{\longleftarrow}{\lim}_{c\in C} F(c,a)
    \longrightarrow 
   \underset{\longleftarrow}{\lim}_{c\in C} \coprod_{a\in A}F(c,a) 
$$

is an [[isomorphism]]. This remains true if [[Set]] is replaced by any [[Grothendieck topos]].

=--

More generally, if $\mathbf{H}$ is an [[(∞,1)-topos]], $A$ is an [[n-groupoid]], and $C$ is a small [[(∞,1)-category]] whose [[classifying space]] is [[n-connected]], then $C$-limits commute with $A$-colimits in $\mathbf{H}$. This follows from the fact that the colimit functor $\mathbf{H}^A\to\mathbf{H}$ induces an equivalence of (∞,1)-topoi $\mathbf{H}^A\simeq \mathbf{H}_{/A}$. For example, if $C$ is a [[cofiltered (∞,1)-category]] or even a [[cosifted (∞,1)-category]], then the classifying space of $C$ is weakly contractible and hence $C$-limits commute with $A$-colimits in $\mathbf{H}$ for any [[∞-groupoid]] $A$.

### Classes of limits and sound doctrines

In general, for any class of limits $\Phi$, one may consider the class of all colimits that commute with $\Phi$-limits and dually.  These classes of limits and colimits share many of the properties of the above examples, especially when $\Phi$ is a [[sound doctrine]].

## Relation to stability under base change 
  {#ColimitsStableByBaseChange}

{#BewareThatUniversalColimitsAreNotStrictlySpeakingColimitsCommutingWithPullback} Stability of a colimit under pullback looks informally like a "commutativity" condition between colimits and pullbacks, but it is not actually in general an instance of the general notion of commutativity of limits and colimits, though it is an instance of [[distributivity of limits over colimits]].  See also [[pullback-stable colimit]] for more.

## Related concepts

* [[distributivity of limits over colimits]]
* [[pullback-stable colimit]]

[[!redirects commutativity of limits and colimits]]
[[!redirects commutativity of limits with colimits]]
[[!redirects commutativity of a limit with a colimit]]
[[!redirects commutativity of limits over colimits]]
[[!redirects commutativity of a limit over a colimit]]

[[!redirects commutativity of colimits and limits]]
[[!redirects commutativity of colimits with limits]]
[[!redirects commutativity of a colimit with a limit]]

[[!redirects limits commuting with colimits]]
