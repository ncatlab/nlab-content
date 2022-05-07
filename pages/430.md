
> This entry is about the notion in [[algebra]]. For the different concept of the same name in [[differential geometry]] see at _[[vector field]]_, and for that in [[physics]] see at _[[field (physics)]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Fields
* table of contents
{: toc}



## Definitions

Classically:
 +-- {: .num_defn #classical}
###### Definition

A **field** is a [[commutative ring]] in which every nonzero element has a multiplicative [[inverse]] and $0 \neq 1$ (which may be combined as: an element is invertible if and only if it is nonzero).
=--

Fields are studied in *field theory*, which is a branch of [[commutative algebra]]. 

If we omit the commutativity axiom, then the result is a [[skewfield]] or [[division ring]] (also in some contexts simply called a "field"). For example, the [[free field (algebra)|free field]] of Cohn and Amitsur is in fact noncommutative.  


### Constructive notions
{#constructive}

Fields are (arguably) not a purely [[algebra|algebraic]] notion in that they don\'t form an [[algebraic category]] (see [discussion below](#category)).  For this reason, it should be unsurprising that in [[constructive mathematics]] (including the [[internal logic]] of a [[topos]]) there are different inequivalent ways to define a field.  In this case the classical definition is not usually the best one; for instance, the real numbers do not satisfy it.  There are several potential replacements with their own advantages and disadvantages.

+-- {: .num_defn #discrete}
###### Definition

If we replace "an element is invertible iff it is nonzero" in Definition \ref{classical} by "an element is invertible [[xor]] it equals zero" (which is equivalent in [[classical logic]] but stronger in [[constructive logic]]), then we obtain the notion of **discrete field**.  This condition means that every element is either $0$ or invertible, and it also implies that $0\neq 1$.
=--

Such a field $F$ is 'discrete' in that it decomposes as a coproduct $F = \{0\} \sqcup F^\times$ (where $F^\times$ is the subset of invertible elements).  An advantage is that this is a [[coherent logic|coherent theory]] and hence also a [[geometric theory]]; for this reason [Johnstone](#Johnstone77) calls such fields **geometric fields**.  A disadvantage is that this axiom is not satisfied (constructively) by the ring of [[real numbers]] (however these are defined), although it is satisfied by the ring of [[rational number|rational]] (or even [[algebraic number|algebraic]]) numbers and by the [[finite field]]s as usual.

+-- {: .num_defn #heyting}
###### Definition

If we interpret 'nonzero' in Definition \ref{classical} as a reference to a [[tight apartness relation]], thus defining the apartness relation $\#$ by $x # y$ iff $x - y$ is invertible, then we obtain the notion of **Heyting field**. (As shown [here](/nlab/show/local+ring#internal), the ring operations become strongly extensional functions.)   In addition to $0\# 1$, the condition then means that every element apart from $0$ is invertible.
=--

This is how 'practising' constructive analysts of the Bishop school usually define the simple word 'field'.  An advantage is that the (located Dedekind) [[real numbers]] form a Heyting field, although (for example) the (less located) [[MacNeille real number]]s need not form a Heyting field; another disadvantage is that this is not a coherent axiom and so cannot be [[internalization|internalized]] in as many categories.

+-- {: .num_defn}
###### Definition

If we replace "an element is invertible iff it is nonzero" in Definition \ref{classical} by "an element is noninvertible iff it is zero" (which is equivalent in [[classical logic]] but incomparable in [[constructive logic]]), we obtain the notion of **residue field** (which is not quite the same as the [[residue fields]] of [[algebraic geometry]]).  In addition to $0\neq 1$, this condition means that every noninvertible element (i.e. element $x$ such that $x y\neq 1$ for all $y$) is zero.
=--

An advantage is that even more versions of the [[real numbers]] (including the [[MacNeille real number]]s) form a residue field; disadvantages are that this axiom is not coherent either and that a residue field lacks an [[apartness relation]] (in particular, the MacNeille reals have no apartness).

Every discrete field is also a Heyting field, and every Heyting field is also a residue field. A Heyting or residue field is a discrete field if and only if [[decidable equality|equality is decidable]]; it is in this sense that a discrete field is 'discrete'.

A residue field is a Heyting field if and only if it is a [[local ring]].  Furthermore, the quotient ring (or 'residue ring') of any local ring by its ideal of noninvertible elements is a Heyting field; in particular, it is a [[residue field]].  On the other hand, not every residue field is even a local ring (the MacNeille reals are not), so not every residue field is the residue ring of any local ring.  The name "residue field" comes from the fact that these fields are precisely the residue rings of *weak local rings* (rings in which the noninvertible elements form an ideal).

Counterexamples were remarked above, but to be explicit: The (located Dedekind) [[real numbers]] form a Heyting field which need not be discrete. The [[MacNeille real number]]s form a residue field which need not be Heyting; see section D4.7 of _[[Elephant|Sketches of an Elephant]]_.

The three definitions above do not exhaust the possible constructive notions of field.  For instance, in [MRR87](#MRR87) the unadorned word **field** is defined like a Heyting field above, but with $\#$ being an arbitrary [[inequality relation]] rather than a tight apartness.  If the inequality is the [[denial inequality]], this reproduces the original classical definition, which in [Johnstone77](#Johnstone77) is called a **field of fractions** since they are precisely the fields of fractions of "weak [[integral domains]]" (defined as rings in which the product of two nonzero elements is nonzero).  In [MRR87](#MRR87) a **denial field** is defined to be a Heyting field with respect to the [[denial inequality]] in which additionally $(0)$ is a [[prime ideal]].


## Properties

### Category of fields
{#category}

Fields are not as well-behaved [[category theory|categorically]] as most other common algebraic structures ([[groups]], [[rings]], [[modules]], etc.).  In particular, the [[category]] of fields and field [[homomorphisms]] (a [[full subcategory]] of the category _[[Rings]]_ of [[rings]] and [[ring homomorphisms]]) is not [[complete category|complete]] or [[cocomplete category|cocomplete]], although it is [[accessible category|accessible]].

In particular, it lacks a [[terminal object]] and also lacks an [[initial object]] (though it has a [[weakly initial set]], namely the set of [[prime fields]], hence has a "[multi-initial object](multi-adjoint#MultiInitialObjectsInFields)").  In particular, it is therefore not [[algebraic category|algebraic]] or [[locally presentable category|locally presentable]].


### Accessibility and sketchability
{#AccSketch}

The [[category]] of fields is [[accessible category|accessible]], even *finitely* accessible, and therefore can be presented as the category of models (in [[Set]]) of a mixed limit-colimit [[sketch]].  It is moreover straightforward to write down such a sketch.

We suppose as given to start with a [[limit sketch]] whose models are [[commutative rings]], with $F$ denoting the ring.  We can construct via limit constructions a subobject $I\hookrightarrow F$ consisting of the invertible elements, as the equalizer of the two maps
$$ F \times F \;\rightrightarrows\; F,$$
the first being given by multiplication and the second by the composite $F\times F \to * \overset{1}{\to} F$, where $*$ is terminal and the map labeled "1" picks out the element $1\in F$.  We now assert that if we take the pullback
$$\array{P & \overset{}{\to} & * \\
  \downarrow && \downarrow^0\\
  I& \hookrightarrow & F,}$$
where the map labeled "0" picks out the element $0\in F$, then the object $P$ is initial (i.e. $0$ is not invertible, or equivalently not equal to $1$), and moreover the pullback is also a pushout (i.e. every element of $F$ is either $0$ or invertible).  Of course, in making these last two assertions we use the fact that we are allowing ourselves a limit-colimit sketch instead of just a limit sketch.

Note that this gives us the notion of *discrete* field (see the [constructive definitions](#constructive) above).  The other constructive notions of field can also be described as models for different limit-colimit sketches.


## Examples
 {#Examples}

+-- {: .num_example}
###### Example

There are the fields of:

* [[rational numbers]],

* (all) [[algebraic numbers]], (Kontsevich-Zagier) [[period]]s

* [[real numbers]],

* [[complex numbers]],

* [[p-adic numbers]] (for $p$ a [[prime number]]).

Other examples

* [[finite field]]s $\mathbf{F}_{p^n}$ where $p$ is a prime

* algebraic [[number field]]s -- finite degree extensions of the field of rational numbers

* [[function field]]s

=--

+-- {: .num_example}
###### Example

The canonical  [[ring object|local ring object]] of the [[Zariski site|gros Zariski topos]] of any [[scheme]] (given by $S \mapsto \Gamma(S, \mathcal{O}_S)$, that is to say, the affine line $\mathbb{A}^{1}_{S}$) is in fact moreover a field object, where the latter is defined by requiring that Definition \ref{classical} holds in the internal logic of this topos. For a proof, see Proposition 2.2 in the article [Universal projective geometry via topos theory](http://www.sciencedirect.com/science/article/pii/0022404976900025) of Anders Kock. The ring $\mathcal{O}_X$ (the [[structure sheaf]]) in the [[category of sheaves|sheaf topos]] (i.e. the petit Zariski topos) is a [[residue field]] if $X$ is a [[reduced scheme|reduced]] scheme.

=--

## Related concepts

* [[division ring]] 

* [[subfield]]

* [[ring]]

* [[finite field]], [[field with one element]]

* [[residue field]]

* [[global field]] 

  * [[number field]]

  * [[function field]] (over a finite field)

* [[positive characteristic]]

* [[topological field]]

* [[graded field]]

* [[model theory of fields]]

* [[infinity-field]]

## References

* {#MRR87} Ray Mines, [[Fred Richman]], Wim Ruitenburg,  _A course in constructive algebra_, Universitext, Springer, 1987.

* {#Elephant} [[Peter Johnstone]], [[Sketches of an Elephant]], Part D.  The [[classifying topos]] for fields is discussed in section D3.1.11(b).
 
* {#Johnstone77} [[Peter Johnstone]], *Rings, Fields, and Spectra*, Journal of Algebra **49** (1977) 238-260 [doi](https://doi.org/10.1016/0021-8693%2877%2990284-8)
 
* [[Olivia Caramello]], [[Peter Johnstone]], _De Morgan's law and the theory of fields_ ([arXiv:0808.1972](http://arxiv.org/abs/0808.1972))


[[!redirects field]]
[[!redirects fields]]

[[!redirects discrete field]]
[[!redirects discrete fields]]

[[!redirects Heyting field]]
[[!redirects Heyting fields]]
[[!redirects heyting field]]
[[!redirects heyting fields]]