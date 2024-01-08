
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

A [[functor]] $F: C \to D$ is __pseudomonic__ if

1. it is [[faithful functor|faithful]]; that is, for any [[pair]] of [[objects]] $x,y\in C$ the component [[function]] $F \colon C(x,y) \to D(F x,F y)$ between [[hom-sets]] is injective, and

2. it is _full on isomorphisms_, meaning that for any [[pair]] of [[objects]] $x,y\in C$ the [[function]] $F \colon Iso_C(x,y) \to Iso_D(F x, F y)$ to the [[set]] of [[isomorphisms]] between them is [[surjective]] (hence [[bijective]]), where $Iso_C(x,y)$.

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

Arguably, pseudomonic functors are precisely the functors for which it makes sense to say that $A$ is uniquely determined by $F A$ up to unique isomorphism.  However, we do not really need faithfulness for this; bijectivity on isos suffices.

## References

Formalization in [[cubical Agda]]:

* [[1lab]], *[Pseudomonic Functors](https://1lab.dev/Cat.Functor.Properties.html#pseudomonic-functors)*



[[!redirects pseudomonic functors]]
[[!redirects pseudomonic]]
