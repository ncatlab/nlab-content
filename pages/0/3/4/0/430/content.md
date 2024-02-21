
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

## Idea

A field is a mathematical structure with the usual arithmetic operations of [[addition]], [[subtraction]], [[multiplication]], and [[division]] of non-zero elements. 

The original concept of a field was developed by [[Gustav Lejeune Dirichlet]] and [[Richard Dedekind]] in 1871 under the name "body" (Körper in German), and referred solely to [[subfields]] of the [[complex numbers]] (cf. [Dirichlet & Dedekind 1871](#DirichletDedekind71)). Later in 1893 [[Heinrich Weber]] generalized the notion of field to today's definition of field as an arbitrary [[commutative ring|commutative]] [[division ring]] (cf. [Weber 1893](#Weber93)). The word "field" itself in the English language was coined by [[E. Hastings Moore]] in 1893 (cf. [Moore 1893](#Moore93)) to refer to the algebraic structure. 

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

Fields are (arguably) not a purely [[algebra|algebraic]] notion in that they don\'t form an [[algebraic category]] (see [discussion below](#category)).  For this reason, it should be unsurprising that in [[constructive mathematics]] (including the [[internal logic]] of a [[topos]]) there are different inequivalent ways to define a field.  In this case the classical definition is not usually the best one; for instance, the real numbers do not satisfy it.  There are several potential replacements with their own advantages and disadvantages. These include: 

* [[discrete field]]
* [[Heyting field]]
* [[weak Heyting field]]
* [[Kock field]]
* [[local ring]]
* [[weak local ring]]

\begin{definition}\label{discrete}
If we replace "an element is invertible iff it is nonzero" in Definition \ref{classical} by "an element is invertible [[xor]] it equals zero" (which is equivalent in [[classical logic]] but stronger in [[constructive logic]]), then we obtain the notion of **discrete field**.  This condition means that every element is either $0$ or invertible, and it also implies that $0\neq 1$.
\end{definition}

Such a field $F$ is 'discrete' in that it decomposes as a coproduct $F = \{0\} \sqcup F^\times$ (where $F^\times$ is the subset of invertible elements).  An advantage is that this is a [[coherent logic|coherent theory]] and hence also a [[geometric theory]]; for this reason [Johnstone](#Johnstone77) calls such fields **geometric fields**.  A disadvantage is that this axiom is not satisfied (constructively) by the ring of [[real numbers]] (however these are defined), although it is satisfied by the ring of [[rational number|rational]] (or even [[algebraic number|algebraic]]) numbers and by the [[finite field]]s as usual.

\begin{definition}\label{heyting}
If we interpret 'nonzero' in Definition \ref{classical} as a reference to a [[tight apartness relation]], thus defining the apartness relation $\#$ by $x # y$ iff $x - y$ is invertible, then we obtain the notion of **[[Heyting field]]**. (As shown [here](/nlab/show/local+ring#internal), the ring operations become strongly extensional functions.)   In addition to $0\# 1$, the condition then means that every element apart from $0$ is invertible.
\end{definition}

This is how 'practising' constructive analysts of the Bishop school usually define the simple word 'field'.  An advantage is that the (located Dedekind) [[real numbers]] form a Heyting field, although (for example) the (less located) [[MacNeille real number]]s need not form a Heyting field; another disadvantage is that this is not a coherent axiom and so cannot be [[internalization|internalized]] in as many categories.

\begin{definition}
If we replace "an element is invertible iff it is nonzero" in Definition \ref{classical} by "an element is noninvertible iff it is zero" (which is equivalent in [[classical logic]] but incomparable in [[constructive logic]]), we obtain the notion of **[[weak Heyting field]]** (cf. [Richman (2020)](#Richman20)) or **[[Johnstone residue field]]** (cf. [Johnstone (1977)](#Johnstone77)), which is not quite the same as the [[residue fields]] of [[algebraic geometry]]). In addition to $0\neq 1$, this condition means that every noninvertible element (i.e. element $x$ such that $x y\neq 1$ for all $y$) is zero.
\end{definition}

An advantage is that even more versions of the [[real numbers]] (including the [[MacNeille real number]]s) form a weak Heyting field; disadvantages are that this axiom is not coherent either and that a residue field lacks an [[apartness relation]] (in particular, the MacNeille reals have no apartness). Another example of a weak Heyting field include the set of [[Laurent series]] of [[real numbers]]. 

Every discrete field is also a Heyting field, and every Heyting field is also a weak Heyting field. A Heyting field is a discrete field if and only if [[decidable equality|equality is decidable]]; it is in this sense that a discrete field is 'discrete'. It is not true that every weak Heyting field with decidable equality is Heyting. See [this proof](https://ncatlab.org/nlab/show/Heyting+field#Weak+Heyting+fields) for details. 

A weak Heyting field is a Heyting field if and only if it is a [[local ring]].  Furthermore, the quotient ring (or 'residue ring') of any local ring by its ideal of noninvertible elements is a Heyting field; in particular, it is a [[residue field]].  On the other hand, not every weak Heyting field is even a local ring (the MacNeille reals are not), so not every residue field is the residue ring of any local ring. The name "residue field" as defined in [Johnstone (1977)](#Johnstone77) comes from the fact that these fields are precisely the residue rings of *weak local rings* (rings in which the noninvertible elements form an ideal).

Counterexamples were remarked above, but to be explicit: The (located Dedekind) [[real numbers]] form a Heyting field which need not be discrete. The [[MacNeille real number]]s form a weak Heyting field which need not be Heyting; see section D4.7 of _[[Elephant|Sketches of an Elephant]]_. 

The three definitions above do not exhaust the possible constructive notions of field.  For instance, in [MRR87](#MRR87) the unadorned word **field** is defined like a Heyting field above, but with $\#$ being an arbitrary [[inequality relation]] rather than a tight apartness.  If the inequality is the [[denial inequality]], this reproduces the original classical definition, which in [Johnstone77](#Johnstone77) is called a **field of fractions** since they are precisely the fields of fractions of "weak [[integral domains]]" (defined as rings in which the product of two nonzero elements is nonzero).  In [MRR87](#MRR87) a **denial field** is defined to be a Heyting field with respect to the [[denial inequality]] in which additionally $(0)$ is a [[prime ideal]].


\begin{remark}\label{TrivialRingAsAField}
In [LombardiQuitté2010](#LombardiQuitté2010), the authors' definitions of discrete field and Heyting field do not include the non-equational axiom $1 \neq 0$ or $1 \# 0$ respectively. With such a definition, the [[trivial ring]] counts as a discrete field as well as a Heyting field and constitutes the [[terminal object]] in the [[category|categories]] of such fields.
\end{remark}


## Properties

### Category of fields
{#category}

Fields are not as well-behaved [[category theory|categorically]] as most other common algebraic structures ([[groups]], [[rings]], [[modules]], etc.).  In particular, [[Field]], the [[category]] of fields and field [[homomorphisms]] (a [[full subcategory]] of the category _[[Rings]]_ of [[rings]] and [[ring homomorphisms]]) is not [[complete category|complete]] or [[cocomplete category|cocomplete]], although it is [[accessible category|accessible]].

In particular, it lacks a [[terminal object]] and also lacks an [[initial object]] (though it has a [[weakly initial set]], namely the set of [[prime fields]], hence has a "[multi-initial object](multi-adjoint#MultiInitialObjectsInFields)").  In particular, it is therefore not [[algebraic category|algebraic]] or [[locally presentable category|locally presentable]].


### Accessibility and sketchability
{#AccSketch}

[[Field]] is [[accessible category|accessible]], even *finitely* accessible, and therefore can be presented as the category of models (in [[Set]]) of a mixed limit-colimit [[sketch]].  It is moreover straightforward to write down such a sketch.

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

* [[prefield ring]]

* [[reciprocal ring]]

* [[division ring]], [[division monoid]]

* [[subfield]]

* [[ring]]

* [[finite field]], [[field with one element]]

* [[possibly trivial field]]

* [[residue field]]

* [[global field]] 

  * [[number field]]

  * [[function field]] (over a finite field)

* [[positive characteristic]]

* [[topological field]]

* [[graded field]]

* [[model theory of fields]]

* [[infinity-field]]

* [[Kock field]]

| [[commutative ring]] | [[reduced ring]] | [[integral domain]] |
---------------------|-----------------|-----------------|
| [[local ring]] | [[reduced local ring]] | [[local integral domain]] |
| [[Artinian ring]] | [[semisimple ring]] | [[field]] |
| [[Weil ring]] | [[field]] | [[field]] |

## References

* {#DirichletDedekind71} [[Gustav Lejeune Dirichlet]] (1871), [[Richard Dedekind]] (ed.), Vorlesungen über Zahlentheorie (Lectures on Number Theory) (in German), vol. 1 (2nd ed.), Braunschweig, Germany: Friedrich Vieweg und Sohn ([Google Books](https://books.google.com/books?id=SRJTAAAAcAAJ&pg=PA424))

* {#Weber93} [[Heinrich Weber]] (1893), "Die allgemeinen Grundlagen der Galois'schen Gleichungstheorie", Mathematische Annalen (in German), 43 (4): 521–549, $[$[doi:10.1007/BF01446451](https://doi.org/10.1007%2FBF01446451), [ISSN:0025-5831](https://www.worldcat.org/issn/0025-5831), [JFM:25.0137.01](https://zbmath.org/?format=complete&q=an:25.0137.01), [S2CID:120528969](https://api.semanticscholar.org/CorpusID:120528969)$]$

* {#Moore93} [[E. Hastings Moore]] (1893), "A doubly-infinite system of simple groups", Bulletin of the American Mathematical Society, 3 (3): 73–78, $[$[doi:10.1090/S0002-9904-1893-00178-X](https://doi.org/10.1090%2FS0002-9904-1893-00178-X), [MR:1557275](https://mathscinet.ams.org/mathscinet-getitem?mr=1557275)$]$

* {#MRR87} Ray Mines, [[Fred Richman]], Wim Ruitenburg,  _A course in constructive algebra_, Universitext, Springer, 1987.

* {#Elephant} [[Peter Johnstone]], [[Sketches of an Elephant]], Part D.  The [[classifying topos]] for fields is discussed in section D3.1.11(b).
 
* {#Johnstone77} [[Peter Johnstone]], *Rings, Fields, and Spectra*, Journal of Algebra **49** (1977) 238-260 [doi](https://doi.org/10.1016/0021-8693%2877%2990284-8)
 
* [[Olivia Caramello]], [[Peter Johnstone]], _De Morgan's law and the theory of fields_ ([arXiv:0808.1972](http://arxiv.org/abs/0808.1972))

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* {#Richman20} [[Fred Richman]], *Laurent series over $\mathbb{R}$*. Communications in Algebra, Volume 48, Issue 5, 11 Jan 2020 Pages 1982-1984 &lbrack;[doi:10.1080/00927872.2019.1710166](https://doi.org/10.1080/00927872.2019.1710166)&rbrack;

Discussion in [[univalent foundations of mathematics]] ([[homotopy type theory]]):

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]]: Chapter 8 of: *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$

[[!redirects field]]
[[!redirects fields]]

[[!redirects discrete field]]
[[!redirects discrete fields]]