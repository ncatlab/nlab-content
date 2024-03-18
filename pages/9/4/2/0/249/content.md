
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[functor]] $F \colon C \to D$ is __pseudomonic__ if it is:

1. [[faithful functor|faithful]]; that is, for any [[pair]] of [[objects]] $x,y\in C$ the component [[function]] $F \colon Hom_C(x,y) \to Hom_D(F x,F y)$ between [[hom-sets]] is [[injective function|injective]],

2. _[[full functor|full]] on [[isomorphisms]]_, meaning that for any [[pair]] of [[objects]] $x,y\in C$ the [[function]] $F \colon Iso_C(x,y) \to Iso_D(F x, F y)$ betwee the [[subsets]] of [[isomorphisms]] is [[surjective]] (hence [[bijective]]).

Arguably, pseudomonic functors are precisely the functors for which it makes sense to say that $A$ is uniquely determined by $F A$ up to unique isomorphism.  However, we do not really need faithfulness for this; bijectivity on isos suffices.

More generally, a [[1-morphism]] $f \colon C\to D$ in any [[2-category]] $K$ is called a **[[pseudomonic morphism]]** if the square analogous to that below is a [[2-pullback]], or equivalently if $K(X,C)\to K(X,D)$ is a pseudomonic functor for any $X$.  


## Properties


Every [[fully faithful functor]] is pseudomonic, and every pseudomonic functor is [[conservative functor|conservative]], as well as [[essentially injective]].

A functor $F \colon C \to D$ is pseudomonic if and only if the [[commuting square]]

$$
  \array{ 
    C &\overset{Id}{\longrightarrow}& C
    \\
    \Big\downarrow\mathrlap{^{Id}}
    &&
    \Big\downarrow\mathrlap{{}^F}
    \\
    C &\underset{F}{\longrightarrow}& D
  }
$$

is a [[2-pullback]] in [[Cat]] (cf. the pullback characterization of 1-[[monomorphisms]], [here](monomorphism#BasicCharacterizationOfMonomorphisms)).

## Examples

An interesting example of the notion appears in the context of Joyal's [[combinatorial species]] of structures.

A *[[combinatorial species]]* is a [[functor]] from the [[category]] $Bij$ of [[finite sets]] and [[bijections]] between them to [[Set]], and the functors that are obtained by taking [[left Kan extensions]] of species along the [[subcategory]]-inclusion $I \colon Bij \to Set$ are called _analytic functors_. Now taking left Kan extensions along $I$ is pseudomonic, and this implies that the [[coefficients]] of an analytic functor are unique up to isomorphism.


## References

* [[Aurelio Carboni]], [[Scott Johnson]], [[Ross Street]], [[Dominic Verity]], §2.7 in: *Modulated bicategories*, Journal of Pure and Applied Algebra **94** (1994) 229-282 &lbrack;<a href="https://doi.org/10.1016/0022-4049(94)90009-4">doi:10.1016/0022-4049(94)90009-4</a>, [pdf](https://core.ac.uk/download/pdf/82129658.pdf)&rbrack;

* [[G. Max Kelly]], [[Steve Lack]], p. 18 of: _On property-like structures_, [[Theory and Applications of Categories]] **3** 9 (1997) &lbrack;[tac:3-09](http://www.tac.mta.ca/tac/volumes/1997/n9/3-09abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/1997/n9/n9.pdf)&rbrack;

Formalization in [[cubical Agda]]:

* [[1lab]], *[Pseudomonic Functors](https://1lab.dev/Cat.Functor.Properties.html#pseudomonic-functors)*



[[!redirects pseudomonic functors]]
[[!redirects pseudomonic]]
