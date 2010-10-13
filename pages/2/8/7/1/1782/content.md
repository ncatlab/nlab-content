#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

From the [[nPOV]], algebraic K-theory is an an [[(∞,1)-functor]] that sends [[stable (∞,1)-categories]] to [[spectra]] -- their [[K-theory]] spectra.

Traditionally the stable $(\infty,1)$-categories that have been considered are those coming from categories of [[chain complex]]es, and in this sense algebraic K-theory is the study of [[K-theory]] of categories more general than that of (bounded [[chain complex]]es of) [[vector bundle]]s on a [[topological space]], which is the topic of [[topological K-theory]].

In its simple form _algebraic K-theory_ provides tools for computing the [[Grothendieck group]] of suitable categories. In its more refined form it studies the [[K-theory spectrum]] assigned to these categories. Crucuial tools for this go by the name [[Q-construction]] and [[Waldhausen S-construction]].

Types of categories for which a theory of algebraic K-theory exist include notably the notions

* [[Quillen exact category]] 

* [[abelian category]]

* [[Waldhausen category]], 

* [[triangulated category]].

Concrete examples of interest include for instance

* the category of finitely generated [[projective object]]s over a unital $k$-[[associative unital algebra|algebra]], 

* the category of [[coherent sheaf|coherent sheaves]] over a [[noetherian ring|noetherian]] [[scheme]],

* the category of locally free sheaves over a scheme, 

and the like. 

## Details

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

## References 

A reference for classical constructions is

* [[Charles Weibel]], _The K-Book: An introduction to algebraic K-theory_ ([web](http://www.math.rutgers.edu/~weibel/Kbook.html))

The $(\infty,1)$-categorical picture is described in

* [[Andrew Blumberg]], [[David Gepner]], [[Gonzalo Tabuada]], _A universal characterization of higher algebraic K-theory_ ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282)).
