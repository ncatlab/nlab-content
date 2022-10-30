
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Idea

Algebraic K-theory was initially a body of theory that attempted to generalise parts of linear algebra, notably the theory of dimension of vector spaces, and determinants,to modules over arbitrary rings. It has grown into a well developed tool for studying a wide range of algebraic, geometric and even analytic situations from a variety of points of view. It is thus difficult to give a single *idea* of what the subject is about.  It has a side that looks at the manipulation and [[rewriting]] of the elementary operations of linear algebra, but also a definite infinity category aspect. Its development uses a lot of algebraic topology, particularly homotopy theory, both stable homotopy theory and the more simplicial parts of that area, and more recently has interacted with infinity category theory in various forms.

Some idea of its history is given in [[Algebraic K-theory, a historical perspective]]. A brief summary of the topics that are subsumed under the title of Algebraic K-theory can be gleaned from the list of subtopic pages and sections listed below:

* [[Algebraic K-theory, a historical perspective]] (Whitehead and Grothendieck);

* [[Milnor's $K_2$]]([[Steinberg group]],[[universal central extension]])

* [[Higher algebraic $K$-theory]] [[Quillen exact category]], [[Quillen's plus construction]], [[Volodin spaces]];

* Links with other areas: [[The algebraic K-theory of spaces]]([[Waldhausen S-construction]]), [[topological cyclic homology]], [[algebraic K-theory of operator algebras]], ...

##More recent history and the nPOV.

From the most recent [[nPOV]], algebraic K-theory is an [[(∞,1)-functor]] that sends [[stable (∞,1)-categories]] to certain [[spectra]] -- their [[K-theory]] spectra -- characterized roughly speaking as the universal finitary Morita invariant of stable (∞,1)-categories under which all exact sequences of stable (∞,1)-categories split. 

Traditionally the stable $(\infty,1)$-categories that have been considered are those coming from categories of [[chain complex]]es, and in this sense algebraic K-theory is the study of [[K-theory]] of categories more general than that of (bounded [[chain complex]]es of) [[vector bundle]]s on a [[topological space]], which is the topic of [[topological K-theory]].

In its simplest initial form _algebraic K-theory_ provides tools for computing the [[Grothendieck group]] of suitable categories. In its more refined form it studies the [[K-theory spectrum]] assigned to these categories. Crucial tools for this include the  [[Q-construction]] and [[Waldhausen S-construction]].

Types of categories for which a theory of algebraic K-theory exist include notably the notions

* [[Quillen exact category]], 

* [[abelian category]],

* [[Waldhausen category]], 

* [[triangulated category]].

Concrete examples of interest include for instance


* the category of finitely generated [[projective object]]s over a unital $k$-[[associative unital algebra|algebra]], 

* the category of [[coherent sheaf|coherent sheaves]] over a [[noetherian ring|noetherian]] [[scheme]],

* the category of locally free sheaves over a scheme, 

and the like. 

## More Details

There is a universal characterization of the construction of the K-theory spectrum $K(A)$ of a stable $(\infty,1)$-category $A$:

there is an $(\infty,1)$-functor

$$
  U : (\infty,1)StabCat \to N
$$

to a stable $(\infty,1)$-category which is universal with the property that it respects colimits and exact sequences in a suitable way. Given any stable $(\infty,1)$-category $A$, its (connective or non-connective, depending on details) algebraic K-theory spectrum is the hom-object

$$
  K(A) \simeq Hom(U(Sp), U(A))
  \,,
$$

where $Sp$ denotes the stable $(\infty,1)$-category of compact [[spectra]]. (See the references below.)






When one talks about the algebraic $K$-theory of [[ring]]s, one means the algebraic $K$-theory of the corresponding category of (one-sided) finitely-generated projective [[module]]s.

A K-theory should be given by a sequence of [[functor]]s $K_i$ from some class of categories as above to [[abelian group]]s having some similarity to [[derived functor]]s and [[cohomology]] theory for spaces. $K_0$ and $K_1$ are rather classical objects from the 1950s; higher $K$-groups are defined by Quillen in two steps: to a [[Quillen exact category]] $C$ one first associates a $K$-theory space $\mathcal{K}(C)$ (or in better versions, a $K$-theory [[spectrum]]) and then defines $K$-groups as [[homotopy group]]s of that space:
$$K_i(C)=\pi_i(\mathcal{K}(C)).$$  

The $K$-theory space of $C$ in Quillen's version was obtained as a [[classifying space]] of the Quillen $Q$-construction applied to $C$. The $Q$-construction has been refined to more sophisticated [[delooping]] methods by Waldhausen, Karoubi and others.

## Properties

### Red-shift conjecture

* [[red-shift conjecture]]

[[!include chromatic tower examples - table]]


## Related concepts

* [[Beilinson regulator]]

* [[differential algebraic K-theory]]

* [[non-connective algebraic K-theory]]

* [[K-theory of a permutative category]]

* [[K-theory of a bipermutative category]]

* [[bivariant algebraic K-theory]]

* [[K-motive]]

* [[red-shift conjecture]]


[[!include noncommutative motives - table]]


## References 

A reference for classical constructions is

* [[Charles Weibel]], _The K-Book: An introduction to algebraic K-theory_ ([web](http://www.math.rutgers.edu/~weibel/Kbook.html))
 {#Weibel}

The [[(infinity,1)-category theory]] picture is discussed in

* [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _A universal characterization of higher algebraic K-theory_ ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282)).
 {#BlumbergGepnerTabuada}

(in terms of [[noncommutative motives]]) and in

* [[Clark Barwick]], _On the algebraic K-theory of higher categories, I. The universal property of Waldhausen K-theory_ ([arXiv:1204.3607](http://de.arxiv.org/abs/1204.3607))

For discussion of stable phenomena in algebraic K-theory, see section 4 of 

* [[Ralph Cohen]], _Stability phenomena in the topology of moduli spaces_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0908/0908.1938v2.pdf))
 {#Cohen}